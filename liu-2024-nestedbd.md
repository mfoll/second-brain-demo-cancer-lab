---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s13015-024-00264-4
doi: 10.1186/s13015-024-00264-4
pmid: "38685065"
licence: cc by
date_accessed: 2025-02-03
belongs_to: "[[single-cell-cnv-pilot]]"
related_to:
  - "[[multi-region-bulk-phylogeny]]"
  - "[[tumour-evolution]]"
_organized: true
---

# NestedBD: Bayesian inference of phylogenetic trees from single-cell copy number profiles under a birth-death model.

Liu Y et al., Algorithms for Molecular Biology, 2024.

## Summary

Introduces a birth-death model of copy-number change and a Bayesian method that infers tree topology and branch lengths from single-cell copy-number data. In simulations it gives more accurate topologies and branch lengths than traditional and recent tools, and the model can improve copy-number estimates. Applied to two colorectal cancer samples, it gives plausible evolutionary histories.

## Why It Matters

The colorectal application made it the Bayesian option in [[felix-achterberg]]'s comparison in the [[single-cell-cnv-pilot]]. Its runtime was the limiting factor at our cell numbers.

## Caveats

Two real samples; assessment of real-data trees is qualitative.

## Source Links

- [DOI 10.1186/s13015-024-00264-4](https://doi.org/10.1186/s13015-024-00264-4)
