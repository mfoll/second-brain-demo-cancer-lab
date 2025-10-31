---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/selection/selection-log-2025-10-17.parquet
access: guarded-write
last_checked: 2026-09-15
date_accessed: 2025-10-17
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[northvale-matching-specification-v2]]"
  - "[[northvale-control-replacement-log]]"
_organized: true
---

# Northvale Sample Selection Log

## Summary

The frozen record of case and control selection: one row per selected sample with matched-set identifier, role, index date, matching values, fallback flag and biobank sample identifier. Frozen on 2025-10-17 when all aliquots were reconciled.

## Key Details

- 1,230 rows: 410 cases (174 pancreatic, 236 colorectal), 820 controls in 410 matched sets.
- 41 people appear as controls in more than one set; 6 controls later became cases themselves, which is expected under [[incidence-density-sampling]].
- Fallback rules used in 21 matched sets.
- Superseded rows are never edited; changes go into [[northvale-control-replacement-log]], and the analysis reads both.

## Source Location

Governed storage on [[halyard-cluster]], `halyard_governed/northvale/selection/`. Pseudonymised identifiers only.
