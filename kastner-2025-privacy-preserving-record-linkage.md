---
type: Source
source_type: Scientific paper
url: https://doi.org/10.1007/s00432-025-06384-7
doi: 10.1007/s00432-025-06384-7
pmid: "41342956"
licence: cc by
date_accessed: 2026-06-19
belongs_to: "[[registry-linkage-agreement]]"
related_to:
  - "[[northern-cancer-registry]]"
  - "[[registry-linkage-update]]"
  - "[[pseudonymisation-vs-anonymisation]]"
_organized: true
---

# Concept and feasibility of privacy-preserving record linkage of cancer registry data and claims data in Germany: results from the DigiNet study on stage IV non-small cell lung cancer

Kästner A et al. Journal of Cancer Research and Clinical Oncology, 2025.

## Summary

Describes a privacy-preserving record linkage between cancer registry records and health insurance claims for a population-based control group of stage IV lung cancer patients, done without individual consent. Identifiers were irreversibly encrypted inside the data-holding institutions, a trusted third party matched on the encrypted values and then discarded the linkage keys. Most eligible cases were linked successfully.

## Why It Matters

[[yara-castellanos]] flagged it when the [[registry-linkage-update]] started in June 2026. Our agreement uses a simpler model: the [[northern-cancer-registry]] sees clear identifiers and links in-house. The paper is a worked example of the alternative, where no single party sees both identity and data. Useful if the registry ever asks to stop receiving clear identifiers, and as a reference when we explain to the board why the linkage key is deleted 90 days after delivery ([[registry-linkage-agreement-summary]]).

## Caveats

Different legal setting and different data (claims, not cohort biobank data). Eligibility depended on insurance coverage with participating funds, so the linked fraction of the full registry group was small; the high success rate applies to the eligible subset.

## Source Links

- [DOI 10.1007/s00432-025-06384-7](https://doi.org/10.1007/s00432-025-06384-7)
