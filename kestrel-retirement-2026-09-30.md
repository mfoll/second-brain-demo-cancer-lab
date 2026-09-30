---
type: Event
date: 2026-09-30
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[kestrel-retirement-notice]]"
  - "[[kestrel-data-inventory]]"
  - "[[ilse-van-dorn]]"
_organized: true
---

# Kestrel Retirement 2026-09-30

Research IT powered off the Kestrel cluster on 2026-09-30, as announced in the [[kestrel-retirement-notice]]. Kestrel had run the group's analyses since 2017.

## What Happened

- Job submission stopped on 2026-09-16. [[amara-okonkwo]]'s last segmentation jobs on Kestrel's GPU nodes finished on 2026-09-15.
- Ines signed off the [[kestrel-data-inventory]] on 2026-09-29: of 186 TB, 41 TB migrated to Halyard, 112 TB in the cold archive, 33 TB deleted.
- [[ilse-van-dorn]] confirmed power-off at 17:00. Storage stays read-only for 30 days, until 2026-10-30, then is destroyed.

## Consequences

- The `kestrel` profile was removed from `varga-cfdna` in v1.2 ([[cfdna-pipeline-repository]]).
- The [[kestrel-job-submission-guide]] was archived the same day.
- Remaining work is verification, not transfer: cold-archive checksum checks are 80% done ([[archive-kestrel-data]]).

## Lessons

Starting the inventory in June, three months before the deadline, was the right call: 61 directories had no clear owner, and chasing former members took most of August. For the next retirement, keep an owner field on every top-level directory from the start ([[who-owns-what]]).
