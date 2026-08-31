---
type: Source
source_type: Internal document
date_accessed: 2026-08-31
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[snapshot-testing]]"
  - "[[forer-2025-nf-test-pipeline-reliability]]"
_organized: true
---

# nf-test Coverage Report 2026-08

Summary of test coverage across the two group pipelines at the end of August 2026, prepared by [[tobias-wren]] for the [[group-retreat-2026]] compute session.

## Summary

31 of 41 local modules (76%) had at least one nf-test test: 24 of 27 in `varga-cfdna` and 7 of 14 in `varga-spatial`. Both pipelines had an end-to-end test on the `test` profile; the spatial one excluded GPU steps.

## Key Details

- Untested modules were mostly GPU segmentation and deconvolution, untestable without the Halyard `gpu` partition at the time.
- Snapshot tests caught two silent changes in 2026: a samtools update that altered duplicate flags, and a rounding change in the end-motif table ([[snapshot-testing]]).
- Median CI time per merge request: 11 minutes with only affected tests run.

## Caveats

"Coverage" here means modules with at least one test, not line coverage. The retreat slide showed 78% because it counted two modules under refactor as tested; use 76% if quoting. Coverage reached 83% (34 of 41) in October after the first spatial GPU tests were added.

## Source Location

Group drive `Pipelines/reports/nf-test-coverage-2026-08.pdf`.
