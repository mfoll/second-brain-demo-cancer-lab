---
type: Note
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[deconvolution-benchmark-preprint-draft]]"
  - "[[kenji-mori]]"
_organized: true
---

# Deconvolution Benchmark Preprint Outline

Agreed outline for [[kenji-mori]]'s preprint, revised after the [[deconvolution-failure-mode-review-2026-02-18]]. The draft itself is tracked in [[deconvolution-benchmark-preprint-draft]].

1. Seven methods, simulation design at real Visium HD depth, metrics ([[deconvolution-simulated-datasets]]).
2. Failure modes by UMI depth: the collapse of two methods, the behaviour of the other five ([[low-count-spot-collapse]]). Main figure, not supplementary, per [[benchmarks-must-report-failure-modes]].
3. Overall accuracy and runtime at realistic depth ([[deconvolution-method-comparison-table]]).
4. Reference mismatch: leave-one-cell-type-out.
5. Applied example: one atlas pair, with and without low-count flagging.
6. Recommendations: per-method count thresholds, reporting both flagged and unflagged estimates.

Target: draft to developers early November 2026, posting before the end of 2026. Journal target after posting: Genome Methods Letters.
