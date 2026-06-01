# Chapter 15b: Spectral Analysis of the GSF — Propagating vs. Bound Modes

*Technical supplement to Chapter 15. Developed after Ch15 corrections.*

This supplement formalizes the dynamical distinction Chapter 15 established algebraically: how do fluctuation modes encode the transition from wave to particle regime, and what is the connection between spectral properties and the matter creation threshold?

---

## 15b.1 Motivation

Chapter 15 established two regimes separated by $\mathrm{rank}(\Gamma)$: the linear regime ($S = A = 0$, adj vanishes, propagating) and the nonlinear regime ($\det(\Gamma) > 0$, attractor exists, localized). This supplement formalizes the distinction dynamically: given a background $\Gamma_0$, what are the masses of the fluctuation modes? The answer turns out to connect the spectral structure directly to the matter creation threshold of Ch14.

**Notation.** $\mu \equiv (\rho/\rho_{\mathrm{GR}})^2$. The full EOM (without driving term, in the field-theoretic form) is:

$$\square\Gamma + \Gamma + \mu\,\mathrm{adj}(\Gamma)^T = 0$$

---

## 15b.2 Linearization Around a Background

Let $\Gamma_0$ be a static background satisfying:

$$\Gamma_0 + \mu\,\mathrm{adj}(\Gamma_0)^T = N_0 \quad\text{(background equilibrium)}$$

Write $\Gamma = \Gamma_0 + \delta\Gamma$ with $|\delta\Gamma| \ll |\Gamma_0|$. Substituting and subtracting the background equation:

$$\square(\delta\Gamma) + \delta\Gamma + \mu\,\frac{d}{d\epsilon}\bigg|_{\epsilon=0}\mathrm{adj}(\Gamma_0 + \epsilon\,\delta\Gamma)^T = 0$$

**Lemma 15b.1 (Derivative of the adjugate).** For invertible $\Gamma_0$, using $\mathrm{adj}(\Gamma) = \det(\Gamma)\Gamma^{-1}$ and the product rule:

$$\frac{d}{d\epsilon}\bigg|_{\epsilon=0}\mathrm{adj}(\Gamma_0 + \epsilon\,\delta\Gamma) = \det(\Gamma_0)\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-1} - \Gamma_0^{-1}\delta\Gamma\,\Gamma_0^{-1}\right]$$

*Proof.* Let $f(\epsilon) = \det(\Gamma_0 + \epsilon\,\delta\Gamma)(\Gamma_0 + \epsilon\,\delta\Gamma)^{-1}$. By the product rule:

$$f'(0) = \det(\Gamma_0)\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\cdot\Gamma_0^{-1} + \det(\Gamma_0)\cdot(-\Gamma_0^{-1}\delta\Gamma\,\Gamma_0^{-1})$$

Factoring out $\det(\Gamma_0)$ gives the result. $\square$

Taking the transpose:

$$\frac{d}{d\epsilon}\bigg|_{\epsilon=0}\mathrm{adj}(\Gamma_0 + \epsilon\,\delta\Gamma)^T = \det(\Gamma_0)\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-T} - \Gamma_0^{-T}\delta\Gamma^T\Gamma_0^{-T}\right]$$

**Definition 15b.1 (Effective mass operator).** The *effective mass operator* at background $\Gamma_0$ is the linear map $\mathcal{M}_{\Gamma_0}: \mathrm{Mat}(4,\mathbb{R}) \to \mathrm{Mat}(4,\mathbb{R})$ defined by:

$$\boxed{\mathcal{M}_{\Gamma_0}[\delta\Gamma] \;=\; \delta\Gamma \;+\; \mu\det(\Gamma_0)\!\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-T} \;-\; \Gamma_0^{-T}\delta\Gamma^T\Gamma_0^{-T}\right]}$$

The linearized field EOM is:

$$\boxed{\square(\delta\Gamma) + \mathcal{M}_{\Gamma_0}[\delta\Gamma] = 0}$$

---

## 15b.3 Spectral Classification

For a plane-wave mode $\delta\Gamma(t,\mathbf{x}) = \hat\delta\Gamma\,e^{i(\mathbf{k}\cdot\mathbf{x} - \omega t)}$, the EOM gives:

