# Scopus Supplementary Search Report

**Project**: Cognitive Effort and Somatic Discomfort — Scoping Review
**Date**: 2026-03-23
**Search Engine**: Elsevier Scopus Search API
**Purpose**: Independent supplementary search to identify records not captured by PubMed, CrossRef, or Semantic Scholar

---

## 1. Search Strategy

Five literature layers were searched independently on Scopus, mirroring the original PubMed strategy:

| Layer | Query | Records |
|-------|-------|---------|
| L1 | `TITLE-ABS-KEY("cognitive effort" OR "mental effort" OR "effort cost") AND TITLE-ABS-KEY("aversive" OR "opportunity cost" OR "fatigue" OR "discomfort")` | 500 |
| L2 | `TITLE-ABS-KEY("glutamate" OR "glycogen" OR "metabolic cost" OR "neuro-metabolic") AND TITLE-ABS-KEY("cognitive" OR "prefrontal" OR "working memory") AND TITLE-ABS-KEY("fatigue" OR "effort" OR "depletion")` | 500 |
| L3 | `TITLE-ABS-KEY("expected value of control" OR "dorsal anterior cingulate" OR "dACC") AND TITLE-ABS-KEY("effort" OR "cognitive control" OR "cost")` | 500 |
| L4 | `TITLE-ABS-KEY("interoceptive" OR "prediction error" OR "allostatic" OR "active inference") AND TITLE-ABS-KEY("fatigue" OR "discomfort" OR "effort" OR "cognitive")` | 500 |
| L5 | `TITLE-ABS-KEY("cognitive" OR "mental") AND TITLE-ABS-KEY("stress" OR "fatigue") AND TITLE-ABS-KEY("headache" OR "head pain" OR "discomfort") AND TITLE-ABS-KEY("healthy" OR "non-clinical" OR "normal")` | 500 |
| **Total** | | **2,500** |

**Note**: Each layer was capped at 500 records (API limit). Some layers may have additional uncaptured records.

---

## 2. Deduplication & Comparison

| Metric | Count |
|--------|-------|
| Scopus records retrieved | 2,500 |
| Unique DOIs from Scopus | 2,440 |
| Entries without DOI | 34 |
| **Already in existing pool** (PubMed + CrossRef + S2) | **1,046** (43%) |
| **New from Scopus** | **1,394** |

---

## 3. Relevance Screening

### 3a. Automated Keyword Scoring

99 of the 1,394 new records matched relevance keywords (score >= 3).

| Relevance Tier | Count |
|----------------|-------|
| High (score >= 6) | 3 |
| Medium (score 3-5) | 96 |
| Not relevant (score < 3) | 1,295 |

### 3b. Manual Title-Abstract Screening (22 candidates)

From the 99 keyword-matched records, 22 passed initial automated filters. Manual review yielded:

| Decision | Count |
|----------|-------|
| **Suggest Include** | **5** |
| **Review Needed** (colleague decision) | **6** |
| Exclude | 11 |

---

## 4. Recommended Additions (5 records)

These 5 records are **not in the current reference pool** and meet inclusion criteria for the scoping review:

### 4.1 Giboin et al. (2019)
- **Title**: The effect of ego depletion or mental fatigue on subsequent physical endurance performance: A meta-analysis
- **Journal**: Performance Enhancement and Health
- **DOI**: `10.1016/j.peh.2019.100150`
- **Layer**: L1 (Effort aversiveness)
- **Rationale**: Meta-analysis synthesizing ego depletion/mental fatigue literature. Directly relevant to whether cognitive effort depletes a shared resource that produces aversive signals.

### 4.2 Place et al. (2025)
- **Title**: Cardiovascular responses to mental fatigue in a sequential task paradigm
- **Journal**: International Journal of Psychophysiology
- **DOI**: `10.1016/j.ijpsycho.2025.113210`
- **Layer**: L1/L2 (Effort aversiveness / Neurometabolic)
- **Rationale**: Physiological (cardiovascular) correlates of mental fatigue in healthy adults during sustained cognitive work. Informs the somatic manifestation of effort cost.

### 4.3 Rewitz et al. (2024)
- **Title**: Examining the alignment between subjective effort and objective force production
- **Journal**: PLoS ONE
- **DOI**: `10.1371/journal.pone.0307994`
- **Layer**: L1 (Effort aversiveness)
- **Rationale**: Dissociates subjective experience of effort from objective performance. Relevant to understanding why effort *feels* aversive independent of actual energy expenditure.

