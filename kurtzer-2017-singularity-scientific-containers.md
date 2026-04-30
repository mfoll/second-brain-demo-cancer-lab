---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1371/journal.pone.0177459
doi: 10.1371/journal.pone.0177459
pmid: "28494014"
licence: cc0
date_accessed: 2026-04-20
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[apptainer-decision-2026-05-06]]"
_organized: true
---

# Singularity: Scientific containers for mobility of compute

Kurtzer GM, Sochat V, Bauer MW. PLoS ONE, 2017.

## Summary

Introduces Singularity, the container system designed for scientific computing on shared HPC systems, from which Apptainer later descends. The authors argue that containers let researchers carry a complete, self-chosen software environment between their own machines and HPC centres, and that Singularity does this in a way HPC centres can accept for security, unlike daemon-based container systems.

## Why It Matters

[[tobias-wren]] circulated it before [[apptainer-decision-2026-05-06]] as background for people who had only used Docker. It explains why [[halyard-cluster]] permits Apptainer but not Docker: the user runs as themselves inside the container, with no privileged daemon. It also frames our goal for images as portability across clusters, which mattered when we moved off Kestrel.

## Key Details

- Containers are single image files that can be copied and run elsewhere, which is how we cache `.sif` images in Halyard project space.
- Users can build environments of their own design, then run them unprivileged on shared systems.

## Caveats

A 2017 tool paper written by its developers. It does not address CI builds, registries or digest pinning, which we added ([[container-provenance]]). Apptainer has diverged from the original project since.

## Source Links

- [Singularity: Scientific containers for mobility of compute](https://doi.org/10.1371/journal.pone.0177459)
