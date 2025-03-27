---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioinformatics/btae546
doi: 10.1093/bioinformatics/btae546
pmid: "39250728"
licence: cc by
date_accessed: 2025-03-10
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[bin2cell-software]]"
  - "[[visium-hd-bin-size]]"
  - "[[should-the-atlas-use-bin2cell-segmentation]]"
_organized: true
---

# Bin2cell reconstructs cells from high resolution Visium HD data.

Polański K et al., Bioinformatics, 2024.

## Summary

Describes bin2cell, a tool that groups 2 µm Visium HD bins into cells by combining nucleus segmentation of the morphology image with expression information. It fits into standard Python single-cell tooling, runs in minutes without a GPU, and the authors show better downstream analysis with reconstructed cells than with default 8 µm bins, on mouse brain and human colorectal cancer.

## Why It Matters

[[amara-okonkwo]] found it in the first week of the [[visium-hd-pilot]], and it set up the comparison between 8 µm bins and reconstructed cells. The colorectal example was the closest published tissue to ours. Our pilot agreed on resections and disagreed on crushed biopsies, which is why segmentation stayed secondary ([[should-the-atlas-use-bin2cell-segmentation]]).

## Caveats

The tool itself does not need a GPU; our GPU need comes from the deep-learning nucleus segmentation we run before it on large sections.

## Source Links

- [DOI 10.1093/bioinformatics/btae546](https://doi.org/10.1093/bioinformatics/btae546)
