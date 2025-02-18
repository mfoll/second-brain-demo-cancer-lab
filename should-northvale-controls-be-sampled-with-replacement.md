---
type: Question
status: Answered
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[incidence-density-sampling]]"
  - "[[shin-2024-nested-case-control-sampling-without-replacement]]"
_organized: true
---

# Should Northvale controls be sampled with replacement?

## Question

Under incidence-density sampling a person can be selected as a control for more than one case, and a control can later become a case. Should we allow this, or exclude previously selected controls from later risk sets?

## Current Answer

Answered in March 2025: sample with replacement, as in the standard design. Implemented in [[northvale-matching-specification-v2]]. In the final set, 41 people are controls in more than one matched set and 6 controls later became cases ([[northvale-sample-selection-log]]).

## Why

- Standard sampling with replacement gives unbiased odds ratios that estimate the hazard ratio with the usual [[conditional-logistic-regression]]; that was the planned analysis.
- Sampling without replacement can be more efficient ([[shin-2024-nested-case-control-sampling-without-replacement]]) but needs weighted estimators, which complicates the window analysis.
- A person used twice costs one assay, not two: their sample is measured once and reused, which saves money.

## Caveat

Excluding people who later became cases from the control pool would have biased results; [[maja-kovac]] checked the sampling code for this explicitly.
