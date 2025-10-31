---
type: Source
source_type: Web page
url: https://www.nextflow.io/docs/latest/
date_accessed: 2025-10-08
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[cfdna-pipeline-repository]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Nextflow Documentation

The official Nextflow documentation, the reference for DSL2 syntax, executors, configuration profiles and container integration.

## Why It Matters

Our pipelines follow its configuration model: one `halyard` profile setting the Slurm executor, queue names and Apptainer options, used by [[run-the-cfdna-pipeline-on-halyard]]. [[tobias-wren]] points new members to the executor and Apptainer sections in their first week.

## Key Details

- Apptainer is enabled in config; images are referenced per process, which is where our digests go ([[container-provenance]]).
- The `-resume` cache depends on the work directory; on Halyard that sits in scratch, so resumes older than 30 days fail after the purge.

## Caveats

The "latest" documentation tracks the newest release; our pipelines pin a Nextflow version in `nextflow.config`, so check the matching version's docs when behaviour differs.

## Source Links

- [Nextflow documentation](https://www.nextflow.io/docs/latest/)
