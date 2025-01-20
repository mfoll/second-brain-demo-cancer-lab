---
type: Person
belongs_to: "[[serve-corvane-institute]]"
related_to:
  - "[[nextflow-pipeline-migration]]"
  - "[[apptainer-image-registry]]"
  - "[[research-software-sustainability]]"
_organized: true
---

# Nikolai Petrov

Research software engineering lead at Corvane. His team runs the institute GitLab, the shared CI runners and the container registry, and offers RSE time to groups on application.

## How We Work With Him

- Set up the CI runners that build our Apptainer images and the registry project where they live ([[apptainer-image-registry]]). Proposed the CI-built option at [[apptainer-decision-2026-05-06]].
- His team reviewed the `varga-cfdna` test layout in spring 2026 and suggested the snapshot-test structure we use ([[snapshot-testing]], [[cfdna-pipeline-repository]]).
- Runs the institute's monthly code review club, which [[tobias-wren]] and [[kenji-mori]] attend; it influenced our [[code-review-guidelines]].

Nikolai thinks groups underinvest in maintenance and says so. He is an ally on [[how-should-research-engineering-time-be-funded]]: his team has proposed shared research engineers funded by a levy on grants, and a costed line for RSE time in the [[aurora-programme-grant-2027]] would fit that model.

## Decisions He Shaped

- **CI over local builds.** At [[apptainer-decision-2026-05-06]] Nikolai argued that builds on Halyard would leave no record of what went into an image. His team's runners could already build Apptainer images without root, which made option 3 cheap.
- **Digest pinning.** He pushed for referencing images by digest rather than tag after another institute group lost a month to a moved tag ([[container-provenance]]).
- **Test structure.** His review of `varga-cfdna` suggested one snapshot test per module plus a single end-to-end test, rather than many end-to-end variants that are slow and hard to debug.

## Working With Him

Requests go through the RSE service desk, not direct messages; he triages weekly. He is generous with advice and strict about scope: RSE time goes to work that other groups can reuse, which is one reason we follow nf-core conventions ([[should-we-adopt-nf-core-modules-or-write-our-own]]).

## Current Threads

- Possible 20% RSE allocation to the spatial pipeline in 2027, application due January.
- Registry storage limits: our image history is the third largest in the institute; he asked us to prune untagged images ([[container-provenance]]).
