---
type: Event
date: 2026-09-10
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[ruth-abernathy]]"
  - "[[victor-lindahl]]"
  - "[[data-access-policy-draft-3]]"
  - "[[halo-cross-site-benchmark]]"
_organized: true
---

# Data Governance Board 2026-09-10

Regular board meeting, chaired by [[ruth-abernathy]]. The main item for us was [[data-access-policy-draft-3]], which adds the consortium transfer clause. The board discussed it for about fifty minutes and did not adopt it. It returns at the next board on 2026-11-12.

## At a Glance

> [!info]
> Support for the principle of consortium transfer, no adoption yet: the board wants a completed DPIA covering receiving sites, the registry's written position on onward transfer of linked outcomes, and tighter wording on deletion at the end of a project.

## Attendees

[[ruth-abernathy]] (chair), [[victor-lindahl]] (data protection officer), [[helena-strom]] (ethics committee secretary, observer), [[paolo-ferrante]] (biobank), [[yara-castellanos]] (for data stewardship, presenting the data flow), Ines (drafting member, declared interest), two other group leaders and the head of research IT. [[margarethe-sell]] joined for the last item.

## Discussion

- Ines presented the problem: six Halo sites, a shared [[halo-truth-set]], and fifteen bilateral agreements under the current policy ([[corvane-data-access-policy-2023]]). She said plainly that her own group is the first beneficiary, through the [[halo-cross-site-benchmark]] and the external validation asked for the [[mrd-manuscript]]. Ruth recorded the interest; Ines did not vote.
- Victor said the consortium clause is acceptable in principle, but the DPIA outline ([[consortium-transfer-dpia-draft]]) does not yet assess the receiving sites' environments. He also noted that pseudonymised fragment-level data is personal data and cannot be treated as anonymous; see [[is-fragment-level-cfdna-data-personal-data]].
- Helena asked whether the St Aldric consent wording (sharing with "academic collaborators under a data transfer agreement") covers multi-site pooling. Her reading was yes for pseudonymised data, but she wants the ethics committee to note it formally.
- Paolo asked that the clause exclude physical samples. Agreed: the clause covers data only; samples stay under the material transfer process.
- A group leader asked whether federated analysis would avoid the need for the clause. Ines answered that it helps for model training ([[federated-cfdna-learning]]) but not for a locked-model validation the journal will audit. Not everyone was convinced; see [[should-halo-validation-run-federated-instead-of-transfer]].
- Registry-derived outcomes: the board will not approve a clause that might conflict with the [[registry-linkage-agreement]]. It needs [[daniel-asante]]'s confirmation of what the registry will allow.

## Decisions

- Not adopted. Re-table at the board on 2026-11-12.
- Deletion wording to be tightened: data deleted at all receiving sites within 90 days of project end, with written confirmation.
- Samples explicitly out of scope of the clause.

## Actions

- Victor: complete DPIA section on receiving sites, with Yara and Ines.
- Ines: draft 4 by 2026-10-29; request the registry's written position.
- Helena: ethics committee note on St Aldric consent scope.

## Consequences

Halo patient-tier data cannot come to Corvane, and St Aldric data cannot go to Brightwater, until at least mid-November. The MRD manuscript revision deadline is 2027-01-29; the plan assumes adoption on 2026-11-12 and countersignature of the Halo agreement by mid-December, which leaves about six weeks for the validation analysis. The federated fallback discussed at [[mrd-revision-planning-2026-07-21]] remains plan B.
