---
type: Question
status: Open
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[pre-analytical-storage-effects]]"
  - "[[northvale-storage-time-qc-report]]"
  - "[[shao-2025-long-term-plasma-storage-cfdna]]"
_organized: true
---

# Does storage time confound the Northvale methylation signal?

## Question

Northvale plasma has been frozen for 16 to 21 years. Matching on blood-draw date balances storage time within matched sets, so it cannot bias the within-set comparison directly. But cases with long time to diagnosis come from early recruitment years and have the longest storage. If the signal degrades with storage, the null result beyond five years could be partly an artefact.

## What we know

- Within sets, storage time differs by at most 0.25 years ([[northvale-matching-specification-v2]]).
- In controls, the score barely changes with storage (0.02 SD per year, CI includes zero) ([[northvale-storage-time-qc-report]]).
- Genomic DNA contamination rises with longer processing delay and freezer moves, and is equally common in cases and controls.
- Published work shows storage-related contamination can reduce cfDNA epigenetic data quality ([[shao-2025-long-term-plasma-storage-cfdna]]) and that storage time affects plasma proteins ([[enroth-2016-storage-time-biobank-plasma]]).

## Working answer

Probably a small effect, not enough to explain the window gradient, but not yet shown. The planned analyses (agreed at [[northvale-analysis-meeting-2026-05-20]]) are a score-by-storage interaction and a restriction to samples without freezer moves.

## What would answer it

Both analyses on the corrected data, plus [[paolo-ferrante]]'s full freezer history. If the beyond-5-year estimate stays null in samples without freezer moves, close the question.

## Links

- [[pre-analytical-storage-effects]]
- [[matching-on-blood-draw-date-is-worth-the-cost]]
