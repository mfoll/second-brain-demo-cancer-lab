---
type: Responsibility
status: Active
related_to:
  - "[[research-culture]]"
  - "[[reproducible-pipelines]]"
  - "[[priya-raman]]"
has:
  - "[[halyard-cluster-migration]]"
  - "[[nextflow-pipeline-migration]]"
  - "[[lab-handbook]]"
  - "[[who-owns-what]]"
_organized: true
---

# Lead Tumour Evolution Group

Running the Computational Tumour Evolution Group as a team: who we hire and how they start, how we meet and decide, where our compute and data live, and how our code stays usable after the person who wrote it moves on. It has no end date; the science itself sits under [[tumour-evolution-research]].

## Scope

- Team composition, hiring, onboarding and offboarding, mentoring arrangements and the yearly retreat.
- Lab meetings and the decisions they record, across all projects.
- Compute and storage: the move from Kestrel to [[halyard-cluster]], allocations, quotas, archiving.
- Pipeline engineering and code practice: Nextflow, Apptainer, testing, code review.
- Group-level data practice: the [[group-data-management-plan]] and its day-to-day use with [[yara-castellanos]].
- Not here: grant writing ([[secure-research-funding]]), PhD supervision ([[teach-and-supervise]]), institute committee work ([[serve-corvane-institute]]).

## Current State

- Team of 14 plus a visiting PhD student; [[owen-mcallister]] joins on 2027-01-11 as the spatial-omics postdoc after [[postdoc-hiring-2026]] closed on 2026-10-09.
- Kestrel was retired on 2026-09-30 ([[kestrel-retirement-2026-09-30]]). All active pipelines now run on Halyard; the spatial pipeline only since the GPU partition was granted on 2026-09-22.
- [[nextflow-pipeline-migration]] is the main engineering effort: the cfDNA pipeline is released, the spatial pipeline is not.
- The 2027 plan from the [[group-retreat-2026]] sets four group priorities and two practice changes (mandatory review of pipeline changes, split lab meeting format).
- [[tobias-wren]] carries most pipeline and HPC knowledge; reducing that single point of failure is the main operational risk ([[software-bus-factor]]).

## Active Projects and Workflows

- [[halyard-cluster-migration]]: finish moving the methylation and CH workflows, close the Kestrel archive.
- [[nextflow-pipeline-migration]]: spatial pipeline to v1.0 with nf-test coverage.
- Fortnightly lab meetings, Thursday 10:00, format in [[lab-meeting-format]]; latest is [[lab-meeting-2026-10-22]].
- Onboarding and offboarding via [[onboard-a-new-lab-member]] and [[offboard-a-leaver]], checklist kept by [[priya-raman]].
- Completed this year: [[postdoc-hiring-2026]], [[group-retreat-2026]]. Completed in 2025: [[lab-data-management-plan]].

## Next Actions

- [ ] Prepare Owen McAllister's first month: Halyard account, desk, mentoring pair with [[amara-okonkwo]], before 2027-01-11.
- [ ] Get a second maintainer trained on each production pipeline by end of March 2027.
- [ ] Revise the group DMP for Halyard and the cold archive (v1.1), with Yara.
- [ ] Settle how research engineering time is funded after 2027 ([[how-should-research-engineering-time-be-funded]]).
- [ ] Run the first quarter of the new lab meeting format and review it at the 2027-03 operations meeting.

## Maintenance Log

- 2026-10-22: Reconciled after the retreat, Kestrel retirement and Owen's acceptance.
- 2026-09-18: Retreat closed with the 2027 research plan ([[research-plan-2027]]).
- 2026-05-06: Apptainer images built in CI chosen for Halyard ([[apptainer-decision-2026-05-06]]).
- 2025-05-30: Group DMP approved; [[lab-data-management-plan]] closed.
