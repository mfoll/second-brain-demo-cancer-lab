---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41598-025-20411-0
doi: 10.1038/s41598-025-20411-0
pmid: "41120464"
licence: cc by-nc-nd
date_accessed: 2026-03-12
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[halyard-cluster]]"
_organized: true
---

# Lightweight self supervised learning framework for domain generalization in histopathology.

Shafique A et al., Scientific Reports, 2025.

## Summary

HistoLite is a lightweight self-supervised framework built on customisable autoencoders, meant to learn domain-invariant features without the compute that large foundation models need. It was benchmarked against state-of-the-art foundation models on breast slides, using a dataset of the same tissue scanned on two different scanners.

## Why It Matters

Two points for us. The same-slide, two-scanner design is the cleanest way to measure scanner effects, and our archival slides come from two hospitals with different scanners; [[amara-okonkwo]] wants to copy the design on ten atlas slides. And it is a reminder that we may not need the largest models, which matters while GPU time on [[halyard-cluster]] is shared.

## Caveats

Breast tissue only; small model trades accuracy for cost, and the abstract does not tell us how much.

## Source Links

- [Lightweight self supervised learning framework for domain generalization in histopathology](https://doi.org/10.1038/s41598-025-20411-0)
