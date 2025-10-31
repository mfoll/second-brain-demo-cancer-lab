---
type: Concept
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[forer-2025-nf-test-pipeline-reliability]]"
  - "[[nf-test-coverage-report-2026-08]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Snapshot Testing

A test that runs a piece of code on fixed input, stores a fingerprint of the output as the expected result, and fails whenever later output differs. The test does not say the output is correct, only that it has not changed.

## Use In Our Pipelines

Every local Nextflow module in `varga-cfdna` and most in `varga-spatial` has an nf-test snapshot test on a small input ([[forer-2025-nf-test-pipeline-reliability]]). When a snapshot changes, the merge request must explain why, and the reviewer decides whether the new output is right before the snapshot is updated.

## What It Has Caught

- A samtools update in an nf-core module that changed duplicate flags (2026-02).
- A rounding change in end-motif frequencies after a pandas upgrade (2026-08), which would have shifted [[fragmentomics-classifier]] inputs.

## Limits

- Snapshots of non-deterministic outputs (GPU segmentation, random seeds) need fixed seeds or tolerance checks instead of exact matches.
- A wrong output can be snapshotted as expected on day one. Snapshot tests protect against drift, not against initial errors; those need review and biological checks.
