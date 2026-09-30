---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/selection/control-replacements-2026-09.csv
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-09-15
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[northvale-sample-selection-log]]"
  - "[[does-registry-lag-misclassify-recent-northvale-controls]]"
  - "[[registry-reporting-lag]]"
_organized: true
---

# Northvale Control Replacement Log

## Summary

Changes to the frozen case-control set after the 2025 registry extract, made on 2026-09-15 and approved by [[mei-lin-zhou]] on 2026-09-18.

## Key Details

- Three controls had a cancer diagnosis registered after the 2023 extract with a diagnosis date before their matched case's index date, so they were not truly cancer-free at the index date. Two were colorectal, one breast. Each was replaced by a new control from the same risk set under [[northvale-matching-specification-v2]] rules. The three replacement aliquots were requested from the biobank under the original approval and assayed in the October run.
- Four cases had diagnosis dates corrected by 11 to 57 days. None moved between [[time-to-diagnosis-windows]].
- No case lost eligibility.

## Caveats

The replaced controls' methylation data remain in the data release, flagged, for a sensitivity check (they are, in effect, cases with more than 14 years from blood draw to diagnosis).

## Source Location

Governed storage on [[halyard-cluster]], `halyard_governed/northvale/selection/`.
