---
type: Question
status: Deferred
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[northvale-health-cohort]]"
  - "[[collider-bias]]"
  - "[[maja-kovac]]"
_organized: true
---

# Does Selection Into Northvale Bias A One-Sample Mendelian Randomization?

If we ran MR using individual-level Northvale data, would voluntary enrolment and survival to enrolment bias the estimates enough to matter?

## Context

Raised by [[maja-kovac]] on 2026-02-19. The [[northvale-health-cohort]] recruited 86,400 adults aged 40 to 69 in 2004 to 2009; participants are healthier than the source population. Selection that depends on factors linked to both the instruments and cancer risk would act as [[collider-bias]].

## What We Know

- Simulations suggest bias is small unless selection effects are large ([[gkatzionis-2019-selection-bias-mendelian-randomization]]).
- Survival bias grows with age at enrolment; Northvale's upper limit of 69 helps ([[smit-2019-survival-bias-mendelian-randomization]]).
- CH is mostly invisible to participants, so direct selection on the exposure is unlikely; selection on smoking-related health is not.

## Why Deferred

The current answer to [[can-mendelian-randomization-test-ch-as-a-cause-of-cancer]] favours two-sample MR, with Northvale only as replication. If that holds, this question matters less. Revisit if a one-sample analysis is ever proposed as the main result.
