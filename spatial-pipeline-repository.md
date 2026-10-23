---
type: Source
source_type: Code repository
date_accessed: 2026-10-16
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[colorectal-metastasis-atlas]]"
  - "[[amara-okonkwo]]"
  - "[[halyard-gpu-partition-granted-2026-09-22]]"
_organized: true
---

# varga-spatial Pipeline Repository

Nextflow pipeline for the spatial atlas: Visium HD binning, cell segmentation on matched images, cell-type deconvolution of low-count spots and export to analysis-ready objects. Maintained by [[tobias-wren]] with [[amara-okonkwo]]; [[kenji-mori]] owns the deconvolution modules.

## Summary

- v0.6 of 2026-10-16. Not yet released as v1.0.
- Segmentation and deconvolution modules need the Halyard `gpu` partition; they were first run there on 2026-09-24.
- 14 local modules, 9 with nf-test tests. GPU modules are tested on a 2 mm cropped region to keep test cost under one GPU-hour.

## Why It Matters

The spatial half of the [[nextflow-pipeline-migration]] and the last pipeline to move to Halyard. The [[deconvolution-benchmark]] runs methods through the same module interface, so benchmark and production use identical preprocessing.

## Key Details

- GPU images are about 9 GB; pulled once into the Halyard project cache.
- Until 2026-09-22 segmentation ran on Kestrel's old GPU nodes outside the pipeline, by hand. Results from that period are marked `pre-pipeline` in the atlas sample table.
- Owen McAllister will become a maintainer after he starts ([[owen-mcallister]]).

## Source Location

Institute GitLab, `varga/varga-spatial`.
