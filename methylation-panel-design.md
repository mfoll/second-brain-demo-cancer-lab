---
type: Project
status: Completed
start: 2025-01-20
end: 2025-09-15
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
has:
  - "[[methylation-panel-design-document-v4]]"
  - "[[methylation-panel-qc-report-2025-09]]"
  - "[[methylation-panel-qc-sign-off-2025-09-15]]"
related_to:
  - "[[dmitri-halvorsen]]"
  - "[[exosome-rna-pilot]]"
  - "[[ben-whitfield]]"
_organized: true
---

# Methylation Panel Design

Design, ordering and QC of a 1,840-region targeted methylation capture panel for tumour-naive detection of pancreatic cancer in post-operative plasma. Completed on 2025-09-15 when the QC report was signed off.

## Outcome

A 1,840-region targeted methylation panel ordered and QC-passed. Reached on 2025-09-15 ([[methylation-panel-qc-sign-off-2025-09-15]]).

## Current State

- Completed. The panel is in routine use for the [[st-aldric-mrd-cohort|St Aldric cohort]]; 1,402 of 1,468 plasma time points were run through it by 2025-12.
- Final design: 1,214 pancreatic-cancer hypermethylated regions, 412 tissue-of-origin regions (pancreas, liver, blood lineages) and 214 normalisation and control regions ([[methylation-panel-region-list]]).
- QC: 98.6% of regions above 500x median deduplicated depth in the validation run; conversion efficiency above 99.2%; limit of detection about 0.1% tumour fraction at 30 ng input ([[methylation-panel-qc-report-2025-09]], [[methylation-panel-spike-in-titration-2025-08]]).
- Remaining stock: two 96-reaction kits, enough for the revision reruns but not for a Halo validation set run at Corvane.

## Scope and Boundaries

Covered design, vendor choice, ordering, wet-lab validation and sign-off. Routine running of the panel and its downstream calls belong to [[pancreatic-cfdna-mrd-study]]. The panel replaced the [[exosome-rna-pilot|Exosome RNA Pilot]], which was superseded in 2025-06 when the methylation spike-ins clearly beat the exosome RNA signal at low input.

## Working Context

Region selection started from public tumour and normal methylomes and the group's own tissue methylation data, then removed regions that are methylated in blood cells at more than 5% because they would mimic tumour signal in leukocyte-rich cfDNA. The design was frozen at version 4 on 2025-04-09 ([[methylation-panel-design-document-v4]]). The vendor's field application scientist, [[ben-whitfield|Ben Whitfield]], helped with probe tiling; the quote and its 18% academic discount are in [[methylation-panel-vendor-quote-2025-06]].

Enzymatic conversion was chosen over bisulfite because the post-operative extracts were small (median 14 ng) and bisulfite losses would have pushed many samples below usable input. That trade-off is summarised in the [[pharo-2025-methylation-biomarker-roadmap|methylation roadmap review]] we read later; its advice on targeted validation matches what we did.

## Decisions and Rejected Options

- Enzymatic conversion rather than bisulfite, because of low input.
- 1,840 regions rather than a 6,000-region discovery panel: similar simulated sensitivity at our depth for about 40% of the per-sample cost.
- Blood-methylated regions removed at a 5% threshold. A stricter 2% threshold was tested and lost 140 informative regions for little gain in specificity.
- Excluded regions (22) are dropped from scoring but not redesigned, to avoid a second ordering cycle.
- UMI adapters from the start, so that the same libraries could later serve variant calling if needed.

## Lessons Kept

The panel run order was randomised from the first production run ([[sequencing-run-sheet-sa-r11]]), which protected the methylation layer from the extraction lot confounding that later hit fragmentomics ([[batch-confounding-in-cfdna-studies]]). This was Dmitri's call and is now standard for every assay in the study.

## Use Beyond St Aldric

The panel was designed for pancreatic cancer but about 400 of its tissue-of-origin and control regions are generic. The [[northvale-early-detection-study|Northvale Early Detection Study]] considered it in 2025 and chose its own assay; the overlap is documented in the region list so that results can be compared if both studies publish. For Halo validation, the panel would only be run at Corvane if samples could be shipped, which the current governance does not allow.

## Next Actions

- [x] Order panel (2025-06-20).
- [x] Spike-in titration (2025-08).
- [x] QC sign-off (2025-09-15).
- [ ] Hand the region list and QC report to the [[mrd-review-article|MRD Review Article]] as a worked example of panel design.

## Important Notes

- [[methylation-panel-design-document-v4]]
- [[methylation-panel-qc-report-2025-09]]
- [[methylation-panel-qc-sign-off-2025-09-15]]
- [[limit-of-detection-in-cfdna-assays]]

## Maintenance Log

- 2025-09-15: QC signed off by Dmitri, Elias and Rafael Ibarrondo; project completed.
- 2025-08-22: Spike-in titration finished; limit of detection about 0.1% tumour fraction.
- 2025-06-20: Panel ordered.
- 2025-04-09: Design frozen at version 4.
- 2025-01-20: Project started.
