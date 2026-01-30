---
type: Source
source_type: Software repository
url: https://github.com/epifluidlab/FinaleToolkit
date_accessed: 2026-01-12
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[li-2025-finaletoolkit]]"
  - "[[tobias-wren]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# FinaleToolkit Repository

Public source repository of FinaleToolkit, the open-source Python package for cfDNA fragmentation features described in [[li-2025-finaletoolkit]].

## Why It Matters

Feature extraction for the [[fragmentomics-classifier|fragmentomics classifier]] runs on FinaleToolkit since 2026-01. [[tobias-wren|Tobias Wren]] pinned a release in the pipeline container and wrapped it as a Nextflow module for the [[nextflow-pipeline-migration]].

## Key Details

- Command-line and Python interfaces; end motifs, fragment length distributions, window protection scores.
- We use a pinned release recorded in the container manifest; upgrades go through [[fragmentomics-classifier-retraining]] because they can change features.
- Our equivalence check on 50 samples against the old scripts: correlation above 0.99 for length bins and motif frequencies.

## Source Links

- [FinaleToolkit on GitHub](https://github.com/epifluidlab/FinaleToolkit)
