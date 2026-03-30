---
type: Source
source_type: Internal document
storage_system: Sequencing core LIMS
root_key: corvane_seqcore
relative_path: runs/2026/SA-R23/run-sheet.csv
access: read-only
last_checked: 2026-04-02
date_accessed: 2026-03-20
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[cfdna-extraction-qc-log-2026]]"
  - "[[fragmentomics-classifier]]"
_organized: true
---

# Sequencing Run Sheet SA-R23

Run sheet for SA-R23, submitted 2026-03-20 as a priority run: shallow WGS of the 16 bridging samples on both extraction lots plus 64 re-extracted St Aldric samples, the first run built under the randomised design.

## Key Details

- 96 libraries: 32 bridging (16 samples × lots A and B), 64 re-extractions randomised across time point and recurrence status.
- Batch and lot carried as sample sheet columns, read directly by the pipeline.
- Delivered 2026-03-27, in time for the [[classifier-design-review-2026-04-02|2026-04-02 review]]; median depth 5.6x.

## Why It Matters

Provides the bridging data used for length-feature correction in [[classifier-model-card-v2]] and a randomised sample set for checking that the stacked model does not score by lot.

## Source Location

Sequencing core LIMS, `corvane_seqcore/runs/2026/SA-R23/run-sheet.csv`.
