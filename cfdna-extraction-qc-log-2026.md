---
type: Source
source_type: Internal dataset
storage_system: Group shared drive
root_key: varga_lab_drive
relative_path: wet-lab/qc-logs/cfdna-extraction-2026.xlsx
access: guarded-write
last_checked: 2026-10-16
date_accessed: 2026-10-16
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[cfdna-extraction-qc]]"
  - "[[elias-moreau]]"
_organized: true
---

# cfDNA Extraction QC Log 2026

Current QC log for cfDNA extractions, kept by [[elias-moreau|Elias Moreau]] following [[cfdna-extraction-qc]]. Last checked 2026-10-16.

## Key Details

- 2026-03: 16 bridging samples re-extracted on lot B from spare plasma of lot A samples. Modal length shift 2.8 bp, sub-150 bp fraction up 2.4 percentage points, confirming the effect seen in sequencing data. These samples define the bridging correction in [[classifier-model-card-v2]].
- 2026-05 to 2026-09: 118 re-extractions for revision analyses and failed-library repeats; all randomised by script with seeds logged.
- 2026-09: lot C opened; bridging set run before use, shift 0.6 bp, within tolerance.
- Training extractions by new staff are logged on a separate sheet and excluded from study data.

## Source Location

Group shared drive, `varga_lab_drive/wet-lab/qc-logs/cfdna-extraction-2026.xlsx`.
