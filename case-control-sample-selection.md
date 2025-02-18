---
type: Project
status: Completed
start: 2025-02-03
end: 2025-10-17
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[incidence-density-sampling]]"
  - "[[paolo-ferrante]]"
  - "[[corvane-biobank]]"
has:
  - "[[northvale-matching-specification-v2]]"
  - "[[northvale-sample-selection-log]]"
  - "[[northvale-power-calculation]]"
  - "[[northvale-aliquot-manifest-2025]]"
_organized: true
---

# Case-Control Sample Selection

Selection of incident cases and matched controls for the [[northvale-early-detection-study]] by incidence-density sampling, and retrieval of their baseline plasma from the [[corvane-biobank]]. Completed on 2025-10-17.

## Outcome

A frozen list of 410 incident cases (174 pancreatic, 236 colorectal) and 820 controls, two per case, each with a 1 ml plasma aliquot delivered to the sequencing core and reconciled against the biobank manifest. Reached.

## Current State

- Closed. The case-control set is frozen in [[northvale-sample-selection-log]] (version tagged 2025-10-17).
- Later changes go through the [[registry-linkage-update]]: three controls were replaced in September 2026 after late registrations, recorded in [[northvale-control-replacement-log]]. The replacement rules from [[northvale-matching-specification-v2]] were reused unchanged.
- Unused aliquots (14) were returned to the biobank on 2025-11-04.

## Scope and Boundaries

This project covered eligibility, matching, the biobank request and shipment. Assay runs belonged to the sequencing core under [[methylation-panel-design]]; analysis belongs to [[lead-time-analysis]].

## Working Context

Cases: first primary pancreatic (ICD-10 C25) or colorectal (C18 to C20) cancer diagnosed after blood draw and before 2023-12-31 in the [[northern-cancer-registry-extract-2023]], with no previous cancer other than non-melanoma skin cancer, adenocarcinoma histology, and at least 1 ml of plasma left. Of 1,214 registered cancers, 945 met the clinical criteria and 410 had usable plasma; the full flow is in [[northern-cancer-registry-extract-2023]]. Controls were drawn from each case's risk set, people still under follow-up and cancer-free at the case's diagnosis date, matched on sex, recruitment centre, age at blood draw (within one year) and blood-draw date (within three months). Sampling was with replacement, so a person could be a control for several cases and could later become a case; see [[should-northvale-controls-be-sampled-with-replacement]].

The first specification ([[northvale-matching-specification-v1]]) matched on draw date within twelve months. [[maja-kovac]] tightened it to three months in May 2025 after reading [[enroth-2016-storage-time-biobank-plasma]], accepting that 19 cases would need the fallback rule (widen to six months). Two controls per case came from the [[northvale-power-calculation]] and the assay budget; see [[are-two-controls-per-case-enough-for-northvale]].

The biobank request followed what became [[requesting-northvale-samples]]. [[paolo-ferrante]] enforced the last-aliquot rule: no participant's final plasma aliquot could be used, which excluded 23 otherwise eligible cases before matching. Earlier Northvale projects had already used up the plasma of 489 others, which is the main reason the study has 410 cases rather than nearly a thousand.

## Important Notes

- [[northvale-matching-specification-v2]]
- [[northvale-sample-selection-log]]
- [[biobank-access-committee-2025-06-18]]
- [[northvale-sample-shipment-2025-09-23]]
- [[shin-2024-nested-case-control-sampling-without-replacement]]

## Lessons

- The registry extract was two years old when selection began. Late registrations surfaced later as control replacements; an earlier refresh would have avoided that. Recorded in [[registry-reporting-lag]].
- Matching on draw date cost about six weeks of extra iterations with the biobank and was worth it.

## Maintenance Log

- 2025-11-04: Unused aliquots returned; project closed in the vault.
- 2025-10-17: All 1,230 aliquots reconciled against the manifest; project Completed.
- 2025-09-23: Shipment from the biobank to the sequencing core.
- 2025-06-18: Biobank access committee approved the request.
- 2025-05-21: Matching specification v2 adopted (draw date within three months).
