# Chapter 13: The Structural Lagrangian
*Condensed version — Part II*

---

## 13.1 The Program

Ch10 presented a "minimal canonical" Lagrangian — explicitly qualified as a starting point, not a derivation. This chapter derives the Lagrangian in four stages:

1. **§13.2–13.3** — Identify the admissible polynomial invariant basis under S1–S2 and minimality constraints.
2. **§13.4** — Select the kinetic term via the isotropy condition → forces $\kappa = -1$.
3. **§13.5** — Determine $\mu(\rho)$ from the structural equilibrium condition (self-consistency).
4. **§13.6** — Verify ghost-freedom (classical, Euclidean signature).

Output: $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma)$ with zero free parameters given the gravitational boundary condition $c(\rho_{\mathrm{GR}}) = 1$.

---

## 13.2 Symmetries and Invariant Basis

### Symmetry hierarchy

Three distinct levels — kept separate throughout:

| Level | Group | Role |
|---|---|---|
| Physical | S1–S2 | Actual symmetries of the GSF Lagrangian |
| Classification | Full conjugation | Tool for enumerating polynomial invariants (Cayley-Hamilton operates here) |
| Isotropy | $\mathrm{O}(4)\times\mathrm{O}(4)$ | Sufficiency argument for Frobenius selection |

The Lagrangian is invariant under S1–S2 only. Larger groups appear as analytical instruments.

### Physical symmetries

**S1 (Orthogonal conjugation on $\{A,\mathbf{I},\mathbf{R}\}$).** $\Gamma \mapsto O\Gamma O^T$, $O \in \mathrm{SO}(3) \subset \mathrm{O}(4)$. Preserves $\mathrm{tr}(\Gamma^k)$ and $\det(\Gamma)$.

**S2 (Parity: $\Gamma \mapsto -\Gamma$).** Eliminates odd-degree invariants ($\mathrm{tr}(\Gamma)$, $\mathrm{tr}(\Gamma^3)$). *Domain-conditional:* valid for source-free physical systems; not universal for biological/economic UoCs, which have intrinsic asymmetry. The minimal universal Lagrangian assumes S2.

### Invariant basis

**Lemma 13.1 (Quadratic invariants).** Under S1, using $\mathrm{tr}(\Gamma_s\Gamma_a) = 0$ identically (linear algebra, no physical symmetry required):
$$I_1 = \|\Gamma_s\|_F^2 - \|\Gamma_a\|_F^2 = \mathrm{tr}(\Gamma^T\Gamma), \qquad I_2 = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2 = \mathrm{tr}(\Gamma^2)$$

**Lemma 13.2 (Quartic invariant).** Cayley-Hamilton for $4\times4$ matrices: $\mathrm{tr}(\Gamma^4)$ is dependent on $\{\mathrm{tr}(\Gamma), \mathrm{tr}(\Gamma^2), \mathrm{tr}(\Gamma^3), \det(\Gamma)\}$. Parity S2 eliminates $\mathrm{tr}(\Gamma)$ and $\mathrm{tr}(\Gamma^3)$. Surviving parity-even basis at degree $\leq 4$:
$$\{I_1,\; I_2,\; \det(\Gamma)\}$$

**Remark 13.1 (Completeness under constraints).** This basis is complete under: (a) the enlarged conjugation group used for classification, (b) sector-decoupling (no $\mathrm{tr}(\Gamma_s^2\Gamma_a^2)$ or similar mixed terms), and (c) minimality (degree $\leq 4$). Items (b) and (c) are structural postulates, not consequences of S1–S2 alone. Uniqueness is *within the minimal decoupled class*.

---

## 13.3 The General Admissible Lagrangian

Under normalization $\alpha_1 + \alpha_2 = 1$ with $\kappa := -\alpha_1 + \alpha_2$:
$$\mathcal{L} = \|\dot\Gamma\|_F^2 + \kappa\,\mathrm{tr}(\dot\Gamma_a^2) - \|\Gamma\|_F^2 - \kappa\,\mathrm{tr}(\Gamma_a^2) - \mu\,\det(\Gamma)$$

Three a priori free parameters: $\alpha_1, \alpha_2, \mu$ (or equivalently: the overall scale, $\kappa$, $\mu$). Two conditions fix $\kappa$; one self-consistency condition fixes $\mu$.

*Notation:* $\kappa$ here is the antisymmetric sector weight (ultimately $= -1$). Distinct from Einstein's $\kappa_{\mathrm{GR}} = 8\pi G/c^4$.

