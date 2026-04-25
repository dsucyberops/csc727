# Detection Bias and Fairness — Synthesized Findings
## Project Phantom · /ethics · https://github.com/DSUcyberops/csc727

Supports §8.3 (Fairness and Bias) and the RQ1 answer in §10.1. Reflects the paper's integrated framing: detection bias is not merely a technical quality issue but an ethical harm that compounds existing inequities — connecting the technical dimension (§6) and the ethics dimension (§8).

---

## Why Detection Bias Is an Ethical Issue

Standard quality evaluation focuses on aggregate accuracy. Bias analysis reveals that aggregate accuracy conceals systematic differences in who is protected and who is harmed. A system achieving 96% aggregate accuracy but 65% for a specific demographic group is not providing 96% protection to that group — it is providing 65% protection while appearing to provide 96%.

This appearance of protection may prevent organizations and individuals from seeking alternative safeguards, making the bias actively harmful rather than merely suboptimal. When the groups receiving worse protection are also the groups most likely to be targeted by non-consensual deepfakes (women, younger individuals, marginalized communities), the bias compounds the harm.

This is the connection between §8.3 and §10.1: the ethical challenge of deepfakes (RQ1) cannot be addressed by deploying detection systems without first auditing and correcting demographic biases in those systems.

---

## Sources of Bias

### 1. Training Data Imbalance
Most benchmark deepfake detection datasets are scraped from publicly available internet video, systematically over-representing light-skinned individuals, male subjects (political and public-figure content), younger adults (18–40), and North American and European subjects. Models trained on these datasets learn features optimized for over-represented groups. On under-represented groups, the model encounters distribution shift, causing degradation in both directions: more false positives (authentic content flagged as synthetic) and, in some cases, fewer true positives.

### 2. Generation Artifact Variation Across Demographics
Generative models trained on imbalanced datasets produce different artifact patterns when generating faces from different demographic groups. Detection classifiers identifying those artifacts may perform differently across groups — not because detection is inherently harder for those individuals, but because the training distribution of deepfakes mirrors the training distribution of the generative model.

### 3. Skin Tone and Compression Artifacts
Visual artifact detection approaches are less reliable for individuals with darker skin tones because: contrast between face and background differs by skin tone; GAN and diffusion models produce different blending artifact patterns across skin tones; JPEG and H.264 compression affects darker tones differently, masking some artifact signals that detectors depend on.

### 4. Biological Signal Baseline Variation
Biological signal approaches rely on population-level physiological baselines (blink rates, micro-expressions, pulse). If training data for these baselines is demographically skewed, detectors perform worse on individuals whose physiological patterns differ from the training baseline — even when their content is genuine.

---

## Documented Performance Disparities

| Group | Bias direction | Mechanism | Source |
|---|---|---|---|
| Darker skin tones | Higher false positive rate | Visual artifact detectors misinterpret rendering variation as generation artifacts | Khan et al. (2025); Gong & Li (2024) |
| Women | Context-dependent | Non-consensual deepfake datasets over-represent women as subjects; detectors may be calibrated toward this context | Singh et al. (2025) |
| Older adults (60+) | Higher false positive rate | Facial texture variation may trigger artifact classifiers | Implied by Gong & Li (2024) dataset analysis |
| Non-Western facial features | Higher false positive rate | Training data under-representation causes distribution shift | Khan et al. (2025) |
| Private vs. public figures | Lower TP rate for private individuals | Models trained on celebrity deepfake datasets may not generalize to non-public individuals | Lin et al. (2025) |

*Note: Most reviewed papers do not explicitly report demographic performance breakdowns — this absence is itself a finding and a gap the research community must address.*

---

## The Safety Theater Risk

When a biased detection system is deployed with claims of deepfake protection:
- Well-represented demographic groups receive genuine protection
- Marginalized groups receive false assurance — they believe they are protected but are not
- Organizations stop seeking alternative protections because they believe the detection system covers them
- Affected individuals have false confidence that may delay reporting or seeking redress

This safety theater effect is more harmful than acknowledged absence of protection, because it prevents the corrective actions that acknowledged gaps would motivate.

---

## Six Recommended Mitigations

### 1. Diverse Dataset Curation
Benchmark datasets must explicitly balance demographic representation before data collection begins — not adjusted post-hoc. Sampling targets should be set for race, gender, age, and geography.

### 2. Mandatory Bias Auditing Before Deployment
Disaggregated performance metrics (FPR and TPR by demographic group) must be a deployment prerequisite, not an optional post-deployment audit.

### 3. Equitable Performance Standards
Governance frameworks should require minimum performance thresholds per demographic subgroup, not only in aggregate. A system meeting aggregate standards while failing subgroup standards should not pass deployment review.

### 4. Transparent Public Reporting
Platforms should publicly report disaggregated performance metrics on a regular cadence, enabling civil society audit of continued compliance.

### 5. Demographic Red-Teaming
Pre-deployment adversarial testing must specifically probe for demographic performance gaps — not only aggregate adversarial robustness. Red teams should include members of the demographic groups at highest risk of false positive harm.

### 6. User Feedback Mechanisms
Platforms should provide accessible mechanisms for reporting suspected false positives, with commitments to human review and correction timelines. This enables ongoing monitoring of real-world demographic bias that controlled pre-deployment evaluation cannot capture.
