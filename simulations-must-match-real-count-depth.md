---
type: Opinion
status: Active
confidence: High
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[deconvolution-simulated-datasets]]"
  - "[[benchmarks-must-report-failure-modes]]"
_organized: true
---

# Simulations Must Match Real Count Depth

## Stance

Simulated data used to benchmark a method must reproduce the count depth and sparsity of the real data the method will be used on, including its low tail. A simulation built at reference depth tests a regime nobody analyses.

## Why I Think This

Kenji's first simulated slides (October 2025) aggregated single cells from the reference at their native depth, so a pseudo-spot of three cells had several thousand UMIs. Every method looked excellent. [[amara-okonkwo]] compared the distribution with the pilot sections, where 8 µm bins have a median of 214 UMIs in resections and 128 in biopsies, and the simulations were redone with downsampling to 25 to 400 UMIs ([[deconvolution-simulated-datasets]]). Only then did the [[low-count-spot-collapse]] appear.

## Scope

Count-based simulations of sequencing assays: spatial, single-cell, cfDNA fragment counts. Less relevant for image-only benchmarks.

## What Would Change My Mind

A demonstration that a method's ranking is stable across depth, so that cheap deep simulations predict shallow behaviour. Our data say the opposite.

## Implications

Every simulation config in [[deconvolution-benchmark-config]] states the target depth distribution and the real dataset it was matched to.
