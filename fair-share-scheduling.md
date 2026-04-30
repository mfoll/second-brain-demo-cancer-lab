---
type: Concept
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-cluster]]"
  - "[[run-the-cfdna-pipeline-on-halyard]]"
_organized: true
---

# Fair-Share Scheduling

The Slurm policy that lowers a group's job priority the more compute it has used recently, so that heavy users do not starve light ones. Halyard uses it on all partitions; Kestrel used simple first-in, first-out queues.

## What It Means For Us

- Priority depends on the group's usage over a decaying window (on Halyard, a half-life of 14 days), not on the individual. One person's large rerun lowers everyone's priority for about two weeks.
- After the cfDNA reprocessing for the [[mrd-manuscript]] revision in August, the group's pending jobs waited up to 20 hours; small test jobs were caught behind.
- GPU usage has its own share within the `gpu` partition, so spatial runs do not affect cfDNA priority ([[halyard-gpu-partition-granted-2026-09-22]]).

## Practice

- Announce reruns over 20,000 core-hours at the lab meeting operations block, so others can plan around the priority drop.
- Use the `test` profile and short partitions for development; they carry the same share but finish before priority matters.
- Check the group's standing with `sshare -A varga` before launching a large batch ([[run-the-cfdna-pipeline-on-halyard]]).

## Caveat

The half-life and weights are set by research IT and may change; [[halyard-user-guide]] v1.4 is expected to document them.
