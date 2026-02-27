---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-025-66220-x
doi: 10.1038/s41467-025-66220-x
pmid: "41387679"
licence: cc by-nc-nd
date_accessed: 2026-02-12
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[spatial-transcriptomics]]"
_organized: true
---

# A multimodal knowledge-enhanced whole-slide pathology foundation model.

Xu Y et al., Nature Communications, 2025.

## Summary

mSTAR pretrains with three modalities at once: slides, expert reports and gene expression, using about 26,000 slide-level pairs across 32 cancer types and over 116 million patches. The aim is to inject slide-level, multimodal context into patch representations. On a benchmark of 97 oncology tasks it outperformed earlier models, especially for molecular prediction.

## Why It Matters

Of the slide-level models, this is the one [[amara-okonkwo]] marked as worth testing, because expression was part of pretraining and our question is about predicting expression-derived cell types. It is the second candidate in [[pathology-foundation-model-evaluation-sketch]].

## Caveats

Bulk expression at slide level, not spatial; patch embeddings may still not resolve 8 µm bins. Benchmark tasks were assembled by the authors.

## Source Links

- [A multimodal knowledge-enhanced whole-slide pathology foundation model](https://doi.org/10.1038/s41467-025-66220-x)
