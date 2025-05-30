---
type: Source
source_type: Internal document
date_accessed: 2025-05-30
belongs_to: "[[lab-data-management-plan]]"
related_to:
  - "[[yara-castellanos]]"
  - "[[corvane-research-data-policy]]"
  - "[[data-tiering]]"
_organized: true
---

# Group Data Management Plan

The Computational Tumour Evolution Group's data management plan, version 1.0, approved by the data governance board on 2025-05-27. Written by [[yara-castellanos]] and Ines Varga in [[lab-data-management-plan]].

## Summary

One plan for all group data, referenced by each grant DMP. It defines three data classes, where each may be stored, who may access it, how long it is kept and who is accountable.

## Key Details

- **Classes.** Identifiable clinical data (never on HPC, stays in hospital or biobank systems); pseudonymised sequencing and imaging data (HPC project space, role-based access); derived and aggregate results (shareable after review).
- **Keys.** Northvale pseudonymisation keys held by the biobank ([[paolo-ferrante]]); St Aldric keys by the hospital study team.
- **Retention.** Raw sequencing kept 10 years after the last publication using it. Intermediates may be deleted once they can be regenerated from raw data with a released pipeline version.
- **Access.** By role, reviewed annually by the steward. Leavers lose access on their last day ([[offboard-a-leaver]]).
- **Sharing.** Consortium transfers follow the institute policy; at approval this did not cover transfer to Halo sites, which is now addressed by the [[data-access-policy-revision]].

## Why It Matters

The intermediate-deletion rule made the Kestrel triage quick ([[kestrel-data-inventory]]). The plan is due a v1.1 for Halyard storage and the cold archive.

## Source Location

Group drive `Governance/DMP/group-dmp-v1.0.pdf`; source text in the `varga-lab-handbook` repository.
