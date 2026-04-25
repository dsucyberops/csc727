# Legislative Framework Notes
## Project Phantom · /governance · https://github.com/DSUcyberops/csc727

Detailed analysis underlying Table 3 in the paper. Supports §7 (Governance and Mitigation) and the cross-cutting analysis in §10.3. Organized around the paper's four-criterion governance assessment framework.

---

## The Four-Criterion Assessment Framework

Each jurisdiction is evaluated against four criteria derived from the paper's integrated three-dimension analytical framework (§4.2):

| Criterion | Definition | Why it matters |
|---|---|---|
| **Transparency** | Mandatory disclosure of AI-generated content to end users | Without transparency, the liar's dividend (§8.2) cannot be countered — users cannot apply appropriate skepticism to content they cannot identify as synthetic |
| **Watermarking** | Technical provenance embedding at generation time | Creates an upstream signal that survives distribution and enables attribution; C2PA provides the open standard but mandating it requires governance |
| **Platform accountability** | Positive obligations on platforms — not merely prohibitions on individuals | Individual prohibitions cannot address industrial-scale synthetic media production; platforms are the only actors with the reach to enforce at scale |
| **Cross-border enforcement** | Mechanisms addressing transnational production and distribution | Deepfake production and distribution is inherently transnational; jurisdiction-specific frameworks create predictable gaps |

---

## Jurisdiction Analysis

### United States (Federal)

**Status:** No federal deepfake-specific legislation enacted as of early 2026.

**Legislative history:**
- *DEFIANCE Act (2024):* Federal civil remedy for non-consensual intimate deepfakes. Passed Senate; stalled in House as of review date.
- *NO FAKES Act (2024):* Federal right of publicity for digital voice and likeness replicas. Bipartisan support; not enacted.
- *Protect Elections from Deceptive AI Act:* Prohibition on materially deceptive AI-generated content in federal election advertising. Not enacted.

**Applicable existing law:**
- Section 230 (CDA): Platform immunity from third-party content liability fundamentally limits platform accountability — the most significant structural barrier to effective U.S. deepfake governance
- FTC Act §5: Unfair or deceptive acts; provides case-by-case enforcement basis for fraudulent deepfakes only
- State laws fill some gaps but create inconsistent national coverage

**Four-criterion score: 0/4** — No transparency mandate, no watermarking mandate, no platform accountability (Section 230), no cross-border mechanism.

**Primary gap:** Absence of federal law means victim redress depends entirely on state of residence, and cross-state cases have no clear legal path.

---

### United States — California

**Statutes:** AB 730 (2019) | AB 602 (2023) | SB 926 (2024)

- AB 730: First U.S. deepfake law; requires disclosure labels on deepfake political ads within 60 days of election
- AB 602: Civil cause of action for non-consensual deepfake intimate imagery; injunctive relief and damages
- SB 926: Extends AB 602; increases platform removal obligations

**Four-criterion score: 1/4** — Partial transparency (political ads only); no watermarking; partial platform accountability (Section 230 still limits); no cross-border.

**Gap:** Does not address commercial fraud, authentication bypass, or AI system watermarking. Platform safe harbor under Section 230 still applies.

---

### United States — Texas

**Statute:** HB 4337 (2023) — Criminal prohibition on deepfakes depicting sexual conduct without consent.

**Four-criterion score: 0/4** — No transparency, no watermarking, no platform accountability, no cross-border.

**Gap:** Narrowest scope of any reviewed jurisdiction. Criminal statute only; no civil remedy; no political deepfake provisions.

---

### European Union

**Primary instrument:** Regulation (EU) 2024/1689 — Artificial Intelligence Act

**Key provisions:**
- *Article 50:* Providers of AI systems generating synthetic audio, video, or image content must ensure outputs are labeled as AI-generated; providers of general-purpose AI systems must watermark synthetically generated content
- *Articles 51–55:* GPAI models with systemic risk (>10²⁵ training FLOPs) face enhanced requirements including adversarial testing, incident reporting, and cybersecurity obligations
- *Annex III:* Biometric identification systems classified as high-risk — relevant to deepfake authentication bypass attacks (§5.2 of the paper)

