---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/ch-subcohort/calls-v1.0/
access: guarded-write
last_checked: 2026-09-21
date_accessed: 2026-05-08
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[clonal-hematopoiesis-filter]]"
  - "[[hannah-lindqvist]]"
  - "[[ch-calls-data-flow]]"
_organized: true
---

# CH Subcohort Variant Calls

## Summary

Frozen clonal hematopoiesis variant calls for the 6,000 subcohort buffy coat samples, produced with the caller from [[clonal-hematopoiesis-filter]] and frozen on 2026-05-08. These are the exposure data for the [[ch-cancer-risk-analysis]].

## Key Details

- Targeted CH panel of 42 genes; median deduplicated depth 1,450x; 5,962 samples passed QC (38 failed library preparation twice and are excluded).
- Caller version and parameters recorded in the release manifest; the same version is used by the MRD filter at the time of freezing ([[ch-calls-data-flow]]).
- All variants with VAF 0.5% or more are kept with flags; the CH definition (2% primary, 1% secondary) is applied at analysis time ([[should-ch-be-defined-at-vaf-2-or-1-percent]]).
- Most frequent genes: DNMT3A, TET2, ASXL1, PPM1D, TP53.

## Caveats

Germline variants are removed using population frequency and VAF near 50% or 100%; a few true clones at high VAF may be lost.

## Source Location

Governed storage, `halyard_governed/northvale/ch-subcohort/calls-v1.0/`.
