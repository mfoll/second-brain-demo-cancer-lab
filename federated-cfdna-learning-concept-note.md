---
type: Source
source_type: Internal document
date_accessed: 2026-10-14
belongs_to: "[[federated-cfdna-learning]]"
related_to:
  - "[[arjun-mehta]]"
  - "[[leila-farouk]]"
  - "[[halo-data-flow-and-transfer-constraints]]"
_organized: true
---

# Federated cfDNA Learning Concept Note

Draft v0.3 of the concept note requested by the [[halo-steering-committee-2026-09-17]], written by [[arjun-mehta]] and Ines, with a section by [[leila-farouk]] on the two-site set-up she uses between Corvane and Thornvale. Five pages, shared with [[sun-hee-park]] on 2026-10-14.

## Summary

Proposes two stages. Stage 1, federated evaluation: a locked model in a container runs at the Brightwater hub on patient-tier data; only aggregate metrics return. Stage 2, federated training: a cross-assay model on a common feature layer, trained with federated averaging across the sites that can produce the features.

## Key Details

- Stage 1 cost: about four weeks of WP4 effort and compute at Brightwater; no new budget line if hub compute is used.
- Stage 2 cost: one postdoc year spread across WP4 and Westmere; needs an amendment to the work plan.
- Toolchain options: [[flower-federated-learning-framework]] or FeatureCloud with fedflow ([[featurecloud-platform]], [[weilguny-2026-fedflow-featurecloud]]).
- Privacy: secure aggregation by default; differential privacy considered for stage 2 but likely to cost accuracy with this few samples ([[ay-2026-privacy-enhancing-technologies-biomedical-ai]]).
- Legal prerequisites listed as open: whether aggregate metrics and model weights count as personal data, and who owns jointly trained models ([[who-owns-models-trained-on-halo-data]]).

## Caveats

Ines added a paragraph stating that stage 1 does not replace the consortium transfer clause for the [[mrd-manuscript]] validation; it is a fallback. Arjun is more optimistic. The disagreement is visible in the draft on purpose.

## Source Location

WP4 folder at the Brightwater hub, `wp4/federated/concept-note-v0.3.docx`.
