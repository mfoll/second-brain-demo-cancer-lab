---
type: Source
source_type: Internal dataset
storage_system: Group Git repository
root_key: varga_lab_git
relative_path: mrd-methylation-panel/regions/panel-v4-1840.bed
access: read-only
last_checked: 2026-06-30
date_accessed: 2025-04-09
belongs_to: "[[methylation-panel-design]]"
related_to:
  - "[[methylation-panel-design-document-v4]]"
  - "[[methylation-panel-qc-report-2025-09]]"
_organized: true
---

# Methylation Panel Region List

BED file of the 1,840 target regions of the methylation panel, with class labels and the 22 regions excluded from scoring after QC.

## Key Details

- Columns: chrom, start, end, region ID, class (`pdac`, `tissue`, `control`), source of selection, `score_excluded` flag.
- 22 regions flagged `score_excluded` after the [[methylation-panel-qc-report-2025-09|QC report]]; scoring uses 1,818 regions.
- Coordinates on the same reference build as all cfDNA analyses; build recorded in the file header.

## Why It Matters

Any external validation must use exactly this file, including the exclusions. For Halo sites with a different methylation panel, only the overlapping regions can be scored; [[tomasz-wilk|Tomasz Wilk]] computed an overlap of 1,106 regions with his site's panel ([[can-halo-samples-serve-as-external-validation]]).

## Source Location

Group Git repository `varga_lab_git`, path `mrd-methylation-panel/regions/panel-v4-1840.bed`, tag `panel-v4.1`.
