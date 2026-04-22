# Annotated Bibliography
## Project Phantom — /literature

Each entry includes: full citation, classification by analytical dimension, brief annotation, and relevance to paper sections.

**Analytical dimensions:** T = Technical Detection | C = Cybersecurity Risk | G = Governance & Ethics

---

### [1] Clark & Lewandowsky (2026)

**Citation:**  
Clark, S., & Lewandowsky, S. (2026). The continued influence of AI-generated deepfake videos despite transparency warnings. *Communications Psychology*.

**Dimensions:** G, C  
**Paper sections:** §2.2, §8.2, §10.1

**Annotation:**  
Empirical study demonstrating that AI-generated deepfake videos continue to influence viewer beliefs even after explicit authenticity warnings are displayed. The authors document the "continued influence effect" — a well-established cognitive phenomenon whereby corrections fail to fully displace initially encountered misinformation. This paper provides the primary empirical grounding for the liar's dividend argument developed in Section 8.2 and for the claim in Section 10.1 that disclosure alone is insufficient to mitigate the persuasive impact of deepfakes. The study uses controlled experimental design with human participants and represents one of the highest-quality empirical sources in this review.

**Key finding for this paper:** Transparency warnings do not neutralize the persuasive effect of deepfake content; cognitive interventions must address underlying processing biases, not merely information disclosure.

---

### [2] Doloriel et al. (2025)

**Citation:**  
Doloriel, C., Ullah, H., Liland, K., Machot, F., & Cheung, N. (2025). Towards sustainable universal deepfake detection with frequency-domain masking. arXiv:2504.07598.

**Dimensions:** T  
**Paper sections:** §2.1, §6.5, §10.2, Table 2, Table 4

**Annotation:**  
Proposes a detection approach that operates in the frequency domain rather than at the pixel level, using spectral masking to identify generation artifacts that are architecture-agnostic. The method achieves higher cross-architecture generalization than any single-modality approach reviewed in this study, making it the strongest current candidate for practical deployment. The paper evaluates the approach across multiple generation methods including both GAN-based and diffusion-based systems, which is the key methodological strength relative to earlier detection work.

**Key finding for this paper:** Frequency-domain masking is the only approach in the reviewed literature rated High across generalization, adversarial robustness, and benchmark accuracy simultaneously. Cited in Table 2 as the method with the best generalization-to-cost ratio.

---

### [3] Farid (2025)

**Citation:**  
Farid, H. (2025). Mitigating the harms of manipulated media: Confronting deepfakes and digital deception. *PNAS Nexus*.

**Dimensions:** G, C  
**Paper sections:** §2.2, §8.2, §10.1

**Annotation:**  
Broad perspective piece by a leading forensic imaging researcher arguing that deepfake technologies pose a systemic threat to digital information ecosystems and that technological countermeasures alone are insufficient without complementary policy and regulatory frameworks. Introduces and elaborates the concept of the liar's dividend as a structural epistemic problem distinct from any individual deepfake incident. Advocates for a multi-pronged response including watermarking, platform transparency, and media literacy as complementary interventions.

**Key finding for this paper:** The liar's dividend operates independently of specific deepfake incidents — it is a systemic consequence of deepfake awareness, not of deepfake exposure. This distinction is foundational to the RQ1 answer in Section 10.1.

---

### [4] Gong & Li (2024)

**Citation:**  
Gong, L. Y., & Li, X. J. (2024). A contemporary survey on deepfake detection: datasets, algorithms, and challenges. *Electronics*.

**Dimensions:** T  
**Paper sections:** §2.1, §6, Table 2

**Annotation:**  
Comprehensive survey covering the landscape of deepfake detection datasets, algorithmic approaches, and open challenges as of 2024. Identifies dataset bias as a primary limiting factor, noting that most benchmark datasets are constructed under controlled conditions that do not reflect real-world deepfake distribution. This has significant implications for the interpretation of reported benchmark accuracy figures across detection methods.

**Key finding for this paper:** Controlled-condition benchmark accuracy is systematically higher than real-world performance due to dataset construction bias. This caveat is reflected in the "Benchmark Accuracy" column of Table 2 and the notes accompanying Table 4.

---

### [5] Guarnera et al. (2023)

**Citation:**  
Guarnera, L., Giudice, O., & Battiato, S. (2023). Level up the deepfake detection: Discriminating GAN and diffusion generated images. arXiv:2303.00917.

**Dimensions:** T  
**Paper sections:** §2.1, §6.1, Table 2

**Annotation:**  
One of the earlier papers to systematically compare detection performance on GAN-generated versus diffusion-model-generated images. Demonstrates that classifiers trained on GAN-generated content fail to generalize to diffusion-based outputs, providing quantitative evidence for the generalization problem that motivates much of Section 6's analysis. Although published in 2023 and therefore reflecting a slightly earlier state of the field, it establishes the GAN-to-diffusion generalization gap that subsequent papers confirm and extend.

