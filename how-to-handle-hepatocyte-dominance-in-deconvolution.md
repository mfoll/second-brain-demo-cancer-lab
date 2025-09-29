---
type: Question
status: Open
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[low-count-spot-collapse]]"
  - "[[colorectal-metastasis-atlas]]"
_organized: true
---

# How To Handle Hepatocyte Dominance In Deconvolution?

Liver metastasis sections are dominated by hepatocytes in the adjacent liver, and two benchmarked methods collapse low-count spots onto hepatocytes. How should the atlas deconvolve without that bias leaking into before-and-after comparisons?

## Options Under Discussion

1. Flag and exclude spots below a per-method count threshold, report results with and without them.
2. Deconvolve within pathologist-annotated regions with region-specific priors, so tumour and fibrosis regions do not inherit the liver's abundance.
3. Use a method that pools neighbouring spots before estimating, trading resolution for counts ([[wang-2025-declust-cluster-deconvolution]]).
4. Down-weight hepatocytes in the reference.

## Current Leaning

Options 1 and 2 together. Option 4 was tried in the benchmark and moved the collapse to the next most abundant type (cholangiocytes in one slide), so it treats the symptom.

## Owner

[[kenji-mori]] proposes, Amara decides for the atlas, by the analysis-set freeze.
