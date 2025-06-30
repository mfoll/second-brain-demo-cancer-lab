---
type: Question
status: Open
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[clonal-hematopoiesis]]"
  - "[[hannah-lindqvist]]"
  - "[[panel-of-normals]]"
  - "[[buffy-coat-sequencing-cost-estimate-2025-11]]"
_organized: true
---

# Do We Still Need Matched Buffy Coat Sequencing?

Should the remaining 152 St Aldric patients, and future MRD cohorts, get matched buffy coat sequencing to remove clonal hematopoiesis variants from cfDNA calls, or is a panel-of-normals approach enough?

## Why It Matters

> [!question]
> Matched buffy coat sequencing costs about 180 EUR per sample, about 27,000 EUR for the 152 remaining St Aldric patients and more for any Halo validation set; a panel of normals is nearly free but missed 16% of CH variants in our pilot. The answer sets the budget and the credibility of every MRD call.

It also decides how we answer Reviewer 1 on the [[mrd-manuscript|MRD Manuscript]], who asked how CH was excluded for the patients without matched sequencing ([[mrd-manuscript-decision-2026-07-14]]), and what we recommend in the [[mrd-review-article|MRD Review Article]].

## What We Know

- **Pilot** (60 patients, [[ch-buffy-coat-pilot-results-2026-01]]): 31% of plasma variants passing the caller were present in buffy coat. Without any filter, 9 of the 60 patients would have had at least one false molecular recurrence call.
- **Panel of normals** ([[ch-panel-of-normals-v1]]), built from Northvale CH calls of [[ch-cancer-risk-analysis]]: recovered 84% of the buffy-coat-confirmed CH variants. The misses were mostly private DNMT3A and TET2 variants below 1% VAF. With the panel alone, 2 of the 60 patients would still have had a false molecular recurrence.
- **Cost** ([[buffy-coat-sequencing-cost-estimate-2025-11]]): about 180 EUR per sample, of which library and capture are about 70 EUR and sequencing about 110 EUR at the depth needed to see 0.5% VAF clones.
- **Literature**: paired plasma and buffy coat series show CH variants in a large share of patients and in clinically important genes ([[magee-2025-cfdna-variants-tumour-or-ch-origin]]). Plasma-only classifiers using fragment features report high accuracy without white-cell sequencing ([[brown-2025-fragmentomic-variant-origin]], [[arango-argoty-2025-metach-cfdna-ch-variants]]), but on assays and populations different from ours.

## Positions

- [[dmitri-halvorsen|Dmitri]]: sequence everyone; a false recurrence call is worse than the cost. Recorded as the Opinion [[matched-normal-sequencing-is-cheaper-than-false-recurrence]], which Ines broadly shares.
- [[hannah-lindqvist|Hannah]]: a hybrid may be enough, with buffy coat only for patients who have any non-tumour-informed plasma variant below 2% VAF. In the pilot that would have meant sequencing 23 of 60 patients.
- Ines: undecided between full and hybrid; wants the hybrid's miss rate measured on the pilot before deciding.

## What Would Answer It

1. Simulate the hybrid rule on the 60 pilot patients and count false recurrences it would let through.
2. Test a fragment-length variant-origin feature on the pilot (Hannah, after Brown et al.).
3. Check whether the [[how-large-must-the-ch-panel-of-normals-be|panel-of-normals size]] explains the misses: if a larger panel catches them, the hybrid becomes more attractive.

Decision expected at the November 2026 MRD study meeting.

## Related

- [[clonal-hematopoiesis-filter]]
- [[ch-filter-design-meeting-2025-11-05]]
- [[clonal-hematopoiesis]]
