---
type: Concept
maturity: Seed
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[instrumental-variable-assumptions]]"
  - "[[reverse-causation-in-prediagnostic-studies]]"
_organized: true
---

# Collider Bias

Bias that appears when an analysis conditions on a variable caused by two others (a collider), opening a spurious path between them. Selecting a sample, stratifying, or adjusting for a collider can all create an association where none exists.

## Where We Meet It

- Selection into a cohort: if enrolment depends on health, and health depends on both a genetic instrument and confounders, the instrument becomes associated with confounders in the sample ([[gkatzionis-2019-selection-bias-mendelian-randomization]]).
- Survival: only people who survived to enrolment are measured ([[smit-2019-survival-bias-mendelian-randomization]]).
- Stratification by a variable the exposure affects ([[coscia-2022-collider-bias-stratified-mendelian-randomization]]).

Outside MR, the same logic applies to the Northvale case-control work: conditioning on having a stored, usable blood sample is a mild form of selection that [[maja-kovac]] discusses alongside [[reverse-causation-in-prediagnostic-studies]].

## Rule Of Thumb

Before stratifying or restricting, draw the causal diagram and ask what the restriction variable is caused by.
