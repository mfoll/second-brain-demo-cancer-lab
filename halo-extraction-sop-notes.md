---
type: Note
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[dmitri-halvorsen]]"
  - "[[fatima-benali]]"
_organized: true
---

# Halo Extraction SOP Notes

Working notes from reading the six Halo sites' cfDNA extraction SOPs, collected by [[dmitri-halvorsen|Dmitri Halvorsen]] for the length-correction step of the [[fragmentomics-classifier|Fragmentomics Classifier]] before Halo validation.

## What Differs Between Sites

- Three extraction chemistries are in use across the six sites: two column-based kits and one magnetic-bead protocol. Our own [[cfdna-extraction-sop-v3|extraction SOP v3]] uses a column kit.
- Plasma input ranges from 2 to 4 mL. Two sites double-spin at different speeds.
- Elution volume varies, which matters for library input but not, as far as we can tell, for fragment length.
- Only two sites record the kit lot per sample, which is the variable that caused our own batch problem ([[extraction-kit-lot-change-2025-06-16|kit lot change]]).

## Why It Matters

The bead protocol is the one most likely to shift the short-fragment fraction, so its site is where the bridging correction on healthy-donor plasma will matter most. [[fatima-benali|Fatima Benali]] has offered size profiles from both bead and column extractions of the same donor plasma.

The side-by-side table of all six SOPs is in [[halo-sop-comparison-v2]]; this note keeps only the points relevant to our classifier.
