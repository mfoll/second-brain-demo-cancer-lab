---
type: Question
status: Open
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[limit-of-detection-in-cfdna-assays]]"
  - "[[low-vaf-caller-benchmark]]"
  - "[[clonal-hematopoiesis-filter]]"
_organized: true
---

# What VAF Threshold Defines a Positive MRD Call?

For the variant-based layer of the MRD call, what is the minimum evidence (VAF, supporting duplex families, number of tumour-informed variants) that counts as positive?

## Why It Matters

Most post-operative positives in St Aldric sit between 0.05% and 0.5% VAF, exactly where sequencing errors and CH variants also live. The threshold trades sensitivity against false molecular recurrence, which patients told us they fear more ([[patient-advisory-meeting-2025-10-22]]).

## Current Rule (Submitted Manuscript)

At least two tumour-informed variants each supported by two or more duplex consensus families, or one variant above 0.1% VAF with three or more families; CH-filtered. Pre-specified in [[mrd-statistical-analysis-plan-v2]].

## Why It Is Still Open

- The [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]] that should calibrate this is paused until the Halo truth set's contrived tier is unblinded.
- The 23 patients without tumour-informed variants rely on tumour-naive calls, where the rule above does not apply.
- The CH filter's miss rate depends on VAF ([[do-we-still-need-matched-buffy-coat-sequencing]]).

Keep the submitted rule for the revision; revisit when the benchmark resumes.
