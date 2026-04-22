# Table 4 — Accuracy Estimate Source Basis
## Project Phantom — /detection-analysis

Table 4 in the paper presents approximate benchmark accuracy and cross-architecture generalization scores for each detection method. This document records the basis for each estimate.

---

## Important Disclaimer

All values in Table 4 are **approximations** derived from ranges reported across the reviewed literature. They are **not** from a single unified benchmark experiment. They are intended to illustrate relative performance differences across methods. A tilde (~) precedes all values in the table to signal this status.

---

## Estimate Basis by Method

| Method | Accuracy Basis | Generalization Basis |
|---|---|---|
| Visual Artifact Detection | ~92% | Multiple GAN-era benchmarks (FaceForensics++, DFDC) consistently report >90% accuracy; Guarnera et al. (2023) and Gong & Li (2024) are primary sources. | ~38% | Guarnera et al. (2023) report near-chance performance on diffusion content; Liu et al. (2025) confirm. Estimate is conservative midpoint. |
| Biological Signal Analysis | ~78% | Khan et al. (2025) report moderate accuracy range; Singh et al. (2025) concur. | ~62% | More architecture-agnostic than artifact methods; estimate reflects moderate cross-architecture transfer reported in Khan et al. (2025). |
| Audio Spectral Analysis | ~84% | Singh et al. (2025) and Martinek (2025) report moderate-high accuracy on benchmark audio. | ~58% | Estimate reflects degradation on newer voice cloning architectures noted by Singh et al. (2025). |
| Metadata Analysis | ~71% | Lin et al. (2025) evaluate metadata-based detection in controlled settings. | ~32% | Very low generalization when metadata is stripped; estimate reflects near-floor performance in adversarial conditions per Lin et al. (2025). |
| ML-based Classifiers | ~91% | Khan et al. (2025) report high accuracy for neural classifiers on matching-distribution benchmarks. | ~66% | Soundarya & Gururaj (2026) document performance degradation on out-of-distribution content; estimate reflects moderate cross-architecture transfer. |
| Multimodal Ensemble | ~96% | Singh et al. (2025) and Soundarya et al. (2025) consistently report highest performance for multimodal systems. | ~74% | Moderate-high generalization due to complementary modality coverage per Singh et al. (2025). |
| Freq-Domain Masking | ~88% | Doloriel et al. (2025) report high accuracy across multiple architectures. | ~81% (★ Best) | Doloriel et al. (2025) demonstrate highest cross-architecture generalization of any reviewed single method. |

---

## Why These Values Are Approximate

1. **No unified benchmark:** Different papers evaluate on different datasets (FaceForensics++, DFDC, Celeb-DF, custom) with different splits. Direct comparison across papers is not methodologically exact.

2. **Training distribution mismatch:** Reported accuracy depends heavily on whether test content matches training distribution. Where papers report multiple conditions, the approximation reflects the more challenging out-of-distribution condition for generalization and the favorable in-distribution condition for benchmark accuracy.

3. **Evolving baselines:** The benchmark landscape is shifting as diffusion-generated content becomes more common. Values reflect early-2026 literature state.

For exact figures, readers should consult the primary sources listed in the table above.
