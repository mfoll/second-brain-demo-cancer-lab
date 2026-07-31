---
type: Event
date: 2026-07-14
belongs_to: "[[mrd-manuscript]]"
related_to:
  - "[[clara-hoffmann]]"
  - "[[mrd-reviewer-comments-2026-07]]"
  - "[[halo-cross-site-benchmark]]"
  - "[[data-access-policy-revision]]"
_organized: true
---

# MRD Manuscript Decision 2026-07-14

Tumour Evolution Reports returned a major revision for the [[mrd-manuscript|MRD Manuscript]], submitted on 2026-02-27. The decision letter came from handling editor [[clara-hoffmann|Clara Hoffmann]] with three reviewer reports ([[mrd-reviewer-comments-2026-07]]).

## At a Glance

> [!warning]
> Reviewer 2 requires validation on an external cohort and the editor marked that request as essential. The only realistic external samples are Halo samples, and using them needs a data access policy change the institute has not yet adopted, so the revision is blocked on governance, not on analysis.

## What the Reviewers Asked

**Reviewer 1 (molecular methods).** Broadly positive. Asked how clonal hematopoiesis was excluded for the 152 patients without matched buffy coat sequencing, and for a sensitivity analysis with and without the CH filter. Also asked whether fragmentomics features were affected by pre-analytical variation. Answerable with St Aldric data ([[clonal-hematopoiesis-filter]], [[classifier-batch-effect-analysis-2026-03]]).

**Reviewer 2 (clinical validation).** The critical one. Main points:

1. All models were developed and evaluated in one centre with one wet lab; internal cross-validation cannot exclude site-specific artefacts. Asks for validation on an independent cohort from another centre, processed separately.
2. The classifier should be locked before validation, with thresholds pre-specified.
3. A temporal split within St Aldric would not address the concern.

**Reviewer 3 (statistics).** Lead time is measured against scheduled imaging, so it is interval-censored; asks for an analysis that accounts for this and for confidence intervals on the median lead time. Also asked for decision-curve analysis. Advisory, per the editor.

## Our Reading

Reviewer 2 is right, and the point overlaps with what we found ourselves in March: the gradient-boosting fragmentomics model had learned St Aldric extraction batches ([[lab-meeting-2026-03-12]]). The revision will report the stacked classifier adopted at the [[classifier-design-review-2026-04-02|2026-04-02 review]], and we will say so in the cover letter.

External samples: the [[halo-cross-site-benchmark|Halo Cross-Site Benchmark]] includes post-resection pancreatic plasma at two sites with outcome data, and the [[halo-truth-set]], shipped to all sites on 2026-05-19, includes 30 post-resection pancreatic patients plus healthy-donor plasma usable for cross-site calibration. Using them for our paper requires transferring derived data between Halo sites and Corvane for a non-consortium publication, which the current institute policy does not cover. The consortium transfer clause is being drafted in the [[data-access-policy-revision|Data Access Policy Revision]] and has not yet gone to the board.

## Decisions Taken That Day

- Ines accepted the revision and asked for the standard 90 days, with the expectation of an extension.
- Revision planning meeting set for 2026-07-21 ([[mrd-revision-planning-2026-07-21]]).
- No new analysis on Halo data until the classifier is frozen ([[external-validation-before-locking-a-classifier]]).

## Follow-Up

- Formal Halo request sent on 2026-08-04 ([[halo-validation-request-2026-08-04]]).
- Extension to 2027-01-29 granted on 2026-10-07 ([[mrd-revision-extension-2026-10-07]]).
- Plan and owners: [[mrd-revision-response-plan]].
