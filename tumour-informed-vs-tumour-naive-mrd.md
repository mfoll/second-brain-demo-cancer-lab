---
type: Concept
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[minimal-residual-disease]]"
  - "[[should-the-mrd-call-combine-methylation-and-fragmentomics]]"
_organized: true
---

# Tumour-Informed vs Tumour-Naive MRD

Two designs for detecting residual cancer in plasma.

**Tumour-informed**: sequence the resected tumour, pick its somatic variants, then track those variants in plasma with deep, error-corrected sequencing. Very specific, because a variant must match the tumour; sensitive because many variants can be tracked at once. Needs good tissue, and a personalised panel or deep sequencing per patient. Pancreatic tumours often have low cellularity: in St Aldric 23 of 212 tumours gave no usable variants.

**Tumour-naive**: look for cancer-like signal without the tumour, using fixed panels of recurrent mutations, methylation, copy number or fragmentation. Works for every patient and does not wait for tissue, but must separate tumour signal from clonal hematopoiesis and normal tissue turnover, and usually has a higher detection limit.

## How We Use It

The [[pancreatic-cfdna-mrd-study|MRD study]] combines both: tumour-informed variants where available, plus the [[methylation-panel-design|methylation panel]] and the [[fragmentomics-classifier|fragmentomics classifier]] as tumour-naive layers ([[should-the-mrd-call-combine-methylation-and-fragmentomics]]).

## Evidence

- Tumour-informed exome-based ctDNA in pancreatic cancer: detection in the post-operative window associated with shorter disease-free survival ([[botta-2024-tumour-informed-ctdna-pdac]]).
- Tumour-naive multimodal profiling: mutations plus copy number and fragment length, with clonal hematopoiesis variants needing exclusion ([[nguyen-2025-tumour-naive-multimodal-mrd]]).
