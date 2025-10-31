---
type: Question
status: Open
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[code-review-guidelines]]"
  - "[[code-review-in-small-labs]]"
  - "[[rokem-2024-ten-simple-rules-scientific-code-review]]"
_organized: true
---

# Should We Require Code Review For All Pipeline Changes?

## Question

The retreat made review mandatory for every change to the two production pipelines. Should the same rule apply to analysis code in project repositories (classifier training, survival models, figure scripts), and if so, at what threshold?

## Current Answer

> [!info]
> Pipelines: yes, adopted on 2026-10-08. Analysis code: not yet. Working rule until December is review before any result goes into a manuscript or a grant, not for every commit.

## Considerations

- For: analysis code is where the 2026 batch problem in the [[fragmentomics-classifier]] was caught, by a person other than the author asking the right question ([[lab-meeting-2026-03-12]]).
- Against: 14 people and one engineer; mandatory review of every analysis commit would stall students, and reviewers with the domain knowledge are the same few people.
- [[nikolai-petrov]]'s review club offers outside reviewers for larger changes.

## Next Step

Review after three months of the pipeline rule: count of merge requests, median time to review, and whether anything was caught. Decide at the first operations block of January 2027.
