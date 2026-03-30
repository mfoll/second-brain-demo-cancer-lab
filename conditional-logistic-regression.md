---
type: Concept
maturity: Evergreen
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[nested-case-control-design]]"
  - "[[kuo-2018-conditional-vs-unconditional-logistic-regression]]"
_organized: true
---

# Conditional Logistic Regression

Logistic regression that conditions on the matched set: each set contributes only through comparisons between its case and its controls, so factors constant within a set (the matching factors, and anything they carry such as storage time) drop out of the likelihood. In a risk-set-sampled design it is equivalent to the Cox partial likelihood restricted to the sampled risk sets.

## Why we use it

In the [[lead-time-analysis]] the matched sets are tight (blood-draw date within three months), so the conditional model removes storage time, season and centre effects without modelling them. It also handles plate effects, because whole matched sets were run on the same plate ([[northvale-sample-shipment-2025-09-23]]).

## Limits

- Matching factors cannot be studied as exposures.
- Sets where case and controls share the same exposure value contribute nothing.
- Interactions with time to diagnosis are expressed through each set's window, since controls inherit their case's window ([[time-to-diagnosis-windows]]).

## Alternatives

An unconditional model adjusted for matching factors can be more precise with loose matching ([[kuo-2018-conditional-vs-unconditional-logistic-regression]]); it is a Northvale sensitivity analysis. Penalised versions exist for many covariates ([[djordjilovic-2024-penalizedclr]]).
