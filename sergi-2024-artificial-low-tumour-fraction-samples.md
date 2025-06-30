---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s12859-024-05793-8
doi: 10.1186/s12859-024-05793-8
pmid: "38720249"
licence: cc by
date_accessed: 2025-06-03
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[can-in-silico-dilutions-replace-a-physical-truth-set]]"
_organized: true
---

# Integrated approach to generate artificial samples with low tumor fraction for somatic variant calling benchmarking

Sergi A et al., BMC Bioinformatics, 2024.

## Summary

Proposes generating artificial ultra-deep targeted sequencing data with a read simulator trained on several real datasets, then inserting low-fraction variants to mimic samples with little tumour DNA. Using these datasets as ground truth, the authors tuned common callers and improved their detection of very low-fraction variants.

## Why It Matters

Read in 2025-06 when choosing between simulation and in-silico mixing of real reads for the [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]]. We chose mixing real reads to keep patient-specific error backgrounds; this paper remains the best argument for simulation and is the counterpoint in [[can-in-silico-dilutions-replace-a-physical-truth-set]].

## Caveats

Simulated reads; whether caller rankings on simulated data hold on real cfDNA is exactly our open question.

## Source Links

- [DOI 10.1186/s12859-024-05793-8](https://doi.org/10.1186/s12859-024-05793-8), PMID 38720249
