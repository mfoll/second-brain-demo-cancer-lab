---
type: Question
status: Open
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[ch-cancer-risk-analysis]]"
  - "[[clonal-hematopoiesis]]"
  - "[[hiroshi-tanabe]]"
  - "[[lucas-brandt]]"
_organized: true
---

# Can Mendelian Randomization Test CH As A Cause Of Cancer?

Can a Mendelian randomization analysis tell us whether clonal hematopoiesis causes incident solid cancers, rather than marking shared ageing, smoking or early disease, well enough to complement the [[ch-cancer-risk-analysis]] results?

## Why It Matters

The CH risk analysis will report hazard ratios for CH at baseline in 6,000 Northvale participants, adjusted for smoking and age. Reviewers will ask about causality and about [[reverse-causation-in-prediagnostic-studies]]. A credible MR would add an independent line of evidence; a weak one would invite criticism we could have avoided.

## Current Answer

> [!info]
> Probably yes as a sensitivity analysis, probably no as a stand-alone test: instruments are weak and pleiotropy is likely, so the realistic design is two-sample MR from public summary statistics, triangulated with the Northvale hazard ratios.

Reasons, from the three calls with [[hiroshi-tanabe]] and [[lucas-brandt]]'s work:

- Of 31 candidate instruments, 12 are flagged for likely direct effects on cancer ([[ch-instrument-shortlist]], [[pleiotropy]]).
- One-sample MR in 6,000 people is underpowered for single cancer sites; Northvale is better used as replication.
- A two-sample MR of CHIP and 18 cancers already exists ([[jin-2026-chip-cancer-mendelian-randomization]]), so the novelty would lie in triangulation and pleiotropy-robust methods, not in running MR at all.
- Driver-specific predisposition ([[liu-2025-germline-variation-clonal-hematopoiesis]]) suggests separate analyses for DNMT3A and TET2 CH.

## What Would Answer It

A pre-registered analysis plan reviewed by Hiroshi, then a pilot two-sample analysis for pancreatic and colorectal cancer with at least three robust methods. If the methods disagree strongly, we report MR as inconclusive and keep it in the supplement.

## Next Step

The current CH paper stays observational; Ines asked [[lucas-brandt]] to keep MR out of it. Whether a follow-up MR is planned inside that Project depends on [[proposal-fold-mendelian-randomization-into-ch-cancer-risk-analysis]]. Until then, no estimates are computed.
