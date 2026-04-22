# Legislative Framework Notes
## Project Phantom — /governance

This document provides detailed notes underlying the jurisdictional comparison in Table 3 of the paper and supports the governance analysis in Section 7.

---

## Overview: The Governance Landscape

As of early 2026, no jurisdiction has enacted a comprehensive deepfake governance framework that simultaneously addresses all four core governance challenges identified in this paper:

1. **Transparency** — mandatory disclosure of AI-generated content to end users
2. **Watermarking** — technical embedding of provenance signals at generation time
3. **Platform accountability** — positive obligations on platforms hosting or distributing synthetic media
4. **Cross-border enforcement** — mechanisms to address the transnational character of production and distribution

The EU AI Act comes closest to addressing all four, but its watermarking and transparency enforcement is still being phased in and does not yet apply extraterritorially to all relevant actors.

---

## Jurisdiction-by-Jurisdiction Analysis

### United States (Federal)

**Status:** No federal deepfake-specific legislation enacted as of early 2026.

**Legislative history:**
- *DEFIANCE Act (2024):* Would create a federal civil cause of action for victims of non-consensual intimate deepfakes. Passed Senate; stalled in House as of review date.
- *NO FAKES Act (2024):* Would create a federal right of publicity for digital replicas of voice and likeness. Bipartisan support; not enacted.
- *Protect Elections from Deceptive AI Act:* Would prohibit materially deceptive AI-generated content in federal election advertising. Not enacted.

**Existing applicable law:**
- Section 230 of the Communications Decency Act provides significant platform immunity from third-party content liability, limiting platform accountability for deepfake distribution
- FTC Act Section 5 (unfair/deceptive acts) provides some basis for action against fraudulent deepfakes, but enforcement is slow and case-by-case
- State laws (see California, Texas below) fill some gaps but create inconsistent national coverage

**Key gap:** No federal framework for transparency, watermarking, or authentication. Absence of federal law means victim redress depends entirely on state of residence.

---

### United States — California

**Primary statutes:**
- AB 730 (2019): First U.S. deepfake law; prohibits distribution of deepfake political ads within 60 days of election without disclosure
- AB 602 (2023): Creates civil cause of action for non-consensual deepfake intimate imagery; right to injunctive relief and damages
- SB 926 (2024): Extends AB 602 protections and increases platform obligations for removal

**Strengths:** Comprehensive civil remedy for non-consensual intimate deepfakes; political disclosure requirement.

**Gaps:** Does not address commercial fraud, authentication bypass, or AI system watermarking. Platform safe harbors under Section 230 still limit third-party liability.

---

### United States — Texas

**Primary statute:** HB 4337 (2023) — criminalizes creation/distribution of deepfakes depicting sexual conduct without consent.

**Strengths:** Criminal penalties (Class A misdemeanor, up to 1 year; enhanced penalties for minors).

**Gaps:** Narrower scope than California; no civil remedy; no disclosure requirements; does not address political deepfakes or fraud.

---

### European Union

**Primary instrument:** Regulation (EU) 2024/1689 — Artificial Intelligence Act

**Relevant provisions:**
- Article 50: Transparency obligations for AI systems that generate or manipulate content; providers must ensure outputs are labeled as artificially generated or manipulated
- Articles 51–55: General-purpose AI (GPAI) model obligations; models with systemic risk (training compute > 10²⁵ FLOPs) face enhanced requirements including adversarial testing and incident reporting
- Annex III: High-risk AI system categories; biometric identification systems (relevant to deepfake authentication bypass) are classified as high-risk

**Enforcement:**
- EU AI Office (established 2024) has primary enforcement authority for GPAI models
- National Competent Authorities (one per member state) enforce for other AI systems
- Non-compliance penalties: up to €35 million or 7% of global annual turnover

**Timeline:**
- February 2025: Prohibitions on unacceptable-risk AI entered force
- August 2025: GPAI obligations entered force
- August 2026: Full high-risk AI obligations enter force

**Extraterritorial scope:** Applies to providers placing AI systems on the EU market regardless of establishment location; significant extraterritorial reach.

**Key gap:** Enforcement against non-EU providers serving EU users through informal channels (social media, peer-to-peer) is practically difficult.

---

### China

**Primary instruments:**
- *Provisions on the Administration of Deep Synthesis Internet Information Services* (CAC, effective March 2022): Requires labeling of AI-generated content; prohibits using deep synthesis technology to spread false information or impersonate individuals; real-name registration for providers
- *Measures for the Administration of Generative Artificial Intelligence Services* (CAC, effective August 2023): Extends obligations to generative AI generally; requires training data compliance; prohibits generation of false information

**Strengths:** Comprehensive content labeling requirements; strong platform liability; administrative penalties.

**Limitations noted in paper:** Enforcement has been applied inconsistently and particularly in politically sensitive contexts; the framework's breadth may reflect content control objectives beyond deepfake safety. Limited independent transparency on enforcement statistics.

---

### United Kingdom

**Primary instruments:**
- Online Safety Act 2023: Creates positive duties on regulated user-to-user services to prevent illegal content (which includes CSAM deepfakes and fraud-enabling deepfakes); requires risk assessments and content moderation
- Criminal Justice Bill 2024: Creates specific offense of sharing intimate deepfake images without consent; carries up to 2 years imprisonment

**Enforcement body:** Ofcom regulates Online Safety Act compliance; CPS prosecutes criminal offenses.

**Key gap:** No general transparency or watermarking requirement for AI-generated content; no equivalent of EU AI Act's broad disclosure obligations.

---

## Cross-Jurisdictional Gaps

The following gaps apply across all reviewed jurisdictions:

| Gap | Description | Affected Jurisdictions |
|---|---|---|
| Transnational enforcement | Content generated in one jurisdiction, hosted in a second, consumed in a third; no binding international coordination mechanism | All |
| Authentication bypass | No jurisdiction explicitly addresses deepfake attacks on KYC/biometric authentication systems | All |
| Training data consent | No jurisdiction requires consent for use of individual likenesses in generative model training data | All |
| Watermarking standards | Only EU mandates watermarking; no international interoperability standard exists | All except EU |
| Provenance chain | C2PA standard voluntary; no jurisdiction mandates cryptographic provenance tracking | All |
| Detection mandate | No jurisdiction requires platforms to deploy deepfake detection systems | All |

---

## Key Recommendation from This Analysis

The most significant governance gap is not within any jurisdiction but *between* jurisdictions. A binding international framework — developed through the UN, OECD, or a dedicated multilateral body — establishing minimum standards for (1) transparency/labeling, (2) provenance tracking, (3) platform detection obligations, and (4) mutual legal assistance in cross-border enforcement is the highest-priority governance intervention not yet underway.
