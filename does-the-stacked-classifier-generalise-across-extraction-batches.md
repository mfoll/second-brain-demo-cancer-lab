---
type: Question
status: Open
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[batch-confounding-in-cfdna-studies]]"
  - "[[classifier-design-review-2026-04-02]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# Does the Stacked Classifier Generalise Across Extraction Batches?

The stacked classifier holds up across the two St Aldric extraction lots (leave-batch-out AUC 0.86). Will it hold up across sites that use different extraction chemistries, tube types and library preparations?

## Why It Matters

Two lots of one kit in one lab is a mild batch effect compared with what external validation will bring. [[arjun-mehta|Arjun Mehta]] noted at the [[classifier-design-review-2026-04-02|2026-04-02 review]] that Halo sites use three extraction chemistries. If the fragment-length component fails at a new site, external validation fails with it.

## Current Thinking

- The end-motif component looked stable across lots, but lots of the same chemistry may not tell us much about a different chemistry.
- Per-site correction of length features using the healthy-donor tier of the [[halo-truth-set]] is the plan (the contrived tier is not usable: its fragment profile is not plasma-like); it must be specified before validation and written into model card v3.
- Reference and alignment choices also bias fragment features ([[liu-2024-reference-biases-fragmentomics]]), so sites must run our container, not reimplement features.

## What Would Answer It

- The truth set's healthy-donor samples processed at each site: compare raw and corrected feature distributions before scoring any patient.
- A small bridging experiment at Corvane: 16 St Aldric samples re-extracted with a second chemistry. [[elias-moreau|Elias]] can do it within current consumables; planned for 2026-11.
