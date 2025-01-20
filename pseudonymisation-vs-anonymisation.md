---
type: Concept
maturity: Evergreen
belongs_to: "[[serve-corvane-institute]]"
related_to:
  - "[[victor-lindahl]]"
  - "[[data-access-policy-draft-3]]"
  - "[[edgcumbe-2025-de-identification-terms]]"
_organized: true
---

# Pseudonymisation Vs Anonymisation

## Definition

> [!info]
> Pseudonymised data has direct identifiers replaced by a code, and someone, somewhere, holds the key or could re-link it; it remains personal data. Anonymous data cannot be linked back to a person by any party using reasonably likely means; it is no longer personal data. Aggregated data is not automatically anonymous.

## Why The Distinction Matters To Us

Almost everything the group works with is pseudonymised: Northvale data keyed by study ID, St Aldric samples keyed by MRD study number, registry extracts keyed by study ID. The key exists at the cohort team, the hospital or the registry. That keeps all of it in scope of the data protection rules and the [[corvane-data-access-policy-2023]], wherever it travels. Calling a feature table "anonymised" because it has no names is the most common mistake in our own emails.

## Practical Rules In The Group

- Use "pseudonymised" for anything at person level with a study ID.
- Use "aggregate" for tables of counts or summaries; treat them as anonymous only with small-cell suppression (cells under 5) and no rare-category combinations.
- Do not use "de-identified" in board papers: it means different things to different readers ([[edgcumbe-2025-de-identification-terms]]).
- Sequencing reads are never anonymous, because germline variants identify a person.

## Where It Shows Up

- [[data-access-policy-draft-3]] section 1, written with [[victor-lindahl]].
- [[is-fragment-level-cfdna-data-personal-data]]
- [[cohen-2026-pseudonymisation-epidemiological-reliability]] for why pseudonymised extracts can be re-identified when the attacker knows the target is in the cohort.
