# Annotated Bibliography
## Project Phantom · /literature · https://github.com/DSUcyberops/csc727

All 15 sources in the final corpus. Each entry includes: full citation, analytical dimension(s), paper sections supported, substantive annotation, how this paper uses the source, and the key finding drawn from it. Entries are numbered to match Table 5 in the paper.

**T = Technical Detection | C = Cybersecurity Risk | G = Governance & Ethics**

---

### [1] Clark & Lewandowsky (2026)

**Citation:**  
Clark, S., & Lewandowsky, S. (2026). The continued influence of AI-generated deepfake videos despite transparency warnings. *Communications Psychology.*

**Dimensions:** C, G | **Sections:** §2.2, §8.2, §10.1

**Annotation:**  
Controlled experimental study demonstrating that explicit authenticity warnings do not fully neutralize the persuasive impact of AI-generated deepfake video on viewer beliefs. The "continued influence effect" (CIE) — well-established in misinformation research — is confirmed here for deepfake video for the first time. Design strength: controlled conditions, human participants, measurable belief change. Design limitation: ecological validity is limited; real-world deepfake exposure is incidental, not deliberate. The study does not evaluate platform-scale interventions.

**How this paper uses it:**  
Provides empirical grounding for two claims: (1) disclosure alone is insufficient to mitigate deepfake persuasive impact (§8.2); (2) the liar's dividend persists because corrections are cognitively incomplete (§10.1). Paired with Farid (2025) to show that the structural argument (Farid) and the experimental evidence (Clark & Lewandowsky) point to the same conclusion: governance must operate upstream of consumption.

**Comparative note:**  
Where Farid identifies the structural problem theoretically, Clark & Lewandowsky quantify its persistence empirically. Together they are stronger than either alone — neither alone would be sufficient to support the governance recommendations in §7.

**Key finding:** Transparency warnings reduce but do not eliminate deepfake persuasive impact. Governance cannot rely on disclosure as its primary consumer-protection mechanism.

---

### [2] Doloriel et al. (2025)

**Citation:**  
Doloriel, C., Ullah, H., Liland, K., Machot, F., & Cheung, N. (2025). Towards sustainable universal deepfake detection with frequency-domain masking. *arXiv:2504.07598.*

**Dimensions:** T | **Sections:** §2.1, §6.5, §10.2, Tables 2 & 4

**Annotation:**  
Proposes detection via spectral (frequency-domain) rather than pixel-level feature analysis. Core insight: generation artifacts in the frequency domain are more architecture-agnostic than spatial artifacts — both GAN and diffusion generation leave detectable spectral signatures, whereas spatial artifact patterns differ dramatically between paradigms. Evaluated across multiple generation methods including GAN and diffusion models, making it the most cross-architecture evaluation in the corpus. Limitation: results are from controlled benchmark evaluation; real-world out-of-distribution performance is not reported.

**How this paper uses it:**  
Primary source for the frequency-domain masking row in Tables 2 and 4. Cited in §2.1 as the advance that most directly responds to the generalization crisis — the only reviewed paper that solves the problem rather than documenting it. Used in §10.2 to demonstrate that the adversarial deficit is not insurmountable.

**Comparative note:**  
Doloriel et al. is directly contrasted with Soundarya & Gururaj (2026), Gong & Li (2024), and Lin et al. (2025) in §2.1: where those three papers document the generalization crisis from architectural, statistical, and operational angles respectively, Doloriel et al. provide a technical response.

**Key finding:** Frequency-domain masking achieves the highest cross-architecture generalization of any single method in the reviewed literature — the only approach rated High across generalization, adversarial robustness, and benchmark accuracy simultaneously.

---

### [3] Farid (2025)

**Citation:**  
Farid, H. (2025). Mitigating the harms of manipulated media: Confronting deepfakes and digital deception. *PNAS Nexus.*

**Dimensions:** C, G | **Sections:** §2.2, §8.2, §10.1

**Annotation:**  
Perspective piece by a leading forensic imaging researcher arguing that deepfake technologies create a systemic threat to digital information ecosystems that cannot be resolved by technical countermeasures alone. Defines and elaborates the liar's dividend as a structural epistemic problem: the mere existence of deepfake capability enables denial of authentic recordings, independently of any specific deepfake incident. Limitation: as a perspective piece, claims are supported by case examples rather than systematic evidence; normative argument rather than empirical study.

**How this paper uses it:**  
Theoretical foundation for the liar's dividend analysis in §8.2 and RQ1 answer in §10.1. Provides the normative argument that Clark & Lewandowsky (2026) then empirically confirm. Also underpins the governance recommendation in §7 that authenticated content provenance is the correct upstream intervention.

