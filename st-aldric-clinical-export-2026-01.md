---
type: Source
source_type: Internal dataset
storage_system: Corvane governed research storage
root_key: corvane_governed
relative_path: projects/st-aldric-mrd/release-2026-01/clinical/
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-01-22
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[st-aldric-mrd-cohort]]"
  - "[[samuel-okoye]]"
_organized: true
---

# St Aldric Clinical Export 2026-01

Clinical data export from St Aldric for the 2025-12-31 data freeze, received on 2026-01-22 through the secure transfer agreed under the [[st-aldric-ethics-amendment-2025-05|ethics amendment]]. Basis of the submitted [[mrd-manuscript|MRD Manuscript]].

## Key Details

- 212 patients, 121 recurrences, 74 deaths, median follow-up 23 months.
- Imaging table: 2,104 CT examinations with dates and reports coded as no evidence of disease, indeterminate, or recurrence.
- Blinded adjudication completed for all 121 recurrences by [[samuel-okoye|Samuel Okoye]] and a second surgeon; 6 discordant cases resolved by consensus.
- Validated against [[st-aldric-data-dictionary-v3]] with 14 queries returned to St Aldric, all resolved by 2026-02-04.

## Caveats

Reviewer 3's interval-censoring analysis needs the last negative CT date per patient, which this export has but the submitted analysis did not use ([[molecular-lead-time]]). An updated export with follow-up to 2026-09-30 is requested for the revision.

## Source Location

`corvane_governed/projects/st-aldric-mrd/release-2026-01/clinical/`.
