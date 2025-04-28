---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s13059-025-03553-2
doi: 10.1186/s13059-025-03553-2
pmid: "40197547"
licence: cc by
date_accessed: 2025-04-22
belongs_to: "[[single-cell-cnv-pilot]]"
related_to:
  - "[[felix-achterberg]]"
  - "[[tumour-evolution]]"
_organized: true
---

# CNRein: an evolution-aware deep reinforcement learning algorithm for single-cell DNA copy number calling.

Ivanovic S et al., Genome Biology, 2025.

## Summary

Low-pass single-cell DNA sequencing lets haplotype-specific copy number be called on thousands of cells, but measurement noise produces copy-number changes inconsistent with plausible evolution. CNRein uses deep reinforcement learning to call copy number under evolutionary constraints; in simulations it recovers profiles and clonal structure more accurately, and on breast and ovarian cancer data it gives more parsimonious solutions consistent with point mutations.

## Why It Matters

[[felix-achterberg]] added an evolution-aware caller to the [[single-cell-cnv-pilot]] after reading it, because spurious per-cell events were inflating tree size. It reduced the noise but did not make minor clades stable ([[single-cell-cnv-pilot-report]]).

## Caveats

Evaluated on breast and ovarian cancer; our tumours were colorectal.

## Source Links

- [DOI 10.1186/s13059-025-03553-2](https://doi.org/10.1186/s13059-025-03553-2)
