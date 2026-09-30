---
type: Question
status: Open
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[federated-learning]]"
  - "[[fragmentomics-classifier]]"
  - "[[arjun-mehta]]"
_organized: true
---

# Can Federated Training Match A Pooled Classifier?

## Why It Matters

Stage 2 of the [[federated-cfdna-learning-concept-note]] asks for a postdoc year. That is worth it only if a model trained across sites without pooling comes close to what a pooled model would achieve, and beats each site's local model.

## What We Know

- Published multicentre examples show federated or swarm training matching pooled training with hundreds of patients per task ([[saldanha-2025-swarm-learning-surgical-video]]).
- Our setting differs: six different assays, so features must first be mapped to a common layer; and the patient tier has 60 patients, with roughly 10 per site.
- The fragment-length block of our classifier is a regularised logistic model, which federates easily; the end-motif block uses gradient boosting, which is harder to federate ([[fragmentomics-classifier]]).
- [[sun-hee-park]] doubts any training is sensible at this scale; [[arjun-mehta]] argues site-level legacy cohorts, not the truth set, would be the training data.

## Current Lean

Arjun's framing is right: the truth set is for evaluation; federated training only makes sense on larger site cohorts, which raises each site's approvals again.

## What Would Settle It

A simulation on Corvane data split into pseudo-sites, comparing pooled, federated and local training of the logistic block. [[leila-farouk]] has offered to run it with Thornvale as a real second site.
