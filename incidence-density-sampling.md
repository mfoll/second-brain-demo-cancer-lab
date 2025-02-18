---
type: Concept
maturity: Evergreen
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[nested-case-control-design]]"
  - "[[should-northvale-controls-be-sampled-with-replacement]]"
_organized: true
---

# Incidence-Density Sampling

A way of choosing controls in a nested case-control study: for each case, controls are drawn at random from the people who are still under follow-up and free of the outcome on the case's diagnosis date (the risk set). Also called risk-set sampling.

## What follows from it

- A control is defined at a time point, not for ever. A person can be a control for one case and later become a case, and can be a control for several cases. Excluding future cases from the control pool introduces bias.
- The odds ratio from a matched analysis estimates the incidence rate ratio (hazard ratio), without a rare-disease assumption.
- The control inherits the case's index date; covariates are taken as of that date or as of baseline, consistently ([[northvale-date-definitions]]).

## In Northvale

Risk sets were further restricted by matching on sex, centre, age and blood-draw date, and by plasma availability ([[northvale-matching-specification-v2]]). 41 people are controls in more than one set; 6 controls later became cases.

## Variants

Sampling without replacement across risk sets can be more efficient but needs weighted analysis ([[shin-2024-nested-case-control-sampling-without-replacement]]).
