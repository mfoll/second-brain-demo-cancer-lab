---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1101/2025.10.02.25337106
doi: 10.1101/2025.10.02.25337106
licence: cc by-nc-nd
date_accessed: 2026-09-22
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[federated-learning]]"
  - "[[can-federated-training-match-a-pooled-classifier]]"
_organized: true
---

# Decentralized, privacy-preserving surgical video analysis with Swarm Learning

Saldanha OL, Pfeiffer K, Bodenstedt S, et al. medRxiv preprint, 2025.

## Summary

A pipeline combining weakly supervised deep learning with Swarm Learning, a decentralised training approach without a central server, applied to 397 laparoscopic appendectomy videos from six surgical centres. On three patient-level staging tasks, Swarm Learning beat single-centre training and performed comparably to centralised training, with stable results on external validation. A survey of the centres named hardware failures and poor integration with local infrastructure as the main practical barriers.

## Why It Matters

The closest example we found of six centres, each with its own data rules, training jointly and matching a pooled model. [[arjun-mehta]] cited it at the [[halo-steering-committee-2026-09-17]]. The practical barriers in the survey are exactly the ones Ines expects at Halo sites, so the concept note budgets engineering time for them.

## Caveats

Preprint, not peer reviewed. Video data with hundreds of patients per task; our patient tier has 60 patients, so the result does not tell us federated training will work at our scale ([[can-federated-training-match-a-pooled-classifier]]).

## Source Links

- [Saldanha et al. 2025, medRxiv](https://doi.org/10.1101/2025.10.02.25337106)
