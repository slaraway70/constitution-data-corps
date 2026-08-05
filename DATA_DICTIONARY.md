# DATA DICTIONARY — Operation Metadata Shield
## Data Corps for the Constitution — v2.0 — 2026-08-04
**ICAI Member Storinger Award 2002 — Lindy Ryan Methodology**

### 1. CORE DATASET — `data-corps-dataset-*.csv/.txt/.json`
Daily update file: 33 entries today (2026-08-04), cumulative 50 total (17 historical + 33 today)

| Field | Type | Required | Example | Definition | Validation | Standard Mapping |
|---|---|---|---|---|---|---|
| **DATE** | DATE ISO8601 | Yes | 2026-08-04 | UTC date of documentation event | YYYY-MM-DD, not future | ISO 8601 |
| **OFFICIAL** | VARCHAR(100) | Yes | Nancy Mace, Nashville Tea Party, Brandon Gill (Arra Posa), The Telegraph, System | Subject official, page, or system actor | Controlled list + Other | COBIT APO09 |
| **PLACARD_TYPE** | VARCHAR(150) | Yes | No Funds for Fascists Act, Foreign-born judges, Hold The Line - Bathroom Bill, TRANS MICE Act, You get the boot with both!, Obamacare is Communism AI meme, Handmaid's Tale I didn't vote for this, Rate Limit / Spam, Typing Tax, Mount Holly Fire District Block | Virtual placard graphic template or event type | Use exact same spelling for duplicate detection | ISO 8000 Data Quality |
| **PLATFORM** | VARCHAR(50) | Yes | Facebook, Instagram, Facebook+Instagram, LinkedIn | Platform where block/filter occurred | Enum: Facebook, Instagram, Threads, LinkedIn, X, Other | COBIT BAI08 |
| **POST_ID** | VARCHAR(50) | Yes | 30, 56, 60, 67, 70, Post_ID 42 | Internal sequential ID from documentation log | Numeric, unique per day | ISO 15489 Records Mgmt |
| **POST_URL** | URL | No | https://facebook.com/... | Public URL of blocked post or screenshot source | Valid URL or blank if blocked | ITIL 4 SVS |
| **IMAGE_HASH** | VARCHAR(100) | No | phash_a1b2c3 | Perceptual hash of placard image for duplicate detection | pHash or SHA256, blank allowed | COBIT APO14 |
| **TEXT_SNIPPET** | VARCHAR(300) | Yes | "You get the boot with both!" | First 100-150 chars of post text for word soup | Max 300 chars, no PII | ISO 27001 A.18 |
| **BLOCK_TYPE** | VARCHAR(50) | Yes | Rate Limit, Block, AI Flag, Local Gov Block, Spam-limit, Filter | Type of platform friction | Controlled list | COSO Principle 10 |
| **NOTES** | VARCHAR(500) | No | DUPLICATE same graphic, 4K likes 1.3K shares, Impersonation test | Analyst notes, engagement counts, hypothesis | Free text, no defamation | COBIT MEA01 |
| **SHA256_EVIDENCE** | CHAR(64) | Recommended | e3b0c44298fc... | SHA256 hash of screenshot preservation | 64 hex chars | ISO 27037 Evidence |
| **DUPLICATE_FLAG** | BOOLEAN | Auto | TRUE/FALSE | Auto-calculated if PLACARD_TYPE repeats | TRUE if count>1 per type | ISO 8000 |
| **WORD_COUNT** | INT | Auto | 8 | Count of words in TEXT_SNIPPET for soup | Auto | — |

### 2. DERIVED METRICS — `placard-lab.html`

| Metric | Formula | Type | Definition | Threshold | Governance |
|---|---|---|---|---|---|
| **Total Tracked** | COUNT(all) | INT | Total documentation events | — | MEA01 Performance |
| **Unique Placards** | COUNT(DISTINCT PLACARD_TYPE) | INT | Distinct templates | — | APO09 Service Agreement |
| **Duplication Rate** | (Total - Unique)/Total *100 | % | % of repeated templates | >40% = High amplification | COSO Risk Assessment |
| **Rate Limit Spike** | COUNT where BLOCK_TYPE=Rate Limit per day | INT/day | Platform friction intensity | >5/day = Inflection Point | ISO 27001 A.16 Incident |
| **Top Words** | TF per OFFICIAL | List | Word frequency per official for soup | Top 20 per official | APO14 Data Mgmt |

**Current Values (2026-08-04):** Total 50, Unique 28, Duplication 44%, Rate Limit Spike 12 (Inflection #2), Nashville 5x, No Funds 4x

### 3. BASEBALL CARD DECKS — `cards.html`

| Field | Type | Definition |
|---|---|---|
| CARD_ID | VARCHAR(20) | Unique ID: nancy-mace, leen-hijaz, etc. — for deep-link ?card=ID |
| DECK_TYPE | ENUM | Evidence (Red) or Honor (Gold) |
| ICAI_VALUE | ENUM | Honesty, trust, fairness, respect, responsibility, courage — Honor deck only |
| ALLEGEDLY_FLAG | BOOLEAN | TRUE for Evidence deck — shows faded watermark — OSINT only |
| SHA256_QR | URL | QR code linking to evidence hash |

### 4. GOVERNANCE LOG — `README.md`

| Field | Standard | Control |
|---|---|---|
| EXCLUSION_LIST | Internal | TD Bank MSB/HRC/TDS — Not germane — filtered out |
| PERSONAL_KIT_DISCLAIMER | FTC / Legal | These companies may not share mission — No endorsement implied |
| ICAI_CREDENTIAL | Academic | Storinger Award 2002 — Member ICAI https://academicintegrity.org/ |
| PROFILA_LINK | Data Sovereignty | https://customers.profila.com/ — Michiel Van Roey Brussels — Data ownership |

### 5. DATA QUALITY RULES — ISO 8000

1. **Accuracy:** POST_URL must be verifiable or marked blocked
2. **Completeness:** DATE, OFFICIAL, PLACARD_TYPE, BLOCK_TYPE required — no nulls
3. **Consistency:** PLACARD_TYPE spelling must match controlled list for duplicate detection — "No Funds for Fascists Act" always same caps
4. **Timeliness:** Daily file named `data-corps-dataset-YYYY-MM-DD.*` — committed within 24h
5. **Validity:** DATE not future, POST_ID numeric, BLOCK_TYPE in enum
6. **Uniqueness:** IMAGE_HASH + TEXT_SNIPPET combo should be unique — flag duplicates

### 6. WORD SOUP DICTIONARY

| Term | Source | Context | Count Sample |
|---|---|---|---|
| boot, both | Nashville Tea Party | "You get the boot with both!" — Socialism comparison meme — 4K likes | 5 |
| communism, Obamacare, Dave Ramsey | Nashville Tea Party | AI meme — Obamacare is Communism — flagged AI content | 5 |
| Handmaid, fascists, funds | Nancy Mace | Handmaid's Tale "I didn't vote for this" + No Funds for Fascists Act | 4+2 |
| thought police, Boy George | The Telegraph | Boy George cancelled by thought police framing vs humanitarian reports | 1 |
| AI content, impersonation | Brandon Gill | Page run by Arra Posa — AI content flag — impersonation test | 1 |
| spam, rate limit, typing tax | System | 12x spike Aug 4 — content-based spam filter hypothesis | 12 |

**Author:** Stone Laraway — MBS Rutgers — ICAI Member Storinger Award 2002 — Mount Holly NJ 08060
**License:** OSINT — SHA256 Preserved — UNCLASSIFIED // FOR PUBLIC RELEASE
