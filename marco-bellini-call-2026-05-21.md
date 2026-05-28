---
type: Event
date: 2026-05-21
belongs_to: "[[deconvolution-benchmark]]"
related_to:
  - "[[marco-bellini]]"
  - "[[kenji-mori]]"
  - "[[low-count-spot-collapse]]"
_organized: true
---

# Marco Bellini Call 2026-05-21

Video call between [[marco-bellini]], [[kenji-mori]] and Ines about the low-count behaviour of Marco's method (M5 in the [[deconvolution-benchmark]]).

## Outcome

- Marco reproduced the collapse from Kenji's example before the call and confirmed the mechanism: with a nearly flat likelihood at low counts, the abundance prior dominates; confidence is computed on the posterior, so it does not drop ([[low-count-spot-collapse]]).
- He plans a warning when a spot's total count is below a threshold, and a minimum-count option, in his next release.
- He agreed to be named in the preprint, with a sentence on the planned fix, and asked to see the draft two weeks before posting.

## Our Actions

- Kenji sends the draft figure 2 and methods section when ready.
- If the release appears before posting, run both versions.
- Keep the M3 developers' silence separate; see [[how-to-report-failing-methods-in-the-benchmark]].
