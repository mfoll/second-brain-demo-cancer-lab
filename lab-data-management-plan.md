---
type: Project
status: Completed
start: 2025-02-03
end: 2025-05-30
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[yara-castellanos]]"
  - "[[ruth-abernathy]]"
  - "[[reproducible-pipelines]]"
has:
  - "[[group-data-management-plan]]"
  - "[[dmp-approval-letter-2025]]"
  - "[[corvane-research-data-policy]]"
_organized: true
---

# Lab Data Management Plan

Writing a single data management plan for the whole group, instead of one per grant, and getting it approved by the institute data governance board.

## Outcome

Group DMP approved by the data governance board. Reached on 2025-05-27; project closed 2025-05-30.

## Current State

- Completed. The approved document is [[group-data-management-plan]] v1.0; the board's approval and two conditions are in [[dmp-approval-letter-2025]].
- Both conditions were met in 2025: an annual access review (first done 2025-12) and a named data steward per dataset, held by [[yara-castellanos]] for all clinical-linked data.
- A v1.1 revision is needed for Halyard storage and the institute cold archive; it is tracked as a next action of [[lead-tumour-evolution-group]], not by reopening this project.

## Scope and Boundaries

Covered all group data: St Aldric MRD samples, Northvale case-control samples, spatial atlas tissue data, Halo consortium data held at Corvane, and derived results. Excluded consortium-level rules, which belong to Halo, and institute policy, which we follow ([[corvane-research-data-policy]]) rather than set.

## Working Context

Why one group plan: in 2024 the group had four grant DMPs with inconsistent retention periods and three different folder layouts on Kestrel. Yara proposed one plan with grant DMPs pointing to it; the Frontier application later did exactly that.

Main decisions in v1.0:

- Three data classes: identifiable clinical (never on HPC), pseudonymised sequencing and imaging, derived and aggregate results.
- Pseudonymisation keys for Northvale samples stay with the biobank ([[paolo-ferrante]]); for St Aldric with the hospital team of [[samuel-okoye]].
- Raw sequencing retained 10 years after the last publication using it; intermediates may be deleted once reproducible from raw data and a released pipeline version.
- Access by role, reviewed yearly, with Yara as steward and Ines as accountable owner.

Drafting ran February to April with Yara, [[dmitri-halvorsen]] and [[tobias-wren]]; [[victor-lindahl]] reviewed the data protection sections. The board, chaired by [[ruth-abernathy]], approved it on 2025-05-27.

The retention rule on intermediates later made the Kestrel triage much faster: 33 TB could be deleted without debate ([[kestrel-data-inventory]]).

## Important Notes

- [[group-data-management-plan]]
- [[dmp-approval-letter-2025]]
- [[how-long-should-we-keep-raw-fastq-on-halyard]]
- [[data-tiering]]

## Maintenance Log

- 2025-05-30: Project closed.
- 2025-05-27: Approved by the data governance board with two conditions.
- 2025-04-24: Final draft sent to the board.
- 2025-02-03: Started with Yara.
