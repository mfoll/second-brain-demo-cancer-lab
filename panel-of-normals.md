---
type: Concept
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[clonal-hematopoiesis]]"
  - "[[ch-panel-of-normals-v1]]"
_organized: true
---

# Panel of Normals

A panel of normals is a collection of samples from people without the disease of interest, processed with the same pipeline, used to flag variants that are artefacts or common non-tumour variants. Any variant seen recurrently in the panel is treated as suspect in a patient sample.

## Two Uses

- **Artefact filtering**: recurrent sequencing or alignment errors at specific positions, the classic use in somatic calling.
- **CH filtering**: here the "normals" are blood samples from healthy older adults, and the panel flags variants and genes that are common clonal hematopoiesis. This is how the [[clonal-hematopoiesis-filter|CH filter]] works for patients without matched buffy coat ([[ch-panel-of-normals-v1]], built from [[ch-cancer-risk-analysis]] calls).

## Limits

A panel of normals catches recurrent variants, not private ones. CH is often private: most clones are unique to the person. In the St Aldric pilot, the panel caught 84% of buffy-coat-confirmed CH variants; the misses were private low-VAF clones. Gene-level flagging catches more but also removes true tumour variants in shared genes such as TP53 and KRAS. Hence [[do-we-still-need-matched-buffy-coat-sequencing]] and [[how-large-must-the-ch-panel-of-normals-be]].
