---
type: Source
source_type: Peer review report
date_accessed: 2026-02-16
belongs_to: "[[peer-review-and-editorial]]"
related_to:
  - "[[peer-review-log]]"
  - "[[reproducible-pipelines]]"
_organized: true
---

# Review Report For Genome Methods Letters, February 2026

Ines's report on a methods manuscript describing a workflow for processing targeted cfDNA sequencing, submitted to Genome Methods Letters (where she sits on the board but did not handle this paper). Recorded generically: the manuscript is confidential and nothing from it is kept here.

## What The Report Asked For

- A runnable example: the code repository lacked test data and a container, so the stated results could not be reproduced. Ines spent two hours trying before writing this point.
- A comparison against at least one established workflow on the same input, with run time and output agreement.
- Clarity on how duplicate reads and UMIs were handled, since that drives low-VAF sensitivity.

## Recommendation

Major revision. The editor agreed; the revised version in 2026-05 addressed the container and test-data points, and Ines recommended acceptance.

## Notes For Us

The same checklist applies to our own [[nextflow-pipeline-migration]] before we publish any pipeline: test data, container, versioned release ([[taschuk-2017-ten-simple-rules-robust-research-software]]). Report not signed; published-report option did not yet exist.

## Source Location

Journal reviewer system; Ines's copy in `Service/reviews/2026/` on her institute drive.
