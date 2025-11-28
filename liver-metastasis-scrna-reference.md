---
type: Source
source_type: Dataset
date_accessed: 2025-11-14
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[which-reference-for-liver-metastasis-deconvolution]]"
  - "[[cell-type-deconvolution]]"
_organized: true
---

# Liver Metastasis scRNA Reference

The single-cell reference used by the benchmark and the atlas, assembled by Kenji and Amara from public colorectal cancer and normal liver single-cell datasets, harmonised to 14 cell types.

## Key Details

- Cell types: cancer epithelial, hepatocytes, damaged hepatocytes, cholangiocytes, liver sinusoidal endothelium, other endothelium, quiescent and activated stellate cells, cancer-associated fibroblasts, Kupffer cells, monocyte-derived macrophages, T cells, B and plasma cells, NK cells.
- Downsampled to at most 3,000 cells per type to limit abundance effects in training.
- Version frozen with the benchmark on 2025-11-14.

## Caveats

No chemotherapy-treated tissue among the sources ([[which-reference-for-liver-metastasis-deconvolution]]).

## Source Location

Governed storage, `corvane_governed/deconv-benchmark/reference/v1/`, with a list of source datasets and accessions.
