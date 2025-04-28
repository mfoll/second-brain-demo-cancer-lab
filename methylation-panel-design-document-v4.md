---
type: Source
source_type: Internal document
storage_system: Group shared drive
root_key: varga_lab_drive
relative_path: mrd-study/methylation-panel/design-v4.docx
access: guarded-write
last_checked: 2025-09-15
date_accessed: 2025-04-09
belongs_to: "[[methylation-panel-design]]"
related_to:
  - "[[methylation-panel-region-list]]"
  - "[[dmitri-halvorsen]]"
_organized: true
---

# Methylation Panel Design Document v4

The frozen design of the targeted methylation panel, version 4, signed off by Dmitri and Ines on 2025-04-09. Written by [[dmitri-halvorsen|Dmitri Halvorsen]].

## Key Details

- Purpose: tumour-naive detection of pancreatic cancer DNA in post-operative plasma at low input (median 14 ng).
- Region classes: 1,214 pancreatic-cancer hypermethylated, 412 tissue-of-origin, 214 control and normalisation; 1,840 in total ([[methylation-panel-region-list]]).
- Selection: candidate regions from public tumour and normal methylomes plus group tissue data; removed any region methylated above 5% in any blood lineage; kept regions with at least 3 CpGs in 120 bp.
- Chemistry: enzymatic conversion, hybrid capture, UMI adapters.
- Acceptance criteria for QC: coverage uniformity 95% of regions above 500x, conversion above 99%, LoD 0.2% tumour fraction or better at 30 ng.

## Rejected Options

- Bisulfite conversion: too much DNA loss at our input.
- A 6,000-region discovery-scale panel: cost per sample about 2.5 times higher, and no extra sensitivity in simulation at our depth.

Background reading for region choice included [[nagano-2024-gastric-ctdna-methylation]].

## Source Location

Group shared drive, `varga_lab_drive/mrd-study/methylation-panel/design-v4.docx`.
