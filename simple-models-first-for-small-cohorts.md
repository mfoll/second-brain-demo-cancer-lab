---
type: Opinion
status: Revising
confidence: Medium
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[fragmentomics-classifier]]"
  - "[[classifier-design-review-2026-04-02]]"
  - "[[model-stacking]]"
_organized: true
---

# Simple Models First for Small Cohorts

## Stance

With a few hundred patients, start with regularised linear models and only add flexible models such as gradient boosting where they demonstrably add out-of-batch performance.

## Scope

Clinical prediction from omics features in cohorts below about 1,000 patients. Not a view on large screening cohorts or image models.

## Why I Think This

The [[lab-meeting-2026-03-12|March 2026 lab meeting]] made this the group's reflex: gradient boosting learned St Aldric extraction batches, and regularised logistic regression did not.

## Why It Is Being Revised

The [[classifier-design-review-2026-04-02|2026-04-02 review]] showed the rule was too blunt. Gradient boosting on end-motif features beat logistic regression on the same features across batches (0.77 vs 0.72 leave-batch-out). The problem was not model flexibility as such but flexibility applied to batch-sensitive features. A better formulation may be: match model capacity to how batch-sensitive each feature family is, and test that with leave-batch-out evaluation ([[model-stacking]]).

## What Would Change My Mind

If the stacked model fails cross-site validation in Halo while a logistic-only model passes, the original, simpler stance was right after all.

## Implications

Until revised, new projects start with a regularised linear baseline and must justify anything more flexible with leave-batch-out numbers.
