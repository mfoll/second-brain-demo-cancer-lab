---
type: Question
status: Open
belongs_to: "[[pathology-foundation-models]]"
related_to:
  - "[[colorectal-metastasis-atlas]]"
  - "[[amara-okonkwo]]"
  - "[[benedikt-kraus]]"
_organized: true
---

# Are Pathology Foundation Models Worth It For The Atlas?

Would embeddings from a pathology foundation model, applied to H&E, predict spatial cell-type composition in our colorectal liver metastases well enough to use the roughly 300 archival slides that were never sequenced?

## Why It Matters

The [[colorectal-metastasis-atlas]] covers 40 metastases with Visium HD. Extending even coarse maps to archival slides from the same patients would add before-and-after chemotherapy time points cheaply. If it does not work, we should stop reading and say so.

## Current Answer

Unknown. Indications either way:

- For abundant compartments (tumour, stroma, immune) prediction from H&E is plausible ([[kwame-boateng]], 2026-03-11 call; [[chen-2025-omiclip-visual-omics-foundation-model]]).
- Rare cell types and fine immune subsets are unlikely to be resolved.
- Archival slides from two hospitals over eight years carry scanner and stain shifts ([[shafique-2025-histolite-domain-generalization]]).
- [[benedikt-kraus]] will only trust predicted maps with uncertainty estimates ([[lou-2025-uncertainty-aware-foundation-model-colorectal]]).

## What Would Answer It

The test in [[pathology-foundation-model-evaluation-sketch]]: leave-one-patient-out prediction of Visium HD-derived compartment fractions from H&E embeddings on the 40 sequenced metastases, with a pre-agreed threshold for usefulness.

## Owner

None yet. Deferred to after [[owen-mcallister]] starts on 2027-01-11.
