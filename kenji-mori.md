---
type: Person
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[deconvolution-benchmark]]"
  - "[[amara-okonkwo]]"
  - "[[colorectal-metastasis-atlas]]"
_organized: true
---

# Kenji Mori

PhD student, second year, supervised by Ines with [[amara-okonkwo]] as co-supervisor. His thesis is on cell-type composition in spatial data of treated tumours; the first chapter is the [[deconvolution-benchmark]].

## Role

- Runs the benchmark end to end: simulation, method wrappers, metrics, figures and the preprint draft ([[deconvolution-benchmark-preprint-draft]]).
- Maintains [[deconvolution-benchmark-repository]] and its frozen configuration ([[deconvolution-benchmark-config]]).
- Will apply the chosen method to the atlas sections once the benchmark recommends one.

## How We Work Together

Weekly check-in with Amara, monthly with Ines, written agenda in the shared benchmark notes. Kenji is careful and quiet in group meetings; the failure-mode result came out first in his one-to-one and was then presented at the lab meeting on 2026-02-18 ([[deconvolution-failure-mode-review-2026-02-18]], [[kenji-benchmark-slides-2026-02]]). Encourage him to present it outside the group: the symposium poster session ([[tumour-evolution-symposium-2026]]) is the next chance.

He handled the contact with [[marco-bellini]] well, sending a reproducible example before the call ([[marco-bellini-call-2026-05-21]]).

## Current Threads

- Failure-mode figure and the discussion section.
- How to name the two failing methods in the preprint ([[how-to-report-failing-methods-in-the-benchmark]]).
- Choice of single-cell reference for liver metastases ([[which-reference-for-liver-metastasis-deconvolution]]).
- Benchmark reruns on Halyard since September 2026; he had his first Apptainer image built in CI by [[tobias-wren]].

## Links

- [[low-count-spot-collapse]]
- [[benchmarks-must-report-failure-modes]]
- [[cell-type-deconvolution]]

## Background and Progress

Kenji started his PhD in September 2025, the week after the [[visium-hd-pilot-decision-2025-08-28]], with a master's in statistics and little biology. The first months went into reading benchmark papers and building the simulation framework; the depth mistake in his first simulations was a useful lesson rather than a setback ([[simulations-must-match-real-count-depth]]). His first-year review in September 2026 went well. The preprint is the milestone for his second-year plan, and the atlas application of his recommended method is planned as chapter two.
