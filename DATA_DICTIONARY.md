# DATA DICTIONARY — Operation Metadata Shield
## Data Corps for the Constitution — v2.0 — 2026-08-04
**ICAI Member Storinger Award 2002 — Lindy Ryan Methodology — SCOPE: OSINT public political posts only**

### 1. CORE DATASET — `data-corps-dataset-*.csv/.txt/.json`
Daily update: 33 entries today (2026-08-04), cumulative 50 total (17 historical + 33 today)

| Field | Type | Required | Example | Definition | Validation | Standard |
|---|---|---|---|---|---|---|
| DATE | DATE ISO8601 | Yes | 2026-08-04 | UTC date of documentation | YYYY-MM-DD, not future | ISO 8601 |
| OFFICIAL | VARCHAR(100) | Yes | Nancy Mace, Nashville Tea Party, Brandon Gill (Arra Posa), The Telegraph, System | Subject official or page | Controlled list + Other | COBIT APO09 |
| PLACARD_TYPE | VARCHAR(150) | Yes | No Funds for Fascists Act, Foreign-born judges, Hold The Line, TRANS MICE Act, You get the boot with both!, Obamacare is Communism AI meme, Handmaid's Tale I didn't vote for this, Rate Limit / Spam, Typing Tax, Mount Holly Fire District Block | Virtual placard graphic template or event type | Exact spelling for duplicate detection | ISO 8000 |
| PLATFORM | VARCHAR(50) | Yes | Facebook, Instagram, Facebook+Instagram, LinkedIn | Platform where block occurred | Enum: Facebook, Instagram, Threads, LinkedIn, X, Other | COBIT BAI08 |
| POST_ID | VARCHAR(50) | Yes | 30, 56, 60, 67, 70 | Internal sequential ID | Numeric, unique per day | ISO 15489 |
| POST_URL | URL | No | https://facebook.com/... | Public URL or blank if blocked | Valid URL or blank | ITIL SVS |
| IMAGE_HASH | VARCHAR(100) | No | phash_a1b2c3 | Perceptual hash for duplicate detection | pHash or SHA256 | APO14 |
| TEXT_SNIPPET | VARCHAR(300) | Yes | "You get the boot with both!" | First 100-150 chars for word soup | Max 300 chars, no PII | ISO 27001 |
| BLOCK_TYPE | VARCHAR(50) | Yes | Rate Limit, Block, AI Flag, Local Gov Block, Spam-limit, Filter | Type of platform friction | Controlled list | COSO P10 |
| NOTES | VARCHAR(500) | No | DUPLICATE same graphic, 4K likes 1.3K shares, Impersonation test | Analyst notes, engagement counts | Free text, no defamation | MEA01 |
| SHA256_EVIDENCE | CHAR(64) | Recommended | e3b0c44298fc... | SHA256 of screenshot preservation | 64 hex | ISO 27037 |
| DUPLICATE_FLAG | BOOLEAN | Auto | TRUE/FALSE | Auto if PLACARD_TYPE repeats | TRUE if count>1 | ISO 8000 |
| WORD_COUNT | INT | Auto | 8 | Words in TEXT_SNIPPET | Auto | — |
| OPENSECRETS_BLEND | VARCHAR(100) | Optional | AIPAC $43,305, Republican/Conservative $485,687 | Funding context from OpenSecrets.org | Credit OpenSecrets | FEC |

### 2. DERIVED METRICS — placard-lab.html
| Metric | Formula | Definition | Threshold |
|---|---|---|---|
| Total Tracked | COUNT(all) | Total events | — |
| Unique Placards | COUNT(DISTINCT PLACARD_TYPE) | Distinct templates | — |
| Duplication Rate | (Total-Unique)/Total*100 | % repeated templates | >40% High amplification |
| Rate Limit Spike | COUNT BLOCK_TYPE=Rate Limit per day | Friction intensity | >5/day = Inflection |
| Top Words | TF per OFFICIAL | Word frequency | Top 20 per official |

Current (2026-08-04): Total 50, Unique 28, Duplication 44%, Rate Limit Spike 12 (Inflection #2), Nashville 5x, No Funds 4x

### 3. BASEBALL CARD DECKS — cards.html
| Field | Type | Definition |
|---|---|---|
| CARD_ID | VARCHAR(20) | Unique ID: nancy-mace, leen-hijaz for deep-link ?card=ID |
| DECK_TYPE | ENUM | Evidence (Red) or Honor (Gold) |
| ICAI_VALUE | ENUM | Honesty, trust, fairness, respect, responsibility, courage — Honor only |
| ALLEGEDLY_FLAG | BOOLEAN | TRUE for Evidence deck — faded watermark — OSINT only |
| SHA256_QR | URL | QR linking to evidence hash |

### 4. GOVERNANCE LOG
| Field | Standard | Control |
|---|---|---|
| SCOPE_LIMITATION | Internal | OSINT public political posts only. No financial crime data, no private banking data, no unrelated investigations. Strictly public placard protest documentation. |
| PERSONAL_KIT_DISCLAIMER | FTC Legal | These companies may not share mission — No endorsement implied |
| ICAI_CREDENTIAL | Academic | Storinger Award 2002 — Member ICAI https://academicintegrity.org/ |
| PROFILA_LINK | Data Sovereignty | https://customers.profila.com/ — Michiel Van Roey Brussels |
| OPENSECRETS_CREDIT | Attribution | Credit OpenSecrets.org — FEC data — Feel free to distribute or cite but credit OpenSecrets |

### 5. DATA QUALITY RULES — ISO 8000
1. Accuracy: POST_URL verifiable or marked blocked
2. Completeness: DATE, OFFICIAL, PLACARD_TYPE, BLOCK_TYPE required
3. Consistency: PLACARD_TYPE spelling exact for duplicate detection — No Funds for Fascists Act same caps
4. Timeliness: Daily file data-corps-dataset-YYYY-MM-DD.* committed within 24h
5. Validity: DATE not future, POST_ID numeric, BLOCK_TYPE in enum
6. Uniqueness: IMAGE_HASH + TEXT_SNIPPET unique — flag duplicates

### 6. WORD SOUP DICTIONARY — Blended
| Term | Source | Context | Count |
|---|---|---|---|
| boot, both | Nashville Tea Party | You get the boot with both! — 4K likes 1.3K shares | 5 |
| communism, Obamacare, Dave Ramsey | Nashville Tea Party | AI meme Obamacare is Communism flagged AI | 5 |
| Handmaid, fascists, funds | Nancy Mace | Handmaid Tale I didn't vote + No Funds for Fascists Act | 6 |
| thought police, Boy George | The Telegraph | Boy George cancelled by thought police vs humanitarian reports | 1 |
| AI content, impersonation | Brandon Gill | Page run by Arra Posa AI content flag | 1 |
| spam, rate limit, typing tax | System | 12x spike Aug 4 content-based filter hypothesis | 12 |

Author: Stone Laraway — MBS Rutgers — ICAI Member Storinger Award 2002 — Mount Holly NJ 08060
License: OSINT — SHA256 Preserved — UNCLASSIFIED // FOR PUBLIC RELEASE — No work-related content
