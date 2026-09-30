---
type: Concept
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[ay-2026-privacy-enhancing-technologies-biomedical-ai]]"
  - "[[pseudonymisation-vs-anonymisation]]"
_organized: true
---

# Federated Learning

Training or evaluating a model across several data holders without pooling the data: each site computes on its own data, and only model updates, parameters or aggregate results are exchanged and combined. Swarm learning is a variant without a central coordinator.

## Two Uses To Keep Apart

- Federated evaluation: a fixed, locked model is sent to each site, run locally, and only performance summaries return. Simple, cheap, and close to an ordinary external validation, except that per-patient predictions stay at the sites.
- Federated training: model updates travel back and forth over many rounds. Needs common features, identical code at each site, and an aggregation strategy; much harder to debug.

## What It Does Not Do

It is not a privacy guarantee by itself. Model updates can leak information about training data, which is why secure aggregation or differential privacy are often added, at a cost in accuracy or compute ([[ay-2026-privacy-enhancing-technologies-biomedical-ai]]). Whether updates or aggregate metrics are personal data is a legal question per institution; at Corvane see [[is-fragment-level-cfdna-data-personal-data]] and [[pseudonymisation-vs-anonymisation]].

## Where We Use It

The [[federated-cfdna-learning]] idea for Halo, and as a fallback route for the external validation of the [[mrd-manuscript]] ([[should-halo-validation-run-federated-instead-of-transfer]]). Tooling: [[flower-federated-learning-framework]], [[featurecloud-platform]].
