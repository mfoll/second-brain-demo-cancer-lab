---
type: Note
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[code-review-in-small-labs]]"
  - "[[rokem-2024-ten-simple-rules-scientific-code-review]]"
  - "[[who-owns-what]]"
_organized: true
---

# Code Review Guidelines

Rules for reviewing changes to the group's production pipelines, in force since 2026-10-08. Adopted at the [[group-retreat-2026]].

## The Rule

Every merge request to `varga-cfdna` or `varga-spatial` needs approval from one person other than the author before merging. The reviewer comes from the weekly rota in [[who-owns-what]].

## For Authors

- Keep merge requests small: one method change or one dependency update, never both.
- Explain why, not only what. Link the issue or lab meeting decision.
- If a snapshot test changed, say why the new output is right ([[snapshot-testing]]).

## For Reviewers

- Aim to review within two working days; say so if you cannot.
- First understand the change well enough to fix it later. Ask questions; questions are a good review.
- Check that the change matches the scientific intent, not only that the code runs.
- Approve when you would be comfortable maintaining it.

## Not Covered

Analysis code outside the pipelines is not yet under this rule; see [[should-we-require-code-review-for-all-pipeline-changes]].
