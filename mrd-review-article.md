---
type: Project
status: Active
start: 2026-08-01
belongs_to: "[[tumour-evolution-research]]"
has:
  - "[[mrd-review-article-outline]]"
  - "[[mrd-review-invitation-2026-07]]"
related_to:
  - "[[minimal-residual-disease]]"
  - "[[cfdna-fragmentomics]]"
  - "[[dmitri-halvorsen]]"
_organized: true
---

# MRD Review Article

An invited review on computational methods for cfDNA minimal residual disease detection for Computational Oncology Review. Ines is lead author with [[dmitri-halvorsen|Dmitri Halvorsen]] and [[hannah-lindqvist|Hannah Lindqvist]].

## Outcome

Review submitted to Computational Oncology Review by the agreed deadline of 2027-02-26 and accepted.

## Current State

- Invitation accepted on 2026-07-29 ([[mrd-review-invitation-2026-07]]); 6,000 words, up to six figures.
- Outline v2 agreed on 2026-09-08 ([[mrd-review-article-outline]]). Five sections: signal sources, tumour-informed versus tumour-naive designs, clonal hematopoiesis, fragmentomics and batch effects, validation and reporting.
- Literature collection is in the vault: the real papers linked from [[minimal-residual-disease]] and [[cfdna-fragmentomics]] are the starting set.
- Writing has not started; the [[mrd-manuscript|MRD Manuscript]] revision has priority until December.

## Scope and Boundaries

A review of others' and our published work. It must not present unpublished St Aldric results beyond what is in the [[mrd-preprint-2026|preprint]], and must not pre-empt the external validation.

## Working Context

The angle we want: most MRD reviews compare assays; ours argues that the computational choices (CH filtering, batch handling, validation design) decide whether a reported lead time is real. The St Aldric batch story ([[batch-confounding-in-cfdna-studies]]) and the CH filter ([[clonal-hematopoiesis]]) are the worked examples. The [[external-validation-before-locking-a-classifier]] Opinion is the review's spine, so the text must state the evidence, not just the stance.

## Collaborators and Roles

- Ines: lead and corresponding author; sections 2 and 5; final edit.
- [[dmitri-halvorsen|Dmitri Halvorsen]]: section 1 and the figure on signal layers.
- [[hannah-lindqvist|Hannah Lindqvist]]: section 3 on clonal hematopoiesis; counts towards her thesis introduction.
- [[sofia-reyes-calderon|Sofia Reyes Calderon]]: co-writes section 4 with Ines.
- No external co-authors. Ines considered inviting a Halo colleague and decided against it while the validation request is pending, to keep the review independent of the consortium decision.

## Reading Plan

The starting set is already in the vault: pancreatic MRD reviews and cohorts ([[ojha-2025-ctdna-pancreatic-critical-appraisal]], [[theocharopoulos-2025-mrd-pdac-perioperative]], [[botta-2024-tumour-informed-ctdna-pdac]]), CH in plasma ([[magee-2025-cfdna-variants-tumour-or-ch-origin]], [[brown-2025-fragmentomic-variant-origin]]), calling benchmarks ([[carrie-2025-benchmarking-ctdna-mutation-calling]]), methylation ([[pharo-2025-methylation-biomarker-roadmap]]) and fragmentomics biases ([[liu-2024-reference-biases-fragmentomics]]). Each section owner adds about 20 references from their own reading, entered as Sources with a `Why It Matters` line so that the review argument and the vault stay aligned. Gaps known now: interval censoring of lead time in other studies, and how commercial MRD assays handle CH.

## Format Notes

Computational Oncology Review asks for a key-points box, a glossary and a box on open problems. The glossary can reuse the definitions in [[tumour-informed-vs-tumour-naive-mrd]], [[molecular-lead-time]] and [[panel-of-normals]], rewritten for a general computational audience. The open-problems box is where federated validation across consortia goes, without naming the Halo case.

## Next Actions

- [ ] Hannah drafts the clonal hematopoiesis section by 2026-12-11.
- [ ] Dmitri drafts the signal sources section by 2026-12-11.
- [ ] Ines writes the validation section after the manuscript revision is resubmitted.
- [ ] Figure 1 (signal layers versus tumour fraction) sketched for the January writing week.

## Open Questions

- [[what-lead-time-over-imaging-is-clinically-meaningful]]
- [[should-the-mrd-call-combine-methylation-and-fragmentomics]]

## Important Notes

- [[mrd-review-article-outline]]
- [[tumour-informed-vs-tumour-naive-mrd]]
- [[ojha-2025-ctdna-pancreatic-critical-appraisal]]

## Do Not Do Yet

> [!warning]
> Do not draft section 5 with St Aldric validation numbers until the revision is accepted; cite the preprint only, and describe our external validation as planned, not done.

## Maintenance Log

- 2026-09-08: Outline v2 agreed.
- 2026-08-01: Project started.
- 2026-07-29: Invitation accepted.
