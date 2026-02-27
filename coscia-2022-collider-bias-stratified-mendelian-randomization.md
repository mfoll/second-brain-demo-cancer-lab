---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1007/s10654-022-00879-0
doi: 10.1007/s10654-022-00879-0
pmid: "35639294"
licence: cc by
date_accessed: 2026-02-23
belongs_to: "[[mendelian-randomization]]"
related_to:
  - "[[collider-bias]]"
  - "[[maja-kovac]]"
_organized: true
---

# Avoiding collider bias in Mendelian randomization when performing stratified analyses.

Coscia C et al., European Journal of Epidemiology, 2022.

## Summary

Stratifying an MR analysis by a variable that is itself affected by the exposure (a collider) can create bias. The authors propose stratifying instead on the "residual collider", the part of the variable not explained by the genetic instrument, and show in simulations that this keeps the stratified interpretation while avoiding the bias.

## Why It Matters

[[maja-kovac]] raised it after the 2026-02-19 call with [[hiroshi-tanabe]]: if we wanted CH effects by smoking stratum, smoking is plausibly affected by some CH instruments' pleiotropic paths, and naive stratification would mislead. The residual approach is the fallback if a stratified analysis is ever requested. Filed under [[collider-bias]].

## Caveats

Requires individual-level data, so it applies only to a one-sample Northvale analysis, which may be underpowered anyway ([[does-selection-into-northvale-bias-a-one-sample-mendelian-randomization]]).

## Source Links

- [Avoiding collider bias in Mendelian randomization when performing stratified analyses](https://doi.org/10.1007/s10654-022-00879-0)
