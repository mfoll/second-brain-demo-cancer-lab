---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: ch-risk/analysis-plan-v1.1.pdf
access: guarded-write
last_checked: 2026-09-16
date_accessed: 2025-12-03
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[competing-risks]]"
  - "[[lucas-brandt]]"
  - "[[mei-lin-zhou]]"
_organized: true
---

# CH Cancer Risk Analysis Plan

## Summary

The analysis plan for the [[ch-cancer-risk-analysis]], written by [[lucas-brandt]], agreed with [[mei-lin-zhou]] on 2025-12-03; version 1.1 (2026-09-16) records the VAF threshold decision.

## Key Details

- Exposure: CH at baseline, any gene in the panel, VAF 2% or more (primary), 1% or more (secondary); gene groups DNMT3A, TET2, other, DNA damage response.
- Outcome: first incident solid cancer; site-specific secondary outcomes.
- Model: Cox regression with attained age as time scale, cause-specific hazards; competing events are non-cancer death and haematological cancer ([[austin-2017-fine-gray-reporting]]).
- Adjustment: sex, recruitment centre, smoking (see [[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]]), body-mass index, alcohol.
- Reverse causation check: exclude the first two years of follow-up ([[reverse-causation-in-prediagnostic-studies]]).
- Cumulative incidence curves by CH status for interpretation.

## Source Location

Group SharePoint, `group_docs/ch-risk/`.
