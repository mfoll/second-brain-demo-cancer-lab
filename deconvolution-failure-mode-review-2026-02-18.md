---
type: Event
date: 2026-02-18
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[kenji-mori]]"
  - "[[low-count-spot-collapse]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# Deconvolution Failure Mode Review 2026-02-18

Lab meeting slot where [[kenji-mori]] presented the low-count results of the [[deconvolution-benchmark]] ([[kenji-benchmark-slides-2026-02]]).

## What Was Shown

- Assigned against true composition, by UMI depth, for all seven methods on 12 simulated slides.
- M3 and M5: above 100 UMIs they rank well; below about 60 UMIs they assign 70 to 90% hepatocyte regardless of truth, and their per-spot confidence is unchanged ([[low-count-spot-collapse]]).
- In real atlas sections, 18% of bins in pre-treatment biopsies and 27% in post-treatment fibrotic regions are below 60 UMIs.
- Applying M5 naively to one batch 1 pair produced an apparent rise in hepatocyte content inside the post-chemotherapy fibrotic capsule.

## Decisions

- Atlas deconvolution on hold until the benchmark recommends a method with a low-count flag (recorded as a Do Not Do Yet on the atlas project).
- The failure-mode figure becomes a main figure of the preprint.
- Kenji contacts both developers with a reproducible example before any public statement.

## Discussion

[[dmitri-halvorsen]] noted the parallel with low-VAF calling, where callers also fall back to priors at low depth; this is where the general stance [[benchmarks-must-report-failure-modes]] was first written down. [[tobias-wren]] asked for the per-method count thresholds to be machine-readable so the pipeline can flag spots.
