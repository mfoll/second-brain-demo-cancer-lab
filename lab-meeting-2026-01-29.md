---
type: Event
date: 2026-01-29
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[halo-cross-site-benchmark]]"
  - "[[mrd-manuscript]]"
  - "[[cancer-genomics-course-2026]]"
_organized: true
---

# Lab Meeting 2026-01-29

Chair Ines Varga, notes [[hannah-lindqvist]]. Thirteen present; [[leila-farouk]]'s first meeting as visiting PhD student.

## Decisions

- **MRD manuscript.** Writing of the [[mrd-manuscript]] starts 2026-02-01. [[dmitri-halvorsen]] leads; the fragmentomics results go in only once the classifier is locked, otherwise the paper reports mutation- and methylation-based MRD calls alone.
- **Halo benchmark.** The [[halo-cross-site-benchmark]] started on 2026-01-19. Our site contributes cfDNA from the shared reference samples; [[tobias-wren]] will run them through `varga-cfdna` on the pre-release branch so Halo gets the same processing as our own data.
- **Course.** The [[cancer-genomics-course-2026]] started on 2026-01-12 with 24 students. Group members teaching: Dmitri, [[amara-okonkwo]], [[maja-kovac]]. Teaching time is protected from lab meeting actions in February.
- **Classifier validation.** [[sofia-reyes-calderon]] reported cross-validated AUC above 0.9 for the boosted model. Ines asked for a check by extraction batch before anyone quotes it.

## Actions

- Sofia: leave-batch-out validation of the fragmentomics classifier for the March meeting.
- Leila: present her site's fragment assay at the March meeting.
