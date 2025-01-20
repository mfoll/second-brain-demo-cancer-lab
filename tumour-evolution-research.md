---
type: Responsibility
status: Active
related_to:
  - "[[tumour-evolution]]"
  - "[[minimal-residual-disease]]"
  - "[[molecular-epidemiology]]"
  - "[[spatial-transcriptomics]]"
has:
  - "[[pancreatic-cfdna-mrd-study]]"
  - "[[northvale-early-detection-study]]"
  - "[[colorectal-metastasis-atlas]]"
  - "[[ch-cancer-risk-analysis]]"
_organized: true
---

# Tumour Evolution Research

The scientific programme of the Computational Tumour Evolution Group: how cancers arise, how they are detected before and after diagnosis, and how they change under treatment. It has no end date because studies start, finish and get replaced inside it; this note is the map of that portfolio.

## Scope

- Every study the group runs or leads analytically, from pre-diagnostic blood in the Northvale Health Cohort to cell-free DNA after surgery and spatial maps of treated metastases.
- Pilots that test whether a technology is worth adopting, including the ones we stopped. Their conclusions stay here because they shape later choices.
- Invited scientific writing that synthesises our own field, such as the [[mrd-review-article]].
- Not here: grant applications and funder reporting ([[secure-research-funding]]), team, compute and data practice ([[lead-tumour-evolution-group]]), the consortium's own deliverables ([[halo-consortium-work]]), teaching ([[teach-and-supervise]]) and institute committees ([[serve-corvane-institute]]). Projects in those trees often feed this one; link them laterally.

## Current State

- Three umbrella studies are active: the pancreatic MRD study, the Northvale early-detection study and the colorectal metastasis atlas. Two stand-alone analyses are active, one benchmark is paused, two pilots are closed.
- The most time-critical item is the [[mrd-manuscript]] revision: Reviewer 2 asked for external validation, which depends on Halo samples and on the [[data-access-policy-revision]].
- The atlas is past its pilot phase. 26 of 40 metastasis pairs are sequenced; the spatial pipeline has run on the Halyard GPU partition since 2026-09-22.
- [[owen-mcallister]] joins on 2027-01-11 and will work on the atlas with [[amara-okonkwo]].
- Funding: the atlas runs on the [[frontier-starting-grant]] until 2030; the next programme bid is the [[aurora-programme-grant-2027]].

## Active Projects and Workflows

### Pancreatic cfDNA MRD study

[[pancreatic-cfdna-mrd-study]] (Active since 2025-01-06) asks whether post-surgery cfDNA detects pancreatic cancer recurrence earlier than imaging, in 212 St Aldric patients. Lead: [[dmitri-halvorsen]]. Children:

- [[fragmentomics-classifier]] (Active): locked classifier from fragment length and end-motif features, to be validated on Halo samples. [[sofia-reyes-calderon]].
- [[methylation-panel-design]] (Completed 2025-09-15): the 1,840-region targeted panel. It replaced the [[exosome-rna-pilot]].
- [[clonal-hematopoiesis-filter]] (Active): removing white-blood-cell variants from cfDNA calls. [[hannah-lindqvist]].
- [[mrd-manuscript]] (Active): in major revision at Tumour Evolution Reports.

### Northvale early-detection study

[[northvale-early-detection-study]] (Active since 2025-02-03): how many years before diagnosis cfDNA methylation signals appear, in 410 incident cases and 820 matched controls. Lead: [[maja-kovac]]. Children:

- [[case-control-sample-selection]] (Completed 2025-10-17).
- [[lead-time-analysis]] (Active): conditional logistic models by time-to-diagnosis window, with reverse-causation sensitivity analyses.
- [[registry-linkage-update]] (Active): follow-up extended to 2025 through the Northern Cancer Registry.

### Colorectal metastasis atlas

[[colorectal-metastasis-atlas]] (Active since 2025-03-03): a spatial atlas of 40 colorectal liver metastases before and after chemotherapy. Lead: [[amara-okonkwo]]. Children:

- [[visium-hd-pilot]] (Completed 2025-08-29): Visium HD resolution is enough, with 8 µm bins as the analysis unit.
- [[deconvolution-benchmark]] (Active): seven deconvolution methods on low-count spots; preprint in preparation. [[kenji-mori]].
- [[atlas-data-portal]] (Idea): a public browser for the atlas.

### Stand-alone studies

- [[ch-cancer-risk-analysis]] (Active since 2025-10-06): clonal hematopoiesis as an exposure for incident solid cancers in a Northvale subcohort of 6,000. [[lucas-brandt]]. Shares variant calls with the CH filter.
- [[low-vaf-caller-benchmark]] (Paused since 2025): variant callers below 0.5% VAF; waits for the Halo truth set.
- [[mrd-review-article]] (Active since 2026-08-01): invited review for Computational Oncology Review.

### Closed pilots

- [[single-cell-cnv-pilot]] (Completed 2025-07-31): single-cell copy number added little to bulk multi-region phylogenies at its cost. [[felix-achterberg]].
- [[exosome-rna-pilot]] (Superseded 2025-06-30): RNA yield too low; budget moved to the methylation panel.

The cross-pilot lessons are in [[lessons-from-the-2025-pilots]].

## Next Actions

- [ ] Agree the external-validation route for the MRD manuscript revision once the data access policy outcome is known.
- [ ] Finish sequencing the last 14 atlas pairs and freeze the atlas analysis set.
- [ ] Post the deconvolution benchmark preprint with the failure-mode section intact.
- [ ] Decide whether to restart the low-VAF caller benchmark when the Halo truth set is released.
- [ ] Write the 2027 research plan section for each umbrella study ahead of the Aurora submission on 2026-12-04.

## Maintenance Log

- 2026-10-23: Portfolio overview reconciled after the atlas progress review and the GPU partition grant.
- 2026-08-01: MRD review article added.
- 2025-10-06: CH cancer risk analysis started as a stand-alone study rather than a child of the MRD study, because it answers an epidemiological question.
- 2025-07-31: Single-cell CNV pilot closed; exosome RNA pilot recorded as superseded.
