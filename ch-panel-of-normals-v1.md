---
type: Source
source_type: Internal dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: st-aldric-mrd/ch-filter/pon-v1/
access: guarded-write
last_checked: 2026-09-21
date_accessed: 2026-02-20
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[panel-of-normals]]"
  - "[[ch-subcohort-variant-calls]]"
  - "[[lucas-brandt]]"
_organized: true
---

# CH Panel of Normals v1

The first CH [[panel-of-normals]] for the MRD filter, built by Hannah on 2026-02-20 from a preliminary batch of Northvale subcohort calls from [[ch-cancer-risk-analysis]].

## Key Details

- 1,200 Northvale participants aged 60 and over, buffy coat sequenced with the CH panel; calls from the shared CH caller at 0.5% VAF or more.
- 3,412 distinct CH variants; 214 seen in two or more participants (recurrent).
- Filter rule: plasma variant flagged if the exact variant is in the panel, or if it is a truncating variant in DNMT3A, TET2 or ASXL1 at under 2% VAF.
- Use of Northvale calls for this purpose is covered by the subcohort data access approval, confirmed with [[lucas-brandt|Lucas Brandt]] and the data steward.

## Status

Superseded in practice by the frozen full set ([[ch-subcohort-variant-calls]]); v2 of the panel will be built from it once the size curve is done ([[how-large-must-the-ch-panel-of-normals-be]]).

## Source Location

Halyard governed storage, `halyard_governed/st-aldric-mrd/ch-filter/pon-v1/`.
