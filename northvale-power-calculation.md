---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/design/power-calculation-2025-04.html
access: guarded-write
last_checked: 2025-10-17
date_accessed: 2025-04-09
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[are-two-controls-per-case-enough-for-northvale]]"
  - "[[conditional-logistic-regression]]"
_organized: true
---

# Northvale Power Calculation

## Summary

Simulation-based power calculation for the nested case-control study, written by [[maja-kovac]] in April 2025. Rendered report with code.

## Key Details

- Assumed 400 to 420 eligible cases after the last-aliquot rule (the final count was 410).
- Effect sizes: odds ratio per standard deviation of 1.2, 1.3 and 1.5 for the pooled analysis, 2.0 or more within 2 years of diagnosis.
- Results: with two controls per case, power 0.83 for an odds ratio of 1.3 at alpha 0.05; three controls raised it to 0.88 at 50% higher assay cost; one control dropped it to 0.67.
- Window-specific power is poor beyond the first two windows unless the effect is large; stated plainly in the report and in the SAP.

## Caveats

Assumed a normally distributed score with equal variance in cases and controls. The observed score is right-skewed in the earliest window.

## Source Location

Group SharePoint, `group_docs/northvale/design/`.
