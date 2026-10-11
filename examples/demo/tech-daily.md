---
schema_version: "issue_v1"
issue_id: "tech-2026-10-05-3de40545aeca"
audience: "tech"
period: {"start": "2026-10-04T05:00:00+00:00", "end": "2026-10-05T05:00:00+00:00"}
generated_at: "2026-10-05T06:00:00+00:00"
corpus_id: "soc-corpus-0cfa1545b9c4db3745279eba"
mode: "fake"
revisions: {"calendar": {"holidays": [], "timezone": "Europe/Moscow", "weekend_days": [5, 6], "working_dates": []}, "profile": {"id": "tech_daily", "revision": 1, "audience": "tech", "inventory": {"id": "default"}, "topic_weights": {"exploitation": 3, "incidents": 3, "industrial_security": 3, "infrastructure": 1, "malware_campaigns": 2, "patches_releases": 2, "regulation_compliance": 1, "research": 1, "vulnerabilities": 3}, "excluded_primary_topics": ["consumer_tech", "marketing"], "inventory_only": false, "watchlist_families": ["perimeter_vpn", "mail_server", "remote_access", "hypervisor"], "digest_size": 12, "p1_full_cards": 5, "min_interest_fit": 0.3, "min_score": 0.0, "top_events": 8, "schedule": {"time": "08:00", "window": "since_last_issue"}, "language": "ru"}, "inventory": {"id": "default", "revision": 1, "items": [{"vendor": "Fortinet", "product": "FortiOS", "version": "7.4.4", "version_is_branch": false, "aliases": ["FortiGate"], "family": "perimeter_vpn", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}, {"vendor": "Microsoft", "product": "Exchange Server", "version": "2019 CU14", "version_is_branch": false, "aliases": ["MS Exchange", "Exchange"], "family": "mail_server", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}, {"vendor": "VMware", "product": "ESXi", "version": "8.0 U2", "version_is_branch": false, "aliases": [], "family": "hypervisor", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}, {"vendor": "PostgreSQL", "product": "PostgreSQL", "version": "16.3", "version_is_branch": false, "aliases": ["Postgres"], "family": "dbms", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}, {"vendor": "Kubernetes", "product": "Kubernetes", "version": "1.30.2", "version_is_branch": false, "aliases": ["K8s"], "family": "container_platform", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}, {"vendor": "1С", "product": "1С:Предприятие", "version": null, "version_is_branch": false, "aliases": ["1C"], "family": "erp", "criticality": "medium", "ecosystem": null, "cpe": null, "version_scheme": "numeric"}]}, "relevance_model": {"version": null, "active": false, "n_labels": 0, "activation_reason": null}, "alpha": 0, "kev_snapshot": null, "importance_config": "4883ad7ae4d3ca834173b765e81e1eeb4a846fa50d2ffa811957d8eba8821143"}
funnel: {"items": 10, "events": 9, "eligible": 9, "selected": 9, "without_ai": 0}
---

# Ежедневный ИБ-дайджест

Период: 04.10.2026 08:00 — 05.10.2026 08:00 (Europe/Moscow). Событий: 9. Без ИИ-разбора: 0.

## Главное

