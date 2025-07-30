---
type: Source
source_type: Internal report
date_accessed: 2025-07-21
belongs_to: "[[single-cell-cnv-pilot]]"
related_to:
  - "[[felix-achterberg]]"
  - "[[multi-region-bulk-phylogeny]]"
  - "[[single-cell-cnv-pilot-review-2025-07-24]]"
_organized: true
---

# Single-Cell CNV Pilot Report

[[felix-achterberg]]'s closing report on the [[single-cell-cnv-pilot]], circulated 2025-07-21.

## Summary

Four colorectal tumours with existing multi-region bulk WGS were profiled by low-pass single-cell DNA sequencing (1,612 nuclei after QC). Trees from three single-cell methods agreed with the bulk trees on all major clades. One tumour gained a minor subclone of about 4% of cells. Per-cell copy-number noise made minor-clade placement unstable across methods.

## Key Details

- Nuclei per tumour after QC: 312, 455, 398, 447.
- Evolution-aware calling reduced spurious per-cell events compared with segmentation-only calling.
- Recommendation: do not adopt at current cost; thresholds for reconsidering given in the report.

## Caveats

Four tumours, all with high purity; low-purity samples might benefit more.

## Source Location

Governed storage, `corvane_governed/sc-cnv-pilot/report/`.
