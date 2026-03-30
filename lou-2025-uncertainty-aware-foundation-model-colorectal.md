---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41746-025-02149-1
doi: 10.1038/s41746-025-02149-1
pmid: "41353286"
licence: cc by-nc-nd
date_accessed: 2026-03-12
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[shafique-2025-histolite-domain-generalization]]"
_organized: true
---

# Uncertainty-aware and causal test-time adaptive foundation model for robust colorectal cancer pathology diagnosis.

Lou S et al., npj Digital Medicine, 2025.

## Summary

UAD-FM adds uncertainty decomposition, causal test-time adaptation and post-hoc calibration to a colorectal pathology foundation model, targeting domain shift and unreliable confidence. Across five public colorectal datasets it reports better accuracy, calibration and robustness than other foundation models and adaptation baselines, with uncertainty maps for human review.

## Why It Matters

Filed after the 2026-03-11 call between [[kwame-boateng]] and [[amara-okonkwo]], where uncertainty maps came up as a way to show the pathologist which regions a model is guessing on. [[benedikt-kraus]] said he would only trust predicted cell maps on archival slides if they came with something like this.

## Caveats

Diagnosis task on public datasets, several of them patch collections; not spatial mapping.

## Source Links

- [Uncertainty-aware and causal test-time adaptive foundation model for colorectal cancer](https://doi.org/10.1038/s41746-025-02149-1)
