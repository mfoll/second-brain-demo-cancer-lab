---
type: Concept
maturity: Growing
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[pleiotropy]]"
  - "[[collider-bias]]"
  - "[[burgess-2019-guidelines-mendelian-randomization]]"
_organized: true
---

# Instrumental Variable Assumptions

The three conditions a genetic variant must meet to serve as an instrument in Mendelian randomization. Everything in the [[mendelian-randomization]] cluster comes back to whether these hold.

## The Three Assumptions

1. Relevance: the variant is associated with the exposure. Testable; weak instruments bias two-sample estimates towards the null and one-sample estimates towards the observational association.
2. Independence: the variant is not associated with confounders of the exposure-outcome relationship. Usually argued from random allocation at conception, but broken by population structure, assortative mating and selection into the sample ([[gkatzionis-2019-selection-bias-mendelian-randomization]]).
3. Exclusion restriction: the variant affects the outcome only through the exposure. Not testable directly; violations are horizontal [[pleiotropy]].

## How They Apply To CH

For clonal hematopoiesis as exposure and incident cancer as outcome ([[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]]):

- Relevance is weak: known germline variants explain little of who develops CH ([[ch-instrument-shortlist]]).
- Independence is probably fine for most variants in Northvale, which is a single-ancestry cohort recruited at 40 to 69, though survival to enrolment matters for discovery GWAS in older samples ([[smit-2019-survival-bias-mendelian-randomization]]).
- Exclusion is the real problem: several CH predisposition loci act on telomere maintenance or DNA repair, which plausibly affect solid tumour risk directly ([[liu-2025-germline-variation-clonal-hematopoiesis]]).

## Working Rule

Treat relevance as measurable, independence as arguable, exclusion as assumed and probed by sensitivity analyses. Report all three explicitly, as [[burgess-2019-guidelines-mendelian-randomization]] asks.
