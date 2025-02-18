---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/registry/extract-2023/
access: guarded-write
last_checked: 2026-09-15
date_accessed: 2025-02-03
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[northern-cancer-registry-extract-2025]]"
  - "[[registry-reporting-lag]]"
_organized: true
---

# Northern Cancer Registry Extract 2023

## Summary

The registry linkage for the Northvale cohort with follow-up to 2023-12-31, delivered to the cohort team in November 2024 under a cohort-specific approval and released to us at the start of the [[northvale-early-detection-study]]. Basis for case selection.

## Key Details

- First primary cancers with ICD-10 site, morphology, diagnosis date, basis of diagnosis and stage where available; deaths with date and underlying cause.
- 1,214 first primary pancreatic (312) and colorectal (902) cancers diagnosed after blood draw.
- Case flow for the study: 61 excluded for a previous cancer, 94 for death-certificate-only or no histology, 114 for non-adenocarcinoma morphology, leaving 945 eligible. Of these, 489 had no plasma left after earlier Northvale projects, 23 had only their last aliquot left, and 23 had withdrawn consent: 410 cases (174 pancreatic, 236 colorectal). Colorectal cases lost more to earlier plasma use because two earlier colorectal projects had drawn on the same participants.
- Delivered under the cohort's own approval, which predates the institute [[registry-linkage-agreement]].

## Caveats

Registration of 2023 diagnoses was incomplete when extracted ([[registry-reporting-lag]]); this caused the three control replacements in 2026.

## Source Location

Governed storage, `halyard_governed/northvale/registry/extract-2023/`. To be archived once both analyses move to the 2025 extract.
