---
type: Question
status: Open
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[benchmarks-must-report-failure-modes]]"
  - "[[marco-bellini]]"
  - "[[kenji-mori]]"
_organized: true
---

# How To Report Failing Methods In The Benchmark?

The preprint must show that two methods collapse low-count spots. Do we name them, and how do we handle a developer who has not replied?

## Where We Are

- [[marco-bellini]] confirmed the mechanism for his method and agreed to be named, with his planned fix mentioned ([[marco-bellini-call-2026-05-21]]).
- The developers of the other method (M3) have not replied to two emails (2026-04-28 and 2026-07-06). An issue on their public repository with a minimal example is drafted but not posted.

## Options

- Name both, with the reproducible example and version numbers, and note that M3's developers were contacted.
- Name Marco's method only, anonymise M3. Rejected by Ines: readers cannot act on an anonymous warning.
- Post the public issue first, wait four weeks, then name.

## Leaning

Post the issue now, name both in the preprint with exact versions and the date of contact. Decide at the November benchmark meeting. Stance behind it: [[benchmarks-must-report-failure-modes]].
