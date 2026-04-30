---
type: Question
status: Open
belongs_to: "[[halyard-cluster-migration]]"
related_to:
  - "[[data-tiering]]"
  - "[[group-data-management-plan]]"
  - "[[halyard-storage-quota-statement]]"
_organized: true
---

# How Long Should We Keep Raw FASTQ On Halyard?

## Question

The DMP keeps raw sequencing for 10 years after the last publication, but says nothing about where. From April 2027 Halyard storage above 100 TB is charged. How long should raw FASTQ stay in project space before moving to the cold archive?

## Current Answer

None agreed. [[yara-castellanos]] proposes moving raw data to the cold archive 12 months after the last pipeline run that used it, keeping aligned CRAM files on Halyard. [[dmitri-halvorsen]] wants St Aldric raw data on Halyard until the [[mrd-manuscript]] is accepted, because the revision may need reprocessing.

## Evidence

- Raw data is 88 of 141 TB used ([[halyard-storage-quota-statement]]).
- Cold-archive retrieval took 2 to 5 working days per batch during the Kestrel verification ([[archive-kestrel-data]]).
- CRAM with reference is about 40% the size of FASTQ for our cfDNA data, and FASTQ can be regenerated from it for our purposes.

## Next Step

Decide before the storage forecast to research IT in December; record the rule in DMP v1.1.
