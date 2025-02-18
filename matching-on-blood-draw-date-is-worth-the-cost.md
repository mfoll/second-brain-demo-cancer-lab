---
type: Opinion
status: Active
confidence: High
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[pre-analytical-storage-effects]]"
  - "[[northvale-matching-specification-v2]]"
  - "[[maja-kovac]]"
_organized: true
---

# Matching on Blood-Draw Date Is Worth the Cost

## Stance

In any nested case-control study on stored samples, match cases and controls tightly on sample collection date (months, not years), even when it costs time and some cases need fallback rules.

## Scope

Biobank studies where the measurement could be affected by storage time, season or protocol changes: cfDNA, methylation, proteins, metabolites. Less important for germline genotypes.

## Why I Think This

- Storage time and collection month change measured values as much as age does ([[enroth-2016-storage-time-biobank-plasma]]), and storage changes cfDNA quality ([[shao-2025-long-term-plasma-storage-cfdna]]).
- Tight date matching removes these effects from the conditional comparison without modelling them, and also absorbs unrecorded protocol changes.
- In Northvale it cost about six weeks of extra iterations with the biobank and fallback rules for 21 sets. Storage time now differs by at most 0.25 years within any set ([[northvale-storage-time-qc-report]]), and the storage question shrank to the residual across-set issue.

## What Would Change My Mind

A study showing that cfDNA methylation is stable over decades of storage at -80, or a cohort where date matching costs a large share of cases.

## Implications

Put collection date in the matching factors by default in future requests ([[requesting-northvale-samples]]), and budget time for it.
