---
type: Project
status: Active
start: 2025-02-03
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[molecular-epidemiology]]"
  - "[[cancer-early-detection]]"
  - "[[mei-lin-zhou]]"
has:
  - "[[case-control-sample-selection]]"
  - "[[lead-time-analysis]]"
  - "[[registry-linkage-update]]"
  - "[[northvale-health-cohort]]"
  - "[[northvale-statistical-analysis-plan]]"
_organized: true
---

# Northvale Early Detection Study

A nested case-control study inside the [[northvale-health-cohort|Northvale Health Cohort]] that asks how many years before clinical diagnosis cfDNA methylation signals of pancreatic and colorectal cancer can be seen in stored baseline plasma. It is the group's main molecular epidemiology study and the bridge between the cfDNA work of [[pancreatic-cfdna-mrd-study]] and population data.

## Outcome

A peer-reviewed estimate of the methylation signal by time-to-diagnosis window in 410 incident cases (174 pancreatic, 236 colorectal) and 820 matched controls, with sensitivity analyses for reverse causation and sample storage time, and an updated follow-up through 2025.

## Current State

- Sample selection is closed: 410 cases and 820 controls selected by [[incidence-density-sampling]], all plasma aliquots retrieved from the [[corvane-biobank]] and assayed with the 1,840-region panel from [[methylation-panel-design]]. See [[case-control-sample-selection]].
- The [[lead-time-analysis]] runs under [[northvale-statistical-analysis-plan|SAP v1.0]] (signed 2026-02-26) and [[northvale-sap-amendment-1|Amendment 1]]. The main model now excludes cases diagnosed in the first year after blood draw and reports every window separately, following the [[northvale-analysis-meeting-2026-06-24|2026-06-24 decision]].
- Interim results: the signal is concentrated in the 58 cases diagnosed within two years of blood draw; beyond five years it is indistinguishable from controls. Summary in [[northvale-interim-results-2026-10]].
- The [[registry-linkage-update]] received the 2025 extract on 2026-09-08 under the institute [[registry-linkage-agreement]]. Three controls were replaced after late registrations; analyses are being re-run.
- [[mei-lin-zhou]] (cohort PI) still prefers a 6-month exclusion. Her preferred model is reported as a named sensitivity analysis, not as the main result.

## Scope and Boundaries

In scope: case and control definition, sample logistics with the biobank, methylation scoring, conditional logistic models, registry follow-up for the nested set, and the lead-time paper.

Out of scope: assay development (owned by [[methylation-panel-design]], now completed), the [[ch-cancer-risk-analysis]] (a separate project on the same cohort, which shares the registry extract and some codebooks), and any claim about screening performance. Individual-level cohort data never leave governed storage on [[halyard-cluster]]; the vault holds pointers only. The [[northvale-collaboration-agreement]] gives the cohort PI co-authorship and sign-off on any outward communication.

## Working Context

The design question was settled early: a [[nested-case-control-design]] with two controls per case, matched on age at blood draw, sex, recruitment centre and blood-draw date (within three months). Matching on draw date was the expensive choice and the right one, because it balances freezer storage time within each matched set ([[matching-on-blood-draw-date-is-worth-the-cost]]). The analysis is a [[conditional-logistic-regression]] of a per-sample methylation score, with time from blood draw to diagnosis split into [[time-to-diagnosis-windows]] (0 to 1, 1 to 2, 2 to 5 and more than 5 years).

The dominant interpretive risk is [[reverse-causation-in-prediagnostic-studies|reverse causation]]: a signal in samples drawn shortly before diagnosis may be tumour DNA from an already present cancer rather than an early marker. The group's answer is in [[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]]. Storage time is the second risk; see [[does-storage-time-confound-the-northvale-methylation-signal]].

## Active Workflows

- Sample requests to the biobank follow [[requesting-northvale-samples]].
- Monthly Northvale analysis meetings, chaired by [[maja-kovac]], with Mei-Lin and, for registry items, [[daniel-asante]].
- Code in [[northvale-lead-time-code-repository]]; processed data in [[northvale-methylation-data-release-v1]].

## Next Actions

- [ ] Re-run the main and window models on the corrected control set from [[northvale-control-replacement-log]] and confirm the interim estimates hold.
- [ ] Finish the storage-time sensitivity analysis and close or narrow [[does-storage-time-confound-the-northvale-methylation-signal]].
- [ ] Decide with Mei-Lin whether the 97 new pancreatic and colorectal cases from the 2025 extract justify a second case set or a separate validation paper.
- [ ] Draft the lead-time manuscript; target a first full draft before the end of 2026.
- [ ] Present the windowed results at [[tumour-evolution-symposium-2026]] using [[northvale-lead-time-symposium-abstract]].

## Open Questions

- [[does-storage-time-confound-the-northvale-methylation-signal]]
- [[can-ch-explain-part-of-the-northvale-methylation-signal]]
- [[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]] (answered; kept as the decision anchor)

## Important Notes

- [[northvale-statistical-analysis-plan]]
- [[northvale-analysis-meeting-2026-06-24]]
- [[northvale-interim-results-2026-10]]
- [[northvale-roles-and-authorship]]
- [[report-lead-time-windows-not-pooled-estimates]]

## Do Not Do Yet

> [!danger]
> Do not describe any Northvale result as evidence of screening performance or quote a detection rate outside the group until the corrected re-run is done and Mei-Lin has signed off under the collaboration agreement.

## Maintenance Log

- 2026-10-14: Analysis meeting agreed to re-run all models on the corrected control set and to scope a second case set separately.
- 2026-09-08: 2025 registry extract received; three controls replaced, four case diagnosis dates corrected.
- 2026-06-24: Reverse-causation decision: exclude year 1 from the main model, report all windows; Mei-Lin's 6-month preference recorded as dissent.
- 2026-02-26: SAP v1.0 signed; [[lead-time-analysis]] opened on 2026-03-02.
- 2025-10-17: Sample selection and retrieval completed.
