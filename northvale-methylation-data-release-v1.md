---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/methylation/release-v1.1/
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-01-30
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[methylation-panel-design]]"
  - "[[northvale-case-control-codebook]]"
  - "[[tobias-wren]]"
_organized: true
---

# Northvale Methylation Data Release v1

## Summary

Processed methylation data for the 1,230 Northvale case-control plasma samples assayed with the 1,840-region panel: region-level methylation fractions, coverage, the per-sample score, and QC metrics. Release 1.0 frozen on 2026-01-30, before the SAP was signed; release 1.1 (2026-10-12) adds the three replacement controls.

## Key Details

- Produced by the panel pipeline maintained by [[tobias-wren]]: release 1.0 on the old Kestrel cluster, release 1.1 on [[halyard-cluster]] after the migration, with the container image digest recorded in each manifest. Tobias checked that re-running 20 samples on Halyard reproduced the 1.0 scores exactly.
- Median unique coverage 412x per region; 9 samples below the 150x QC threshold were re-sequenced, all passed.
- The score was computed blind: case-control status was held by [[yara-castellanos]] and joined only after SAP sign-off.
- Columns described in [[northvale-case-control-codebook]].

## Caveats

Score weights come from tissue data; plasma background from blood cells is not removed. See [[can-ch-explain-part-of-the-northvale-methylation-signal]].

## Source Location

Governed storage, `halyard_governed/northvale/methylation/release-v1.1/`. Release 1.0 kept read-only alongside.
