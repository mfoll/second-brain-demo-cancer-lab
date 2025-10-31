---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/ch-subcohort/sampling-frame-2025-10.parquet
access: guarded-write
last_checked: 2026-09-21
date_accessed: 2025-10-10
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[lucas-brandt]]"
  - "[[ch-subcohort-data-access-approval]]"
_organized: true
---

# CH Subcohort Sampling Frame

## Summary

The list of 6,000 Northvale participants selected at random for buffy coat sequencing in the [[ch-cancer-risk-analysis]], drawn by [[lucas-brandt]] on 2025-10-10.

## Key Details

- Eligible: participants with at least 200 ng of buffy coat DNA in the [[corvane-biobank]] and no cancer before blood draw (79,850 people).
- Simple random sample without stratification, fixed seed; Lucas argued that a random subcohort keeps the analysis a straightforward cohort analysis and leaves the door open to case-cohort designs for later outcomes.
- 86 participants overlap with the Northvale case-control set (31 cases, 55 controls), as expected by chance.
- Median age at blood draw 56; 52% women.

## Caveats

Not enriched for cancer cases, so site-specific analyses are small; accepted at planning.

## Source Location

Governed storage on [[halyard-cluster]], `halyard_governed/northvale/ch-subcohort/`.
