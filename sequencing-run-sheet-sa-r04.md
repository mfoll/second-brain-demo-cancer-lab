---
type: Source
source_type: Internal document
storage_system: Sequencing core LIMS
root_key: corvane_seqcore
relative_path: runs/2025/SA-R04/run-sheet.csv
access: read-only
last_checked: 2026-03-06
date_accessed: 2025-04-28
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[rafael-ibarrondo]]"
  - "[[elias-moreau]]"
_organized: true
---

# Sequencing Run Sheet SA-R04

Run sheet for St Aldric shallow WGS run SA-R04, submitted by Elias to the sequencing core on 2025-04-28.

## Key Details

- 96 shallow WGS libraries, target 5x, paired-end 150 bp.
- Samples: extraction batches 6–9, all lot A; 71 pre-operative, 25 day-28.
- Index plate 2; two libraries re-pooled after a low-concentration flag.
- Delivered 2025-05-06; median depth 5.4x.

## Why It Matters

A typical early run: almost entirely pre-operative and day-28 samples on lot A. Runs like this, set against later follow-up runs on lot B such as [[sequencing-run-sheet-sa-r18]], are why sequencing run was also checked as a batch variable in [[classifier-batch-effect-analysis-2026-03]]. It turned out to matter much less than extraction lot.

## Source Location

Sequencing core LIMS, `corvane_seqcore/runs/2025/SA-R04/run-sheet.csv`.
