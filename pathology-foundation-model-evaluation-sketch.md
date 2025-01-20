---
type: Note
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[are-pathology-foundation-models-worth-it-for-the-atlas]]"
  - "[[amara-okonkwo]]"
  - "[[colorectal-metastasis-atlas]]"
_organized: true
---

# Pathology Foundation Model Evaluation Sketch

A sketch, not a plan, written by [[amara-okonkwo]] and Ines on 2026-03-18 after Amara's call with [[kwame-boateng]]. It describes the smallest test that would answer [[are-pathology-foundation-models-worth-it-for-the-atlas]].

## Design

- Data: the 40 sequenced metastases from the [[colorectal-metastasis-atlas]], H&E images registered to Visium HD.
- Target: compartment fractions (tumour, stroma, immune, hepatocyte, necrosis) per 16 µm bin, from the best method in the [[deconvolution-benchmark]] once it is frozen.
- Features: frozen tile embeddings from two models chosen with [[campanella-2025-clinical-benchmark-pathology-foundation-models]] in mind, plus [[chen-2025-omiclip-visual-omics-foundation-model]] as the expression-aware option.
- Model: regularised linear regression per compartment. No fine-tuning in the first round.
- Validation: leave one patient out. Success threshold agreed in advance: correlation of at least 0.7 for tumour and stroma fractions at bin level.
- Scanner check: ten slides rescanned on the second hospital's scanner, after [[shafique-2025-histolite-domain-generalization]].

## Cost

About four weeks of postdoc time, plus a day per model for [[tobias-wren]] to build Apptainer images for the GPU partition on [[halyard-cluster]]. Weight licences need checking with [[yara-castellanos]].

## Not Doing

No archival slides until the test passes; no rare cell types; no attention maps as proxies ([[multiple-instance-learning]]).
