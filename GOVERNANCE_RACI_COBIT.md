# RACI CHART + GOVERNANCE FRAMEWORKS — Operation Metadata Shield
## Data Corps for the Constitution — 2026-08-04 — CLEAN — No work-related content
**ICAI Member Storinger Award 2002 — Lincoln Protocol Red+Blue=Purple — SCOPE: OSINT public placard documentation only**

---

## 1. RACI CHART — Data Corps Roles (Novice to Guru)

| Activity / Deliverable | Novice / Spotter L1 | Journeyman / Analyst L2 | Expert / Architect L3 | Guru / Sentinel L4 | Stone Laraway (Founder / Data Owner) | Community / Public |
|---|---|---|---|---|---|---|
| Screenshot suppression + UTC timestamp log | R — Capture image + time | A — Validate format | C — Advise on hash | I | A — Final Accountable | I via hub |
| Daily dataset update TXT/CSV/JSON | R — Add line DATE|OFFICIAL|... | R — QA controlled list spelling | C — Check duplicate logic | I | A — Merge + commit | I via GitHub |
| Placard duplicate detection (pHash + TEXT) | I | R — Calculate Duplication Rate = (Total-Unique)/Total | A — Define threshold >40% | C — Method review | A | I |
| Word Soup — Top words per official | R — Paste TEXT_SNIPPET | R — Generate TF table + cloud | C — TF-IDF guidance | A — Publish methodology | A | C — Crowd-suggest words |
| Baseball Cards — Evidence Deck (Allegedly) | C — Suggest new placard | R — Draft front/back stats | A — Verify SHA256 + ALLEGEDLY watermark | C — Legal/OSINT review | A — Final approval + deep-link ?card= | I — Collect/share |
| Baseball Cards — Honor Deck (Integrity) | R — Nominate integrity champion (Leen Hijaz etc) | R — Map to ICAI value | A — Verify courage story | C — ICAI liaison | A — Approve honor + gold border | C — Nominate |
| Dashboard — Timeline, Bar, Donut, Heatmap | I | R — Build frequency tables | R — Build visualizations (Lindy Ryan) | A — Portfolio-ready review | A — Host GitHub Pages | I — Discover pattern |
| QR Poster + Hub index.html | I | R — Generate QR codes | R — Build hub linking all pages | C | A | I — Scan/share |
| Governance — COBIT/COSO/ITIL/PRINCE2/ISO | I | C — Document controls | R — Map controls to frameworks | A — Audit | A — Data Owner | I |
| Personal Kit Disclaimer | I | I | C — FTC wording | A — Legal review note | R/A — Personal ethos statement | I |
| OpenSecrets Blend | I | R — Pull FEC data from OpenSecrets.org | A — Validate funding context join on OFFICIAL | C | A | I |

**Legend:** R=Responsible, A=Accountable, C=Consulted, I=Informed
**Founder:** Stone Laraway — Data Owner — MBS Rutgers — ICAI Member Storinger Award 2002

---

## 2. COBIT 2019 MAPPING

| COBIT Objective | Application | Artifact | Control |
|---|---|---|---|
| APO09 Service Agreements | Define dataset format DATE|OFFICIAL|... | DATA_DICTIONARY.md | Controlled list PLACARD_TYPE, BLOCK_TYPE |
| APO10 Project Management | Phased: Briefing → Dashboard → Cards → Lab → QR → Governance | index.html, README | Timeline 2024-2026 + Inflections July 28-29, Aug 4 |
| APO14 Data Management | Data quality Accuracy Completeness Consistency Timeliness | DATA_DICTIONARY §5 | ISO 8000 rules + daily commit 24h |
| BAI08 Knowledge Management | Visual Imperative Story First Discovery culture | dashboard.html, cards.html | Lindy Ryan multiple perspectives same truth |
| BAI10 Configuration | Version control TXT/CSV/JSON daily | GitHub slaraway70/constitution-data-corps | File naming YYYY-MM-DD |
| DSS01 Operations | Daily 2-min workflow screenshot → log → commit → push | README §Datasets | Documented in DATA_DICTIONARY + QR poster |
| MEA01 Performance Monitoring | Duplication Rate 44%, Rate Limit Spike 12/day Inflection | placard-lab.html | Thresholds auto-calculated |
| MEA02 Internal Control | ALLEGEDLY watermark OSINT only SHA256 preservation | cards.html Evidence Deck Red | OSINT disclaimer + hash + QR |
| MEA03 Compliance | Personal kit disclaimer No endorsement FTC + OpenSecrets credit | index.html, cards.html, README | Disclaimer banner + OpenSecrets attribution |

