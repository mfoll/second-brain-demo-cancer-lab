---
type: Source
source_type: Scientific paper
url: https://doi.org/10.26508/lsa.202402923
doi: 10.26508/lsa.202402923
pmid: "39667913"
licence: cc by
date_accessed: 2025-02-17
belongs_to: "[[single-cell-cnv-pilot]]"
related_to:
  - "[[multi-region-bulk-phylogeny]]"
  - "[[felix-achterberg]]"
_organized: true
---

# DICE: fast and accurate distance-based reconstruction of single-cell copy number phylogenies.

Weiner S et al., Life Science Alliance, 2025.

## Summary

Proposes two distance-based methods for building tumour phylogenies from single-cell copy-number profiles. On simulations, one matches or beats other methods on noise-free data and the other is notably robust to noise; both are much faster than many alternatives. The authors also show how strongly copy-number calling errors degrade most methods, and apply the noise-robust variant to breast and ovarian cancer data.

## Why It Matters

Its point about noise was the most useful lesson for the [[single-cell-cnv-pilot]]: tree accuracy depends more on per-cell call quality than on the tree method. [[felix-achterberg]] used it as the fast method in his three-way comparison.

## Caveats

Simulation-heavy; real-data reliability judged by comparison rather than ground truth.

## Source Links

- [DOI 10.26508/lsa.202402923](https://doi.org/10.26508/lsa.202402923)
