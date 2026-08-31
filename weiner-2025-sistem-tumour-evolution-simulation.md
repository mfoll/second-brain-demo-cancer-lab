---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1093/bioinformatics/btaf634
doi: 10.1093/bioinformatics/btaf634
pmid: "41275416"
licence: cc by
date_accessed: 2026-08-17
belongs_to: "[[tumour-evolution-symposium-2026]]"
related_to:
  - "[[tumour-evolution]]"
  - "[[low-vaf-caller-benchmark]]"
_organized: true
---

# SISTEM: simulation of tumor evolution, metastasis, and DNA-seq data under genotype-driven selection.

Weiner S, Bansal MS. Bioinformatics, 2025.

## Summary

Open-source Python framework that simulates tumour evolution and cell migration at single-cell resolution under somatic selection, using agents rather than neutral coalescent or simple birth-death models. It outputs mutation profiles, read counts and sequencing reads with ground-truth lineages and migration graphs, and lets fitness depend on events from point mutations to whole-genome duplication.

## Why It Matters

Ines read it while preparing to introduce [[katarina-vukovic]]'s keynote, to have a current example of simulation tools in the field. It also has a practical use: [[tobias-wren]] wondered whether simulated reads with known subclonal structure could stand in for the missing truth set in the paused [[low-vaf-caller-benchmark]]. Ines's view: useful for debugging, not a substitute for the [[halo-truth-set]], because simulators do not reproduce cfDNA fragment biology.

## Caveats

Simulated data only reflect the error models built into them.

## Source Links

- [SISTEM](https://doi.org/10.1093/bioinformatics/btaf634)
