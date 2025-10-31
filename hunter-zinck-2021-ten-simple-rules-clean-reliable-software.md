---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1371/journal.pcbi.1009481
doi: 10.1371/journal.pcbi.1009481
pmid: "34762641"
licence: cc by
date_accessed: 2025-10-13
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[nextflow-pipeline-migration]]"
  - "[[taschuk-2017-ten-simple-rules-robust-research-software]]"
_organized: true
---

# Ten simple rules on writing clean and reliable open-source scientific software.

Hunter-Zinck H et al., PLOS Computational Biology, 2021.

## Summary

Ten rules grouped around two practices that give a lot for little training: clean code and testing. Clean code lowers the cognitive load for the original author and later contributors; modular code is easier to unit test, and unit tests double as usage examples. Other test types catch errors that unit tests miss.

## Why It Matters

Used in the first week of the [[nextflow-pipeline-migration]] (started 2025-10-06) to agree what "nf-test coverage" means for us: every module gets at least one test with a stub dataset, and every bug fix adds a test. [[sofia-reyes-calderon]] and [[kenji-mori]] were asked to read it before contributing modules.

## Caveats

Generic software practice; it does not address workflow managers or HPC specifics.

## Source Links

- [Ten simple rules on writing clean and reliable open-source scientific software](https://doi.org/10.1371/journal.pcbi.1009481)
