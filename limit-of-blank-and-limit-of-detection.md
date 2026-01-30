---
type: Concept
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[halo-wp4-analysis-plan]]"
  - "[[minimal-residual-disease]]"
  - "[[sun-hee-park]]"
_organized: true
---

# Limit Of Blank And Limit Of Detection

Two analytical limits that every Halo assay reports from the contrived tier.

- Limit of blank (LoB): the highest result expected from samples with no analyte. In practice for mutation assays, the rate of positive calls on 0% VAF samples; for score-based assays, a high percentile of the score on blanks.
- Limit of detection (LoD): the lowest analyte level detected reliably, conventionally in at least 95% of replicates, given the LoB.

## How Halo Uses Them

The [[halo-wp4-analysis-plan]] estimates both per assay from the contrived tier, with exact binomial intervals. With four replicates per VAF level, "4 of 4 detected" is consistent with a true detection rate as low as about 40%, so the [[halo-interim-benchmark-report-2026-10]] reports LoD as a range between levels rather than a point. [[sun-hee-park]] insisted on this.

## Caveats

- LoD depends on input: a 0.65 mL aliquot holds fewer genome copies than a full clinical draw, so Halo LoDs are conservative compared with each site's own validation.
- For MRD the clinically relevant false-positive source is often biological, not technical: clonal haematopoiesis variants pass any LoB estimated on cell-line blanks ([[clonal-hematopoiesis]]).
- For fragmentomics, LoB and LoD on contrived material are not meaningful because the material is not commutable ([[commutability-of-reference-materials]]).
