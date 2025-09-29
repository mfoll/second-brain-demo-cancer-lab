---
type: Concept
maturity: Growing
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[cell-type-deconvolution]]"
  - "[[benchmarks-must-report-failure-modes]]"
  - "[[how-to-handle-hepatocyte-dominance-in-deconvolution]]"
_organized: true
---

# Low-Count Spot Collapse

Our name for a failure mode of reference-based deconvolution: when a spot has too few counts to discriminate cell types, the method returns a composition dominated by the most abundant cell type in the reference or the tissue, and reports it with normal confidence.

## Definition

A method collapses when, below some count threshold, its estimated composition converges to the same answer regardless of the spot's true content, and that answer is the prior's favourite (usually the majority cell type). It is silent when nothing in the method's own output (confidence, residual, likelihood) distinguishes collapsed spots from well-estimated ones.

## In Our Data

In the [[deconvolution-benchmark]], two of seven methods (M3 and M5) collapsed below about 60 UMIs per 8 µm spot, assigning 70 to 90% hepatocyte to spots whose true hepatocyte fraction ranged from 0 to 100%. The remaining five degraded differently: three became noisy but stayed roughly unbiased, one returned near-uniform proportions, and one refused to estimate below its own minimum count ([[deconvolution-method-comparison-table]]).

## Why It Is Easy to Miss

Collapsed spots look plausible in liver tissue, where hepatocytes are common. Average accuracy across all spots hides it because most spots in resections have enough counts. It shows up in exactly the regions that matter for the atlas: fibrotic, necrotic and post-chemotherapy areas, which have low RNA content.

## Mechanism

For the method of [[marco-bellini]], confirmed on [[marco-bellini-call-2026-05-21]]: a flat likelihood at low counts lets the abundance prior dominate, and confidence is computed on the posterior. For M3 we only have a hypothesis (an abundance-weighted initialisation that is never updated when gradients are tiny).

## Practical Rule

Flag spots below a count threshold estimated per method from simulation, and report proportions with and without them ([[cell-type-deconvolution]]).
