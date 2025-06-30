---
type: Source
source_type: Web page
url: https://fulcrumgenomics.github.io/fgbio/
date_accessed: 2025-06-09
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[low-vaf-caller-shortlist-2025-06]]"
  - "[[minimal-residual-disease]]"
_organized: true
---

# fgbio Documentation

Documentation of fgbio, an open-source toolkit for working with UMI-tagged sequencing data, including grouping reads by UMI and building single-strand and duplex consensus reads.

## Why It Matters

All low-VAF variant calling in the group, in the MRD study and in the [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]], uses fgbio consensus reads upstream of the caller. Keeping consensus fixed lets the benchmark compare callers rather than consensus strategies ([[low-vaf-caller-shortlist-2025-06]]).

## Key Details

- Our settings: minimum two reads per strand for duplex consensus; error-rate parameters as recorded in the pipeline config.
- Duplex consensus cut false positives by roughly six times in our in-silico tests ([[low-vaf-in-silico-dilution-results-2025-08]]).

## Source Links

- [fgbio documentation](https://fulcrumgenomics.github.io/fgbio/)
