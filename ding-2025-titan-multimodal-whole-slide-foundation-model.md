---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41591-025-03982-3
doi: 10.1038/s41591-025-03982-3
pmid: "41193692"
licence: cc by-nc-nd
date_accessed: 2026-02-05
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[xu-2024-prov-gigapath-whole-slide-foundation-model]]"
_organized: true
---

# A multimodal whole-slide foundation model for pathology.

Ding T et al., Nature Medicine, 2025.

## Summary

TITAN is a whole-slide model pretrained on about 336,000 slides with visual self-supervision and alignment to pathology reports and several hundred thousand synthetic captions. Without fine-tuning it produces general slide representations and can generate reports, and the authors target low-data settings such as rare disease retrieval and prognosis.

## Why It Matters

Context, not a tool for us. [[benedikt-kraus]] was interested in the report-generation claim for the tissue unit and asked Ines to keep it on file. For the [[colorectal-metastasis-atlas]] the vision-language part adds little, since we have no free-text reports for the archival slides.

## Caveats

Synthetic captions come from a generative copilot; how errors in those captions propagate is not something we can judge.

## Source Links

- [A multimodal whole-slide foundation model for pathology](https://doi.org/10.1038/s41591-025-03982-3)
