---
type: Note
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[fragment-length-and-end-motif-features]]"
  - "[[sofia-reyes-calderon]]"
  - "[[classifier-stacking-evaluation-2026-04]]"
_organized: true
---

# Classifier Feature Ablation Results

Sofia's ablation of the stacked [[fragmentomics-classifier|fragmentomics classifier]], run in 2026-05 on feature matrix v5 ([[fragmentomics-feature-matrix-v5]]) with leave-batch-out folds. Draft for the revision supplement.

## Results (Leave-Batch-Out AUC)

| Removed | AUC | Change |
|---|---|---|
| Nothing (full stacked model) | 0.86 | |
| Short-to-long window ratios | 0.80 | -0.06 |
| Length histogram bins | 0.84 | -0.02 |
| Periodicity and summary length features | 0.86 | 0.00 |
| All 256 end-motif frequencies (keep diversity score) | 0.83 | -0.03 |
| Motif diversity score | 0.85 | -0.01 |

## Reading

- Window ratios carry most of the length signal; summary features add nothing once ratios are in, and will be dropped in model card v3 to simplify.
- The motif family contributes about 0.03, consistent with the stacking evaluation.
- Without batch correction, window ratios gain within-batch but lose 0.05 across batches; correction stays mandatory.

## Caveat

All numbers are St Aldric only, with two lots of the same kit. See [[does-the-stacked-classifier-generalise-across-extraction-batches]].
