---
type: Question
status: Answered
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[registry-reporting-lag]]"
  - "[[northvale-control-replacement-log]]"
  - "[[daniel-asante]]"
_organized: true
---

# Does registry lag misclassify recent Northvale controls?

## Question

Controls must be cancer-free at their case's index date. If the registry had not yet recorded a cancer when the 2023 extract was produced, a control could have been an undiagnosed or unregistered case. How large is the problem?

## Current Answer

Small and now fixed for the current set. The 2025 extract showed three of 820 controls had a cancer diagnosed before their index date but registered late; all three were replaced ([[northvale-control-replacement-log]]). All three index dates were in 2023, the last year of the old extract.

## Rule going forward

Do not select controls for index dates in the most recent 24 months of an extract without a refresh, per [[daniel-asante]]'s completeness figures ([[registry-reporting-lag]]). Applies to any second case set from the 2025 extract.
