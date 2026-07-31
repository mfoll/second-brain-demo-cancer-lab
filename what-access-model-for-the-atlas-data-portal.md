---
type: Question
status: Open
belongs_to: "[[atlas-data-portal]]"
related_to:
  - "[[data-access-policy-revision]]"
  - "[[atlas-tissue-access-agreement]]"
_organized: true
---

# What Access Model For The Atlas Data Portal?

Which parts of the atlas can be open, which need controlled access, and who grants access?

## Constraints Known

- The Westmere tissue agreement allows publication of de-identified derived data; images are not mentioned explicitly ([[atlas-tissue-access-agreement]]).
- The institute's revised data access policy, which would define a controlled-access route, is still under revision ([[data-access-policy-revision]]).
- [[yara-castellanos]] considers bin-level counts with section coordinates low-risk; whole-slide images with unique tissue features are the grey zone.

## Candidate Model

Open: processed matrices, annotations, cell-type estimates, treatment group and regression grade. Controlled: raw images and FASTQ through an institute data access committee. Not shared: dates, regimens at patient level, any free-text pathology.

Deferred until the policy is adopted; no action before 2027-02.
