---
type: Source
source_type: Internal document
storage_system: Institute contracts register
root_key: corvane_contracts
relative_path: data-agreements/NCR-2025-017/dpia-summary.pdf
access: read-only
date_accessed: 2025-09-18
belongs_to: "[[registry-linkage-agreement]]"
related_to:
  - "[[victor-lindahl]]"
  - "[[consortium-transfer-dpia-draft]]"
_organized: true
---

# Registry Linkage DPIA Summary

## Summary

Summary of the data protection impact assessment for the registry linkage, signed off by [[victor-lindahl]] on 2025-09-18. It concluded that residual risk was low once the linkage key is deleted at the registry and extracts are held only in the institute secure data environment.

## Key Details

- Data flows assessed: identifiers from the biobank and St Aldric to the registry; pseudonymised extract back to the secure environment; analysis inside it.
- Main risks: identifier files in transit, small-cell disclosure in published tables for rare sites, and staff access beyond the named projects.
- Mitigations: encrypted transfer over the registry's portal, identifier files deleted on our side after confirmation of receipt, cell suppression under 5, quarterly access review by [[yara-castellanos]].
- Out of scope: any transfer outside the institute. This is why the consortium clause needs its own DPIA ([[consortium-transfer-dpia-draft]]).

## Source Location

Institute contracts register, root key `corvane_contracts`, `data-agreements/NCR-2025-017/dpia-summary.pdf`.
