---
type: Question
status: Answered
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[northvale-analysis-meeting-2026-06-24]]"
  - "[[reverse-causation-in-prediagnostic-studies]]"
  - "[[mei-lin-zhou]]"
_organized: true
---

# How do we handle reverse causation in the Northvale lead-time analysis?

## Question

Most of the methylation signal in the [[northvale-early-detection-study]] comes from the 58 cases diagnosed within two years of blood draw. Those samples may contain DNA from cancers already present. How should the main analysis and the paper deal with this?

## Current Answer

> [!info]
> Decided on 2026-06-24: the main model excludes cases diagnosed less than one year after blood draw (and their matched controls), and all four time-to-diagnosis windows are reported separately in the main results table. The 6-month exclusion preferred by Mei-Lin Zhou and the no-exclusion model are named sensitivity analyses.

Implemented in [[northvale-sap-amendment-1]] (2026-06-30). Interim estimates per SD of score: main model 1.24 (1.06 to 1.45); 6-month exclusion 1.33 (1.14 to 1.55); no exclusion 1.48 (1.27 to 1.72). Window estimates in [[northvale-window-sensitivity-tables]].

## Why this answer

- The windows are the finding; the main model is a single conservative headline ([[report-lead-time-windows-not-pooled-estimates]]).
- A 1-year exclusion is a common convention and leaves the main estimate least affected by prevalent undiagnosed disease.
- The design has one sample per person, so short [[lead-time]] and reverse causation cannot be separated; reporting windows lets readers see the gradient instead of a blended number.

## Dissent

[[mei-lin-zhou]] prefers 6 months: pancreatic cancer progresses fast, a year discards informative cases, and the windows already show the gradient. Her view is recorded in the minutes and the amendment, and will be discussed in the paper.

## Rejected options

- No exclusion with a pooled estimate: would be read as a long-range effect.
- 2-year exclusion: leaves only 352 cases and removes the window where the signal is.
- Modelling time to diagnosis continuously ([[massi-2022-deep-survival-ewas-time-to-diagnosis]]): too few cases for the matched design.

## Revisit if

The corrected re-run changes the window pattern, or a repeat-sample substudy becomes possible.

## Links

- [[northvale-analysis-meeting-2026-06-24]]
- [[reverse-causation-in-prediagnostic-studies]]
- [[safizadeh-2026-inflammation-colorectal-reverse-causality]]
