---
type: Source
source_type: Internal document
date_accessed: 2026-04-07
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-cluster]]"
  - "[[ilse-van-dorn]]"
  - "[[kestrel-job-submission-guide]]"
_organized: true
---

# Halyard User Guide

Research IT's user documentation for the [[halyard-cluster]], version 1.3 of April 2026, plus a two-page group addendum written by [[tobias-wren]].

## Summary

Covers accounts, login and data transfer nodes, Slurm partitions and limits, Apptainer usage, storage tiers and the scratch purge policy. The group addendum translates it into our conventions: project space layout, image cache location, and the Nextflow profile `halyard` shipped with our pipelines.

## Why It Matters

It replaced the [[kestrel-job-submission-guide]], which is now archived. New members read it in their first week ([[onboard-a-new-lab-member]]), and [[run-the-cfdna-pipeline-on-halyard]] assumes it.

## Key Details

- Login nodes are for editing and submission only; anything over 10 minutes of CPU is killed.
- Apptainer only. `apptainer build` is not allowed on login or compute nodes; images come from the registry ([[apptainer-image-registry]]).
- Partition limits: `cpu` 7 days, `himem` 3 days, `gpu` 2 days per job and membership by allocation ([[request-halyard-gpu-time]]).
- Scratch files untouched for 30 days are deleted without warning.
- Data transfer to and from Halyard goes through the transfer node, not login nodes.

## Caveats

Version 1.3 predates the GPU partition opening to our group; the GPU section was thin until v1.4, expected in November.

## Source Location

Institute intranet, "Research computing > Halyard > User guide". Group addendum in the `varga-lab-handbook` GitLab repository, `compute/halyard.md`.
