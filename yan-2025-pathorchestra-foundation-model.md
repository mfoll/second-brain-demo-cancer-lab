---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41746-025-02027-w
doi: 10.1038/s41746-025-02027-w
pmid: "41258399"
licence: cc by-nc-nd
date_accessed: 2026-02-12
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[foundation-model]]"
  - "[[colorectal-metastasis-atlas]]"
_organized: true
---

# PathOrchestra: a comprehensive foundation model for computational pathology with over 100 diverse clinical-grade tasks.

Yan F et al., npj Digital Medicine, 2025.

## Summary

A pathology foundation model trained on about 287,000 slides from 21 tissue types at three centres and evaluated on 112 tasks from private and public datasets, from slide preprocessing to subtype classification, biomarker assessment, expression prediction and structured report generation. Accuracy above 0.95 on 47 tasks; the authors report structured reports for colorectal cancer and lymphoma.

## Why It Matters

Filed because it covers colorectal tissue explicitly and includes slide preprocessing tasks (quality control, artefact detection), which [[kwame-boateng]] said is where models save most time on archival slides. Not on the shortlist for the atlas evaluation.

## Caveats

Very broad task list with mostly the developers' data; independent evaluation would be needed. High headline accuracies on many tasks say little about the hard ones.

## Source Links

- [PathOrchestra](https://doi.org/10.1038/s41746-025-02027-w)
