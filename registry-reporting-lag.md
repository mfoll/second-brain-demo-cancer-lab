---
type: Concept
belongs_to: "[[registry-linkage-update]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[does-registry-lag-misclassify-recent-northvale-controls]]"
  - "[[daniel-asante]]"
_organized: true
---

# Registry Reporting Lag

The delay between a cancer diagnosis and its appearance in a registry extract. Notifications from pathology, hospitals and death certificates arrive over months to years, so the most recent calendar years of any extract are incomplete and later corrected.

## Working figures for the Northern Cancer Registry

From [[daniel-asante]]: about 95% of a year's cases are registered twelve months after year end, more than 99% after 24 months. Death-certificate-initiated registrations, more common for pancreatic cancer, come last.

## Consequences

- Cases: incidence in the final year is undercounted; analyses should not treat it as final.
- Controls: a person with an unregistered diagnosis can be selected as a cancer-free control. This happened to three Northvale controls ([[northvale-control-replacement-log]]).
- Dates: diagnosis dates are revised as more notifications arrive; 1.8% of 2023 dates changed in the 2025 extract.

## Rule

Avoid index dates in the last 24 months of an extract, or refresh before analysis ([[does-registry-lag-misclassify-recent-northvale-controls]]).
