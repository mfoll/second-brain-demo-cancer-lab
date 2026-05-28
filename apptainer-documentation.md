---
type: Source
source_type: Web page
url: https://apptainer.org/docs/
date_accessed: 2026-05-04
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[apptainer-decision-2026-05-06]]"
  - "[[kurtzer-2017-singularity-scientific-containers]]"
_organized: true
---

# Apptainer Documentation

The official Apptainer user and admin documentation, consulted before the [[apptainer-decision-2026-05-06]].

## Why It Matters

Halyard allows Apptainer only. The documentation answered the practical questions behind the decision: how definition files work, how unprivileged builds work, and how images can be pushed to and pulled from OCI registries over ORAS, which is what our CI uses ([[apptainer-image-registry]]).

## Key Details

- Definition files declare base image, files, post-install steps and labels; ours add the Git commit as a label.
- GPU support is enabled at run time with the `--nv` flag, set in the `halyard` Nextflow profile for GPU processes.

## Caveats

Fakeroot builds are documented but disabled on Halyard by research IT policy ([[halyard-user-guide]]).

## Source Links

- [Apptainer documentation](https://apptainer.org/docs/)
