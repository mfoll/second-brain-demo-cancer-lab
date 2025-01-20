---
type: Note
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[ch-cancer-risk-analysis]]"
  - "[[exploratory-reading-review-2026-10]]"
  - "[[lucas-brandt]]"
_organized: true
---

# Proposal: Fold Mendelian Randomization Into CH Cancer Risk Analysis

Proposal raised at the [[exploratory-reading-review-2026-10]] on 2026-10-21. Status: proposed, not approved. Nothing has been re-parented.

## Proposal

Re-parent the [[mendelian-randomization]] Topic under [[ch-cancer-risk-analysis]] and add one outcome-level item to that Project: a pre-specified two-sample MR analysis of CH and incident pancreatic and colorectal cancer, triangulated with the Northvale hazard ratios, as a follow-up analysis once the observational paper is submitted.

## What It Revisits

Ines has asked [[lucas-brandt]] to keep MR out of the current CH paper, so that the observational analysis is not delayed, and to route any MR work through this cluster first. The proposal does not reverse that: the first paper stays observational. It asks whether the follow-up MR analysis should be planned inside the same Project rather than left as reading.

## Why Now

Under [[adr/0011-root-belongs-to-at-responsibilities-and-home-exploration-clusters-in-topics|ADR 0011]] a cluster becomes Project work when it gains an outcome, actions, collaborators or a deliverable. This one has:

- An outcome: a defined follow-up analysis to the CH paper ([[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]]).
- A collaborator: [[hiroshi-tanabe]], three calls in.
- A working document: [[ch-instrument-shortlist]].
- A reason to move: [[jin-2026-chip-cancer-mendelian-randomization]] means reviewers will ask why we did not do it.

## Why Not A Separate Project

A stand-alone MR project would duplicate the cohort context and compete for Lucas's time. The MR result only has value next to the hazard ratios.

## Open Points Before Approval

- Lucas's time: the CH risk analysis is already the main thread of his postdoc. He estimates six weeks for the MR part.
- Co-authorship terms with Hiroshi.
- [[maja-kovac]] wants the analysis plan written before approval, not after.

## Decision

Pending Ines and Lucas, target 2026-11-27. If approved: re-parent the Topic, add the outcome and actions to the Project, and keep this note as the record.