**Key finding for this paper:** Detection classifiers are not architecture-agnostic; the GAN-to-diffusion shift represents a fundamental generalization challenge, not merely a performance variation. Supports the "Low (diffusion)" generalization rating for Visual Artifact Detection in Table 2.

---

### [6] Khan et al. (2025)

**Citation:**  
Khan, N., Nguyen, T., Bermak, A., & Khalil, I. (2025). Unmasking synthetic realities in generative AI: A comprehensive review of adversarially robust deepfake detection systems. arXiv:2501.09283.

**Dimensions:** T  
**Paper sections:** §2.1, §6, Table 2

**Annotation:**  
Comprehensive review focusing specifically on adversarial robustness of detection systems — the ability of detectors to maintain performance when generative models are optimized to evade them. Categorizes detection methods into visual artifact analysis, biological signal detection, and neural network-based classifiers. Critically demonstrates that no single detection method achieves robust performance across all deepfake modalities. The categorization framework in this paper forms the basis for the detection taxonomy used in Section 6 and Table 2.

**Key finding for this paper:** Adversarial robustness and cross-modality generalization are distinct failure modes; detection systems can be robust to adversarial perturbation of their training distribution while still failing on out-of-distribution generation methods. The five-dimension framework in Table 2 reflects this distinction.

---

### [7] Bateman et al. (2025)

**Citation:**  
Bateman, J., et al. (2025). Deepfake detection in generative AI: A legal framework proposal to protect human rights. *Computer Law & Security Review*. https://doi.org/10.1016/j.clsr.2025.01.002

**Dimensions:** G  
**Paper sections:** §2.4, §7, §8.4