$$(-\omega^2 + |\mathbf{k}|^2)\hat\delta\Gamma + \mathcal{M}_{\Gamma_0}[\hat\delta\Gamma] = 0$$

If $\hat\delta\Gamma$ is an eigenvector of $\mathcal{M}_{\Gamma_0}$ with eigenvalue $\lambda$:

$$\omega^2 = |\mathbf{k}|^2 + \lambda$$

**Spectral classification:**

| Eigenvalue | Dispersion | Physical interpretation |
|---|---|---|
| $\lambda > 0$ | $\omega^2 = |\mathbf{k}|^2 + \lambda$ | Massive mode — bound, localized |
| $\lambda = 0$ | $\omega^2 = |\mathbf{k}|^2$ | Massless — propagating on light cone |
| $\lambda < 0$ | $\omega^2 < |\mathbf{k}|^2$ (for small $k$: imaginary $\omega$) | Tachyonic — instability, phase transition |

**Remark 15b.1 (Lifting required).** In the mechanical version ($\Gamma = \Gamma(t)$ only), the spatial gradient term $|\mathbf{k}|^2\hat\delta\Gamma$ is absent and propagation has no meaning. The spectral classification applies only after the canonical covariant lifting to a field $\Gamma(t,\mathbf{x})$ (§15.5). Propagation is a property of the field-theoretic level of description, not of the finite-dimensional system.

---

## 15b.4 Evaluation on the Scalar Background $\Gamma_0 = \sigma\mathbf{1}_4$

The most tractable background is the *uniform scalar* $\Gamma_0 = \sigma\mathbf{1}_4$ with $\sigma > 0$. This is the simplest element of $\mathcal{M}_{\mathrm{adm}}$ (since $\sigma\mathbf{1}_4$ has $\Gamma_s = \sigma\mathbf{1}_4 \succ 0$, $\Gamma_a = 0$).

**Background data:**
- $\det(\sigma\mathbf{1}_4) = \sigma^4$
- $(\sigma\mathbf{1}_4)^{-1} = \sigma^{-1}\mathbf{1}_4$
- $(\sigma\mathbf{1}_4)^{-T} = \sigma^{-1}\mathbf{1}_4$

The operator becomes:

$$\mathcal{M}_{\sigma\mathbf{1}}[\delta\Gamma] = \delta\Gamma + \mu\sigma^4\left[\sigma^{-1}\mathrm{Tr}(\delta\Gamma)\cdot\sigma^{-1}\mathbf{1} - \sigma^{-1}\delta\Gamma^T\sigma^{-1}\right]$$

$$= \delta\Gamma + \mu\sigma^2\left[\mathrm{Tr}(\delta\Gamma)\,\mathbf{1} - \delta\Gamma^T\right]$$

### 15b.4.1 Mode Decomposition

Every $\delta\Gamma \in \mathrm{Mat}(4,\mathbb{R})$ decomposes as:

$$\delta\Gamma = \underbrace{\frac{\mathrm{Tr}(\delta\Gamma)}{4}\mathbf{1}}_{\text{trace}} \;+\; \underbrace{\delta\Gamma_s^{(0)}}_{\text{traceless sym}} \;+\; \underbrace{\delta\Gamma_a}_{\text{antisym}}$$

where $\delta\Gamma_s^{(0)} = \delta\Gamma_s - \frac{\mathrm{Tr}(\delta\Gamma)}{4}\mathbf{1}$ is traceless symmetric and $\delta\Gamma_a = \frac{1}{2}(\delta\Gamma - \delta\Gamma^T)$ is antisymmetric.

**Dimensions:** trace (1), traceless symmetric (9), antisymmetric (6). Total: $1 + 9 + 6 = 16 = 4^2$. ✓

**Mode 1 — Trace sector.** Let $\delta\Gamma = \tau\mathbf{1}$ (so $\mathrm{Tr}(\delta\Gamma) = 4\tau$, $\delta\Gamma^T = \tau\mathbf{1}$):

$$\mathcal{M}_{\sigma\mathbf{1}}[\tau\mathbf{1}] = \tau\mathbf{1} + \mu\sigma^2[4\tau\mathbf{1} - \tau\mathbf{1}] = (1 + 3\mu\sigma^2)\tau\mathbf{1}$$

$$\boxed{\lambda_{\mathrm{tr}} = 1 + 3\mu\sigma^2 > 0 \quad \text{for all } \sigma > 0}$$

