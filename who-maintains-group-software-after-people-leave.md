---
type: Question
status: Open
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[software-bus-factor]]"
  - "[[tobias-wren]]"
  - "[[felix-achterberg]]"
_organized: true
---

# Who Maintains Group Software After People Leave?

When the person who wrote a tool leaves the group, who is responsible for keeping it runnable, and for how long?

## Why It Matters

Results in published papers depend on our code. [[felix-achterberg]]'s departure in 2025-08 left the single-cell CNV code unmaintained, and [[kenji-mori]] and [[sofia-reyes-calderon]] will finish their PhDs in 2028 and 2029. [[tobias-wren]] cannot absorb every tool.

## Current Answer

Partial. The rule [[every-group-tool-needs-two-maintainers]] covers tools in active use: a second maintainer is named before the first leaves. Undecided:

- How long we keep archived tools rerunnable. Proposal: five years after the last paper that depends on them, with a container image frozen at publication.
- Whether a shared RSE post with [[nikolai-petrov]]'s team could take over archived tools. Depends on the [[aurora-programme-grant-2027]] budget.
- Whether leaving PhD students should commit to answering questions for a period. Ines thinks this is unfair to ask.

## What Would Answer It

A short section in the next [[lab-data-management-plan]] revision, agreed at a group meeting.
