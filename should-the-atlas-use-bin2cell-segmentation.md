---
type: Question
status: Open
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[visium-hd-bin-size]]"
  - "[[polanski-2024-bin2cell]]"
  - "[[amara-okonkwo]]"
_organized: true
---

# Should The Atlas Use Bin2cell Segmentation?

Should reconstructed cells from bin2cell replace 8 µm bins as the main analysis unit of the atlas, or stay a secondary layer?

## Why It Matters

Cells are the natural unit for clone and niche questions, and segmented cells avoid mixing tumour and stroma at boundaries. But segmentation quality varies with section quality, and the pre-chemotherapy core biopsies often have crush artefact.

## Current Answer

Provisional: 8 µm bins stay the main unit ([[visium-hd-pilot-decision-2025-08-28]]). Segmentation runs for every section since the Halyard GPU partition became available on 2026-09-22 and is used for the invasive-margin analysis only.

## Evidence So Far

- Pilot: good segmentation on four resections, patchy on two of three biopsies ([[visium-hd-pilot-report]]).
- Batch 1 and 2: Amara is scoring segmentation quality per section against H&E; 41 of 52 sections pass so far.

## What Would Settle It

If at least 70 of 80 sections pass segmentation QC and cell-level results agree with bin-level results on the margin analysis, switch. Decide at the analysis-set freeze.
