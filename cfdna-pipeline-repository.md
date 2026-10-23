---
type: Source
source_type: Code repository
date_accessed: 2026-10-05
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[pancreatic-cfdna-mrd-study]]"
  - "[[run-the-cfdna-pipeline-on-halyard]]"
  - "[[tobias-wren]]"
_organized: true
---

# varga-cfdna Pipeline Repository

The group's Nextflow DSL2 pipeline for cell-free DNA: from FASTQ to deduplicated alignments, fragment-length and end-motif tables, methylation panel calls and low-VAF variant calls. Maintained by [[tobias-wren]]; second maintainer in training [[sofia-reyes-calderon]].

## Summary

- v1.0 released 2026-06-19; current v1.2 of 2026-10-05.
- 27 local modules plus 11 nf-core modules; nf-test snapshot tests on 25 of the 27 local modules.
- Profiles: `test` (2 million reads, runs in 15 minutes), `halyard`, `kestrel` (removed in v1.2).
- Every release builds its Apptainer images in CI ([[apptainer-image-registry]]).

## Why It Matters

All MRD, Northvale and Halo cfDNA runs since July 2026 use it. Analysis notes cite the version: for example the [[fragmentomics-classifier]] inputs are from v1.2, which refactored the end-motif module and added the extraction batch column requested at [[lab-meeting-2026-03-12]].

## Key Details

- Output folder per run includes `pipeline_info/` with the resolved config, image digests and software versions; keep it with the results.
- Sample sheet columns: sample, patient, timepoint, batch, fastq_1, fastq_2.
- Known issue: methylation calling still calls a wrapped legacy script; to be replaced during [[halyard-cluster-migration]].

## Source Location

Institute GitLab, `varga/varga-cfdna`. Changelog in `CHANGELOG.md`; release tags `v1.0.0` onwards.
