---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41746-025-02020-3
doi: 10.1038/s41746-025-02020-3
pmid: "41238784"
licence: cc by-nc-nd
date_accessed: 2026-02-09
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[chen-2025-omiclip-visual-omics-foundation-model]]"
_organized: true
---

# STPath: a generative foundation model for integrating spatial transcriptomics and whole-slide images.

Huang T et al., npj Digital Medicine, 2025.

## Summary

STPath is pretrained on whole-slide images paired with spatial transcriptomics and predicts expression for about 39,000 genes across 17 organs without fine-tuning. A geometry-aware transformer combines histology, expression, organ type and sequencing technology, trained by masked expression prediction. It was evaluated on six tasks across 23 datasets, including expression prediction, spot imputation and spatial clustering.

## Why It Matters

Read alongside [[chen-2025-omiclip-visual-omics-foundation-model]] by [[amara-okonkwo]]. The spot imputation task is interesting for the atlas: if it worked on our tissue, it could fill in sections where Visium HD failed QC (four of the 40 metastases have one failed section). That is a much smaller and more testable claim than mapping archival slides.

## Caveats

Sequencing technology is a model input, so it may handle Visium HD differently from older platforms; we do not know whether HD was in pretraining.

## Source Links

- [STPath](https://doi.org/10.1038/s41746-025-02020-3)
