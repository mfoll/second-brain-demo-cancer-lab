---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1016/j.crmeth.2024.100877
doi: 10.1016/j.crmeth.2024.100877
pmid: "39406232"
licence: cc by-nc-nd
date_accessed: 2025-11-04
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[fragment-length-and-end-motif-features]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# Cell-free DNA end characteristics enable accurate and sensitive cancer diagnosis

Ju J et al., Cell Reports Methods, 2024.

## Summary

Compares cfDNA fragment ends with nucleosome positions in blood cells. Molecules whose ends fall inside nucleosomes are shorter and have altered end-motif patterns, so selecting them enriches tumour-derived DNA. Three end-based metrics built on this selection differed in cancer patients, and machine-learning models combining them reached an overall AUC around 0.95 with 85% sensitivity at 95% specificity.

## Why It Matters

Read by Sofia in 2025-11. It gave a mechanistic reason to treat end motifs as a feature family distinct from length, rather than a by-product of it. That framing was what Dmitri relied on at the [[classifier-design-review-2026-04-02|2026-04-02 review]] when he suggested motif features might escape the length batch effect ([[fragment-length-and-end-motif-features]]).

## Caveats

Diagnostic setting with mostly untreated cancers; post-operative MRD has far lower tumour fractions. The performance figures do not transfer.

## Source Links

- [DOI 10.1016/j.crmeth.2024.100877](https://doi.org/10.1016/j.crmeth.2024.100877), PMID 39406232
