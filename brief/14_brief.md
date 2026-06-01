# Chapter 14: The Scaling Law — T1
*Condensed version — Part II*

---

## 14.1 The Residual Problem

Ch13 derived $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma)$ with $\mu(\rho) = 2/\sqrt{c(\rho)}$, but left $c(\rho)$ open except at the anchor $c(\rho_{\mathrm{GR}}) = 1$. Ch14 derives $c(\rho)$ for all $\rho$ via the **scaling law T1**: $\Gamma(\rho) \propto \rho^{-1}$.

**Result previewed:**
$$c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4, \qquad \mu(\rho) = 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^2, \qquad \kappa(\rho) = -1 \;\text{(universal)}$$

**Dimensionality note.** $\rho$ is dimensionless (organizational index); $\Gamma$ carries dimension $\rho^{-1}$ — also dimensionless in GSF natural units. The Lagrangian $\mathcal{L}$ is therefore dimensionless: it measures *relative structural cost*, not energy in Joules. Correspondence to physical units requires a global scaling constant (Hito 3, Part III). Chapters 15–18 verify structural (same functional form), not quantitative (same SI coefficients), recovery of known results.

---

## 14.2 Structural Triangulation

T1 is established by three structural roles, not three independent derivations:

| Argument | Role | Output |
|---|---|---|
| 1 — Group structure | Establishes form | $\Gamma \propto \rho^\alpha$; $\alpha$ free |
| 2 — Lagrangian covariance | **Selects** $\alpha$ | C2: $\alpha < 0$; C3 (Lemma 14.2): $\alpha = -1$ |
| 3 — EOM covariance | Confirms + extracts $\delta = 0$ | $\alpha = -1$ consistent; time absolute |

---

## 14.3 Argument 1 — Group Structure

Level changes compose: $f(\lambda_1\lambda_2) = f(\lambda_1)f(\lambda_2)$.

**Lemma 14.1.** The only continuous solution is $f(\lambda) = \lambda^\alpha$ (Cauchy on $\mathbb{R}_{>0}$).

Result: $\Gamma(\rho) = \Gamma_0\cdot\rho^\alpha$. Form established; $\alpha$ free.

---

## 14.4 Argument 2 — Lagrangian Covariance

Uniform scaling $(\rho \to \lambda\rho,\; \Gamma \to \lambda^\alpha\Gamma)$ forces $\mathrm{deg}(\mu) = -2\alpha$.

**Constraint C2 (Coordination cost).** More organizationally complex systems require more structural "glue" to maintain their coupling pattern $\Gamma$ against perturbations — not behavioral rigidity, but higher *coordination cost*. Formally: $\mu(\rho)$ must be increasing in $\rho$:
$$\frac{d\mu}{d\rho} > 0 \implies \alpha < 0$$

**Constraint C3 (Minimal representation-invariant section).** The level-invariant structural object $\mathcal{I}(\rho,\Gamma)$ must:
- *(a) G-invariance:* $\mathcal{I}(\lambda\rho, \lambda^\alpha\Gamma) = \mathcal{I}(\rho,\Gamma)$
- *(b) H-covariance:* transform in the same representation of the structural group as $\Gamma$

Condition (b) forces $\mathcal{I}$ to be *linear* in $\Gamma$ — scalars ($\det$), norms (metric-dependent), and $\mathrm{adj}$ are in different representations. The most general H-covariant linear map is $\mathcal{I} = f(\rho)\Gamma$; G-invariance forces $f(\rho) \propto \rho^{-\alpha}$.

**Lemma 14.2 (Fixed section and $\alpha = -1$).** The scaling generator $\rho\,d/d\rho$ acts on $\rho^k\Gamma$ as $(k+\alpha)\rho^k\Gamma$. A fixed section (eigenvalue 0) requires $k = -\alpha$. With C2 forcing $\alpha < 0$ (so $k > 0$), the *minimum* positive $k$ is $k=1$, giving the primitive level-invariant object $\rho\Gamma$ and forcing:
$$\boxed{\alpha = -1}$$

The case $\alpha = -2$ requires $k = 2$ — a second-order section, excluded by minimality. The case $\alpha = -1/2$ gives $k = 1/2$, outside the polynomial representation.

---

## 14.5 Argument 3 — EOM Covariance and Time-Scale Invariance

Under general $\alpha$ with $\mathrm{deg}(\mu) = -2\alpha$, all four EOM terms scale as $\lambda^\alpha$ — EOM covariance holds for *any* $\alpha$. Argument 3 cannot fix $\alpha$; it is a consistency check.

**Postulate 14.1 (Time-Scale Invariance).** Under joint rescaling $(t \to \lambda^\delta t,\; \rho \to \lambda\rho,\; \Gamma \to \lambda^\alpha\Gamma)$, EOM covariance forces $\delta = 0$: terms $\ddot\Gamma$, $\dot\Gamma$, $\Gamma$ scale as $\lambda^{\alpha-2\delta}$, $\lambda^{\alpha-\delta}$, $\lambda^\alpha$ respectively — equal only if $\delta = 0$.

