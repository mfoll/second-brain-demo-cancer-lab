---
type: Source
source_type: Internal document
storage_system: Group Git repository
root_key: varga_lab_git
relative_path: low-vaf-benchmark/docs/caller-shortlist.md
access: read-only
last_checked: 2025-11-17
date_accessed: 2025-06-11
belongs_to: "[[low-vaf-caller-benchmark]]"
related_to:
  - "[[maruzani-2024-umi-aware-variant-callers]]"
  - "[[fgbio-documentation]]"
_organized: true
---

# Low-VAF Caller Shortlist 2025-06

Dmitri's shortlist of callers for the [[low-vaf-caller-benchmark|Low-VAF Caller Benchmark]], agreed 2025-06-11.

## Shortlist

1. Mutect2 on fgbio duplex consensus reads.
2. VarDictJava on consensus reads.
3. LoFreq on consensus reads.
4. A UMI-aware caller (UMI-VarCal) on raw reads.
5. Our in-house position-specific error model, used in the MRD study.

Consensus building with fgbio ([[fgbio-documentation]]) is fixed across callers so that only the calling step varies.

## Excluded

- Callers without a maintained release in the last two years.
- Commercial pipelines that cannot run in our container.

## Rationale

Choice informed by [[maruzani-2024-umi-aware-variant-callers]] and by what the Halo sites run, so that results transfer to the [[halo-cross-site-benchmark]].

## Source Location

Group Git repository, `varga_lab_git/low-vaf-benchmark/docs/caller-shortlist.md`.
