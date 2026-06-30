---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1002/pds.70120
doi: 10.1002/pds.70120
pmid: "40130753"
licence: cc by
date_accessed: 2026-06-17
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[registry-linkage-variable-specification]]"
_organized: true
---

# Exploring the Complexity of Real-World Health Data Record Linkage-An Exemplary Study Linking Cancer Registry and Claims Data.

## Summary

The authors examine why record linkage based on quasi-identifiers fails when linking cancer registry data with insurance claims, and use gold-standard links to train informed linkage algorithms (deterministic, regression, tree-based and neural). A gradient-boosting approach performed best but still reached only moderate precision and recall, and discrepancies between sources explained many failures.

## Why It Matters

Read when drafting the [[registry-linkage-variable-specification]] for the 2025 extract. Northvale links on a stable pseudonymised identifier, so our situation is much better, but the paper's catalogue of discrepancy types (date transpositions, name changes, moves) is what [[daniel-asante]] checks in the registry's probabilistic step for the 412 records that failed deterministic linkage.

## Caveats

Quasi-identifier linkage without a unique key; not directly comparable to ours.

## Source Links

- [Exploring the Complexity of Real-World Health Data Record Linkage](https://doi.org/10.1002/pds.70120)
