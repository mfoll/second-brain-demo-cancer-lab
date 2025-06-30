---
type: Question
status: Open
belongs_to: "[[clonal-hematopoiesis-filter]]"
related_to:
  - "[[panel-of-normals]]"
  - "[[ch-panel-of-normals-v1]]"
  - "[[lucas-brandt]]"
_organized: true
---

# How Large Must the CH Panel of Normals Be?

How many healthy-donor buffy coat samples, and of what age profile, does the CH [[panel-of-normals]] need before it catches most clonal hematopoiesis variants seen in post-operative pancreatic cancer plasma?

## Why It Matters

Version 1 of the panel ([[ch-panel-of-normals-v1]]) uses 1,200 Northvale participants aged 60 and over, a preliminary batch of [[ch-cancer-risk-analysis|CH Cancer Risk Analysis]] calls available in 2026-02, before the full set was frozen. It caught 84% of buffy-coat-confirmed CH variants in the St Aldric pilot. If the misses are mainly a size effect, the full frozen callset may close the gap and make matched buffy coat sequencing unnecessary for most patients ([[do-we-still-need-matched-buffy-coat-sequencing]]).

## Current Thinking

- A third data point: [[noor-haddad|Noor Haddad]]'s 2026 internship prototype used only 96 healthy-donor buffy coats and, on 40 St Aldric patients, still removed most of what matched buffy coat removes while missing private DNMT3A and TET2 clones ([[intern-project-panel-of-normals-ch]]). Numbers being checked by Hannah.

- Hotspot CH variants (DNMT3A R882, JAK2 V617F, some PPM1D truncations) saturate quickly; a few hundred donors find them.
- The misses are private variants, unique to one person. No panel size will catch these by variant identity, only at gene level, which costs specificity because TP53 and KRAS are also tumour genes.
- So the answer is probably "6,000 is enough for hotspots, and size cannot fix private variants".

## What Would Answer It

Down-sample the frozen Northvale calls ([[ch-subcohort-variant-calls]], 5,962 samples passing QC) to 500, 1,000, 2,000, 4,000 and all, and plot recovery of pilot CH variants. Hannah is running the curve; results expected at the November 2026 MRD study meeting.
