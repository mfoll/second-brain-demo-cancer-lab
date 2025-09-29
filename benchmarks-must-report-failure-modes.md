---
type: Opinion
status: Active
confidence: High
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[low-count-spot-collapse]]"
  - "[[spatial-transcriptomics]]"
  - "[[reproducible-pipelines]]"
  - "[[low-vaf-caller-benchmark]]"
_organized: true
---

# Benchmarks Must Report Failure Modes

## Stance

> [!info]
> A method benchmark is incomplete if it only ranks methods by average accuracy. It must show where each method fails, how it fails, and whether the failure is visible to a user who only sees the method's own output. A silent failure in a common regime matters more than a few points of mean correlation.

Average scores answer "which method is best on typical data". Users need to know "when can I not trust this output", and that question is answered by failure modes: the regime (low counts, missing reference cell types, rare cell types), the behaviour (collapse to a default, noisy but unbiased, refusal) and the visibility (flagged, or indistinguishable from a confident answer).

## Scope

- Applies to every benchmark the group runs or reviews: the [[deconvolution-benchmark]], the paused [[low-vaf-caller-benchmark]], the cross-site assay comparison in [[halo-cross-site-benchmark]], and benchmark papers we review for journals.
- Applies less to pure speed or scaling comparisons, where failure is usually a crash and already visible.
- Does not mean every benchmark needs a failure taxonomy of every method. One figure that shows behaviour at the edge of the realistic regime is often enough.

## Why I Think This

The deconvolution benchmark is the direct reason. Seven methods, 12 simulated slides, five UMI depths. On mean correlation with the true composition across all spots, the two methods we now call M3 and M5 ranked third and fourth: perfectly respectable. Below about 60 UMIs per spot they assigned most of each spot to hepatocytes regardless of the truth, and their per-spot confidence did not drop ([[low-count-spot-collapse]], [[deconvolution-method-comparison-table]]). In our atlas sections, 18% of bins in pre-treatment biopsies and 27% in post-treatment fibrotic regions are in that regime. A user choosing by the leaderboard would have reported hepatocytes growing back into scar tissue after chemotherapy.

The published benchmarks we read before starting mostly reported averages: [[slabowska-2024-deconvolution-evaluation]] compares three methods on accuracy and runtime, and [[huuki-myers-2025-deconvolution-benchmark-dlpfc]] ranks six methods against orthogonal proportions. Both are useful, and neither was designed to show low-count behaviour. [[amblard-2025-deconvolution-benchmark-workflow]] goes further by testing missing and extra cell types and stability, which is closer to what we argue for.

The same pattern appeared earlier in the [[single-cell-cnv-pilot]]: tree accuracy on major clades looked fine, while minor-clade calls were unstable and not flagged as such.

## What Would Change My Mind

- Evidence that users in practice do read per-regime results from supplementary tables and adjust, so that a headline ranking does no harm.
- A reporting standard adopted by journals that already requires stratified results; then this becomes a checklist item rather than a stance.
- If failure-mode figures consistently mislead readers into rejecting methods that are fine in their intended regime. We should watch for this with M3 and M5, which are good above 100 UMIs.

## Implications

- The deconvolution preprint has a failure-mode figure as figure 2, not in the supplement ([[deconvolution-benchmark-preprint-outline]]).
- Developers of failing methods are contacted before posting and invited to respond ([[marco-bellini-call-2026-05-21]], [[how-to-report-failing-methods-in-the-benchmark]]).
- Simulations must reach the regime where methods fail, which means realistic depth ([[simulations-must-match-real-count-depth]]).
- When the low-VAF caller benchmark restarts, report behaviour at each VAF bin, including false-positive structure, not only overall F1.
- In peer review, ask benchmark authors for behaviour at the low end of the realistic range.
