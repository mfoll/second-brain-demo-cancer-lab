---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1016/j.crmeth.2024.100793
doi: 10.1016/j.crmeth.2024.100793
pmid: "38866008"
licence: cc by-nc-nd
date_accessed: 2026-01-13
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[batch-confounding-in-cfdna-studies]]"
  - "[[does-the-stacked-classifier-generalise-across-extraction-batches]]"
  - "[[arjun-mehta]]"
_organized: true
---

# Systematic biases in reference-based plasma cell-free DNA fragmentomic profiling

Liu X et al., Cell Reports Methods, 2024.

## Summary

Profiling the same cfDNA datasets against different reference genomes revealed systematic, sample-dependent biases in fragmentomic features, varying with ancestry, which could hurt diagnostic assays across clinical centres. The authors propose a reference-free approach (Freefly) that runs much faster and gives consistent features usable for cancer diagnosis.

## Why It Matters

[[arjun-mehta|Arjun Mehta]] flagged it at a Halo modelling call in 2026-01. For us it means the reference genome and aligner are part of the model, and Halo sites must run our container rather than their own feature code if the [[fragmentomics-classifier|classifier]] is to be validated there ([[does-the-stacked-classifier-generalise-across-extraction-batches]]). Cited in [[external-validation-before-locking-a-classifier]].

## Caveats

We have not tested reference-free features; switching now would mean retraining before validation.

## Source Links

- [DOI 10.1016/j.crmeth.2024.100793](https://doi.org/10.1016/j.crmeth.2024.100793), PMID 38866008
