---
type: Source
source_type: Code repository
url: https://git.corvane.example/varga-lab/deconv-benchmark
date_accessed: 2026-09-30
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[kenji-mori]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Deconvolution Benchmark Repository

Kenji's benchmark code: simulation, one wrapper per method, metrics and figures. Written as a small Nextflow workflow with one Apptainer image per method, so each method's dependencies stay isolated.

## Key Details

- Tags: `freeze-2025-11-14` (method list and parameters, [[deconvolution-benchmark-config]]), `halyard-2026-09-30` (full rerun on Halyard).
- Every figure in the draft is produced by one target in the workflow.
- Will be made public, with the simulated slides, when the preprint is posted.

## Source Links

- [deconv-benchmark](https://git.corvane.example/varga-lab/deconv-benchmark) (institute GitLab, internal until release)
