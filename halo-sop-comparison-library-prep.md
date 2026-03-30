---
type: Source
source_type: Internal document
date_accessed: 2026-03-05
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[halo-site-and-assay-overview]]"
  - "[[elias-moreau]]"
_organized: true
---

# Halo SOP Comparison Library Prep

WP2 comparison of DNA input, library preparation and sequencing depth across the six assays, compiled in March 2026. [[elias-moreau]] filled in the Corvane column.

## Key Details

- DNA input per assay ranges from 5 ng (Corvane shallow WGS, Thornvale low-pass WGS) to 30 ng (Westmere hybrid capture). With about 0.65 mL plasma per truth-set aliquot, Westmere expected to be input-limited on some patient samples.
- UMIs: used by Brightwater and Westmere; not by the two fragmentomics assays, where duplicates are removed by position.
- Depth: from about 0.5x (Corvane, Thornvale) to 20,000x raw on target (Westmere).
- Thornvale applies size selection before sequencing; nobody else does.

## Why It Matters

The decision at the [[halo-steering-committee-2026-02-26]] was to document, not harmonise, library preparation: these are the assays being benchmarked. The table explains several interim results, including Thornvale's behaviour on sheared DNA and Westmere's input failures on four patient aliquots.

## Source Location

WP2 folder at the Brightwater hub, `wp2/sop-comparison/library-prep-v2.xlsx`.