---

## 3. COSO 2013

| Component | Principle | Implementation |
|---|---|---|
| Control Environment | 1. Integrity & Ethics | ICAI 6 values Honesty trust fairness respect responsibility courage Gold banner |
| Risk Assessment | 7. Identifies risks | Risk: Metadata filtering suppresses constitutional discourse — Measured via Rate Limit Spike + Duplication Rate |
| Control Activities | 10. Selects controls | Controls: SHA256 preservation, ALLEGEDLY watermark, controlled vocabulary, OpenSecrets credit |
| Information & Communication | 13. Quality info | Data dictionary validation rules ISO 8000 Daily TXT/CSV/JSON same format |
| Monitoring | 16. Ongoing evaluations | Daily review Guru L4 reviews methodology Founder final accountable |

---

## 4. ITIL 4

| Practice | Service | Artifact |
|---|---|---|
| Incident Management | Block / Rate Limit = Incident Logged DATE POST_ID BLOCK_TYPE | data-corps-dataset-*.csv 33 incidents Aug 4 |
| Problem Management | Problem: Content-based spam filter? Hypothesis structured vs plain both blocked | placard-lab.html Rate limit hypothesis |
| Knowledge Management | Knowledge base Visual dashboards + baseball cards discoverable | dashboard.html, cards.html, DATA_DICTIONARY.md |
| Service Request | Request: Nominate integrity champion | Honor Deck Leen Hijaz 17, Erika Jordan, Jefferson Fisher etc. |
| Service Validation | Validation: IMAGE_HASH duplicate detection SHA256 | DATA_DICTIONARY §5 Quality Rules |
| Continual Improvement | Daily commit Repetition Rate trending Word Soup evolving | GitHub history Inflection #1 July 28-29 8 events #2 Aug 4 33 events |

---

## 5. PRINCE2

| Theme | Application |
|---|---|
| Business Case | Benefit: Document metadata filtering impact on 1A discourse — Academic portfolio, citizen defense — No funding ask — IRB-exempt OSINT — OpenSecrets blend adds funding context |
| Organization | Roles L1 Novice L2 Journeyman L3 Expert L4 Guru Founder Data Owner — RACI defined |
| Quality | Criteria ISO 8000 data quality Lindy Ryan visual imperative ALLEGEDLY OSINT disclaimer SHA256 preservation OpenSecrets attribution |
| Plans | Phases Phase1 Briefing index.html Phase2 Dashboard dashboard.html Phase3 Cards cards.html Phase4 Lab placard-lab.html Phase5 QR qr-poster.html Phase6 Governance governance.html Phase7 Datasets blended datasets.html — Daily updates |
| Risk | Risks Platform suppression of documentation itself (experienced Aug 4) defamation mitigated ALLEGEDLY watermark OSINT only |
| Change | Change control Controlled vocabulary PLACARD_TYPE exact spelling New types via Journeyman QA |
| Progress | Progress 17 historical +33 today=50 total Duplication 44% GitHub commit log progress register |

---

## 6. ISO STANDARDS

