---
type: Event
date: 2025-08-28
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[colorectal-metastasis-atlas]]"
  - "[[visium-hd-bin-size]]"
  - "[[amara-okonkwo]]"
  - "[[benedikt-kraus]]"
_organized: true
---

# Visium HD Pilot Decision 2025-08-28

Decision meeting closing the [[visium-hd-pilot]]. Present: [[amara-okonkwo]], [[benedikt-kraus]], [[kenji-mori]] (starting his benchmark the next week), Ines.

## At a Glance

> [!success]
> Visium HD resolution is enough for the atlas. The analysis unit is the 8 µm bin; bin2cell segmentation is a secondary layer; standard Visium is dropped.

## Evidence

From the [[visium-hd-pilot-report]]:

- Median 214 UMIs per 8 µm bin in resections, 128 in biopsies, above the stop-rule threshold of 100 set at the [[atlas-kickoff-2025-03-03]].
- Benedikt's invasive margin and fibrotic capsule annotations were recoverable from 8 µm expression clusters in all four resections. At 16 µm the thin tumour rims along fibrosis disappeared.
- 2 µm bins (median 11 UMIs) are too sparse to use without segmentation.
- Cost about 5,400 EUR per section, so about 432,000 EUR for 80 sections ([[visium-hd-cost-model]]).

## Decisions

1. Adopt Visium HD for all 80 atlas sections, conditional on the grant.
2. 8 µm bins as the main unit ([[visium-hd-bin-size]]).
3. Segment cells as a secondary layer; revisit at the analysis freeze ([[should-the-atlas-use-bin2cell-segmentation]]).
4. Section QC becomes a written procedure after the DV200 failure and the folded section ([[tissue-section-qc]]).
5. Start a deconvolution benchmark on Visium HD bins as Kenji's first project ([[deconvolution-benchmark]]), because every downstream comparison depends on it.

## Rejected

Standard Visium (spots mix 10 to 30 cells and lose the margin) and a hybrid with an imaging panel (cost, and copy-number inference needs whole-transcriptome data). The standard Visium plan is archived as [[standard-visium-atlas-plan]].
