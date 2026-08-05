# RACI CHART + GOVERNANCE FRAMEWORKS — Operation Metadata Shield
## Data Corps for the Constitution — 2026-08-04
**ICAI Member Storinger Award 2002 — Lincoln Protocol Red+Blue=Purple**

---

## 1. RACI CHART — Data Corps Roles (Novice to Guru)

| Activity / Deliverable | **Novice / Spotter** L1 | **Journeyman / Analyst** L2 | **Expert / Architect** L3 | **Guru / Sentinel** L4 | **Stone Laraway (Founder / Data Owner)** | **Community / Public** |
|---|---|---|---|---|---|---|
| **Screenshot suppression + UTC timestamp log** | **R** Responsible — Capture image + time | A Accountable — Validate format | C Consulted — Advise on hash | I Informed | **A** Final Accountable | I Informed via hub |
| **Daily dataset update TXT/CSV/JSON** | R — Add line DATE\|OFFICIAL\|... | R — QA controlled list spelling | C — Check duplicate logic | I | **A** — Merge + commit | I — Via GitHub |
| **Placard duplicate detection (pHash + TEXT)** | I | **R** — Calculate Duplication Rate = (Total-Unique)/Total | A — Define threshold >40% | C — Method review | **A** | I |
| **Word Soup — Top words per official** | R — Paste TEXT_SNIPPET | **R** — Generate TF table + cloud | C — TF-IDF guidance | A — Publish methodology | **A** | C — Crowd-suggest words |
| **Baseball Cards — Evidence Deck (Allegedly)** | C — Suggest new placard | R — Draft front/back stats | A — Verify SHA256 + ALLEGEDLY watermark | C — Legal/OSINT review | **A** — Final approval + deep-link ?card= | I — Collect/share |
| **Baseball Cards — Honor Deck (Integrity)** | R — Nominate integrity champion (Leen Hijaz etc) | R — Map to ICAI value | A — Verify courage/responsibility story | C — ICAI liaison | **A** — Approve honor + gold border | C — Nominate |
| **Dashboard — Timeline, Bar, Donut, Heatmap** | I | R — Build frequency tables | **R** — Build visualizations (Lindy Ryan method) | **A** — Portfolio-ready review | **A** — Host on GitHub Pages | I — Discover pattern |
| **QR Poster + Hub index.html** | I | R — Generate QR codes | **R** — Build hub linking all pages | C | **A** | I — Scan/share |
| **Governance — COBIT/COSO/ITIL/PRINCE2/ISO compliance** | I | C — Document controls | **R** — Map controls to frameworks | **A** — Audit | **A** — Data Owner | I |
| **Exclusion — TD Bank MSB/HRC/TDS filter** | R — Do not log if keywords present | A — Validate filter | C | I | **A** — Enforce | I |
| **Personal Kit Disclaimer** | I | I | C — FTC compliance wording | A — Legal review note | **R/A** — Personal ethos statement | I |

**RACI Legend:** R=Responsible (does), A=Accountable (owns), C=Consulted, I=Informed
**Founder Role:** Stone Laraway — Data Owner — MBS Rutgers — ICAI Member Storinger Award 2002 — Final Accountability for all deliverables

---

## 2. COBIT 2019 MAPPING — IT Governance

