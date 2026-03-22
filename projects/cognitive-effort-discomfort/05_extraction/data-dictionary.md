# Data Dictionary — Charting Table

## Overview
This charting table captures study characteristics for the scoping review on somatic discomfort during sustained cognitive effort. Variables follow the Arksey & O'Malley (2005) charting framework.

## Variables

| Variable | Type | Description | Values/Format |
|----------|------|-------------|---------------|
| study_id | string | BibTeX record ID (first author + year) | e.g., "Wiehler2022neurometabolic" |
| title | string | Shortened study title | Free text |
| year | integer | Publication year | 2004–2025 |
| country | string | Country of first/corresponding author | ISO country names |
| n_participants | integer/string | Total sample size | Number or "N/A (review)" |
| population | string | Study population description | "Healthy adults", "Mixed", "Clinical + controls", "N/A" |
| task_type | string | Cognitive task used | e.g., "N-back", "Stroop", "Working memory", "Demand selection" |
| task_duration_min | integer/string | Duration of cognitive task in minutes | Number or "N/A" |
| control_condition | string | Comparison/control condition | e.g., "Rest", "Low-demand control", "Pre-task baseline" |
| discomfort_measure | string | How somatic discomfort was measured | e.g., "VAS discomfort", "Fatigue VAS", "None" |
| effort_measure | string | How effort/cost was measured | e.g., "Effort discounting", "Subjective effort", "None" |
| neural_measure | string | Neuroimaging/neurophysiology method | e.g., "fMRI", "EEG", "Pupillometry", "None" |
| metabolic_measure | string | Metabolic marker measured | e.g., "MRS glutamate", "Glycogen model", "None" |
| somatic_localization | string | Where discomfort was localized | "Head", "General fatigue", "Not assessed", "N/A" |
| theoretical_framework | string | Primary literature layer | L1-L5 or combinations |
| key_finding | string | 1-2 sentence summary of main finding | Free text |
| study_design | string | Research design | e.g., "Within-subjects", "RCT", "Review", "Computational" |
| literature_layer | string | Classification per 5-layer model | L1, L2, L3, L4, L5, or combinations |

## Literature Layer Codes
- **L1**: Cognitive effort cost (opportunity cost, effort paradox, effort valuation)
- **L2**: Neural metabolic cost (glutamate, glycogen, energetic allocation)
- **L3**: Effort as aversive signal (dACC, EVC, effort monitoring)
- **L4**: Predictive processing / allostasis (interoception, active inference)
- **L5**: Somatic referral of cognitive fatigue (pericranial, stress-hyperalgesia)
