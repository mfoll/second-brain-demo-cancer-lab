---
type: Source
source_type: Cohort resource
storage_system: Halyard governed storage
root_key: halyard_governed
relative_path: northvale/cohort/release-2026-09/
access: guarded-write
last_checked: 2026-10-12
date_accessed: 2025-02-03
belongs_to: "[[northvale-early-detection-study]]"
related_to:
  - "[[mei-lin-zhou]]"
  - "[[corvane-biobank]]"
  - "[[northern-cancer-registry]]"
  - "[[molecular-epidemiology]]"
_organized: true
---

# Northvale Health Cohort

## Summary

A prospective population cohort of 86,400 adults recruited between 2004 and 2009 at four recruitment centres, with a baseline questionnaire, physical measurements, and baseline plasma and buffy coat stored in the [[corvane-biobank]]. Cancer incidence and deaths come from linkage with the [[northern-cancer-registry]]. The principal investigator is [[mei-lin-zhou]]. The group uses it for the [[northvale-early-detection-study]] and the [[ch-cancer-risk-analysis]].

## Why It Matters

Stored blood drawn years before diagnosis is the only way to ask how early a molecular signal appears without waiting decades. Northvale is large enough to give 410 incident pancreatic and colorectal cases with usable plasma and a random subcohort of 6,000 with buffy coat DNA. Its weaknesses define much of our analysis work: one blood draw per person, samples stored 16 to 21 years, and a questionnaire designed before anyone thought about clonal hematopoiesis.

## Key Details

- Participants: 86,400; 53% women; age at recruitment 40 to 69 years (median 55).
- Blood: one baseline draw, EDTA, processed within four hours at three centres and within eight hours at the fourth (the centre that changed protocol in 2006). Plasma stored in 0.5 ml straws, typically 4 per participant; buffy coat as extracted DNA.
- Questionnaire: smoking (two versions of the pack-year question, 2004 to 2005 and 2005 onwards), alcohol, diet, medication, family history. Derived smoking variables in [[northvale-smoking-history-derivation]]; codebook in [[northvale-baseline-questionnaire-codebook]].
- Follow-up: registry linkage to 2023-12-31 in [[northern-cancer-registry-extract-2023]], extended to 2025-12-31 in [[northern-cancer-registry-extract-2025]]. Linkage rate 99.2% on the deterministic key.
- Incident cancers to 2025: 11,940 first primary cancers, of which 964 colorectal and 347 pancreatic (902 and 312 to 2023).
- Access: through the cohort steering group (chaired by Mei-Lin) for data and the biobank access committee for samples ([[requesting-northvale-samples]]). Our terms are in [[northvale-collaboration-agreement]].

## Caveats

- One baseline sample: no within-person change over time.
- Storage time and calendar time of draw are tied to recruitment period; any analysis comparing people drawn in different years must handle [[pre-analytical-storage-effects]].
- The fourth centre's longer processing delay raises genomic DNA contamination in plasma; recruitment centre is a matching factor for this reason.
- The cohort is mostly people who volunteered for a health study; incidence is lower than the general population for smoking-related cancers.

## Source Location

Governed storage on [[halyard-cluster]], root `halyard_governed`, path `northvale/cohort/release-2026-09/`. Read-only for the group; writes need [[yara-castellanos]] and an explicit request. The September 2026 release adds the 2025 registry follow-up. Earlier releases are kept for reproducibility of frozen analyses.
