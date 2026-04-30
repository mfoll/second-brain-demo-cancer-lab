---
type: Procedure
status: Active
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[halyard-gpu-allocation-request]]"
  - "[[halyard-cluster]]"
  - "[[ilse-van-dorn]]"
_organized: true
---

# Request Halyard GPU Time

How to get GPU partition access on Halyard for the group or add a person to the existing allocation. Based on the 2026 request, which took two months ([[halyard-gpu-allocation-request]]).

## Adding A Person To The Existing Allocation

1. Check the person has a Halyard account and the training certificate.
2. [[tobias-wren]] submits a membership change in the research IT portal under the group allocation, naming the project.
3. Usually done within three working days. Confirm with `sacctmgr show assoc user=<name>` that the `gpu` partition appears.

## Requesting New Or Renewed GPU Hours

1. **Estimate from measurements.** Use real timings per sample from previous runs, multiplied by the samples planned to the end of the period, plus 20% for reruns. Requests with numbers are approved faster ([[ilse-van-dorn]]).
2. **Separate essential from optional.** In 2026 the optional benchmark hours were cut; listing them separately avoided losing the essential ones.
3. **Name a technical and a scientific contact.**
4. **Submit through the research IT portal**, attaching the usage report of the current allocation if renewing.
5. **Plan for the wait.** Allow eight weeks. Keep a CPU or alternative plan for that period ([[should-the-spatial-pipeline-stay-on-gpu]]).

## Verification

Record the grant (hours, end date, members) in [[halyard-cluster]] and the decision as an Event, as done in [[halyard-gpu-partition-granted-2026-09-22]].
