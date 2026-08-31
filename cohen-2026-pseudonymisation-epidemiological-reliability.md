---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1186/s12911-026-03360-0
doi: 10.1186/s12911-026-03360-0
pmid: "41715132"
licence: cc by
date_accessed: 2026-08-20
belongs_to: "[[data-access-policy-revision]]"
related_to:
  - "[[pseudonymisation-vs-anonymisation]]"
  - "[[consortium-transfer-dpia-draft]]"
  - "[[victor-lindahl]]"
_organized: true
---

# Quantifying the effects of pseudonymisation on epidemiological research reliability: a tailored evaluation using a clinical data warehouse

Cohen A et al. BMC Medical Informatics and Decision Making, 2026.

## Summary

Simulates re-identification attacks on a large hospital clinical data warehouse under several minimisation and pseudonymisation schemes, mainly random date shifting with different degrees of preserved temporal coherence, and measures the effect on six archetypal epidemiological study designs. Attack success depended heavily on the scenario: low when the attacker targets a random person, very high when the attacker knows the target is in the delivered cohort. Minimisation contributed much of the protection.

## Why It Matters

[[victor-lindahl]] cited it in the [[consortium-transfer-dpia-draft]]. The target-in-cohort scenario is exactly the Halo case: a receiving site knows that St Aldric surgical patients are in the dataset. It supports two choices in [[data-access-policy-draft-3]]: a minimum dataset per use (no exact dates, sampling times as days from surgery), and the position that pseudonymised data is personal data ([[pseudonymisation-vs-anonymisation]]).

## Caveats

Structured EHR data, not sequencing data. Date shifting is relevant for our clinical variables; it says nothing about re-identification from fragment-level cfDNA, which is a separate question ([[is-fragment-level-cfdna-data-personal-data]]).

## Source Links

- [DOI 10.1186/s12911-026-03360-0](https://doi.org/10.1186/s12911-026-03360-0)
