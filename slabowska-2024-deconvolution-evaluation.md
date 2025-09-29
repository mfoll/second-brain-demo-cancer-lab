---
type: Source
source_type: Scientific paper
url: https://doi.org/10.3389/fbinf.2024.1352594
doi: 10.3389/fbinf.2024.1352594
pmid: "38601476"
licence: cc by
date_accessed: 2025-09-08
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[cell-type-deconvolution]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# A systematic evaluation of state-of-the-art deconvolution methods in spatial transcriptomics: insights from cardiovascular disease and chronic kidney disease.

Slabowska AO et al., Frontiers in Bioinformatics, 2024.

## Summary

Compares three deconvolution methods (Cell2location, RCTD, spatialDWLS) on human cardiovascular and kidney disease tissue, using expert annotation as reference. All three perform comparably on verifiable cell types; one is slightly more accurate in vascular samples, another best on average and needs less reference data but more compute, and one is fastest and simplest to run. The authors conclude the best choice depends on the use case.

## Why It Matters

One of the first papers [[kenji-mori]] read when the [[deconvolution-benchmark]] started. It shaped the practical metrics we report (runtime, dependencies). It was not designed to examine low-count behaviour, which is the gap we argue about in [[benchmarks-must-report-failure-modes]].

## Caveats

Standard Visium spots, not Visium HD bins; non-cancer tissue; three methods. From the abstract, accuracy is summarised per method rather than by count depth.

## Source Links

- [DOI 10.3389/fbinf.2024.1352594](https://doi.org/10.3389/fbinf.2024.1352594)
