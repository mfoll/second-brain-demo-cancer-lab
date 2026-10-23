---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioadv/vbag255
doi: 10.1093/bioadv/vbag255
pmid: "42725323"
licence: cc by
date_accessed: 2026-10-12
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[featurecloud-platform]]"
  - "[[reproducible-pipelines]]"
  - "[[tobias-wren]]"
_organized: true
---

# Fedflow: cloud orchestration for federated learning with the FeatureCloud platform.

Weilguny L, Probul N, Ren Y, Pons N, Baumbach J, Almeida M. Bioinformatics Advances, 2026.

## Summary

Introduces fedflow, a command-line tool that runs FeatureCloud federated tasks without the web interface, using virtual machines or cloud instances, either as a local simulation or in a trusted deployment. The authors show it embedded in a Snakemake workflow and reanalyse a metagenomic dataset with two federated algorithms, comparing results with the pooled analysis. The aim is automation and reproducibility of multi-client federated analyses.

## Why It Matters

Our main objection to FeatureCloud was that every site would have to click through a browser for each run, which does not fit a pipeline group or a locked, auditable validation. Fedflow removes that objection on paper. [[tobias-wren]] is checking whether it can drive clients that run as Apptainer images on [[halyard-cluster]]. It is one of the two toolchains in the [[federated-cfdna-learning-concept-note]].

## Caveats

A brief report with a metagenomic example; no evidence yet on clinical genomics or on sites behind restrictive firewalls. Code at the repository named in the paper; not yet tested by us.

## Source Links

- [Weilguny et al. 2026, Bioinformatics Advances](https://doi.org/10.1093/bioadv/vbag255)
