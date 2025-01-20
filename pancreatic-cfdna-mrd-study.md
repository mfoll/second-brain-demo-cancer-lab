---
type: Project
status: Active
start: 2025-01-06
belongs_to: "[[tumour-evolution-research]]"
has:
  - "[[fragmentomics-classifier]]"
  - "[[clonal-hematopoiesis-filter]]"
  - "[[mrd-manuscript]]"
  - "[[st-aldric-mrd-cohort]]"
  - "[[methylation-panel-design]]"
related_to:
  - "[[minimal-residual-disease]]"
  - "[[cfdna-fragmentomics]]"
  - "[[samuel-okoye]]"
  - "[[dmitri-halvorsen]]"
_organized: true
---

# Pancreatic cfDNA MRD Study

Umbrella study testing whether serial cell-free DNA after pancreatic cancer surgery detects recurrence earlier than routine imaging, in 212 resected patients from St Aldric University Hospital. Ines Varga is PI, [[dmitri-halvorsen|Dmitri Halvorsen]] runs the cfDNA side day to day, and [[samuel-okoye|Samuel Okoye]] is the clinical lead at St Aldric.

## Outcome

A peer-reviewed result showing that a combined methylation, fragmentomics and variant-based MRD call detects pancreatic cancer recurrence earlier than three-monthly CT, with external validation on samples that were not used to build any part of the model. The working target is the [[mrd-manuscript|MRD Manuscript]] in Tumour Evolution Reports.

## Current State

- The [[mrd-manuscript|MRD Manuscript]] received a major revision on 2026-07-14 ([[mrd-manuscript-decision-2026-07-14]]). Reviewer 2 requires external validation. The editor extended the deadline to 2027-01-29 ([[mrd-revision-extension-2026-10-07]]).
- External validation is blocked: the candidate samples come from the [[halo-cross-site-benchmark|Halo Cross-Site Benchmark]] and its [[halo-truth-set]], and their transfer needs the consortium clause of the [[data-access-policy-revision|Data Access Policy Revision]], which the board discussed on 2026-09-10 without adopting it; it returns on 2026-11-12 ([[data-governance-board-2026-09-10]]).
- The [[fragmentomics-classifier|Fragmentomics Classifier]] is a stacked model: regularised logistic regression on fragment-length features plus gradient boosting kept for end-motif features. The [[lab-meeting-2026-03-12|lab meeting of 2026-03-12]] first decided to drop gradient boosting entirely because it overfitted St Aldric extraction batches; the [[classifier-design-review-2026-04-02|review of 2026-04-02]] kept it for end motifs only.
- The [[clonal-hematopoiesis-filter|Clonal Hematopoiesis Filter]] works with matched buffy coat; whether a panel of normals is enough is still open ([[do-we-still-need-matched-buffy-coat-sequencing]]).
- The [[methylation-panel-design|1,840-region methylation panel]] is complete and QC-passed since 2025-09-15.

## Scope and Boundaries

In scope: the [[st-aldric-mrd-cohort|St Aldric MRD cohort]] (212 patients, 1,468 plasma time points), the methylation panel, shallow whole-genome fragmentomics, the CH filter and the manuscript. Outcome ascertainment uses St Aldric imaging plus the Northern Cancer Registry under the [[registry-linkage-agreement|institute linkage agreement]].

Out of scope: pre-diagnostic detection in the Northvale cohort (that is the [[northvale-early-detection-study|Northvale Early Detection Study]]), the cross-site assay comparison itself (owned by [[halo-consortium-work|Halo Consortium Work]]) and clinical decision-making. Patient-level data stay in governed storage; the vault only points to it through [[st-aldric-mrd-cohort]] and [[st-aldric-data-dictionary-v3]].

## Working Context

The study has three signal layers. Tumour-informed variants from the resected tumour give the most specific call but miss patients whose tumour sequencing failed (23 of 212). The methylation panel gives a tumour-naive call with a spike-in limit of detection around 0.1% tumour fraction ([[methylation-panel-spike-in-titration-2025-08]]). Fragmentomics adds sensitivity at low tumour fraction but is the layer most exposed to pre-analytical variation, which is why the [[extraction-kit-lot-change-2025-06-16|extraction kit lot change]] became the central methodological problem of 2026. See [[tumour-informed-vs-tumour-naive-mrd]] and [[batch-confounding-in-cfdna-studies]].

In the submitted analysis, the landmark call at post-operative day 28 detected 86 of 121 recurrences (71%) with 84 of 91 non-recurrent patients negative (92%), and serial monitoring preceded imaging by a median of 4.3 months ([[molecular-lead-time]]). These numbers will move once the stacked classifier and the CH filter are applied in the revision.

Clonal hematopoiesis calls are shared with [[ch-cancer-risk-analysis|CH Cancer Risk Analysis]]: noise here, exposure there. The [[clonal-hematopoiesis]] Concept explains why one callset serves both.

## Active Workflows

- Sample QC: [[cfdna-extraction-qc]] for every new extraction batch, logged in [[cfdna-extraction-qc-log-2026]].
- Model updates: [[fragmentomics-classifier-retraining]], which forces a leave-batch-out evaluation before any change is accepted.
- Monthly MRD study meeting, first Wednesday, notes as Events (latest: [[mrd-revision-planning-2026-07-21]]).
- Pipelines move to Nextflow on Halyard with [[tobias-wren|Tobias Wren]] under [[nextflow-pipeline-migration]].

## Next Actions

- [ ] Secure external validation samples: follow the consortium clause through the board with [[yara-castellanos|Yara Castellanos]] and keep the [[halo-validation-request-2026-08-04|Halo request]] alive.
- [ ] Lock the stacked classifier (model card v3) before any Halo data are seen.
- [ ] Re-run the full St Aldric analysis with the CH filter and stacked classifier for the revision.
- [ ] Decide the buffy coat strategy for the remaining 152 patients without matched sequencing.
- [ ] Draft the response to reviewers ([[mrd-response-to-reviewers-draft-2026-10]]) so that only the validation section waits on Halo.

## Open Questions

- [[can-halo-samples-serve-as-external-validation]]
- [[do-we-still-need-matched-buffy-coat-sequencing]]
- [[does-the-stacked-classifier-generalise-across-extraction-batches]]
- [[what-lead-time-over-imaging-is-clinically-meaningful]]
- [[what-vaf-threshold-defines-a-positive-mrd-call]]

## Important Notes

- [[st-aldric-mrd-cohort]]: cohort, consent scope and governed storage.
- [[mrd-manuscript-decision-2026-07-14]]: what the reviewers asked.
- [[classifier-design-review-2026-04-02]]: why the classifier is stacked.
- [[clonal-hematopoiesis]]: one callset, two roles.
- [[mrd-revision-response-plan]]: the revision work plan.

## Do Not Do Yet

> [!danger]
> Do not run the classifier on any Halo sample, or let anyone see Halo outcomes, until model card v3 is frozen and committed; otherwise the validation is no longer external.

## Maintenance Log

- 2026-10-07: Revision deadline extended to 2027-01-29; validation still waiting on the data access policy.
- 2026-07-14: Major revision from Tumour Evolution Reports; external validation becomes the critical path.
- 2026-04-02: Classifier design settled as a stacked model after the 2026-03-12 decision was partly reversed.
- 2026-02-27: Manuscript submitted.
- 2025-09-15: Methylation panel QC signed off; panel design project completed.
