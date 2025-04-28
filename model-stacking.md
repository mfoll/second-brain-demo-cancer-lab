---
type: Concept
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[classifier-design-review-2026-04-02]]"
  - "[[fragment-length-and-end-motif-features]]"
_organized: true
---

# Model Stacking

Stacking trains several base models, each producing a score, and then a meta-learner that combines those scores. The meta-learner must be trained on out-of-fold predictions; otherwise it learns to trust whichever base model overfits most.

## In Our Classifier

The [[fragmentomics-classifier|Fragmentomics Classifier]] stacks two base models by feature family ([[fragment-length-and-end-motif-features]]):

- L2-regularised logistic regression on batch-corrected fragment-length features;
- gradient boosting on end-motif features;
- a logistic meta-learner on the two out-of-fold scores, with no access to raw features.

This is stacking by feature family, chosen so that each family gets the model that suits its noise. It was adopted at the [[classifier-design-review-2026-04-02|2026-04-02 review]] after the [[lab-meeting-2026-03-12|2026-03-12 decision]] to drop gradient boosting entirely turned out to be too broad.

## Pitfalls

- Out-of-fold predictions must use the same folds as evaluation, and in our case the folds are extraction batches. Using random folds would bring the batch leak back through the meta-learner.
- The meta-learner weights are part of the locked model and must be in the model card ([[classifier-model-card-v2]]).
- Stacking adds parameters; with 212 patients the meta-learner is kept to two inputs and an intercept.
