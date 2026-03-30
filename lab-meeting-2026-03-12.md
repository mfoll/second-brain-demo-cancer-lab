---
type: Event
date: 2026-03-12
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[fragmentomics-classifier]]"
  - "[[sofia-reyes-calderon]]"
  - "[[st-aldric-mrd-cohort]]"
_organized: true
---

# Lab Meeting 2026-03-12

Fortnightly lab meeting, Thursday 10:00 to 11:40, seminar room 2. Present: Ines Varga (chair), [[dmitri-halvorsen]], [[sofia-reyes-calderon]], [[amara-okonkwo]], [[lucas-brandt]], [[maja-kovac]], [[kenji-mori]], [[hannah-lindqvist]], [[tobias-wren]], [[priya-raman]] (notes), [[elias-moreau]], [[leila-farouk]]. Apologies: [[yara-castellanos]].

## At a Glance

> [!note]
> Decided to replace the gradient-boosting fragmentomics classifier with a regularised logistic regression model, because the boosted model overfitted batch effects in the St Aldric samples. Sofia owns the refit; the classifier stays unlocked until the new model passes the batch checks.

## Fragmentomics Classifier

Sofia presented the batch analysis she ran after the February cross-validation looked too good. The gradient-boosting model ([[fragmentomics-classifier]]) reached a cross-validated AUC of 0.91 within batches on the St Aldric training set, but only 0.74 under leave-batch-out folds. Feature importance was dominated by a handful of fragment-length bins near the modal length. The extraction kit lot changed on 2025-06-16 ([[extraction-kit-lot-change-2025-06-16]]): most pre-operative samples in the [[st-aldric-mrd-cohort]] were extracted before the change and most follow-up samples after it, and the new lot shifted the modal fragment length by about 3 bp. Batch and label were confounded, so the model could learn the batch.

Discussion:

- Dmitri argued that leave-batch-out cross-validation is the honest estimate and should become the default for every cfDNA model.
- Lucas suggested ComBat-style correction before boosting. Rejected for now: with 212 patients and time point confounded with batch, correction risks removing real signal and is hard to defend to reviewers.
- Tobias noted that extraction batch can be carried through the pipeline sample sheet from `varga-cfdna` v0.9, so leave-batch-out folds are cheap to run.
- Ines asked whether a simpler model would hold up under leave-batch-out folds. Sofia had a quick L2-regularised logistic regression on the same [[fragment-length-and-end-motif-features]]: AUC 0.80 within batches and 0.78 leave-batch-out, a much smaller gap.

## Decisions

- Replace gradient boosting with regularised logistic regression in the fragmentomics classifier. Reason: the boosted model overfitted St Aldric batch effects; the logistic model loses far less under leave-batch-out validation and is easier to explain in the [[mrd-manuscript]].
- Leave-batch-out cross-validation becomes the reported validation for all cfDNA classifiers. Dmitri to add it to the group's analysis checklist.
- The classifier stays unlocked. No locked model until the refit passes leave-batch-out folds and a check on Halo samples from the [[halo-cross-site-benchmark]].

## Other Items

- [[lead-time-analysis]] started on 2026-03-02; Maja showed the storage-time distribution of Northvale samples. No decisions.
- Amara: atlas batch 2 sections booked with the sequencing core for April.
- Priya: Halyard accounts opening from April; Tobias will run a migration briefing at the next meeting.

## Actions

- Sofia: refit with elastic-net logistic regression, report leave-batch-out and within-batch AUC, by 2026-04-02.
- Dmitri: leave-batch-out validation into the checklist, by 2026-03-26.
- Tobias: expose extraction batch as a column in the classifier input table. See also [[batch-confounding-in-cfdna-studies]].