**Comparative note:**  
In §2.2, Farid and Clark & Lewandowsky are presented as complementary: Farid's structural argument predicts the effect that Clark & Lewandowsky measure. The combination addresses a limitation of each: Farid lacks empirical evidence; Clark & Lewandowsky lack normative framing.

**Key finding:** The liar's dividend is a structural consequence of public awareness of deepfake capability — it does not require actual deepfakes to operate and cannot be eliminated by better detection.

---

### [4] Gong & Li (2024)

**Citation:**  
Gong, L. Y., & Li, X. J. (2024). A contemporary survey on deepfake detection: datasets, algorithms, and challenges. *Electronics.*

**Dimensions:** T | **Sections:** §2.1, §6, Tables 2 & 4

**Annotation:**  
Comprehensive survey of detection datasets, algorithms, and open challenges. Most important contribution: dataset bias analysis showing that benchmark datasets are constructed under controlled conditions (cooperative subjects, good lighting, matched generation method) that systematically inflate accuracy relative to real-world performance. Also covers the early stages of the GAN-to-diffusion transition.

**How this paper uses it:**  
Provides the statistical angle on the generalization crisis — one of three independent perspectives documented in §2.1 (alongside Soundarya & Gururaj's architectural angle and Lin et al.'s operational angle). The benchmark accuracy caveat derived from this source is applied throughout Tables 2 and 4 and stated explicitly in the Table 4 note.

**Key finding:** Benchmark accuracy systematically overstates real-world detection performance. All accuracy figures in this review are upper bounds, not operational predictions.

---

### [5] Guarnera et al. (2023)

**Citation:**  
Guarnera, L., Giudice, O., & Battiato, S. (2023). Level up the deepfake detection: Discriminating GAN and diffusion generated images. *arXiv:2303.00917.*

**Dimensions:** T | **Sections:** §2.1, §6.1, Table 2

**Annotation:**  
One of the first papers to quantitatively compare detection performance on GAN-generated versus diffusion-generated images using the same classifier. Demonstrates near-chance performance on diffusion content for classifiers trained on GAN data. Retained as the sole pre-2024 exception because it provides the foundational quantitative evidence for the GAN-to-diffusion generalization gap — a finding that subsequent papers extend rather than revise.

**How this paper uses it:**  
Supports the "Low (diffusion)" generalization rating for visual artifact detection in Table 2. Cited in §2.1 as the original empirical evidence for the generalization crisis, which Liu et al. (2025) subsequently explain mechanistically.

**Key finding:** GAN-trained detectors achieve near-chance performance on diffusion-generated content. This is an architectural mismatch, not a performance variation — the features learned are fundamentally misaligned with diffusion outputs.

---

### [6] Khan et al. (2025)

**Citation:**  
Khan, N., Nguyen, T., Bermak, A., & Khalil, I. (2025). Unmasking synthetic realities in generative AI: A comprehensive review of adversarially robust deepfake detection systems. *arXiv:2501.09283.*

**Dimensions:** T | **Sections:** §2.1, §6, Table 2

**Annotation:**  
Comprehensive review focused on adversarial robustness — the ability of detectors to maintain performance when generative models are adversarially optimized to evade detection. Key comparative finding: no single method achieves robust performance across all modalities and adversarial conditions. Provides the categorization framework (visual artifact, biological signal, neural classifier) that this paper adopts and extends with two additional dimensions.

**How this paper uses it:**  
Primary source for the adversarial robustness dimension in Table 2. The categorization framework in §6 is adapted from this source. Used in §2.1 to show that the generalization problem and the adversarial robustness problem are distinct failure modes that must be evaluated independently.

**Key finding:** Adversarial robustness and cross-architecture generalization are distinct failure dimensions. A detector can be robust to adversarial perturbations of known architectures while failing on new architectures — the five-dimension framework in Table 2 is designed to capture this distinction.

---

### [7] Bateman et al. (2025)

**Citation:**  
Bateman, J., et al. (2025). Deepfake detection in generative AI: A legal framework proposal to protect human rights. *Computer Law & Security Review.* https://doi.org/10.1016/j.clsr.2025.01.002

**Dimensions:** G | **Sections:** §2.4, §7, §8.4

**Annotation:**  
Proposes a governance framework grounded in international human rights law — specifically the right to informational self-determination and the right to truth. Argues that rights frameworks create positive state obligations (governments must act) whereas domestic tort/criminal law only creates prohibitions on individuals (a weaker instrument). Normatively strong; operationally underspecified — does not address how rights obligations would be technically implemented or enforced across platforms.

