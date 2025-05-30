---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/selection/matching-specification-v2.md
access: guarded-write
last_checked: 2025-10-17
date_accessed: 2025-05-21
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[incidence-density-sampling]]"
  - "[[northvale-matching-specification-v1]]"
  - "[[maja-kovac]]"
_organized: true
---

# Northvale Matching Specification v2

## Summary

The matching rules used to select controls for the [[northvale-early-detection-study]], adopted on 2025-05-21. Supersedes [[northvale-matching-specification-v1]].

## Key Details

- Design: [[incidence-density-sampling]] with replacement, two controls per case.
- Risk set: cohort members alive, cancer-free (except non-melanoma skin cancer) and under follow-up on the case's diagnosis date, with at least 1 ml of plasma excluding the last aliquot.
- Matching factors: sex; recruitment centre; age at blood draw within 1 year; blood-draw date within 3 months.
- Fallback when fewer than two eligible controls: widen draw date to 6 months, then age to 2 years. Used for 19 cases (draw date) and 2 cases (age). Logged in [[northvale-sample-selection-log]].
- Random selection within the eligible set with a fixed seed (20250521).
- Replacement rule for later exclusions: draw a new control from the same risk set with the same rules; used in September 2026 ([[northvale-control-replacement-log]]).

## Caveats

Fasting status was considered and dropped: 31% missing.

## Source Location

Group SharePoint, `group_docs/northvale/selection/`; the sampling code is tagged `selection-v2` in [[northvale-lead-time-code-repository]].
