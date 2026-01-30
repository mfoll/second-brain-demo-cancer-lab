---
type: Project
status: Active
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[cfdna-fragmentomics]]"
  - "[[minimal-residual-disease]]"
  - "[[mrd-manuscript]]"
has:
  - "[[halo-truth-set]]"
  - "[[halo-truth-set-design-document]]"
  - "[[halo-interim-benchmark-report-2026-10]]"
  - "[[halo-wp4-analysis-plan]]"
  - "[[halo-data-flow-and-transfer-constraints]]"
_organized: true
---

# Halo Cross-Site Benchmark

Compare the six Halo cfDNA assays on one blinded, shared truth set, so that each site knows its real detection limit and the consortium can say which assay suits which clinical question. It is the main deliverable of Work Package 4, which Ines leads.

## Outcome

A benchmark report and paper that give, for each of the six assays, limit of blank, limit of detection, concordance on contrived samples, and sensitivity and specificity for recurrence on the patient-derived samples, with failure modes reported per site. Done when the consortium paper is submitted.

## Current State

- The [[halo-truth-set]] (40 contrived, 60 patient, 20 healthy-donor samples, six aliquots each) was shipped on 2026-05-19. Five sites returned FASTQ or call files by 2026-09-30; Kelstow's ddPCR results are promised for mid-November.
- Contrived tier: interim results in [[halo-interim-benchmark-report-2026-10]]. All six assays detect 1% VAF; at 0.1% detection ranges from 3 of 4 to 0 of 4 replicates depending on the assay.
- Our fragmentomics assay scores the contrived samples badly because their fragment profile does not look like patient plasma. This is a commutability problem, not an assay failure ([[commutability-of-reference-materials]]).
- Patient tier: blinded, and the unblinding key and clinical follow-up sit at Brightwater. Analysis at Corvane is blocked until the institute policy allows consortium transfer ([[halo-data-flow-and-transfer-constraints]]).
- The truth set is also the planned external validation for the [[mrd-manuscript]], together with about 150 pancreatic patients from two site cohorts ([[halo-validation-request-2026-08-04]]); Reviewer 2 asked for it at the [[mrd-manuscript-decision-2026-07-14]].

## Scope and Boundaries

In scope: analysis plan, harmonised feature and call definitions, statistics, the shared code, the WP4 report. Out of scope: each site's wet-lab work (sites own their assays), and the MRD manuscript's own analysis, which stays in [[mrd-manuscript]]. Sample custody and the unblinding key belong to the coordinating centre ([[ngozi-adeyemi]]).

## Working Context

The design deliberately separates what contrived material can test (analytical sensitivity, LoB, LoD, linearity) from what only patient plasma can test (clinical sensitivity, fragmentomics). The first draft design used contrived material only and was rejected at the [[halo-steering-committee-2025-11-20]]; it is kept as [[halo-truth-set-draft-plan-2025]]. Pre-analytical differences between sites were mapped in [[halo-sop-comparison-preanalytics]] and largely harmonised for the shipment; library and bioinformatics differences are documented, not harmonised ([[halo-sop-comparison-library-prep]], [[halo-sop-comparison-bioinformatics]]).

## Active Workflows

- Monthly WP4 call, analysis code in [[halo-wp4-analysis-code-repository]], run on [[halyard-cluster]].
- Blinding and unblinding follow [[halo-truth-set-blinding-and-unblinding-rules]].

## Next Actions

- [ ] Finish the contrived-tier report with failure modes per site, including Kelstow once data arrive.
- [ ] Prepare the patient-tier analysis so it can run the day transfer is allowed, or run remotely at Brightwater if the federated route is approved.
- [ ] Decide with [[sun-hee-park]] how to report assays that cannot produce a fragmentomics score on contrived samples.
- [ ] Draft the consortium paper outline for the steering committee.

## Open Questions

- [[is-the-halo-patient-tier-large-enough-for-validation]]
- [[are-contrived-reference-materials-commutable-for-fragmentomics]]
- [[should-halo-harmonise-preanalytics-or-correct-statistically]]

## Important Notes

- [[halo-truth-set]]
- [[halo-wp4-analysis-plan]]
- [[halo-interim-benchmark-report-2026-10]]
- [[reference-materials-cannot-replace-patient-plasma]]
- [[benchmarks-must-report-failure-modes]]

## Do Not Do Yet

> [!danger]
> Do not request the unblinding key or any patient-tier clinical data at Corvane until the revised data access policy is adopted; analysing them under the current policy would breach both the consortium agreement and the institute rules.

## Maintenance Log

- 2026-10-08: Interim contrived-tier results discussed; patient tier held ([[halo-wp4-analysis-call-2026-10-08]]).
- 2026-09-17: Steering committee accepts that the patient tier waits for policy.
- 2026-06-12: Annual meeting agrees to report commutability as a finding.
- 2026-05-19: Truth set shipped to all six sites.
- 2026-02-26: Truth set design v2 and harmonised pre-analytics approved.