The trace mode is **always massive**. It cannot become massless or unstable. It is the "breathing mode" of the coupling structure — changing the overall scale of $\Gamma$ costs energy at every $\sigma$.

**Mode 2 — Traceless symmetric sector.** Let $\delta\Gamma = \delta\Gamma_s^{(0)}$ ($\mathrm{Tr} = 0$, $(\delta\Gamma_s^{(0)})^T = \delta\Gamma_s^{(0)}$):

$$\mathcal{M}_{\sigma\mathbf{1}}[\delta\Gamma_s^{(0)}] = \delta\Gamma_s^{(0)} + \mu\sigma^2[0 - \delta\Gamma_s^{(0)}] = (1 - \mu\sigma^2)\delta\Gamma_s^{(0)}$$

$$\boxed{\lambda_{\mathrm{sym}} = 1 - \mu\sigma^2 = 1 - \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^2\sigma^2}$$

This eigenvalue changes sign. Three regimes:
- $\sigma < \sigma^\star$: $\lambda > 0$ (massive, stable)
- $\sigma = \sigma^\star$: $\lambda = 0$ (massless — phase transition)
- $\sigma > \sigma^\star$: $\lambda < 0$ (tachyonic — instability)

where $\sigma^\star \equiv 1/\sqrt{\mu} = \rho_{\mathrm{GR}}/\rho$.

**Mode 3 — Antisymmetric sector.** Let $\delta\Gamma = \delta\Gamma_a$ ($\mathrm{Tr} = 0$, $\delta\Gamma_a^T = -\delta\Gamma_a$):

$$\mathcal{M}_{\sigma\mathbf{1}}[\delta\Gamma_a] = \delta\Gamma_a + \mu\sigma^2[0 - (-\delta\Gamma_a)] = (1 + \mu\sigma^2)\delta\Gamma_a$$

$$\boxed{\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2 > 0 \quad \text{for all } \sigma > 0}$$

The antisymmetric modes are **always massive** around the scalar background. (Note: masslessness of the photon is a property of the sector structure $\Gamma_a = dA$, independent of the scalar background — see §15.6.3.)

**Complete spectrum summary:**

| Sector | Multiplicity | $\lambda$ | Behavior |
|---|---|---|---|
| Trace | 1 | $1 + 3\mu\sigma^2$ | Always massive |
| Traceless symmetric | 9 | $1 - \mu\sigma^2$ | Sign depends on $\sigma$ vs $\sigma^\star$ |
| Antisymmetric | 6 | $1 + \mu\sigma^2$ | Always massive |

---

## 15b.5 The Critical Point and the Matter Creation Threshold

**Theorem 15b.1 (Spectral-threshold correspondence).** *The critical background value $\sigma^\star = \rho_{\mathrm{GR}}/\rho$ at which the traceless symmetric modes become massless coincides exactly with the matter creation threshold of Ch14 §14.8.1.*

*Proof.* From Ch14, the effective potential on the scalar sector is:

$$V_{\mathrm{eff}}(\sigma) = 4\sigma^2 - 2\mu\sigma^4$$

The potential barrier (local maximum) is at $dV_{\mathrm{eff}}/d\sigma = 0$:

$$8\sigma - 8\mu\sigma^3 = 0 \implies \sigma^2 = \frac{1}{\mu} \implies \sigma^\star = \frac{1}{\sqrt{\mu}} = \frac{\rho_{\mathrm{GR}}}{\rho}$$

This is the same $\sigma^\star$ at which $\lambda_{\mathrm{sym}} = 1 - \mu\sigma^{*2} = 1 - 1 = 0$. $\square$

**Corollary 15b.1.** The instability region $\lambda_{\mathrm{sym}} < 0$ (where traceless symmetric perturbations grow exponentially) corresponds exactly to $\sigma > \sigma^\star$ — the regime where the system has crossed the potential barrier and rolls toward the deep nonlinear regime ($\sigma \to \infty$ instability of the $-\sigma^4$ potential, Ch14 Remark 14.5).

**Spectral portrait at the three critical values:**

