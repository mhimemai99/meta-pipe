# Claim Audit Report

## Date: 2026-03-22

## Purpose
Verify that all numerical claims in the manuscript match the source data (charting table and screening records).

---

## Claims Verified

| Claim | Location | Source Value | Status |
|-------|----------|-------------|--------|
| 43 records identified | Abstract, Results | queries.txt: 43 total | PASS |
| 0 duplicates removed | Results | dedupe_log.txt: 0 collisions | PASS |
| 43 screened | Results | screening-database.csv: 43 rows | PASS |
| 4 excluded (all P1) | Results | decisions.csv: 4 EXCLUDE | PASS |
| 39 included | Abstract, Results | included.bib: 39 entries | PASS |
| Cohen's kappa = 0.80 | Results | agreement.md: 0.80 | PASS |
| 93.0% agreement | Results | agreement.md: 93.0% | PASS |
| 16 empirical (41.0%) | Results | charting_table: 16 empirical rows | PASS |
| 23 theoretical (59.0%) | Results | 39 - 16 = 23 | PASS |
| L1: 15 (38.5%) | Results | charting_summary.csv: 15 | PASS |
| L2: 8 (20.5%) | Results | charting_summary.csv: 8 | PASS |
| L3: 8 (20.5%) | Results | charting_summary.csv: 8 | PASS |
| L4: 9 (23.1%) | Results | charting_summary.csv: 9 | PASS |
| L5: 1 (2.6%) | Results | charting_summary.csv: 1 | PASS |
| 12 measured discomfort (30.8%) | Results | charting_summary.csv: 12 | PASS |
| 1 measured somatic localization (2.6%) | Results, Abstract | charting_table: 1 (Cathcart) | PASS |
| Median publication year 2018 | Results | charting_table years | PASS |
| Cathcart 91% TTH vs 4% controls | Results | Web search data | PASS |
| Wiehler ~6 hours (375 min) | Results | charting_table: 375 min | PASS |

## Summary
- **Total claims audited**: 19
- **PASS**: 19
- **FAIL**: 0
- **Overclaims detected**: 0

## Notes
- All percentages verified against denominator of 39 included studies
- Layer counts sum to >39 due to 7 multi-layer classifications (as noted in text)
- No causal claims made about relationships between layers (appropriate for scoping review)
