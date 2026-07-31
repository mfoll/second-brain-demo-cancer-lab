---
type: Source
source_type: Internal document
date_accessed: 2026-07-21
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[request-halyard-gpu-time]]"
  - "[[halyard-gpu-partition-granted-2026-09-22]]"
  - "[[spatial-pipeline-repository]]"
_organized: true
---

# Halyard GPU Allocation Request

The group's application for access to the Halyard `gpu` partition, submitted through the research IT portal on 2026-07-21 by [[tobias-wren]] and [[amara-okonkwo]], approved on 2026-09-22.

## Summary

Requested 8,000 GPU-hours to 2027-03-31 for cell segmentation and cell-type deconvolution on Visium HD data and matched histology images in the [[colorectal-metastasis-atlas]]. Granted 6,000 GPU-hours.

## Key Details

- Estimate: 40 pre- and post-chemotherapy pairs, about 120 GPU-hours each for segmentation and deconvolution across parameter sweeps, plus 2,000 hours for the [[deconvolution-benchmark]] reruns.
- Evidence: timings from Kestrel's old GPU nodes, scaled by the expected speed-up of Halyard's newer cards.
- Named technical contact: Tobias. Scientific contact: Amara.
- Research IT reduced the grant because the benchmark reruns were judged optional; they asked us to show usage before any top-up.

## Why It Matters

The two-month wait between submission and approval is the main reason the [[halyard-cluster-migration]] slipped. The template and timings are reused in [[request-halyard-gpu-time]].

## Source Location

Research IT portal, request RIT-2026-0412; PDF copy in group drive `Admin/Compute/Halyard/gpu-request-2026.pdf`.
