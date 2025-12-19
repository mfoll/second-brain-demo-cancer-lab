---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1016/j.ajhg.2023.12.002
doi: 10.1016/j.ajhg.2023.12.002
pmid: "38181732"
licence: cc by
date_accessed: 2025-12-04
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[pleiotropy]]"
  - "[[hiroshi-tanabe]]"
_organized: true
---

# A Bayesian approach to Mendelian randomization using summary statistics in the univariable and multivariable settings with correlated pleiotropy.

Grant AJ, Burgess S. American Journal of Human Genetics, 2024.

## Summary

Polygenic MR gains power from many instruments but also more chances that some are invalid. Correlated pleiotropy, where variants act on the outcome through a shared factor that also affects the exposure, breaks a key assumption of several common robust methods. The authors propose a Bayesian framework (MR-Horse) that gives valid inference under more general conditions, for one or several exposures.

## Why It Matters

On [[hiroshi-tanabe]]'s first-read list. Correlated pleiotropy is the specific failure we fear for CH: a shared ageing or telomere-length factor could drive both CH and cancer. A method that tolerates it is a candidate for the sensitivity set in any CH analysis. See [[pleiotropy]].

## Key Details

Works from summary statistics, so it fits a two-sample design. Multivariable extension could adjust for genetically predicted smoking.

## Caveats

Bayesian priors and computational cost; [[lucas-brandt]] has not tried it yet. Not yet compared by us against [[tang-2025-pleiotropic-clustering-mendelian-randomization]].

## Source Links

- [A Bayesian approach to Mendelian randomization with correlated pleiotropy](https://doi.org/10.1016/j.ajhg.2023.12.002)
