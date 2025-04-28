---
type: Procedure
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[sofia-reyes-calderon]]"
  - "[[classifier-model-card-v2]]"
  - "[[model-stacking]]"
_organized: true
---

# Fragmentomics Classifier Retraining

How to retrain the stacked [[fragmentomics-classifier|fragmentomics classifier]] and decide whether the new version replaces the current one. Owner: [[sofia-reyes-calderon|Sofia Reyes Calderon]]. Written after the [[classifier-design-review-2026-04-02|2026-04-02 review]].

## When

New St Aldric samples, a new feature matrix version, a change in feature code, or a change to batch correction. Not after looking at external validation data: a locked model is never retrained on its validation set ([[external-validation-before-locking-a-classifier]]).

## Steps

1. **Freeze inputs**: record feature matrix version ([[fragmentomics-feature-matrix-v5]] or later), container image digest, and code commit.
2. **Batch correction** of fragment-length features, fitted on training folds only.
3. **Folds**: leave-one-extraction-batch-out. Random folds are reported only as a secondary number.
4. **Base models**: L2 logistic regression on length features; gradient boosting on end-motif features. Hyperparameters by inner leave-batch-out loop.
5. **Meta-learner**: logistic regression on out-of-fold base scores from the same folds.
6. **Report**: within-batch and leave-batch-out AUC, sensitivity at 95% specificity, and a batch-prediction check (can the length features predict the batch? AUC above 0.65 is a red flag).
7. **Compare** with the current model card. Replace only if leave-batch-out performance does not drop and the batch-prediction check passes.
8. **Update the model card** and commit; announce in the Thursday check-in.

## Verification

Dmitri reviews steps 6–7 before a new version is used in any manuscript analysis. Runs on Halyard through the Nextflow pipeline ([[nextflow-pipeline-migration]]).
