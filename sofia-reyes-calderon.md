---
type: Person
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[fragmentomics-classifier]]"
  - "[[sofia-thesis-committee]]"
  - "[[cfdna-fragmentomics]]"
_organized: true
---

# Sofia Reyes Calderon

PhD student since 2024-10, working on the [[fragmentomics-classifier|Fragmentomics Classifier]]. Supervised by Ines, with [[dmitri-halvorsen|Dmitri Halvorsen]] as co-supervisor. Joint first author of the [[mrd-manuscript|MRD Manuscript]].

## Role

- Builds and maintains the fragmentomics feature pipeline (now on FinaleToolkit, see [[finaletoolkit-repository]]) and the classifier itself.
- Ran the batch analysis that triggered the [[lab-meeting-2026-03-12|2026-03-12 decision]] to drop gradient boosting ([[classifier-batch-effect-analysis-2026-03]]), then the stacking evaluation that partly reversed it ([[classifier-stacking-evaluation-2026-04]]).
- Maintains [[classifier-model-card-v2]] and follows [[fragmentomics-classifier-retraining]].

## How We Work Together

Weekly supervision on Thursdays with Dmitri; monthly one-to-one with Ines on thesis progress and career. Sofia works best with a clear question and freedom on method, and she reports negative results quickly, which is how the batch problem was found within two weeks of the first leave-batch-out run. She asked for more statistics training in 2025; she took the institute's biostatistics module in spring 2026 and now leads the classifier's evaluation design.

## Current Threads

- Second-year committee in 2026-11 ([[sofia-thesis-committee]]): chapter 1 is the stacked classifier and the batch story.
- Freezing model card v3 before any external data are seen.
- Feature ablation write-up for the revision supplement ([[classifier-feature-ablation-results]]).
- Discussion with [[leila-farouk|Leila Farouk]] about how her Halo site extracts cfDNA, as a first look at cross-site batch effects.

## Background

Sofia came from a statistics MSc with a project on survival models and had not worked with sequencing data before her PhD. She spent her first six months on the feature pipeline and on [[jin-2021-hcc-fragment-size-end-motifs|the early fragmentomics literature]]. Her thesis plan has three chapters: the stacked classifier and the batch problem, external validation on Halo, and a methods chapter on fragment features of variant-supporting reads shared with Hannah. She is the student representative on the institute's computing users' group and gives the Halyard onboarding session to new students.

## Links

- [[fragment-length-and-end-motif-features]]
- [[does-the-stacked-classifier-generalise-across-extraction-batches]]
- [[ju-2024-cfdna-end-characteristics]]
