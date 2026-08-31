---
type: Note
belongs_to: "[[mrd-review-article]]"
related_to:
  - "[[minimal-residual-disease]]"
  - "[[mrd-review-invitation-2026-07]]"
_organized: true
---

# MRD Review Article Outline

Outline v2, agreed on 2026-09-08 for the [[mrd-review-article|MRD Review Article]] in Computational Oncology Review. About 6,000 words, six figures.

1. **Where the signal comes from** (Dmitri, 1,000 words). Variants, methylation, copy number, fragmentation; how each scales with tumour fraction and input ([[limit-of-detection-in-cfdna-assays]]).
2. **Tumour-informed and tumour-naive designs** (Ines, 1,000 words). Costs, failure modes, tissue availability ([[tumour-informed-vs-tumour-naive-mrd]]).
3. **Clonal hematopoiesis** (Hannah, 1,200 words). Matched normal, panel of normals, plasma-only classifiers ([[clonal-hematopoiesis]]).
4. **Fragmentomics and batch effects** (Sofia with Ines, 1,200 words). Pre-analytical variables, reference bias, model choice ([[batch-confounding-in-cfdna-studies]]).
5. **Validation and reporting** (Ines, 1,200 words). Locking, external validation, lead time and interval censoring ([[external-validation-before-locking-a-classifier]], [[molecular-lead-time]]).
6. **Outlook** (400 words). Federated validation across consortia.

Figure 1: signal layers against tumour fraction. Figure 4: the leave-batch-out gap, using only published or preprint numbers ([[mrd-preprint-2026]]).

Rejected from v1: a section on clinical utility trials, which would duplicate assay-focused reviews; covered in two paragraphs in section 5 instead.
