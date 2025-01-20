---
type: Topic
belongs_to: "[[exploratory-reading]]"
related_to:
  - "[[spatial-transcriptomics]]"
  - "[[colorectal-metastasis-atlas]]"
  - "[[kwame-boateng]]"
has:
  - "[[foundation-model]]"
  - "[[are-pathology-foundation-models-worth-it-for-the-atlas]]"
  - "[[pathology-foundation-model-evaluation-sketch]]"
  - "[[campanella-2025-clinical-benchmark-pathology-foundation-models]]"
_organized: true
---

# Pathology Foundation Models

Exploration cluster on large self-supervised models trained on H&E whole-slide images, and the newer ones that link histology to reports or spatial transcriptomics. Started after [[kwame-boateng]]'s institute seminar on 2026-01-28.

## Why We Are Reading This

The [[colorectal-metastasis-atlas]] has H&E for every Visium HD section and for about 300 further archival slides from the same 40 patients that were never sequenced. If slide embeddings from a pathology foundation model could predict spatial cell-type maps, or at least flag regions worth sequencing, the archival slides would stop being dead weight. [[benedikt-kraus]] is sceptical but curious, and [[amara-okonkwo]] wants a cheap test before anyone writes it into a grant. The question that matters is [[are-pathology-foundation-models-worth-it-for-the-atlas]].

## What We Have Learned So Far

- The field moved from patch encoders to slide-level and multimodal models within two years: [[xu-2024-prov-gigapath-whole-slide-foundation-model]], [[ding-2025-titan-multimodal-whole-slide-foundation-model]], [[xu-2025-mstar-knowledge-enhanced-pathology-foundation-model]], [[yan-2025-pathorchestra-foundation-model]].
- Independent benchmarks matter more than the papers' own: [[campanella-2025-clinical-benchmark-pathology-foundation-models]] is the one we trust most, because the slides come from routine clinical workflow at three centres.
- Two papers go directly at our use case, predicting expression from H&E: [[chen-2025-omiclip-visual-omics-foundation-model]] and [[huang-2025-stpath-generative-foundation-model]].
- Domain shift between scanners and stain protocols is the practical problem for our archival slides, which come from two hospitals over eight years: [[shafique-2025-histolite-domain-generalization]], [[wang-2025-stainlut-stain-normalization]], [[lou-2025-uncertainty-aware-foundation-model-colorectal]].
- Concepts: [[foundation-model]], [[multiple-instance-learning]].

## Constraints

Model weights for several of these require accepting licence terms through a model hub account, and some forbid commercial use. Running them on [[halyard-cluster]] needs the GPU partition (granted 2026-09-22) and an Apptainer image, which [[tobias-wren]] says is a day's work per model. Nothing here should touch patient slides until [[yara-castellanos]] has checked that our data agreements allow it.

## Notes In This Cluster

Sources: the ten papers above plus [[kwame-boateng-seminar-slides-2026-01]]. Note: [[pathology-foundation-model-evaluation-sketch]]. Question: [[are-pathology-foundation-models-worth-it-for-the-atlas]].

## Promotion Status

Not yet. There is an evaluation sketch but no owner time. The [[exploratory-reading-review-2026-10]] deferred the decision until [[owen-mcallister]] joins in 2027-01, because the atlas postdoc role was written with imaging in mind.
