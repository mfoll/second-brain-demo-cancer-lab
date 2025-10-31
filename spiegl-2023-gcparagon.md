---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/nargab/lqad102
doi: 10.1093/nargab/lqad102
pmid: "38025047"
licence: cc by
date_accessed: 2025-10-06
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[batch-confounding-in-cfdna-studies]]"
  - "[[cfdna-fragmentomics]]"
_organized: true
---

# GCparagon: evaluating and correcting GC biases in cell-free DNA at the fragment level

Spiegl B et al., NAR Genomics and Bioinformatics, 2023.

## Summary

Describes a two-stage algorithm that estimates GC bias from fragment length and GC base count while avoiding problematic regions, then writes per-fragment correction weights as BAM tags. It runs in under a minute per sample in parallel mode and improves signals at regulatory regions, which often have distinctive GC composition.

## Why It Matters

Sofia read it in 2025-10 while chasing unexplained between-run variation in short-to-long ratios. We implemented fragment-level GC weighting in our feature pipeline before computing window ratios ([[fragment-length-and-end-motif-features]]). It did not remove the extraction lot effect found later, which is not a GC effect, but it reduced run-to-run noise.

## Caveats

We did not adopt the tool itself; we reimplemented the weighting inside the pipeline so it could run in the same container. Worth revisiting for the Nextflow rewrite.

## Source Links

- [DOI 10.1093/nargab/lqad102](https://doi.org/10.1093/nargab/lqad102), PMID 38025047
