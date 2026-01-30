---
type: Source
source_type: Scientific paper
url: https://doi.org/10.3389/fpubh.2018.00057
doi: 10.3389/fpubh.2018.00057
pmid: "29552553"
licence: cc by
date_accessed: 2026-01-14
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[conditional-logistic-regression]]"
  - "[[northvale-statistical-analysis-plan]]"
_organized: true
---

# Unconditional or Conditional Logistic Regression Model for Age-Matched Case-Control Data?

## Summary

A simulation study comparing unconditional and conditional logistic regression for case-control data matched loosely on a few demographic variables. Unconditional models can be more precise in that setting, but the conditional model is more robust when matching distorts the comparison between cases and controls.

## Why It Matters

[[lucas-brandt]] raised it during SAP drafting: why not unconditional logistic regression adjusted for matching factors, which would be more precise? Maja's answer, recorded in the [[northvale-statistical-analysis-plan]], is that Northvale matching is not loose: blood-draw date within three months is tight, it carries storage time, and the conditional model is the robust choice. An unconditional model adjusted for matching factors is a listed sensitivity analysis.

## Caveats

Simulations matched on age only.

## Source Links

- [Unconditional or Conditional Logistic Regression Model for Age-Matched Case-Control Data?](https://doi.org/10.3389/fpubh.2018.00057)
