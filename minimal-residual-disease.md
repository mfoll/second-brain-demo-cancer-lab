---
type: Topic
related_to:
  - "[[pancreatic-cfdna-mrd-study]]"
  - "[[cfdna-fragmentomics]]"
  - "[[tumour-evolution]]"
_organized: true
---

# Minimal Residual Disease

Retrieval surface for detecting cancer that remains after curative-intent treatment, mainly through circulating tumour DNA. In this vault it centres on the [[pancreatic-cfdna-mrd-study|Pancreatic cfDNA MRD Study]] and the [[mrd-review-article|MRD Review Article]].

## Scope

This Topic gathers the group's notes on post-treatment detection: the assays (tumour-informed variants, methylation, fragmentomics), the confounders (clonal hematopoiesis, pre-analytical batch effects, sequencing errors at very low allele fractions), and how results are validated and reported. Pre-diagnostic detection in healthy people belongs to [[cancer-early-detection]] and the [[northvale-early-detection-study|Northvale Early Detection Study]], although the technical problems overlap.

## Our Working View

Post-operative MRD in pancreatic cancer is mostly a problem of very low tumour fraction in small extracts: median 14 ng of cfDNA, often below 0.1% tumour fraction. Assay sensitivity is limited by input before it is limited by chemistry ([[limit-of-detection-in-cfdna-assays]]). The main sources of false positives are biological (clonal hematopoiesis) rather than technical once duplex consensus is used. And the main source of overoptimistic results is evaluation design: single-centre development, unlocked models and lead times measured against scheduled imaging ([[external-validation-before-locking-a-classifier]], [[molecular-lead-time]]).

## Start Here

- [[tumour-informed-vs-tumour-naive-mrd]]: the two assay designs and what each costs.
- [[molecular-lead-time]]: how we define and censor lead time over imaging.
- [[clonal-hematopoiesis]]: the main source of false-positive MRD calls.
- [[limit-of-detection-in-cfdna-assays]]: what our 0.1% figure means and does not mean.

## People

[[dmitri-halvorsen|Dmitri Halvorsen]] (assays and calling), [[sofia-reyes-calderon|Sofia Reyes Calderon]] (fragmentomics), [[hannah-lindqvist|Hannah Lindqvist]] (clonal hematopoiesis), [[samuel-okoye|Samuel Okoye]] (clinical lead).

## Open Threads

- [[what-lead-time-over-imaging-is-clinically-meaningful]]
- [[what-vaf-threshold-defines-a-positive-mrd-call]]
- [[can-halo-samples-serve-as-external-validation]]

## Papers

- Pancreatic MRD: [[botta-2024-tumour-informed-ctdna-pdac]], [[maulat-2024-portal-peripheral-ctdna-pdac]], [[theocharopoulos-2025-mrd-pdac-perioperative]], [[ojha-2025-ctdna-pancreatic-critical-appraisal]].
- Tumour-naive designs: [[nguyen-2025-tumour-naive-multimodal-mrd]].
- CH confounding: [[spoor-2021-false-positive-ctdna-ch]], [[magee-2025-cfdna-variants-tumour-or-ch-origin]].
- Low-VAF calling: [[carrie-2025-benchmarking-ctdna-mutation-calling]], [[maruzani-2024-umi-aware-variant-callers]].

## Related Topics

[[cfdna-fragmentomics]], [[cancer-early-detection]], [[tumour-evolution]].
