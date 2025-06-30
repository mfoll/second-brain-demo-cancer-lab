---
type: Project
status: Active
start: 2025-06-02
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
has:
  - "[[clonal-hematopoiesis]]"
  - "[[do-we-still-need-matched-buffy-coat-sequencing]]"
  - "[[ch-buffy-coat-pilot-results-2026-01]]"
  - "[[ch-subcohort-variant-calls]]"
related_to:
  - "[[hannah-lindqvist]]"
  - "[[ch-cancer-risk-analysis]]"
  - "[[minimal-residual-disease]]"
_organized: true
---

# Clonal Hematopoiesis Filter

A filter that removes white-blood-cell variants from cfDNA variant calls so that clonal hematopoiesis (CH) is not mistaken for residual pancreatic cancer. It is [[hannah-lindqvist|Hannah Lindqvist]]'s PhD project, supervised by Ines with [[dmitri-halvorsen|Dmitri Halvorsen]].

## Outcome

A validated filter usable in two modes: with a matched buffy coat (reference standard) and without one (panel of normals plus variant features), with documented sensitivity for CH removal and loss of true tumour variants in each mode.

## Current State

- Matched mode works. In the 60-patient buffy coat pilot, 31% of cfDNA variants passing the caller were also present in buffy coat and therefore CH, mostly DNMT3A, TET2, ASXL1, PPM1D and TP53 ([[ch-buffy-coat-pilot-results-2026-01]]).
- Unmatched mode: a panel of normals built from the Northvale CH callset recovers 84% of the CH variants found by matched buffy coat in the pilot; it misses private, low-frequency clones ([[ch-panel-of-normals-v1]]).
- Matched buffy coat sequencing costs about 180 EUR per sample ([[buffy-coat-sequencing-cost-estimate-2025-11]]). Whether we still need it for the other 152 patients is open: [[do-we-still-need-matched-buffy-coat-sequencing]].
- Reviewer 1 on the manuscript asked how CH was handled, which makes this filter part of the revision ([[mrd-manuscript-decision-2026-07-14]]).

## Scope and Boundaries

In scope: CH detection in buffy coat, the panel of normals, the filter logic and its evaluation on St Aldric. Out of scope: CH as an exposure for cancer risk, which is [[ch-cancer-risk-analysis|CH Cancer Risk Analysis]] led by [[lucas-brandt|Lucas Brandt]]. Both projects use the same CH caller, which started here, and the Northvale calls frozen for that project ([[ch-subcohort-variant-calls]]) feed this filter's panel of normals; the [[clonal-hematopoiesis]] Concept explains why the same calls are noise here and exposure there.

## Working Context

Three evidence lines decide whether a cfDNA variant is CH: presence in matched buffy coat, presence or gene-level recurrence in the panel of normals, and variant features (gene, VAF stability across time points, fragment length of supporting reads). Published work points the same way: large paired plasma and buffy coat series show that CH variants are common in clinically reportable genes ([[magee-2025-cfdna-variants-tumour-or-ch-origin]]), and plasma-only classifiers using fragment features can approximate a buffy coat ([[brown-2025-fragmentomic-variant-origin]], [[arango-argoty-2025-metach-cfdna-ch-variants]]). We have not yet tested either approach on our data.

The [[panel-of-normals]] approach is cheap but biased towards common hotspots. The pilot misses were mainly private DNMT3A variants below 1% VAF, which matter because our MRD calls often sit in the same VAF range ([[what-vaf-threshold-defines-a-positive-mrd-call]]).

## Decisions So Far

- 2025-11-05: pilot of 60 matched patients rather than sequencing all 212 or none ([[ch-filter-design-meeting-2025-11-05]]).
- Tumour-informed variants override the filter, even when found in buffy coat.
- KRAS added as "check only" in 2026-02; flagged, not removed ([[ch-filter-gene-list]]).
- The filter's threshold (0.5% in buffy coat) is deliberately lower than the cohort analysis's CH definition, because here the costly error is a false recurrence call ([[clonal-hematopoiesis]]).

## Next Actions

- [ ] Re-run the St Aldric MRD calls with the filter in both modes for the revision.
- [ ] Estimate how many recurrence calls change if the 152 unmatched patients get buffy coat sequencing, using the pilot as a model.
- [ ] Test a fragment-length feature for variant origin on the pilot, following the published plasma-only approaches.
- [ ] Bring a costed recommendation on buffy coat sequencing to the November MRD study meeting.

## Open Questions

- [[do-we-still-need-matched-buffy-coat-sequencing]]
- [[how-large-must-the-ch-panel-of-normals-be]]
- [[what-vaf-threshold-defines-a-positive-mrd-call]]

## Important Notes

- [[clonal-hematopoiesis]]
- [[ch-filter-gene-list]]
- [[ch-filter-design-meeting-2025-11-05]]
- [[matched-normal-sequencing-is-cheaper-than-false-recurrence]]

## Maintenance Log

- 2026-07-14: CH handling becomes a reviewer requirement.
- 2026-01-28: Buffy coat pilot results on 60 patients.
- 2025-11-05: Design meeting chooses a 60-patient matched pilot plus a panel of normals.
- 2025-06-02: Project started with Hannah.
