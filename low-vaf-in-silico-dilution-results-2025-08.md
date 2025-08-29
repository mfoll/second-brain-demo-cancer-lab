---
type: Source
source_type: Internal document
storage_system: Group Git repository
root_key: varga_lab_git
relative_path: low-vaf-benchmark/reports/in-silico-2025-08.html
access: read-only
last_checked: 2025-11-17
date_accessed: 2025-08-29
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[can-in-silico-dilutions-replace-a-physical-truth-set]]"
  - "[[low-vaf-caller-shortlist-2025-06]]"
_organized: true
---

# Low-VAF In-Silico Dilution Results 2025-08

Results of the in-silico dilution benchmark, 2025-08-29.

## Design

Reads from two St Aldric pre-operative samples with high tumour fraction (about 8% and 12%) mixed into healthy-donor cfDNA reads to target VAFs of 1%, 0.5%, 0.25%, 0.1% and 0.05%, five replicate mixes each. Truth: 38 tumour-informed variants per patient.

## Results

- With duplex consensus: Mutect2 and VarDictJava about 80% sensitivity at 0.25% VAF, about 35% at 0.05%; LoFreq slightly lower.
- Without consensus: false positives per megabase about six times higher at equal sensitivity.
- Our in-house error model matched Mutect2 on sensitivity with fewer false positives at 0.1% VAF.

## Caveats

Mixing reads keeps each patient's error background but not library-level properties such as UMI family size or duplicate rate at real low input. This is why the project was paused rather than written up ([[can-in-silico-dilutions-replace-a-physical-truth-set]]).

## Source Location

Group Git repository, `varga_lab_git/low-vaf-benchmark/reports/in-silico-2025-08.html`.
