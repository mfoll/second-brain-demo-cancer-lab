---
type: Source
source_type: Code repository
url: https://git.corvane.example/varga-lab/northvale-lead-time
date_accessed: 2026-03-02
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[maja-kovac]]"
  - "[[reproducible-pipelines]]"
  - "[[halyard-cluster]]"
_organized: true
---

# Northvale Lead-Time Code Repository

## Summary

The analysis repository for the [[lead-time-analysis]] on the institute GitLab: R code for sampling, models and tables, the SAP source, and a `targets` pipeline that rebuilds every table from the frozen data releases. Maintained by [[maja-kovac]]; [[tobias-wren]] set up CI.

## Key Details

- Tags: `selection-v2` (sampling, 2025-05), `sap-v1.0` (2026-02-26), `interim-2026-07` (results after Amendment 1), `rerun-2026-10` (in progress).
- Moved from Kestrel to [[halyard-cluster]] in July 2026 and runs inside the group's R Apptainer image; no data in the repository, only paths resolved from the governed storage root.
- Every model output carries the data release version and commit hash in its footer.

## Caveats

The repository is private to the group and the cohort PI.

## Source Links

- [northvale-lead-time on the institute GitLab](https://git.corvane.example/varga-lab/northvale-lead-time)
