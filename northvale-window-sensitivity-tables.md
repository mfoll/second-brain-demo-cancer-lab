---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/results/interim-2026-07/tables/
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-07-17
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[time-to-diagnosis-windows]]"
  - "[[northvale-interim-results-2026-10]]"
_organized: true
---

# Northvale Window and Sensitivity Tables

## Summary

The interim results tables produced on 2026-07-17 after [[northvale-sap-amendment-1]], tag `interim-2026-07`. Superseded once the October re-run on the corrected control set is frozen.

## Key Details

Odds ratio per SD of methylation score, conditional logistic regression:

| Analysis | Cases | OR (95% CI) |
| --- | --- | --- |
| 0 to 1 year | 27 | 4.9 (2.6 to 9.3) |
| 1 to 2 years | 31 | 2.2 (1.3 to 3.7) |
| 2 to 5 years | 84 | 1.31 (0.98 to 1.75) |
| More than 5 years | 268 | 1.06 (0.91 to 1.23) |
| Main (exclude year 1) | 383 | 1.24 (1.06 to 1.45) |
| Sensitivity: exclude 6 months | 399 | 1.33 (1.14 to 1.55) |
| Sensitivity: no exclusion | 410 | 1.48 (1.27 to 1.72) |

Site-specific and storage-time models are in separate sheets; the storage sheet is incomplete.

## Caveats

Interim. Do not quote outside the group ([[northvale-collaboration-agreement]]).

## Source Location

Governed storage, `halyard_governed/northvale/results/interim-2026-07/tables/`.
