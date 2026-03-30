---
type: Source
source_type: Internal document
date_accessed: 2026-03-20
belongs_to: "[[summer-internships-2026]]"
related_to:
  - "[[kofi-mensah]]"
  - "[[deconvolution-benchmark]]"
  - "[[spatial-transcriptomics]]"
_organized: true
---

# Intern Project Low-Count Spot Simulation

## Summary

One-page description of [[kofi-mensah]]'s internship topic, written by [[kenji-mori]] on 2026-03-20: simulate Visium HD spots at controlled count levels to show where deconvolution methods stop being reliable.

## Key Details

- Data: high-count spots from the [[visium-hd-pilot]], downsampled to 50, 100, 200 and 500 UMIs.
- Methods: four of the seven in the [[deconvolution-benchmark]], chosen for run time.
- Expected figure: error in estimated cell-type proportions against count level, one curve per method.
- Supervisor: Kenji (daily), Ines (formal).

## Why It Matters

Gives the benchmark a controlled experiment to support the failure mode Kenji saw on real low-count spots, and answers Reviewer 3 of the [[frontier-reviewer-reports-2025]] more directly.

## Source Location

Group repository, `internships/2026/mensah/README.md`.
