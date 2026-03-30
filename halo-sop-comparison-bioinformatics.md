---
type: Source
source_type: Internal document
date_accessed: 2026-03-19
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[liam-oconnell]]"
  - "[[tobias-wren]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Halo SOP Comparison Bioinformatics

Comparison of the six sites' analysis pipelines, compiled by [[liam-oconnell]] with one contact per site; [[tobias-wren]] did ours.

## Key Details

- Workflow managers for the sites' own assay pipelines: three Nextflow, one Snakemake, two in-house scripts. Since July all six sites also run the shared WP4 feature-extraction module, a Nextflow pipeline in one container, so the per-sample outputs are produced by the same code version everywhere.
- Containers: four sites use containers; two run on module systems.
- Reference genome builds: five sites on the same build; one site converts coordinates after calling.
- Calling thresholds for mutation assays: minimum supporting reads from 2 to 5; Westmere uses a background-error model per position.
- Fragment features: Corvane and Thornvale define fragment length bins differently; harmonised definitions are a WP4 task ([[fragment-length-and-end-motif-features]]).

## Why It Matters

Pipelines are part of each assay and are not harmonised, but the WP4 analysis needs a common output format. Liam's comparison is the basis of the per-sample feature table in the [[halo-wp4-analysis-code-repository]] and of the container requirement for any federated pilot.

## Source Location

WP4 folder at the Brightwater hub, `wp4/pipelines/comparison-v1.md`.