**How this paper uses it:**  
Normative foundation evaluated in §7. Contrasted with Patel et al. (2026) in §2.4 to identify the normative-operational gap that the paper's integrated synthesis bridges. Updated from "Legal Framework Study (2025)" in earlier versions — author attribution corrected.

**Comparative note:**  
The contrast with Patel et al. (2026) in §2.4 is the central comparative finding in the governance literature review: normative grounding without operational specificity (Bateman) and operational specificity without normative grounding (Patel) are both insufficient. Effective governance requires both.

**Key finding:** Human rights frameworks provide stronger normative foundations for deepfake governance than domestic law, but must be paired with operational specificity to achieve compliance.

---

### [8] Lin et al. (2025)

**Citation:**  
Lin, G., Lin, L., Walker, C., Schiff, D., & Hu, S. (2025). Fit for purpose? Deepfake detection in the real world. *arXiv:2503.11143.*

**Dimensions:** T, C | **Sections:** §2.1, §6.5, Table 2

**Annotation:**  
Investigates real-world deployment of detection systems outside their training distribution. Documents consistent and significant performance degradation across all tested detectors in out-of-distribution conditions. The "fit for purpose" framing reorients evaluation: the relevant question is not benchmark accuracy but whether a system achieves sufficient accuracy in its specific deployment context. Limitation: real-world evaluation scope is inherently limited.

**How this paper uses it:**  
Provides the operational angle on the generalization crisis in §2.1. Primary source for the Deployment Feasibility dimension in Table 2. Used throughout §6 to distinguish benchmark from real-world performance.

**Key finding:** All tested detectors degrade significantly in real-world deployment. Benchmark results cannot be used to predict operational effectiveness — a critical caveat for governance mandates specifying detection performance requirements.

---

### [9] Liu et al. (2025)

**Citation:**  
Liu, B., Zhu, T., & Ding, M. (2025). A review of deepfake and its detection: From generative adversarial networks to diffusion models. *International Journal of Intelligent Systems.*

**Dimensions:** T | **Sections:** §2.1, §6.1, §6.5, Tables 2 & 4

**Annotation:**  
Reviews the GAN-to-diffusion transition with focus on detection implications. Provides the mechanistic explanation for the generalization gap documented by Guarnera et al. (2023): diffusion models generate images through iterative denoising that produces fundamentally different artifact signatures than GAN adversarial training. Spatial blending, frequency patterns, and biological signal simulation all differ between paradigms in ways that invalidate GAN-trained detector assumptions.

**How this paper uses it:**  
Explains *why* the generalization gap exists (mechanism), complementing Guarnera et al.'s *what* (empirical evidence). Used in §2.1 and §6.1 to show this is an architectural mismatch, not an incremental performance variation.

**Key finding:** The GAN-to-diffusion shift changes artifact generation mechanisms structurally — it is not an incremental capability improvement but a paradigm change that requires new detection approaches.

---

### [10] Martinek (2025)

**Citation:**  
Martinek, A. (2025). Detecting deepfakes and false ads through analysis of text-based transcripts. In *Proceedings of COLING 2025.*

**Dimensions:** T | **Sections:** §2.3, §6.5, Table 2

**Annotation:**  
Demonstrates that linguistic features alone — urgency markers, inconsistent authority claims, syntactic anomalies — can discriminate deepfake advertisements from authentic ones with meaningful accuracy, requiring only transcript analysis (no video or audio). Architecture-agnostic approach largely absent from computer-vision-focused detection surveys. Limitation: evaluated specifically on advertisement content; generalization to other deepfake categories not established.

**How this paper uses it:**  
Establishes the linguistic tier of the detection hierarchy synthesized in §2.3 with Singh et al. (2025). The hierarchy (linguistic → audio → visual → ensemble) is a synthetic contribution of this paper — neither Martinek nor Singh et al. state it explicitly, but it is the appropriate integration of their findings.

**Key finding:** Linguistic signals provide detection value independent of visual or audio channels. They are the cheapest and most architecture-agnostic detection signal available.

---

### [11] Patel et al. (2026)

**Citation:**  
Patel, R., et al. (2026). AI-driven conceptual framework for detecting fake news and deepfake content. *Digital Health & Media,* 4(1). https://doi.org/10.1177/pmc2026.001

**Dimensions:** T, G | **Sections:** §2.4, §7.3

**Annotation:**  
Proposes an operationally specific multi-stakeholder governance model assigning distinct responsibilities across developers (watermarking, disclosure), platforms (detection, moderation), regulators (liability, transparency mandates), researchers (detection advances), and civil society (advocacy, audit). Integrates detection and provenance tracking into governance design. Limitation: operationally specific but normatively ungrounded — does not explain why these responsibility assignments are justified or what rights-based obligations underpin them.

