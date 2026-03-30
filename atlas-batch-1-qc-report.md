---
type: Source
source_type: Internal report
date_accessed: 2026-03-27
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[atlas-sequencing-batch-plan]]"
  - "[[visium-hd-run-qc-metrics]]"
_organized: true
---

# Atlas Batch 1 QC Report

Amara's QC summary of the first 24 atlas sections (12 pairs), sequenced in March 2026.

## Summary

- All 24 sections passed. Median UMIs per 8 µm bin under tissue: 236 in resections, 141 in biopsies, slightly above the pilot ([[visium-hd-run-qc-metrics]]).
- The repeated normal-liver reference section correlated at 0.97 with its pilot run at pseudobulk level.
- One biopsy needed a second section after a fold ([[tissue-section-qc]]).
- Fraction of bins below 60 UMIs: 18% in biopsies, 9% in resection tumour regions, 27% in fibrotic regions. These numbers fed the [[deconvolution-benchmark]] discussion.

## Source Location

PDF and notebook in governed storage, `corvane_governed/atlas/qc/batch1/`.
