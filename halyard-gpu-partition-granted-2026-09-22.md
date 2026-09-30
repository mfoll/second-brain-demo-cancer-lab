---
type: Event
date: 2026-09-22
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-gpu-allocation-request]]"
  - "[[spatial-pipeline-repository]]"
  - "[[ilse-van-dorn]]"
_organized: true
---

# Halyard GPU Partition Granted 2026-09-22

Research IT approved the group's request for the Halyard `gpu` partition on 2026-09-22, two months after it was submitted ([[halyard-gpu-allocation-request]]).

## Details

- Granted 6,000 GPU-hours to 2027-03-31, against 8,000 requested. The deconvolution benchmark reruns were judged optional.
- Members: [[tobias-wren]], [[amara-okonkwo]], [[kenji-mori]]; [[owen-mcallister]] to be added on arrival.
- Renewal decided in March 2027 on actual usage. [[ilse-van-dorn]] asked for a usage report in January.

## Consequences

- First `varga-spatial` run on Halyard GPU nodes on 2026-09-24; segmentation and deconvolution modules got their first tests in October ([[spatial-pipeline-repository]]).
- The spatial pipeline was the last blocker for the [[halyard-cluster-migration]] on the spatial side. The three-month slip of the migration is entirely explained by this wait.
- The 6,000 hours cover the atlas but not much else; see [[should-the-spatial-pipeline-stay-on-gpu]].
