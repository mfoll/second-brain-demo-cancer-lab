---
type: Source
source_type: Internal dataset
storage_system: Group drive
root_key: group_drive
relative_path: Admin/Compute/Kestrel/kestrel-inventory-final.xlsx
access: guarded-write
last_checked: 2026-10-20
date_accessed: 2026-09-29
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[archive-kestrel-data]]"
  - "[[yara-castellanos]]"
  - "[[kestrel-retirement-2026-09-30]]"
_organized: true
---

# Kestrel Data Inventory

The spreadsheet listing every group directory on Kestrel, its owner, data class and fate (migrate, archive, delete), built by [[yara-castellanos]] and [[tobias-wren]] between June and September 2026 and signed off by Ines on 2026-09-29.

## Summary

186 TB of group data in 412 top-level directories. Fate: 41 TB migrated to Halyard project space, 112 TB written to the institute cold archive in 23 batches, 33 TB deleted.

## Key Details

- Deleted data was limited to intermediates reproducible from raw data with a released pipeline version, as the [[group-data-management-plan]] allows, plus exact duplicates found by checksum.
- 61 directories had no clear owner; 58 were resolved by asking former members, including [[felix-achterberg]] about the single-cell CNV data. Three were archived by default.
- Each archive batch has a manifest with SHA-256 checksums. Verification after retrieval of a sample of files per batch is 80% done.
- Single-cell CNV pilot data ([[single-cell-cnv-pilot]]) was archived whole because the paper may need it.

## Source Location

Group drive, `Admin/Compute/Kestrel/kestrel-inventory-final.xlsx`. Edits only by Yara or Tobias.
