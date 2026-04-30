---
type: Procedure
status: Active
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[kestrel-data-inventory]]"
  - "[[yara-castellanos]]"
  - "[[data-tiering]]"
_organized: true
---

# Archive Kestrel Data

How the group moved Kestrel data to the institute cold archive before the 2026-09-30 retirement, and how to finish verification. Written by [[yara-castellanos]] and [[tobias-wren]]. Reusable for any future move to cold storage.

## Steps

1. **Inventory.** List every top-level directory with size, owner, data class and proposed fate (migrate, archive, delete) in the [[kestrel-data-inventory]].
2. **Resolve owners.** Ask current members, then former members through Ines. Unresolved after two reminders: archive by default, never delete.
3. **Delete only what the DMP allows.** Intermediates reproducible from raw data with a released pipeline, and exact duplicates by checksum ([[group-data-management-plan]]).
4. **Batch.** Group archive data into batches of at most 10 TB by project. Generate a manifest with SHA-256 checksums per file.
5. **Transfer.** Use the research IT archive tool from the transfer node; record batch ID and date in the inventory.
6. **Verify.** For each batch, retrieve a random 1% of files (at least 20) and compare checksums. Record the result in the inventory.
7. **Sign-off.** The accountable owner (Ines) signs the inventory once every row has a fate and transfer date.

## Current State

All 23 batches transferred before 2026-09-30. Verification done for 18 of 23 batches (about 80%); remaining five expected by mid-November.

## Guardrails

> [!warning]
> Do not delete the staging copy of a batch until its verification result is recorded, even if storage is tight.
