---
type: Question
status: Open
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[spatial-pipeline-repository]]"
  - "[[halyard-gpu-partition-granted-2026-09-22]]"
  - "[[deconvolution-benchmark]]"
_organized: true
---

# Should The Spatial Pipeline Stay On GPU?

## Question

The GPU allocation (6,000 hours to 2027-03-31) is not guaranteed beyond March. Should `varga-spatial` keep GPU-only segmentation and deconvolution steps, or offer CPU fallbacks that are slower but always available?

## Current Answer

Keep GPU as default and add a CPU fallback for segmentation only. Deconvolution on CPU was about 12 times slower in Kestrel tests, too slow for 40 samples.

## Evidence

- First month on Halyard: about 900 GPU-hours used for 9 samples including parameter tuning ([[halyard-gpu-partition-granted-2026-09-22]]).
- At that rate the 14 batch 3 pairs and reruns fit within the grant, but the [[deconvolution-benchmark]] reruns do not.
- A CPU fallback costs test time: each GPU module would need two test paths ([[snapshot-testing]]).

## Next Step

[[tobias-wren]] and [[amara-okonkwo]] report usage in January; decide on renewal and fallback scope then.
