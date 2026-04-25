# Table 4 — Accuracy Estimate Source Basis
## Project Phantom · /detection-analysis · https://github.com/DSUcyberops/csc727

All values in Table 4 are prefixed with ~ to signal their approximate status. This file records the source basis for every estimate and explains why approximation is unavoidable.

---

## Why Approximation Is Unavoidable

There is no single unified benchmark evaluating all seven methods under identical conditions. Different papers use different datasets (FaceForensics++, DFDC, Celeb-DF, WildDeepfake, custom), different train/test splits, different generation architectures in the test set, and different evaluation protocols. Direct numerical comparison across papers is not methodologically valid.

**Derivation method for each value:**
1. Identify the range of accuracy figures reported across relevant sources for each method and condition
2. Select a representative point that reflects challenging conditions (out-of-distribution for generalization; in-distribution for benchmark accuracy)
3. Apply conservative estimates where reported figures vary widely

The **ordering** of methods (which is better than which) is robust across sources. The **specific numbers** are illustrative starting points, not citable empirical results.

---

## Per-Method Source Basis

| Method | Benchmark (~%) | Primary source(s) | Generalization (~%) | Primary source(s) |
|---|---|---|---|---|
| Visual Artifact | 92% | FaceForensics++ GAN results across multiple papers; Guarnera et al. (2023) report >90% | 38% | Guarnera et al. (2023) near-chance on diffusion; conservative midpoint |
| Biological Signal | 78% | Khan et al. (2025) moderate accuracy range; Singh et al. (2025) concur | 62% | More architecture-agnostic; moderate cross-architecture transfer from Khan et al. (2025) |
| Audio Spectral | 84% | Singh et al. (2025); Martinek (2025) on benchmark audio | 58% | Degradation on newer voice cloning architectures noted by Singh et al. (2025) |
| Metadata Analysis | 71% | Lin et al. (2025) in intact-metadata conditions | 32% | Near-floor in adversarial (stripped metadata) conditions per Lin et al. (2025) |
| ML Classifiers | 91% | Khan et al. (2025) on matching-distribution benchmarks | 66% | Soundarya & Gururaj (2026) document out-of-distribution degradation |
| Multimodal Ensemble | 96% | Singh et al. (2025); Soundarya et al. (2025) consistently highest | 74% | Moderate-high due to complementary modality coverage per Singh et al. (2025) |
| Freq-Domain Masking | 88% | Doloriel et al. (2025) across multiple architectures | 81% ★ | Doloriel et al. (2025) — highest cross-architecture result in corpus |

---

## Caveats

1. **Benchmark ≠ real-world:** Lin et al. (2025) and Gong & Li (2024) both demonstrate that benchmark accuracy systematically overstates real-world performance. All figures are upper bounds.
2. **Conservative generalization estimates:** Where reported figures vary widely, the lower end was selected.
3. **Temporal validity:** Early 2026 state of literature. The generation landscape is evolving rapidly.
4. **Primary sources:** Readers seeking precise figures should consult the sources cited above. These values are for relative comparison only.
