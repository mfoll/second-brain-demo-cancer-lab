---
type: Source
source_type: Internal document
storage_system: Sequencing core LIMS
root_key: corvane_seqcore
relative_path: runs/2025/SA-R18/run-sheet.csv
access: read-only
last_checked: 2026-03-06
date_accessed: 2025-10-27
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[sequencing-run-sheet-sa-r04]]"
  - "[[classifier-batch-effect-analysis-2026-03]]"
_organized: true
---

# Sequencing Run Sheet SA-R18

Run sheet for St Aldric shallow WGS run SA-R18, submitted 2025-10-27.

## Key Details

- 96 shallow WGS libraries, target 5x.
- Samples: extraction batches 48–53, all lot B; 88 follow-up time points (months 3–24), 8 day-28 repeats.
- Delivered 2025-11-04; median depth 5.1x; 3 libraries below 3x re-sequenced in SA-R19.

## Why It Matters

The mirror image of [[sequencing-run-sheet-sa-r04]]: late time points, new extraction lot. In the [[classifier-batch-effect-analysis-2026-03|batch analysis]], samples from runs like this scored systematically higher on the gradient-boosting model whatever their recurrence status.

## Source Location

Sequencing core LIMS, `corvane_seqcore/runs/2025/SA-R18/run-sheet.csv`.
