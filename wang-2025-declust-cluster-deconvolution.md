---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/nar/gkaf714
doi: 10.1093/nar/gkaf714
pmid: "40705925"
licence: cc by
date_accessed: 2025-12-01
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[how-to-handle-hepatocyte-dominance-in-deconvolution]]"
  - "[[cell-type-deconvolution]]"
_organized: true
---

# A cluster-based cell-type deconvolution of spatial transcriptomic data.

Wang Q et al., Nucleic Acids Research, 2025.

## Summary

Introduces DECLUST, which first finds spatial clusters of spots from expression and coordinates, then deconvolves the aggregated expression of each cluster. Pooling addresses the low expression of individual spots while keeping tissue structure. On simulated breast cancer and real ovarian cancer and mouse brain data it compares favourably with several established methods.

## Why It Matters

Read after the method freeze, so not in the [[deconvolution-benchmark]]. Its premise, that per-spot estimates fail at low expression, is the same problem as our [[low-count-spot-collapse]], solved by pooling. Our own cluster-based method (M6) behaved this way: robust at low depth, coarser. It is option 3 in [[how-to-handle-hepatocyte-dominance-in-deconvolution]].

## Caveats

Pooling loses exactly the fine structure (thin tumour rims) that made us choose Visium HD.

## Source Links

- [DOI 10.1093/nar/gkaf714](https://doi.org/10.1093/nar/gkaf714)
