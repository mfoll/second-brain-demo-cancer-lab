---
type: Project
status: Active
start: 2026-02-01
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
has:
  - "[[mrd-manuscript-decision-2026-07-14]]"
  - "[[mrd-revision-response-plan]]"
  - "[[mrd-reviewer-comments-2026-07]]"
  - "[[mrd-preprint-2026]]"
related_to:
  - "[[clara-hoffmann]]"
  - "[[halo-cross-site-benchmark]]"
  - "[[data-access-policy-revision]]"
  - "[[minimal-residual-disease]]"
_organized: true
---

# MRD Manuscript

The main paper of the [[pancreatic-cfdna-mrd-study|Pancreatic cfDNA MRD Study]]: serial post-operative cfDNA in 212 St Aldric patients detects recurrence a median 4.3 months before imaging. Submitted to Tumour Evolution Reports on 2026-02-27, now in major revision.

## Outcome

Paper accepted in Tumour Evolution Reports. The revision must answer three reviewers, one of whom requires external validation.

## Current State

- Major revision received on 2026-07-14 from handling editor [[clara-hoffmann|Clara Hoffmann]] ([[mrd-manuscript-decision-2026-07-14]]). Deadline extended on 2026-10-07 to 2027-01-29 ([[mrd-revision-extension-2026-10-07]]).
- **Blocked on external validation.** Reviewer 2 asks for validation on an independent cohort. The only realistic source is Halo post-resection samples from the [[halo-cross-site-benchmark|Halo Cross-Site Benchmark]] and its [[halo-truth-set]]. Moving those data to Corvane needs the consortium transfer clause of the [[data-access-policy-revision|Data Access Policy Revision]]; the board discussed it on 2026-09-10 and did not adopt it ([[data-governance-board-2026-09-10]]).
- Reviewer 1 (CH handling) and Reviewer 3 (interval censoring of lead time) can be answered with St Aldric data; work is under way in [[mrd-revision-response-plan]].
- The revision will report the stacked classifier, not the gradient-boosting model in the submitted version ([[classifier-design-review-2026-04-02]]).
- The preprint ([[mrd-preprint-2026]]) is public and will be updated with the revision.

## Scope and Boundaries

Writing, analyses requested by reviewers, submission logistics and the preprint. New method development stays in [[fragmentomics-classifier]] and [[clonal-hematopoiesis-filter]]. Ines is corresponding author; Dmitri and Sofia are joint first authors; Samuel Okoye is senior clinical author.

## Working Context

Two fallbacks were discussed at [[mrd-revision-planning-2026-07-21]] in case the policy is not adopted in time: (1) a federated run in which Halo sites score their own samples with the frozen model and return only aggregate performance, which needs Arjun Mehta's sites to run our container; (2) a temporal split within St Aldric, which Reviewer 2 explicitly said would not be enough. Option 1 overlaps with the [[federated-cfdna-learning|Federated cfDNA Learning]] idea and is the current plan B; the trade-offs are in [[should-halo-validation-run-federated-instead-of-transfer]].

The submitted version's headline used gradient boosting on fragmentomics. Since the [[lab-meeting-2026-03-12|2026-03-12 lab meeting]] showed batch overfitting, the revised numbers will be lower but defensible; we tell the editor this openly in the cover letter rather than burying it.

## Authorship and Roles

- Joint first authors: [[dmitri-halvorsen|Dmitri Halvorsen]] and [[sofia-reyes-calderon|Sofia Reyes Calderon]].
- Co-authors: [[hannah-lindqvist|Hannah Lindqvist]] (CH filter), [[elias-moreau|Elias Moreau]] (wet lab), [[maja-kovac|Maja Kovac]] (statistics), [[samuel-okoye|Samuel Okoye]] (senior clinical author), Ines (corresponding).
- If Halo data are used, site investigators join as co-authors under the consortium publication policy.

## Do Not Do Yet

> [!danger]
> Do not request or open any Halo outcome data before model card v3 is frozen and committed, even if the policy is adopted early.

## What Changes in the Revision

- Fragmentomics layer: stacked classifier from [[classifier-model-card-v2]] (v3 when frozen), evaluated leave-batch-out.
- CH: both filter modes reported, with a sensitivity analysis without the filter.
- Lead time: interval-censored estimate as main result, naive median as secondary; preliminary estimate is shorter than the submitted 4.3 months.
- Clinical data: updated export to 2026-09-30, with the five registry-only recurrences already included ([[registry-recurrence-extract-2026-03]]).
- External validation section, central or federated.

## Next Actions

- [ ] Support the consortium clause at the board of 2026-11-12 (papers due 2026-10-29) with [[ruth-abernathy|Ruth Abernathy]] and Yara Castellanos.
- [ ] Prepare plan B: frozen container for federated scoring, agreed with [[arjun-mehta|Arjun Mehta]].
- [ ] Complete Reviewer 1 and 3 analyses by 2026-11-30.
- [ ] Draft the cover letter explaining the classifier change ([[mrd-response-to-reviewers-draft-2026-10]]).

## Open Questions

- [[can-halo-samples-serve-as-external-validation]]
- [[what-lead-time-over-imaging-is-clinically-meaningful]]
- [[should-we-report-ca19-9-alongside-cfdna]]

## Important Notes

- [[mrd-manuscript-decision-2026-07-14]]
- [[mrd-reviewer-comments-2026-07]]
- [[mrd-revision-response-plan]]
- [[halo-validation-request-2026-08-04]]
- [[mrd-manuscript-submission-2026-02-27]]

## Maintenance Log

- 2026-10-07: Extension to 2027-01-29 granted.
- 2026-08-04: Formal Halo sample request; legal says it needs the revised institute policy.
- 2026-07-21: Revision plan agreed, external validation is the critical path.
- 2026-07-14: Major revision.
- 2026-02-27: Submitted to Tumour Evolution Reports.
