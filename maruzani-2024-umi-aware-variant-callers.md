---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s12864-024-10737-w
doi: 10.1186/s12864-024-10737-w
pmid: "39227777"
licence: cc by
date_accessed: 2025-05-20
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[low-vaf-caller-shortlist-2025-06]]"
  - "[[dmitri-halvorsen]]"
_organized: true
---

# Benchmarking UMI-aware and standard variant callers for low frequency ctDNA variant detection

Maruzani R et al., BMC Genomics, 2024.

## Summary

Benchmarks four standard callers (Mutect2, bcftools, LoFreq, FreeBayes) and two UMI-aware callers (UMI-VarCal, UMIErrorCorrect) on spike-in and ctDNA datasets, adding synthetic UMIs where needed. Callers differed in their sensitivity and specificity trade-offs; Mutect2 was sensitive but made more private calls without UMIs, UMI-VarCal had the fewest likely false positives on synthetic data, and Mutect2 balanced both when UMIs were present.

## Why It Matters

Starting point for Dmitri's [[low-vaf-caller-shortlist-2025-06|caller shortlist]] in the [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]]. It is why Mutect2 with consensus reads stayed on the list and why we insisted on UMI consensus for every caller.

## Caveats

Synthetic UMIs do not reproduce real UMI family structure, the same limitation that paused our own in-silico work.

## Source Links

- [DOI 10.1186/s12864-024-10737-w](https://doi.org/10.1186/s12864-024-10737-w), PMID 39227777
