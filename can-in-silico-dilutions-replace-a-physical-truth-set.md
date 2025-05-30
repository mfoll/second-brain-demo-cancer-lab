---
type: Question
status: Deferred
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[halo-truth-set]]"
  - "[[low-vaf-in-silico-dilution-results-2025-08]]"
  - "[[sergi-2024-artificial-low-tumour-fraction-samples]]"
_organized: true
---

# Can In-Silico Dilutions Replace a Physical Truth Set?

Can mixing reads from high-tumour-fraction and healthy cfDNA in silico give caller benchmarks at 0.05–0.5% VAF that are trustworthy enough to publish, or do we need physical dilution series?

## Why It Was Asked

The [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]] started with in-silico dilutions because they are cheap ([[low-vaf-in-silico-dilution-results-2025-08]]).

## Status

Deferred on 2025-11-17, when the benchmark was paused. Our in-silico data preserved the patients' own error background but not library-level effects such as duplicate rates and UMI family sizes, which are exactly what decides low-VAF performance. Published work goes both ways: simulated datasets can tune callers ([[sergi-2024-artificial-low-tumour-fraction-samples]]), while dilutions of real patient cfDNA preserve properties simulations miss ([[carrie-2025-benchmarking-ctdna-mutation-calling]]).

Revisit when the contrived tier of the [[halo-truth-set]] (shipped 2026-05-19) is unblinded to sites: compare caller rankings on in-silico and physical data. If they agree, in-silico dilutions are fine for future tuning.
