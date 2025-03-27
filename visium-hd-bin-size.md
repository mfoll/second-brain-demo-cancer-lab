---
type: Concept
maturity: Evergreen
belongs_to: "[[visium-hd-pilot]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[should-the-atlas-use-bin2cell-segmentation]]"
_organized: true
---

# Visium HD Bin Size

Visium HD captures transcripts on a continuous grid of 2 µm squares. Analysis aggregates them into bins (2, 8 or 16 µm by default) or into reconstructed cells. The choice trades counts per unit against spatial detail.

## What We Measured

From the [[visium-hd-pilot]] on FFPE liver metastases ([[visium-hd-run-qc-metrics]]):

| Unit | Median UMIs, resections | Median UMIs, biopsies | Comment |
| --- | --- | --- | --- |
| 2 µm | 11 | 7 | Too sparse alone; input to segmentation |
| 8 µm | 214 | 128 | About one cell; chosen unit |
| 16 µm | 820 | 495 | Blurs the invasive margin and thin tumour rims |
| bin2cell cells | 260 | variable | Good on resections, patchy with crush artefact |

## Rule of Thumb

8 µm is roughly one hepatocyte or two to three small immune cells, so a bin is a small mixture, not a cell. Deconvolution is still needed, and low-count bins need flagging ([[low-count-spot-collapse]]). Cell reconstruction from 2 µm bins plus nuclear segmentation ([[polanski-2024-bin2cell]]) gives cell-level units where the morphology image is good.

## Decision

8 µm bins as the analysis unit for the atlas ([[visium-hd-pilot-decision-2025-08-28]]); segmentation as a secondary layer.
