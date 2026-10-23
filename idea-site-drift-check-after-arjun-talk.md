---
type: Note
date: 2026-10-16
_organized: false
---

# Idea after Arjun's talk on site drift

Arjun's Halo ML seminar today: their models drift most where sites changed extraction chemistry, and they only notice after scoring. Thought for our stacked model: before scoring anything at a new site, compare the healthy-donor length profile to St Aldric bridging samples and refuse to score if the modal-length shift is above ~2 bp?? Would be a pre-specified gate, not tuning, so maybe OK under the lock rule. Motif side probably doesn't need it.

Ask Sofia if this belongs in model card v3 or as a separate QC step. Also: is 2 bp sensible, the kit lot shift was ~3 bp
