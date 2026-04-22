# Ethical Framework Notes
## Project Phantom — /ethics

This document provides the extended analysis underlying the five ethical dimensions addressed in Section 8 of the paper: consent and identity ownership, the liar's dividend, fairness and bias, accountability and transparency, and research ethics. It includes the analytical reasoning that connects the reviewed literature to the ethical positions taken in the paper.

---

## 1. Consent and Identity Ownership

### The Problem

Deepfake technology makes it trivially easy to create realistic synthetic media of any individual whose image or voice appears in publicly accessible data. This creates a fundamental mismatch between:

- The *legal status* of publicly shared content (often legally accessible for many purposes)
- The *reasonable expectation* of individuals who shared that content (typically not expecting it to be used to generate synthetic media depicting them)

### The Pipeline Problem

The consent issue is not limited to the distribution of the finished deepfake. It is distributed throughout the entire generation pipeline:

| Pipeline Stage | Consent Issue |
|---|---|
| Training data collection | Individuals depicted in scraped training data typically have not consented to use of their likeness for generative model training |
| Model training | The generative capability is built on unconsented likenesses |
| Synthetic content generation | Specific individuals are depicted in synthetic content they have not approved |
| Distribution | The synthetic content reaches audiences who may not know it is synthetic |

A consent framework adequate to address deepfake harm must operate at all four stages, not only at distribution.

### Identity as Property vs. Identity as Right

Two distinct legal frameworks apply to identity ownership:

- **Right of publicity** (property framework): Treats an individual's likeness as property with commercial value; protects primarily against commercial exploitation without consent. Relevant: NO FAKES Act (proposed, U.S.)
- **Right of informational self-determination** (rights framework): Treats control over one's digital identity representation as a fundamental right, not merely a commercial interest. Relevant: EU AI Act; Bateman et al. (2025) human rights framework

The rights framework is broader and more protective, particularly for non-commercial deepfakes (political manipulation, harassment) where the property framework provides limited protection.

### Psychological Harm Evidence

The paper's claim that non-consensual deepfakes cause "severe and lasting psychological harm" is grounded in research on non-consensual intimate imagery (NCII) more broadly, which demonstrates:

- Victims report outcomes equivalent to sexual assault trauma in severity
- Harm persists beyond removal of content due to ongoing uncertainty about distribution
- Social withdrawal, employment consequences, and reputational damage are widely documented
- Young women and adolescent girls are disproportionately targeted

---

## 2. The Liar's Dividend

### Mechanism

The liar's dividend describes a second-order harm distinct from any individual deepfake incident:

1. Deepfake technology becomes widely known
2. Public awareness creates plausible deniability for any individual who appears in authentic incriminating media
3. That individual can claim the media is a deepfake, regardless of whether it is
4. Even if the claim is false, the epistemic uncertainty creates reasonable doubt in audiences

### Empirical Grounding

Clark and Lewandowsky (2026) provide the strongest empirical grounding for the liar's dividend mechanism, demonstrating the "continued influence effect" — corrections do not fully displace the persuasive impact of previously consumed false content. This means:

- Even when a deepfake is identified and corrected, the original persuasive impact partially persists
- Symmetric: when authentic content is labeled potentially synthetic, the original persuasive impact is partially undermined even if the label is retracted

Farid (2025) argues this creates a structural epistemic problem — the liar's dividend is not caused by any specific deepfake but by the *existence* of deepfake capability, which is now a permanent feature of the information environment.

### Implications for Legal Systems

The liar's dividend is particularly acute in legal contexts:

- Video and audio evidence has traditionally been treated as highly credible
- Deepfake capability introduces plausible deniability for defendants contesting authenticity
- Authenticated content provenance (cryptographic signing, C2PA) is the primary technical mitigation
- Without provenance authentication, courts may need to develop new standards for digital evidence admissibility

---

## 3. Accountability and Transparency

### The Diffusion of Responsibility Problem

When a deepfake causes harm, identifying who is responsible involves:

| Actor | Role | Accountability Gap |
|---|---|---|
| Model developer | Created the generative capability | Typically no liability under existing law; capability is dual-use |
| Platform hosting the model | Enabled access to generation capability | Section 230 / equivalent provides immunity in most jurisdictions |
| Person who generated the deepfake | Created the specific harmful content | Often anonymous; may be in another jurisdiction |
| Platform distributing the content | Hosted/amplified the harmful content | Section 230 immunity in U.S.; platform duties under Online Safety Act in UK |
| End user who consumed/shared | Extended distribution | Typically no liability unless specific intent to harm demonstrated |

In practice, harm victims often cannot obtain redress from any actor in this chain because the chain is anonymous, cross-jurisdictional, and shielded by existing legal immunities at multiple points.

### Transparency Requirements as a Foundation for Accountability

Transparency requirements — mandatory disclosure of AI-generated content and retention of generation logs — are necessary preconditions for accountability because they:

1. Make the existence of synthetic content visible to end users (enabling informed skepticism)
2. Create an audit trail that supports forensic attribution when harm occurs
3. Shift the burden of provenance from victims (who must prove a deepfake) to producers (who must prove authenticity)
4. Enable platform enforcement by providing a detectable signal for content moderation

The paper's recommendation that transparency obligations be non-waivable and apply throughout the content supply chain is grounded in this analysis: optional transparency creates predictable gaps that bad actors will exploit.

---

## 4. Research Ethics in Deepfake Scholarship

### The Dual-Use Problem for Researchers

Deepfake research creates a specific form of dual-use tension:

- Research on detection methods inherently discloses detection weaknesses, which adversarial actors can exploit to improve evasion
- Research on attack typologies (like Section 5 of this paper) catalogues attack methods that could serve as a roadmap for malicious actors
- Publication in open venues maximizes beneficial impact (practitioners can use findings) while also maximizing adversarial accessibility

### How This Paper Manages the Tension

1. **Source-only approach:** This review draws exclusively on published academic literature. It does not develop new attack methods, generate deepfake content, or disclose novel detection vulnerabilities.

2. **Defensive framing:** All findings are framed in terms of defensive applications — improving detection, strengthening governance, protecting affected individuals — not in terms of how attacks could be improved.

3. **No operational specificity:** The cybersecurity section (Section 5) describes attack categories and documented impact but does not provide step-by-step operational instructions that would enable a non-technical actor to execute an attack.

4. **No human subjects:** No individuals were studied, observed, or exposed to content in the course of this research.

### Norms for Future Research

Based on the ethical analysis in this paper, the following norms are recommended for deepfake research:

- Detection vulnerability disclosures should follow responsible disclosure practices (notify platform developers before publication; allow remediation time)
- Attack research should include explicit discussion of dual-use risks and defensive framing
- Dataset publication for detection research should address demographic balance and consent for depicted individuals
- Research incentive structures (publication requirements, grant criteria) should reward defensive research with equivalent prestige to generative research