| $\sigma$ | $\lambda_{\mathrm{tr}}$ | $\lambda_{\mathrm{sym}}$ | $\lambda_{\mathrm{anti}}$ | Regime |
|---|---|---|---|---|
| $0 < \sigma \ll \sigma^\star$ | $\approx 1$ | $\approx 1$ | $\approx 1$ | Deep wave regime — all modes nearly degenerate |
| $\sigma = \sigma^\star$ | $4$ | $0$ | $2$ | **Phase transition** — 9 massless Goldstone-like modes |
| $\sigma \gg \sigma^\star$ | $\gg 1$ | $\ll 0$ | $\gg 1$ | Unstable — particle regime beyond barrier |

**Remark 15b.2 (Structure of the phase transition).** At $\sigma = \sigma^\star$, the 9 traceless symmetric modes become massless while the trace mode (1) acquires mass $\lambda_{\mathrm{tr}} = 4$ and the antisymmetric sector (6) acquires mass $\lambda_{\mathrm{anti}} = 2$. The ratio $\lambda_{\mathrm{tr}}/\lambda_{\mathrm{anti}} = 2$ at the transition point is a pure number, independent of $\rho$ and $\sigma^\star$. This pattern — one heavy mode, a set of massless modes, and an intermediate sector — is structurally analogous to the Higgs mechanism, but here it emerges from the GSF EOM without an external symmetry breaking potential. The "symmetry" being broken is the $\mathrm{SO}(4)$ rotational symmetry of $\mathcal{M}_{\mathrm{adm}}$ around $\sigma\mathbf{1}$.

---

## 15b.6 Vacuum Background: $\Gamma_0 = 0$

When $\Gamma_0 = 0$: $\det(\Gamma_0) = 0$, so the adj correction vanishes identically regardless of $\delta\Gamma$:

$$\mathcal{M}_0[\delta\Gamma] = \delta\Gamma$$

**All 16 modes have eigenvalue $\lambda = 1$.** The GSF vacuum is not empty — it has a universal mass gap $m^2 = 1$ (in GSF units, set by the $-\|\Gamma\|_F^2$ potential term). No mode propagates on the light cone from the trivial vacuum. Massless propagation requires a nontrivial background.

**Remark 15b.3 (Mass gap of the vacuum).** The universal mass $m^2 = 1$ at $\Gamma_0 = 0$ is not a free parameter — it is fixed by the ratio of the kinetic and potential coefficients in the Lagrangian, both equal to 1 in GSF units. In physical units (via Hito 3), this mass sets the intrinsic structural scale. The massless photon and graviton do not emerge from the trivial vacuum; they emerge from the structure of the respective sectors ($\Gamma_a = dA$ for the photon; the $\mu = 2$ cancellation for the graviton).

---

## 15b.7 Attractor Background: $\Gamma_0 = P(\Gamma)$

The structural attractor $P(\Gamma)$ satisfies $P(\Gamma)P(\Gamma)^T = \det(P(\Gamma))\cdot\mathbf{1}_4$ (Ch13 §13.5). This means $P/\sqrt{\det(P)} \in O(4)$ — the attractor is proportional to an orthogonal matrix.

Write $P = \sqrt{d_P}\,Q$ with $Q \in O(4)$, $d_P = \det(P)$. Then:
- $\det(P) = d_P$
- $P^{-1} = (1/\sqrt{d_P})Q^{-1} = (1/\sqrt{d_P})Q^T$ (since $Q \in O(4)$)
- $P^{-T} = (1/\sqrt{d_P})Q$

The operator at the attractor background:

$$\mathcal{M}_P[\delta\Gamma] = \delta\Gamma + \mu d_P\left[\mathrm{Tr}\!\left(\tfrac{1}{\sqrt{d_P}}Q^T\delta\Gamma\right)\tfrac{1}{\sqrt{d_P}}Q - \tfrac{1}{\sqrt{d_P}}Q\,\delta\Gamma^T\tfrac{1}{\sqrt{d_P}}Q\right]$$

$$= \delta\Gamma + \mu\left[\mathrm{Tr}(Q^T\delta\Gamma)\,Q - Q\,\delta\Gamma^T Q\right]$$

Define the $Q$-rotated perturbation $\widetilde{\delta\Gamma} = Q^T\delta\Gamma$. Then:

$$Q^T\mathcal{M}_P[\delta\Gamma] = \widetilde{\delta\Gamma} + \mu\left[\mathrm{Tr}(\widetilde{\delta\Gamma})\,\mathbf{1} - \widetilde{\delta\Gamma}^T\right]$$

