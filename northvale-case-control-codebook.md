---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/codebooks/case-control-codebook-v3.xlsx
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-02-20
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[northvale-date-definitions]]"
  - "[[northvale-baseline-questionnaire-codebook]]"
_organized: true
---

# Northvale Case-Control Codebook

## Summary

Variable dictionary for the analysis dataset of the [[lead-time-analysis]]: identifiers, matched-set structure, dates, outcome, exposure and covariates. Version 3, February 2026, maintained by [[maja-kovac]].

## Key Details

- `set_id`, `role` (case/control), `index_date`, `draw_date`, `ttd_years` (time from draw to the set's index date), `window` (four levels).
- `site` (pancreas C25, colorectum C18 to C20), `stage_at_dx` where registered (missing for 22% of pancreatic cases).
- `meth_score`, `meth_score_z` (standardised on controls), `gdna_flag`, `storage_years`, `freezer_moves`.
- Covariates from [[northvale-baseline-questionnaire-codebook]] and [[northvale-smoking-history-derivation]].
- `replaced_2026` flag for the three controls replaced after the 2025 extract.

Date conventions are spelled out in [[northvale-date-definitions]].

## Source Location

Group SharePoint, `group_docs/northvale/codebooks/`.
