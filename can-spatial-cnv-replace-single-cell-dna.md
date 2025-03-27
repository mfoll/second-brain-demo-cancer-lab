---
type: Question
status: Open
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[single-cell-cnv-pilot]]"
  - "[[zhang-2025-slidecna]]"
  - "[[tumour-evolution]]"
_organized: true
---

# Can Spatial CNV Replace Single-Cell DNA?

Can copy-number subclones inferred from spatial expression give the atlas enough clonal resolution that we do not need single-cell DNA sequencing?

## Context

The [[single-cell-cnv-pilot]] concluded in July 2025 that single-cell DNA added little to bulk phylogenies at about 11,500 EUR per tumour. The atlas instead infers copy number from Visium HD expression, which comes free with the data but is noisier and limited to large events.

## Current Answer

Partly. In the 26 sequenced pairs, expression-based inference recovers arm-level and large segmental events and separates two to four subclones per section, located in space. It does not see focal events and cannot build deep trees. Published tools show the same profile of strengths ([[zhang-2025-slidecna]], [[denisenko-2024-ovarian-subclones-spatial]]).

## What Would Change It

If the atlas finds a candidate resistance subclone that only focal events define, a targeted single-cell DNA follow-up on a few lesions would be justified. Felix's reconsideration thresholds still apply ([[single-cell-cnv-pilot-review-2025-07-24]]).
