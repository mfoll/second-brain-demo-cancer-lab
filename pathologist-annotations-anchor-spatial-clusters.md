---
type: Opinion
status: Active
confidence: Medium
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[benedikt-kraus]]"
  - "[[atlas-pathology-annotations]]"
  - "[[spatial-transcriptomics]]"
_organized: true
---

# Pathologist Annotations Anchor Spatial Clusters

## Stance

In the atlas, expression clusters are interpreted against the pathologist's region annotations, not the reverse. A cluster that crosses an annotated boundary is a question for [[benedikt-kraus]], not a new tissue compartment.

## Why I Think This

In the [[visium-hd-pilot]], unsupervised clustering split one post-chemotherapy resection into a "novel" compartment that turned out to be a fold artefact plus section-edge drying. Benedikt recognised it in minutes from the H&E. In treated tissue, necrosis, fibrosis and mucin pools produce strong expression structure that is not biology of interest.

## Scope

Tissue-level interpretation in the [[colorectal-metastasis-atlas]]. Not a rule against discovering structure within an annotated region, such as niches inside viable tumour.

## What Would Change My Mind

Reproducible expression compartments that recur across patients and that pathologists cannot map to morphology even after review.

## Implications

Annotations are loaded before clustering in the spatial pipeline ([[atlas-pathology-annotations]]), and figure drafts show the annotation outline on every section.
