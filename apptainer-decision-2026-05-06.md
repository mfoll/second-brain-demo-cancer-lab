---
type: Event
date: 2026-05-06
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-cluster]]"
  - "[[container-provenance]]"
  - "[[ilse-van-dorn]]"
  - "[[nikolai-petrov]]"
_organized: true
---

# Apptainer Decision 2026-05-06

Decision meeting on how the group builds and distributes container images for the [[halyard-cluster]]. Wednesday 14:00 to 15:15, research IT meeting room. Present: Ines Varga, [[tobias-wren]], [[dmitri-halvorsen]], [[ilse-van-dorn]] (research IT), [[nikolai-petrov]] (RSE). [[amara-okonkwo]] joined for the spatial items.

## At a Glance

> [!note]
> Halyard does not allow Docker. We will build Apptainer images in GitLab CI from version-controlled definition files, push them to the institute registry, and reference them by digest in the Nextflow configs. Building on Halyard login nodes and pulling Docker Hub images at run time were rejected.

## Context

Halyard runs Slurm with Apptainer as the only container runtime; Docker daemons are not permitted on any node, for security reasons Ilse restated at the start ([[halyard-user-guide]]). On Kestrel the group had used a mix of conda environments, a few Docker images run through Singularity, and system modules. The [[halyard-cluster-migration]] needed one way of doing it before the cfDNA pipeline moved over.

## Options Considered

1. **Build on Halyard with `--fakeroot`**. Fast to start. Rejected: research IT does not allow builds on login nodes, builds would depend on whoever ran them, and there is no record of what went into an image.
2. **Pull public Docker images at run time** and let Apptainer convert them. Simple for nf-core modules. Rejected as the default: tags move, conversion happens on every new node cache, and Docker Hub rate limits hit large array jobs. Allowed only for nf-core modules whose BioContainers images are pinned by digest.
3. **Build in CI** from Apptainer definition files kept in each pipeline repository, push `.sif` images to the institute registry over ORAS, and pin by digest in Nextflow configs. Chosen.

## Reasons For Option 3

- One build per change, logged in CI, with the definition file in Git: every image can be traced to a commit ([[container-provenance]]).
- Nikolai's team already runs CI runners able to build Apptainer images without root on Halyard.
- Images are pulled once into the group cache on Halyard project space, so jobs do not depend on the internet.
- Matches community recommendations on packaging and versioning ([[gruening-2018-packaging-containerizing-bioinformatics-software]]) and the HPC container model Apptainer comes from ([[kurtzer-2017-singularity-scientific-containers]]).

## Decisions

- CI-built Apptainer images for all local tools, one definition file per tool or tool group, versioned with the pipeline.
- Nextflow configs reference images by digest, never by `latest`.
- nf-core modules may use their pinned BioContainers images directly.
- The spatial pipeline's GPU images get the same treatment; testing waits for GPU partition access, which we must apply for.

## Actions

- Nikolai: registry project and CI runner access for the group, by 2026-05-15. Done 2026-05-13.
- Tobias: definition files and CI for `varga-cfdna`, by 2026-06-01 ([[cfdna-pipeline-repository]], [[apptainer-image-registry]]).
- Tobias and Amara: GPU allocation request ([[halyard-gpu-allocation-request]]).
- Ilse: confirm registry pulls work from compute nodes. Confirmed 2026-05-11.

## Consequences

The cfDNA pipeline moved to Halyard in July using this route. The spatial pipeline could not be tested end to end until the GPU partition was granted on 2026-09-22, which is why the migration slipped by three months.
