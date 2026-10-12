# Research notes

[Русская версия](research.md)

Data: the prototype's working corpus, October 2–4, 2026. LLM answers, not expert annotations, are the reference labels.

## 1. Where time is spent

Overnight labeling run: 577 publications, 1,361 model requests across two passes.

| Stage | Time | Share |
|---|---|---|
| Waiting for the LLM | 301.7 of 301.8 minutes (first pass) | 99.97% |
| Validation, JSON handling, and SQLite writes between requests | ~0.01 seconds per request | < 0.1% |
| Corpus snapshot | ~6.5 seconds | — |
| Issue assembly | ~2 seconds | — |
| Polling one source | 0.4–1 seconds | — |

Why the LLM stage is slow:

1. **Requests are sequential:** classification and extraction for each publication.
2. **Latency follows output length:** correlation with output tokens is 0.76, versus 0.39 for input tokens. Model throughput is ~110–140 tokens per second.
   - The median classification answer is ~1,400 tokens, although only a short JSON result is needed.
   - The median extraction answer is ~2,900 tokens.
3. **Most input is overhead.** Median publication text is 192 characters, while the input is ~3,000 tokens of system prompt and JSON schema.
4. **101 of 560 extraction requests returned “insufficient content.”** Each took about 20 seconds.

**Estimate:** time ≈ number of new publications × ~42 seconds + ~10 seconds.

| Scenario | Time |
|---|---|
| Daily issue with 1–5 new publications | 1–4 minutes |
| Monthly issue after daily runs, with everything cached | Seconds |
| Initial load of 577 archived publications | ~6.7 hours |

Ways to reduce the delay:

- analyze only new publications;
- run requests in parallel;
- reject very short texts before calling the model;
- request extraction only for issue candidates, as hybrid mode does.

## 2. Rules, local classifier, and LLM

Comparison with LLM answers on 577 publications.

| Method | Primary topic: accuracy / macro-F1 | Event type: accuracy / macro-F1 |
|---|---|---|
| Most frequent class | 0.42 | 0.41 |
| Dictionary rules | 0.28 / 0.13 | 0.04 / 0.04 |
| TF-IDF + logistic regression, five-fold CV | **0.77 / 0.54** | **0.82 / 0.70** |

- **Rules** performed much worse and would have sent only half as many publications onward as the LLM. The main cause was poor coverage of Russian-language industrial security text.
- **Classifier** matched the LLM well on large classes (vulnerabilities: F1 0.94; product releases: 0.86) but struggled with classes having only 10–16 examples. Training and labeling the full corpus took ~5–7 seconds versus ~2.5 hours for the LLM.

## 3. Transfer across sources

Three categories from the dataset (“Attack,” “Vulnerability,” “Information”); 896 publications from 32 sources; five splits.

| Model | Macro-F1, event split | Macro-F1, source split |
|---|---|---|
| TF-IDF → logistic regression | 0.830 | 0.274 |
| TF-IDF → LinearSVC | 0.823 | 0.274 |
| Multilingual MiniLM → logistic regression | 0.764 | 0.399 |

An event split makes the classifier look strong. On sources absent from training, TF-IDF nearly loses the “Attack” and “Vulnerability” categories. The encoder transfers better but needs ~1.4 GB of RAM and is still not reliable enough to decide alone.

**Conclusion:** the local model saves requests on common, confident cases; the LLM and verifiable rules remain the fallback.

## 4. Robustness of quotation validation

The first version rejected an entire publication when one quotation could not be verified, even if 3–4 of its 4–5 quotations matched. After switching to partial rejection, all eight publications rejected for that reason in a 40-publication test corpus passed with verified claims. Failed quotations are logged for review.
