---
type: Opinion
status: Active
confidence: Medium
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[federated-cfdna-learning]]"
  - "[[should-halo-validation-run-federated-instead-of-transfer]]"
  - "[[carinci-2026-federated-analytics-ncd-surveillance]]"
_organized: true
---

# Federated Analysis Is Not A Substitute For A Transfer Clause

## Stance

> [!info]
> Federated analysis is a good tool for training and for estimates that sites can compute locally, but an institute that only allows federated use has not solved data sharing; it has postponed it. The consortium transfer clause should be adopted on its own merits, and federated methods offered alongside it, not instead of it.

## Scope

Applies to the institute data access policy and to validation of locked clinical models across consortium sites. It does not apply to exploratory model training across Halo, where federated learning may well be the better default ([[federated-cfdna-learning]]).

## Why I Think This

- Validation that a journal will audit needs per-patient predictions, calibration and identical preprocessing. Remote runs can deliver this, but checking five remote environments is slower and harder to defend than one controlled environment.
- Federated set-ups still move personal information: per-patient predictions and model updates. [[victor-lindahl]] made this point himself. The governance work does not go away.
- The policy problem predates Halo: seven consortium requests in 2025 became bilateral agreements with a median 97 days to data release ([[data-request-statistics-2025]]). Federated methods would have helped few of them.
- The review literature ([[carinci-2026-federated-analytics-ncd-surveillance]]) is strongest on indicators and distributed regression, not on diagnostic validation.

## What Would Change My Mind

- If [[clara-hoffmann]] or the reviewers accept federated metrics as external validation without per-patient data.
- If two or more Halo sites cannot legally receive data in any case, making a pooled environment unrealistic.
- If the November board adopts the clause in a form so restrictive that federated runs are faster in practice.

## Implications

Keep transfer as the plan for the [[mrd-manuscript]]; ask [[dmitri-halvorsen]] to prepare the federated metrics-only fallback anyway; argue for both routes in draft 4 of the policy.
