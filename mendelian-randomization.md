---
type: Topic
belongs_to: "[[exploratory-reading]]"
related_to:
  - "[[molecular-epidemiology]]"
  - "[[ch-cancer-risk-analysis]]"
  - "[[hiroshi-tanabe]]"
  - "[[lucas-brandt]]"
has:
  - "[[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]]"
  - "[[proposal-fold-mendelian-randomization-into-ch-cancer-risk-analysis]]"
  - "[[instrumental-variable-assumptions]]"
  - "[[burgess-2019-guidelines-mendelian-randomization]]"
_organized: true
---

# Mendelian Randomization

Exploration cluster on Mendelian randomization (MR): using germline variants as instruments to ask whether an exposure causes an outcome. It started as background reading for [[ch-cancer-risk-analysis]] in October 2025 and has grown into the cluster closest to becoming real work.

## Why We Are Reading This

The CH risk analysis estimates hazard ratios of incident solid cancers for clonal hematopoiesis at baseline in 6,000 Northvale participants. Those are associations. Reviewers will ask the obvious question: is CH a cause, a marker of shared ageing and smoking, or an early sign of the cancer itself (see [[reverse-causation-in-prediagnostic-studies]])? Published germline predisposition loci for CH make an MR analysis possible in principle, and [[lucas-brandt]] has the genotype data for the subcohort. The central open question is [[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]].

## What We Have Learned So Far

- The method rests on three assumptions, and the third one (no path from instrument to outcome except through the exposure) is where CH gets difficult: [[instrumental-variable-assumptions]], [[pleiotropy]].
- Germline variants that predispose to CH often sit in genes that also affect cancer risk directly, which is a textbook pleiotropy problem ([[liu-2025-germline-variation-clonal-hematopoiesis]]).
- A published two-sample MR of CHIP and 18 cancers exists ([[jin-2026-chip-cancer-mendelian-randomization]], filed under the CH risk analysis because Lucas reads it as context for that paper). It gives us a comparison point but uses consortia we cannot replicate in Northvale.
- Selection and survival in an older cohort can bias estimates ([[gkatzionis-2019-selection-bias-mendelian-randomization]], [[smit-2019-survival-bias-mendelian-randomization]], [[collider-bias]]); Northvale recruited adults aged 40 to 69, so this matters less than in elderly cohorts but is not zero.
- Robust methods move quickly: [[grant-2024-bayesian-mendelian-randomization-correlated-pleiotropy]], [[tang-2025-pleiotropic-clustering-mendelian-randomization]] and [[van-der-graaf-2025-mr-link-2]] are the ones [[hiroshi-tanabe]] recommended we read first.
- For reporting, [[burgess-2019-guidelines-mendelian-randomization]] is our checklist.

Ines's working stance is in [[mendelian-randomization-is-triangulation-not-a-verdict]].

## People

- [[hiroshi-tanabe]], external methodologist, has offered to advise on instrument choice and sensitivity analyses.
- [[lucas-brandt]] leads the CH risk analysis and would run any MR.
- [[maja-kovac]] reviews the epidemiology and has reservations about the instrument strength (see [[does-selection-into-northvale-bias-a-one-sample-mendelian-randomization]]).

## Notes In This Cluster

Sources: [[burgess-2019-guidelines-mendelian-randomization]], [[coscia-2022-collider-bias-stratified-mendelian-randomization]], [[gkatzionis-2019-selection-bias-mendelian-randomization]], [[smit-2019-survival-bias-mendelian-randomization]], [[grant-2024-bayesian-mendelian-randomization-correlated-pleiotropy]], [[tang-2025-pleiotropic-clustering-mendelian-randomization]], [[van-der-graaf-2025-mr-link-2]], [[larsson-2025-alcohol-cancer-mendelian-randomization]], [[liu-2025-germline-variation-clonal-hematopoiesis]], [[wang-2025-methylation-pancreatic-cancer-mendelian-randomization]], [[mr-reading-list-hiroshi-tanabe]], [[ch-instrument-shortlist]].

Concepts: [[instrumental-variable-assumptions]], [[pleiotropy]], [[collider-bias]].

Questions: [[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]], [[does-selection-into-northvale-bias-a-one-sample-mendelian-randomization]].

Retired: [[mr-reading-group-proposal-2025]].

## Promotion Status

> [!info]
> This cluster now has an outcome (a follow-up MR analysis to the CH risk paper, which itself stays observational), a collaborator and a dataset, so under ADR 0011 it should become Project work; the proposal to fold it into ch-cancer-risk-analysis is written but not yet approved.

The proposal is [[proposal-fold-mendelian-randomization-into-ch-cancer-risk-analysis]], raised at the [[exploratory-reading-review-2026-10]]. If approved, this Topic is re-parented under [[ch-cancer-risk-analysis]] and its notes follow. Until then it stays under [[exploratory-reading]].
