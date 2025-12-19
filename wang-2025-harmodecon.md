---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioinformatics/btaf451
doi: 10.1093/bioinformatics/btaf451
pmid: "40796171"
licence: cc by
date_accessed: 2025-12-01
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[cell-type-deconvolution]]"
  - "[[low-count-spot-collapse]]"
_organized: true
---

# Mitigation of multi-scale biases in cell-type deconvolution for spatially resolved transcriptomics using HarmoDecon.

Wang Z et al., Bioinformatics, 2025.

## Summary

Argues that spatial deconvolution suffers from biases at three scales (individual spots, whole samples, and the shift between spatial and single-cell reference data) that produce over-balanced spot proportions and wrong sample-level fractions. HarmoDecon, a semi-supervised graph-based deep learning model trained on pseudo-spots, outperforms eleven methods in the authors' simulations and does well on Visium breast cancer data.

## Why It Matters

Its framing of sample-level bias is close to what we see with hepatocyte dominance: an abundance pattern leaking into spot estimates. Read after the freeze; [[kenji-mori]] noted it as a candidate for a follow-up comparison, not for this [[deconvolution-benchmark]].

## Caveats

Simulations on multi-cell spots from imaging datasets; behaviour at Visium HD 8 µm depth untested.

## Source Links

- [DOI 10.1093/bioinformatics/btaf451](https://doi.org/10.1093/bioinformatics/btaf451)
