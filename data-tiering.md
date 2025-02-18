---
type: Concept
belongs_to: "[[lab-data-management-plan]]"
related_to:
  - "[[group-data-management-plan]]"
  - "[[how-long-should-we-keep-raw-fastq-on-halyard]]"
  - "[[halyard-cluster]]"
_organized: true
---

# Data Tiering

Placing each dataset on the cheapest storage that still meets how often and how fast it must be read.

## Our Tiers

| Tier | Where | For | Retrieval |
| --- | --- | --- | --- |
| Hot | Halyard scratch | Running jobs, work directories | Immediate, purged after 30 days |
| Warm | Halyard project space | Raw and derived data in active projects | Immediate, charged above 100 TB from 2027-04 |
| Cold | Institute cold archive | Finished projects, Kestrel archive | 2 to 5 working days per batch |

## Rules We Apply

- Nothing irreplaceable lives only in hot storage.
- Intermediates that a released pipeline can regenerate are not kept in warm storage after a project ends, as the [[group-data-management-plan]] allows.
- Moving to cold storage needs a manifest with checksums ([[archive-kestrel-data]]).

## Open Point

When raw data moves from warm to cold is not yet fixed; see [[how-long-should-we-keep-raw-fastq-on-halyard]].
