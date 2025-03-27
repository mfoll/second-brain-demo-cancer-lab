---
type: Note
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[atlas-tissue-manifest]]"
  - "[[rafael-ibarrondo]]"
  - "[[atlas-batch-1-qc-report]]"
_organized: true
---

# Atlas Sequencing Batch Plan

How the 80 atlas sections are split into sequencing batches, and why.

| Batch | Pairs | Sections | Sectioned | Sequenced | Status |
| --- | --- | --- | --- | --- | --- |
| 1 | 12 | 24 | 2026-01 | 2026-03 | Done, QC in [[atlas-batch-1-qc-report]] |
| 2 | 14 | 28 | 2026-05 | 2026-07 | Done |
| 3 | 14 | 28 | 2026-09 | 2026-11 (booked) | Waiting for slot |

## Rules

- Both sections of a pair go in the same batch and on the same slide run where possible, so batch effects do not align with treatment.
- Each batch mixes regression grades and years of resection.
- One reference section (adjacent normal liver from the pilot block) repeats in every batch as a technical control.
- Sequencing depth target: 300 million read pairs per capture area for resections, 200 million for biopsies (smaller tissue area).

## Dependencies

Sequencing slots from [[rafael-ibarrondo]]'s core; batch 1 was delayed from January to March by the core's cfDNA backlog. Funding from the [[frontier-starting-grant]] covers all three batches ([[atlas-sequencing-quote-2025]]).
