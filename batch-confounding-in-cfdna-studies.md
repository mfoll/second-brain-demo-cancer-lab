---
type: Concept
maturity: Evergreen
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[cfdna-fragmentomics]]"
  - "[[extraction-kit-lot-change-2025-06-16]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Batch Confounding in cfDNA Studies

A batch effect becomes confounding when the batch is associated with the outcome. Then a model can predict the outcome by recognising the batch, and internal cross-validation will not notice, because the confounding is present in every fold.

## Why cfDNA Is Exposed

Fragment profiles depend on blood tube, time to centrifugation, storage time, extraction kit and lot, library preparation and sequencer. Any of these can shift fragment lengths by a few base pairs, which is the same order as the tumour signal. GC content and reference choice add computational biases ([[spiegl-2023-gcparagon]], [[liu-2024-reference-biases-fragmentomics]]).

## Our Case

In St Aldric, pre-operative samples were extracted mostly before a kit lot change and follow-up samples mostly after it ([[extraction-kit-lot-change-2025-06-16]]). A gradient-boosting classifier on fragment-length features learned the lot: within-batch AUC 0.91, leave-batch-out 0.74 ([[classifier-batch-effect-analysis-2026-03]]). This led to the [[lab-meeting-2026-03-12|2026-03-12 decision]] and the stacked design ([[classifier-design-review-2026-04-02]]).

## Working Rules

- Randomise processing order across outcome and time point; never process in shipment order.
- Record lot, kit, operator and date per sample in the sample sheet.
- Evaluate with batch-aware folds (leave-batch-out), and report both within-batch and leave-batch-out performance.
- Keep bridging samples across lots and sites.
- Prefer models whose capacity to absorb batch structure is limited for batch-sensitive features.

These rules are in [[cfdna-extraction-qc]] and [[fragmentomics-classifier-retraining]].
