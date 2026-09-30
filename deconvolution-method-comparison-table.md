---
type: Source
source_type: Internal results table
date_accessed: 2026-09-30
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[low-count-spot-collapse]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# Deconvolution Method Comparison Table

Kenji's summary table of the seven methods across UMI depths, regenerated on Halyard on 2026-09-30. Values below are the 8 µm results averaged over the nine full-reference slides.

| Method | Family | Corr. at 400 UMIs | Corr. at 50 UMIs | Behaviour below 60 UMIs | Flagged by own output |
| --- | --- | --- | --- | --- | --- |
| M1 | Probabilistic | 0.86 | 0.61 | Noisy, unbiased | Partly |
| M2 | Regression | 0.83 | 0.55 | Noisy, unbiased | No |
| M3 | Regression | 0.85 | 0.22 | Collapse to hepatocyte | No |
| M4 | NMF | 0.74 | 0.40 | Near-uniform | No |
| M5 | Probabilistic | 0.87 | 0.19 | Collapse to hepatocyte | No |
| M6 | Cluster-based | 0.80 | 0.66 | Smoothed, unbiased | Not applicable |
| M7 | Deep learning | 0.82 | n/a | Refuses below 80 UMIs | Yes |

## Reading It

Averaged over all depths, M3 and M5 rank third and fourth; the collapse only appears when results are split by depth ([[low-count-spot-collapse]]). The cluster-based method is the most robust at low depth at the cost of resolution.

## Source Location

`results/summary/comparison_table.tsv` in [[deconvolution-benchmark-repository]], run tag `halyard-2026-09-30`.
