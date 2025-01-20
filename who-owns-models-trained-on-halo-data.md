---
type: Question
status: Open
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[eva-novak]]"
  - "[[halo-consortium-agreement-summary]]"
  - "[[federated-cfdna-learning]]"
_organized: true
---

# Who Owns Models Trained On Halo Data?

## Why It Matters

The consortium agreement says background IP stays with each partner and foreground IP is jointly owned, but says nothing about models trained on hub data ([[halo-consortium-agreement-summary]]). Our [[fragmentomics-classifier]] is Corvane background; if it is retrained or recalibrated on Halo data, or trained federatedly, the result may be joint foreground. [[ravi-vellanki]]'s diagnostics company has already asked whether the classifier could be licensed.

## Options

- Locked model evaluated, never retrained: stays Corvane background; only the performance numbers are joint results. Safest for the MRD manuscript.
- Recalibrated on Halo data: probably joint foreground for the recalibration.
- Federated cross-assay model: joint foreground by default.

## Current Status

[[eva-novak]] was asked at the [[halo-steering-committee-2026-09-17]] to draft a position. Ines has asked the institute grants office ([[chloe-armitage]]) to check what Corvane needs before any model leaves a site.

## What Would Settle It

A short annex to the consortium agreement, adopted by unanimity at a steering committee.
