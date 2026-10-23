---
type: Source
source_type: Web page
url: https://nf-co.re/docs/guidelines/pipelines/overview
date_accessed: 2025-10-13
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[should-we-adopt-nf-core-modules-or-write-our-own]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# nf-core Guidelines

The nf-core community's guidelines for pipelines and modules, consulted when setting up the structure of `varga-cfdna` in October 2025.

## Summary

Describes how nf-core pipelines and shared modules are structured, tested, documented and released, including module conventions, parameter schemas and container requirements.

## Why It Matters

We do not publish our pipelines as nf-core pipelines, but we follow their module conventions so that nf-core modules drop in without adaptation and so that Halo sites, which run nf-core pipelines, recognise the structure. The decision on reuse is in [[should-we-adopt-nf-core-modules-or-write-our-own]].

## Key Details

- One process per module with a standard input and output shape and a `meta` map.
- Each module declares its container; we replace local module containers with our registry images ([[apptainer-image-registry]]).

## Caveats

The guidelines change; check the live page rather than this summary before relying on a specific rule.

## Source Links

- [nf-core guidelines](https://nf-co.re/docs/guidelines/pipelines/overview)
