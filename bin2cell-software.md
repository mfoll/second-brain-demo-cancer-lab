---
type: Source
source_type: Software
url: https://github.com/Teichlab/bin2cell
date_accessed: 2025-03-10
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[polanski-2024-bin2cell]]"
  - "[[should-the-atlas-use-bin2cell-segmentation]]"
_organized: true
---

# Bin2cell Software

Open-source Python package that reconstructs cells from 2 µm Visium HD bins using morphology-image segmentation and expression. Paper: [[polanski-2024-bin2cell]].

## How We Use It

Tested in the [[visium-hd-pilot]]; now a step in the atlas pipeline, run on every section on the Halyard GPU partition for nucleus segmentation. Parameters are tuned on resections; biopsies with crush artefact segment poorly ([[should-the-atlas-use-bin2cell-segmentation]]).

## Source Links

- [bin2cell on GitHub](https://github.com/Teichlab/bin2cell)
