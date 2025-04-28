---
type: Note
belongs_to: "[[fragmentomics-classifier]]"
related_to:
  - "[[cfdna-fragmentomics]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# cfDNA Fragmentomics Reading Notes

Running digest of what fragmentomics papers changed in our practice, kept by Sofia and Ines. Newest first. Each line links the Source note.

- 2026-02: [[li-2025-finaletoolkit]]. Adopted FinaleToolkit for feature extraction in January after timing it on Halyard; it also gives window protection scores we have not used yet.
- 2026-01: [[liu-2024-reference-biases-fragmentomics]]. Fragment features depend on the reference genome in a sample-dependent way. Consequence: reference and aligner are pinned in the model card and in the Halo container.
- 2025-11: [[ju-2024-cfdna-end-characteristics]]. Ends inside nucleosomes carry altered motifs and shorter fragments. Supports keeping end motifs as a separate family; this later justified the stacked design.
- 2025-10: [[spiegl-2023-gcparagon]]. Fragment-level GC correction. We implemented the same idea in our pipeline before computing window ratios.
- 2025-07: [[sirajee-2024-cell-free-nucleic-acid-fragmentomics]]. Good overview for new students; assigned to Noor in 2026.
- 2025-05: [[jin-2021-hcc-fragment-size-end-motifs]]. Size selection below 150 bp raises tumour fraction; 4-mer end motifs coupled to size. Basis of our first feature list.

Not yet read carefully: work combining methylation and fragmentation from the same library; relevant only if we stop doing separate shallow WGS.
