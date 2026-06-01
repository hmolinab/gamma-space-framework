# Chapter 10: The Structural Lagrangian
*Condensed version — source: Ch10 of the full GSF*

---

## 10.1 The Program

Ch9 gave the evolution law $f(\xi,\rho)$ and purpose function $P$ as postulates. Ch10 addresses the variational origins of these objects in two structurally distinct parts:

- **Dissipative sector** (§10.3): $\dot\xi = -M\nabla P$, $M = \Gamma_s^{-1}/\gamma$ — *derived* from the structural Lagrangian + Rayleigh dissipation in the overdamped limit.
- **Reactive sector** (§10.3.2): $-A\nabla P$ — *not* produced by the Lagrangian; introduced as the **minimal Onsager-Casimir postulate** for rotational dynamics.

"Closes the dissipative variational structure" does not mean formal completeness: (1) $P(\Gamma)$ explicit form remains open; (2) admissible Lagrangian class not fully classified; (3) antisymmetric sector postulated.

**Tensions closed:** T3 (structure of $f$, partial), T6 (Lyapunov selection), T7 (derivation chain).

**Epistemic status summary:** dissipative sector and Lyapunov selection are derived (overdamped limit); reactive sector is postulated; coefficients $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$, $\gamma(\rho)$ pending explicit $P(\Gamma)$.

---

## 10.2 The Structural Action

### 10.2.1 Minimal Requirements

Three requirements on $\mathcal{L}(\xi, \dot\xi)$:

1. **G(3)-invariance** — scalar under the UoC symmetry group.
2. **Canonical kinetic term** — quadratic in $\dot\xi$ (lowest-order, well-posed Cauchy problem).
3. **Coupling-metric consistency** — kinetic metric $K_{ij}$ induced by $\Gamma_s$ of Ch5.

### 10.2.2 The Structural Lagrangian

$$\boxed{\mathcal{L}(\xi, \dot{\xi}) = \frac{1}{2}\,\dot{\xi}^T \Gamma_s(\xi)\,\dot{\xi} - P\!\left(\Gamma[\xi]\right)}$$

- $\Gamma_s(\xi)$: kinetic metric (symmetric part of Ch5 configuration matrix)
- $P(\Gamma[\xi])$: structural potential (purpose function, Ch9 §9.5)
- Action: $\mathcal{A}[\xi] = \int \mathcal{L}\,dt$ (notation $\mathcal{A}$ to avoid collision with $S$ = Singularity)

This is the **minimal canonical choice at lowest order** — additional G(3)-invariant cross-sector terms and Born-Infeld higher-order kinetic terms exist but are excluded. The admissible class of Lagrangians is not fully classified.

---

## 10.3 Euler-Lagrange Equations and the Overdamped Limit

### 10.3.1 The Full Euler-Lagrange Equations

**Postulate 10.1 (Γ_s as Riemannian Metric).** $\Gamma_s(\xi)$ is promoted to a positive-definite Riemannian metric on the state manifold. Of the three requirements:
1. **Transformation law**: $\Gamma_s \mapsto J^T\Gamma_s J$ under $G(3)$ — **derived in Ch8 §8.8**, not an assumption.
2. **Smoothness**: $\Gamma \in C^\infty(\mathcal{V})$ — **derived in Ch8 §8.5** (Gram map is polynomial), not an assumption.
3. **Connection choice** *(genuine postulate)*: Levi-Civita (torsion-free, metric-compatible) — minimal choice.

The Euler-Lagrange equations give the **structural geodesic equation with forcing**:

$$\nabla_{\dot\xi}\dot\xi = -\operatorname{grad}_{\Gamma_s} P$$

In coordinates: $\ddot\xi^i + \Gamma^i_{jk}\dot\xi^j\dot\xi^k = -(\Gamma_s^{-1})^{ij}\partial_j P$, where $\Gamma^i_{jk}$ are the Christoffel symbols of $\Gamma_s$ (distinct from the configuration matrix $\Gamma$ — see notation note in §10.5.2).

### 10.3.2 The Overdamped Limit

