---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/registry/variable-specification-2026-07.docx
access: guarded-write
last_checked: 2026-09-08
date_accessed: 2026-07-03
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[northern-cancer-registry-extract-2025]]"
  - "[[victor-lindahl]]"
_organized: true
---

# Registry Linkage Variable Specification

## Summary

The variable list and transfer conditions sent to the [[northern-cancer-registry]] on 2026-07-03 for the 2025 extract. Drafted by [[maja-kovac]] and [[lucas-brandt]], reviewed by [[daniel-asante]] and checked against the data protection impact assessment by [[victor-lindahl]].

## Key Details

- Identifiers: cohort pseudonym only; the registry holds the key.
- Incidence: ICD-10 site, ICD-O-3 morphology and behaviour, diagnosis date, basis of diagnosis, stage (TNM where registered), laterality, sequence number.
- Deaths: date, underlying cause, contributing causes (added after Daniel's review; needed for [[competing-risks]] in the CH analysis).
- Emigration and loss to follow-up dates.
- Retention: registry extracts kept for the life of the analyses plus ten years; superseded extracts archived read-only, not deleted.
- Transfer: secure file exchange to governed storage; no copy outside [[halyard-cluster]].

## Source Location

Group SharePoint, `group_docs/northvale/registry/`.
