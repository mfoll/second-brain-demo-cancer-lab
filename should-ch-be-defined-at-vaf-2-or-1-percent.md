---
type: Question
status: Answered
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[ch-analysis-meeting-2026-09-16]]"
  - "[[ch-vaf-threshold-comparison]]"
  - "[[clonal-hematopoiesis]]"
_organized: true
---

# Should CH be defined at VAF 2% or 1%?

## Question

Our CH panel is deep enough to call variants below 2% variant allele fraction, the conventional CHIP threshold. Should the [[ch-cancer-risk-analysis]] define CH at 1% instead?

## Current Answer

> [!info]
> Decided on 2026-09-16: VAF 2% or more is the primary definition; 1% or more is a prespecified secondary analysis. Fixed in the analysis plan before the 2025 follow-up was opened.

## Why

- Comparability: almost all published cohort analyses use 2% ([[xi-2025-chip-gastric-cancer-uk-biobank]], [[lai-2025-chip-breast-cancer-uk-biobank]]).
- Reliability: replicate concordance is 97% at 2% or more but 84% between 1% and 2% ([[ch-vaf-threshold-comparison]]).
- The interim estimate is weaker at 1% (1.11 against 1.18), which could be dilution by noisier calls or a dose-response; the secondary analysis keeps both visible.

## Note on the other use of the same calls

In the [[clonal-hematopoiesis-filter]] the same caller uses a lower threshold, because there the aim is to remove every blood-derived variant from cfDNA. Different purpose, different threshold, same calls ([[ch-calls-data-flow]]).

## Revisit if

A technical replicate study at higher depth raises concordance between 1% and 2% above 95%.
