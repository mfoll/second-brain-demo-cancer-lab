---
type: Project
status: Idea
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[arjun-mehta]]"
  - "[[data-access-policy-revision]]"
  - "[[fragmentomics-classifier]]"
has:
  - "[[federated-cfdna-learning-concept-note]]"
  - "[[federated-learning]]"
  - "[[can-federated-training-match-a-pooled-classifier]]"
  - "[[who-owns-models-trained-on-halo-data]]"
_organized: true
---

# Federated cfDNA Learning

A proposal to train and evaluate cfDNA models across the Halo sites without moving patient-level data: each site runs the same code on its own data and only model parameters or aggregate metrics leave. It answers one constraint directly: pseudonymised data cannot leave Corvane, or come in, until the revised institute data access policy covers consortium transfer ([[data-access-policy-revision]]).

## Outcome

A costed proposal accepted by the Halo steering committee, with a pilot plan for (a) federated evaluation of the locked [[fragmentomics-classifier]] on the patient tier of the [[halo-truth-set]], and (b) federated training of a cross-assay model. Done when the steering committee accepts or rejects it.

## Current State

- Idea. Raised by [[arjun-mehta]] at the [[halo-steering-committee-2026-09-17]] after the [[data-governance-board-2026-09-10]] did not adopt the consortium transfer clause.
- First draft of the concept note exists ([[federated-cfdna-learning-concept-note]]), written by Arjun and Ines, with input from [[leila-farouk]] on running the classifier at Thornvale.
- [[victor-lindahl]] has not yet said whether model weights trained on St Aldric data count as personal data under institute rules. Until he does, even the federated route may need the policy.
- Tooling not chosen. Candidates: [[flower-federated-learning-framework]] and the FeatureCloud stack ([[featurecloud-platform]], [[weilguny-2026-fedflow-featurecloud]]).

## Scope and Boundaries

In scope: the proposal, a pilot design, legal questions that decide whether it is worth doing. Out of scope: lobbying for the policy itself, which is [[data-access-policy-revision]] under [[serve-corvane-institute]]. This is not a way around the policy; if Victor or the board says weights are personal data, we wait like everyone else.

## Working Context

Federated evaluation is the cheap half: send a locked model in an Apptainer image to Brightwater, run it on the patient-tier sequencing data there, and get back a confusion matrix and ROC curve. It is plan B for the [[mrd-manuscript]] if the board does not adopt the clause on 2026-11-12, but Ines does not see it as a substitute for the transfer clause: a journal-audited validation needs calibration plots built from per-patient predictions, and those are personal data too. The arguments are kept in [[should-halo-validation-run-federated-instead-of-transfer]]; the status of feature tables and predictions in [[is-fragment-level-cfdna-data-personal-data]]. Where federation is genuinely useful is training and exploration across sites, which no transfer clause will make easy because every site has its own approvals. That is harder: six assays produce different features, so a shared model needs a common feature layer, and with 60 patient samples split across sites the gain over local models is doubtful ([[can-federated-training-match-a-pooled-classifier]]). Literature we leaned on: [[ay-2026-privacy-enhancing-technologies-biomedical-ai]] for leakage risks, [[saldanha-2025-swarm-learning-surgical-video]] for a multicentre case where decentralised training matched pooled training. See [[federated-learning]] for the concept.

## Next Actions

- [ ] Get Victor's written view on whether weights and aggregate metrics leaving Corvane need the revised policy.
- [ ] Cost a federated-evaluation pilot with [[ngozi-adeyemi]] and [[tobias-wren]] (compute at Brightwater, container build in our CI).
- [ ] Present the concept note at the next steering committee.
- [ ] Agree with [[eva-novak]] on ownership of jointly trained models.

## Open Questions

- [[can-federated-training-match-a-pooled-classifier]]
- [[who-owns-models-trained-on-halo-data]]
- [[should-halo-validation-run-federated-instead-of-transfer]]

## Important Notes

- [[federated-cfdna-learning-concept-note]]
- [[halo-data-flow-and-transfer-constraints]]
- [[federated-learning]]

## Maintenance Log

- 2026-10-14: Concept note draft v0.3 shared with Arjun and Sun-hee.
- 2026-09-17: Idea raised at the steering committee; Ines and Arjun asked to write it up.
- 2026-09-01: Project note opened after informal discussion with Arjun.
