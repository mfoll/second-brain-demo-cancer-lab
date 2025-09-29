---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1371/journal.pcbi.1005412
doi: 10.1371/journal.pcbi.1005412
pmid: "28407023"
licence: cc by
date_accessed: 2025-09-09
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[reproducible-pipelines]]"
  - "[[tobias-wren]]"
_organized: true
---

# Ten simple rules for making research software more robust.

Taschuk M, Wilson G. PLOS Computational Biology, 2017.

## Summary

Ten rules for making research software run outside the original lab or the original developer's machine, addressing the common problems that stop others from installing, configuring or running it.

## Why It Matters

[[tobias-wren]] circulated it on 2025-09-09, the day after he finished making [[felix-achterberg]]'s CNV code rerunnable. Almost every problem he hit is one of the ten: hard-coded paths, undocumented dependencies, no example data, no version number. It became the seed of the [[research-software-sustainability]] cluster and of the checklist in the [[nextflow-pipeline-migration]].

## Key Details

Rules we adopted outright: a versioned release, a small test dataset in the repository, configuration outside the code, and no reliance on the developer's environment. The Apptainer images chosen on 2026-05-06 ([[apptainer-decision-2026-05-06]]) cover the environment rule for Halyard.

## Source Links

- [Ten simple rules for making research software more robust](https://doi.org/10.1371/journal.pcbi.1005412)
