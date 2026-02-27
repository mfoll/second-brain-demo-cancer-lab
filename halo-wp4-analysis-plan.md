---
type: Source
source_type: Internal document
date_accessed: 2026-02-26
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[sun-hee-park]]"
  - "[[limit-of-blank-and-limit-of-detection]]"
  - "[[halo-truth-set]]"
_organized: true
---

# Halo WP4 Analysis Plan

The statistical analysis plan for the Halo cross-site benchmark, version 1.0, written by Ines and [[sun-hee-park]] and accepted by the [[halo-steering-committee-2026-02-26]]. Version 1.1 (2026-06-24) added the lead-time requirement from the annual meeting.

## Summary

Pre-specifies, per tier of the [[halo-truth-set]], which assays are scored, on what endpoint, and with what statistics. The principle is that no assay is scored on a question it was not designed to answer, and that every assay's failures are reported.

## Key Details

- Tasks: 4.1 analytical performance (contrived tier), 4.2 harmonised fragmentomics features (with Thornvale), 4.3 cross-assay modelling ([[arjun-mehta]]), 4.4 clinical performance (patient and donor tiers, with WP6).
- Contrived tier: limit of blank from the 0% samples, limit of detection as the lowest VAF detected in at least 95% of replicates, with an exact binomial interval; with four replicates per level that interval is wide, which the plan states openly ([[limit-of-blank-and-limit-of-detection]]).
- Patient tier: sensitivity and specificity for recurrence by imaging, lead time over imaging, per assay and per cancer type; specificity also on the 20 healthy donors.
- Concordance between assays: Cohen's kappa on binary calls, Bland-Altman on VAF where comparable.
- Multiplicity: no formal correction across assays; the benchmark is descriptive.
- Pre-registration: the plan was deposited internally with a date stamp before unblinding.

## Caveats

The plan assumes WP4 can access patient-tier hub data. It does not foresee the Corvane policy block; a v1.2 will specify remote or federated analysis if needed ([[federated-cfdna-learning]]).

## Source Location

WP4 shared folder at the Brightwater hub, `wp4/sap/`; versioned copy in the [[halo-wp4-analysis-code-repository]] under `docs/`.
