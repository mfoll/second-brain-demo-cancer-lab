---
type: Concept
maturity: Evergreen
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[low-count-spot-collapse]]"
_organized: true
---

# Cell-Type Deconvolution

Estimating the cell-type composition of a mixed measurement (a bulk sample, a spatial spot or bin) from its expression profile, usually with a single-cell reference that defines each cell type's expected profile.

## Families

- Reference-based probabilistic models: count likelihood per cell type, priors on abundance.
- Regression-based: non-negative least squares or weighted regression on marker genes ([[chen-2024-nlsdeconv]] is a recent example).
- Matrix factorisation (NMF) with or without a reference.
- Cluster- or neighbourhood-based: pool spatially and transcriptionally similar spots before estimating, which trades resolution for counts ([[wang-2025-declust-cluster-deconvolution]]).
- Deep learning on pseudo-spots built from the reference ([[wang-2025-harmodecon]]).

## What Decides Accuracy in Practice

- The reference: missing cell types, platform differences and tissue mismatch ([[which-reference-for-liver-metastasis-deconvolution]]).
- Counts per spot: at Visium HD 8 µm resolution, many bins are in the low-count regime where [[low-count-spot-collapse]] occurs.
- Majority cell types: in liver tissue hepatocytes dominate, which biases priors ([[how-to-handle-hepatocyte-dominance-in-deconvolution]]).

## In the Group

Benchmarked in the [[deconvolution-benchmark]]; the atlas chooses its method from that result. Bulk deconvolution of methylation data, relevant to cfDNA tissue-of-origin, follows the same logic; [[amblard-2025-deconvolution-benchmark-workflow]] covers both omics.