**Enforcement timeline:**
| Date | Obligation |
|---|---|
| February 2025 | Prohibitions on unacceptable-risk AI in force |
| August 2025 | GPAI obligations in force |
| August 2026 | Full high-risk AI obligations in force |

**Four-criterion score: 3.5/4** — Transparency: ✓ | Watermarking: ✓ | Platform accountability: ✓ | Cross-border: Partial (extraterritorial scope strong; informal-channel enforcement practically difficult)

**Gap:** Enforcement against non-EU providers serving EU users through informal channels (peer-to-peer, encrypted messaging) remains practically challenging. Phased enforcement means full obligation coverage is still being implemented.

---

### China

**Primary instruments:**
- *Provisions on Deep Synthesis Internet Information Services* (CAC, effective March 2022)
- *Measures for the Administration of Generative Artificial Intelligence Services* (CAC, effective August 2023)

**Requirements:** Mandatory content labeling; real-name registration for providers; platform liability; prohibited uses include political manipulation, impersonation, and fraud; training data compliance obligations.

**Four-criterion score: 3/4** — Transparency: ✓ | Watermarking: ✓ (label requirement functions as watermark-equivalent) | Platform accountability: ✓ | Cross-border: ✗ (domestic focus)

**Limitation:** Enforcement applied inconsistently and primarily in politically sensitive contexts per international observers. The framework's breadth may reflect content control objectives beyond deepfake safety. Limited independent enforcement transparency.

---

### United Kingdom

**Primary instruments:**
- *Online Safety Act 2023:* Positive duties on user-to-user platforms to prevent illegal content (includes CSAM deepfakes and fraud-enabling deepfakes); risk assessment and moderation obligations; regulated by Ofcom
- *Criminal Justice Bill 2024:* Sharing intimate deepfake images without consent — criminal offense; up to 2 years imprisonment

**Four-criterion score: 2/4** — Transparency: Partial | Watermarking: ✗ | Platform accountability: ✓ | Cross-border: ✗

**Gap:** No general transparency or watermarking requirement for AI-generated content. The Online Safety Act creates strong platform duties but does not mandate synthetic content disclosure equivalent to EU AI Act Article 50.

---

### Australia

**Status:** No dedicated deepfake legislation as of early 2026.

**Applicable existing law:** Existing criminal law applies to some deepfake misuse; eSafety Commissioner has jurisdiction over certain harmful online content; no deepfake-specific transparency, watermarking, or platform accountability requirements.

**Four-criterion score: 0/4**

**Status:** Australian Law Reform Commission reviewing deepfake harms as of 2026. Government has acknowledged the regulatory gap.

---

## Cross-Jurisdictional Gap Table

The following gaps exist across all reviewed jurisdictions, regardless of individual framework maturity:

| Gap | Description | Affected jurisdictions |
|---|---|---|
| Transnational enforcement | No binding international coordination mechanism | All |
| Authentication bypass | No jurisdiction explicitly addresses deepfake attacks on KYC/biometric authentication | All |
| Training data consent | No jurisdiction requires consent for use of likenesses in generative model training | All |
| Watermarking interoperability | No international standard; EU and China have domestic requirements that are incompatible | All |
| Cryptographic provenance | C2PA standard is voluntary; no jurisdiction mandates it | All |
| Platform detection mandate | No jurisdiction requires platforms to deploy detection systems | All |
| Civil redress for fraud victims | Most jurisdictions lack specific civil redress for deepfake-enabled financial fraud | All except CA (limited) |

---

## Primary Recommendation (from §10.3)

The most significant governance gap is not within any jurisdiction but between them. An international framework — developed through the UN, OECD, or a dedicated multilateral body — establishing binding minimum standards in four areas is the highest-priority governance intervention not yet underway:

1. **Transparency and labeling** — minimum disclosure standards with cross-border recognition
2. **Watermarking interoperability** — a common technical standard recognizable across jurisdictions
3. **Platform detection obligations** — minimum detection deployment requirements with mutual recognition of certified systems
4. **Mutual legal assistance** — cross-border enforcement cooperation for deepfake-enabled crimes
