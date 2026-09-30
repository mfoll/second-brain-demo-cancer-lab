---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/registry/extract-2025/
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-09-08
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[registry-linkage-agreement]]"
  - "[[daniel-asante]]"
_organized: true
---

# Northern Cancer Registry Extract 2025

## Summary

The registry linkage for the whole Northvale cohort with cancer incidence and deaths to 2025-12-31, the first delivered under the institute [[registry-linkage-agreement]]. Received on 2026-09-08 ([[registry-extract-received-2026-09-08]]).

## Key Details

- Variables as in [[registry-linkage-variable-specification]], now including underlying and contributing causes of death.
- Linkage: 99.2% deterministic on the pseudonymised key, 412 records resolved probabilistically by the registry, 37 unlinked.
- New since 2023: 97 first primary pancreatic or colorectal cancers (35 pancreatic, 62 colorectal) diagnosed in 2024 and 2025.
- Revisions to earlier records: diagnosis dates for 2023 cancers corrected in 1.8% of records; 3 controls in the nested set found to have been diagnosed before their index date ([[northvale-control-replacement-log]]).
- Completeness for 2025 diagnoses estimated by [[daniel-asante]] at about 95% ([[registry-reporting-lag]]).

## Caveats

2025 incidence is provisional and will change in a 2027 refresh. Analyses should treat the last year as incomplete.

## Source Location

Governed storage on [[halyard-cluster]], `halyard_governed/northvale/registry/extract-2025/`. Access logged by [[yara-castellanos]].
