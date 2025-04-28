---
type: Source
source_type: Governed dataset
storage_system: Corvane governed research storage
root_key: corvane_governed
relative_path: atlas/tissue/manifest/
access: guarded-write
last_checked: 2026-10-07
date_accessed: 2025-04-02
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[benedikt-kraus]]"
  - "[[tissue-section-qc]]"
  - "[[atlas-sequencing-batch-plan]]"
_organized: true
---

# Atlas Tissue Manifest

The controlled list of the 40 metastasis pairs in the [[colorectal-metastasis-atlas]]: pseudonymised pair ID, block IDs for the pre-chemotherapy biopsy and the resection, year of resection, batch, QC outcome and replacement history. First version 2025-04-02, current version v7 (2026-10-07).

## Summary

- 40 pairs from 36 patients (four patients contribute two metastases each), Westmere Cancer Centre archive, resections 2019 to 2024.
- Two reserve pairs; one was used on 2026-04-15 to replace a pair whose biopsy failed RNA QC ([[atlas-tissue-review-2026-04-15]]).
- Every change is logged with date, reason and who approved it.

## Caveats

Pseudonym key held by the tissue unit only. The vault never stores block IDs or patient identifiers.

## Source Location

Governed storage, `corvane_governed` root, `atlas/tissue/manifest/`. Read access for atlas members; writes only by [[amara-okonkwo]] after Benedikt's sign-off.
