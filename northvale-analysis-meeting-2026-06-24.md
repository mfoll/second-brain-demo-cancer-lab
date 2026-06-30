---
type: Event
date: 2026-06-24
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]]"
  - "[[reverse-causation-in-prediagnostic-studies]]"
  - "[[mei-lin-zhou]]"
  - "[[maja-kovac]]"
_organized: true
---

# Northvale Analysis Meeting 2026-06-24

The meeting where the group decided how the [[lead-time-analysis]] handles reverse causation. Present: Ines, [[maja-kovac]] (chair), [[mei-lin-zhou]] (video), [[lucas-brandt]], [[dmitri-halvorsen]] for the assay side. Slides: [[northvale-lead-time-slides-2026-06-24]].

## At a Glance

> [!note]
> Decision: the main model excludes cases diagnosed less than one year after blood draw, and every time-to-diagnosis window (0 to 1, 1 to 2, 2 to 5, more than 5 years) is reported separately with its own estimate. Mei-Lin Zhou dissented and prefers a 6-month exclusion; her model is reported as a named sensitivity analysis.

## Context

The first window results ([[northvale-analysis-meeting-2026-04-22]]) showed most of the methylation signal sits in the 58 cases diagnosed within two years of blood draw. A pooled odds ratio of 1.48 per standard deviation would have been driven by those cases. The [[northvale-statistical-analysis-plan|SAP]] prespecified windows but left the main-model exclusion to be decided after a blinded look at the distribution of time to diagnosis, which Maja had done in May.

## Discussion

Maja presented three options with estimates:

1. No exclusion, pooled estimate: 1.48 (1.27 to 1.72). Rejected: the number would be read as a long-range early-detection effect when it is mostly cases already near diagnosis.
2. Exclude the first 6 months (11 cases): 1.33 (1.14 to 1.55). Mei-Lin's preference.
3. Exclude the first year (27 cases): 1.24 (1.06 to 1.45). Maja's proposal.

Mei-Lin argued that pancreatic cancer moves fast, that a 1-year exclusion discards cases that are informative about lead time, and that the windows already show the gradient so the exclusion matters less. Maja argued that the main estimate should be the one least contaminated by prevalent but undiagnosed disease, that 1 year is a common convention in comparable cohort analyses (she pointed to [[rossides-2020-reverse-causation-nested-case-control]] for treating the period before diagnosis as an explicit bias window), and that 6 months would leave the main model sensitive to diagnostic delay in colorectal cancer. Dmitri noted that in the MRD work tumour fraction rises steeply in the months before radiological recurrence, which fits Maja's concern.

Ines summarised: the windowed results are the real finding; the main model is a single headline and should be conservative.

## Decisions

- Main model: exclude cases with less than one year from blood draw to diagnosis, and their matched controls.
- Report all four windows with estimates and case counts in the main results table, not the supplement ([[report-lead-time-windows-not-pooled-estimates]]).
- Report the 6-month exclusion and the no-exclusion model as named sensitivity analyses.
- Record Mei-Lin's dissent in the minutes and in the paper's methods discussion.
- Maja writes an SAP amendment before re-running anything. Done as [[northvale-sap-amendment-1]] on 2026-06-30.

## Actions

- [x] Maja: SAP amendment (done 2026-06-30).
- [x] Maja: re-run with the new main model (done 2026-07-17).
- [ ] Lucas: check whether CH status explains any of the early-window signal ([[can-ch-explain-part-of-the-northvale-methylation-signal]]).

## Follow-up

The answer is recorded in [[how-do-we-handle-reverse-causation-in-the-northvale-lead-time-analysis]]. The concept is in [[reverse-causation-in-prediagnostic-studies]].
