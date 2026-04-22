# Literature Search Protocol
## Project Phantom — /literature

This document records the search strategy used to identify and select sources for this review, in accordance with structured literature review methodology. It supports reproducibility: a researcher following this protocol should be able to replicate the search and arrive at a comparable source set.

---

## 1. Search Databases

| Database | URL | Coverage |
|---|---|---|
| Google Scholar | scholar.google.com | Broad academic coverage, preprints |
| IEEE Xplore | ieeexplore.ieee.org | Computer science, engineering, cybersecurity |
| ACM Digital Library | dl.acm.org | Computing and information science |
| arXiv | arxiv.org | Preprints in CS, AI, and ML |
| SSRN | ssrn.com | Legal and policy working papers |

---

## 2. Search Terms

Searches were conducted using the following terms, both individually and in combination using Boolean AND/OR operators.

### Primary terms
- `deepfake detection`
- `synthetic media ethics`
- `generative AI governance`
- `GAN deepfake`
- `diffusion model detection`
- `deepfake policy`
- `deepfake fraud`
- `deepfake cybersecurity`

### Secondary terms (used in combination with primary terms)
- `deepfake bias`
- `deepfake consent`
- `deepfake legislation`
- `voice cloning fraud`
- `identity impersonation AI`
- `liar's dividend`
- `multimodal deepfake detection`
- `frequency domain deepfake`

### Example combined queries
- `"deepfake detection" AND "diffusion model" AND 2024..2026`
- `"deepfake" AND ("governance" OR "regulation") AND "artificial intelligence"`
- `"synthetic media" AND ("fraud" OR "cybersecurity")`
- `"deepfake" AND ("bias" OR "fairness") AND "detection"`

---

## 3. Date Range

**Primary range:** January 2021 – April 2026  
**Rationale:** The generative AI landscape has evolved rapidly; sources older than five years are unlikely to reflect the current capability or governance environment. One source (Guarnera et al., 2023) predates 2024 but was included because it provides the foundational quantitative evidence for the GAN-to-diffusion generalization gap.

---

## 4. Inclusion Criteria

A source was included if it met **all** of the following:

1. Published in a peer-reviewed venue, conference proceeding, or reputable preprint archive (arXiv, SSRN)
2. Addresses at least one of the three analytical dimensions: (a) technical detection, (b) cybersecurity risk, or (c) governance and ethics
3. Within the 2021–2026 date range (with one justified exception)
4. Available in English

---

## 5. Exclusion Criteria

A source was excluded if it met **any** of the following:

1. Focuses solely on generative model development without addressing detection, risk, or governance
2. Does not appear in a verifiable academic venue (no peer review or reputable preprint)
3. Predates 2021 without providing foundational evidence not available in more recent work
4. Is a secondary news article, blog post, or non-academic commentary

---

## 6. Selection Process

1. Initial search across all databases using primary terms → ~340 candidate titles
2. Title and abstract screening against inclusion/exclusion criteria → ~60 retained
3. Full-text review for relevance and quality → 30 candidates
4. Final selection prioritizing: recency, methodological rigor, and coverage of at least one analytical dimension → **15 sources selected**
5. Cross-reference check: cited papers in selected sources were reviewed for any missed foundational works → 0 additional sources added

---

## 7. Source Classification by Dimension

| # | Author(s) | Year | Technical (T) | Cybersecurity (C) | Governance/Ethics (G) |
|---|---|---|:---:|:---:|:---:|
| 1 | Clark & Lewandowsky | 2026 | | ✓ | ✓ |
| 2 | Doloriel et al. | 2025 | ✓ | | |
| 3 | Farid | 2025 | | ✓ | ✓ |
| 4 | Gong & Li | 2024 | ✓ | | |
| 5 | Guarnera et al. | 2023 | ✓ | | |
| 6 | Khan et al. | 2025 | ✓ | | |
| 7 | Bateman et al. | 2025 | | | ✓ |
| 8 | Lin et al. | 2025 | ✓ | ✓ | |
| 9 | Liu et al. | 2025 | ✓ | | |
| 10 | Martinek | 2025 | ✓ | | |
| 11 | Patel et al. | 2026 | ✓ | | ✓ |
| 12 | Singh et al. | 2025 | ✓ | | |
| 13 | Soundarya & Gururaj | 2026 | ✓ | | |
| 14 | Soundarya et al. | 2025 | ✓ | | |
| 15 | European Parliament | 2024 | | | ✓ |

**Totals:** Technical: 10 sources | Cybersecurity: 3 sources | Governance/Ethics: 6 sources  
*(Several sources span multiple dimensions)*
