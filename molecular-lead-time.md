---
type: Concept
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[minimal-residual-disease]]"
  - "[[what-lead-time-over-imaging-is-clinically-meaningful]]"
  - "[[maja-kovac]]"
_organized: true
---

# Molecular Lead Time

Molecular lead time is the interval between the first positive cfDNA sample and clinical detection of recurrence, here radiological recurrence on scheduled CT.

## Definition Used in the MRD Study

For each recurrent patient with at least one positive sample before recurrence: date of radiological recurrence minus date of first positive plasma sample, after which all later samples are positive or missing. Patients positive only at or after recurrence contribute zero. Pre-specified in [[mrd-statistical-analysis-plan-v2]].

## Pitfalls

- **Interval censoring**: recurrence is only seen at scheduled scans, so its true date lies between the last negative and the first positive scan. Measuring to the scan date overstates lead time by up to one scan interval. Reviewer 3 asked for a censoring-aware estimate ([[mrd-manuscript-decision-2026-07-14]]); [[maja-kovac|Maja Kovac]] is fitting it.
- **Sampling frequency**: lead time also depends on how often blood is drawn; a three-monthly schedule caps resolution at three months.
- **Not the same as pre-diagnostic lead time**: in the [[northvale-early-detection-study]], lead time is measured before a first diagnosis in a cohort, with reverse causation concerns. Here it is after surgery, in patients known to have had cancer.

Submitted estimate: median 4.3 months (IQR 2.1–7.0). Expect it to shrink in the revision.
