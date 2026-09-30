---
type: Source
source_type: Web page
url: https://flower.ai/
date_accessed: 2026-09-24
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[arjun-mehta]]"
  - "[[federated-learning]]"
_organized: true
---

# Flower Federated Learning Framework

Web page and documentation of Flower, an open-source Python framework for federated learning that works with common machine-learning libraries. [[arjun-mehta]] has used it at Westmere and proposes it for the Halo pilot.

## Why It Matters

Flower is code-first, which suits a pipeline group better than a web interface: the client is a Python process we could run inside our own Apptainer image on [[halyard-cluster]]. It supports custom aggregation strategies, which we would need for the stacked logistic plus boosting model, and simulation mode, which lets us test the whole set-up on Corvane data split into pseudo-sites before involving anyone else.

## Caveats

Flexibility means more of our own code to audit. Secure aggregation and differential privacy are available but not on by default; using them is a design decision for the concept note ([[federated-cfdna-learning-concept-note]]).

## Source Links

- [Flower](https://flower.ai/)
