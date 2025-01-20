---
type: Opinion
status: Active
confidence: Medium
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[code-review-guidelines]]"
  - "[[rokem-2024-ten-simple-rules-scientific-code-review]]"
  - "[[research-culture]]"
_organized: true
---

# Code Review In Small Labs

## Stance

In a group of our size, code review is worth its cost mainly as a way to share ownership, not as quality control. The reviewer's first job is to understand the change well enough to fix it later; finding bugs is a welcome side effect.

## Scope

Production pipelines and code whose output goes into a paper or grant. Not exploratory notebooks, and not a gate on students trying things.

## Why I Think This

- The 2026 survey showed that pipeline knowledge sat with one person ([[software-bus-factor]]). Review is the cheapest regular way to spread it.
- The bugs that hurt us most were scientific, not technical: the batch leakage in the classifier was caught by a question at a lab meeting, not a code reviewer ([[lab-meeting-2026-03-12]]). Domain review matters as much as code review ([[rokem-2024-ten-simple-rules-scientific-code-review]]).
- Small, frequent reviews take minutes; large, rare reviews get skimmed.

## What Would Change My Mind

If after six months reviews are mostly rubber stamps, or if median review time exceeds three working days and stalls students, the rule needs changing, perhaps to review by pairing instead.

## Implications

- Rotate reviewers so that juniors review seniors' code too.
- Keep merge requests small; split method changes from dependency updates.
- See [[should-we-require-code-review-for-all-pipeline-changes]] for the analysis-code question.
