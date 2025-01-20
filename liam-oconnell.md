---
type: Person
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[halo-sop-comparison-bioinformatics]]"
  - "[[tobias-wren]]"
  - "[[tomasz-wilk]]"
_organized: true
---

# Liam O'Connell

Site bioinformatician at Hollinmoor University Medical Centre, working with [[tomasz-wilk]] on the methylation assay. Within WP4 he is the most active contributor to the shared analysis code.

## Role

- Runs Hollinmoor's methylation pipeline and returned the site's truth-set calls first, on 2026-07-21.
- Compiled the bioinformatics part of the site comparison ([[halo-sop-comparison-bioinformatics]]): aligners, deduplication, UMI handling and calling thresholds at all six sites.
- Maintains the input validation module in the [[halo-wp4-analysis-code-repository]].

## How We Work Together

Liam and [[tobias-wren]] speak the same language: both moved pipelines to Nextflow in the last year, and Liam's nf-test layout influenced ours in the [[nextflow-pipeline-migration]]. He reviews WP4 pull requests within a day or two and is blunt about untested code.

He is also the consortium's informal container person. When Corvane decided on Apptainer images built in CI ([[apptainer-decision-2026-05-06]]), he adopted the same approach so that a WP4 image runs unchanged at both sites, which matters for any federated pilot.

## Current Threads

- Common file format for per-sample feature tables, so that a cross-assay model can read all six sites.
- Testing the WP4 container at Hollinmoor before the federated pilot is costed.
- Helping [[leila-farouk]] port the end-motif feature code to the Thornvale assay.

## History With The Group

Liam first worked with [[tobias-wren]] on the shared feature-extraction module in spring 2026, when the two of them agreed on one output schema for per-sample feature tables. He spent two days at Corvane after the annual meeting to finish the module's tests, and since July all six sites run it in the same container. He is also the person most likely to notice when a Corvane pull request skips a test.

## Links

- [[halo-consortium-work]]
- [[halo-cross-site-benchmark]]
