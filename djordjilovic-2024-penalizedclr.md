---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s12859-024-05850-2
doi: 10.1186/s12859-024-05850-2
pmid: "38937668"
licence: cc by
date_accessed: 2026-03-18
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[conditional-logistic-regression]]"
  - "[[page-2022-prediagnostic-methylation-melanoma]]"
_organized: true
---

# penalizedclr: an R package for penalized conditional logistic regression for integration of multiple omics layers.

## Summary

An R package for penalised conditional logistic regression in matched case-control studies, with separate L1 or L2 penalties for different blocks of covariates and stability selection for variable choice.

## Why It Matters

The main Northvale analysis uses one summary methylation score, but the SAP lists an exploratory region-level analysis across the 1,840 panel regions. [[maja-kovac]] tested this package on the frozen data in March 2026 for that exploratory step, with clinical covariates unpenalised and methylation regions penalised. It ran on the old Kestrel cluster in under ten minutes per fit. Kept as the planned tool; exploratory results will not be used to choose the main score.

## Caveats

Tool paper; selection stability depends heavily on the number of matched sets.

## Source Links

- [penalizedclr](https://doi.org/10.1186/s12859-024-05850-2)
