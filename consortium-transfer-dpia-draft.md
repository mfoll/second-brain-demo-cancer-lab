---
type: Source
source_type: Internal document
storage_system: Board shared drive
root_key: corvane_board
relative_path: policy-revision-2026/dpia-consortium-transfer-draft.docx
access: guarded-write
date_accessed: 2026-08-28
last_checked: 2026-10-21
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[victor-lindahl]]"
  - "[[registry-linkage-dpia-summary]]"
  - "[[cohen-2026-pseudonymisation-epidemiological-reliability]]"
_organized: true
---

# Consortium Transfer DPIA Draft

## Summary

[[victor-lindahl]]'s data protection impact assessment for the consortium transfer clause in [[data-access-policy-draft-3]]. The outline was ready for [[data-governance-board-2026-09-10]]; the board would not adopt the clause until the section on receiving sites is complete.

## Key Details

- Processing assessed: transfer of pseudonymised cfDNA fragment features, sequencing-derived variant calls and minimal clinical variables from Corvane to a consortium secure environment hosted at Brightwater University Hospital, with access by five other Halo sites.
- Main risks identified: re-identification by a receiving site that knows who is in the cohort (target-in-cohort; see [[cohen-2026-pseudonymisation-epidemiological-reliability]]), germline information in raw reads, and onward transfer.
- Mitigations proposed: feature tables rather than reads where the analysis allows, minimum dataset, days-from-surgery instead of dates, access logs reviewed quarterly, deletion within 90 days.
- Missing as of 2026-10-21: answers from two of the five receiving sites to Victor's site questionnaire, collected by [[eva-novak]].

## Caveats

Assesses only data, not samples. Does not cover federated model training, which would need its own screening ([[federated-cfdna-learning]]).

## Source Location

Board shared drive, root key `corvane_board`, `policy-revision-2026/dpia-consortium-transfer-draft.docx`. Victor edits; the drafting group comments.
