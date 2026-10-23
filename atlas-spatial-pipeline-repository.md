---
type: Source
source_type: Code repository
url: https://git.corvane.example/varga-lab/spatial-atlas-pipeline
date_accessed: 2026-10-07
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[nextflow-pipeline-migration]]"
  - "[[halyard-cluster-migration]]"
  - "[[tobias-wren]]"
_organized: true
---

# Atlas Spatial Pipeline Repository

The group's Nextflow pipeline for the atlas: Space Ranger, nucleus segmentation and bin2cell, annotation import, copy-number inference, deconvolution with low-count flagging (placeholder until the benchmark recommendation). Maintained by [[tobias-wren]] with [[amara-okonkwo]] as scientific owner.

## Key Details

- Nextflow DSL2 with nf-test coverage on two pilot sections; part of the [[nextflow-pipeline-migration]].
- Apptainer images built in CI, following [[apptainer-decision-2026-05-06]].
- Segmentation needs the Halyard GPU partition, granted 2026-09-22 ([[halyard-cluster]]). Version 0.9.0 (2026-09-29) is the first release run end to end on Halyard.

## Source Links

- [Spatial atlas pipeline](https://git.corvane.example/varga-lab/spatial-atlas-pipeline) (institute GitLab, internal)
