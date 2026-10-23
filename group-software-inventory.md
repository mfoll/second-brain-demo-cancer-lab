---
type: Source
source_type: Internal spreadsheet
date_accessed: 2026-10-05
belongs_to: "[[research-software-sustainability]]"
related_to:
  - "[[software-bus-factor]]"
  - "[[tobias-wren]]"
  - "[[nextflow-pipeline-migration]]"
_organized: true
---

# Group Software Inventory

Spreadsheet listing every tool and pipeline the group's results depend on, kept by [[tobias-wren]] since 2025-11 and reviewed each quarter.

## Columns

Tool, purpose, language or workflow manager, repository, test coverage, container image, primary and secondary maintainer, maintainers' contract end dates, and [[software-bus-factor]].

## State On 2026-10-05

| Tool | Bus factor 2025-11 | Bus factor 2026-10 |
|---|---|---|
| cfDNA preprocessing pipeline | 1 | 2 |
| Fragmentomics feature extraction | 1 | 2 |
| CH variant calling and filter | 1 | 2 |
| Spatial preprocessing pipeline | 2 | 2 |
| Deconvolution benchmark harness | 1 | 1 |
| Single-cell CNV code (archived) | 0 | 0 |

The benchmark harness stays at one because [[kenji-mori]] is still changing it before the preprint; a second maintainer is planned once it is frozen. The CNV code is archived and rerunnable but nobody maintains it, which is accepted.

## Why It Matters

Evidence base for [[every-group-tool-needs-two-maintainers]] and input to [[who-maintains-group-software-after-people-leave]].

## Source Location

Group drive, `Computing/software-inventory.xlsx`.
