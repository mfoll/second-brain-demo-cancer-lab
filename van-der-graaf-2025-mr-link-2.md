---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-025-60868-1
doi: 10.1038/s41467-025-60868-1
pmid: "40610416"
licence: cc by
date_accessed: 2026-02-19
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[pleiotropy]]"
  - "[[ch-instrument-shortlist]]"
_organized: true
---

# MR-link-2: pleiotropy robust cis Mendelian randomization validated in three independent reference datasets of causality.

van der Graaf A et al., Nature Communications, 2025.

## Summary

When instruments come from a single genomic region, as is typical for molecular exposures, standard MR inflates type 1 error. MR-link-2 uses summary statistics and linkage disequilibrium to estimate both the causal effect and pleiotropy within one region. It was calibrated in simulations and outperformed other cis-MR methods on reference sets of known metabolic and complex-trait causal links.

## Why It Matters

[[hiroshi-tanabe]] raised it on the 2026-02-19 call. Some of the strongest CH instruments are single loci with a clear mechanism, for example a region acting on one CH driver gene. A cis design around such a locus might be cleaner than a polygenic score that mixes mechanisms. Added as an option in [[ch-instrument-shortlist]].

## Caveats

Cis-MR answers a narrower question (the effect of perturbing one pathway), which is not the same as "does CH cause cancer". Needs LD reference matched to the GWAS ancestry.

## Source Links

- [MR-link-2](https://doi.org/10.1038/s41467-025-60868-1)
