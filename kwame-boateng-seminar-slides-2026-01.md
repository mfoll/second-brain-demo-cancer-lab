---
type: Source
source_type: Slide deck
date_accessed: 2026-01-29
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[kwame-boateng]]"
  - "[[benedikt-kraus]]"
  - "[[foundation-model]]"
_organized: true
---

# Kwame Boateng Seminar Slides, January 2026

Slides from [[kwame-boateng]]'s institute pathology seminar on 2026-01-28, "Foundation models on the diagnostic floor", shared by [[benedikt-kraus]] with his permission for internal use.

## What We Took From It

- A short history from tile encoders to slide-level and multimodal models, with [[xu-2024-prov-gigapath-whole-slide-foundation-model]] as the turning point.
- His unit's experience: frozen embeddings plus a small classifier usually match fine-tuning for common tasks and are far cheaper. That matches our own preference for simple models after the fragmentomics classifier episode ([[lab-meeting-2026-03-12]]).
- Failure modes he has seen: pen marks, tissue folds, scanner changes, slides cut before a stain protocol change. Each shifted embeddings more than tumour type did in some tests.
- His recommendation to rely on independent benchmarks, in particular [[campanella-2025-clinical-benchmark-pathology-foundation-models]].

## Why It Matters

Origin of the [[pathology-foundation-models]] cluster, created the next day.

## Caveats

Contains unpublished results from his unit; not to be shared outside the group. Figures are not copied here.

## Source Location

Institute seminar archive, pathology series, 2026-01-28. PDF copy in the group drive under `Reading/pathology-fm/`.