- В учебном примере раскрыта уязвимость CVE-2099-10006 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [E-ae612dbe346ee7ae2662](#e-ae612dbe346ee7ae2662)
- В учебном примере раскрыта уязвимость CVE-2099-10005 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [E-f0c0d503d89bd75cd794](#e-f0c0d503d89bd75cd794)
- В учебном примере раскрыта уязвимость CVE-2099-10004 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [E-bbe3a44155199b104f76](#e-bbe3a44155199b104f76)
- В учебном примере раскрыта уязвимость CVE-2099-10003 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [E-debe7d548e81d39801b1](#e-debe7d548e81d39801b1)
- В учебном примере раскрыта уязвимость CVE-2099-10002 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [E-bcf770c196ab91c27bd1](#e-bcf770c196ab91c27bd1)

**Разделы:** [Уязвимости](#уязвимости) · [Информация](#информация) · [Атаки](#атаки)

## Уязвимости

<a id="e-ae612dbe346ee7ae2662"></a>
### В учебном примере раскрыта уязвимость CVE-2099-10006 в FortiOS

`P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · CVSS 9.8 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий.

В учебном примере раскрыта уязвимость CVE-2099-10006 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [1](https://example.org/fictional/advisory/6)

Источники: [1 · Учебный источник](https://example.org/fictional/advisory/6)

<details><summary>Цитаты и применимость</summary>

- «Synthetic advisory CVE-2099-10006. FortiOS: \>=7.4.0, \<7.4.5; actively exploited. CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H» [1](https://example.org/fictional/advisory/6)

</details>

<a id="e-f0c0d503d89bd75cd794"></a>
### В учебном примере раскрыта уязвимость CVE-2099-10005 в FortiOS

`P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · CVSS 9.8 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий.

В учебном примере раскрыта уязвимость CVE-2099-10005 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [1](https://example.org/fictional/advisory/5)

Источники: [1 · Учебный источник](https://example.org/fictional/advisory/5)

<details><summary>Цитаты и применимость</summary>

- «Synthetic advisory CVE-2099-10005. FortiOS: \>=7.4.0, \<7.4.5; actively exploited. CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H» [1](https://example.org/fictional/advisory/5)

</details>

<a id="e-bbe3a44155199b104f76"></a>
### В учебном примере раскрыта уязвимость CVE-2099-10004 в FortiOS

`P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · CVSS 9.8 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий.

В учебном примере раскрыта уязвимость CVE-2099-10004 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [1](https://example.org/fictional/advisory/4)

Источники: [1 · Учебный источник](https://example.org/fictional/advisory/4)

<details><summary>Цитаты и применимость</summary>

- «Synthetic advisory CVE-2099-10004. FortiOS: \>=7.4.0, \<7.4.5; actively exploited. CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H» [1](https://example.org/fictional/advisory/4)

</details>

<a id="e-debe7d548e81d39801b1"></a>
### В учебном примере раскрыта уязвимость CVE-2099-10003 в FortiOS

`P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · CVSS 9.8 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий.

В учебном примере раскрыта уязвимость CVE-2099-10003 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [1](https://example.org/fictional/advisory/3)

Источники: [1 · Учебный источник](https://example.org/fictional/advisory/3)

<details><summary>Цитаты и применимость</summary>

- «Synthetic advisory CVE-2099-10003. FortiOS: \>=7.4.0, \<7.4.5; actively exploited. CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H» [1](https://example.org/fictional/advisory/3)

</details>

<a id="e-bcf770c196ab91c27bd1"></a>
### В учебном примере раскрыта уязвимость CVE-2099-10002 в FortiOS

`P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · CVSS 9.8 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий.

В учебном примере раскрыта уязвимость CVE-2099-10002 в FortiOS. Источник сообщает об эксплуатации в реальных атаках. [1](https://example.org/fictional/advisory/2)

Источники: [1 · Учебный источник](https://example.org/fictional/advisory/2)

<details><summary>Цитаты и применимость</summary>

- «Synthetic advisory CVE-2099-10002. FortiOS: \>=7.4.0, \<7.4.5; actively exploited. CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H» [1](https://example.org/fictional/advisory/2)

</details>

<a id="e-e2dfadfb392dc3397096"></a>
- В учебном примере раскрыта уязвимость CVE-2099-10001 в FortiOS · `P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий. · [источник](https://example.org/fictional/advisory/1)
<a id="e-4bb57db0a76eca767833"></a>
- В учебном примере раскрыта уязвимость CVE-2099-10000 в FortiOS · `P1` · Опубликовано 2026-09-30 · затронута наша версия 7.4.4 · Тег: Уязвимость. Приоритеты: Уязвимость — высокий. Общий приоритет: высокий. · [источник](https://example.org/fictional/advisory/0)
## Информация

<a id="e-c6e4cf431a7e30b5f806"></a>
### В учебном примере PostgreSQL получил обновление с исправлениями безопасности.

`P3` · Опубликовано 2026-09-30 · применимость не установлена 16.3 · Тег: Инфо \(требует проверки\). Приоритеты: Инфо — требует проверки. Общий приоритет: требует проверки.

В учебном примере PostgreSQL получил обновление с исправлениями безопасности. [1](https://example.org/fictional/postgresql)

Источники: [1 · Учебный источник](https://example.org/fictional/postgresql)

<details><summary>Цитаты и применимость</summary>

- «Synthetic PostgreSQL security update improves infrastructure safety.» [1](https://example.org/fictional/postgresql)

</details>

## Атаки

<a id="e-867b65e4978cd22c6f1c"></a>
### В учебном примере опубликовано сообщение об утечке данных.

`P3` · Опубликовано 2026-09-30 · внешний фон · Тег: Атака. Приоритеты: Атака — не определён. Общий приоритет: не определён.

В учебном примере опубликовано сообщение об утечке данных. [1](https://example.org/fictional/incident)

**Профиль атаки по техническому датасету:**

1. **Страна жертвы:** Информация отсутствует
2. **Наименование группировки:** Информация отсутствует
3. **Предполагаемая дата атаки:** Информация отсутствует
4. **Затронутые отрасли/компании:** Информация отсутствует
5. **Метод первоначального доступа:** Информация отсутствует
6. **Используемые инструменты злоумышленника:** Информация отсутствует
7. **Идентификатор используемых уязвимостей:** Информация отсутствует
8. **Наличие индикаторов компрометации:** Информация отсутствует

Источники: [1 · Учебный источник](https://example.org/fictional/incident)

<details><summary>Цитаты и применимость</summary>

- «Synthetic report: a data breach was confirmed by the organization.» [1](https://example.org/fictional/incident)
- Первоисточник не установлен; приведены публикации источников корпуса.

</details>

## Метод и ограничения

- Ссылки и цитаты проверены; смысловая подтверждённость требует экспертной оценки.
- Применимость неподдерживаемых схем версий — unknown.
- Снимок KEV отсутствует; отсутствие отметки KEV не означает отсутствия эксплуатации.
- Модель обратной связи накапливает метки; отбор выполняют правила.
- Учебные вымышленные события; показатели не описывают качество на реальных новостях.
