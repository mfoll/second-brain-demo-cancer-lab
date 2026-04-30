---
type: Source
source_type: Internal document
storage_system: Group Git repository
root_key: varga_lab_git
relative_path: mrd-fragmentomics-classifier/MODEL_CARD.md
access: guarded-write
last_checked: 2026-10-12
date_accessed: 2026-04-24
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[classifier-design-review-2026-04-02]]"
  - "[[fragmentomics-classifier-retraining]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# Classifier Model Card v2

Model card of the stacked [[fragmentomics-classifier|fragmentomics classifier]], version 2, committed by Sofia on 2026-04-24 after the [[classifier-design-review-2026-04-02|design review]]. Version 3, the locked version for external validation, is due by 2026-11-30.

## Model

- **Intended use**: research scoring of post-operative plasma for residual pancreatic cancer, as one layer of the MRD call. Not for clinical use.
- **Inputs**: [[fragmentomics-feature-matrix-v5]] columns; shallow WGS at 3x or more; reference build and aligner pinned.
- **Base model 1**: L2 logistic regression (C = 0.1) on 66 length bins, 541 window ratios and 4 summary features, after bridging correction (per-lot centring on 16 bridging samples).
- **Base model 2**: gradient boosting (LightGBM, depth 3, 400 trees, learning rate 0.03) on 256 end-motif frequencies and the motif diversity score. No correction.
- **Meta-learner**: logistic regression on out-of-fold base scores, weights 0.62 (length) and 0.38 (motif).
- **Threshold**: 95% specificity on leave-batch-out out-of-fold scores in recurrence-free patients.

## Performance (St Aldric, Leave-Batch-Out)

AUC 0.86; sensitivity 58% at 95% specificity (sample level). Batch-prediction check: final score predicts lot with AUC 0.57.

## Known Limitations

- One centre, two lots of one extraction kit.
- Bridging correction cannot be applied at a site without bridging or shared reference samples; for Halo, the healthy-donor tier of the [[halo-truth-set]] must play that role, since its contrived samples do not have plasma-like fragment profiles.
- Summary length features add nothing ([[classifier-feature-ablation-results]]) and will be removed in v3.

## Source Location

Group Git repository, `varga_lab_git/mrd-fragmentomics-classifier/MODEL_CARD.md`, tag `model-v2.0`.
