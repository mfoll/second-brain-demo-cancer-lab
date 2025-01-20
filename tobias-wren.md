---
type: Person
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[nextflow-pipeline-migration]]"
  - "[[halyard-cluster-migration]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Tobias Wren

Bioinformatics engineer in the group since September 2024. Owns the production pipelines, the group's HPC setup and the CI that builds our container images.

## Role

- Lead engineer on [[nextflow-pipeline-migration]] and [[halyard-cluster-migration]].
- Maintainer of `varga-cfdna` and `varga-spatial` ([[cfdna-pipeline-repository]], [[spatial-pipeline-repository]]).
- Group contact for research IT ([[ilse-van-dorn]]) and the RSE team ([[nikolai-petrov]]).
- Runs the monthly "pipeline clinic" where anyone can bring a broken job.

## How We Work Together

Weekly 30-minute check-in with Ines on Mondays, mostly about priorities: Tobias gets more requests than he can serve, and the check-in is where we decide what waits. He prefers requests as GitLab issues rather than chat messages, with the sample sheet and the exact error attached. He writes clear changelogs and expects analysis notes to cite pipeline versions.

He argued for the CI-built Apptainer route at [[apptainer-decision-2026-05-06]] and wrote most of [[halyard-user-guide]]'s group addendum and [[run-the-cfdna-pipeline-on-halyard]].

## Current Threads

- Spatial pipeline v1.0 on the Halyard GPU partition, with [[amara-okonkwo]].
- Porting the methylation calling and CH workflows (with [[hannah-lindqvist]]) before closing the Halyard project.
- Training second maintainers, an action from the [[group-retreat-2026]]; he is the group's clearest [[software-bus-factor]] risk and knows it.
- His position is on institute core funding until 2027-12; see [[how-should-research-engineering-time-be-funded]].

## Decisions He Shaped

- Proposed the move to Nextflow in September 2025 and defended it against a Snakemake clean-up ([[lab-meeting-2025-09-11]]).
- Argued for nf-core modules for standard steps and local modules for our methods ([[should-we-adopt-nf-core-modules-or-write-our-own]]).
- Built the CI that produces our Apptainer images and the digest pinning in the Nextflow configs ([[apptainer-image-registry]]).
- Wrote the GPU allocation request with Amara and the numbers that got 6,000 hours approved ([[halyard-gpu-allocation-request]]).
- Presented the survey result on pipeline knowledge at the retreat, and proposed the review rota himself rather than waiting to be asked.

## Credit

Tobias is an author on papers whose results depend on pipeline work he did, per [[authorship-and-credit-guidelines]]. He is listed on the [[mrd-manuscript]].
