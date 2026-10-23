---
type: Source
source_type: Scientific paper
url: https://doi.org/10.3389/fdgth.2026.1726771
doi: 10.3389/fdgth.2026.1726771
pmid: "42676525"
licence: cc by
date_accessed: 2026-10-05
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[federated-learning]]"
  - "[[arjun-mehta]]"
  - "[[is-fragment-level-cfdna-data-personal-data]]"
_organized: true
---

# Safeguarding biomedical AI: a critical scoping review of privacy-enhancing technologies, hybrid approaches, and deployment models.

Ay S, Topaloglu U, Zhang W. Frontiers in Digital Health, 2026.

## Summary

A scoping review of 87 studies on privacy-enhancing technologies in biomedical AI, covering differential privacy, federated learning, secure multiparty computation, homomorphic encryption and hybrids, across clinical decision support, genomics and imaging. Each family has a characteristic trade-off: differential privacy gives provable guarantees but hurts performance on imbalanced data; federated learning improves access to data but remains exposed to gradient leakage; cryptographic methods protect confidentiality at a high computational cost.

## Why It Matters

[[arjun-mehta]] circulated it to the WP4 list after the [[halo-steering-committee-2026-09-17]]. It is our main reference for the privacy section of the [[federated-cfdna-learning-concept-note]]: federated training alone is not a privacy guarantee, which is relevant to [[victor-lindahl]]'s question of whether model updates leaving Corvane count as personal data. Our recurrence outcome is imbalanced (about a third positive), so the differential-privacy cost is a real concern.

## Caveats

A review of methods literature, mostly not cfDNA. Its appraisal of deployment realism is the most useful part for us; specific numbers from included studies were not checked.

## Source Links

- [Ay et al. 2026, Frontiers in Digital Health](https://doi.org/10.3389/fdgth.2026.1726771)
