---
type: Note
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[can-in-silico-dilutions-replace-a-physical-truth-set]]"
  - "[[halo-truth-set]]"
_archived: true
_organized: true
---

# Low-VAF Spike-In Design v1

> [!warning]
> Archived 2025-11-17 when the [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]] was paused; the Halo truth set will replace this design.

First design (2025-06) for a physical truth set for the benchmark: commercial reference DNA with 40 known variants, sheared to cfDNA-like length, spiked into pooled healthy-donor cfDNA at 1%, 0.5%, 0.25%, 0.1% and 0.05%, three replicates each, 30 ng input.

## Why It Was Dropped

- Cost about 6,500 EUR for reference material and sequencing, for one site only.
- Sheared reference DNA does not reproduce cfDNA fragment ends or nucleosome-protected lengths, so it flatters callers ([[limit-of-detection-in-cfdna-assays]]).
- The Halo consortium decided in 2025-11 to build a shared multi-site truth set ([[halo-truth-set]]), which answers the same question better and across assays.

Kept because its dilution levels were our input to the Halo truth set design, which ended up with a similar ladder (0.1% to 2%) but dropped our 0.05% level.
