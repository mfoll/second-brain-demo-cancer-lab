---
type: Concept
maturity: Evergreen
belongs_to: "[[ch-cancer-risk-analysis]]"
related_to:
  - "[[cause-specific-or-fine-gray-for-ch-cancer-risk]]"
  - "[[austin-2016-competing-risks-introduction]]"
  - "[[molecular-epidemiology]]"
_organized: true
---

# Competing Risks

A competing risk is an event that prevents the event of interest from happening. For incident cancer in an older cohort, death from other causes is the main one: someone who dies of heart disease at 70 cannot develop cancer at 75.

## Two questions, two models

- **Cause-specific hazard**: the rate of the event among people still event-free. Answers aetiological questions (does CH change the rate of cancer?). Competing events are treated as censoring.
- **Subdistribution hazard (Fine-Gray)** and the **cumulative incidence function**: the probability of the event by a given time, accounting for competing events. Answers prediction and absolute-risk questions.

The complement of the Kaplan-Meier estimate overstates incidence when competing events occur; use the cumulative incidence function instead ([[austin-2016-competing-risks-introduction]]). Subdistribution hazard ratios are often misread as rate ratios ([[austin-2017-fine-gray-reporting]]).

## Where it bites in our work

In the [[ch-cancer-risk-analysis]], CH is linked to cardiovascular death, so CH carriers are removed from the cancer risk pool faster. A raised cause-specific hazard can therefore coexist with a smaller difference in cumulative incidence. The death causes in the 2025 extract ([[registry-linkage-variable-specification]]) are what makes this analysis possible.
