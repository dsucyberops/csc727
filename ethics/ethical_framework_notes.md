# Ethical Framework Notes
## Project Phantom · /ethics · https://github.com/DSUcyberops/csc727

Extended analysis underlying the five ethical dimensions in §8. Also reflects the research gap framing from §2.5: prior governance literature is split between normatively grounded frameworks (Bateman et al., 2025) and operationally specific frameworks (Patel et al., 2026). The ethical analysis in this paper bridges that gap by grounding operational recommendations in explicit normative principles.

---

## 1. Consent and Identity Ownership

### The Pipeline Problem (§8.1)

Consent for deepfake use is commonly framed as a question about distribution: did the individual consent to appearing in this synthetic content? The paper argues this framing is too narrow. Consent must operate at every stage of the generation pipeline:

| Stage | Consent issue | Current status |
|---|---|---|
| Training data collection | Individuals depicted in scraped training data have not consented to use of their likeness for generative model training | Unregulated in most jurisdictions; voluntary commitments only |
| Model training | Generative capability is built on unconsented likenesses | No jurisdiction requires consent for training data inclusion |
| Content generation | Specific individuals depicted in synthetic content without approval | Addressed only for specific harms (non-consensual intimate imagery) in some jurisdictions |
| Distribution | Synthetic content reaches audiences who may not know it is synthetic | Addressed partially by EU AI Act Article 50 labeling requirements |

A consent framework adequate to address deepfake harm must operate at all four stages. Interventions targeting only distribution — the current norm — leave three stages unaddressed.

### Rights Framework vs. Property Framework

**Right of publicity (property framework):** Treats individual likeness as property with commercial value. Protects primarily against commercial exploitation. Provides limited protection for non-commercial deepfakes (political manipulation, harassment). Relevant: NO FAKES Act (proposed, U.S.).

**Right of informational self-determination (rights framework):** Treats control over one's digital identity as a fundamental right. Creates positive state obligations (governments must act), not merely individual prohibitions. Applies regardless of commercial motive. Relevant: EU AI Act Article 50; Bateman et al. (2025).

The rights framework provides stronger, broader protection, particularly for non-commercial deepfakes. The paper endorses this framework as the appropriate normative foundation in §8.1.

### Psychological Harm Evidence

The claim in §8.1 that non-consensual deepfakes cause severe and lasting psychological harm draws on the broader non-consensual intimate imagery (NCII) literature (deepfake-specific research is still emerging):
- Trauma outcomes comparable in severity to sexual assault, including PTSD, acute anxiety, and depression
- Persistent harm beyond content removal due to ongoing uncertainty about distribution scope
- Social withdrawal, employment consequences, and reputational damage
- Disproportionate targeting of young women and adolescent girls

---

## 2. The Liar's Dividend and Epistemic Harm

### Mechanism (§8.2)

The liar's dividend is a second-order harm distinct from any individual deepfake incident:

1. Deepfake technology becomes publicly known
2. This awareness creates plausible deniability: any individual in authentic incriminating media can claim it is synthetic
3. The claim generates epistemic uncertainty even when false — audiences who know deepfakes exist cannot easily dismiss it
4. Legal, journalistic, and political accountability mechanisms that depend on recorded evidence are structurally weakened

The critical feature, documented by Farid (2025) and empirically confirmed by Clark and Lewandowsky (2026): the liar's dividend does not require any actual deepfake. The mere existence and public awareness of deepfake capability is sufficient.

### Why Detection Cannot Eliminate the Liar's Dividend

Even perfect detection cannot eliminate the liar's dividend, for two reasons:

1. **Verification lag:** By the time a recording is authenticated, the accused has already had time to generate doubt and delay proceedings.
2. **Asymmetric epistemic burden:** Communicating "this video is authentic because its provenance chain checks out cryptographically" requires technical literacy. Saying "this could be a deepfake" requires only awareness that deepfakes exist.

The correct upstream intervention is authenticated content provenance (C2PA, watermarking) — shifting the burden of proof to authenticity rather than requiring victims to disprove synthetic origin after the fact.

### Legal Implications

The liar's dividend is most acute in legal proceedings:
- Documented cases exist of defendants contesting video evidence by alleging deepfake manipulation without technical basis
- Courts developed digital evidence authenticity standards assuming metadata integrity and chain of custody — both of which deepfakes can defeat
- Recommendations: require cryptographic provenance for digital video evidence after a jurisdiction-specific cutoff date; develop specific deepfake authentication standards for evidentiary rules (FRE equivalent)

---

## 3. Accountability and Transparency

### The Diffusion of Responsibility Problem (§8.4)

When a deepfake causes harm, responsibility is fragmented across:

| Actor | Role | Current accountability |
|---|---|---|
| Model developer | Created generative capability | Typically no liability — capability is dual-use |
| Platform hosting model | Enabled access to generation | Section 230 (U.S.) / equivalent immunity most jurisdictions |
| Content generator | Created specific harmful content | Often anonymous; may be in another jurisdiction |
| Platform distributing content | Hosted/amplified harmful content | Section 230 (U.S.); platform duties (Online Safety Act UK; EU AI Act) |
| End user sharing content | Extended distribution | Typically no liability unless specific intent demonstrated |

In practice, harm victims often cannot obtain redress from any actor in this chain because: the generator is anonymous; platforms claim immunity; the model developer's capability is lawful; cross-jurisdictional enforcement is absent.

### Transparency as an Accountability Prerequisite

Transparency requirements — mandatory disclosure of AI-generated content, retention of generation provenance logs — are necessary preconditions for accountability:

1. Make synthetic content visible to end users before persuasive damage occurs
2. Create an audit trail that supports forensic attribution
3. Shift the burden of provenance from victims (prove it's a deepfake) to producers (prove it's authentic)
4. Enable platform enforcement by providing a detectable signal

The paper's recommendation in §8.4 that transparency obligations be non-waivable throughout the content supply chain reflects this analysis. Optional transparency creates gaps that will be exploited by the actors who cause the most harm.

---

## 4. Research Ethics

### The Dual-Use Tension

Deepfake research creates a specific dual-use tension relevant to this paper:
- Detection research discloses weaknesses that adversarial actors can exploit to improve evasion
- Attack typology research (§5) catalogs methods that could serve as a roadmap for malicious actors
- Publication in open venues maximizes beneficial impact while maximizing adversarial accessibility

### How This Paper Manages the Tension

- **Source-only:** Draws exclusively on published academic literature; does not develop new attack methods or disclose novel detection vulnerabilities
- **Defensive framing:** All findings are framed in terms of improving detection, strengthening governance, and protecting affected individuals — not in terms of how attacks could be improved
- **No operational specificity:** §5 describes attack categories and documented impact but not step-by-step operational instructions
- **No human subjects:** No individuals were studied, observed, or exposed to content in the course of this research

### Norms for Future Research

- Detection vulnerability disclosures should follow responsible disclosure (notify platform developers before publication; allow remediation time)
- Attack research should include explicit dual-use risk discussion as a publication condition
- Dataset publication for detection research should address demographic balance and consent for depicted individuals
- Research incentive structures should reward defensive research with equivalent prestige to generative research — the current imbalance favors generation advances and compounds the detection deficit
