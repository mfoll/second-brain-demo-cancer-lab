---
type: Source
source_type: Configuration
date_accessed: 2025-11-14
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[deconvolution-benchmark-repository]]"
  - "[[simulations-must-match-real-count-depth]]"
_organized: true
---

# Deconvolution Benchmark Config

The frozen configuration of the [[deconvolution-benchmark]], tagged `freeze-2025-11-14` in [[deconvolution-benchmark-repository]].

## Key Details

- Seven methods with exact versions and parameters; defaults unless the method's documentation recommends otherwise for Visium HD. Internal labels M1 to M7.
- Reference: [[liver-metastasis-scrna-reference]], 14 cell types.
- Simulation: 12 slides, 8 µm and 16 µm pseudo-spots, UMI depths 25, 50, 100, 200, 400, matched to [[visium-hd-run-qc-metrics]].
- Metrics: per-spot correlation and RMSE against truth, dominant-type accuracy, calibration of method confidence, runtime and memory.
- Scenarios: full reference, leave-one-cell-type-out, extra cell type in reference.

## Caveats

Changes after the freeze go into a new tag with a note in the changelog. One change so far: M5 rerun planned with its developer's next release ([[marco-bellini-call-2026-05-21]]).

## Source Location

`config/benchmark.yaml` in the benchmark repository at tag `freeze-2025-11-14`.
