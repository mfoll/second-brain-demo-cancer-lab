---
type: Concept
belongs_to: "[[lead-time-analysis]]"
related_to:
  - "[[reverse-causation-in-prediagnostic-studies]]"
  - "[[lead-time]]"
  - "[[report-lead-time-windows-not-pooled-estimates]]"
_organized: true
---

# Time-to-Diagnosis Windows

Grouping cases in a prediagnostic study by the time between sample collection and diagnosis, and estimating the association separately in each group. Controls take the window of their matched case.

## Northvale windows

Fixed in the [[northvale-statistical-analysis-plan]] before results were seen:

| Window | Cases |
| --- | --- |
| 0 to 1 year | 27 |
| 1 to 2 years | 31 |
| 2 to 5 years | 84 |
| More than 5 years | 268 |

## Why windows

A gradient across windows is the most informative output of a single-sample prediagnostic study. A signal that is strong close to diagnosis and fades with distance points to detection of existing disease (short [[lead-time]] or [[reverse-causation-in-prediagnostic-studies|reverse causation]]); a flat association points to a risk marker. A pooled estimate hides the difference.

## Costs

- Few cases in the earliest windows, so wide intervals.
- Window boundaries are arbitrary; we chose them on clinical intuition (one year, two years, five years) and report a continuous interaction as a check.
- Diagnosis date errors move cases across boundaries; the 2025 registry corrections moved none ([[northvale-control-replacement-log]]).
