---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: ch-risk/codebook-v2.xlsx
access: guarded-write
last_checked: 2026-09-21
date_accessed: 2026-05-12
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[northvale-baseline-questionnaire-codebook]]"
  - "[[ch-subcohort-variant-calls]]"
_organized: true
---

# CH Subcohort Codebook

## Summary

Variable dictionary for the CH analysis dataset, maintained by [[lucas-brandt]]. Version 2 (May 2026) adds per-sample CH summaries derived from [[ch-subcohort-variant-calls]].

## Key Details

- `ch_any_2`, `ch_any_1`: binary CH status at the two thresholds; `ch_max_vaf`, `ch_n_variants`.
- `ch_dnmt3a`, `ch_tet2`, `ch_ddr` (PPM1D, TP53, CHEK2), `ch_other`.
- Follow-up: `entry_age`, `exit_age`, `event_type` (solid cancer, haematological cancer, non-cancer death, censored), `event_site`.
- Covariates shared with the case-control codebook; smoking variables from [[northvale-smoking-history-derivation]].

## Source Location

Group SharePoint, `group_docs/ch-risk/`.
