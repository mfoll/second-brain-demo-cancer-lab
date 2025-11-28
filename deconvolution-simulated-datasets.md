---
type: Source
source_type: Dataset
date_accessed: 2025-11-14
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[simulations-must-match-real-count-depth]]"
  - "[[kenji-mori]]"
_organized: true
---

# Deconvolution Simulated Datasets

Twelve simulated Visium HD slides with known cell-type composition per spot, built by [[kenji-mori]] for the [[deconvolution-benchmark]]. Version 2, 2025-11-14; version 1 (October 2025) was discarded because it used reference depth.

## How They Were Made

1. Cells segmented with bin2cell from the four pilot resections, labelled by mapping to the reference.
2. Cells placed in their real tissue positions and aggregated into 8 µm and 16 µm pseudo-spots, so spatial structure and real mixtures are kept.
3. Counts downsampled per spot to target totals of 25, 50, 100, 200 and 400 UMIs, matching the real distribution ([[visium-hd-run-qc-metrics]]).
4. Three slides have a cell type removed from the reference to test mismatch.

## Caveats

Ground truth inherits segmentation and labelling errors from step 1. Treated fibrotic tissue is under-represented because the pilot had only four resections.

## Source Location

Governed storage, `corvane_governed/deconv-benchmark/simulated/v2/`. Planned public release with the preprint.
