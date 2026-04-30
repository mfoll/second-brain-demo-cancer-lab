---
type: Source
source_type: Slide deck
storage_system: Group shared drive
root_key: varga_lab_drive
relative_path: mrd-study/classifier/stacking-evaluation-2026-04-02.pdf
access: read-only
last_checked: 2026-04-20
date_accessed: 2026-04-02
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[classifier-design-review-2026-04-02]]"
  - "[[model-stacking]]"
_organized: true
---

# Classifier Stacking Evaluation 2026-04

Sofia's slide deck for the [[classifier-design-review-2026-04-02|classifier design review of 2026-04-02]].

## Key Findings

- Feature-family split under leave-batch-out folds: gradient boosting on end motifs 0.77, logistic on end motifs 0.72; logistic on bridging-corrected length features 0.81, gradient boosting on the same 0.75.
- End-motif features predict extraction lot with AUC 0.56, close to chance; length features 0.88 raw and 0.61 after bridging correction.
- Stacked model (logistic on length, boosting on motifs, logistic meta-learner on out-of-fold scores): 0.88 within batch, 0.86 leave-batch-out; sensitivity 58% at 95% specificity for any-time recurrence, sample level.
- Meta-learner weights: 0.62 length score, 0.38 motif score.

## Why It Matters

The evidence for the stacked design now recorded in [[classifier-model-card-v2]].

## Source Location

Group shared drive, `varga_lab_drive/mrd-study/classifier/stacking-evaluation-2026-04-02.pdf`.
