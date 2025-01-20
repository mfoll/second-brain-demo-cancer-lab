---
type: Project
status: Completed
start: 2025-01-06
end: 2025-07-31
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[tumour-evolution]]"
  - "[[felix-achterberg]]"
  - "[[multi-region-bulk-phylogeny]]"
has:
  - "[[single-cell-cnv-pilot-report]]"
  - "[[single-cell-cnv-cost-comparison]]"
  - "[[single-cell-cnv-pilot-review-2025-07-24]]"
_organized: true
---

# Single-Cell CNV Pilot

A seven-month pilot, run by [[felix-achterberg]], testing whether low-pass single-cell DNA sequencing of copy number adds anything to the phylogenies we already build from multi-region bulk sequencing. The answer, at current cost, was no.

## Outcome

A decision on whether to add single-cell copy number to our tumour evolution studies, with the conditions under which to reconsider. Reached on 2025-07-24 ([[single-cell-cnv-pilot-review-2025-07-24]]): do not adopt.

## Current State

- Completed 2025-07-31. Felix left for industry in August 2025; the data and code are archived ([[single-cell-cnv-pilot-data]]).
- Four colorectal tumours with existing multi-region bulk whole-genome data (four to six regions each) were profiled; 1,612 nuclei passed QC across the four.
- In all four tumours the single-cell trees recovered the same major clades as the bulk multi-region trees. In one tumour the single-cell data resolved an extra minor subclone (about 4% of cells) that bulk could not separate; it changed no conclusion we cared about.
- Cost was about 11,500 EUR per tumour against about 1,900 EUR for one extra bulk region ([[single-cell-cnv-cost-comparison]]).

## Scope and Boundaries

Copy number only, low-pass, nuclei from frozen tissue. Joint SNV and copy-number calling from targeted single-cell panels was read about ([[sollier-2023-compass]]) but not tested. Spatial inference of copy number from expression was not part of this pilot; it later became the route for the atlas ([[can-spatial-cnv-replace-single-cell-dna]]).

## Working Context

Felix compared trees from three single-cell methods, chosen after reading [[liu-2024-nestedbd]], [[weiner-2025-dice-copy-number-phylogenies]] and [[ivanovic-2025-cnrein]], against the bulk trees from our standard approach ([[multi-region-bulk-phylogeny]]). Noise in per-cell copy-number calls was the main practical problem: the evolution-aware caller reduced spurious changes, but tree topology was stable only for the major clades.

The question that would make single-cell worth its cost is rare subclones, for example resistance seeds present at a few percent before treatment. That is an atlas question, and the atlas answers it more cheaply from spatial expression, at lower resolution.

## Important Notes

- [[single-cell-cnv-pilot-report]]
- [[single-cell-cnv-cost-comparison]]
- [[lessons-from-the-2025-pilots]]
- [[pilots-need-a-written-stop-rule]]

## Maintenance Log

- 2025-07-31: Closed. Data archived to governed storage before Felix's departure.
- 2025-07-24: Review meeting; do not adopt. Reconsider if cost per tumour falls below about 3,000 EUR or a study needs subclones below 5%.
- 2025-05-09: All four tumours sequenced; tree comparison started.
- 2025-01-06: Started with Felix Achterberg.