Rayleigh dissipation function: $\mathcal{R} = \frac{\gamma}{2}\dot\xi^T\Gamma_s\dot\xi$, adding dissipative force $-\gamma\Gamma_s\dot\xi$.

**Scaling argument:** Christoffel terms scale as $O(1/\gamma^2)$, dissipation as $O(1/\gamma)$ — ratio $O(1/\gamma)\to 0$ as $\gamma\to\infty$. So in the overdamped limit:

$$\boxed{\dot{\xi} = -M(\rho, \xi)\,\nabla_\xi P, \qquad M = \frac{1}{\gamma(\rho)}\,\Gamma_s^{-1}(\xi)} \qquad \text{(derived, overdamped Rayleigh limit)}$$

**Onsager-Casimir extension (postulated):**

$$\boxed{\dot{\xi} = -(M + A)\,\nabla_\xi P} \qquad \text{(postulated)}$$

$A^T = -A$ — reactive part. Generates rotational motion on level sets of $P$ without $P$-descent. Required to explain the $\mathbf{R}\times\nabla_\mathbf{I}P$ coupling of Ch9 §9.4; not produced by the Lagrangian + Rayleigh structure.

---

## 10.4 The Lyapunov Selection (T6 Closed)

**Theorem 10.1 (Primary Lyapunov Function).** *Hypotheses:* (H1) $M \succ 0$ (holds by $\Gamma_s \succ 0$, $\gamma > 0$); (H2) $f$ locally Lipschitz; (H3) $D_\xi(\rho)$ compact (Ch9 Prop 9.1a H1) or $P$ coercive.

Under $\dot\xi = -(M+A)\nabla P$:

$$\frac{dP}{dt} = -\nabla_\xi P^T M\,\nabla_\xi P = -\frac{1}{\gamma}\|\nabla_\xi P\|^2_{\Gamma_s^{-1}} \leq 0$$

Antisymmetric contribution vanishes: $x^T A x = 0$ for all $x$ when $A^T = -A$. Strict descent away from $\mathcal{C} = \{\nabla P = 0\}$. By LaSalle, trajectories converge to largest invariant subset of $\mathcal{C}$; convergence to $\xi^*$ specifically requires isolated strict minimum (generic under Ch9 Prop 9.1a).

**Note on constructive circularity:** the dynamics are *constructed* so that $\dot P \leq 0$ — this is the gradient-flow ansatz. Theorem 10.1 establishes the specific descent rate and LaSalle convergence, not the Lyapunov property as an independent check.

**Candidate resolution (Ch9 §9.6):**
- $V(\Gamma) = \|\Gamma - \Gamma^*\|_F^2$: local proxy for $P$ near $\xi^*$ (valid when Hessian of $P$ is isotropic).
- $V(\xi) = \alpha|\text{Force}|^2 + \beta|\text{Field}|^2$: structural intensity diagnostic — **not** a Lyapunov function.
- Hierarchy: $P(\xi)$ (global Lyapunov) $\supset$ $V(\Gamma)$ (local proxy) $\supset$ $V(\xi)$ (diagnostic only).

---

## 10.5 G(3) Symmetry and the Nonlinear Terms of Ch9 §9.4 (T3 Partial)

### 10.5.1 Taylor Expansion of f

Near $\xi^*$: $(\nabla_\xi P)_i = H_{ij}\delta\xi_j + T_{ijk}\delta\xi_j\delta\xi_k + \mathcal{O}(\delta\xi^3)$. G(3)-invariance constrains admissible tensors $H$, $T$.

### 10.5.2 G(3)-Admissible Nonlinear Terms

**Notation disambiguation:**
- $\mathbf{A} \in \mathbb{R}^3$: Agency (bold, intrinsic state attribute)
- $A(\rho,\xi)$: Onsager-Casimir antisymmetric matrix (italic, operator on $\nabla P$)
- $\Gamma^i_{jk}$: Christoffel symbols of Levi-Civita connection of $\Gamma_s$ — distinct from configuration matrix $\Gamma$

