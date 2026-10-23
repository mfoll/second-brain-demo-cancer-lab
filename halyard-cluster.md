---
type: Source
source_type: Internal resource
storage_system: Corvane research IT
date_accessed: 2026-10-20
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[ilse-van-dorn]]"
  - "[[halyard-user-guide]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Halyard Cluster

Halyard is the Corvane Institute's high-performance computing cluster, run by research IT under [[ilse-van-dorn]]. It replaced Kestrel, which was retired on 2026-09-30. This note records what the group has on Halyard and the rules that apply to us; the general user documentation is [[halyard-user-guide]].

## Summary

- Scheduler: Slurm. Container runtime: Apptainer only; Docker is not allowed on any node.
- Partitions we use: `cpu` (general, 7-day limit), `himem` (1.5 TB nodes, 3-day limit), `gpu` (by application only).
- Group allocation: 600,000 core-hours per year on `cpu` and `himem`; 6,000 GPU-hours on `gpu` from 2026-09-22 to 2027-03-31.
- Storage: 200 TB group project space (backed up, quota), 50 TB scratch (purged after 30 days without access), institute cold archive for retired data.

## Why It Matters

Every production pipeline of the group runs here, and the group's compute budget and data layout follow from it. The ban on Docker drove [[apptainer-decision-2026-05-06]]. The GPU partition gate is why the spatial pipeline moved last ([[halyard-gpu-partition-granted-2026-09-22]]).

## Key Details

- **GPU partition granted 2026-09-22.** 6,000 GPU-hours on nodes with four GPUs each, for cell segmentation and deconvolution in the spatial pipeline. Request in [[halyard-gpu-allocation-request]]; renewal decided by research IT in March 2027 on usage. First spatial job ran 2026-09-24.
- Group project space layout: `/projects/varga/{raw,derived,images,shared}`. Raw data is read-only for everyone except Tobias and Yara. Images live in `/projects/varga/images` as pinned `.sif` files pulled from the registry ([[apptainer-image-registry]]).
- Quota: 141 TB used of 200 TB on 2026-10-20, after the 41 TB moved from Kestrel ([[halyard-storage-quota-statement]]).
- Charging: free until 2027-03-31; from April 2027 storage above 100 TB per group is charged. Forecast due to research IT in December.
- Accounts are requested by the group leader through the research IT portal and need the data protection training certificate ([[onboard-a-new-lab-member]]).
- Identifiable clinical data must not be stored on Halyard, consistent with the [[group-data-management-plan]].

## Caveats

- Figures are the group's own record from research IT statements and our quota report; check the research IT portal for current usage.
- The GPU allocation is not permanent. Do not design 2027 analyses that assume more than the current grant ([[should-the-spatial-pipeline-stay-on-gpu]]).
- Scratch purge is automatic. Several people lost intermediate files in August; keep anything needed beyond a month in project space.

## Source Location

- Research IT portal, Halyard section: institute intranet, "Research computing > Halyard".
- Group allocation letters and quota statements: group drive `Admin/Compute/Halyard/`.
