---
type: Note
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[northvale-case-control-codebook]]"
  - "[[incidence-density-sampling]]"
_organized: true
---

# Northvale Date Definitions

The dates the Northvale analyses use, defined once so that code, tables and text agree.

- **Blood-draw date** (`draw_date`): date of the baseline visit at which plasma and buffy coat were collected.
- **Diagnosis date**: the registry's incidence date, the earliest of pathology, clinical or death-certificate date per registry rules. Revised dates from a later extract replace earlier ones.
- **Index date** (`index_date`): the case's diagnosis date; each control in the matched set inherits it. Controls must be alive, cancer-free and under follow-up on the index date.
- **Time to diagnosis** (`ttd_years`): index date minus blood-draw date of the case, in years. Controls inherit their case's value and window ([[time-to-diagnosis-windows]]).
- **Storage time** (`storage_years`): assay date minus blood-draw date. For the 2025 runs, 16.1 to 21.4 years.
- **End of follow-up**: 2023-12-31 for case selection; 2025-12-31 for the CH analysis after the [[registry-linkage-update]].

Ages are computed at blood draw, in completed years for matching and in decimal years for models.
