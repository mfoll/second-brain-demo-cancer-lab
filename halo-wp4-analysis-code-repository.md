---
type: Source
source_type: Code repository
storage_system: Halo GitLab at Brightwater
root_key: halo_git
relative_path: wp4/halo-benchmark
access: guarded-write
last_checked: 2026-10-08
date_accessed: 2026-10-08
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[liam-oconnell]]"
  - "[[tobias-wren]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Halo WP4 Analysis Code Repository

The shared WP4 repository: the feature-extraction Nextflow module run at every site, the analysis code for the benchmark, and the analysis plan under `docs/`. Hosted on the consortium GitLab at Brightwater; Corvane has maintainer rights.

## Key Details

- `modules/features/`: per-sample feature table from each assay's calls or reads; one container image built in CI, same approach as ours ([[apptainer-decision-2026-05-06]]).
- `analysis/contrived/`: LoB, LoD and concordance code used for [[halo-interim-benchmark-report-2026-10]].
- `analysis/patient/`: written and tested on simulated data; never run on real patient-tier data.
- Tests with nf-test; [[liam-oconnell]] and [[tobias-wren]] review pull requests.
- Tag `v0.6.0` (2026-10-02) is the version used for the interim report.

## Caveats

The repository holds code and synthetic test data only. Never commit truth-set data or keys.

## Source Location

Consortium GitLab, root key `halo_git`, `wp4/halo-benchmark`. Guarded write: changes through merge requests.
