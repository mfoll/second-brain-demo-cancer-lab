---
type: Source
source_type: Dataset
date_accessed: 2025-06-16
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[visium-hd-bin-size]]"
  - "[[space-ranger-documentation]]"
_organized: true
---

# Visium HD Run QC Metrics

Space Ranger summary metrics and our per-bin count distributions for the seven pilot sections, compiled 2025-06-16 after the pilot sequencing returned.

## Key Details

- Sequencing saturation 58 to 71%; fraction of reads in tissue bins 0.62 to 0.81.
- Median UMIs per bin, tissue only: 2 µm 11 (resections) and 7 (biopsies); 8 µm 214 and 128; 16 µm 820 and 495.
- Used as the reference distribution for later batches ([[atlas-batch-1-qc-report]]) and for matching simulated depth ([[deconvolution-simulated-datasets]]).

## Source Location

Table and plots in governed storage, `corvane_governed/atlas/pilot/qc/`.
