---
type: Source
source_type: Internal document
date_accessed: 2026-10-20
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-cluster]]"
  - "[[data-tiering]]"
_organized: true
---

# Halyard Storage Quota Statement

Monthly quota statement for the group's Halyard project space, issued by research IT. This note tracks the latest one, of 2026-10-20.

## Summary

141 TB used of the 200 TB quota in `/projects/varga`, up from 97 TB in August after the Kestrel transfers. Scratch usage 18 TB of 50 TB.

## Key Details

| Area | TB |
| --- | --- |
| raw | 88 |
| derived | 39 |
| images | 0.6 |
| shared | 13.4 |

- Largest single area: Northvale methylation panel raw data (31 TB).
- Projected 175 TB by 2027-03-31 if the atlas and the [[registry-linkage-update]] reruns go as planned.
- From April 2027 storage above 100 TB per group is charged; the forecast for [[ilse-van-dorn]] is due in December and depends on [[how-long-should-we-keep-raw-fastq-on-halyard]].

## Source Location

Research IT portal, "Usage > Storage > varga". Monthly PDFs in group drive `Admin/Compute/Halyard/quota/`.