**Remark on G(3) and dimension.** Cross-products $\mathbf{u}\times\mathbf{v}$ are SO(3)-equivariant, and any antisymmetric $3\times3$ operator is $x\mapsto\Omega\times x$ — both properties are **specific to three dimensions** via $\mathfrak{so}(3)\cong\mathbb{R}^3$. The G(3)-admissible terms below are 3D features.

G(3)-admissible quadratic terms in $\nabla_\mathbf{I}P$:

| Term | G(3) type |
|------|-----------|
| $\mathbf{R}\times\mathbf{I}$ | Vector |
| $\mathbf{A}\times\mathbf{I}$ | Vector |
| $S(\mathbf{A}\times\mathbf{R})$ | Vector |
| $|\mathbf{I}|^2\mathbf{I}$ | Vector (cubic self-coupling) |
| $(\mathbf{I}\cdot\mathbf{R})\mathbf{R}$ | Vector |

**Ch9 ansatz** $\dot{\mathbf{I}} = \alpha_\mathbf{I}(\mathbf{R}\times\mathbf{I}) + \beta_\mathbf{I}|\mathbf{I}|^2\mathbf{I}$ selects two:

- **$\mathbf{R}\times\nabla_\mathbf{I}P$**: from antisymmetric (reactive) part $A\nabla P$. In 3D: $A_\mathbf{I}\,x = \Omega\times x$; minimal G(3)-invariant choice is $\Omega = \alpha_\mathbf{I}\mathbf{R}$ — $\mathbf{R}$ is the environmental coupling vector, preserving the Field = $\mathbf{I}\times\mathbf{R}$ structure. Near equilibrium: $\nabla_\mathbf{I}P \propto \mathbf{I}$, so the full term reduces to $\alpha_\mathbf{I}\mathbf{R}\times\mathbf{I}$. In dim $\neq 3$, this coupling would require a bivector/2-form.

- **$|\mathbf{I}|^2\mathbf{I}$**: from nonlinearity of $\nabla P$ — leading cubic term in the Taylor expansion; present in dissipative part $M\nabla P$, does not require $A\neq 0$.

**Open:** coefficients $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$, explicit $A(\rho,\xi)$, additional G(3)-invariant terms — all require $P(\Gamma)$.

---

## 10.6 The Lagrangian in Terms of Γ

$$\mathcal{L}(\Gamma, \dot\Gamma) = \frac{1}{2}\text{Tr}(\dot\Gamma^T G_\Gamma\,\dot\Gamma) - P(\Gamma)$$

$G_\Gamma$ = induced metric on $\Gamma$-space. Jacobian $J_\Gamma = \partial\Gamma/\partial\xi$ is non-square ($d\geq n$), so compatibility condition $J_\Gamma^T G_\Gamma J_\Gamma = \Gamma_s$ has infinitely many solutions.

**Effective isotropic closure ansatz:** $G_\Gamma \propto \Gamma_s^{-1}$ — the most conservative (maximum-entropy) choice, introducing no additional asymmetry beyond what $\Gamma_s$ supplies and assuming no preferred direction in the normal space of $J_\Gamma$. This is an effective identification across different tensor types (not a tensorial equality). Gives in the overdamped limit: $\dot\Gamma \approx -\frac{1}{\gamma}\nabla_\Gamma P$.

---

## 10.7 The Structural Constants: ρ and γ

Linearized relaxation time near $\xi^*$: $\tau_\text{relax} \sim \gamma/\lambda_\text{min}(\Gamma_s^{-1}H)$.

**Phenomenological scaling ansatz** $\gamma \sim \rho\|\Gamma_s\|$ from two heuristics:
1. Higher $\rho$ → slower relaxation *(structural hypothesis, not derived)*
2. Rayleigh proportional damping: $\gamma\propto\|\Gamma_s\|$ (stiffness analogy — heuristic correspondence)

With this ansatz: ego-level UoCs ($\rho$ large) relax slowly *(candidate)*; soul-level UoCs ($\rho\to 0$) relax quickly *(candidate)*. The identification of $\rho$ levels with ego/soul is established in Ch11 §11.7, not here.

