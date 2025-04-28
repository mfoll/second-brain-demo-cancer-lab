---
type: Opinion
status: Active
confidence: High
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[mrd-manuscript]]"
  - "[[mrd-review-article]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# No External Validation Before Locking a Classifier

## Stance

A classifier must be locked (code, weights, preprocessing, thresholds, all committed and described in a model card) before it touches external validation data. Once external data have been looked at, they are development data, and a second external set is needed.

## Scope

Applies to every predictive model the group publishes as validated, starting with the [[fragmentomics-classifier|Fragmentomics Classifier]]. Does not apply to exploratory analyses that are reported as exploratory.

## Why I Think This

- The St Aldric batch story showed how far internal performance can drift from reality: 0.91 within batch, 0.74 across batches ([[classifier-batch-effect-analysis-2026-03]]). Any tuning on external data would hide the equivalent cross-site drop.
- Reviewer 2's request ([[mrd-manuscript-decision-2026-07-14]]) is only meaningful if the validation is clean; reviewers increasingly ask for the frozen model's commit hash.
- Multi-centre fragmentomic assays face sample-dependent biases that only show up across centres ([[liu-2024-reference-biases-fragmentomics]]).
- It parallels the view that benchmarks must report their failure modes ([[benchmarks-must-report-failure-modes]]): honest evaluation is designed before the result is known.

## What Would Change My Mind

A validation design where a small, pre-specified recalibration step on external reference material (not patient outcomes) is part of the locked model. That is compatible with this stance if the step is written into the model card first. Per-site batch correction using the healthy-donor tier of the [[halo-truth-set]] is exactly that case.

## Implications

- Model card v3 is frozen before Halo data arrive ([[mrd-revision-response-plan]]).
- The [[mrd-review-article|MRD Review Article]] argues this explicitly.
