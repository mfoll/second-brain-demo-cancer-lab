---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-025-67842-x
doi: 10.1038/s41467-025-67842-x
pmid: "41407694"
licence: cc by-nc-nd
date_accessed: 2026-02-02
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[can-in-silico-dilutions-replace-a-physical-truth-set]]"
  - "[[halo-truth-set]]"
  - "[[minimal-residual-disease]]"
_organized: true
---

# Comprehensive benchmarking of methods for mutation calling in circulating tumor DNA

Carrié H et al., Nature Communications, 2025.

## Summary

Builds a benchmark from longitudinal patient-matched cfDNA in colorectal and breast cancer: high- and ultra-low-tumour samples from the same patient are mixed into dilution series that keep the patient's germline and blood-cell mutation background. With deep whole-genome and exome sequencing they define a reference of about 37,000 SNVs and 58,000 indels, benchmark nine somatic callers across ctDNA levels and depths, and test machine-learning tuning of callers.

## Why It Matters

Read in 2026-02, after our [[low-vaf-caller-benchmark|benchmark]] was paused. Its design keeps the blood-cell mutation background, so CH is in the truth set, which our in-silico design also did but without real library effects. Dmitri proposed it as a model for the analysis plan of the [[halo-truth-set]], and it is the main published benchmark we will compare against when the project resumes.

## Caveats

Whole-genome and exome depths, not ultra-deep targeted panels with duplex consensus; detection limits will differ from ours.

## Source Links

- [DOI 10.1038/s41467-025-67842-x](https://doi.org/10.1038/s41467-025-67842-x), PMID 41407694
