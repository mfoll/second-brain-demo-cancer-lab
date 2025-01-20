---
type: Person
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[colorectal-metastasis-atlas]]"
  - "[[deconvolution-benchmark]]"
  - "[[kenji-mori]]"
  - "[[owen-mcallister]]"
_organized: true
---

# Amara Okonkwo

Postdoc in the group and lead analyst of the [[colorectal-metastasis-atlas]]. She ran the [[visium-hd-pilot]], designed the atlas analysis around 8 µm bins, and co-supervises [[kenji-mori]] on the [[deconvolution-benchmark]].

## Role

- Owns the atlas analysis plan, the spatial pipeline's scientific choices, and the atlas paper as first author.
- Day-to-day contact for [[benedikt-kraus]] on section QC and pathology annotations, and for the sequencing core on batch scheduling.
- Reviews Kenji's benchmark design and code; she spotted in November 2025 that the first simulations used unrealistically deep spots, which led to [[simulations-must-match-real-count-depth]].

## How We Work Together

Weekly one-to-one with Ines on Thursdays, monthly atlas meeting with Kenji and Benedikt. Amara prefers decisions written down with the evidence attached; most atlas Events in the vault are from her notes. She is direct about scope and has twice argued successfully against adding a second platform to the atlas.

Technical decisions on the spatial pipeline go through her before [[tobias-wren]] implements them in Nextflow. She tested the GPU segmentation step on Halyard the week the partition was granted.

## Current Threads

- Sequencing batch 3 and freezing the analysis set ([[atlas-sequencing-batch-plan]]).
- Whether bin2cell segmentation enters the main analysis ([[should-the-atlas-use-bin2cell-segmentation]]).
- Representativeness of pre-chemotherapy core biopsies ([[are-pre-chemo-core-biopsies-representative]]).
- Onboarding [[owen-mcallister]] from 2027-01-11 ([[owen-atlas-onboarding-plan]]); she sat on the interview panel in [[postdoc-hiring-2026]].
- Career: her fellowship application is planned for 2027; the atlas paper is the anchor publication.

## Links

- [[atlas-progress-review-2026-10-07]]
- [[visium-hd-pilot-decision-2025-08-28]]
- [[pathologist-annotations-anchor-spatial-clusters]]

## History With the Group

Amara joined in late 2024 from a single-cell immunology background and took the atlas from an idea to a funded study. She wrote the pilot stop rule at the [[atlas-kickoff-2025-03-03]], ran the [[visium-hd-pilot]] on time, and drafted the atlas work packages for the [[frontier-starting-grant]] ([[frontier-grant-atlas-workplan]]).
