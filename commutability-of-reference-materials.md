---
type: Concept
maturity: Growing
belongs_to: "[[halo-cross-site-benchmark]]"
related_to:
  - "[[cfdna-fragmentomics]]"
  - "[[shibeeb-2026-harmonising-ctdna-measurement]]"
  - "[[halo-truth-set]]"
_organized: true
---

# Commutability Of Reference Materials

A reference material is commutable for a given set of measurement procedures when it behaves like real patient samples across those procedures: the relationship between results from two assays is the same for the material as for patient samples. A non-commutable material can make an assay look biased, or hide a real bias, because the assay is responding to something about the material rather than the analyte.

## Definition

> [!info]
> Commutability is a property of a material relative to a set of assays and a measurand, not a property of the material alone; the same tube can be commutable for mutation detection by ddPCR and not commutable for fragment-length features.

## Why It Matters For cfDNA

Most cfDNA reference materials are designed for mutation detection: a known allele at a known fraction in a DNA background. Mutation assays mostly ignore how that DNA was fragmented, so such materials can be commutable for them. Fragmentomics assays measure exactly the thing the manufacturing process changes. Sheared genomic DNA has no nucleosomal 167 bp peak and the wrong end motifs; even nucleosomal material from a cell line carries one cell type's nuclease footprint rather than the mixture found in plasma.

In Halo this showed up in the pilot panel: our shallow-WGS assay scored sheared DNA as if it came from a patient with recurrence, regardless of mutant fraction, and Thornvale's size selection discarded most of it ([[halo-pilot-panel-results-2026-04]]). The consortium now reports this as a finding and scores fragmentomics assays only on plasma ([[halo-annual-meeting-2026-06-10]]).

## How To Test It

Run patient samples and the candidate material on the same set of assays and compare the between-assay relationship, or each assay's bias against a reference, for both sample types. A difference in bias that exceeds a pre-set criterion indicates non-commutability; a consistent bias across both sample types points to the assay instead. [[vierbaum-2026-eqa-material-commutability]] shows the design in external quality assessment; [[he-2026-methylated-cfdna-reference-materials]] and [[hong-2026-nucleosomal-egfr-reference-materials]] describe cfDNA materials that are promising for methylation and mutation assays respectively.

## Where We Use It

- Truth set design: the sheared DNA samples were added to measure commutability rather than assume it ([[halo-truth-set-design-document]]).
- The open question for fragmentomics: [[are-contrived-reference-materials-commutable-for-fragmentomics]].
- The stance that patient plasma remains necessary: [[reference-materials-cannot-replace-patient-plasma]].
- Possibly in the [[low-vaf-caller-benchmark]], where caller performance on contrived material may overstate performance on plasma.

## Related Terms

Traceability (linking a result to a reference with stated uncertainty) and fitness for purpose (a material good enough for one intended use) are the other two pillars of the harmonisation framework in [[shibeeb-2026-harmonising-ctdna-measurement]].