| ISO | Title | Applicability | Implementation |
|---|---|---|---|
| ISO 8601 | Date/time | DATE field | YYYY-MM-DD All files Validation |
| ISO 8000 | Data Quality | Quality rules | Accuracy Completeness Consistency Timeliness Validity Uniqueness §5 DATA_DICTIONARY |
| ISO 15489 | Records Mgmt | Evidence preservation | POST_ID unique SHA256 hash screenshot retention GitHub Pages |
| ISO 27001 | Info Security | A.18 Compliance A.16 Incident | Personal kit disclaimer A.18 IP Rate Limit Spike Security incident A.16 12x Aug 4 |
| ISO 27037 | Digital Evidence | Evidence collection | Screenshot + UTC + SHA256 + chain via GitHub commit |
| ISO 31000 | Risk Mgmt | Risk Metadata suppression | Likelihood High 33 events/day Impact High 1A discourse Treatment Document Decentralize GitHub |
| ISO 9001 | Quality Mgmt | Quality dashboards | Lindy Ryan Clarity over decoration Multiple perspectives same truth Portfolio-ready |
| ISO 26000 | Social Responsibility | Civic duty | Bullhorn Global call ALL NAICS/SIC Support defend Constitution E Pluribus Unum |
| ISO 690 | Citation | OpenSecrets attribution | Credit OpenSecrets.org Feel free to distribute or cite but credit OpenSecrets — FEC data |

---

## 7. OPENSECRETS BLEND — NEW

| Field | Source | Method | Note |
|---|---|---|---|
| Top Contributor | OpenSecrets.org Nancy Mace summary | Join OFFICIAL=Nancy Mace | AIPAC $43,305 Club for Growth $28,100 Oracle $19,900 |
| Top Industry | OpenSecrets.org | Join OFFICIAL | Republican/Conservative $485,687 Retired $384,711 Securities $196,148 Leadership PACs $187,000 Real Estate $111,989 |
| Source of Funds | OpenSecrets.org | % breakdown | Other 48.74% Large 21.13% PAC 17.14% Small 12.99% $449,704 |
| Funding Context | Blended analysis | Qualitative placard + Quantitative finance | Example: No Funds for Fascists Act + Republican/Conservative backing — messaging pattern analysis |

Credit: https://www.opensecrets.org/members-of-congress/nancy-mace/summary?cid=N00035670 — FEC data released electronically — Summary based on FEC reports Detailed records based on itemized contributions over $200 requiring occupation/employer disclosure

---

## 8. COMPLIANCE CHECKLIST

- [x] Data Dictionary 13 fields + OpenSecrets blend — ISO 8000
- [x] RACI 4 tiers Novice to Guru + Founder + Community
- [x] COBIT APO09 APO10 APO14 BAI08 BAI10 DSS01 MEA01-03 mapped
- [x] COSO 5 components ICAI integrity environment
- [x] ITIL 4 Incident Problem Knowledge Request Validation Improvement
- [x] PRINCE2 7 themes phases business case
- [x] ISO 8601 8000 15489 27001 27037 31000 9001 26000 690
- [x] ALLEGEDLY watermark Evidence Deck OSINT only Not legal finding
- [x] Personal kit disclaimer No endorsement FTC Profila https://customers.profila.com/ Michiel Van Roey Brussels
- [x] SCOPE LIMITATION OSINT public political posts only No financial crime data No private banking data No unrelated investigations Strictly public placard protest documentation
- [x] OpenSecrets credit attribution per requirement
- [x] SHA256 preservation Evidence hash
- [x] Daily workflow 2 min TXT/CSV/JSON same format
- [x] ICAI credential Storinger Award 2002 6 values banner
- [x] Lincoln Protocol Red+Blue=Purple #5B2C6F
- [x] NO work-related content anywhere — CLEAN

Author: Stone Laraway — MBS Rutgers — ICAI Member Storinger Award 2002 — Mount Holly NJ 08060 — Paying forward
License: UNCLASSIFIED // FOR PUBLIC RELEASE — Citizen Data Defense — No work-related content
