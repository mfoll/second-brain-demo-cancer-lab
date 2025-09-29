---
type: Source
source_type: Dataset
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/biobank/manifest-2025-09-23.csv
access: guarded-write
last_checked: 2025-10-17
date_accessed: 2025-09-23
belongs_to: "[[case-control-sample-selection]]"
related_to:
  - "[[northvale-sample-shipment-2025-09-23]]"
  - "[[corvane-biobank]]"
_organized: true
---

# Northvale Aliquot Manifest 2025

## Summary

The biobank's shipment manifest for the Northvale plasma aliquots, one row per straw pair, with biobank sample identifier, box and position, volume, freezer history code and blood-draw date. Delivered with the shipment on 2025-09-23 and reconciled against the [[northvale-sample-selection-log]] by [[elias-moreau]] and [[priya-raman]].

## Key Details

- 1,244 rows: 1,230 primary aliquots and 14 spares.
- Reconciliation on 2025-10-17: all 1,230 primary aliquots present; two box-position swaps corrected by barcode; one straw pair with visible haemolysis flagged and kept.
- Freezer history codes record two freezer moves (2011 and 2018) for about 40% of samples; these feed the storage-time sensitivity analysis ([[northvale-storage-time-qc-report]]).

## Source Location

Governed storage on [[halyard-cluster]], `halyard_governed/northvale/biobank/`.
