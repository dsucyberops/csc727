# Detection Bias and Fairness — Synthesized Findings
## Project Phantom — /ethics

This document synthesizes findings from the reviewed literature on demographic bias in deepfake detection systems. It supports the analysis in Section 8.3 of the paper (Fairness and Bias in Detection Systems).

---

## Summary

Deepfake detection models exhibit measurable and consistent demographic biases that cause them to perform differently across racial, gender, and age groups. These biases manifest in two directions:

- **False positive bias:** Some demographic groups are more likely to be incorrectly flagged as synthetic when their content is genuine
- **True positive deficit:** Some groups are *less* likely to have actual deepfakes detected, meaning synthetic content of those individuals passes undetected at higher rates

Both types of disparity have harmful consequences, and together they represent a form of algorithmic unfairness that must be addressed as a prerequisite for responsible large-scale deployment.

---

## Sources of Bias

### 1. Training Data Imbalance

Most benchmark deepfake detection datasets are constructed from publicly available video data scraped from the internet. This data systematically over-represents:
- Light-skinned individuals
- Male subjects (particularly in political and public-figure content)
- Younger adults (18–40)
- North American and European subjects

As a result, detectors trained on these datasets learn features that are optimized for the over-represented demographic groups. When applied to individuals from under-represented groups, the models encounter distribution shift — their learned features are less reliable — leading to performance degradation.

### 2. Generation Artifact Variation Across Demographics

Generative models trained on the same imbalanced datasets produce different artifact patterns when generating faces from different demographic groups. Detection classifiers trained to identify these artifacts may perform differently on deepfakes targeting different groups, not because the deepfakes are harder to detect in principle, but because the training distribution of *deepfakes* also reflects the training distribution of the generative model.

### 3. Skin Tone and Compression Artifacts

Some detection approaches based on visual artifacts rely on subtle variations in skin tone rendering and blending at facial boundaries. These signals are less discriminative for individuals with darker skin tones because:
- Contrast between face and background is different
- GAN and diffusion models both produce different artifact patterns for different skin tones
- Compression (JPEG, H.264) affects darker tones differently, masking some artifact signals

---

## Documented Disparities

The following table summarizes demographic performance disparities reported or implied across reviewed sources:

| Group | Direction of Bias | Mechanism | Source |
|---|---|---|---|
| Darker skin tones | Higher FP rate (flagged as synthetic when genuine) | Visual artifact detectors confuse rendering variations with generation artifacts | Khan et al. (2025); Gong & Li (2024) |
| Women | Mixed (context-dependent) | Non-consensual deepfake datasets over-represent women as subjects; detection models optimized for this context may not generalize | Singh et al. (2025) |
| Older adults (60+) | Higher FP rate | Facial texture variation in older faces may trigger artifact classifiers | Implied by Gong & Li (2024) dataset analysis |
| Non-Western facial features | Higher FP rate | Training data under-representation leads to distribution shift | Khan et al. (2025) |
| Public figures vs. private individuals | Lower TP rate for private individuals | Detection models trained on celebrity/politician deepfakes may not generalize to deepfakes of non-public individuals | Lin et al. (2025) |

*Note: Most reviewed papers do not explicitly report demographic breakdowns. The above reflects inferences from dataset descriptions and implied performance characteristics.*

---

## Ethical Implications

### Compounding Harm for Already Vulnerable Groups

Bias in detection systems is not merely a technical inconvenience — it has concrete ethical consequences:

1. **False positives harm authentic expression.** Individuals from marginalized groups whose genuine content is repeatedly flagged as synthetic face compounded barriers to digital participation: their authentic communications may be suppressed, demoted, or removed based on algorithmic error.

2. **True positive deficits enable targeted harm.** If detection systems are less effective at identifying deepfakes of certain demographic groups, those groups receive less protection from the harms deepfakes can cause — non-consensual intimate imagery, identity fraud, reputational attacks.

3. **Scale amplifies the harm.** Detection systems deployed at platform scale make millions of decisions per day. A small demographic bias in per-decision error rates translates to a large absolute number of harmful misclassifications, disproportionately affecting the groups already at higher risk from deepfake misuse.

### The "Safety Theater" Risk

If a platform deploys a biased detection system and claims it is protecting users from deepfakes, the system may provide:
- Genuine protection to well-represented demographic groups
- False assurance to marginalized groups who believe they are protected but are not

This creates a form of safety theater that is arguably more harmful than no detection claim at all, because it prevents organizations from pursuing alternative protections and gives affected individuals false confidence.

---

## Recommended Mitigations

The following mitigations are drawn from the reviewed literature and from the ethics analysis in Section 8.3:

1. **Diverse dataset curation:** Benchmark datasets must explicitly balance demographic representation across race, gender, age, and geography. This requires active curation, not passive scraping.

2. **Mandatory bias auditing:** Before deployment, detection models should be evaluated for demographic fairness using disaggregated performance metrics (accuracy, FPR, TPR by demographic group). This should be a deployment prerequisite, not an optional step.

3. **Equitable performance standards:** Governance frameworks should require that deployed detection systems meet minimum performance thresholds *for each demographic subgroup*, not solely aggregate accuracy. A system that achieves 96% aggregate accuracy while performing at 60% for a specific demographic group should not pass deployment review.

4. **Transparent reporting:** Platforms deploying detection systems should publicly report disaggregated performance metrics, enabling civil society audit.

5. **Red-teaming for demographic disparities:** Pre-deployment adversarial testing should specifically probe for demographic performance gaps, not solely for aggregate robustness.
