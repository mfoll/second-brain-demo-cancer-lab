---
type: Concept
maturity: Growing
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[multiple-instance-learning]]"
  - "[[campanella-2025-clinical-benchmark-pathology-foundation-models]]"
_organized: true
---

# Foundation Model

A large model pretrained on broad, mostly unlabelled data, whose learned representations are reused for many downstream tasks with little or no task-specific training.

## In Pathology

Pathology foundation models are trained by self-supervision on millions of H&E image tiles, sometimes with reports or expression as a second modality. Downstream use takes three forms:

- Frozen embeddings plus a small model (linear probe or attention pooling). Cheap, and often as good as fine-tuning for common tasks, as [[kwame-boateng]] reported ([[kwame-boateng-seminar-slides-2026-01]]).
- Fine-tuning on labelled data. Better for unusual tasks, expensive, easy to overfit with small cohorts.
- Zero-shot use for multimodal models, such as retrieval or report generation ([[ding-2025-titan-multimodal-whole-slide-foundation-model]]).

Tile-level models produce one embedding per patch; slide-level models aggregate patches, typically through [[multiple-instance-learning]].

## What To Watch For

- Pretraining data overlap with the evaluation data, which inflates published results. Independent benchmarks such as [[campanella-2025-clinical-benchmark-pathology-foundation-models]] are the corrective.
- Domain shift from scanners and staining ([[shafique-2025-histolite-domain-generalization]], [[wang-2025-stainlut-stain-normalization]]).
- Licences: several weights are research-only and gated.

## Relation To Our Work

The idea also appears in the [[federated-cfdna-learning]] discussions, where [[arjun-mehta]] has floated pretraining a fragment-level model across Halo sites. Ines's view is that cfDNA cohorts are too small for that to beat engineered features yet.
