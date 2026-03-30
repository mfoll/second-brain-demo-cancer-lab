---
type: Source
source_type: Governed dataset
storage_system: Corvane governed research storage
root_key: corvane_governed
relative_path: atlas/pathology/annotations/
access: guarded-write
last_checked: 2026-10-07
date_accessed: 2026-03-20
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[benedikt-kraus]]"
  - "[[pathologist-annotations-anchor-spatial-clusters]]"
_organized: true
---

# Atlas Pathology Annotations

Region annotations drawn by [[benedikt-kraus]] on the H&E image of every atlas section: viable tumour, invasive margin, fibrotic capsule, necrosis, mucin, adjacent liver, and artefacts to exclude. Exported as polygons registered to Visium HD coordinates.

## Key Details

- 52 sections annotated (batches 1 and 2); batch 3 in progress.
- Annotation schema v2 (2026-03) added "damaged hepatocytes" after the pilot showed a distinct expression zone at the margin.
- Loaded before clustering in the spatial pipeline, per [[pathologist-annotations-anchor-spatial-clusters]].

## Source Location

Governed storage, `corvane_governed` root, `atlas/pathology/annotations/`.