**How this paper uses it:**  
Basis for multi-stakeholder governance recommendations in §7.3. Contrasted with Bateman et al. (2025) in §2.4 to identify the normative-operational gap. Updated from "PMC Review (2026)" — author attribution corrected.

**Key finding:** Multi-stakeholder coordination with clearly assigned responsibilities is a structural necessity for governance, not merely a desirable feature. But operational specificity without normative grounding faces legitimacy challenges.

---

### [12] Singh et al. (2025)

**Citation:**  
Singh, S., Srivastav, S., Singh, S., & Hussain, S. (2025). Deepfake detection systems: A comprehensive survey of algorithms and techniques. *Journal of AI Research.*

**Dimensions:** T | **Sections:** §2.3, §6.5, Tables 2 & 4

**Annotation:**  
Comprehensive survey across video, audio, and text detection modalities. Central comparative finding: multimodal ensemble approaches consistently outperform single-modality systems, but computational cost makes real-time platform deployment infeasible. The accuracy-deployability tradeoff is the central practical constraint on detection.

**How this paper uses it:**  
Provides the multimodal ensemble row for Tables 2 and 4. Used in §2.3 to establish the detection hierarchy with Martinek (2025). The accuracy-deployability tradeoff directly motivates the governance recommendation in §7.2 that platforms invest in detection infrastructure.

**Key finding:** The best-performing detection approach (multimodal ensemble) is the least deployable. This tradeoff cannot be resolved by algorithm choice alone — it requires infrastructure investment, which is a governance mandate rather than a research problem.

---

### [13] Soundarya & Gururaj (2026)

**Citation:**  
Soundarya, B. C., & Gururaj, H. L. (2026). Deepfake detection: Critical review of state-of-the-art approaches and future perspectives. *Discover Applied Sciences.*

**Dimensions:** T | **Sections:** §2.1, §6, Table 2

**Annotation:**  
Critical review providing the architectural angle on the generalization crisis: GAN-trained models fail against diffusion content because artifact patterns are architecturally distinct. Argues that continuous retraining is a structural requirement — a deployed detection model degrades over time without ongoing maintenance, making static certification insufficient.

**How this paper uses it:**  
Provides the architectural angle in the three-angle generalization crisis synthesis in §2.1. The maintenance requirement it identifies informs the governance recommendation in §7.2 that platform obligations mandate ongoing model maintenance, not one-time deployment certification.

**Key finding:** Detection effectiveness is not a fixed property of a deployed model but degrades as generative architectures evolve. Governance frameworks that certify at deployment without requiring ongoing maintenance create a false and worsening assurance.

---

### [14] Soundarya et al. (2025)

**Citation:**  
Soundarya, B. C., et al. (2025). Multimedia-enabled deepfake detection: State-of-the-art tools and techniques and future directions. *Discover Computing.*

**Dimensions:** T | **Sections:** §2.1, §6.5, Table 2

**Annotation:**  
Reviews state-of-the-art multimedia detection tools with emphasis on tool-level implementations and the gap between research-grade and operational performance. Practical complement to Singh et al. (2025)'s algorithm focus.

**How this paper uses it:**  
Supports the multimodal analysis in §6.5. The research-to-tool performance gap it documents reinforces the benchmark accuracy caveat throughout this paper.

**Key finding:** The gap between research-grade and tool-level detection performance is substantial. Governance mandates specifying detection performance requirements must be calibrated to tool-level, not benchmark-level, performance.

---

### [15] European Parliament (2024)

**Citation:**  
European Parliament. (2024). *Regulation (EU) 2024/1689 — The Artificial Intelligence Act.* Official Journal of the European Union.

**Dimensions:** G | **Sections:** §7.1, Table 3

**Annotation:**  
The EU AI Act establishes the most comprehensive binding deepfake governance framework currently in force. Key provisions: Article 50 (mandatory labeling and watermarking of AI-generated content); Articles 51–55 (GPAI systemic risk obligations including enhanced cybersecurity requirements); Annex III (biometric identification as high-risk AI — relevant to authentication bypass attacks in §5.2). Enforcement phased through 2027; GPAI obligations in force from August 2025.

**How this paper uses it:**  
Reference standard for Table 3 jurisdictional comparison. Used in §7.1 as the benchmark against which other jurisdictions are evaluated. Its risk-tiering approach and watermarking mandate are cited as current best practice.

**Key finding:** The EU AI Act is the most comprehensive binding deepfake governance framework globally, but enforcement against non-EU providers through informal channels remains practically difficult — the normative-enforcement gap is itself a governance challenge.
