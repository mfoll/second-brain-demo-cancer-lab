---
type: Procedure
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[benedikt-kraus]]"
  - "[[visium-hd-pilot]]"
  - "[[atlas-tissue-manifest]]"
_organized: true
---

# Tissue Section QC

Steps to check FFPE liver metastasis blocks and sections before a Visium HD run. Written after the [[visium-hd-pilot]] lost one section to a fold and one biopsy to degraded RNA; updated after the [[atlas-tissue-review-2026-04-15]].

## Inputs

- Block list for the batch from [[atlas-tissue-manifest]], with pair IDs.
- Tissue unit request approved by [[benedikt-kraus]].

## Steps

1. Pre-sectioning H&E from the block face. Benedikt confirms the lesion, estimates viable tumour content and marks the region to place on the capture area. Reject if viable content is below 10% in a resection, unless the pair is a complete responder kept for niche analysis.
2. RNA quality: cut two scrolls, measure DV200. Pass at 30% or above. If below, cut deeper levels once and retest; if still below, flag the pair for replacement.
3. Section at 5 µm onto standard slides within 14 days of the DV200 test. Inspect under the microscope for folds, tears and bubbles over the marked region. Recut if any fault crosses it.
4. H&E stain and image at 40x before the CytAssist transfer. File images with the pair ID.
5. Log section ID, block, DV200, viable content, operator and date in the batch QC sheet.
6. Benedikt signs off the batch. Only signed batches go to the sequencing core.

## Outputs

Signed batch QC sheet, H&E images, updated manifest.

## Verification

After sequencing, compare UMIs per 8 µm bin per section with the pilot distribution ([[visium-hd-run-qc-metrics]]). A section below 100 median UMIs in tissue triggers a review of its QC record before analysis.
