---
type: Source
source_type: Web page
url: https://featurecloud.ai/
date_accessed: 2026-10-12
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[weilguny-2026-fedflow-featurecloud]]"
  - "[[federated-learning]]"
_organized: true
---

# FeatureCloud Platform

Web page of FeatureCloud, an open platform for federated analysis in biomedicine with a web interface and an app store of federated methods (regression, random forests, normalisation and others). Looked at as one of two candidate toolchains for [[federated-cfdna-learning]].

## Why It Matters

FeatureCloud already packages federated versions of the simple models we would need first, notably logistic regression, which is the fragment-length half of our stacked classifier ([[fragmentomics-classifier]]). Its weakness for us was manual, browser-driven operation at every site; [[weilguny-2026-fedflow-featurecloud]] describes a command-line orchestrator that addresses that and fits pipelines.

## Caveats

Apps run as Docker containers in the standard set-up; Halyard does not allow Docker ([[halyard-cluster]]), so a Corvane participant would need a separate machine or an Apptainer route. Not tested by us yet.

## Source Links

- [FeatureCloud](https://featurecloud.ai/)
