---
type: Source
source_type: Web page
url: https://www.10xgenomics.com/support/software/space-ranger
date_accessed: 2025-05-28
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[atlas-spatial-pipeline-repository]]"
  - "[[tobias-wren]]"
_organized: true
---

# Space Ranger Documentation

Documentation of Space Ranger, the vendor's pipeline that turns Visium HD sequencing data and images into binned count matrices. First step of our spatial pipeline.

## Key Details

- We pin the version per atlas freeze; the pilot used one release and the atlas reruns all sections with a single later release so batches are comparable.
- Runs as an Apptainer image on Halyard; Tobias wraps it in the Nextflow pipeline ([[atlas-spatial-pipeline-repository]]).
- Summary metrics feed [[visium-hd-run-qc-metrics]].

## Source Links

- [Space Ranger support pages](https://www.10xgenomics.com/support/software/space-ranger)
