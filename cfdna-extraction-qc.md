---
type: Procedure
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[elias-moreau]]"
  - "[[cfdna-extraction-sop-v3]]"
  - "[[batch-confounding-in-cfdna-studies]]"
_organized: true
---

# cfDNA Extraction QC

How to check every cfDNA extraction batch before libraries are made. Owner: [[elias-moreau|Elias Moreau]]. Applies to St Aldric and any future plasma cohort. The wet-lab protocol itself is [[cfdna-extraction-sop-v3]]; this Procedure covers acceptance and logging.

## Inputs

- Extraction batch of up to 24 samples, including one healthy-donor pooled plasma control and, for any new kit lot, the bridging samples.
- Sample sheet with sample ID, time point, plasma volume, tube type, kit name and **lot number**, operator, date.

## Steps

1. **Randomise** before extraction: samples in each batch are assigned by script across time point and recurrence status, never in shipment order. Save the seed in the sample sheet.
2. **Quantify** with a fluorometric assay. Accept yield of at least 0.5 ng per ml plasma; flag below.
3. **Fragment profile** on capillary electrophoresis. Accept if the mononucleosomal peak is at 160–175 bp and the high-molecular-weight fraction (above 1,000 bp) is below 20% of total. Above 20% suggests leukocyte lysis; flag and do not use for fragmentomics.
4. **Control**: pooled plasma control yield within 25% of its running mean, peak within 3 bp. If not, the batch is held.
5. **New kit lot**: re-extract 16 previously extracted samples (bridging set). Compare modal length and sub-150 bp fraction; a shift above 2 bp or 2 percentage points is reported to the classifier owner before any data are used ([[extraction-kit-lot-change-2025-06-16]]).
6. **Log** every result in the current QC log ([[cfdna-extraction-qc-log-2026]]) and in the sample sheet.

## Outputs

QC-passed extracts with status, lot and batch ID recorded; flagged samples listed for the study meeting.

## Verification

Monthly, Dmitri checks the control's running chart and that every sample in the sheet has a lot number. Batch ID is a required column in [[fragmentomics-feature-matrix-v5]].