---

## 13.4 Frobenius Fixes $\kappa = -1$

**Theorem 13.1 (Frobenius as minimal isotropic kinetic term).** Under S1–S2 alone, the kinetic term admits a two-parameter family $a\|\dot\Gamma_s\|_F^2 + b\|\dot\Gamma_a\|_F^2$. The **isotropy postulate** ($a = b$, no preferred sector weight) selects $a = b = 1$, i.e., the Frobenius metric:
$$T = \mathrm{tr}(\dot\Gamma^T\dot\Gamma) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$

This forces $\alpha_1 = 1$, $\alpha_2 = 0$, $\kappa = -1$.

Key algebraic fact: for antisymmetric $\Gamma_a$, eigenvalues are purely imaginary pairs $\pm i\lambda_k$, so $\mathrm{tr}(\Gamma_a^2) = -2\sum_k\lambda_k^2 \leq 0$, giving $\mathrm{tr}(\dot\Gamma_a^T\dot\Gamma_a) = -\mathrm{tr}(\dot\Gamma_a^2) = \|\dot\Gamma_a\|_F^2 \geq 0$.

**EM note.** Frobenius gives $\|\Gamma_a\|_F^2 = \mathbf{E}^2 + \mathbf{B}^2$ (Euclidean). Standard EM requires $\mathbf{E}^2 - \mathbf{B}^2$ (Lorentzian). The GSF Lagrangian is a *consistency constraint* with EM structure, not yet a derivation. Lorentzian signature deferred to Part III.

---

## 13.5 Attractor Condition Self-Consistently Fixes $\mu$

### 13.5.1 Structural Equilibrium

$P(\Gamma)$ is the structural **equilibrium** — minimum of the purpose function. In the conservative system it is a center (Liouville: no attractors in volume-preserving dynamics); it becomes an attractor in the dissipative regime ($\gamma > 0$). The critical-point condition:

$$\frac{\partial\mathcal{L}}{\partial\Gamma}\bigg|_{P(\Gamma)} = 0 \implies -2P - \mu\det(P)\cdot P^{-T} = 0$$

Multiplying right by $P^T$:
$$\boxed{P(\Gamma)P(\Gamma)^T = -\frac{\mu}{2}\det(P(\Gamma))\cdot\mathbf{1}_4}$$

**Proposition 13.1.** The equilibrium satisfies $P(\Gamma)P(\Gamma)^T \propto \mathbf{1}_4$ — all singular values equal. This is a **consequence** of the extremum condition, not a postulate. It implies the UoC couples equally to all output directions at structural equilibrium.

### 13.5.2 Self-Consistency Derivation of $\mu$

Write $P(\Gamma)P(\Gamma)^T = \lambda\mathbf{1}_4$ with $\lambda = -\tfrac{\mu}{2}\det(P)$.

**Step 1 (LHS):** $\det(PP^T) = \det(P)^2$

**Step 2 (RHS):** $\det(\lambda\mathbf{1}_4) = \lambda^4 = \left(\frac{\mu}{2}\right)^4\!\det(P)^4$

**Step 3 (Equate, divide by $\det(P)^4 > 0$):** $\det(P)^{-2} = \left(\frac{\mu}{2}\right)^4$, so $\det(P) = \frac{4}{\mu^2}$.

