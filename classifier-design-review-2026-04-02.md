---
type: Event
date: 2026-04-02
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[lab-meeting-2026-03-12]]"
  - "[[sofia-reyes-calderon]]"
  - "[[classifier-stacking-evaluation-2026-04]]"
  - "[[model-stacking]]"
_organized: true
---

# Classifier Design Review 2026-04-02

Review of the [[fragmentomics-classifier|Fragmentomics Classifier]] three weeks after the [[lab-meeting-2026-03-12|2026-03-12 lab meeting]] had decided to replace gradient boosting with regularised logistic regression. Present: Ines, [[sofia-reyes-calderon|Sofia Reyes Calderon]], [[dmitri-halvorsen|Dmitri Halvorsen]], [[maja-kovac|Maja Kovac]], and [[arjun-mehta|Arjun Mehta]] from Halo by video.

## At a Glance

> [!note]
> The March decision was partly reversed. Gradient boosting overfitted extraction batches through fragment-length features, not end-motif features, so the classifier became a stacked model: regularised logistic regression on fragment-length features, gradient boosting kept for end-motif features, combined by a logistic meta-learner.

## Background

On 2026-03-12 the group saw that the gradient-boosting model could predict the extraction kit lot ([[extraction-kit-lot-change-2025-06-16]]) and that its leave-batch-out AUC fell from 0.91 to 0.74 ([[classifier-batch-effect-analysis-2026-03]]). A quick logistic model shown at that meeting held up much better (0.80 within batches, 0.78 leave-batch-out). The decision was to drop gradient boosting entirely in favour of regularised logistic regression, and ComBat-style correction was rejected.

## What Sofia Showed

Implementing the March decision, Sofia refitted the logistic model (L2 and elastic net gave the same result; L2 kept) and added a bridging correction for length features: each lot's features are centred on the mean of 16 bridging samples extracted on both lots. Unlike ComBat, this uses no outcome labels and no patient samples beyond the bridging set. She then split the evaluation by feature family ([[classifier-stacking-evaluation-2026-04]]):

| Model | Within-batch CV AUC | Leave-batch-out AUC |
|---|---|---|
| Gradient boosting, all features | 0.91 | 0.74 |
| Logistic, all features (quick fit, 2026-03-12) | 0.80 | 0.78 |
| Logistic, all features (refit, bridging-corrected) | 0.85 | 0.83 |
| Gradient boosting, end motifs only | 0.79 | 0.77 |
| Logistic, end motifs only | 0.73 | 0.72 |
| Stacked (logistic length + boosting motifs) | 0.88 | 0.86 |

End-motif features barely moved between lots, and gradient boosting extracted more from them than logistic regression did, probably through motif interactions. The batch problem sat in the fragment-length features.

## Discussion

- Dmitri had suggested in March that the motif family might be clean; the numbers supported it.
- Maja asked whether a 0.03 gain over logistic-only justified the complexity. Ines's view: yes, because the gain is in leave-batch-out, the setting that matters for external validation, and because the stacked model degrades gracefully if one family fails at a new site.
- Arjun noted that Halo sites use three extraction chemistries, so the length component must be batch-corrected per site before validation. Logged as [[does-the-stacked-classifier-generalise-across-extraction-batches]].

## Decisions

- Adopt the stacked design ([[model-stacking]]); record it in [[classifier-model-card-v2]].
- Keep the 2026-03-12 rationale on record: gradient boosting is not used on fragment-length features.
- Every retraining must report leave-batch-out performance ([[fragmentomics-classifier-retraining]]).
- The revision of the [[mrd-manuscript|MRD Manuscript]] reports the stacked model; the archived [[gradient-boosting-only-classifier-plan]] stays linked for provenance.
