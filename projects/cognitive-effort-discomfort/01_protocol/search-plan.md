# Search Plan

## Overview
Multi-source search strategy using PubMed API, Semantic Scholar API, and CrossRef API. All searches are programmatic and reproducible.

---

## Database 1: PubMed (via E-utilities API)

### Query Strategy
Four complementary queries covering the 5 literature layers:

**Query 1 — Cognitive effort + somatic discomfort (L1, L3, L5)**
```
(("cognitive effort"[tiab] OR "mental effort"[tiab] OR "cognitive fatigue"[tiab] OR "mental fatigue"[tiab] OR "cognitive load"[tiab])
AND ("discomfort"[tiab] OR "headache"[tiab] OR "somatic"[tiab] OR "fatigue"[tiab] OR "pain"[tiab])
AND ("healthy"[tiab] OR "healthy adults"[tiab] OR "healthy volunteers"[tiab] OR "non-clinical"[tiab]))
```

**Query 2 — Neural metabolic cost of cognition (L2)**
```
(("mental fatigue"[tiab] OR "cognitive fatigue"[tiab] OR "cognitive effort"[tiab] OR "sustained cognition"[tiab])
AND ("glutamate"[tiab] OR "metabolic"[tiab] OR "prefrontal"[tiab] OR "glycogen"[tiab] OR "magnetic resonance spectroscopy"[tiab])
AND ("effort"[tiab] OR "cost"[tiab] OR "fatigue"[tiab]))
```

**Query 3 — Interoception + cognitive effort (L4)**
```
(("interoception"[tiab] OR "interoceptive"[tiab] OR "predictive processing"[tiab] OR "allostasis"[tiab] OR "active inference"[tiab])
AND ("cognitive effort"[tiab] OR "mental effort"[tiab] OR "cognitive control"[tiab])
AND ("discomfort"[tiab] OR "fatigue"[tiab] OR "aversive"[tiab] OR "prediction error"[tiab]))
```

**Query 4 — Effort discounting + cognitive control cost (L1, L3)**
```
(("effort discounting"[tiab] OR "effort-based decision"[tiab] OR "expected value of control"[tiab] OR "effort paradox"[tiab] OR "opportunity cost"[tiab])
AND ("cognitive"[tiab] OR "mental"[tiab])
AND ("aversive"[tiab] OR "cost"[tiab] OR "fatigue"[tiab] OR "discomfort"[tiab]))
```

### Filters
- Date: 2010/01/01 – 2026/12/31
- Language: English
- Species: Humans

### Execution
```bash
cd /home/user/meta-pipe/ma-search-bibliography/scripts
uv run pubmed_fetch.py --query "<query>" --output <output.bib> --mindate 2010/01/01 --maxdate 2026/12/31
```

---

## Database 2: Semantic Scholar (via API)

### Strategy
1. **Citation chasing**: Forward and backward citations of 8 key references from literature map
2. **Keyword search**: Complementary queries for papers not indexed in PubMed

### Key Papers for Citation Chasing
| Paper | Semantic Scholar ID / DOI |
|-------|--------------------------|
| Kurzban et al. (2013) | doi:10.1017/S0140525X12003196 |
| Inzlicht et al. (2018) | doi:10.1016/j.tics.2018.01.007 |
| Shenhav et al. (2017) | doi:10.1146/annurev-neuro-072116-031526 |
| Wiehler et al. (2022) | doi:10.1016/j.cub.2022.07.010 |
| Christie & Schrater (2015) | doi:10.3389/fnins.2015.00289 |
| Otto et al. (2018) | doi:10.1371/journal.pone.0198204 |
| Yee et al. (2022) | doi:10.1016/j.neubiorev.2021.12.016 |
| Seth & Friston (2016) | doi:10.1098/rstb.2016.0007 |

### Execution
Custom script: `projects/cognitive-effort-discomfort/tooling/semantic_scholar_fetch.py`

---

## Database 3: CrossRef (via API)

### Purpose
- DOI validation for all retrieved records
- Metadata enrichment for non-PubMed papers
- Not a primary search source

---

## Deduplication Strategy
1. Exact DOI match
2. Exact PMID match
3. Normalized title similarity (≥90% Jaccard on lowercased, stopword-removed tokens)

### Execution
```bash
uv run dedupe_bib.py --input projects/cognitive-effort-discomfort/02_search/round-01/ --output projects/cognitive-effort-discomfort/02_search/round-01/dedupe.bib
```

---

## Expected Results
- PubMed queries: ~30-50 records per query, ~60-120 total before dedup
- Semantic Scholar citation chasing: ~20-40 additional unique records
- Post-deduplication: ~40-80 unique records for screening
- Post-screening: ~20-60 included studies

---

## Search Documentation
All queries, counts, and dates will be recorded in:
- `02_search/round-01/queries.txt` — Exact query strings
- `02_search/round-01/log.md` — Search dates, counts, notes
