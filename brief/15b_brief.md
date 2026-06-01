# Chapter 15b: Spectral Analysis of the GSF
*Condensed version — Part II*

---

## 15b.1 Propagating vs. Bound Modes

The spectral structure of linearized dynamics reveals a fundamental distinction:

| Regime | Condition | Spectral eigenvalue | Physical meaning |
|---|---|---|---|
| Propagating (wave) | $S = A = 0$, $\mathrm{rank}(\Gamma) \leq 2$ | $\lambda = 0$ | No restoring force; system propagates without attractor |
| Bound (particle) | $S \neq 0$ or $A \neq 0$, $\det(\Gamma) > 0$ | $\lambda > 0$ or $\lambda < 0$ | Restoring force or instability; attractor exists |

**Effective mass operator.** Linearizing the EOM around a static background $\Gamma_0 = \sigma I$ (homogeneous, isotropic) produces:

$$\mathcal{M}_{\Gamma_0}[\delta\Gamma] = \delta\Gamma + \mu\det(\Gamma_0)\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-T} - \Gamma_0^{-T}\delta\Gamma^T\Gamma_0^{-T}\right]$$

For the scalar background $\Gamma_0 = \sigma I$, three mode sectors separate:

| Sector | Mode | Eigenvalue $\lambda$ |
|---|---|---|
| Trace | Uniform scaling | $\lambda_{\mathrm{tr}} = 1 + 3\mu\sigma^2$ |
| Symmetric traceless | Shape deformation | $\lambda_{\mathrm{sym}} = 1 - \mu\sigma^2$ |
| Antisymmetric | Gauge field | $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2$ |

---

## 15b.2 The Critical Point: Spectral Threshold = Matter Creation Threshold

The symmetric sector eigenvalue $\lambda_{\mathrm{sym}} = 0$ at:

$$\sigma^* = \sqrt{1/\mu} = \rho_{\mathrm{GR}}/\rho$$

**Theorem 15b.1.** This critical point coincides exactly with the matter creation threshold $\sigma^*$ from Ch14 §14.8.1. Same equation derived from two independent perspectives (spectral vs. thermodynamic).

**Consequence:** The attractor $P(\Gamma) \sim \sigma^* I$ is equivalent to the phase transition where the symmetric traceless mode transitions from stable to tachyonic (massless to imaginary mass).

| Regime | $\sigma < \sigma^*$ | $\sigma = \sigma^*$ | $\sigma > \sigma^*$ |
|---|---|---|---|
| **Trace** | $\lambda_{\mathrm{tr}} > 1$ (stable) | $\lambda_{\mathrm{tr}} = 4$ | $> 4$ (decoupled) |
| **Symmetric** | $\lambda_{\mathrm{sym}} > 0$ (stable) | $\lambda_{\mathrm{sym}} = 0$ (critical) | $< 0$ (tachyonic) |
| **Antisymmetric** | $\lambda_{\mathrm{anti}} > 1$ | $\lambda_{\mathrm{anti}} = 2$ | $> 2$ (always stable) |
| **Physics** | No matter, all modes propagate | Threshold; mode becomes massless | Matter condensed; instability |

---

## 15b.3 Mass Protection in the Antisymmetric Sector

The antisymmetric eigenvalue $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2 > 0$ for all $\sigma > 0$.

**Consequence:** No mode in the antisymmetric sector becomes tachyonic. This is the structural origin of photon masslessness: the curvature sector $\Gamma_a = dA$ maintains its kinetic term and never develops a mass term, independent of the background configuration.

---

## 15b.4 Connection to Part III

The spectral structure is the gateway to three open problems:

1. **Lorentzian signature** ($\det < 0$): The sign of $\mu\det(\Gamma_0)$ reverses. How does the critical point move? Does the hierarchy of thresholds change?

2. **Beyond homogeneous backgrounds:** The $\Gamma_0 = \sigma I$ calculation is structurally complete but covers only isotropic backgrounds. Generalization to anisotropic backgrounds and cosmological evolution requires Part III.

3. **Topological structure of the spectrum:** The moduli space of homogeneous solutions and their bifurcations is determined by the topology of $\mathcal{M}(\Gamma) = \mathrm{SO}(4)$. This is the connection to Chapter 20's topological analysis.

---

## Epistemic Status

| Claim | Status |
|---|---|
| Effective mass operator $\mathcal{M}_{\Gamma_0}$ | Derived (Lemma 15b.1) |
| Three-sector spectral decomposition | Exact for $\Gamma_0 = \sigma I$ |
| Theorem 15b.1 (critical point coincidence) | Proved; validated by Ch14 |
| Antisymmetric sector mass protection | Structural; consequence of adjugate rank |
| Full spectral evolution (general $\Gamma_0$) | Open; requires Part III |

The pattern: Same GSF Lagrangian analyzed from spectral perspective reveals that the matter creation threshold is not a phenomenological input but a structural bifurcation of the fluctuation spectrum.
