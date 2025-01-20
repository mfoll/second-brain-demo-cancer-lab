---
type: Topic
related_to:
  - "[[northvale-early-detection-study]]"
  - "[[ch-cancer-risk-analysis]]"
  - "[[cancer-early-detection]]"
_organized: true
---

# Molecular Epidemiology

Retrieval surface for the group's population-level work: molecular measurements in stored samples from healthy people, linked to later cancer outcomes. In practice this means the [[northvale-health-cohort]], the [[corvane-biobank]] and the [[northern-cancer-registry]].

## What lives here

Molecular epidemiology is where the lab's sequencing methods meet study design. The methods come from the cfDNA and clonal hematopoiesis work; the questions are epidemiological: what is the exposure, who is the comparison group, when was the sample taken relative to the outcome, and what else could explain an association.

Two active studies use the cohort:

- [[northvale-early-detection-study]]: cfDNA methylation as an early marker of pancreatic and colorectal cancer, in a nested case-control design.
- [[ch-cancer-risk-analysis]]: [[clonal-hematopoiesis]] as an exposure for incident solid cancer, in a random subcohort of 6,000.

## Design concepts

- [[nested-case-control-design]] and [[incidence-density-sampling]]
- [[conditional-logistic-regression]]
- [[competing-risks]]
- [[reverse-causation-in-prediagnostic-studies]]
- [[pre-analytical-storage-effects]]
- [[registry-reporting-lag]]

## People

[[maja-kovac]] and [[lucas-brandt]] are the group's epidemiologists. [[mei-lin-zhou]] runs the cohort, [[daniel-asante]] is the registry statistician, and [[paolo-ferrante]] holds the samples.

## Stances and open issues

- [[matching-on-blood-draw-date-is-worth-the-cost]]
- [[how-should-we-adjust-for-smoking-in-the-ch-cancer-risk-analysis]]
- [[does-storage-time-confound-the-northvale-methylation-signal]]

## Reading

Useful starting papers: [[partlett-2020-matched-nested-case-control-design]], [[kuo-2018-conditional-vs-unconditional-logistic-regression]], [[austin-2016-competing-risks-introduction]] and [[safizadeh-2026-inflammation-colorectal-reverse-causality]]. Mendelian randomization reading sits in its own exploration cluster, [[mendelian-randomization]].

## Current threads

- Whether storage time can explain any of the Northvale window pattern ([[does-storage-time-confound-the-northvale-methylation-signal]]). This is the most generic lesson the group is learning: in biobank studies, sample handling history is a covariate like any other ([[pre-analytical-storage-effects]]).
- How registry lag affects control selection and the last year of follow-up ([[registry-reporting-lag]]). The 2025 extract, the first under the institute [[registry-linkage-agreement]], gave a concrete example with three replaced controls.
- How competing non-cancer deaths should be presented in the CH paper ([[cause-specific-or-fine-gray-for-ch-cancer-risk]]).
- Whether the 97 new cancers in the 2025 extract justify a validation set, which would be the group's second Northvale biobank request ([[requesting-northvale-samples]]).

## How this area grew

Until 2025 the group worked almost entirely on patient samples. The Northvale collaboration, agreed with [[mei-lin-zhou]] in February 2025 ([[northvale-kickoff-2025-02-10]]), brought population design into the lab, and hiring [[maja-kovac]] and then [[lucas-brandt]] made it sustainable. The habits it brought, signed analysis plans before unblinding and dissent recorded in minutes, are spreading to the MRD work.
