---
type: Project
status: Idea
start: 2026-07-01
belongs_to: "[[colorectal-metastasis-atlas]]"
related_to:
  - "[[data-access-policy-revision]]"
  - "[[nikolai-petrov]]"
  - "[[spatial-transcriptomics]]"
has:
  - "[[what-access-model-for-the-atlas-data-portal]]"
_organized: true
---

# Atlas Data Portal

A public web browser for the [[colorectal-metastasis-atlas]]: view each section with its pathology annotation, bins coloured by cell type or subclone, and download processed matrices. Not started; recorded so that the design constraints are not lost.

## Outcome

A browser launched with the atlas paper, showing all 80 sections, with processed data openly downloadable and raw data behind a controlled-access route.

## Current State

- Idea since 2026-07-01, raised at the group retreat planning ([[group-retreat-2026]]). No developer time allocated.
- [[nikolai-petrov]] (research software engineering) offered a scoping conversation; he suggested reusing an existing open-source spatial viewer rather than building one.
- The access model depends on the revised institute data access policy ([[data-access-policy-revision]]), which is not yet adopted.

## Scope and Boundaries

Processed, de-identified data only in the open part: bin-level counts, annotations, cell-type estimates. Clinical variables beyond treatment group and regression grade stay out. Raw images and FASTQ files would sit in a controlled-access archive. The portal is not a clinical tool.

## Working Context

The open questions are about governance more than software ([[what-access-model-for-the-atlas-data-portal]]). The Westmere tissue agreement allows publication of de-identified derived data but needs re-reading for images ([[atlas-tissue-access-agreement]]). Hosting would be on institute infrastructure; [[yara-castellanos]] flagged that whole-slide images at full resolution are about 2 GB per section.

## Next Actions

- [ ] Scope with Nikolai Petrov after the atlas analysis set is frozen (not before 2027-02).
- [ ] Ask Yara Castellanos whether section images count as identifiable under the tissue agreement.
- [ ] Include a portal line in the [[frontier-interim-report]] plan.

## Do Not Do Yet

> [!danger]
> Do not publish any section image or bin-level matrix outside the institute before the data access policy revision is adopted and the tissue agreement has been checked for images.

## Maintenance Log

- 2026-07-01: Recorded as an Idea after the retreat planning discussion.
