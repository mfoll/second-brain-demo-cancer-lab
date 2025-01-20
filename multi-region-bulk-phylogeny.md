---
type: Concept
maturity: Evergreen
belongs_to: "[[tumour-evolution-research]]"
related_to:
  - "[[tumour-evolution]]"
  - "[[single-cell-cnv-pilot]]"
_organized: true
---

# Multi-Region Bulk Phylogeny

Reconstructing a tumour's clonal history from several bulk samples taken from different regions of the same tumour. Each region is a mixture of clones; cancer cell fractions of mutations and copy-number changes across regions constrain which clones exist and how they nest.

## How We Do It

Four to six regions per tumour, whole-genome sequencing at about 60x tumour and 30x normal, clustering of cancer cell fractions, then tree building under the infinite-sites assumption with copy-number-aware corrections. The scripts moved into the Nextflow pipelines in 2026 ([[nextflow-pipeline-migration]]).

## What It Resolves and What It Does Not

- Resolves major clades and their ordering reliably when regions differ in composition.
- Does not separate clones that co-occur at similar fractions in every region, and cannot see subclones below a few percent.
- The [[single-cell-cnv-pilot]] tested whether single-cell copy number fills those gaps. In four tumours it recovered the same major clades and added one minor subclone; not worth the cost for our questions ([[single-cell-cnv-pilot-report]]).

## Related Approaches

Single-cell copy-number trees ([[weiner-2025-dice-copy-number-phylogenies]], [[liu-2024-nestedbd]]) and spatial copy-number inference from expression ([[zhang-2025-slidecna]]), which the atlas uses instead.
