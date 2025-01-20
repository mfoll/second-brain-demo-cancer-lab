---
type: Question
status: Answered
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[tumour-informed-vs-tumour-naive-mrd]]"
  - "[[fragmentomics-classifier]]"
  - "[[methylation-panel-design]]"
_organized: true
---

# Should the MRD Call Combine Methylation and Fragmentomics?

Should the main MRD call be a single combined score across variants, methylation and fragmentomics, or should each layer be reported separately?

## Current Answer

Combined, with each layer also reported separately in a supplementary table. Decided at the [[mrd-interim-analysis-meeting-2025-12-03|2025-12-03 interim meeting]] and pre-specified in [[mrd-statistical-analysis-plan-v2]].

## Reasoning

- Variants are most specific but unavailable for 23 of 212 patients.
- Methylation gives a tumour-naive call with about 0.1% tumour fraction detection limit ([[methylation-panel-qc-report-2025-09]]).
- Fragmentomics adds sensitivity at very low tumour fraction but is most exposed to batch effects ([[batch-confounding-in-cfdna-studies]]).
- Combining is the pattern in recent tumour-naive MRD work, where copy-number and fragment-length profiles added sensitivity on top of mutations, more in advanced than in early disease ([[nguyen-2025-tumour-naive-multimodal-mrd]]).

## Caveat

The combination rule is an OR across layers with layer-specific thresholds, not a learned meta-model, to keep it interpretable for clinicians. If the stacked fragmentomics model changes its operating point, the combined specificity must be rechecked.
