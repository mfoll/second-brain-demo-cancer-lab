---
type: Source
source_type: Slide deck
storage_system: Group shared drive
root_key: varga_lab_drive
relative_path: mrd-study/classifier/batch-analysis-2026-03-12.pdf
access: read-only
last_checked: 2026-04-02
date_accessed: 2026-03-12
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[lab-meeting-2026-03-12]]"
  - "[[batch-confounding-in-cfdna-studies]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# Classifier Batch Effect Analysis 2026-03

Sofia's slide deck presented at the [[lab-meeting-2026-03-12|lab meeting of 2026-03-12]].

## Key Findings

- Gradient boosting on all features: within-batch cross-validated AUC 0.91, leave-batch-out 0.74.
- The same features predict extraction lot (A vs B) with AUC 0.88; sequencing run predicts much less once lot is accounted for.
- Top feature importances: fragment-length bins at 160–172 bp and the sub-150 bp fraction, exactly where the lot shift sits (modal length about 3 bp shorter on lot B).
- Lot B holds 71% of follow-up samples and 18% of pre-operative samples ([[cfdna-extraction-qc-log-2025]]).
- A quick L2 logistic model: 0.80 within batch, 0.78 leave-batch-out.

## Why It Matters

Basis of the March decision to drop gradient boosting, and of the later analysis by feature family ([[classifier-stacking-evaluation-2026-04]]) that partly reversed it. Also the evidence Reviewer 1 will see on pre-analytical variation ([[mrd-revision-response-plan]]).

## Source Location

Group shared drive, `varga_lab_drive/mrd-study/classifier/batch-analysis-2026-03-12.pdf`.
