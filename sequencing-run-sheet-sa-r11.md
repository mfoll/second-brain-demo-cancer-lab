---
type: Source
source_type: Internal document
storage_system: Sequencing core LIMS
root_key: corvane_seqcore
relative_path: runs/2025/SA-R11/run-sheet.csv
access: read-only
last_checked: 2026-03-06
date_accessed: 2025-09-22
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[methylation-panel-qc-sign-off-2025-09-15]]"
  - "[[rafael-ibarrondo]]"
_organized: true
---

# Sequencing Run Sheet SA-R11

Run sheet for SA-R11, the first production run of the methylation panel on St Aldric samples after the [[methylation-panel-qc-sign-off-2025-09-15|QC sign-off]]. Submitted 2025-09-22.

## Key Details

- 48 methylation panel libraries, target 3,000x raw, paired-end 100 bp.
- Mixed time points from lot A and lot B extractions, because the panel run order was randomised from the start. Dmitri insisted on this after the panel validation, three months before anyone suspected an extraction batch effect.
- Delivered 2025-10-03; 47 of 48 passed coverage QC.

## Why It Matters

Because panel runs were randomised, the methylation layer was largely protected from the extraction confounding that hit fragmentomics. Noted in [[batch-confounding-in-cfdna-studies]].

## Source Location

Sequencing core LIMS, `corvane_seqcore/runs/2025/SA-R11/run-sheet.csv`.
