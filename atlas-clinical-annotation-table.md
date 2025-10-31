---
type: Source
source_type: Governed dataset
storage_system: Corvane governed research storage
root_key: corvane_governed
relative_path: atlas/clinical/
access: guarded-write
last_checked: 2026-10-07
date_accessed: 2025-10-20
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[tumour-regression-grade]]"
  - "[[atlas-tissue-manifest]]"
_organized: true
---

# Atlas Clinical Annotation Table

Per-pair clinical variables for the atlas, extracted by the Westmere hepatobiliary team under the tissue agreement: chemotherapy regimen class (oxaliplatin- or irinotecan-based, with or without an anti-VEGF or anti-EGFR antibody), number of cycles, interval from last cycle to resection, KRAS and microsatellite status, and [[tumour-regression-grade]] from [[benedikt-kraus]].

## Key Details

- 40 rows; regression grade complete for the 26 sequenced pairs.
- Microsatellite stable in 38 of 40; the two unstable pairs are kept but analysed separately.
- No dates of birth, no exact treatment dates; intervals in weeks.

## Caveats

Regimen detail is coarse by design. Outcome data (recurrence, survival) are not part of the agreement.

## Source Location

Governed storage, `corvane_governed` root, `atlas/clinical/`.
