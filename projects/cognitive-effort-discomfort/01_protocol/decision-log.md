# Decision Log

## 2026-03-22: Review Type Decision

**Decision**: Scoping review (not meta-analysis)

**Rationale**:
1. The outcome (discomfort during cognitive work) is not operationalized consistently across studies — VAS fatigue, effort discounting, PPT, headache diary, and self-reported "difficulty" are not poolable
2. No common manipulation: "sustained cognitive effort" ranges from 15-min Stroop to 8-hour simulated workday
3. The healthy non-clinical population of interest is almost entirely absent from existing literature (most studies use TTH patients or burnout cohorts)
4. Zero studies have jointly measured interoceptive discomfort localization + effort economics — there is nothing to pool for the key relationship
5. The question crosses at least 4 literatures (headache medicine, cognitive effort economics, neuro-metabolic fatigue, predictive processing/interoception) — a scoping review is precisely designed to map heterogeneous cross-disciplinary terrain

**Framework**: Arksey & O'Malley (2005), PRISMA-ScR (Tricco et al., 2018)

## 2026-03-22: Database Selection

**Decision**: PubMed + CrossRef + Semantic Scholar (no Scopus, no Embase)

**Rationale**:
- PubMed: primary biomedical database, best for layers L2 and L5
- CrossRef: broadest DOI coverage, captures psychology/neuroscience journals not indexed in PubMed
- Semantic Scholar: AI-curated, excellent for citation chaining and discovering cross-disciplinary work
- Scopus/Embase excluded: API access not available; CrossRef + Semantic Scholar provide equivalent coverage for this topic

## 2026-03-22: Analysis Type

**Decision**: Narrative synthesis organized by 5 literature layers, no quantitative pooling

**Rationale**: See review type decision above. Evidence gap map will be produced instead of forest plots.

## 2026-03-23: Scopus Supplementary Search

**Decision**: Added Scopus as a 4th database to check for missed records

**What was done**:
- Ran all 5 literature layers (L1–L5) through the Elsevier Scopus Search API
- Retrieved 2,500 records (500 per layer), yielding 2,440 unique DOIs
- 1,046 (43%) already in our existing pool → confirms good overlap with PubMed/CrossRef/S2
- 1,394 new DOIs screened for relevance → 99 keyword-matched → 22 manually reviewed

**Outcome**:
- **5 records recommended to add** (all L1 — effort aversiveness)
- **6 records flagged for colleague review** (borderline, need full-text)
- 11 excluded from candidates (clinical-only, sport performance, applied domains)

**Recommended additions**:
1. Giboin et al. (2019) — ego depletion/mental fatigue meta-analysis — `10.1016/j.peh.2019.100150`
2. Place et al. (2025) — cardiovascular responses to mental fatigue — `10.1016/j.ijpsycho.2025.113210`
3. Rewitz et al. (2024) — subjective effort vs. objective force — `10.1371/journal.pone.0307994`
4. Sjåstad & Baumeister (2018) — ego depletion → planning aversion — `10.1016/j.jesp.2018.01.005`
5. Hopstaken et al. (2015) — pupil dynamics & mental fatigue — `10.1016/j.biopsycho.2015.06.013`

**Files**: Full report and all raw data at:
→ `02_search/round-01/scopus/SCOPUS_SUPPLEMENTARY_SEARCH_REPORT.md`
→ `02_search/round-01/scopus/scopus_manual_screening.json`

**Impact on review**: No critical gaps found in L2–L5. Adds useful L1 depth. PRISMA flow diagram should be updated to include Scopus as a database.
