---
type: Project
status: Active
start: 2026-04-01
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[tobias-wren]]"
  - "[[ilse-van-dorn]]"
has:
  - "[[halyard-cluster]]"
  - "[[apptainer-decision-2026-05-06]]"
  - "[[halyard-migration-tracker]]"
  - "[[archive-kestrel-data]]"
  - "[[kestrel-retirement-2026-09-30]]"
_organized: true
---

# Halyard Cluster Migration

Moving every group pipeline and dataset from the old Kestrel cluster to the institute's new [[halyard-cluster]], which runs Slurm and allows Apptainer containers only.

## Outcome

All group pipelines run on Halyard with Apptainer images, and Kestrel data is either migrated or archived with an inventory. Done when the last two workflows (methylation panel calling and the CH variant workflow) run on Halyard and the Kestrel archive is verified.

## Current State

- Kestrel was retired on 2026-09-30 ([[kestrel-retirement-2026-09-30]]). Group data there (186 TB) was triaged: 41 TB moved to Halyard project space, 112 TB written to the institute cold archive, 33 TB of intermediates and duplicates deleted with sign-off ([[kestrel-data-inventory]]).
- The cfDNA pipeline has run on Halyard since July 2026. The spatial pipeline's CPU steps moved in August; its GPU steps started on 2026-09-24, two days after the GPU partition was granted on 2026-09-22 ([[halyard-gpu-partition-granted-2026-09-22]]).
- Images are Apptainer `.sif` files built in GitLab CI and pinned by digest ([[apptainer-decision-2026-05-06]], [[apptainer-image-registry]]).
- Remaining: the methylation panel calling workflow and [[hannah-lindqvist]]'s CH variant workflow still run as wrapped legacy scripts; the cold-archive checksum verification is 80% done.

## Scope and Boundaries

Covers infrastructure moves, images, data transfer and archive. Rewriting pipelines in Nextflow is [[nextflow-pipeline-migration]]; the two projects share people and overlap in time but have different end conditions. Governance of what may be stored where follows the [[group-data-management-plan]]; changes to it go through Yara and the board, not this project.

## Working Context

The plan in April assumed a June finish. It slipped for one reason: the spatial pipeline's cell segmentation and deconvolution steps need GPUs, and Halyard's GPU partition was allocated by application only. We applied in July ([[halyard-gpu-allocation-request]]); research IT granted 6,000 GPU-hours to 2027-03-31 on 2026-09-22. Until then [[amara-okonkwo]] ran segmentation on Kestrel's two old GPU nodes, which is why the Kestrel archive could not close earlier.

Docker is not permitted on Halyard. The options weighed on 2026-05-06 were building on login nodes with fakeroot, pulling Docker Hub images at run time, or building in CI. CI won; the decision note has the reasons.

Per-pipeline status is kept in [[halyard-migration-tracker]] rather than here.

## Active Workflows

- [[run-the-cfdna-pipeline-on-halyard]] for production cfDNA runs.
- [[request-halyard-gpu-time]] when the allocation runs low.
- [[archive-kestrel-data]] for the remaining checksum verification.

## Next Actions

- [ ] Wrap the methylation panel calling workflow in a CI-built image and run it on Halyard (Tobias, November).
- [ ] Port Hannah's CH variant workflow, coordinated with [[clonal-hematopoiesis-filter]] milestones.
- [ ] Finish cold-archive checksum verification and send the inventory to Yara for the DMP record.
- [ ] Review GPU usage in January and decide whether to apply for a 2027-04 renewal ([[should-the-spatial-pipeline-stay-on-gpu]]).
- [ ] Close the project once the two workflows pass a full test run.

## Open Questions

- [[should-the-spatial-pipeline-stay-on-gpu]]
- [[how-long-should-we-keep-raw-fastq-on-halyard]]

## Important Notes

- [[halyard-cluster]] and [[halyard-user-guide]]
- [[apptainer-decision-2026-05-06]]
- [[kestrel-data-inventory]]
- [[halyard-migration-tracker]]

## Do Not Do Yet

> [!danger]
> Do not delete anything from Halyard scratch or the cold archive staging area until the checksum verification for that batch is recorded in the Kestrel data inventory.

## Maintenance Log

- 2026-09-30: Kestrel retired; all group data accounted for.
- 2026-09-22: GPU partition granted; spatial pipeline unblocked.
- 2026-05-06: Apptainer images built in CI chosen.
- 2026-04-01: Project started after the [[kestrel-retirement-notice]].