**Step 4:** Define $c(\rho) := \det(P(\Gamma|\rho))$:
$$c(\rho) = \frac{4}{\mu(\rho)^2} \implies \boxed{\mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

**Theorem 13.2 (Self-consistency determination of $\mu$).** This is a **fixed-point condition**: $P(\Gamma)$ depends on the dynamics (which contains $\mu$), and $\mu$ is extracted from $\det(P(\Gamma))$. The derivation closes the circle self-consistently within the stated Lagrangian structure. It is not an independent derivation of $\mu$ from first principles.

**Remark 13.5 (Gravitational boundary condition).** $\mu(\rho)$ requires one calibration anchor. GR provides it: massless graviton propagation forces $\mu(\rho_{\mathrm{GR}}) = 2$, hence $c(\rho_{\mathrm{GR}}) = 1$. This is a **gravitational boundary condition** — the GSF scale is calibrated against physical reality at one reference level. It is not a free parameter adjustment (the massless spin-2 constraint is structural, not tunable), but it IS a calibration: without it, $c(\rho)$ is determined only up to an overall scale.

---

## 13.6 Ghost-Freedom (Classical, Euclidean Signature)

**Theorem 13.3 (Classical ghost-freedom — Euclidean signature).** For all $\dot\Gamma \in T_\Gamma\mathcal{M}_{\mathrm{adm}}$:
$$T(\dot\Gamma) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$

**Proposition 13.2 (Double-negative mechanism).** The apparent ghost from $\kappa = -1$:
- Kinetic: $(-1)\cdot\mathrm{tr}(\dot\Gamma_a^2) = +\|\dot\Gamma_a\|_F^2 > 0$ ✓
- Potential: $-(-1)\cdot\mathrm{tr}(\Gamma_a^2) = -\|\Gamma_a\|_F^2 < 0$ (potential well, not hill) ✓

Two negatives cancel. No ghost.

**Scope.** Ghost-freedom holds strictly in Euclidean signature ($\mathcal{M}_{\mathrm{adm}}$, Frobenius metric). A Lorentzian extension (Part III) introduces $ds^2 < 0$ for timelike modes and requires its own ghost-freedom proof. Classical result is necessary but not sufficient for quantum ghost-freedom (Dirac constraint analysis deferred).

---

## 13.7 Main Result

$$\boxed{\mathcal{L}(\Gamma,\dot\Gamma,\rho) = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma), \qquad \mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

**Theorem 13.4.** Unique *within* the class defined by: parity S2 + G(3)-invariance + isotropy + sector-decoupling + minimality (degree $\leq 4$) + attractor self-consistency + ghost-freedom. Each constraint is independently motivated; their conjunction leaves no free parameter given $c(\rho_{\mathrm{GR}}) = 1$.

---

## 13.8 Equations of Motion

**Conservative ($\gamma = 0$, $N = 0$):**
$$\ddot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\,\mathrm{adj}(\Gamma)^T = 0$$

(Written as $\frac{\mu}{2}\det(\Gamma)\Gamma^{-T}$ for $\det > 0$, but the adjugate form is smooth everywhere.)

**Dissipative (physical regime):**
$$\boxed{\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\,\mathrm{adj}(\Gamma)^T = N(t)}$$

| Term | Structural reading |
|---|---|
| $\ddot\Gamma$ | Inertia of structural change |
| $\gamma\dot\Gamma$ | Structural damping ($\gamma$ = organizational rigidity) |
| $\Gamma$ | Linear restoring force toward $\Gamma = 0$ |
| $\frac{\mu}{2}\mathrm{adj}(\Gamma)^T$ | Purpose force toward equilibrium $P(\Gamma)$; the force that makes the system a UoC |

**Remark 13.8 (No singularity at boundary).** $\det(\Gamma)\cdot\Gamma^{-T} = \mathrm{adj}(\Gamma)^T$ by the cofactor identity. The adjugate is a polynomial in $\Gamma$ — smooth everywhere, including $\det(\Gamma) = 0$. The apparent singularity is a representation artifact.

**Hamiltonian (conservative):** $H = T + \|\Gamma\|_F^2 + \mu\det(\Gamma)$ — positive definite on $\mathcal{M}_{\mathrm{adm}}$.

---

## 13.10 Epistemic Status

| Claim | Status | Conditions |
|---|---|---|
| Invariant basis $\{I_1, I_2, \det\}$ | Derived | Under S1–S2 + sector-decoupling + minimality |
| $\kappa = -1$ | Derived under postulate | Requires isotropy $a=b$; under S1–S2 alone, 2-param family exists |
| $\mu = 2/\sqrt{c(\rho)}$ | Self-consistency condition | Fixed-point; not independent derivation |
| Ghost-freedom (classical) | Proved | Euclidean signature only; Lorentzian case open |
| Ghost-freedom (quantum) | Open | Dirac constraint analysis deferred |
| $c(\rho_{\mathrm{GR}}) = 1$ | Gravitational boundary condition | Calibration against GR, not pure geometry |
| $c(\rho)$ for all $\rho$ | Ch14 | Requires scaling law T1 |
| EM correspondence | Consistency constraint | Euclidean vs Lorentzian signature gap; Hito 3 |
| GR correspondence | Partial | Massless graviton confirmed; full GR requires Hito 3 |
| Higher-order corrections | Open | Quantum extension |

---

*Ch10 declared the Lagrangian. Ch13 derives why it must have this form — conditional on stated postulates. Ch14 determines $c(\rho)$ for all organizational levels.*
