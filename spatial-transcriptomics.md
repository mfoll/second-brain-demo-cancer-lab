---
type: Topic
related_to:
  - "[[colorectal-metastasis-atlas]]"
  - "[[tumour-evolution]]"
  - "[[pathology-foundation-models]]"
_organized: true
---

# Spatial Transcriptomics

Retrieval surface for everything the group knows and has decided about measuring gene expression in tissue sections: platforms, resolution, deconvolution, segmentation and spatial copy-number inference. Most of it comes from the [[colorectal-metastasis-atlas]] and its children.

## Where Our Work Lives

- [[colorectal-metastasis-atlas]]: 40 colorectal liver metastases before and after chemotherapy, on Visium HD.
- [[visium-hd-pilot]]: why Visium HD with 8 µm bins ([[visium-hd-pilot-decision-2025-08-28]]).
- [[deconvolution-benchmark]]: seven methods, low-count failure modes.
- [[atlas-data-portal]]: public browser, an idea for now.

## Core Ideas

- [[visium-hd-bin-size]]: 2, 8 or 16 µm, and what each costs in counts and in tissue detail.
- [[cell-type-deconvolution]] and its main failure in our hands, [[low-count-spot-collapse]].
- [[pathologist-annotations-anchor-spatial-clusters]] and [[benchmarks-must-report-failure-modes]], the two stances that most shape how we analyse.
- [[tissue-section-qc]]: the procedure that keeps bad sections off the slide.

## Literature Entry Points

- Platforms: [[rademacher-2025-spatial-technologies-tumour-cryosections]], [[long-2025-xenium-5k-vs-visium-hd]], [[hasan-2026-visium-hd-human-liver]].
- Segmentation: [[polanski-2024-bin2cell]].
- Deconvolution: [[slabowska-2024-deconvolution-evaluation]], [[chen-2024-nlsdeconv]], [[wang-2025-declust-cluster-deconvolution]], [[wang-2025-harmodecon]].
- Copy number from spatial data: [[zhang-2025-slidecna]], [[denisenko-2024-ovarian-subclones-spatial]].
- Liver metastasis biology: [[bellomo-2026-thbs1-spp1-crlm]], [[escriva-conde-2026-crlm-growth-patterns]].

## Open Questions

- [[should-the-atlas-use-bin2cell-segmentation]]
- [[how-to-handle-hepatocyte-dominance-in-deconvolution]]
- [[can-spatial-cnv-replace-single-cell-dna]]

## People

[[amara-okonkwo]], [[kenji-mori]], [[benedikt-kraus]], [[marco-bellini]], and from 2027-01-11 [[owen-mcallister]].

## Decisions on Record

- Visium HD with 8 µm bins over standard Visium and over targeted imaging panels ([[visium-hd-pilot-decision-2025-08-28]]); the old plan is archived as [[standard-visium-atlas-plan]].
- No cross-sample cell-type comparisons in the atlas until low-count bins are flagged ([[deconvolution-failure-mode-review-2026-02-18]]).
- Copy-number subclones from expression rather than single-cell DNA ([[single-cell-cnv-pilot-review-2025-07-24]]).
- Pipeline on Halyard with GPU segmentation from 2026-09-22 ([[atlas-spatial-pipeline-repository]], [[halyard-cluster]]).

## How to Use This Topic

Start here for any question about spatial methods; for the state of the atlas itself go to [[colorectal-metastasis-atlas]].

Adjacent reading on tissue-image models sits in [[pathology-foundation-models]], an exploration cluster that may matter once the atlas starts linking H&E morphology to expression. Pipeline and container practice for spatial work is shared with the cfDNA side through [[reproducible-pipelines]].
