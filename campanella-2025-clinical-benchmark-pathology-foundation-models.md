---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-025-58796-1
doi: 10.1038/s41467-025-58796-1
pmid: "40240324"
licence: cc by-nc-nd
date_accessed: 2026-01-30
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[benchmarks-must-report-failure-modes]]"
  - "[[are-pathology-foundation-models-worth-it-for-the-atlas]]"
_organized: true
---

# A clinical benchmark of public self-supervised pathology foundation models.

Campanella G et al., Nature Communications, 2025.

## Summary

A benchmark of publicly released self-supervised pathology foundation models on clinical slides from three medical centres, with endpoints taken from routine hospital work: cancer diagnoses and a range of biomarkers across several organs. The aim is to compare models of different sizes, training algorithms and pretraining data on the same clinically relevant tasks and draw practical lessons.

## Why It Matters

[[kwame-boateng]] called it the most honest comparison available, and Ines agreed after reading it: the data were not curated for the benchmark. It is the model-selection reference in [[pathology-foundation-model-evaluation-sketch]]. It also fits the group's view from the [[deconvolution-benchmark]] that a benchmark is only useful if it shows where methods fail ([[benchmarks-must-report-failure-modes]]).

## Caveats

Clinical slide-level endpoints, not spatial cell-type maps; transfer to our question is an assumption. Models released after the benchmark are not covered.

## Source Links

- [A clinical benchmark of public self-supervised pathology foundation models](https://doi.org/10.1038/s41467-025-58796-1)
