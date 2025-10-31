---
type: Project
status: Active
start: 2025-10-06
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[clonal-hematopoiesis]]"
  - "[[clonal-hematopoiesis-filter]]"
  - "[[molecular-epidemiology]]"
  - "[[lucas-brandt]]"
has:
  - "[[ch-cancer-risk-analysis-plan]]"
  - "[[ch-subcohort-variant-calls]]"
  - "[[should-ch-be-defined-at-vaf-2-or-1-percent]]"
  - "[[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]]"
  - "[[ch-analysis-meeting-2026-09-16]]"
_organized: true
---

# CH Cancer Risk Analysis

Does clonal hematopoiesis at baseline predict incident solid cancer? A cohort analysis of a random subcohort of 6,000 Northvale participants with buffy coat sequencing, led by [[lucas-brandt]]. Here clonal hematopoiesis is the exposure; in the MRD study the same calls are noise to remove ([[clonal-hematopoiesis]]).

## Outcome

Hazard ratios of incident solid cancer, overall and for the main sites, for CH at baseline, adjusted for age and smoking, with follow-up to 2025-12-31, written up as a short paper.

## Current State

- All 6,000 buffy coat samples sequenced with the CH panel; variant calls produced with the caller from [[clonal-hematopoiesis-filter]] and frozen in [[ch-subcohort-variant-calls]].
- CH prevalence at baseline among the 5,962 samples passing QC: 11.9% (708) at variant allele fraction 2% or more, 19.5% (1,164) at 1% or more.
- Definition settled on 2026-09-16: 2% is the primary threshold, 1% a prespecified secondary analysis ([[should-ch-be-defined-at-vaf-2-or-1-percent]]).
- Follow-up extended to 2025 by the [[registry-linkage-update]]: 861 incident solid cancers and 512 non-cancer deaths in the subcohort.
- Interim estimate with follow-up to 2023: hazard ratio 1.18 (95% CI 1.01 to 1.38) for any solid cancer, adjusted for age, sex and smoking status. The smoking adjustment is not yet good enough to trust this; see [[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]].

## Scope and Boundaries

Solid cancers only; haematological cancers are reported descriptively because CH is on their causal path. No Mendelian randomization here; [[jin-2026-chip-cancer-mendelian-randomization]] and [[levin-2022-smoking-genetics-clonal-hematopoiesis]] are context, and any MR follow-up would go to [[mendelian-randomization]] first. The variant caller is owned by [[hannah-lindqvist]] in [[clonal-hematopoiesis-filter]]; this project consumes its output and does not fork it ([[ch-calls-data-flow]]).

## Working Context

Two confounders dominate. Age drives both CH and cancer, so the time scale is attained age rather than time on study. Smoking drives lung and bladder cancer and is associated with some CH subtypes; the Northvale baseline questionnaire has pack-years only for 71% of ever-smokers ([[northvale-smoking-history-derivation]]). Non-cancer death is frequent in this age range and is a competing event; the analysis plan reports cause-specific hazards as the main estimate and cumulative incidence for interpretation ([[cause-specific-or-fine-gray-for-ch-cancer-risk]]).

## Next Actions

- [ ] Re-fit the models with 2025 follow-up and the 2% definition; produce the site-specific table (lung, colorectal, pancreatic, breast, prostate).
- [ ] Settle the smoking model: pack-years with multiple imputation against smoking status categories only.
- [ ] Run the 1% secondary analysis and the gene-specific models (DNMT3A, TET2, other).
- [ ] Draft the short paper; Lucas aims for a first draft by 2027-01.

## Open Questions

- [[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]]
- [[cause-specific-or-fine-gray-for-ch-cancer-risk]]
- [[can-ch-explain-part-of-the-northvale-methylation-signal]]

## Important Notes

- [[ch-cancer-risk-analysis-plan]]
- [[ch-subcohort-sampling-frame]]
- [[ch-vaf-threshold-comparison]]
- [[ch-calls-data-flow]]
- [[nguyen-2025-clonal-hematopoiesis-solid-cancers]]

## Maintenance Log

- 2026-09-21: 2025 follow-up received from the registry linkage update.
- 2026-09-16: VAF threshold decision (2% primary, 1% secondary).
- 2026-05-08: Variant calls for all 6,000 samples frozen.
- 2025-12-03: Analysis plan agreed with Mei-Lin Zhou.
- 2025-10-06: Project opened; subcohort sampling frame drawn.
