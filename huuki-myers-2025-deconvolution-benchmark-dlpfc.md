---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s13059-025-03552-3
doi: 10.1186/s13059-025-03552-3
pmid: "40197307"
licence: cc by
date_accessed: 2025-09-22
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[cell-type-deconvolution]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# Benchmark of cellular deconvolution methods using a multi-assay dataset from postmortem human prefrontal cortex.

Huuki-Myers LA et al., Genome Biology, 2025.

## Summary

Generates a multi-assay dataset from 22 blocks of human prefrontal cortex: bulk RNA-seq, a single-nucleus reference, and orthogonal cell-type proportions measured by RNAScope and immunofluorescence. Six bulk deconvolution algorithms are evaluated against these measured proportions, two coming out as most accurate. Data and a marker-finding method are released as an R/Bioconductor package.

## Why It Matters

The design we admire: orthogonal ground truth measured in the same tissue rather than simulated. We cannot afford that for 80 atlas sections, but [[kenji-mori]] considered RNAScope on a subset of fibrotic regions to confirm the low-count collapse in real tissue. It stayed a possible extension of the [[deconvolution-benchmark]].

## Caveats

Bulk deconvolution in brain, not spatial spots in liver.

## Source Links

- [DOI 10.1186/s13059-025-03552-3](https://doi.org/10.1186/s13059-025-03552-3)
