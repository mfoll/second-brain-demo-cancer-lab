---
type: Topic
related_to:
  - "[[tumour-evolution-research]]"
  - "[[spatial-transcriptomics]]"
  - "[[minimal-residual-disease]]"
_organized: true
---

# Tumour Evolution

Retrieval surface for how tumours change over time: clonal structure, phylogenies, and selection under treatment. It cuts across the group's studies; the portfolio itself is in [[tumour-evolution-research]].

## Where It Shows Up in Our Work

- [[colorectal-metastasis-atlas]]: which subclones and niches survive chemotherapy, read from paired pre- and post-treatment sections ([[paired-pre-post-treatment-design]]).
- [[single-cell-cnv-pilot]]: single-cell copy number against bulk multi-region trees; not worth the cost in 2025.
- [[pancreatic-cfdna-mrd-study]]: recurrence as the visible end of residual clones, read from cfDNA.
- [[clonal-hematopoiesis-filter]] and [[ch-cancer-risk-analysis]]: clonal expansion in blood, as noise in one study and an exposure in the other.

## Core Ideas

- [[multi-region-bulk-phylogeny]]: our default way to build trees.
- [[chemotherapy-induced-clonal-selection]]: sweep, drift or niche remodelling.
- [[tumour-regression-grade]]: the histological response scale we stratify by.

## Literature Entry Points

- Evolution under therapy: [[shi-2024-crlm-evolution-under-chemotherapy]], [[simhadri-2024-braf-colon-clonal-dynamics]].
- Single-cell copy-number phylogenies: [[sollier-2023-compass]], [[liu-2024-nestedbd]], [[weiner-2025-dice-copy-number-phylogenies]], [[ivanovic-2025-cnrein]].
- Spatial subclones: [[denisenko-2024-ovarian-subclones-spatial]], [[zhang-2025-slidecna]].

## Open Questions

- [[can-spatial-cnv-replace-single-cell-dna]]
- [[are-pre-chemo-core-biopsies-representative]]

## Decisions on Record

- Bulk multi-region sequencing stays the default for tree building; single-cell copy number was not adopted in 2025 at about 11,500 EUR per tumour ([[single-cell-cnv-pilot-review-2025-07-24]]). Reconsider below about 3,000 EUR per tumour or for subclones under 5%.
- In the atlas, clones are inferred from spatial expression and interpreted against pathology annotations ([[pathologist-annotations-anchor-spatial-clusters]]).
- Apparent new subclones after chemotherapy are reported as "not detected before", because a core biopsy may miss them ([[are-pre-chemo-core-biopsies-representative]]).

## How to Use This Topic

For the portfolio and who leads what, go to [[tumour-evolution-research]]. For method details, start from the Core Ideas above.

The topic also connects to early detection: pre-diagnostic signals in the [[northvale-early-detection-study]] are, in evolutionary terms, the earliest visible traces of a clone that has already expanded. That framing is used in grant writing ([[aurora-programme-grant-2027]]) rather than in analysis.