**Annotation:**  
Proposes a legal framework for deepfake governance grounded in international human rights law, emphasizing the right to informational self-determination (the right to control one's own digital identity) and the right to truth (the right to access authentic information). Highlights the tension between freedom of expression protections and the need to regulate harmful synthetic content. The framework is evaluated in Section 7 of this paper against concrete jurisdictional examples.

**Key finding for this paper:** Human rights law provides a stronger normative foundation for deepfake governance than existing domestic tort or criminal frameworks because it establishes positive obligations on states, not merely prohibitions on individuals.

---

### [8] Lin et al. (2025)

**Citation:**  
Lin, G., Lin, L., Walker, C., Schiff, D., & Hu, S. (2025). Fit for purpose? Deepfake detection in the real world. arXiv:2503.11143.

**Dimensions:** T, C  
**Paper sections:** §2.1, §6.5, Table 2

**Annotation:**  
Investigates real-world deployment of deepfake detection systems outside their training distribution. Finds significant and consistent performance degradation across all tested detectors when evaluated on out-of-distribution content, raising questions about the real-world utility of detection systems evaluated solely on benchmark datasets. Emphasizes the need for ecologically valid evaluation protocols as a prerequisite for meaningful performance claims.

**Key finding for this paper:** Benchmark accuracy systematically overestimates real-world detection performance; the "Deployment Feasibility" and "Generalization" dimensions in Table 2 reflect the distinction between controlled and real-world performance, drawing directly on this work's findings.

---

### [9] Liu et al. (2025)

**Citation:**  
Liu, B., Zhu, T., & Ding, M. (2025). A review of deepfake and its detection: From generative adversarial networks to diffusion models. *International Journal of Intelligent Systems*.

**Dimensions:** T  
**Paper sections:** §2.1, §6.1, §6.5, Table 2

**Annotation:**  
Reviews the transition from GAN-based to diffusion model-based generation and its implications for detection. Demonstrates quantitatively that diffusion models produce fewer detectable visual artifacts — both spatial and spectral — than GAN-based models, posing fundamental challenges for pixel-level and many frequency-level detection approaches. Provides one of the most comprehensive analyses of the diffusion-detection gap in the reviewed literature.

**Key finding for this paper:** The shift to diffusion-based generation is not merely an incremental capability improvement but a qualitative change that invalidates artifact-based detection assumptions. Supports the claim in Sections 6.1 and 10.2 that detection is in a persistent adversarial deficit.

---

### [10] Martinek (2025)

**Citation:**  
Martinek, A. (2025). Detecting deepfakes and false ads through analysis of text-based transcripts. In *Proceedings of COLING 2025*.

**Dimensions:** T  
**Paper sections:** §2.3, §6.5, Table 2

**Annotation:**  
Analyzes deepfake advertisements using transcript-based linguistic analysis, demonstrating that patterns such as unusual urgency markers, inconsistent authority claims, and syntactic anomalies can serve as useful classification signals. Establishes the value of linguistic modality as a complement to visual and audio detection. Relevant to the multimodal ensemble discussion in Section 6.5.

**Key finding for this paper:** Linguistic signals provide detection value independent of visual or audio channels, supporting the argument that multimodal approaches outperform any single modality and that deepfake detection should extend beyond pixel-level analysis.

---

### [11] Patel et al. (2026)

**Citation:**  
Patel, R., et al. (2026). AI-driven conceptual framework for detecting fake news and deepfake content. *Digital Health & Media*, 4(1). https://doi.org/10.1177/pmc2026.001

**Dimensions:** G, T  
**Paper sections:** §2.4, §7.3

**Annotation:**  
Proposes an AI-driven multi-stakeholder governance model integrating detection, content provenance tracking, and platform accountability for addressing synthetic media at scale. The framework assigns distinct responsibilities to developers, platforms, regulators, researchers, and civil society. Adopted in Section 7.3 of this paper as the basis for governance recommendations, with extensions addressing implementation barriers not covered in the original framework.

**Key finding for this paper:** Effective deepfake governance cannot be achieved by any single actor; multi-stakeholder coordination with clearly assigned responsibilities is a necessary structural condition, not merely a desirable one.

---

### [12] Singh et al. (2025)

**Citation:**  
Singh, S., Srivastav, S., Singh, S., & Hussain, S. (2025). Deepfake detection systems: A comprehensive survey of algorithms and techniques. *Journal of AI Research*.

**Dimensions:** T  
**Paper sections:** §2.3, §6.5, Table 2

**Annotation:**  
Comprehensive survey of detection algorithms across modalities — video, audio, and text. The key finding relevant to this paper is that multimodal approaches consistently outperform single-modality systems by combining complementary signal types, but that the computational cost of multimodal systems limits real-time deployment feasibility. This tension between performance and deployability is a central theme in Section 6 and directly informs the Deployment Feasibility ratings in Table 2.

**Key finding for this paper:** The accuracy-deployability tradeoff is the central practical constraint on detection: the best-performing systems (multimodal ensembles) are the least deployable, and the most deployable systems (single-modality, low-cost) have the weakest performance. This finding motivates the governance recommendation that platforms invest in detection infrastructure rather than relying solely on available commercial tools.

---

### [13] Soundarya & Gururaj (2026)

**Citation:**  
Soundarya, B. C., & Gururaj, H. L. (2026). Deepfake detection: Critical review of state-of-the-art approaches and future perspectives. *Discover Applied Sciences*.

**Dimensions:** T  
**Paper sections:** §2.1, §6, Table 2

**Annotation:**  
Critical review emphasizing the limitations of detection models trained on GAN-generated content when evaluated against diffusion-based synthetic media. Argues for continuously updated datasets and model retraining pipelines as structural requirements for maintaining detection effectiveness over time. This requirement is incorporated into governance recommendations in Section 7.2 regarding platform detection infrastructure obligations.

**Key finding for this paper:** Detection effectiveness is not a fixed property of a deployed model but degrades over time as generative architectures evolve; governance frameworks must mandate ongoing model maintenance, not one-time certification.

---

### [14] Soundarya et al. (2025)

**Citation:**  
Soundarya, B. C., et al. (2025). Multimedia-enabled deepfake detection: State-of-the-art tools and techniques and future directions. *Discover Computing*.

**Dimensions:** T  
**Paper sections:** §2.1, §6.5, Table 2

**Annotation:**  
Reviews state-of-the-art multimedia detection tools spanning video, audio, and image modalities. Provides a useful companion to Singh et al. (2025) with additional coverage of tool-level implementations and practical deployment considerations. Supports the multimodal detection analysis in Section 6.5.

**Key finding for this paper:** The gap between research-grade detection performance and tool-level deployment performance is substantial; claims derived from academic benchmarks should not be directly translated to operational performance expectations.

---

### [15] European Parliament (2024)

**Citation:**  
European Parliament. (2024). Regulation (EU) 2024/1689 — The Artificial Intelligence Act. *Official Journal of the European Union*.

**Dimensions:** G  
**Paper sections:** §7.1, Table 3

**Annotation:**  
The EU AI Act establishes a risk-based regulatory framework for AI systems, classifying deepfake generation as a transparency-obligation activity requiring watermarking of AI-generated content and disclosure of synthetic media to end users. It mandates that providers of general-purpose AI systems with systemic risk implement additional safeguards. This is the most comprehensive binding governance framework among those reviewed and is used as the reference point for evaluating other jurisdictions' frameworks in Table 3.

**Key finding for this paper:** The EU AI Act's risk-tiering approach represents the current best practice in deepfake governance, but its enforcement across member states and against non-EU generative AI providers remains an open implementation challenge.
