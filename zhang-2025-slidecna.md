---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s13059-025-03573-y
doi: 10.1186/s13059-025-03573-y
pmid: "40317049"
licence: cc by
date_accessed: 2025-11-10
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[can-spatial-cnv-replace-single-cell-dna]]"
  - "[[multi-region-bulk-phylogeny]]"
_organized: true
---

# SlideCNA: spatial copy number alteration detection from Slide-seq-like spatial transcriptomics data.

Zhang D et al., Genome Biology, 2025.

## Summary

Presents SlideCNA, which extracts copy-number signals from sparse near-cellular spatial transcriptomics by binning spots in an expression-aware way, balancing sparsity against spatial detail. Tested on simulated data and on Slide-seq of breast cancer and metastases, it shows potential for detecting spatial subclones.

## Why It Matters

The atlas has the same sparsity problem at 8 µm: per-bin counts are too low for copy-number inference, so bins must be pooled. Expression-aware pooling is the approach Amara adopted in the pipeline ([[atlas-spatial-pipeline-repository]]), rather than fixed 16 µm aggregation.

## Caveats

Slide-seq, not Visium HD; resolution of focal events remains limited.

## Source Links

- [DOI 10.1186/s13059-025-03573-y](https://doi.org/10.1186/s13059-025-03573-y)
