---
type: Question
status: Answered
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[nf-core-guidelines]]"
  - "[[cfdna-pipeline-repository]]"
_organized: true
---

# Should We Adopt nf-core Modules Or Write Our Own?

## Question

When porting to Nextflow, should we reuse nf-core modules for standard steps or write every module ourselves for full control?

## Current Answer

> [!info]
> Use nf-core modules for standard tools (alignment, deduplication, QC) and write local modules, following nf-core conventions, for our own methods. Decided by Tobias and Dmitri in October 2025.

## Reasons

- 11 of 38 modules in `varga-cfdna` are nf-core; they come with tests and pinned BioContainers images.
- Our fragment, end-motif and methylation steps have no nf-core equivalent.
- Following the conventions ([[nf-core-guidelines]]) keeps the option of contributing modules back, and Halo sites recognise the layout.

## Caveat

nf-core module updates have changed outputs once (a samtools update altering duplicate flags), caught by [[snapshot-testing]]. Update nf-core modules deliberately, never in the same merge request as a method change.
