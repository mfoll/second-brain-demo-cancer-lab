---
type: Note
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[classifier-design-review-2026-04-02]]"
  - "[[lab-meeting-2026-03-12]]"
_archived: true
_organized: true
---

# Gradient-Boosting-Only Classifier Plan

> [!warning]
> Superseded. Gradient boosting on all features overfitted St Aldric extraction batches; see the [[lab-meeting-2026-03-12|2026-03-12 lab meeting]] and the stacked design adopted at the [[classifier-design-review-2026-04-02|2026-04-02 review]]. Kept for provenance because the submitted manuscript used this model.

## Original Plan (2025-09-24)

Written by Sofia and Dmitri for the [[fragmentomics-classifier|Fragmentomics Classifier]].

- One gradient-boosting model (LightGBM) on all fragment-length and end-motif features, about 860 inputs.
- Five-fold cross-validation stratified by recurrence status, repeated ten times.
- Hyperparameters by nested cross-validation: depth 3–6, learning rate 0.01–0.1, 200–1,000 trees.
- Threshold at 95% specificity on out-of-fold predictions.
- Rationale: boosting handles feature interactions and mixed scales without much preprocessing, and was the best performer in a quick comparison on 400 samples (AUC 0.89 against 0.84 for logistic regression).

## What Went Wrong

The folds were random, not batch-aware, and the extraction lot was confounded with time point ([[extraction-kit-lot-change-2025-06-16]]). The comparison that favoured boosting was therefore measuring how well each model learned the batch.

## Successor

[[classifier-model-card-v2]].
