---
type: Note
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[tobias-wren]]"
  - "[[halyard-cluster]]"
_organized: true
---

# Halyard Migration Tracker

Per-workflow status of the move to Halyard. Updated by [[tobias-wren]]; last update 2026-10-22.

| Workflow | Owner | Image built in CI | Runs on Halyard | Status |
| --- | --- | --- | --- | --- |
| `varga-cfdna` (alignment, fragments, end motifs) | Tobias | Yes | Since 2026-07-06 | Done |
| `varga-spatial` CPU steps | Tobias, [[amara-okonkwo]] | Yes | Since 2026-08-03 | Done |
| `varga-spatial` GPU segmentation and deconvolution | Amara, [[kenji-mori]] | Yes | Since 2026-09-24 | Done, tests in progress |
| Methylation panel calling (legacy script) | [[dmitri-halvorsen]] | No | Wrapped, manual | November |
| CH variant workflow | [[hannah-lindqvist]] | No | Wrapped, manual | November |
| CH risk models (R) | [[lucas-brandt]] | Yes (R image) | Since 2026-06-22 | Done |
| Northvale lead-time models (R) | [[maja-kovac]] | Yes (R image) | Since 2026-06-22 | Done |

## Notes

- "Wrapped, manual" means the legacy script runs inside a generic image by hand, without the pipeline's provenance record. Results from these runs must cite the script commit.
- Kestrel is gone since 2026-09-30, so nothing can fall back to it ([[kestrel-retirement-2026-09-30]]).
