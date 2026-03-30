---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1371/journal.pcbi.1009959
doi: 10.1371/journal.pcbi.1009959
pmid: "36155971"
licence: cc by
date_accessed: 2026-03-25
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[time-to-diagnosis-windows]]"
  - "[[reverse-causation-in-prediagnostic-studies]]"
_organized: true
---

# A Deep Survival EWAS approach estimating risk profile based on pre-diagnostic DNA methylation: An application to breast cancer time to diagnosis.

## Summary

The authors argue that prediagnostic methylation studies either ignore time to diagnosis or model CpG sites one at a time, and propose a deep-learning survival model that weights CpG islands jointly against time to diagnosis, with SHAP values for interpretation. Applied to breast cancer.

## Why It Matters

Raised by [[sofia-reyes-calderon]] at a group journal club in March 2026 as an alternative to windows: model time to diagnosis as a continuous outcome. The group decided against it for the main Northvale analysis because a matched design with 410 cases is too small for this kind of model and windows are easier to explain. It remains the reference for why treating time to diagnosis explicitly matters ([[time-to-diagnosis-windows]]).

## Caveats

Complex model, modest sample sizes, and blood leucocyte methylation rather than cfDNA.

## Source Links

- [A Deep Survival EWAS approach estimating risk profile based on pre-diagnostic DNA methylation](https://doi.org/10.1371/journal.pcbi.1009959)
