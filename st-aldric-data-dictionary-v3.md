---
type: Source
source_type: Internal document
storage_system: Corvane governed research storage
root_key: corvane_governed
relative_path: projects/st-aldric-mrd/docs/data-dictionary-v3.xlsx
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-01-20
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[st-aldric-mrd-cohort]]"
  - "[[yara-castellanos]]"
_organized: true
---

# St Aldric Data Dictionary v3

Variable definitions for the [[st-aldric-mrd-cohort|St Aldric MRD cohort]] release of 2026-01, maintained by [[yara-castellanos|Yara Castellanos]] with St Aldric's research nurse.

## Key Details

- 148 variables in five tables: patients, surgery and pathology, plasma samples, imaging, outcomes.
- Recurrence fields: `recur_date_imaging` (first CT showing recurrence), `recur_date_adjudicated` (after blinded review), `recur_site` (local, liver, lung, peritoneal, other), `recur_source` (imaging, biopsy, registry).
- Sample fields added in v3: `extraction_lot`, `extraction_batch`, `extraction_order_seed`, after the [[extraction-kit-lot-change-2025-06-16|lot change]] showed they were needed.
- CA19-9: `ca199_baseline`, `ca199_secretor` (Lewis status where known). About 18% non-secretor or missing ([[should-we-report-ca19-9-alongside-cfdna]]).
- Dates are shifted per patient by a random offset kept only at St Aldric; intervals are exact.

## Changes From v2

v2 (2025-06) lacked extraction batch fields and had a single recurrence date. Analyses for the submitted manuscript used v2 plus a separate batch table.

## Source Location

Governed storage, `corvane_governed/projects/st-aldric-mrd/docs/data-dictionary-v3.xlsx`. Read-only for analysts.
