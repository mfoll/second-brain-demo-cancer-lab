---
type: Event
date: 2025-06-16
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[elias-moreau]]"
  - "[[batch-confounding-in-cfdna-studies]]"
  - "[[cfdna-extraction-qc-log-2025]]"
_organized: true
---

# Extraction Kit Lot Change 2025-06-16

On 2025-06-16 [[elias-moreau|Elias Moreau]] switched to a new lot of the cfDNA extraction kit when the previous lot ran out. He recorded the lot number and date in the QC log as the SOP requires ([[cfdna-extraction-qc-log-2025]]). At the time it looked like a routine event: yields and Bioanalyzer profiles of the first 24 samples on the new lot were within the acceptance ranges of [[cfdna-extraction-qc]].

## Why It Became Important

By then about 640 samples had been extracted, mostly pre-operative and day-28 samples, because the extraction order followed the shipment order from St Aldric. The later samples, mostly follow-up time points, were extracted with the new lot. Batch and clinical time point were therefore strongly confounded.

In 2026-03, [[sofia-reyes-calderon|Sofia Reyes Calderon]] found that the gradient-boosting fragmentomics classifier could predict the extraction lot with AUC 0.88 from fragment-length features alone ([[classifier-batch-effect-analysis-2026-03]]). The new lot shifted the modal fragment length by about 3 bp and raised the sub-150 bp fraction, mimicking a tumour-like signal. This led to the [[lab-meeting-2026-03-12|2026-03-12 lab meeting]] decision.

## Lessons Recorded

- Randomise extraction order across time points and outcomes, not shipment order. Now in the SOP update.
- Keep bridging samples: re-extract 16 samples on each new lot.
- Record lot numbers in the sample sheet, not only in the lab log.

See [[batch-confounding-in-cfdna-studies]].
