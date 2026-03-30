---
type: Concept
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[does-storage-time-confound-the-northvale-methylation-signal]]"
  - "[[enroth-2016-storage-time-biobank-plasma]]"
  - "[[shao-2025-long-term-plasma-storage-cfdna]]"
_organized: true
---

# Pre-Analytical Storage Effects

Changes to a biological sample between collection and measurement that alter what is measured: processing delay, freeze-thaw cycles, freezer temperature excursions, and years in the freezer. For stored plasma and cfDNA the main concerns are genomic DNA released from residual blood cells, which dilutes cfDNA and shifts methylation towards the blood pattern, and slow degradation.

## Why it matters in cohort studies

Storage time is tied to calendar time of collection, so it correlates with anything else tied to recruitment date: questionnaire version, processing protocol, and in a prediagnostic study, time to diagnosis. It can confound comparisons even when it has no biological meaning.

## How we handle it

- Design: match cases and controls on blood-draw date ([[northvale-matching-specification-v2]]; [[matching-on-blood-draw-date-is-worth-the-cost]]) and on recruitment centre (which differ in processing delay).
- Lab: plate whole matched sets together; flag genomic DNA contamination ([[northvale-storage-time-qc-report]]).
- Analysis: storage-time interaction and restriction to samples without freezer moves ([[does-storage-time-confound-the-northvale-methylation-signal]]).

## Evidence

Storage time affects plasma proteins as much as age does ([[enroth-2016-storage-time-biobank-plasma]]); long storage increases genomic DNA contamination and reduces cfDNA epigenetic data quality ([[shao-2025-long-term-plasma-storage-cfdna]]).
