---
type: Opinion
status: Active
confidence: High
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[software-bus-factor]]"
  - "[[group-software-inventory]]"
  - "[[lead-tumour-evolution-group]]"
_organized: true
---

# Every Group Tool Needs Two Maintainers

## Stance

Any tool that a current or planned paper depends on must have two people who can run, fix and explain it, and the second one is named and trained before the first leaves.

## Scope

Group tools and pipelines in active use. Archived tools are frozen in a container at publication and exempt. Not a rule about external packages.

## Why I Think This

- The single-cell CNV code reached a [[software-bus-factor]] of zero when [[felix-achterberg]] left, and making it rerunnable cost four days of [[tobias-wren]]'s time.
- The institute survey shows we were typical, not unlucky ([[corvane-rse-survey-2025]]).
- Small labs can run real process without a software team ([[crusoe-2016-sustainable-software-small-biology-lab]]); the binding constraint is named people, not tools.
- Contract end dates are known in advance, so the risk is predictable.

## What Would Change My Mind

If maintaining two people per tool cost so much research time that projects slipped noticeably, a shared institute RSE service would be a better use of money. We would see that in the quarterly inventory review.

## Implications

- Bus factor is reviewed quarterly in [[group-software-inventory]]; it went from mostly one to mostly two between 2025-11 and 2026-10.
- New students pair with an existing maintainer on one tool in their first six months.
- [[owen-mcallister]] will be named second maintainer of the spatial pipeline when he starts.
