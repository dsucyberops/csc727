# Literature Search Protocol
## Project Phantom · /literature · https://github.com/DSUcyberops/csc727

This document records the complete search strategy and PRISMA-style screening process used to identify and select the 15 sources included in this review (referenced in §4.1 of the paper). It is designed to support full reproducibility: a researcher following this protocol should arrive at a comparable source set.

---

## 1. Search Databases

| Database | URL | Primary Coverage |
|---|---|---|
| Google Scholar | scholar.google.com | Broad academic coverage; preprints; grey literature |
| IEEE Xplore | ieeexplore.ieee.org | Computer science; electrical engineering; cybersecurity |
| ACM Digital Library | dl.acm.org | Computing; information science; HCI |
| arXiv | arxiv.org | CS preprints (cs.CV, cs.CR, cs.LG, cs.CL) |

---

## 2. Search Terms

### Primary terms
```
deepfake detection
synthetic media ethics
generative AI governance
GAN deepfake
diffusion model detection
deepfake policy
deepfake cybersecurity
deepfake fraud
```

### Secondary terms (combined with primary using AND/OR)
```
deepfake bias
deepfake fairness
deepfake consent
deepfake identity
deepfake legislation
deepfake regulation
voice cloning fraud
voice cloning authentication
multimodal deepfake detection
frequency domain deepfake
liar's dividend
epistemic harm AI
synthetic media disinformation
```

### Example Boolean queries
```
"deepfake detection" AND "diffusion model" AND (2024 OR 2025 OR 2026)
"deepfake" AND ("governance" OR "regulation") AND "artificial intelligence"
"synthetic media" AND ("fraud" OR "cybersecurity" OR "authentication")
"deepfake" AND ("bias" OR "fairness") AND "detection"
"voice cloning" AND ("fraud" OR "business email compromise")
"deepfake" AND ("consent" OR "non-consensual") AND ("policy" OR "ethics")
```

---

## 3. Date Range

**Primary window:** January 2021 – April 2026

**Rationale:** The generative AI landscape has evolved fundamentally since 2021, particularly with the rise of diffusion-based generation. Sources older than five years do not reflect current capabilities, threats, or governance environments and were excluded unless they provided foundational evidence unavailable in more recent work.

**Exception:** Guarnera et al. (2023) was retained despite predating 2024 because it is the earliest paper to quantitatively document the GAN-to-diffusion generalization gap. No more recent paper supersedes this finding; subsequent papers extend it.

---

## 4. PRISMA-Style Screening Flowchart

```
┌─────────────────────────────────────────────────────────────┐
│  IDENTIFICATION                                             │
│  Initial database search across Google Scholar,            │
│  IEEE Xplore, ACM Digital Library, arXiv                   │
│                         ↓                                   │
│              ~340 candidate titles identified               │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│  SCREENING (Title & Abstract)                               │
│  Applied inclusion/exclusion criteria                       │
│  Removed: sole generative model development (no detection,  │
│  risk, or governance dimension); no peer review; pre-2021   │
│  without foundational justification; non-English            │
│                         ↓                                   │
│              ~60 sources retained                           │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│  ELIGIBILITY (Full-Text Review)                             │
│  Assessed for: methodological quality, relevance to         │
│  at least one analytical dimension, recency, empirical      │
│  grounding, and cross-dimensional coverage                  │
│                         ↓                                   │
│              30 candidates                                  │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│  FINAL SELECTION                                            │
│  Prioritized: recency within 2021–2026 window; empirical    │
│  rigor; coverage of ≥1 analytical dimension; ability to     │
│  support cross-dimensional synthesis                        │
│                         ↓                                   │
│              15 primary sources selected                    │
└─────────────────────────────────────────────────────────────┘
                          ↓
┌─────────────────────────────────────────────────────────────┐
│  CROSS-REFERENCE CHECK                                      │
│  Reviewed cited works in selected sources                   │
│                         ↓                                   │
│              0 additional sources added                     │
│              FINAL CORPUS: 15 sources                       │
└─────────────────────────────────────────────────────────────┘
```

---

## 5. Inclusion Criteria

A source was **included** if it met ALL of the following:

1. Published in a peer-reviewed journal, conference proceeding, or reputable preprint archive (arXiv, SSRN)
2. Addresses at least one of three analytical dimensions: (a) technical detection, (b) cybersecurity/fraud risk, or (c) governance and ethics
3. Falls within the 2021–2026 date range, with one justified exception (Guarnera et al., 2023)
4. Available in English

---

## 6. Exclusion Criteria

A source was **excluded** if it met ANY of the following:

1. Focused solely on generative model development without addressing detection, risk, or governance
2. Not published in a verifiable academic venue
3. Predates 2021 without providing foundational evidence unavailable in more recent work
4. Secondary news article, blog post, or non-academic commentary
5. Not available in English

---

## 7. Source Summary Table (matches Table 5 in paper)

T = Technical Detection | C = Cybersecurity Risk | G = Governance & Ethics

| # | Author(s) | Year | Venue Type | T | C | G |
|---|---|---|---|:---:|:---:|:---:|
| 1 | Clark & Lewandowsky | 2026 | Peer-reviewed journal | | ✓ | ✓ |
| 2 | Doloriel et al. | 2025 | arXiv preprint | ✓ | | |
| 3 | Farid | 2025 | Peer-reviewed journal | | ✓ | ✓ |
| 4 | Gong & Li | 2024 | Peer-reviewed journal | ✓ | | |
| 5 | Guarnera et al. | 2023 | arXiv preprint | ✓ | | |
| 6 | Khan et al. | 2025 | arXiv preprint | ✓ | | |
| 7 | Bateman et al. | 2025 | Peer-reviewed journal | | | ✓ |
| 8 | Lin et al. | 2025 | arXiv preprint | ✓ | ✓ | |
| 9 | Liu et al. | 2025 | Peer-reviewed journal | ✓ | | |
| 10 | Martinek | 2025 | Conference proceeding (COLING) | ✓ | | |
| 11 | Patel et al. | 2026 | Peer-reviewed journal | ✓ | | ✓ |
| 12 | Singh et al. | 2025 | Peer-reviewed journal | ✓ | | |
| 13 | Soundarya & Gururaj | 2026 | Peer-reviewed journal | ✓ | | |
| 14 | Soundarya et al. | 2025 | Peer-reviewed journal | ✓ | | |
| 15 | European Parliament | 2024 | Legislative text | | | ✓ |

**Totals:** T: 10 sources | C: 3 sources | G: 6 sources  
**Venue breakdown:** Peer-reviewed journals: 9 | Conference proceedings: 1 | arXiv preprints: 4 | Legislative text: 1

---

## 8. Quality Assessment Notes

Sources were assessed on the following quality indicators during full-text review:

| Source type | Quality indicators assessed |
|---|---|
| Empirical studies (Clark & Lewandowsky; Lin et al.) | Experimental design, sample size, ecological validity |
| Survey/review papers (Khan et al.; Singh et al.; Gong & Li) | Coverage breadth, recency of included studies, comparative analysis present |
| Technical papers (Doloriel et al.; Guarnera et al.) | Benchmark diversity, out-of-distribution evaluation included |
| Legal/governance papers (Bateman et al.; Patel et al.) | Normative grounding, engagement with actual legislation |
| Perspective pieces (Farid) | Author expertise, argument quality, engagement with counter-arguments |
| Legislative text (EU Parliament) | Official source, current enforcement status verified |
