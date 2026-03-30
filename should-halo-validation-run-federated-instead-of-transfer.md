---
type: Question
status: Open
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[federated-cfdna-learning]]"
  - "[[mrd-manuscript]]"
  - "[[federated-analysis-is-not-a-substitute-for-a-transfer-clause]]"
_organized: true
---

# Should Halo Validation Run Federated Instead Of Transfer?

## Why It Matters

Raised by a board member at [[data-governance-board-2026-09-10]]. If the locked classifier could be run at each Halo site and only performance metrics returned, Corvane would need no outbound transfer, and the [[mrd-manuscript]] revision would not depend on the November board.

## Arguments So Far

- For: no person-level data leaves any site; aligns with the [[federated-cfdna-learning]] idea; the Halo sites already run the same Nextflow pipeline version.
- Against: the validation set should include St Aldric as well as the Halo sites for a pooled estimate, which a federated set-up handles only with extra work. Reviewers will want to see that preprocessing was identical, and auditing five remote runs is harder than one. Calibration plots and decision curves need per-patient predictions, which are themselves personal data.
- Mixed: [[victor-lindahl]] sees federated runs as lower risk but notes that per-patient predictions returned to Corvane would still need a basis at the sending sites.

## Current Lean

Ines's working stance is in [[federated-analysis-is-not-a-substitute-for-a-transfer-clause]]: keep the transfer route as the plan, and prepare a federated fallback (metrics only) in case adoption slips past November. This matches plan B from [[mrd-revision-planning-2026-07-21]], in which [[arjun-mehta]]'s sites run our container. [[dmitri-halvorsen]] estimates two weeks to package the locked model for remote execution.

## What Would Settle It

Adoption timing at the 2026-11-12 board, and whether [[clara-hoffmann]] would accept federated metrics as external validation.
