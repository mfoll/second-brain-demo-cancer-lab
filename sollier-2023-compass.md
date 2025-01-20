---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1038/s41467-023-40378-8
doi: 10.1038/s41467-023-40378-8
pmid: "37582954"
licence: cc by
date_accessed: 2025-01-20
belongs_to: "[[single-cell-cnv-pilot]]"
related_to:
  - "[[tumour-evolution]]"
  - "[[can-spatial-cnv-replace-single-cell-dna]]"
_organized: true
---

# COMPASS: joint copy number and mutation phylogeny reconstruction from amplicon single-cell sequencing data.

Sollier E et al., Nature Communications, 2023.

## Summary

Most single-cell phylogeny methods handle either point mutations or large copy-number changes, and few work on targeted sequencing. COMPASS infers a joint phylogeny of both from targeted single-cell DNA data. Evaluated on simulations and applied to datasets including 123 patients with acute myeloid leukaemia, it detected clonal copy-number changes confirmed by bulk data and subclonal ones that needed single-cell resolution.

## Why It Matters

Read at the start of the [[single-cell-cnv-pilot]] as the alternative design: a targeted panel giving mutations and copy number together. We stayed with low-pass whole-genome because colorectal copy-number changes are large and a panel would need designing. If single-cell is reopened for rare resistance subclones, a targeted joint approach like this is the likelier route.

## Caveats

Mostly blood cancers with amplicon panels; solid-tumour nuclei behave differently.

## Source Links

- [DOI 10.1038/s41467-023-40378-8](https://doi.org/10.1038/s41467-023-40378-8)
