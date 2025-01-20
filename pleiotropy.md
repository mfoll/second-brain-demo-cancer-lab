---
type: Concept
maturity: Growing
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[instrumental-variable-assumptions]]"
  - "[[clonal-hematopoiesis]]"
_organized: true
---

# Pleiotropy

When one genetic variant influences more than one trait. In Mendelian randomization it matters in two forms.

## Vertical And Horizontal

- Vertical pleiotropy: the variant affects the exposure, which in turn affects the outcome. This is the path MR wants to measure and is harmless.
- Horizontal pleiotropy: the variant affects the outcome through a path that bypasses the exposure. This violates the exclusion restriction ([[instrumental-variable-assumptions]]) and biases estimates.

Horizontal pleiotropy can be balanced (direct effects average to zero across instruments) or directional. It can also be correlated: variants act on both exposure and outcome through a shared factor, which defeats methods that assume direct effects are independent of instrument strength. [[grant-2024-bayesian-mendelian-randomization-correlated-pleiotropy]] and [[tang-2025-pleiotropic-clustering-mendelian-randomization]] target this case; [[van-der-graaf-2025-mr-link-2]] handles it within a single region.

## Why It Dominates For CH

The germline loci that predispose to [[clonal-hematopoiesis]] include telomere-length and DNA repair genes. A variant that lengthens telomeres raises the chance of a clonal expansion in blood and may raise the chance of a clonal expansion in the pancreas through the same biology. An MR estimate would then credit CH with an effect that comes from the shared factor. [[hiroshi-tanabe]] calls this the central problem; [[lucas-brandt]] flags such variants in [[ch-instrument-shortlist]].

## Practical Consequence

Use sensitivity methods with different assumptions and read disagreement between them as evidence of pleiotropy, not as noise.