| COBIT Objective | Application to Data Corps | Artifact | Control Implemented |
|---|---|---|---|
| **APO09 Service Agreements** | Define dataset format contract DATE\|OFFICIAL\|... | DATA_DICTIONARY.md | Controlled list for PLACARD_TYPE, BLOCK_TYPE |
| **APO10 Project Management** | Phased: Phase 1 Briefing → Dashboard → Cards → Lab → QR | index.html, README | Timeline 2024-2026 + Inflection points July 28-29, Aug 4 |
| **APO14 Data Management** | Data quality: Accuracy, Completeness, Consistency, Timeliness | DATA_DICTIONARY.md §5 | ISO 8000 rules + daily commit SLA 24h |
| **BAI08 Knowledge Management** | Visual Imperative — Story First, Discovery culture | dashboard.html, cards.html | Lindy Ryan methodology — multiple perspectives same truth |
| **BAI10 Configuration** | Version control of TXT/CSV/JSON daily files | GitHub repo slaraway70/constitution-data-corps | File naming data-corps-dataset-YYYY-MM-DD.* |
| **DSS01 Operations** | Daily 2-min workflow screenshot → log → commit → push | README §Datasets | Documented in DATA_DICTIONARY + QR poster |
| **MEA01 Performance Monitoring** | Duplication Rate 44%, Rate Limit Spike 12/day = Inflection | placard-lab.html | Thresholds defined, auto-calculated |
| **MEA02 Internal Control** | ALLEGEDLY watermark, OSINT only, SHA256 evidence preservation | cards.html (Evidence Deck Red) | OSINT disclaimer + hash + QR |
| **MEA03 Compliance** | Personal kit disclaimer — No endorsement implied — FTC | index.html, cards.html, README | Disclaimer banner: These companies may not share mission... |

---

## 3. COSO 2013 — Internal Controls

| COSO Component | Principle | Data Corps Implementation |
|---|---|---|
| **Control Environment** | 1. Integrity & Ethics | ICAI 6 values: Honesty, trust, fairness, respect, responsibility, courage — Gold banner on all pages |
| **Risk Assessment** | 7. Identifies risks | Risk: Metadata filtering suppresses constitutional discourse — Measured via Rate Limit Spike + Duplication Rate |
| **Control Activities** | 10. Selects controls | Controls: SHA256 preservation, ALLEGEDLY watermark, TD Bank exclusion filter, controlled vocabulary |
| **Information & Communication** | 13. Quality info | Data dictionary with validation rules — ISO 8000 — Daily TXT/CSV/JSON in same format |
| **Monitoring** | 16. Ongoing evaluations | Daily dataset review — Guru/Sentinel L4 reviews methodology — Founder final accountable |

---

## 4. ITIL 4 — Service Management

| ITIL Practice | Data Corps Service | Artifact |
|---|---|---|
| **Incident Management** | Block / Rate Limit event = Incident — Logged with DATE, POST_ID, BLOCK_TYPE | data-corps-dataset-*.csv — 33 incidents Aug 4 |
| **Problem Management** | Problem: Content-based spam filter? Hypothesis testing structured vs plain opinion both blocked | placard-lab.html — Rate limit hypothesis |
| **Knowledge Management** | Knowledge base: Visual dashboards + baseball cards make pattern discoverable | dashboard.html, cards.html, DATA_DICTIONARY.md |
| **Service Request** | Request: "Nominate integrity champion" — Community can suggest via RACI C | Honor Deck — Leen Hijaz 17, Erika Jordan, Jefferson Fisher etc. |
| **Service Validation** | Validation: IMAGE_HASH duplicate detection, SHA256 evidence | DATA_DICTIONARY §5 Quality Rules |
| **Continual Improvement** | Daily commit, Repetition Rate trending, Word Soup evolving | GitHub commit history — Inflection #1 July 28-29 8 events, #2 Aug 4 33 events |

---

## 5. PRINCE2 — Project Management

