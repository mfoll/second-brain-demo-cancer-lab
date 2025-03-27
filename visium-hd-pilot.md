---
type: Project
status: Completed
start: 2025-03-03
end: 2025-08-29
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[amara-okonkwo]]"
  - "[[benedikt-kraus]]"
has:
  - "[[visium-hd-pilot-report]]"
  - "[[visium-hd-pilot-decision-2025-08-28]]"
  - "[[visium-hd-bin-size]]"
_organized: true
---

# Visium HD Pilot

A six-month pilot to decide whether Visium HD gives enough resolution and enough counts on archival liver metastasis tissue to carry the [[colorectal-metastasis-atlas]], before committing grant money to 80 sections.

## Outcome

A go or no-go decision on Visium HD for the atlas, with the analysis unit fixed. Reached on 2025-08-28: go, with 8 µm bins as the unit of analysis ([[visium-hd-pilot-decision-2025-08-28]]).

## Current State

- Completed 2025-08-29. Nothing is expected here; follow-up work lives in the atlas and the [[deconvolution-benchmark]].
- Seven FFPE sections were run: three metastases as pre-chemotherapy biopsy and post-chemotherapy resection pairs, plus one block of adjacent normal liver ([[visium-hd-pilot-report]]).
- At 8 µm, resections gave a median of 214 UMIs and 141 genes per bin; biopsies were lower at 128 UMIs. At 2 µm the median was 11 UMIs, too sparse to use alone. 16 µm bins blurred the invasive margin that [[benedikt-kraus]] annotated.
- Cost per section, all in, was about 5,400 EUR ([[visium-hd-cost-model]]).

## Scope and Boundaries

Technical feasibility only: section quality, counts per bin, whether pathologist-annotated structures (invasive margin, fibrotic capsule, residual tumour islands) are recoverable. Biological findings from seven sections were explicitly out of scope, and none were written up.

## Working Context

The alternative on the table was standard Visium with 55 µm spots, which the group had used before ([[standard-visium-atlas-plan]]). With 55 µm spots each spot mixes 10 to 30 cells, and in treated metastases the interesting structures (thin rims of residual tumour along fibrosis) are narrower than a spot. The pilot compared bin sizes on the same sections and tried cell reconstruction with bin2cell ([[polanski-2024-bin2cell]], [[bin2cell-software]]). Bin2cell worked on resections and was patchy on biopsies with crush artefact, which is why segmentation stayed a secondary layer ([[should-the-atlas-use-bin2cell-segmentation]]).

Platform comparisons read during the pilot: [[rademacher-2025-spatial-technologies-tumour-cryosections]] and, after the decision, [[long-2025-xenium-5k-vs-visium-hd]]. Imaging-based targeted panels were rejected because the atlas needs whole-transcriptome coverage to infer copy-number subclones.

Section handling problems in the pilot (one biopsy with DV200 below 30%, one section with a fold across the capture area) produced the [[tissue-section-qc]] procedure.

## Important Notes

- [[visium-hd-pilot-report]]
- [[visium-hd-run-qc-metrics]]
- [[visium-hd-bin-size]]
- [[visium-hd-product-documentation]]
- [[space-ranger-documentation]]

## Maintenance Log

- 2025-08-29: Closed after the decision meeting; report filed.
- 2025-08-28: Decision: Visium HD with 8 µm bins; standard Visium plan archived.
- 2025-06-12: Sequencing of the seven pilot sections returned; first count summaries.
- 2025-03-03: Started with [[amara-okonkwo]] and [[benedikt-kraus]]; blocks selected from the Westmere tissue archive.