### 4.4 Sjastad & Baumeister (2018)
- **Title**: The Future and the Will: Planning requires self-control, and ego depletion leads to planning aversion
- **Journal**: Journal of Experimental Social Psychology
- **DOI**: `10.1016/j.jesp.2018.01.005`
- **Layer**: L1 (Effort aversiveness)
- **Rationale**: Demonstrates that effortful cognitive tasks (planning) become aversive after prior cognitive exertion. Direct evidence for effort-as-discomfort signal.

### 4.5 Hopstaken et al. (2015)
- **Title**: The window of my eyes: Task disengagement and mental fatigue covary with pupil dynamics
- **Journal**: Biological Psychology
- **DOI**: `10.1016/j.biopsycho.2015.06.013`
- **Layer**: L1/L3 (Effort aversiveness / dACC)
- **Rationale**: Pupillometry evidence linking mental fatigue to disengagement. Pupil diameter indexes LC-NE system activity, connecting effort cost to arousal regulation and discomfort signaling.

---

## 5. Records Requiring Colleague Review (6 records)

These records have potential relevance but need full-text assessment:

| # | Year | Authors | Title | DOI | Note |
|---|------|---------|-------|-----|------|
| 1 | 2025 | Wojcik N. | The relationship between task value, mental fatigue, and motivation: The role of trait mindfulness | `10.1016/j.paid.2025.113120` | Motivation-fatigue interaction; may address effort aversiveness mechanism |
| 2 | 2025 | Allaw J. | Predicting Cognitive Fatigue Levels Using Multimodal Signals | `10.1109/icabme66883.2025.11211834` | Multimodal (EEG, physiological) fatigue measurement — check if mechanism-focused |
| 3 | 2023 | Ceynar M.L. | Studying Mental Fatigue: Dr. Tsuruko Arai Haraguchi Inspires from the Past | `10.4324/9781003246183-2` | Historical perspective on mental fatigue research — may provide theoretical context |
| 4 | 2022 | Rubio-Morales A. | Do Cognitive, Physical, and Combined Tasks Induce Similar Levels of Mental Fatigue? | `10.1123/mc.2022-0042` | Compares cognitive vs physical fatigue induction; may inform whether fatigue signal is domain-general |
| 5 | 2018 | Zhban E.S. | The role of mathematical and trait anxiety in mental fatigue: An EEG investigation | `10.11621/pir.2018.0406` | Individual differences (anxiety) in mental fatigue EEG — may inform L1 |
| 6 | 2013 | Shou G. | Ongoing EEG oscillatory dynamics suggesting evolution of mental fatigue in a color-word matching Stroop task | `10.1109/ner.2013.6696189` | EEG dynamics during cognitively fatiguing Stroop task; may inform L2/L3 neural correlates |

---

## 6. Exclusion Summary (11 records from candidates + 77 from initial filter)

| Reason | Count |
|--------|-------|
| Insufficient effort + outcome overlap | 49 |
| Sport performance focus | 14 |
| Clinical population only (no healthy controls) | 8 |
| Education/consumer domain | 4 |
| Ergonomics/HCI focus | 4 |
| Applied decision domain (not mechanism) | 2 |
| ML classification focus | 2 |
| Pharmacological focus | 2 |
| BCI/motor imagery | 1 |
| Historical/biographical | 1 |
| Economic decision-making | 1 |

---

## 7. Conclusion

Scopus adds **breadth** (1,394 new DOIs) but limited **depth** for our specific scoping review question. The existing PubMed + CrossRef + Semantic Scholar search captured the core literature well.

**Action items**:
1. Add the 5 recommended records to `included.bib`
2. Have colleagues review the 6 borderline records
3. Update PRISMA flow diagram to reflect Scopus as additional database

---

## Files Generated

| File | Description |
|------|-------------|
| `L1-L5_*.json` | Raw Scopus API results per layer |
| `L1-L5_*.bib` | BibTeX per layer |
| `L1-L5_*.log` | Search metadata per layer |
| `scopus_merged_all.bib` | All 2,500 entries merged |
| `scopus_new_relevant.bib` | 99 relevance-scored new entries (BibTeX) |
| `scopus_new_relevance_scored.json` | Full relevance scoring data |
| `scopus_screening_results.json` | Automated screening results |
| `scopus_manual_screening.json` | Manual screening decisions |
