---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s13059-025-03897-9
doi: 10.1186/s13059-025-03897-9
pmid: "41408313"
licence: cc by
date_accessed: 2026-01-14
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[benchmarks-must-report-failure-modes]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# A robust workflow to benchmark deconvolution of multi-omic data.

Amblard E et al., Genome Biology, 2025.

## Summary

Presents an evaluation framework for deconvolution algorithms across transcriptomic and methylation data, covering reference-based and reference-free methods. Beyond raw accuracy it measures stability and computational cost under perturbations such as missing or extra cell types and varied compositions, includes a new multi-omics dataset, and ships as a containerised, reproducible workflow.

## Why It Matters

Read in January 2026 while we wrote the methods section. It is the closest published benchmark to our view that robustness under realistic perturbations matters as much as average accuracy ([[benchmarks-must-report-failure-modes]]). Its missing-cell-type scenarios match our leave-one-out design. The methylation side is relevant to cfDNA tissue-of-origin work in the [[pancreatic-cfdna-mrd-study]]; flagged to [[dmitri-halvorsen]].

## Caveats

Bulk data; spatial count depth is not one of its perturbations.

## Source Links

- [DOI 10.1186/s13059-025-03897-9](https://doi.org/10.1186/s13059-025-03897-9)