| PRINCE2 Theme | Data Corps Application |
|---|---|
| **Business Case** | Benefit: Document metadata filtering impact on 1A discourse — Academic portfolio, citizen defense — No funding ask — IRB-exempt OSINT |
| **Organization** | Roles: L1 Novice Spotter, L2 Journeyman Analyst, L3 Expert Architect, L4 Guru Sentinel, Founder Stone Laraway Data Owner — RACI defined |
| **Quality** | Quality criteria: ISO 8000 data quality, Lindy Ryan visual imperative, ALLEGEDLY OSINT disclaimer, SHA256 preservation |
| **Plans** | Phases: Phase 1 Briefing (index.html), Phase 2 Dashboard (dashboard.html), Phase 3 Cards (cards.html), Phase 4 Lab (placard-lab.html), Phase 5 QR (qr-poster.html) — Daily dataset updates |
| **Risk** | Risks: Platform suppression of documentation itself (experienced Aug 4), defamation risk mitigated by ALLEGEDLY watermark + OSINT only |
| **Change** | Change control: Controlled vocabulary for PLACARD_TYPE — must use exact spelling — New types via Journeyman QA |
| **Progress** | Progress tracking: 17 historical (2024-2026) + 33 today = 50 total — Duplication Rate 44% — GitHub commit log as progress register |

---

## 6. ISO STANDARDS

| ISO | Title | Applicability | Implementation |
|---|---|---|---|
| **ISO 8601** | Date/time format | DATE field | YYYY-MM-DD — All dataset files — Validation rule |
| **ISO 8000** | Data Quality | Data dictionary quality rules | Accuracy, Completeness, Consistency, Timeliness, Validity, Uniqueness — §5 DATA_DICTIONARY |
| **ISO 15489** | Records Management | Evidence preservation | POST_ID unique, SHA256_EVIDENCE hash of screenshot, retention in GitHub Pages |
| **ISO 27001** | Info Security | Controls A.18 Compliance, A.16 Incident | Personal kit disclaimer (A.18 IP), Rate Limit Spike = Security incident (A.16) — 12x Aug 4 |
| **ISO 27037** | Digital Evidence | Evidence collection | Screenshot + UTC + SHA256 + chain of custody via GitHub commit — Core insight preserved |
| **ISO 31000** | Risk Management | Risk: Metadata suppression | Risk assessment: Likelihood High (33 events/day), Impact High (1A discourse), Treatment: Document + Decentralize via GitHub Pages |
| **ISO 9001** | Quality Management | Quality of dashboards | Lindy Ryan visual imperative — Clarity over decoration — Multiple perspectives same truth — Portfolio-ready |
| **ISO 14001** | Environmental (adapted) | Digital sustainability | No funding ask, open-source, GitHub Pages hosting — low carbon citizen science |
| **ISO 26000** | Social Responsibility | Civic duty | Bullhorn notice — Global call across ALL NAICS/SIC — Support and defend Constitution — E Pluribus Unum |

---

## 7. COMPLIANCE CHECKLIST

- [x] Data Dictionary with types, validation, controlled lists — ISO 8000
- [x] RACI for 4 tiers Novice to Guru + Founder + Community
- [x] COBIT APO09, APO10, APO14, BAI08, BAI10, DSS01, MEA01-03 mapped
- [x] COSO 5 components with ICAI integrity environment
- [x] ITIL 4 Incident, Problem, Knowledge, Request, Validation, Improvement
- [x] PRINCE2 7 themes with phases and business case
- [x] ISO 8601, 8000, 15489, 27001, 27037, 31000, 9001, 26000
- [x] ALLEGEDLY watermark for Evidence Deck — OSINT only — Not legal finding
- [x] Personal kit disclaimer — No endorsement — FTC compliance — Profila https://customers.profila.com/ Michiel Van Roey Brussels
- [x] Exclusion TD Bank MSB/HRC/TDS — Not germane — Filtered
- [x] SHA256 preservation — Evidence hash
- [x] Daily update workflow — 2 min — TXT/CSV/JSON same format
- [x] ICAI credential — Storinger Award 2002 — 6 values banner on all pages
- [x] Lincoln Protocol Red+Blue=Purple #5B2C6F

**Author:** Stone Laraway — MBS Rutgers — ICAI Member Storinger Award 2002 — Mount Holly NJ 08060 — Paying forward  
**License:** UNCLASSIFIED // FOR PUBLIC RELEASE — Citizen Data Defense
