---
type: Source
source_type: Dataset manifest
date_accessed: 2026-05-20
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[halo-truth-set]]"
  - "[[halo-truth-set-shipment-2026-05-19]]"
  - "[[elias-moreau]]"
_organized: true
---

# Halo Truth Set Shipment Manifest

The manifest for Corvane's box of the [[halo-truth-set]], received 2026-05-20. One row per aliquot: blinded sample code, tube barcode, nominal volume or DNA mass, tier flag withheld, box position.

## Key Details

- 120 rows; tier is not shown, but the contrived tier is recognisable by DNA mass (20 ng) rather than plasma volume, which the blinding rules accept as unavoidable ([[halo-truth-set-blinding-and-unblinding-rules]]).
- [[elias-moreau]] signed the receipt with two smudged labels resolved by barcode; logger file attached.
- Our run sheet maps each blinded code to the sequencing batch (batch 1: 64 samples, 2026-06-15; batch 2: 56 samples, 2026-07-13).

## Caveats

The manifest is not the key. Do not try to infer tiers beyond what the blinding rules accept.

## Source Location

Governed storage, `corvane_governed`, `halo/truth-set/manifest-corvane-2026-05-20.csv`; paper receipt in the wet-lab sample log.
