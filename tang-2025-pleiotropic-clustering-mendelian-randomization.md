---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-025-57912-5
doi: 10.1038/s41467-025-57912-5
pmid: "40118820"
licence: cc by-nc-nd
date_accessed: 2026-01-15
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[pleiotropy]]"
  - "[[grant-2024-bayesian-mendelian-randomization-correlated-pleiotropy]]"
_organized: true
---

# Leveraging pleiotropic clustering to address high proportion correlated horizontal pleiotropy in Mendelian randomization studies.

Tang B et al., Nature Communications, 2025.

## Summary

Proposes PCMR, which clusters variants to detect correlated horizontal pleiotropy and extends the zero-modal pleiotropy assumption. In simulations it detected correlated pleiotropy and avoided false positives even when such variants made up 30 to 40% of those linking the traits. Across 48 exposure and common-disease pairs it flagged correlated pleiotropy in seven.

## Why It Matters

A complement to [[grant-2024-bayesian-mendelian-randomization-correlated-pleiotropy]]: one models correlated pleiotropy, the other tries to find and separate it. For CH the instrument set will be small, so a clustering approach may simply not have enough variants. [[lucas-brandt]] noted this on 2026-01-15.

## Caveats

Designed for exposures with many instruments. Whether it behaves with ten or fewer is unclear from the abstract.

## Source Links

- [Leveraging pleiotropic clustering in Mendelian randomization](https://doi.org/10.1038/s41467-025-57912-5)
