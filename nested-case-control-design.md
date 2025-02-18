---
type: Concept
maturity: Evergreen
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[incidence-density-sampling]]"
  - "[[conditional-logistic-regression]]"
  - "[[molecular-epidemiology]]"
_organized: true
---

# Nested Case-Control Design

A case-control study drawn from inside a defined cohort: all (or a sample of) incident cases, and for each case a small number of controls sampled from the people still at risk when the case occurred. Exposures are measured only in the selected people, often from stored samples collected before anyone was ill.

## Why use it

When the exposure measurement is expensive, such as a methylation panel on stored plasma, measuring 1,230 people instead of 86,400 makes a study possible. With controls sampled from risk sets ([[incidence-density-sampling]]), the odds ratio estimates the hazard ratio that the full cohort would give, with some loss of precision.

## Main choices

- Number of controls per case: gains flatten beyond four or five; we use two for budget reasons ([[are-two-controls-per-case-enough-for-northvale]]).
- Matching factors: anything that affects the measurement and is not of interest, such as sample storage time ([[matching-on-blood-draw-date-is-worth-the-cost]]).
- Analysis: [[conditional-logistic-regression]] on the matched sets.

## Compared with case-cohort

A case-cohort design uses one random subcohort for all outcomes, which suits studies with many outcomes. Northvale chose nested case-control for two cancers ([[northvale-case-cohort-option]]); the [[ch-cancer-risk-analysis]] uses a random subcohort because it studies all solid cancers.

## Reading

[[partlett-2020-matched-nested-case-control-design]], [[oakey-2023-nested-case-control-omics-protocol]], [[keogh-2018-multiple-imputation-nested-case-control]].
