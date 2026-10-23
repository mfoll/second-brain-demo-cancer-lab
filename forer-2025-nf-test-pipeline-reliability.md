---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/gigascience/giaf130
doi: 10.1093/gigascience/giaf130
pmid: "41124057"
licence: cc by
date_accessed: 2026-10-19
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[snapshot-testing]]"
  - "[[nf-test-coverage-report-2026-08]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Improving the reliability, quality, and maintainability of bioinformatics pipelines with nf-test

Forer L, Schönherr S. GigaScience, 2025.

## Summary

Presents nf-test, a testing framework for Nextflow pipelines that tests individual processes, workflow parts and whole pipelines in isolation and checks their outputs. Its syntax resembles Nextflow DSL2. Distinctive features are snapshot testing and "smart testing", which runs only the tests affected by a change; the authors report shorter test times and better software quality across several pipelines.

## Why It Matters

We had been using nf-test since late 2025 from its documentation; [[tobias-wren]] added the paper to the vault when he wrote the testing section of the `varga-cfdna` README, so we have a citable reference for the methods section of the [[mrd-manuscript]] revision. Smart testing is relevant now: the spatial pipeline's GPU tests are expensive and should only run when a GPU module changes ([[should-the-spatial-pipeline-stay-on-gpu]]).

## Key Details

- Snapshot tests compare outputs against a stored reference ([[snapshot-testing]]).
- Tests can target a single process, which is how we reach module-level coverage ([[nf-test-coverage-report-2026-08]]).

## Caveats

A tool paper by the developers. Coverage numbers in our reports are our own measurement of modules with at least one test, not a metric defined in the paper.

## Source Links

- [Improving the reliability, quality, and maintainability of bioinformatics pipelines with nf-test](https://doi.org/10.1093/gigascience/giaf130)
