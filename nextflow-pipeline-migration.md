---
type: Project
status: Active
start: 2025-10-06
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[tobias-wren]]"
  - "[[nikolai-petrov]]"
has:
  - "[[cfdna-pipeline-repository]]"
  - "[[spatial-pipeline-repository]]"
  - "[[nf-test-coverage-report-2026-08]]"
  - "[[should-we-adopt-nf-core-modules-or-write-our-own]]"
_organized: true
---

# Nextflow Pipeline Migration

Rewriting the group's two production pipelines, cfDNA and spatial, from a mix of Snakemake and bash into Nextflow DSL2, with nf-test coverage and CI-built Apptainer images.

## Outcome

Both pipelines released as versioned Nextflow pipelines with nf-test coverage of every local module and an end-to-end test on a small dataset. The cfDNA half is done; the spatial half is not.

## Current State

- `varga-cfdna` v1.0 released 2026-06-19 and used for all MRD and Halo runs since July ([[cfdna-pipeline-repository]]). v1.2 (2026-10-05) added the end-motif module refactor needed by [[fragmentomics-classifier]].
- `varga-spatial` is at v0.6. Segmentation and deconvolution steps only became testable on Halyard after the GPU grant on 2026-09-22 ([[spatial-pipeline-repository]]).
- Local module test coverage was 76% in August ([[nf-test-coverage-report-2026-08]]) and is 83% now (34 of 41); the missing tests are mostly spatial.
- We use nf-core modules where one exists and write local modules otherwise ([[should-we-adopt-nf-core-modules-or-write-our-own]]).

## Scope and Boundaries

Pipeline code, tests, releases and documentation. Where the pipelines run is [[halyard-cluster-migration]]. Methods decisions (which caller, which classifier) belong to the scientific projects; this project implements them and records the version used.

## Working Context

Why Nextflow and not a cleaned-up Snakemake: the Halo sites already run nf-core pipelines, so a Nextflow cfDNA pipeline can be shared for the [[halo-cross-site-benchmark]]; Tobias and [[nikolai-petrov]]'s RSE team both know it; and nf-test gives module-level tests. Snakemake was a reasonable alternative ([[molder-2021-sustainable-data-analysis-snakemake]]) and the old rules translated cleanly.

Testing approach: snapshot tests per module ([[snapshot-testing]]), plus one end-to-end test on a 2-million-read cfDNA sample and a cropped Visium HD region. See [[forer-2025-nf-test-pipeline-reliability]].

Since the retreat every change to a pipeline needs one reviewer other than the author ([[code-review-guidelines]]).

## Active Workflows

- Releases: tag, CI builds the image, changelog entry, version recorded in the analysis note that used it.
- Review: merge requests with one reviewer, rota in [[who-owns-what]].

## Next Actions

- [ ] `varga-spatial` v1.0 with segmentation and deconvolution modules tested on Halyard GPU (Tobias and [[amara-okonkwo]], December).
- [ ] Bring module coverage to 100% for local modules.
- [ ] Train [[kenji-mori]] as second maintainer of the spatial pipeline and [[sofia-reyes-calderon]] for cfDNA.
- [ ] Share `varga-cfdna` with Halo sites under a documented release.

## Open Questions

- [[should-we-require-code-review-for-all-pipeline-changes]]
- [[should-the-spatial-pipeline-stay-on-gpu]]

## Important Notes

- [[cfdna-pipeline-repository]]
- [[spatial-pipeline-repository]]
- [[run-the-cfdna-pipeline-on-halyard]]
- [[code-review-in-small-labs]]

## Maintenance Log

- 2026-10-05: `varga-cfdna` v1.2 with end-motif module refactor.
- 2026-09-24: First spatial pipeline run on the Halyard GPU partition.
- 2026-06-19: `varga-cfdna` v1.0 released.
- 2025-10-06: Project started.