**Remark (missing damping-gradient terms):** if $\gamma$ depends on $\xi$ through $\|\Gamma_s(\xi)\|$, a full derivation would generate $\frac{\partial\gamma}{\partial\xi}\dot\xi$ corrections. These are $O(1/\gamma)$ relative to dissipation and are dropped consistently with the overdamped limit.

**This remains a phenomenological scaling ansatz.** Proportionality constant and full functional form require the explicit Lagrangian.

### 10.7.1 Epistemic Status Table

| Result | Status |
|--------|--------|
| $\dot\xi = -M\nabla P$, $M = \Gamma_s^{-1}/\gamma$ | **Derived** (overdamped Rayleigh limit, leading order in $1/\gamma$) |
| $P(\xi)$ primary Lyapunov function | **Derived** ($\dot P = -\nabla P^T M\nabla P\leq 0$, $M\succ 0$) |
| Convergence to $\mathcal{C}$ | **Derived** (LaSalle, under H1–H3) |
| Convergence to $\xi^*$ specifically | **Conditional** (isolated strict minimum, generic by Ch9 Prop 9.1a) |
| $A$ antisymmetric (reactive part) | **Postulated** (minimal Onsager-Casimir) |
| $\mathbf{R}\times\nabla_\mathbf{I}P$ rotational term | **Symmetry-admissible** (G(3) + 3D antisymmetry; not derived from $P$) |
| $|\mathbf{I}|^2\mathbf{I}$ self-interaction | **Symmetry-admissible** (leading nonlinear G(3)-invariant in $\nabla_\mathbf{I}P$) |
| $G_\Gamma = \Gamma_s^{-1}$ in $\Gamma$-space | **Working approximation** (isotropic closure ansatz) |
| $\gamma\sim\rho\|\Gamma_s\|$ | **Empirical law** (PR-24, 2026-05-31): $\gamma \propto \rho$ confirmed in air over 5 decades to 0.1% precision; with $c^2(\rho)$ saturated (E6×E1). Formal derivation from Rayleigh dissipation remains Part III. |
| Lagrangian form $\|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu\det(\Gamma)$ | **Derived in Part II** (Ch13: Frobenius uniqueness + attractor condition + ghost-freedom) |
| $\kappa = -1$ | **Derived in Part II** (Ch13: ghost-freedom requires $\kappa < 0$; $\kappa = -1$ from Frobenius normalization) |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | **Derived in Part II** (Ch14: T1 scaling law + massless graviton anchor) |
| $P(\Gamma)P(\Gamma)^T \propto I$ at attractor | **Derived in Part II** (Ch13 Thm 13.2 + Ch19 Lemma 19.1: unique max of $\mathcal{C}(\Gamma)$) |
| Homeodynamic Lyapunov function | **Derived in Part II** (Ch19 Thm 19.1: $V = \|\dot\Gamma\|^2 + (1-\mathcal{C})^2$; supersedes T6 here) |

---

## 10.8 Closing the Tensions

| Tension | Status |
|---------|--------|
| **T3** — form of $f$ | **Partially closed**: $f = -(M+A)\nabla P$; $M$ derived; $A$ postulated; $\mathbf{R}\times\nabla_\mathbf{I}P$ and $|\mathbf{I}|^2\mathbf{I}$ G(3)-admissible. Coefficients pending $P(\Gamma)$. |
| **T6** — Lyapunov selection | **Closed**: $P(\xi)$ primary; $V(\Gamma)$ local proxy; $V(\xi)$ diagnostic only. |
| **T7** — derivation chain | **Structurally closed**: Lagrangian → $f$ (§10.3.2) → Lyapunov (§10.4). Coefficients pending $P$. |

---

## 10.9 Open Questions

- **Explicit $P(\Gamma)$**: developed in Ch11 from G(3)-invariant polynomial constraints; coefficients $\kappa=-1$, $\mu(\rho)$ derived in Part II (Ch13–14).
- **Inertial regime**: full second-order equation deferred to future work.
- **Position-dependent $\Gamma_s$**: Christoffel corrections may be significant near structural bifurcations.
- **Derivation of $\gamma(\rho)$**: proportionality constant requires explicit Lagrangian from first principles.

---

*End of Chapter 10 (condensed)*
