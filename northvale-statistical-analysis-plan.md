---
type: Source
source_type: Internal document
storage_system: Group SharePoint
root_key: group_docs
relative_path: northvale/sap/northvale-lead-time-sap-v1.0.pdf
access: guarded-write
last_checked: 2026-10-14
date_accessed: 2026-02-26
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[maja-kovac]]"
  - "[[northvale-sap-amendment-1]]"
  - "[[northvale-sap-sign-off-2026-02-26]]"
_organized: true
---

# Northvale Lead-Time Statistical Analysis Plan v1.0

## Summary

The signed statistical analysis plan for the [[lead-time-analysis]] of the [[northvale-early-detection-study]]. Written by [[maja-kovac]], signed on 2026-02-26 by Maja, Ines and [[mei-lin-zhou]] before anyone saw case-control status linked to methylation scores. Amended once ([[northvale-sap-amendment-1]]).

## Key Details

- Primary exposure: per-sample methylation score from the 1,840-region panel, a weighted sum of region-level methylation fractions with weights fixed from tumour and normal tissue data in [[methylation-panel-design]], standardised on controls.
- Primary model: [[conditional-logistic-regression]] stratified on matched set; odds ratio per standard deviation.
- Windows: 0 to 1, 1 to 2, 2 to 5, more than 5 years from blood draw to diagnosis ([[time-to-diagnosis-windows]]).
- Main-model exclusion: deliberately left open in v1.0, to be fixed after a blinded look at the time-to-diagnosis distribution. Settled by the amendment.
- Secondary: site-specific models; adjustment for smoking and body-mass index; unconditional model adjusted for matching factors ([[kuo-2018-conditional-vs-unconditional-logistic-regression]]).
- Sensitivity: storage time within matched sets, genomic DNA contamination flag, recruitment centre 4 excluded.
- Missing covariates: multiple imputation ([[keogh-2018-multiple-imputation-nested-case-control]]).
- Exploratory: region-level penalised models ([[djordjilovic-2024-penalizedclr]]), not used to redefine the score.

## Caveats

The score weights come from tissue, not plasma, so the score is a fixed hypothesis rather than an optimised classifier. That was intentional.

## Source Location

Group SharePoint, `group_docs/northvale/sap/`, PDF with signatures; source LaTeX in [[northvale-lead-time-code-repository]].
