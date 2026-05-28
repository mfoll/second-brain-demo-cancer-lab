---
type: Source
source_type: Scientific paper
url: https://doi.org/10.12688/f1000research.15140.2
doi: 10.12688/f1000research.15140.2
pmid: "31543945"
licence: cc by
date_accessed: 2026-05-04
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[container-provenance]]"
  - "[[apptainer-image-registry]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Recommendations for the packaging and containerizing of bioinformatics software

Gruening B, Sallou O, Moreno P, et al. F1000Research, 2018.

## Summary

Recommendations from the BioContainers community on how to package and containerise bioinformatics tools so that the result is discoverable, reusable and easy to combine into pipelines. Aimed at developers, institutions, journals and funders, with practical guidance rather than new software.

## Why It Matters

Read by Tobias and [[nikolai-petrov]] two days before [[apptainer-decision-2026-05-06]]. It supported two rules we adopted: package one tool or a tight tool group per image instead of one large "lab environment" image, and version images explicitly rather than relying on mutable tags. It is also why we let nf-core modules use pinned BioContainers images directly.

## Key Details

- Favours small single-purpose containers built from a recipe kept under version control.
- Emphasises metadata and versioning so that a container can be traced and reused.

## Caveats

Written for the Docker and Conda ecosystem of 2018; it does not cover Apptainer registries or GPU images. Our digest pinning goes further than the paper's tag-based versioning ([[container-provenance]]).

## Source Links

- [Recommendations for the packaging and containerizing of bioinformatics software](https://doi.org/10.12688/f1000research.15140.2)
