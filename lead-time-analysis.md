---
type: Project
status: Active
start: 2026-03-02
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[maja-kovac]]"
  - "[[reverse-causation-in-prediagnostic-studies]]"
  - "[[lead-time]]"
has:
  - "[[northvale-statistical-analysis-plan]]"
  - "[[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]]"
  - "[[northvale-analysis-meeting-2026-06-24]]"
  - "[[northvale-window-sensitivity-tables]]"
_organized: true
---

# Lead-Time Analysis

The statistical analysis of the [[northvale-early-detection-study]]: conditional logistic models of the cfDNA methylation score by time from blood draw to diagnosis, with sensitivity analyses for reverse causation and sample storage time. Led by [[maja-kovac]].

## Outcome

Final estimates for each time-to-diagnosis window and for the main model, all sensitivity analyses specified in the SAP and its amendment run on the corrected case-control set, and a results package ready for the manuscript.

## Current State

- The main model follows [[northvale-statistical-analysis-plan|SAP v1.0]] as changed by [[northvale-sap-amendment-1]]: cases diagnosed less than one year after blood draw are excluded from the main estimate; all four windows are reported separately.
- Interim, before the control correction: odds ratio per standard deviation of methylation score 1.48 (95% CI 1.27 to 1.72) with all cases; 1.24 (1.06 to 1.45) excluding year 1; 1.33 (1.14 to 1.55) excluding the first six months. Window estimates in [[northvale-window-sensitivity-tables]].
- [[mei-lin-zhou]] dissents from the 1-year exclusion and prefers 6 months. The decision and dissent are in [[northvale-analysis-meeting-2026-06-24]].
- The re-run on the corrected control set ([[northvale-control-replacement-log]]) started on 2026-10-15.
- Storage-time sensitivity analysis is half done; see [[does-storage-time-confound-the-northvale-methylation-signal]].

## Scope and Boundaries

Covers modelling, sensitivity analyses and results tables. Sample selection is closed ([[case-control-sample-selection]]); follow-up extension is in [[registry-linkage-update]]. Writing the paper will open as its own project once results are frozen.

## Working Context

The model is a [[conditional-logistic-regression]] stratified on matched set, with the methylation score standardised on controls. Smoking status and body-mass index enter as covariates in a secondary model; matching factors are handled by the conditioning. Windows are 0 to 1, 1 to 2, 2 to 5 and more than 5 years ([[time-to-diagnosis-windows]]); each case's controls inherit its window.

The pattern so far is steep: the 27 cases in year 1 and 31 in year 2 carry most of the signal, the 84 cases at 2 to 5 years show a weak excess, and the 268 cases beyond 5 years show none. This is what [[reverse-causation-in-prediagnostic-studies|reverse causation]] would predict and also what a genuine but short [[lead-time]] would predict; the two cannot be separated with this design, which is why the group chose to report windows rather than one pooled number ([[report-lead-time-windows-not-pooled-estimates]]). External results point the same way: [[patel-2026-prediagnostic-methylation-cps3]] found detectability falling sharply with time before diagnosis.

Missing covariates (pack-years missing for 29% of ever-smokers, see [[northvale-smoking-history-derivation]]) are handled with the matched-set multiple imputation approach in [[keogh-2018-multiple-imputation-nested-case-control]].

## Active Workflows

- Code and frozen outputs: [[northvale-lead-time-code-repository]], runs on [[halyard-cluster]].
- Monthly analysis meeting; next on 2026-11-11.

## Next Actions

- [ ] Re-run main, window and sensitivity models on the corrected control set and diff against the interim tables.
- [ ] Finish the storage-time analysis (score versus years in freezer within matched sets, and the genomic DNA contamination flag from [[northvale-storage-time-qc-report]]).
- [ ] Run the cancer-site-specific models (pancreatic, colorectal) prespecified in the SAP.
- [ ] Freeze results and hand a table and figure package to the manuscript draft.

## Open Questions

- [[does-storage-time-confound-the-northvale-methylation-signal]]
- [[can-ch-explain-part-of-the-northvale-methylation-signal]]
- [[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]]

## Important Notes

- [[northvale-statistical-analysis-plan]]
- [[northvale-sap-amendment-1]]
- [[northvale-interim-results-2026-10]]
- [[northvale-date-definitions]]
- [[northvale-lead-time-slides-2026-06-24]]

## Maintenance Log

- 2026-10-15: Re-run on the corrected control set started.
- 2026-06-30: [[northvale-sap-amendment-1]] signed, implementing the 2026-06-24 decision.
- 2026-06-24: Decision to exclude year 1 from the main model and report all windows.
- 2026-04-22: First window results reviewed; signal concentrated within two years.
- 2026-03-02: Project opened after SAP sign-off.
