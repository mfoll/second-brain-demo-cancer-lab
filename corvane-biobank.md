---
type: Source
source_type: Institute resource
storage_system: Corvane biobank LIMS
root_key: corvane_biobank
relative_path: requests/varga-group/
access: guarded-write
date_accessed: 2025-03-10
last_checked: 2026-10-02
belongs_to: "[[serve-corvane-institute]]"
related_to:
  - "[[paolo-ferrante]]"
  - "[[northvale-health-cohort]]"
  - "[[case-control-sample-selection]]"
  - "[[biobank-material-request-form]]"
_organized: true
---

# Corvane Biobank

## Summary

The institute biobank holds the baseline plasma and buffy coat of the Northvale Health Cohort (86,400 adults recruited 2004 to 2009) and the serial post-surgery plasma of the St Aldric MRD study. [[paolo-ferrante]] is the manager and the named custodian of the Northvale samples. The group is its heaviest user since 2025: the 1,230 case-control samples for the [[northvale-early-detection-study]], 6,000 buffy coat DNA extracts for the [[ch-cancer-risk-analysis]], and St Aldric aliquots for the [[pancreatic-cfdna-mrd-study]].

## Why It Matters

Sample retrieval rules shape study design more than people expect. The one-aliquot rule is why the Northvale lead-time analysis uses a single targeted methylation assay rather than two platforms, and the storage-time record is the input for the storage sensitivity analysis in [[lead-time-analysis]]. Any request for Northvale material needs board approval; St Aldric material is governed by the MRD study protocol and only needs custodian sign-off.

## Key Details

- Storage: plasma in 0.5 mL aliquots at minus 80 °C; buffy coat in 1 mL straws in vapour-phase nitrogen. Northvale has four plasma aliquots per participant at baseline; about 11% of participants are down to their last one.
- Retrieval rules for Northvale: one plasma aliquot per participant per project unless the board approves more; the last aliquot is never released without explicit board approval; requests go through the [[biobank-material-request-form]] and the [[data-governance-board-membership|data governance board]].
- Thaw log: every freeze-thaw is logged. Samples with more than one prior thaw are flagged and analysed as a covariate.
- Turnaround: retrievals are batched monthly, up to 600 aliquots per batch. The case-control retrieval ran in three batches between July and October 2025.
- Cost recovery: 6 EUR per aliquot retrieved, 14 EUR per DNA extraction from buffy coat.
- Data returned with samples: biobank ID, draw date, processing delay category (under 2 h, 2 to 6 h, over 6 h), thaw count. Linkage to cohort data uses the Northvale study ID, held by [[mei-lin-zhou]]'s team, never the biobank ID alone.

## Caveats

Processing delay is recorded in categories only, and about 4% of Northvale samples have it missing. St Aldric plasma from 2023 was processed at the hospital, not at the institute; its pre-analytics differ and are documented in [[st-aldric-mrd-cohort]].

## Source Location

Biobank LIMS, project folder `requests/varga-group/` under root key `corvane_biobank`. Read access through Paolo's team; the group never writes to it directly.
