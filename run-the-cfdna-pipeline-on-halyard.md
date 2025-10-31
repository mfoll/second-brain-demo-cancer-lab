---
type: Procedure
status: Active
belongs_to: "[[nextflow-pipeline-migration]]"
related_to:
  - "[[cfdna-pipeline-repository]]"
  - "[[halyard-cluster]]"
  - "[[pancreatic-cfdna-mrd-study]]"
_organized: true
---

# Run The cfDNA Pipeline On Halyard

How to run `varga-cfdna` on the Halyard cluster for a batch of cfDNA samples. Written by [[tobias-wren]]; tested by [[sofia-reyes-calderon]] as second maintainer.

## Inputs

- Halyard account with access to `/projects/varga`.
- FASTQ files in `/projects/varga/raw/<study>/<batch>/`, already registered by [[elias-moreau]] or the sequencing core.
- A sample sheet with columns sample, patient, timepoint, batch, fastq_1, fastq_2.

## Steps

1. Log in to a Halyard login node. Load Nextflow with `module load nextflow` (the version pinned in the pipeline config is used regardless).
2. Create a run directory in project space, `/projects/varga/derived/<study>/<run-date>/`, and copy the sample sheet there.
3. Test first: `nextflow run varga/varga-cfdna -r v1.2.0 -profile test,halyard`. It should finish in about 15 minutes.
4. Launch the real run from a small Slurm job, not the login node: submit `sbatch run_cfdna.slurm` with `-r <release> -profile halyard --input samplesheet.csv --outdir results`. Always give a release tag with `-r`, never a branch.
5. The work directory goes in scratch automatically. Resume with `-resume` within 30 days; after the purge, rerun.
6. When finished, check `results/multiqc/` and `results/pipeline_info/`.

## Outputs

`results/` with alignments (CRAM), fragment and end-motif tables, methylation calls and variant calls. Keep `pipeline_info/` with the results: it holds the resolved image digests ([[container-provenance]]).

## Verification

- MultiQC shows no sample with under 10 million deduplicated reads; flag any to [[dmitri-halvorsen]].
- Record the pipeline version and run directory in the analysis note that uses the results.

## Troubleshooting

Open a GitLab issue with the `.nextflow.log` attached; bring it to Tobias's monthly pipeline clinic if urgent.
