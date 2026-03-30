---
type: Question
status: Open
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[pseudonymisation-vs-anonymisation]]"
  - "[[victor-lindahl]]"
  - "[[cfdna-fragmentomics]]"
_organized: true
---

# Is Fragment-Level cfDNA Data Personal Data?

## Why It Matters

The DPIA for the consortium clause ([[consortium-transfer-dpia-draft]]) and the minimum dataset per use depend on how identifying each layer of cfDNA data is. If per-sample fragment-length and end-motif feature tables count as low risk, we could share those more easily than reads.

## Current Answer

Partly answered. [[victor-lindahl]]'s position, which the board accepted at [[data-governance-board-2026-09-10]]:

- Reads and BAM files: personal data, and genetic data, because germline variants are recoverable even from low-pass cfDNA.
- Per-sample feature tables ([[fragment-length-and-end-motif-features]]): personal data while a key to the person exists anywhere, because they are pseudonymised, not anonymous ([[pseudonymisation-vs-anonymisation]]). Lower re-identification risk than reads, which can count in the DPIA.
- Cohort-level summaries with small-cell suppression: not personal data.

## What Remains Open

Whether per-sample feature tables could carry a genotype-like signal (for example copy-number features at germline deletion sites) that would make them re-identifiable without the key. [[sofia-reyes-calderon]] offered to test whether feature vectors can be matched across two draws of the same patient better than chance; a quick check, not yet scheduled.
