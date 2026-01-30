---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioadv/vbaf236
doi: 10.1093/bioadv/vbaf236
pmid: "41221372"
licence: cc by
date_accessed: 2026-01-12
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[finaletoolkit-repository]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# FinaleToolkit: accelerating cell-free DNA fragmentation analysis with a high-speed computational toolkit

Li JW et al., Bioinformatics Advances, 2025.

## Summary

Presents an open-source Python package with command-line and API interfaces for computing cfDNA fragmentation features, including end motifs and window protection scores, from large whole-genome datasets. The authors report large speed-ups over original implementations, benchmark it against them, and show genome-wide feature generation over arbitrary intervals.

## Why It Matters

Adopted for the [[fragmentomics-classifier|classifier]] feature pipeline in 2026-01 after Sofia and [[tobias-wren|Tobias Wren]] timed it on Halyard: about 6 instead of 40 minutes per sample. Using a maintained public tool rather than our scripts also makes the Halo container easier to audit. Code location: [[finaletoolkit-repository]].

## Caveats

We validated that its length and motif outputs match our previous scripts on 50 samples (correlation above 0.99); window protection scores are not used yet.

## Source Links

- [DOI 10.1093/bioadv/vbaf236](https://doi.org/10.1093/bioadv/vbaf236), PMID 41221372