**Proposition 14.1.** With $\delta = 0$, the EOM confirms $\alpha = -1$ consistent. $\alpha = -2$ excluded by C3 (minimal section, not by Ch13 alone — avoiding circularity).

---

## 14.6 Theorem 14.1 — T1

$$\boxed{T1:\quad\Gamma(\rho) = \frac{\Gamma(\rho_{\mathrm{ref}})\cdot\rho_{\mathrm{ref}}}{\rho} \qquad\Longleftrightarrow\qquad \frac{d\Gamma}{d\rho} = -\frac{\Gamma}{\rho}}$$

---

## 14.7 Consequences of T1

**Structural coherence.** The attractor condition $P(\Gamma)P(\Gamma)^T \propto \det(P(\Gamma))\cdot\mathbf{1}_4$ is homogeneous of degree 2 in $P$ — so $\Gamma \to \lambda^{-1}\Gamma$ implies $P \to \lambda^{-1}P$ and $\det(P) \to \lambda^{-4}\det(P)$. The attractor projection inherits the $\rho^{-4}$ scaling of $\det(\Gamma)$:
$$\boxed{c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4}$$

**Coupling strength:** $\mu(\rho) = 2/\sqrt{c(\rho)} \implies \mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$.

The monotone increase encodes *coordination cost*: at higher $\rho$, maintaining identity requires more structural glue. A neural network is behaviorally flexible but structurally expensive to reorganize.

**$\kappa = -1$ universal:** Frobenius shape (sector ratio) is invariant under $\Gamma \to \lambda^{-1}\Gamma$ — the kinetic grammar is universal across all $\rho$.

**Complete Lagrangian:**
$$\boxed{\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)}$$

---

## 14.8 Structural Predictions

### Matter creation threshold

Lorentzian-signature potential: $V_{\mathrm{eff}} = 4\sigma^2 - 2(\rho/\rho_{\mathrm{GR}})^2\sigma^4$. Nucleation threshold (requires $E_{\mathrm{fluct}} < 2$ explicitly):
$$\rho_{\mathrm{mat}} = \rho_{\mathrm{GR}}\sqrt{2/E_{\mathrm{fluct}}} > \rho_{\mathrm{GR}}$$

**Global instability.** The $-\sigma^4$ potential has no global minimum — once the barrier is crossed, the system rolls to $\sigma \to \infty$. Two resolutions: (a) degree-6 stabilizing term from higher-order invariants (beyond minimal Lagrangian), or (b) matter as a long-lived metastable state. Open for Part III.

### Cosmological constant

GSF classical prediction: $\Lambda_{\mathrm{eff}} = 0$ (from $c(\rho_{\mathrm{GR}}) = 1$ exactly).

**Tension:** $\Lambda_{\mathrm{obs}} > 0$ is a genuine open problem. Unit conversion cannot rescue zero: 0 × (any factor) = 0.

**Structural observation (sign).** A deviation $c(\rho_{\mathrm{GR}}) = 1 - \varepsilon < 1$ gives $\Delta\mu = \mu(\rho_{\mathrm{GR}}) - 2 > 0$, producing $\Lambda_{\mathrm{eff}} \propto \Delta\mu > 0$ — qualitatively consistent with the observed *positive* sign of $\Lambda_{\mathrm{obs}}$. Not a quantitative prediction; a structural sign-consistency result.

---

## 14.9 Epistemic Status

| Result | Status | Notes |
|---|---|---|
| Scaling form $\Gamma \propto \rho^\alpha$ | Derived | Cauchy functional equation |
| C2: $\alpha < 0$ | Derived | Coordination cost → $\mu$ increasing |
| C3: $\alpha = -1$ | Derived — Lemma 14.2 | Minimal representation-invariant fixed section |
| $\delta = 0$ (time absolute) | Derived — Postulate 14.1 | EOM covariance under joint rescaling |
| Attractor scaling inherits $\rho^{-4}$ | Derived | Homogeneity of attractor condition |
| $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ | Derived | Exact within power-law assumption |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | Derived | Parameter-free |
| $\kappa = -1$ universal | Derived | Frobenius shape invariance |
| $[\mathcal{L}] = 1$ (dimensionless) | Structural | Physical units via Hito 3 |
| "Zero free parameters" ($\mathcal{L}$) | Structural only | $\gamma$, $N(t)$ open in dissipative EOM |
| $\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$ | Conditional | Requires $E_{\mathrm{fluct}} < 2$ (open) |
| Matter state global stability | Open | $-\sigma^4$ instability; Part III |
| $\Lambda_{\mathrm{eff}} = 0$ vs $\Lambda_{\mathrm{obs}} > 0$ | Open | Sign of $\Delta\mu$ qualitatively consistent |
| Logarithmic corrections to T1 | Open | Quantum extension |
| Absolute scale of $\rho_{\mathrm{GR}}$ | Open | Hito 3 (Planck bridge) |

---

*Ch14 completes the classical GSF Lagrangian. Chapters 15–18 verify structural consistency across five domains.*
