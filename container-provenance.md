---
type: Concept
maturity: Growing
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[apptainer-decision-2026-05-06]]"
  - "[[apptainer-image-registry]]"
_organized: true
---

# Container Provenance

The ability to say, for any result, exactly which software image produced it and how that image was built.

## Definition

An image has provenance when it can be traced from the result to an immutable identifier (the digest), from the digest to a build record, and from the build record to a definition file at a specific commit. A tag such as `1.4` or `latest` is not enough: tags can be moved to point at a different image.

## In Practice Here

- Images are built only in CI from definition files in the pipeline repository ([[apptainer-decision-2026-05-06]]).
- CI writes the commit and job ID into image labels ([[apptainer-image-registry]]).
- Nextflow configs reference images by digest; every run writes the resolved digests to `pipeline_info/`.
- An analysis note cites the pipeline version, and through it the digests.

## Why It Matters

Kestrel-era results were produced with unversioned conda environments ([[kestrel-job-submission-guide]]); reproducing a 2024 figure took Sofia two weeks of guessing package versions. Provenance turns that into a lookup.

## Limits

Provenance does not guarantee the image still runs: base images and drivers age. Keeping archived images runnable is the separate problem of [[research-software-sustainability]].
