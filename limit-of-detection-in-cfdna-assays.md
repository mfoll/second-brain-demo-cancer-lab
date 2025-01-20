---
type: Concept
belongs_to: "[[pancreatic-cfdna-mrd-study]]"
related_to:
  - "[[methylation-panel-spike-in-titration-2025-08]]"
  - "[[low-vaf-caller-benchmark]]"
_organized: true
---

# Limit of Detection in cfDNA Assays

The limit of detection (LoD) is the lowest tumour fraction, or variant allele fraction, at which an assay detects signal with a stated probability, usually 95%. For cfDNA it depends as much on input DNA as on the assay.

## Why Input Matters

At 10 ng of cfDNA there are about 3,000 haploid genome copies. At 0.01% tumour fraction that is on average 0.3 tumour copies per locus: no assay can see what is not in the tube. Tracking many loci (tumour-informed) or many regions (methylation) raises the chance that some tumour molecules are sampled, which is why multi-locus designs reach lower LoD than single-locus ones.

## Our Numbers

- Methylation panel: about 0.1% tumour fraction at 30 ng input, 95% detection ([[methylation-panel-spike-in-titration-2025-08]]). St Aldric post-operative extracts have a median of 14 ng, so the effective LoD in practice is higher.
- Variant calling below 0.5% VAF: being benchmarked ([[low-vaf-caller-benchmark]]); in-silico data suggest about 80% sensitivity at 0.25% VAF with duplex consensus.

## Caveat

A stated LoD from spike-ins of sheared cell-line DNA can flatter an assay, because spike-in fragments do not have the length profile of real ctDNA. Report LoD with input amount and spike-in material, and treat it as an upper bound on performance.
