---
type: Question
status: Answered
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[liver-metastasis-scrna-reference]]"
  - "[[hasan-2026-visium-hd-human-liver]]"
_organized: true
---

# Which Reference For Liver Metastasis Deconvolution?

Which single-cell reference should the benchmark and the atlas use to define cell types in colorectal liver metastases?

## Current Answer

A combined reference built in-house from public colorectal cancer and normal liver single-cell datasets, harmonised to 14 cell types, with cancer cells from colorectal primaries and metastases ([[liver-metastasis-scrna-reference]]). Accepted 2025-11-14 at the benchmark freeze.

## Why

- No single public dataset covered tumour, liver parenchyma and treated stroma.
- Missing cell types hurt every method in our tests; damaged hepatocytes and activated stellate cells needed explicit categories.
- The benchmark tests reference mismatch separately by removing one cell type at a time.

## Remaining Caveat

None of the source datasets is from chemotherapy-treated tissue. If a treated-tissue reference appears, rerun the atlas deconvolution with it. The Visium HD liver map in [[hasan-2026-visium-hd-human-liver]] is a useful check on normal-liver cell-type positions but is not a single-cell reference.
