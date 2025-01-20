---
type: Person
belongs_to: "[[lead-tumour-evolution-group]]"
related_to:
  - "[[summer-internships-2026]]"
  - "[[kenji-mori]]"
  - "[[deconvolution-benchmark]]"
_organized: true
---

# Kofi Mensah

MSc intern in the group from 2026-06-01 to 2026-08-28, from a computational biology master's programme. Former member.

## Role

Kofi simulated low-count Visium HD spots to test how deconvolution methods behave as counts drop ([[intern-project-low-count-spot-simulation]]). Daily supervisor [[kenji-mori]].

## Work Done

- Wrote a simulator that downsamples real spots from the [[visium-hd-pilot]] to fixed count levels while keeping the known cell-type mix from adjacent high-count spots.
- Ran four of the seven benchmarked methods on the simulated spots. His curves showed the same failure Kenji had seen on real data: as counts fall, two methods assign spots to the most abundant cell type without any warning. This became a supplementary experiment in the [[deconvolution-benchmark]] and supports [[benchmarks-must-report-failure-modes]].
- Final talk at the [[intern-final-talks-2026-08-26]].

## Notes

Kofi will be acknowledged in the benchmark preprint; Kenji proposed middle authorship, which Ines agreed given the simulation is a distinct contribution.
