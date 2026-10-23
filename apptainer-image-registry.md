---
type: Source
source_type: Internal resource
date_accessed: 2026-10-14
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[apptainer-decision-2026-05-06]]"
  - "[[container-provenance]]"
  - "[[nikolai-petrov]]"
_organized: true
---

# Apptainer Image Registry

The group's project in the institute container registry, run by [[nikolai-petrov]]'s RSE team, where CI pushes our Apptainer images. Set up on 2026-05-13 after [[apptainer-decision-2026-05-06]].

## Summary

Holds 34 image repositories, one per tool or tool group, each built from a definition file in the owning pipeline repository. Images are pushed over ORAS with a version tag and resolved by digest in the Nextflow configs.

## Key Details

- Naming: `varga/<pipeline>/<tool>:<tool-version>-<build>`; for example the end-motif module image used by `varga-cfdna` v1.2.
- Every push records the Git commit and CI job in image labels ([[container-provenance]]).
- Untagged images older than 90 days are pruned monthly since October, at Nikolai's request.
- GPU images for the spatial pipeline are about 9 GB each, which is why the Halyard image cache sits in project space and not in home directories.

## Source Location

Institute GitLab, group `varga`, "Packages and registries"; read access for all group members, push only from CI.
