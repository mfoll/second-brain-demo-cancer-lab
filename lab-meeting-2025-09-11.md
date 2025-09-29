---
type: Event
date: 2025-09-11
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[nextflow-pipeline-migration]]"
  - "[[deconvolution-benchmark]]"
  - "[[single-cell-cnv-pilot]]"
_organized: true
---

# Lab Meeting 2025-09-11

First meeting after the summer. Chair Ines Varga, notes [[sofia-reyes-calderon]]. Twelve present.

## Decisions

- **Pipelines move to Nextflow.** After two discussions over the summer, [[tobias-wren]] proposed rewriting the cfDNA and spatial pipelines in Nextflow. [[dmitri-halvorsen]] argued for cleaning up the existing Snakemake code ([[molder-2021-sustainable-data-analysis-snakemake]]). Decided for Nextflow because Halo sites run nf-core pipelines and the cfDNA pipeline will be shared with them. [[nextflow-pipeline-migration]] starts on 2025-10-06.
- **Single-cell CNV closed.** The [[single-cell-cnv-pilot]] ended on 2025-07-31: single-cell copy number did not add enough to bulk phylogenies at this cost. Data archived whole; no further sequencing.
- **Atlas.** The [[visium-hd-pilot]] closed on 2025-08-29. The atlas proceeds with Visium HD; low-count spots need deconvolution, and [[kenji-mori]] starts the [[deconvolution-benchmark]] (begun 2025-09-01) before any method is chosen.
- **Methylation panel.** The QC run is finishing; [[dmitri-halvorsen]] expects sign-off by 2025-09-15, which would close [[methylation-panel-design]].

## Actions

- Tobias: Nextflow repository skeleton following nf-core module conventions.
- Kenji: shortlist of seven deconvolution methods.
