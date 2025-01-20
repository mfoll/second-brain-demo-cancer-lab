---
type: Person
belongs_to: "[[halo-consortium-work]]"
related_to:
  - "[[federated-cfdna-learning]]"
  - "[[fragmentomics-classifier]]"
  - "[[sofia-reyes-calderon]]"
_organized: true
---

# Arjun Mehta

Halo machine-learning lead, a computational scientist at Westmere Cancer Centre. He leads the modelling task in WP4 under Ines and is the author of the federated idea.

## Role

- Leads WP4 task 4.3 (cross-assay modelling) in the [[halo-wp4-analysis-plan]].
- Proposed federated training and evaluation at the [[halo-steering-committee-2026-09-17]] and co-wrote the [[federated-cfdna-learning-concept-note]] with Ines.
- Maintains Westmere's analysis of the hybrid-capture assay.

## How We Work Together

Arjun is quick, opinionated and generous with code. He has run federated pilots on imaging data at Westmere and knows the practical traps: site dropouts, version drift between containers, and how hard it is to debug a model you cannot see the data for. He favours [[flower-federated-learning-framework]]; Ines leans towards something that fits our Nextflow and Apptainer setup, so the choice is open.

He reviewed the [[fragmentomics-classifier]] code in July and agreed with the group's move away from a single gradient-boosting model ([[lab-meeting-2026-03-12]]), though he argued for keeping boosting on the end-motif block, which is close to where the group ended up. [[sofia-reyes-calderon]] and [[leila-farouk]] have a fortnightly call with him.

## Current Threads

- Concept note revision and costing for [[federated-cfdna-learning]].
- Common feature layer across assays: which fragment-length features can every sequencing assay produce?
- Leakage risk from shared gradients; he circulated [[ay-2026-privacy-enhancing-technologies-biomedical-ai]] to the WP4 list.

## History With The Group

Arjun joined Halo in 2025 as Westmere's computational lead and became WP4 task lead in the first work plan revision. He has visited Corvane twice, the second time for the annual meeting, where he and Sofia sketched the cross-assay feature layer on a whiteboard that [[priya-raman]] photographed for the WP4 folder. He is also on the external advisory list for the institute course.

## Links

- [[halo-consortium-work]]
- [[can-federated-training-match-a-pooled-classifier]]
