---
type: Project
status: Active
start: 2025-09-01
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[kenji-mori]]"
  - "[[spatial-transcriptomics]]"
  - "[[benchmarks-must-report-failure-modes]]"
has:
  - "[[deconvolution-benchmark-config]]"
  - "[[deconvolution-simulated-datasets]]"
  - "[[deconvolution-method-comparison-table]]"
  - "[[deconvolution-benchmark-preprint-draft]]"
  - "[[low-count-spot-collapse]]"
_organized: true
---

# Deconvolution Benchmark

A benchmark of seven cell-type deconvolution methods on Visium HD bins, with a focus on what happens to low-count spots. It is [[kenji-mori]]'s first thesis chapter and decides which method the [[colorectal-metastasis-atlas]] uses.

## Outcome

A preprint describing accuracy and failure behaviour of seven methods across count depths, with code and simulated data released, and a method recommendation for the atlas.

## Current State

- All seven methods have run on 12 simulated slides at five UMI depths (25, 50, 100, 200 and 400 per spot) and on the seven pilot sections ([[deconvolution-method-comparison-table]]).
- Main finding (first shown on 2026-02-18, [[deconvolution-failure-mode-review-2026-02-18]]): below about 60 UMIs per spot, two widely used methods assign most of the spot to hepatocytes, the most abundant cell type in the reference, whatever the true composition, and their per-spot confidence output does not flag it ([[low-count-spot-collapse]]).
- In the methods' own outputs these two are labelled M3 and M5 until the preprint. One developer, [[marco-bellini]], confirmed the mechanism on 2026-05-21 and plans a warning in his next release ([[marco-bellini-call-2026-05-21]]).
- Draft v0.6 has figures 1 to 4; the discussion and the failure-mode figure are being rewritten ([[deconvolution-benchmark-preprint-draft]]).

## Scope and Boundaries

Seven methods chosen in September 2025 for coverage of model families: probabilistic reference-based (two), regression-based (two), NMF-based, cluster-based and one deep-learning method. Adding methods after the freeze on 2025-11-14 is out of scope for this preprint, including DECLUST and HarmoDecon, which we read after the freeze ([[wang-2025-declust-cluster-deconvolution]], [[wang-2025-harmodecon]]). Real atlas sections are used only as an applied example, not as ground truth.

## Working Context

Ground truth comes from simulation: segmented cells from the pilot resections, aggregated into 8 µm and 16 µm pseudo-spots and downsampled ([[deconvolution-simulated-datasets]]). Kenji's early simulations used reference single-cell depth, which flattered every method; Amara caught it in November 2025 and the simulations were redone at real Visium HD depth ([[simulations-must-match-real-count-depth]]).

The failure matters for the atlas because 18% of 8 µm bins in pre-chemotherapy biopsies and 27% in post-chemotherapy fibrotic regions fall below 60 UMIs. Comparing proportions before and after treatment with M3 or M5 would show hepatocytes appearing in scar tissue.

Earlier benchmarks shaped the design: [[slabowska-2024-deconvolution-evaluation]], [[huuki-myers-2025-deconvolution-benchmark-dlpfc]], [[chen-2024-nlsdeconv]] and the reproducibility workflow of [[amblard-2025-deconvolution-benchmark-workflow]].

## Active Workflows

- Benchmark runs from [[deconvolution-benchmark-repository]] with frozen parameters in [[deconvolution-benchmark-config]]; on Halyard since 2026-09.
- Weekly check-in, Kenji and [[amara-okonkwo]]; monthly with Ines.

## Next Actions

- [ ] Finish the failure-mode figure: assigned composition against true composition by UMI depth, all seven methods.
- [ ] Decide how to name M3 and M5 in the preprint ([[how-to-report-failing-methods-in-the-benchmark]]).
- [ ] Send the draft to both developers two weeks before posting.
- [ ] Post the preprint and release the simulated slides.
- [ ] Recommend the atlas method with a low-count flag threshold.

## Open Questions

- [[how-to-report-failing-methods-in-the-benchmark]]
- [[how-to-handle-hepatocyte-dominance-in-deconvolution]]
- [[which-reference-for-liver-metastasis-deconvolution]]

## Important Notes

- [[benchmarks-must-report-failure-modes]]
- [[cell-type-deconvolution]]
- [[kenji-benchmark-slides-2026-02]]
- [[deconvolution-benchmark-preprint-outline]]

## Maintenance Log

- 2026-09-24: Benchmark reruns moved to Halyard after the GPU partition grant.
- 2026-05-21: Call with Marco Bellini; mechanism confirmed for one of the two methods.
- 2026-02-18: Failure mode presented to the group; atlas deconvolution put on hold.
- 2025-11-14: Method list and parameters frozen; simulations redone at real depth.
- 2025-09-01: Started.
