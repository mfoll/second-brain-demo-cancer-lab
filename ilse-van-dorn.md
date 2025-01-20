---
type: Person
belongs_to: "[[serve-corvane-institute]]"
related_to:
  - "[[halyard-cluster]]"
  - "[[halyard-cluster-migration]]"
  - "[[kestrel-retirement-2026-09-30]]"
_organized: true
---

# Ilse van Dorn

Head of research IT at Corvane and responsible for the [[halyard-cluster]]. She set the Halyard rules that shaped our migration: Slurm only, Apptainer only, no Docker, GPU partition by application.

## How We Work With Her

- Our main contact through [[tobias-wren]]; Ines meets her when a decision needs a group leader, such as the GPU allocation or the Kestrel deadline.
- Attended the [[apptainer-decision-2026-05-06]] meeting and confirmed that CI-built images pushed to the institute registry meet Halyard's security rules.
- Approved our GPU request on 2026-09-22 ([[halyard-gpu-partition-granted-2026-09-22]], [[halyard-gpu-allocation-request]]) with 6,000 GPU-hours to 2027-03-31.
- Signed off the Kestrel retirement plan and our data inventory ([[kestrel-retirement-notice]], [[kestrel-retirement-2026-09-30]]).

She expects requests through the research IT portal, with a named technical contact and a usage estimate. Requests with numbers get answers faster than requests with adjectives.

## History With The Group

- 2025: during the Kestrel years, Ilse's team handled our requests for long-queue priority; in January 2025 we chose to restructure jobs instead of asking for priority ([[lab-meeting-2025-01-16]]).
- 2026-03-16: she sent the [[kestrel-retirement-notice]], which set the deadline for the [[halyard-cluster-migration]].
- 2026-05-06: she restated that Docker would not be allowed on Halyard and agreed that images built in CI could be pulled on compute nodes.
- 2026-09-22: she approved 6,000 of the 8,000 GPU-hours requested and explained the cut: optional benchmark reruns are funded only after usage is shown.
- 2026-09-30: Kestrel powered off; she gave groups 30 days of read-only access as a safety net ([[kestrel-retirement-2026-09-30]]).

Her team writes the [[halyard-user-guide]]. When our group addendum disagrees with it, hers wins and Tobias updates ours.

## Current Threads

- GPU allocation review in January 2027 and possible renewal from April.
- Halyard storage charging model from April 2027; she asked group leaders for forecasts by December.
- Research IT seat on the institute procurement committee for the next GPU nodes.
