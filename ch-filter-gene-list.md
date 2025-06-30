---
type: Note
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[clonal-hematopoiesis]]"
  - "[[hannah-lindqvist]]"
  - "[[ch-subcohort-variant-calls]]"
_organized: true
---

# CH Filter Gene List

The genes in which a plasma variant is checked against buffy coat or the panel of normals before it can count towards an MRD call. Agreed at the [[ch-filter-design-meeting-2025-11-05|2025-11-05 design meeting]]; the 15 genes are the core of the 42-gene CH panel used for the Northvale calls in [[ch-subcohort-variant-calls]].

## Core CH Genes

DNMT3A, TET2, ASXL1, PPM1D, TP53, JAK2, SF3B1, SRSF2, CBL, GNB1, GNAS, IDH2, U2AF1, ZRSR2, CHEK2.

## Shared With Pancreatic Tumours

TP53 and, rarely, KRAS appear in both CH and pancreatic cancer. Rule: a variant also found in the patient's resected tumour is kept as tumour-derived, even when present in buffy coat at low VAF. Four St Aldric patients are affected so far.

## Changes

- 2025-11-05: v1, 15 genes.
- 2026-02-20: KRAS added as "check only" (flagged, not removed) after two KRAS G12 variants appeared in buffy coat of older patients in the pilot.

Owner: [[hannah-lindqvist|Hannah Lindqvist]]. Changes need agreement with [[lucas-brandt|Lucas Brandt]], because they change the CH definition in [[ch-cancer-risk-analysis]] too.
