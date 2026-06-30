---
type: Project
status: Active
start: 2026-06-15
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[registry-linkage-agreement]]"
  - "[[daniel-asante]]"
has:
  - "[[northern-cancer-registry-extract-2025]]"
  - "[[registry-linkage-variable-specification]]"
  - "[[northvale-control-replacement-log]]"
  - "[[registry-extract-received-2026-09-08]]"
_organized: true
---

# Registry Linkage Update

Extension of cancer incidence and death follow-up for Northvale participants from 2023-12-31 to 2025-12-31 through the [[northern-cancer-registry]], using the institute-level [[registry-linkage-agreement]] signed on 2025-10-31. The update serves both the [[northvale-early-detection-study]] and the [[ch-cancer-risk-analysis]].

## Outcome

A validated 2025 extract linked to the whole cohort, the nested case-control set checked against it, and the CH subcohort follow-up extended, with any changes to cases or controls documented and approved by the cohort PI.

## Current State

- Extract received on 2026-09-08 ([[registry-extract-received-2026-09-08]]); described in [[northern-cancer-registry-extract-2025]].
- Linkage rate 99.2% of the 86,400 participants on the deterministic key; 412 unmatched records resolved by the registry's probabilistic step, 37 left unlinked and treated as lost to follow-up at last contact.
- Nested set check done: three controls had a diagnosis registered late with a date before their index date and were replaced; four case diagnosis dates moved by less than 60 days, no case changed window. See [[northvale-control-replacement-log]].
- 97 new pancreatic and colorectal cases diagnosed in 2024 and 2025 are not part of the current study. Whether to add them is open with [[mei-lin-zhou]].
- The CH subcohort gained 119 incident solid cancers and 74 deaths; handed to [[lucas-brandt]] on 2026-09-21.

## Scope and Boundaries

In scope: the extract request, variable specification, validation, and the impact on the Northvale analyses. The agreement itself belongs to [[registry-linkage-agreement]] under the institute service; the governance of the linked file follows the data protection impact assessment held by [[victor-lindahl]].

## Working Context

The first linkage (extract to 2023) was done under a cohort-specific approval before the institute agreement existed ([[northern-cancer-registry-extract-2023]]). Registration is not complete for the most recent year: [[daniel-asante]] estimates about 95% completeness twelve months after year end, rising above 99% at 24 months ([[registry-reporting-lag]]). That is why the 2023 extract missed the three late diagnoses among controls, and why the 2025 extract will itself be refreshed in 2027 before any analysis uses 2025 incidence as final.

Death follow-up comes from the same extract through the registry's link to death certificates. For the CH analysis this matters because non-cancer death is a competing event ([[competing-risks]]).

## Next Actions

- [ ] Agree with Mei-Lin and Ines whether the 97 new cases become a second case set or a validation set; record the decision in the umbrella project.
- [ ] Confirm with Daniel the refresh date for a 2027 extract and add it to the agreement's schedule.
- [ ] Archive the 2023 extract per the retention rule in [[registry-linkage-variable-specification]] once both analyses have migrated.

## Open Questions

- [[does-registry-lag-misclassify-recent-northvale-controls]] (answered; check again in 2027)
- [[cause-specific-or-fine-gray-for-ch-cancer-risk]]

## Important Notes

- [[northern-cancer-registry-extract-2025]]
- [[registry-linkage-variable-specification]]
- [[lendle-2025-record-linkage-complexity]]
- [[langner-2019-registry-linkage-mortality-validation]]

## Maintenance Log

- 2026-09-21: Updated follow-up delivered to the CH analysis.
- 2026-09-15: Nested set check complete; three controls replaced.
- 2026-09-08: 2025 extract received.
- 2026-07-03: Extract request and variable specification sent to the registry.
- 2026-06-15: Project opened.
