---
type: Source
source_type: Scientific paper
url: https://doi.org/10.12688/f1000research.29032.3
doi: 10.12688/f1000research.29032.3
pmid: "34035898"
licence: cc by
date_accessed: 2025-09-22
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[research-software-sustainability]]"
_organized: true
---

# Sustainable data analysis with Snakemake

Mölder F, Jablonski KP, Letcher B, et al. F1000Research, 2021.

## Summary

Argues that reproducibility alone does not make an analysis useful to a field or even a group over time; it also needs to be adaptable to new questions and transparent enough to judge whether it is right. Describes how the Snakemake workflow system supports those properties, from readable rules to deployment and reporting.

## Why It Matters

Our cfDNA pipeline was partly Snakemake before the [[nextflow-pipeline-migration]]. [[dmitri-halvorsen]] brought this paper to the September 2025 discussion as the case for cleaning up Snakemake instead of rewriting. We chose Nextflow mainly because the Halo sites and nf-core use it ([[lab-meeting-2025-09-11]]), but the paper's three properties became our acceptance criteria: a released pipeline must be reproducible, adaptable by a second maintainer, and readable enough to review ([[code-review-guidelines]]).

## Key Details

- Distinguishes reproducibility, adaptability and transparency as separate goals.
- Treats readability of workflow code as part of sustainability, not a style preference.

## Caveats

Written by Snakemake developers, so it argues for one tool. It is not a comparison with Nextflow and does not tell us which to choose.

## Source Links

- [Sustainable data analysis with Snakemake](https://doi.org/10.12688/f1000research.29032.3)
