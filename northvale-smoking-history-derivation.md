---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/codebooks/smoking-derivation-v2.md
access: guarded-write
last_checked: 2026-09-21
date_accessed: 2026-01-26
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]]"
  - "[[northvale-baseline-questionnaire-codebook]]"
_organized: true
---

# Northvale Smoking History Derivation

## Summary

How the group derives smoking variables from the two Northvale questionnaire versions. Written by [[lucas-brandt]] with input from [[mei-lin-zhou]]; used by both the [[ch-cancer-risk-analysis]] and the [[lead-time-analysis]].

## Key Details

- Status (never, former, current): available for 99.1% of participants in both versions.
- Pack-years: computable for 71% of ever-smokers. Missing mostly for V1 former smokers, who were not asked intensity.
- Time since quitting: V2 only.
- Missing pack-years are multiply imputed using status, age, sex, centre, questionnaire version and alcohol, following [[keogh-2018-multiple-imputation-nested-case-control]] for the nested study; the CH analysis uses the same imputation model on the full subcohort.

## Caveats

Missingness depends on questionnaire version, which depends on recruitment date. Imputation assumes that, given version, missing intensity is like observed intensity.

## Source Location

Group SharePoint, `group_docs/northvale/codebooks/`.
