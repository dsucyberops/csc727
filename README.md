# Project Phantom

**Ethical, Security, and Governance Challenges of Deepfake Technology in the Era of Generative Artificial Intelligence**

> Walther Del Orbe · Nawaz Syed · Kwaku Dei Amoani · Gwendolyn Vongkasemsiri  
> The Beacom College of Computer and Cyber Sciences  
> Dakota State University · CSC 727 · Spring 2026

---

## About This Repository

This repository contains all supplementary research materials for *Project Phantom*, a structured literature review and comparative analysis of deepfake technologies across three interconnected dimensions: **technical detection**, **cybersecurity risk**, and **governance and ethics**. Every file is directly tied to a section of the paper and is organized to support full reproducibility.

---

## Quick Links

| Resource | Location |
|---|---|
| Final paper (.docx) | [`/paper/ProjectPhantom_Final.docx`](paper/ProjectPhantom_Final.docx) |
| Annotated bibliography (all 15 sources) | [`/literature/annotated_bibliography.md`](literature/annotated_bibliography.md) |
| Search protocol + PRISMA screening | [`/literature/search_protocol.md`](literature/search_protocol.md) |
| Detection comparison data (CSV) | [`/detection-analysis/detection_comparison.csv`](detection-analysis/detection_comparison.csv) |
| Jurisdiction comparison data (CSV) | [`/governance/jurisdiction_comparison.csv`](governance/jurisdiction_comparison.csv) |
| Detection bias synthesis | [`/ethics/bias_findings_synthesis.md`](ethics/bias_findings_synthesis.md) |

---

## Repository Structure

```
csc727/
├── README.md
│
├── literature/
│   ├── annotated_bibliography.md     # All 15 sources: full citations, annotations,
│   │                                 # key findings, and section cross-references
│   └── search_protocol.md            # Databases, search terms, inclusion/exclusion
│                                     # criteria, PRISMA flowchart (340→60→30→15)
│
├── detection-analysis/
│   ├── detection_comparison.csv      # Raw data for Tables 2 & 4 (7 methods × 7 fields)
│   ├── detection_comparison_notes.md # 5-criterion framework rationale + per-method
│   │                                 # rating justification with source citations
│   └── table4_accuracy_estimates.md  # Source basis for all ~% values in Table 4
│
├── governance/
│   ├── jurisdiction_comparison.csv   # Raw data for Table 3 (7 jurisdictions × 11 fields)
│   └── legislative_notes.md          # Per-jurisdiction analysis, 4-criterion assessment,
│                                     # and cross-jurisdictional gap table
│
├── ethics/
│   ├── bias_findings_synthesis.md    # Detection bias by demographic group,
│   │                                 # documented disparities, 6 mitigations
│   └── ethical_framework_notes.md    # Consent pipeline, liar's dividend mechanism,
│                                     # accountability diffusion, research ethics norms
│
└── paper/
    └── ProjectPhantom_Final.docx     # Final report (v6)
```

---

## Research Questions

**RQ1.** What ethical challenges arise from the development and use of deepfake technologies, particularly regarding consent, identity protection, and human dignity?

**RQ2.** What cybersecurity and fraud risks are introduced by deepfake technologies, and how effective are current detection approaches?

Both questions are answered directly in **Section 10 (Discussion and Findings)** of the paper — §10.1 answers RQ1 and §10.2 answers RQ2.

---

## Folder → Paper Section Map

| Folder | Supports Paper Sections |
|---|---|
| `/literature` | §2 Related Work · §2.5 Research Gap · §4.1 Literature Search (Table 5) |
| `/detection-analysis` | §6 Detection Techniques · Tables 2 & 4 |
| `/governance` | §7 Governance and Mitigation · Table 3 |
| `/ethics` | §8 Ethics Statement · §10.1 RQ1 Answer |
| `/paper` | Full report |

---

## Paper Version History

| Version | Key changes |
|---|---|
| v1 (Progress2) | Initial draft — descriptive Related Work; no research gap section; no screening counts |
| v2 | Added detection techniques section; Table 3 governance comparison; Figure 1 |
| v3 | Repository link added; Related Work repositioned relative to prior work |
| v4 | Research Questions section added; Conclusion restructured to answer RQs |
| v5 | Related Work rewritten comparatively; §2.5 Research Gap added; §4.1 with PRISMA counts and Table 5; §4.2 five-criterion rationale; anonymous citations fixed; arXiv IDs added |
| **v6 (current)** | Repository migrated to GitHub; all SharePoint references replaced; folder structure documented in §4.3; abstract updated |

---

## How to Reproduce the Analysis

1. Review the search protocol in `/literature/search_protocol.md` for exact search terms and screening criteria
2. The full source corpus is in `/literature/annotated_bibliography.md` — 15 entries with dimension classifications
3. Detection ratings in Tables 2 and 4 are derived from `/detection-analysis/detection_comparison.csv`; rating justifications are in `detection_comparison_notes.md`
4. Governance ratings in Table 3 are derived from `/governance/jurisdiction_comparison.csv`; legislative analysis is in `legislative_notes.md`
5. Ethics analysis in §8 is supported by both files in `/ethics/`

---

## Citation

```
Del Orbe, W., Syed, N., Amoani, K. D., & Vongkasemsiri, G. (2026). Project Phantom:
Ethical, Security, and Governance Challenges of Deepfake Technology in the Era of
Generative Artificial Intelligence. The Beacom College of Computer and Cyber Sciences,
Dakota State University. https://github.com/DSUcyberops/csc727
```

---

## Course Information

| Field | Value |
|---|---|
| Course | CSC 727 — Advanced Topics in Cybersecurity |
| Institution | Dakota State University |
| College | Beacom College of Computer and Cyber Sciences |
| Term | Spring 2026 |
| Repository | https://github.com/DSUcyberops/csc727 |
