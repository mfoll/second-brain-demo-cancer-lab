---
type: Concept
_organized: true
---

# Tumour Fraction

The proportion of cell-free DNA in a plasma sample that comes from tumour cells, as opposed to the background shed mostly by blood cells. It is the single quantity that most limits what any cfDNA assay can see.

## Why It Matters

Every signal layer has a floor. Tumour-informed variant tracking can reach very low fractions because it integrates many known variants. Methylation and fragmentomics are genome-wide and degrade more gracefully, but they lose specificity as the fraction falls. After curative surgery, tumour fraction is often far below 1%, which is why minimal residual disease detection is hard and why combining layers helps.

## How It Is Estimated

- From variant allele frequencies of tumour-specific mutations, corrected for copy number and clonality.
- From copy-number profiles in shallow whole-genome sequencing, for example with ichorCNA-style methods, which work only above a few percent.
- From methylation deconvolution against reference tissue profiles.

## Pitfalls

- Clonal hematopoiesis variants can look like tumour variants and inflate the estimate.
- Pre-analytical factors such as delayed processing release extra leukocyte DNA and dilute the tumour fraction.
- Estimates from different methods are not interchangeable and should be reported with the method named.
