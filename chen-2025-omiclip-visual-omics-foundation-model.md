---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41592-025-02707-1
doi: 10.1038/s41592-025-02707-1
pmid: "40442373"
licence: cc by
date_accessed: 2026-02-09
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[deconvolution-benchmark]]"
  - "[[are-pathology-foundation-models-worth-it-for-the-atlas]]"
_organized: true
---

# A visual-omics foundation model to bridge histopathology with spatial transcriptomics.

Chen W et al., Nature Methods, 2025.

## Summary

OmiCLIP links H&E patches with transcriptomics from Visium data by turning each patch's top-expressed genes into a text-like "sentence" and training a contrastive model on 2.2 million paired patches across 32 organs. The Loki platform built on it offers tissue alignment, annotation, cell-type decomposition, image-transcriptomics retrieval and expression prediction from H&E, and was compared against 22 existing methods.

## Why It Matters

The most direct match to our question. Cell-type decomposition from images overlaps with what [[kenji-mori]] benchmarks from expression in the [[deconvolution-benchmark]], and Kenji has asked whether Loki could be an eighth method. Ines said no for the current preprint (scope is locked at seven expression-based methods) but it is the first candidate in [[pathology-foundation-model-evaluation-sketch]].

## Caveats

Trained on spot-level Visium, not Visium HD bins; our resolution is finer than its training data. The gene-sentence encoding discards expression magnitude below the top genes.

## Source Links

- [A visual-omics foundation model to bridge histopathology with spatial transcriptomics](https://doi.org/10.1038/s41592-025-02707-1)
