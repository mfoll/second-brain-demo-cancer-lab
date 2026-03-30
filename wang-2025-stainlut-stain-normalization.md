---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41746-025-02196-8
doi: 10.1038/s41746-025-02196-8
pmid: "41360962"
licence: cc by-nc-nd
date_accessed: 2026-03-16
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[federated-cfdna-learning]]"
  - "[[shafique-2025-histolite-domain-generalization]]"
_organized: true
---

# Self-supervised stain normalization empowers privacy-preserving and model generalization in digital pathology.

Wang J et al., npj Digital Medicine, 2025.

## Summary

StainLUT is a self-supervised stain normalisation model that exploits structural similarity between tissue of the same disease across centres, so a model trained at one centre can be applied elsewhere without moving data between centres. Single-centre models with StainLUT performed comparably to models trained on pooled or same-centre data for slide-level tumour localisation and patch classification.

## Why It Matters

Filed for the stain problem in our archival slides, but Ines also forwarded it to [[arjun-mehta]] for the [[federated-cfdna-learning]] idea: it is an example of normalising inputs locally so that models travel and data does not. The analogy for cfDNA would be per-site fragment-length normalisation.

## Caveats

Assumes tissue of the same disease type looks structurally alike across centres; metastases after chemotherapy may break that.

## Source Links

- [Self-supervised stain normalization in digital pathology](https://doi.org/10.1038/s41746-025-02196-8)