This is exactly the $\sigma = 1/\sqrt{\mu}$ case of the scalar background operator! The attractor background $P(\Gamma)$ is spectrally equivalent (via an $O(4)$ rotation) to the scalar background at $\sigma = \sigma^\star$.

**Proposition 15b.1 (Attractor spectrum).** *The effective mass operator at the structural attractor $P(\Gamma)$ has the same eigenvalue spectrum as $\mathcal{M}_{\sigma^\star\mathbf{1}}$:*

| Sector | Multiplicity | $\lambda$ |
|---|---|---|
| $Q$-trace | 1 | $4$ |
| $Q$-traceless symmetric | 9 | $0$ |
| $Q$-antisymmetric | 6 | $2$ |

*The 9 traceless symmetric modes are massless at the attractor. The attractor is precisely the phase transition point.*

**Proof.** The spectral equivalence follows from the $O(4)$ rotation $Q$ relating $\mathcal{M}_P$ to $\mathcal{M}_{\sigma^\star\mathbf{1}}$. Eigenvalues are $O(4)$-invariant. $\square$

---

## 15b.8 Synthesis: Three Backgrounds, One Story

| Background | $\det(\Gamma_0)$ | Spectrum | Regime |
|---|---|---|---|
| $\Gamma_0 = 0$ | $0$ | All $\lambda = 1$ (degenerate massive) | Trivial vacuum, no propagation |
| $\Gamma_0 = \sigma\mathbf{1}$, $\sigma < \sigma^\star$ | $\sigma^4$ | $\lambda_{\mathrm{sym}} > 0$, all massive | Stable wave regime |
| $\Gamma_0 = \sigma^\star\mathbf{1} = P(\Gamma)$ | $\sigma^{*4}$ | 9 massless, others massive | **Phase transition = matter creation threshold** |
| $\Gamma_0 = \sigma\mathbf{1}$, $\sigma > \sigma^\star$ | $\sigma^4$ | $\lambda_{\mathrm{sym}} < 0$, unstable | Tachyonic — beyond barrier |

**The physical picture.** The GSF has no massless modes in the trivial vacuum. Massless propagation emerges only when the background is nontrivial — either from the sector structure ($\Gamma_a = dA$ for photons) or at the critical background $\sigma = \sigma^\star$ where the traceless symmetric sector goes massless. The matter creation threshold of Ch14 is not an accident of the potential shape: it is the spectral phase transition of the effective mass operator.

---

## 15b.9 Epistemic Status

| Result | Status | Notes |
|---|---|---|
| Linearized EOM and $\mathcal{M}_{\Gamma_0}$ | Derived (Lemma 15b.1) | Requires $\Gamma_0$ invertible |
| Mode decomposition for $\sigma\mathbf{1}$ background | Derived | Exact; 16 modes in three sectors |
| $\lambda_{\mathrm{tr}} = 1 + 3\mu\sigma^2$ | Derived | Always positive |
| $\lambda_{\mathrm{sym}} = 1 - \mu\sigma^2$ | Derived | Changes sign at $\sigma^\star$ |
| $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2$ | Derived | Always positive |
| Spectral-threshold correspondence (Theorem 15b.1) | Proved | $\sigma^\star$ in spectrum = $\sigma^\star$ in Ch14 |
| Attractor spectrum = phase transition spectrum (Prop 15b.1) | Proved | $O(4)$ rotation equivalence |
| Vacuum mass gap $m^2 = 1$ | Derived | Fixed by Lagrangian coefficients |
| General $\Gamma_0$ (non-scalar, non-attractor) | Open | Requires full diagonalization of $\mathcal{M}_{\Gamma_0}$ |
| Lorentzian signature backgrounds ($\det < 0$) | Open | GR sector; sign of $\mu\det(\Gamma_0)$ changes |
| Quantum corrections to $\lambda_{\mathrm{sym}}$ | Open | May shift critical $\sigma^\star$ |

---

*The spectral analysis transforms the wave-particle dichotomy of §15.8 (Remark 15.8) from a qualitative structural observation into a quantitative result: the transition between regimes is a phase transition of the effective mass operator, and the transition point is the matter creation threshold derived independently in Ch14.*
