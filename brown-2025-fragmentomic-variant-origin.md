---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1016/j.jlb.2025.100311
doi: 10.1016/j.jlb.2025.100311
pmid: "40704056"
licence: cc by-nc-nd
date_accessed: 2025-10-13
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[clonal-hematopoiesis]]"
  - "[[cfdna-fragmentomics]]"
  - "[[hannah-lindqvist]]"
_organized: true
---

# Fragmentomic-based algorithm to computationally predict tumor-somatic, germline, and clonal hematopoiesis variant origin in liquid biopsy

Brown DW et al., The Journal of Liquid Biopsy, 2025.

## Summary

Trained and validated a machine-learning algorithm (Variant Origin Prediction) on paired plasma and white-blood-cell sequencing at equal depth, using fragmentomic properties of the reads supporting each variant to assign tumour, germline or CH origin. About two-thirds of liquid biopsies had at least one reportable CH variant. Agreement with white-cell sequencing was high, including for variants at or below 1% VAF and in TP53, and it allowed separate tracking of tumour and CH variants over time in a prostate cancer cohort.

## Why It Matters

The most direct published answer to [[do-we-still-need-matched-buffy-coat-sequencing]]: if fragment features of supporting reads can separate CH from tumour variants, buffy coat sequencing could be limited to ambiguous cases. Hannah plans to test a simple version (supporting-read length distribution) on the pilot.

## Caveats

Vendor assay and metastatic disease; post-operative MRD variants have very few supporting reads, so fragment-based origin calls may be underpowered for us.

## Source Links

- [DOI 10.1016/j.jlb.2025.100311](https://doi.org/10.1016/j.jlb.2025.100311), PMID 40704056
