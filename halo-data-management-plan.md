---
type: Source
source_type: Internal document
date_accessed: 2025-06-30
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[ngozi-adeyemi]]"
  - "[[yara-castellanos]]"
  - "[[group-data-management-plan]]"
_organized: true
---

# Halo Data Management Plan

The consortium data management plan, version 1.1 of 2025-06-30, written by [[ngozi-adeyemi]] with input from each site's data steward; [[yara-castellanos]] wrote the Corvane section.

## Key Details

- Hub at Brightwater; each site uploads raw reads, per-sample feature tables and calls with checksums.
- Pseudonymisation: sites use local codes; the hub holds the link between local codes and consortium codes; truth-set samples carry a third, blinded code.
- Retention: raw data for ten years after the consortium ends; deletion confirmation required at receiving sites on exit.
- Access: through the multi-party data sharing agreement and a per-use request to the steering committee.
- Corvane section: our raw data and features stay on governed storage at Corvane; only the uploads permitted by our policy go to the hub. In 2025 we assumed this would be enough. It is not, for the patient tier.

## Why It Matters

The DMP describes the intended flow; [[halo-data-flow-and-transfer-constraints]] describes what actually can move today. Our own [[group-data-management-plan]] refers to this document for Halo data.

## Source Location

Halo hub, `wp1/dmp/halo-dmp-v1.1.pdf`.
