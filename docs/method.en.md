# Method

[Русская версия](method.md)

## 1. Sources and normalization

- The registry includes required sources from the organizers' dataset: websites and Telegram channels. Additional sources can be added. For each website, the system checks for RSS/Atom once; if no feed exists, it parses HTML.
- A publication records its source, URL, title, text, timestamp (“published” or “discovered”), version, CVEs, and bulletin IDs. An edit creates a new version instead of overwriting the old one.
- A failure in one source is logged without stopping the others.

## 2. Classification

Each publication is assigned a primary topic, all applicable topics, event type, vendors, products, and versions found literally in the text.

- **Hybrid mode.** The local TF-IDF and logistic regression classifier decides on its own only when confidence is at least 0.72 and each predicted class has at least 30 training examples. Other cases go to the LLM.
- **LLM answers as weak labels.** The classifier learns from LLM answers; experts have not verified those labels.

## 3. Fact extraction

The model returns:

- 1–6 short claims in Russian, each with a verbatim source quotation of up to 300 characters;
- importance signals such as exploitation in the wild, a public exploit, ransomware, a breach, end of support, and unauthenticated remote exploitation;
- affected and fixed version ranges;
- an event date if the text provides one.

Validation checks that:

- the response matches the JSON schema and its `item_id` matches;
- claims contain no CVEs absent from the publication and no invented URLs;
- each quotation occurs in the normalized source text;
- the quotation supports the reported date and versions.

Text that is too short is marked “insufficient content” instead of being completed by guesswork.

## 4. Events and importance

- Reports about one CVE or event are merged, retaining all sources and updates.
- Importance also considers verified signals: CVSS computed from the vector, presence in CISA KEV, and exploitation.
- Applicability compares affected versions with the inventory: affected, unaffected, or unknown. A PoC mention is not treated as proof of an attack; a victim's country is not inferred from an incidental country mention.

## 5. Interest-based selection

- **Technical profile:** topic weights for vulnerabilities, exploitation, incidents, industrial security, and other topics; watched product classes such as perimeter/VPN, mail, remote access, and hypervisors; five full P1 cards, with the rest compact.
- **Management profile:** 12 signals from the dataset, including geography, major losses, critical infrastructure, energy, industry, breaches, and government. Their weights are added and thresholds produce high, medium, or low importance.
- **Changing interests or inventory** recalculates selection without new LLM requests. In the synthetic example, updating FortiOS in the inventory moves related events from P1 to P3.

## 6. Issue

- The daily issue is scheduled for 08:00 Moscow time; the monthly issue is produced on the first working day for the previous month.
- Structure: “Highlights” → sections → cards (priority, applicability, claims, quotations, sources) → “Additional items” → selection funnel.
- A published issue is immutable; changes are checked through a preview.
