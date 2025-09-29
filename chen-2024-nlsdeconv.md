---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioinformatics/btae747
doi: 10.1093/bioinformatics/btae747
pmid: "39705170"
licence: cc by
date_accessed: 2025-09-15
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[cell-type-deconvolution]]"
  - "[[deconvolution-benchmark-config]]"
_organized: true
---

# NLSDeconv: an efficient cell-type deconvolution method for spatial transcriptomics data.

Chen Y et al., Bioinformatics, 2024.

## Summary

A short paper introducing a deconvolution method based on non-negative least squares, released as a Python package. Benchmarked against 18 existing methods on several spatial datasets, it is statistically competitive and much faster.

## Why It Matters

Its comparison of 18 methods helped [[kenji-mori]] pick seven that span model families for the [[deconvolution-benchmark]] ([[deconvolution-benchmark-config]]). It also reminded us that a simple regression baseline belongs in any benchmark.

## Caveats

The abstract reports overall performance; we did not see results split by count depth.

## Source Links

- [DOI 10.1093/bioinformatics/btae747](https://doi.org/10.1093/bioinformatics/btae747)
