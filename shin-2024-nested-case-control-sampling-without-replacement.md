---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1007/s10985-024-09633-y
doi: 10.1007/s10985-024-09633-y
pmid: "39235702"
licence: cc by
date_accessed: 2025-03-10
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[incidence-density-sampling]]"
  - "[[should-northvale-controls-be-sampled-with-replacement]]"
_organized: true
---

# Nested case-control sampling without replacement.

## Summary

Shin and Saegusa (Lifetime Data Analysis, 2024) study a variant of the nested case-control design in which controls already selected for an earlier case are removed from later risk sets. They extend inverse probability weighting estimators to this design, derive variance estimators, and show by simulation that it can be more efficient than standard sampling. The example uses a large diet and health cohort.

## Why It Matters

[[maja-kovac]] read it while deciding between sampling with and without replacement for the [[case-control-sample-selection]]. The efficiency gain depends on weighted analysis rather than the conditional likelihood, and our analysis plan was built around [[conditional-logistic-regression]]. We kept standard sampling with replacement; see [[should-northvale-controls-be-sampled-with-replacement]].

## Caveats

Methodological paper; the gain is shown in simulation and one example, not for small matched sets of two controls.

## Source Links

- [Nested case-control sampling without replacement](https://doi.org/10.1007/s10985-024-09633-y)
