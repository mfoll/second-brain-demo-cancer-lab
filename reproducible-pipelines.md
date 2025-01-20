---
type: Topic
related_to:
  - "[[lead-tumour-evolution-group]]"
  - "[[research-software-sustainability]]"
  - "[[nextflow-pipeline-migration]]"
_organized: true
---

# Reproducible Pipelines

How the group makes analyses rerunnable by someone other than their author, years later, on a different cluster. This Topic gathers the notes on workflow managers, containers, testing, versioning and review; the work itself sits in [[nextflow-pipeline-migration]] and [[halyard-cluster-migration]].

## Working Position

- Pipelines are Nextflow DSL2, one repository per pipeline, released with a version tag ([[cfdna-pipeline-repository]], [[spatial-pipeline-repository]]).
- Software runs in Apptainer images built in CI from definition files and pinned by digest ([[apptainer-decision-2026-05-06]], [[container-provenance]]).
- Modules carry nf-test snapshot tests ([[snapshot-testing]]); every change gets a reviewer ([[code-review-guidelines]]).
- An analysis note records the pipeline version and image digest it used. A result without both is not reproducible by our own standard.

## Key Notes

- Decisions: [[apptainer-decision-2026-05-06]], [[should-we-adopt-nf-core-modules-or-write-our-own]].
- Procedures: [[run-the-cfdna-pipeline-on-halyard]], [[request-halyard-gpu-time]].
- Stances: [[code-review-in-small-labs]], [[research-engineers-deserve-authorship]].
- Open: [[should-we-require-code-review-for-all-pipeline-changes]], [[should-the-spatial-pipeline-stay-on-gpu]].

## Reading

- [[kurtzer-2017-singularity-scientific-containers]]: the container model Apptainer grew out of.
- [[gruening-2018-packaging-containerizing-bioinformatics-software]]: packaging recommendations we follow for images.
- [[molder-2021-sustainable-data-analysis-snakemake]]: the alternative we weighed.
- [[forer-2025-nf-test-pipeline-reliability]]: the testing framework we adopted.
- [[rokem-2024-ten-simple-rules-scientific-code-review]]: the basis for our review rules.

The broader question of keeping research software alive after its grant is in [[research-software-sustainability]].

## How We Got Here

Before 2025 the group's analyses ran on Kestrel through bash wrappers, a partly Snakemake cfDNA pipeline and unversioned conda environments ([[kestrel-job-submission-guide]]). Results were correct as far as anyone knew, but reproducing a 2024 figure meant guessing package versions. Three decisions changed that. In September 2025 the group chose Nextflow for both production pipelines ([[lab-meeting-2025-09-11]]). In May 2026, with Kestrel due to retire and Halyard forbidding Docker, it chose CI-built Apptainer images pinned by digest ([[apptainer-decision-2026-05-06]]). At the September 2026 retreat it made review mandatory for pipeline changes.

## Known Gaps

- Two workflows still run as wrapped legacy scripts without the pipeline provenance record ([[halyard-migration-tracker]]).
- GPU modules are hard to snapshot-test exactly because segmentation is not fully deterministic ([[snapshot-testing]]).
- Kestrel-era results remain reproducible only approximately; their environments sit in the cold archive.
- Keeping archived images runnable in five years is unsolved; see [[software-bus-factor]] and [[research-software-sustainability]].
