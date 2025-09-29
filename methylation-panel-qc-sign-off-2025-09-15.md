---
type: Event
date: 2025-09-15
belongs_to: "[[methylation-panel-design]]"
related_to:
  - "[[methylation-panel-qc-report-2025-09]]"
  - "[[dmitri-halvorsen]]"
  - "[[rafael-ibarrondo]]"
_organized: true
---

# Methylation Panel QC Sign-Off 2025-09-15

Formal sign-off of the 1,840-region methylation panel, closing [[methylation-panel-design|Methylation Panel Design]]. Signed by [[dmitri-halvorsen|Dmitri Halvorsen]] (scientific), [[elias-moreau|Elias Moreau]] (wet lab) and [[rafael-ibarrondo|Rafael Ibarrondo]] (sequencing core). Ines attended.

## What Was Checked

Against the acceptance criteria written in the design document ([[methylation-panel-design-document-v4]]):

- Coverage uniformity: 98.6% of regions above 500x median deduplicated depth (criterion 95%). Passed.
- Conversion efficiency above 99.2% on unmethylated lambda controls (criterion 99%). Passed.
- Limit of detection: about 0.1% tumour fraction at 30 ng input in the spike-in titration ([[methylation-panel-spike-in-titration-2025-08]]); criterion was 0.2%. Passed.
- Reproducibility: inter-run correlation of region-level methylation 0.97 on six replicate pairs. Passed.
- 22 regions with consistently poor capture: flagged and excluded from scoring, not redesigned. The panel still counts as 1,840 regions; the scoring model uses 1,818.

## Decisions

- Panel released for the full St Aldric run, starting with sequencing run SA-R11 ([[sequencing-run-sheet-sa-r11]]).
- The exosome RNA pilot is formally closed as superseded ([[exosome-rna-pilot]]).
- The 22 excluded regions are listed in the QC report and must be excluded in any external validation too.

Full numbers: [[methylation-panel-qc-report-2025-09]].
