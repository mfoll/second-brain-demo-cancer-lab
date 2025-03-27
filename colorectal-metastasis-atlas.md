---
type: Project
status: Active
start: 2025-03-03
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[tumour-evolution]]"
  - "[[frontier-starting-grant]]"
has:
  - "[[visium-hd-pilot]]"
  - "[[deconvolution-benchmark]]"
  - "[[atlas-data-portal]]"
  - "[[atlas-tissue-manifest]]"
  - "[[tissue-section-qc]]"
_organized: true
---

# Colorectal Metastasis Atlas

A spatial transcriptomic atlas of 40 colorectal liver metastases, each profiled before chemotherapy (core biopsy) and after it (resection), to see which tumour clones and which microenvironments survive treatment. Lead analyst [[amara-okonkwo]]; pathology [[benedikt-kraus]]; PI Ines Varga.

## Outcome

A frozen, annotated Visium HD dataset of 80 sections (40 pre/post pairs), a description of how tumour subclones and the immune and stromal niches change under chemotherapy, and an atlas paper. A public browser is a separate, later project ([[atlas-data-portal]]).

## Current State

- 26 of 40 pairs are sequenced (batch 1: 12 pairs, batch 2: 14 pairs). Batch 3 (14 pairs) is sectioned and QC-passed and waits for a sequencing slot in November 2026 ([[atlas-sequencing-batch-plan]]).
- Analysis unit is the 8 µm bin, decided at the end of the [[visium-hd-pilot]] ([[visium-hd-pilot-decision-2025-08-28]]). Cell segmentation with bin2cell is a secondary layer, still under evaluation ([[should-the-atlas-use-bin2cell-segmentation]]).
- The spatial pipeline runs on the Halyard GPU partition since it was granted on 2026-09-22 ([[halyard-cluster]]). Until then nucleus segmentation sat on Kestrel CPU nodes and the migration stalled.
- The [[deconvolution-benchmark]] showed that two common methods silently collapse low-count spots onto hepatocytes. Post-chemotherapy fibrotic regions are exactly where counts are low, so the atlas will not use either method without a low-count flag.
- [[owen-mcallister]] joins on 2027-01-11 and takes over the clone-tracking analysis ([[owen-atlas-onboarding-plan]]).

## Scope and Boundaries

In scope: tissue selection with the Westmere Cancer Centre hepatobiliary team, section QC, Visium HD runs through the sequencing core, analysis, the atlas paper. Out of scope: the deconvolution method paper (its own child project), cfDNA work on the same patients (not consented), and any clinical prediction claim. Tissue and clinical data stay in governed storage; the vault holds pointers only ([[atlas-tissue-manifest]], [[atlas-clinical-annotation-table]]).

## Working Context

The design is paired: the same metastasis before and after chemotherapy ([[paired-pre-post-treatment-design]]). That makes the core-biopsy question central, since a 1 mm core may miss subclones that the resection shows ([[are-pre-chemo-core-biopsies-representative]]). Copy-number subclones are inferred from expression ([[can-spatial-cnv-replace-single-cell-dna]]), which is also why the [[single-cell-cnv-pilot]] result matters here: we chose not to add single-cell DNA. Regression grade from Benedikt's review stratifies responders ([[tumour-regression-grade]]).

The literature most often reopened: [[shi-2024-crlm-evolution-under-chemotherapy]] for the genomic-versus-transcriptomic contrast, [[bellomo-2026-thbs1-spp1-crlm]] for myeloid niches, [[escriva-conde-2026-crlm-growth-patterns]] for growth patterns.

## Active Workflows

- Section QC before every batch: [[tissue-section-qc]].
- Pipeline: Space Ranger then the Nextflow spatial pipeline ([[atlas-spatial-pipeline-repository]]), part of [[nextflow-pipeline-migration]] and [[halyard-cluster-migration]].
- Monthly atlas meeting (Amara, Kenji, Benedikt, Ines); last full review [[atlas-progress-review-2026-10-07]].

## Next Actions

- [ ] Sequence batch 3 and run it through the pipeline on Halyard.
- [ ] Freeze the atlas analysis set (80 sections, annotations, clinical table) before Owen starts.
- [ ] Choose the deconvolution approach for the atlas from the benchmark results, with low-count flagging.
- [ ] Decide whether bin2cell segmentation enters the main analysis.
- [ ] Draft the atlas paper figure plan for the 2027 research plan.

## Open Questions

- [[are-pre-chemo-core-biopsies-representative]]
- [[should-the-atlas-use-bin2cell-segmentation]]
- [[how-to-handle-hepatocyte-dominance-in-deconvolution]]
- [[can-spatial-cnv-replace-single-cell-dna]]
- [[what-access-model-for-the-atlas-data-portal]]

## Important Notes

- [[visium-hd-pilot-report]]
- [[atlas-tissue-manifest]]
- [[low-count-spot-collapse]]
- [[benchmarks-must-report-failure-modes]]
- [[visium-hd-cost-model]]

## Do Not Do Yet

> [!danger]
> Do not run cross-sample comparisons of post-chemotherapy cell-type proportions until the deconvolution method for the atlas is chosen and low-count spots are flagged; the obvious defaults invent hepatocytes in fibrotic tissue.

## Maintenance Log

- 2026-10-07: Progress review; 26/40 pairs sequenced, pipeline on Halyard GPU, Owen's onboarding agreed.
- 2026-09-22: Halyard GPU partition granted; segmentation unblocked.
- 2026-02-18: Benchmark failure mode found; atlas deconvolution put on hold.
- 2025-11-28: Frontier Starting Grant awarded; funds the atlas until 2030.
- 2025-08-28: Visium HD accepted with 8 µm bins; standard Visium plan archived ([[standard-visium-atlas-plan]]).
