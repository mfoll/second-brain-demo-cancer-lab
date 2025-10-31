---
type: Question
status: Open
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[northvale-smoking-history-derivation]]"
  - "[[levin-2022-smoking-genetics-clonal-hematopoiesis]]"
  - "[[lucas-brandt]]"
_organized: true
---

# How should we adjust for smoking in the CH cancer risk analysis?

## Question

Smoking causes many solid cancers and is associated with some forms of clonal hematopoiesis. The Northvale questionnaire gives smoking status for nearly everyone but pack-years for only 71% of ever-smokers, missing mostly for early-recruited former smokers ([[northvale-smoking-history-derivation]]). Which adjustment is good enough for the hazard ratio to be credible?

## Options

1. Status only (never, former, current). Simple, complete; leaves residual confounding by intensity, which matters most for lung cancer.
2. Pack-years with multiple imputation. Uses all participants; relies on missing-at-random given questionnaire version.
3. Pack-years, complete cases only. Loses about 10% of the subcohort and is not missing at random.
4. Restrict to never-smokers as a sensitivity analysis. Clean but small (about 2,700 people).

## Current thinking

[[lucas-brandt]] favours option 2 as primary, with option 4 as a sensitivity analysis and lung cancer reported separately. Interim hazard ratio with status only: 1.18 (1.01 to 1.38) for any solid cancer. [[levin-2022-smoking-genetics-clonal-hematopoiesis]] suggests smoking affects CHIP-type clones less than chromosomal alterations, which would make smoking a weaker confounder for non-lung cancers.

## What would answer it

Comparing estimates across the four options with 2025 follow-up. If options 1, 2 and 4 agree for non-lung cancers, adopt option 2 and stop.

## Links

- [[ch-cancer-risk-analysis-plan]]
- [[mei-lin-zhou]] (questionnaire history)
