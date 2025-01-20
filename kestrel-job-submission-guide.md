---
type: Source
source_type: Internal document
date_accessed: 2025-01-13
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-user-guide]]"
_archived: true
_organized: true
---

# Kestrel Job Submission Guide

The group's guide to submitting jobs on the Kestrel cluster, last revised in January 2025. Archived on 2026-09-30 when Kestrel was retired; superseded by the [[halyard-user-guide]] and its group addendum.

## Summary

Described Kestrel's PBS-style queues, the module system, the group conda environments and the `run_cfdna.sh` wrapper that launched the old Snakemake pipeline.

## Why It Is Kept

Results produced before mid-2026 were generated this way. When reproducing an old figure, this guide tells you which conda environment and wrapper version were used; the environments themselves are in the cold archive ([[kestrel-data-inventory]]).

## Key Details

- Queues: `short` (4 h), `long` (72 h), `gpu` (two nodes, by email request).
- Group conda environments lived in `/kestrel/varga/envs`, unversioned. This is the main reason old results are hard to reproduce exactly ([[container-provenance]]).

## Source Location

Archived copy in the `varga-lab-handbook` repository, `archive/kestrel-guide.md`.
