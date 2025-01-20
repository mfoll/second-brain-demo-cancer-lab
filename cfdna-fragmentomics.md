---
type: Topic
related_to:
  - "[[fragmentomics-classifier]]"
  - "[[minimal-residual-disease]]"
  - "[[cancer-early-detection]]"
_organized: true
---

# cfDNA Fragmentomics

Retrieval surface for everything about how cell-free DNA is cut: fragment lengths, end motifs, nucleosome footprints, and the pre-analytical and computational biases that distort them. The group uses fragmentomics as one signal layer of the [[pancreatic-cfdna-mrd-study|Pancreatic cfDNA MRD Study]] and watches it for the [[northvale-early-detection-study|Northvale Early Detection Study]].

## Start Here

- [[fragment-length-and-end-motif-features]]: the feature families our classifier uses and why.
- [[fragmentomics-classifier]]: the current stacked model and its history.
- [[batch-confounding-in-cfdna-studies]]: the lesson from the St Aldric extraction lot change.
- [[cfdna-fragmentomics-reading-notes]]: running digest of what the papers below changed in our thinking.

## Our Working View

Fragment-length features carry most of the tumour signal at low tumour fraction but are the most sensitive to extraction, storage and library preparation. End motifs are noisier per sample but, in our data, more stable across batches. That asymmetry is why the classifier is stacked rather than a single model ([[classifier-design-review-2026-04-02]]).

## Practical Lessons

- Record extraction kit, lot and operator per sample, and randomise processing order across outcomes. The St Aldric lot change of 2025-06-16 cost us a classifier ([[extraction-kit-lot-change-2025-06-16]]).
- Evaluate with leave-batch-out folds; within-batch cross-validation overstated performance by 0.17 AUC for gradient boosting ([[classifier-batch-effect-analysis-2026-03]]).
- Pin the reference genome, aligner and feature tool version; they change features ([[liu-2024-reference-biases-fragmentomics]], [[finaletoolkit-repository]]).
- Do not take fragment features from methylation libraries; take them from shallow WGS of the same extract.
- Shallow WGS at about 5x is enough for length and motif features but not for nucleosome footprinting at single loci.

## Papers

- Reviews: [[sirajee-2024-cell-free-nucleic-acid-fragmentomics]].
- End motifs and size: [[ju-2024-cfdna-end-characteristics]], [[jin-2021-hcc-fragment-size-end-motifs]].
- Biases and tools: [[liu-2024-reference-biases-fragmentomics]], [[spiegl-2023-gcparagon]], [[li-2025-finaletoolkit]].
- Variant origin from fragments: [[brown-2025-fragmentomic-variant-origin]].

## Open Threads

- [[does-the-stacked-classifier-generalise-across-extraction-batches]]
- [[should-the-mrd-call-combine-methylation-and-fragmentomics]]
- Fragment features of variant-supporting reads as a CH marker, tested in the [[clonal-hematopoiesis-filter]].

## Related Topics

[[minimal-residual-disease]], [[cancer-early-detection]], [[reproducible-pipelines]].
