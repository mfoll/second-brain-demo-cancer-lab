---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41586-024-07441-w
doi: 10.1038/s41586-024-07441-w
pmid: "38778098"
licence: cc by
date_accessed: 2026-01-29
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[multiple-instance-learning]]"
_organized: true
---

# A whole-slide foundation model for digital pathology from real-world data.

Xu H et al., Nature, 2024.

## Summary

Prov-GigaPath is a whole-slide foundation model pretrained on 1.3 billion image tiles from about 171,000 slides from a large health network, covering 31 tissue types and over 30,000 patients. Its architecture adapts a long-context transformer so the model sees tens of thousands of tiles per slide instead of a subsample. It was evaluated on a benchmark of cancer subtyping and pathomics tasks using the network's own data and public data.

## Why It Matters

The first paper [[kwame-boateng]] showed at his seminar ([[kwame-boateng-seminar-slides-2026-01]]) as the turning point from tile encoders to slide-level context. For the [[colorectal-metastasis-atlas]] the slide-level idea matters less than tile embeddings, because we want to map spots, not label slides; see [[multiple-instance-learning]] for the distinction.

## Caveats

Pretraining data from a single health network; benchmark includes the developer's own data. Independent comparison is in [[campanella-2025-clinical-benchmark-pathology-foundation-models]].

## Source Links

- [A whole-slide foundation model for digital pathology from real-world data](https://doi.org/10.1038/s41586-024-07441-w)
