---
type: Concept
maturity: Evergreen
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[group-software-inventory]]"
  - "[[every-group-tool-needs-two-maintainers]]"
_organized: true
---

# Software Bus Factor

The number of people who would have to leave before nobody can run, fix or explain a piece of software. The name is morbid; the idea is practical.

## How We Count It

For each tool in [[group-software-inventory]], a person counts towards the bus factor only if they have, in the last six months:

- run the tool end to end on real data from a clean checkout,
- fixed or reviewed a change to it, and
- could explain its main parameters to a new student.

Reading the code is not enough. Under this definition most of our tools were at one in 2025-11, consistent with the institute picture in [[corvane-rse-survey-2025]].

## Why It Matters In A Research Group

Contracts are short and staggered, so a bus factor of one means a planned, dated loss, not a hypothetical one ([[westner-2025-perilous-state-open-source-neuroscience-software]]). The single-cell CNV code reached zero when [[felix-achterberg]] left. Raising it costs time, roughly two days per tool per new maintainer by [[tobias-wren]]'s estimate, which is why it needs to be planned.

## Related

The group rule is [[every-group-tool-needs-two-maintainers]]. Open issue: [[who-maintains-group-software-after-people-leave]].
