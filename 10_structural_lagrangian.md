# Chapter 10: The Structural Lagrangian

## 10.1 The Program

Ch9 presented the nonlinear dynamics of a UoC through the purpose function $P(\Gamma)$ and a minimal nonlinear ansatz for the evolution law $f(\xi, \rho)$, deferring their derivation from variational principles. This chapter addresses that deferral in two structurally distinct parts:

- **Dissipative sector** (§10.3): the symmetric part of the evolution law $\dot\xi = -M\nabla P$ is *derived* from the structural Lagrangian via the overdamped Rayleigh limit — modulo the explicit form of $P(\Gamma)$, which remains open.
- **Reactive sector** (§10.3.2): the antisymmetric part $-A\nabla P$ is *not* produced by the Lagrangian + Rayleigh structure alone — it requires additional geometric input (gyroscopic term, symplectic connection). It is introduced as the **minimal Onsager-Casimir postulate** required to accommodate rotational dynamics (in particular, the $R \times \nabla_I P$ coupling that the variational structure cannot generate internally).

This chapter therefore **closes the dissipative variational structure at the level of minimal canonical modeling assumptions** and **identifies the minimal postulated extension required for reactive dynamics**. "Closes" does not mean formal completeness: (1) the explicit $P(\Gamma)$ remains unknown; (2) the admissible class of Lagrangians is not fully classified; (3) the antisymmetric sector is postulated, not variationally derived.

Three open tensions are addressed:

- **T3** — the specific functional form of $f$, in particular the origin of the nonlinear terms $R \times \nabla_I P$ and $|I|^2 I$ of Ch9 §9.4
- **T6** — which of the two Lyapunov candidates of Ch9 §9.6 is primary
- **T7** — the derivation chain: Lagrangian → $f$ → Lyapunov → Ch9 completed

The strategy: identify the minimal structural requirements on the action and show that they identify the **minimal canonical structural Lagrangian compatible with those requirements** at lowest order.

**Epistemic status.** The dissipative sector of $f$ and the Lyapunov selection (T6) are derived (in the overdamped Rayleigh limit), modulo the explicit $P(\Gamma)$ (structure determined, coefficients open). The reactive sector is postulated as the minimal Onsager-Casimir generalization; its G(3) admissible form is identified in §10.5 but not derived from the action. T3 is partially closed; T7 is structurally closed.

This chapter establishes the **geometric-dissipative skeleton** of the UoC dynamics — the kinematic structure (Riemannian metric $\Gamma_s$, Levi-Civita connection, gradient flow) and the dissipative law ($M = \Gamma_s^{-1}/\gamma$, Lyapunov $P$). The explicit force landscape — the specific form of $P(\Gamma)$ that determines what the UoC is actually optimizing — remains open. Kinematics and dissipation structure: established. Full dynamics: contingent on $P(\Gamma)$.

**Part II status (added after Part II completion).** Several results left open in this chapter are derived in Part II. The Lagrangian is no longer "minimal canonical ansatz" — Part II (Ch13) derives it as the *unique* form consistent with Frobenius uniqueness, the attractor condition, and ghost-freedom. The coefficients $\kappa = -1$ and $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ are derived, not postulated. The function $P(\Gamma)$ — left open here — is resolved in Part II (Ch13 Theorem 13.2): the attractor satisfies $P(\Gamma)P(\Gamma)^T \propto I$, and the structural coherence $\mathcal{C}(\Gamma)$ (Ch19) provides the Lyapunov function whose formal stability theorem (Ch19 Theorem 19.1) supersedes the T6 resolution of §10.4. The reader is referred to Part II for these derivations.

---

## 10.2 The Structural Action

### 10.2.1 Minimal Requirements

The structural Lagrangian $\mathcal{L}(\xi, \dot{\xi})$ governing the evolution of a UoC's state $\xi = (S, A, I, R)$ must satisfy three minimal requirements:

**Requirement 1 (G(3)-invariance).** $\mathcal{L}$ is a scalar under the symmetry group $G(3)$ of the UoC — it is invariant under the transformations that preserve the algebraic structure $\{S, A, I, R\}$ (Ch3).

**Requirement 2 (Canonical kinetic term).** $\mathcal{L}$ is quadratic in velocities $\dot{\xi}$. This is the lowest-order Lagrangian consistent with a well-posed Cauchy problem and with second-order Euler-Lagrange equations.

**Requirement 3 (Coupling-metric consistency).** The kinetic metric on $\xi$-space — the matrix $K_{ij}$ such that $T = \frac{1}{2}\dot{\xi}^T K \dot{\xi}$ — is induced by the configuration matrix $\Gamma_s$ of Ch5. This requirement links the Lagrangian geometry to the structural coupling already defined.

### 10.2.2 The Structural Lagrangian

A minimal canonical Lagrangian satisfying Requirements 1–3 at lowest order is:

$$\boxed{\mathcal{L}(\xi, \dot{\xi}) = \frac{1}{2}\,\dot{\xi}^T \Gamma_s(\xi)\,\dot{\xi} - P\!\left(\Gamma[\xi]\right)}$$

where:
- $\Gamma_s(\xi)$ is the symmetric part of the configuration matrix (Ch5 §5.4), evaluated at the current state $\xi$ — it plays the role of the **kinetic metric** on attribute space
- $P(\Gamma[\xi])$ is the purpose function (Ch9 §9.5) — it plays the role of the **structural potential**
- The structural action is $\mathcal{A}[\xi] = \int \mathcal{L}(\xi, \dot{\xi})\,dt$ (notation: $\mathcal{A}$ for action to avoid collision with $S$ = Singularity)

**Canonical choice at lowest order.** The kinetic term $\frac{1}{2}\dot{\xi}^T \Gamma_s \dot{\xi}$ is the **minimal canonical choice** of G(3)-invariant quadratic form on $\dot{\xi}$ consistent with Requirement 3. In general, the space of G(3)-invariant quadratic forms on $\dot{\xi}$ may include additional invariants (e.g., cross-sector terms $\dot{\xi}_I^T K_{IR} \dot{\xi}_R$ coupling different sectors); these are not included here as they require further structure not established by Requirements 1–3 alone. Higher-order kinetic terms also exist (Born-Infeld-like) but are excluded at lowest order. The potential $P(\Gamma[\xi])$ is specified by Postulate 9.1; its explicit form is an open question (T3, pending Lagrangian derivation from first principles).

**Antisymmetric sector.** The restriction of the structural Lagrangian to the antisymmetric sector in the static configuration ($\dot{\xi} = 0$) gives $\mathcal{L}\big|_{\text{static}} \propto \text{Tr}(\Gamma_a^T \Gamma_a)$. The full structural Lagrangian $\mathcal{L}$ extends this to time-dependent configurations.

---

## 10.3 Euler-Lagrange Equations and the Overdamped Limit

### 10.3.1 The Full Euler-Lagrange Equations

**Postulate 10.1 (Γ_s as Riemannian Metric).** In this section, $\Gamma_s(\xi)$ is interpreted as a **positive-definite Riemannian metric on the state manifold** of the UoC. This requires:

$$\Gamma_s(\xi) \succ 0 \qquad \text{for all } \xi \text{ in the dynamically accessible region}$$

which holds by Ch5 §5.5.2 and Ch5 Remark 5.1 (Γ_s ≻ 0 is not merely a health condition but a necessary consequence of the UoC having well-defined Lyapunov dynamics — a circularity that is acknowledged: Ch5 Remark 5.1 establishes this necessity using the present chapter's Theorem 10.1 as a forward reference). Promoting $\Gamma_s$ to a Riemannian metric identifies the intrinsic coupling geometry of the UoC with the geometry of its state space. Of the three requirements for this promotion, two are now derived:

1. **Transformation law**: $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ under G(3). **Derived in Ch8 §8.8** — not an assumption.
2. **Smoothness**: $\Gamma_s \in C^\infty(\mathcal{V})$ — the Gram map of Ch8 §8.5 is polynomial, hence $C^\infty$. Not an assumption — a consequence.
3. **Connection choice** *(genuine postulate)*: the Levi-Civita connection is selected as the natural (torsion-free, metric-compatible) connection. Alternative connections with torsion are possible; the Levi-Civita choice is minimal.

The Euler-Lagrange equations for $\mathcal{L}$:

$$\frac{d}{dt}\frac{\partial \mathcal{L}}{\partial \dot{\xi}} - \frac{\partial \mathcal{L}}{\partial \xi} = 0$$

give the **structural geodesic equation with forcing**, written in coordinate-free form as:

$$\nabla_{\dot\xi}\dot\xi = -\operatorname{grad}_{\Gamma_s} P$$

where $\nabla$ is the Levi-Civita connection of $\Gamma_s$ and $\operatorname{grad}_{\Gamma_s} P = \Gamma_s^{-1}\nabla_\xi P$ is the Riemannian gradient. The left-hand side is the covariant acceleration; the right-hand side is the structural force. In coordinates:

$$\ddot{\xi}^i + \Gamma^i_{jk}\,\dot{\xi}^j\dot{\xi}^k = -\left(\Gamma_s^{-1}\right)^{ij}\partial_j P$$

where $\Gamma^i_{jk} = \frac{1}{2}(\Gamma_s^{-1})^{il}\left(\partial_j (\Gamma_s)_{lk} + \partial_k (\Gamma_s)_{lj} - \partial_l (\Gamma_s)_{jk}\right)$ are the Christoffel symbols of the Levi-Civita connection of $\Gamma_s$.

**Remark.** If $\Gamma_s$ were constant (position-independent), all Christoffel symbols vanish and the equation reduces to $\Gamma_s \ddot{\xi} = -\nabla_\xi P$ — a standard equation of motion in a flat attribute space with constant mass matrix.

### 10.3.2 The Overdamped Limit: Deriving f

A UoC operating in the biological and psychological regimes is strongly dissipative — the inertial term $\Gamma_s \ddot{\xi}$ is negligible compared to the dissipative term. This is formalized by introducing a **Rayleigh dissipation function**:

$$\mathcal{R}(\dot{\xi}) = \frac{\gamma}{2}\,\dot{\xi}^T \Gamma_s(\xi)\,\dot{\xi}, \qquad \gamma > 0$$

The generalized dissipative force from $\mathcal{R}$ is $Q_i^\text{(diss)} = -\partial\mathcal{R}/\partial\dot\xi^i = -\gamma(\Gamma_s)_{ij}\dot\xi^j$. Adding this to the Euler-Lagrange equation gives the covariant form:

$$\Gamma_s\bigl(\nabla_{\dot\xi}\dot\xi\bigr) + \gamma\,\Gamma_s\,\dot\xi = -\nabla_\xi P$$

After raising the index with $\Gamma_s^{-1}$, this takes the coordinate-free form:

$$\nabla_{\dot\xi}\dot\xi + \gamma\,\dot\xi = -\operatorname{grad}_{\Gamma_s} P$$

In the **overdamped limit**, the scaling argument is as follows. In coordinates, the covariant acceleration expands as:

$$\nabla_{\dot\xi}\dot\xi = \ddot\xi + \Gamma^i_{jk}\dot\xi^j\dot\xi^k$$

Near a trajectory with $|\dot\xi| \sim P_0/(\gamma \|\Gamma_s\|)$ (set by the force balance), the Christoffel term scales as $O(1/\gamma^2)$ while the dissipative term $\gamma\dot\xi$ scales as $O(1/\gamma)$. As $\gamma \to \infty$, the Christoffel term is suppressed relative to dissipation by $O(1/\gamma)$:

$$\frac{|\Gamma^i_{jk}\dot\xi^j\dot\xi^k|}{|\gamma\dot\xi^i|} = O(1/\gamma) \to 0$$

so $\nabla_{\dot\xi}\dot\xi \approx 0$ to leading order in $1/\gamma$:

$$\gamma\,\dot\xi \approx -\operatorname{grad}_{\Gamma_s} P = -\Gamma_s^{-1}(\xi)\,\nabla_\xi P \qquad \Longrightarrow \qquad \dot{\xi} = -\frac{1}{\gamma}\,\Gamma_s^{-1}(\xi)\,\nabla_\xi P$$

**This identifies the dissipative sector of the evolution law:**

$$\boxed{\dot{\xi} = -M(\rho, \xi)\,\nabla_\xi P, \qquad M(\rho, \xi) = \frac{1}{\gamma(\rho)}\,\Gamma_s^{-1}(\xi)} \qquad \text{(derived in the overdamped Rayleigh limit)}$$

The Lagrangian + Rayleigh formalism reduces to this at leading order in $1/\gamma$: $\dot{\xi} = -M\nabla P$ with $M$ symmetric positive definite. Corrections at order $O(1/\gamma^2)$ come from Christoffel curvature terms and are dropped. No antisymmetric term is generated by this structure — a reactive part $A\nabla P$ requires additional geometric input (a gyroscopic Lagrangian term $\mathcal{L}_A = \mathbf{C}(\xi)\cdot\dot{\xi}$, a Poisson bracket, or a symplectic connection).

**Onsager-Casimir extension (postulated).** The minimal generalization that accommodates rotational dynamics — required to explain the $R \times I$ coupling of Ch9 §9.4 (§10.5) — is:

$$\boxed{\dot{\xi} = -\bigl(M(\rho, \xi) + A(\rho, \xi)\bigr)\,\nabla_\xi P} \qquad \text{(postulated)}$$

where $A(\rho, \xi)$ is **antisymmetric** ($A^T = -A$) — the reactive (Onsager-Casimir) part, generating rotational motion in $\xi$-space along level sets of $P$ without consuming $P$. This is the standard **Onsager-Casimir decomposition** of the linear response operator $L = M + A$: $M$ captures irreversible relaxation, $A$ captures reversible conservative rotation. The Lyapunov property is preserved for any $A$ (§10.4).

**Connections:**

1. **Symmetric limit**: the limit $A = 0$ recovers $\dot{\xi} = -M\nabla P$, the purely dissipative gradient flow. The Onsager-Casimir extension adds reactive dynamics when $A \neq 0$.

2. **Mobility duality**: the dissipative mobility $M = \Gamma_s^{-1}/\gamma$ and the coupling operator $\Gamma_s$ satisfy $\Gamma_s \cdot M = \frac{1}{\gamma} I$. Tightly coupled attributes ($\Gamma_s$ large) move slowly ($M$ small); loosely coupled attributes move quickly. The reactive part $A$ does not affect this duality.

3. **$\rho$-dependence**: both $M$ and $A$ depend on $\rho$. The dissipation rate $\gamma(\rho)$ and the structure of $A(\rho, \xi)$ require the full Lagrangian from first principles (open question, §10.7).

---

## 10.4 The Lyapunov Selection (T6 Closed)

**Theorem 10.1 (Primary Lyapunov Function).** *Hypotheses:* (H1) $M(\rho,\xi) \succ 0$ (symmetric positive definite — holds by $\Gamma_s \succ 0$ and $\gamma > 0$); (H2) $f(\xi,\rho) = -(M+A)\nabla P$ is locally Lipschitz continuous in $\xi$ (required for existence and uniqueness of trajectories); (H3) either (a) the dynamically accessible domain $D_\xi(\rho)$ is compact (Ch9 Prop 9.1a H1) or (b) $P$ is coercive ($P(\xi) \to \infty$ as $|\xi| \to \infty$), which ensures trajectories remain in a sublevel set and LaSalle applies.

*Conclusion:* Under these hypotheses and the overdamped structural dynamics $\dot{\xi} = -(M+A)\nabla P$, the purpose function $P(\xi)$ is the **primary Lyapunov function**:

**Note on constructive circularity.** The dynamics $\dot\xi = -(M+A)\nabla P$ are *constructed* so that $\dot P \leq 0$ — this is the defining feature of the gradient-flow ansatz. The Lyapunov property of $P$ is therefore a consequence of the structural choice of dynamics, not an independent verification. What Theorem 10.1 establishes is that: given this choice, $P$ is a valid strict Lyapunov function with the specific descent rate $-\frac{1}{\gamma}\|\nabla P\|^2_{\Gamma_s^{-1}}$, and LaSalle's principle implies asymptotic convergence to the critical set $\mathcal{C}$.

$$\frac{dP}{dt} = \nabla_\xi P \cdot \dot{\xi} = -\nabla_\xi P^T (M+A)\,\nabla_\xi P = -\nabla_\xi P^T M\,\nabla_\xi P = -\frac{1}{\gamma}\|\nabla_\xi P\|^2_{\Gamma_s^{-1}} \leq 0$$

where the antisymmetric contribution vanishes identically: $\nabla_\xi P^T A\,\nabla_\xi P = 0$ for any antisymmetric $A$ (since $x^T A x = 0$ for all $x$ when $A^T = -A$). Equality holds iff $\nabla_\xi P \in \ker M$; since $M \succ 0$, this is equivalent to $\nabla_\xi P = 0$, i.e., at the structural attractor $\xi^*$. The reactive part $A$ generates rotational motion on level sets of $P$ without affecting the descent.

**Strict Lyapunov function.** Since $M = \Gamma_s^{-1}/\gamma \succ 0$, the rate $-\nabla_\xi P^T M \nabla_\xi P < 0$ strictly whenever $\nabla_\xi P \neq 0$. $P$ is therefore a **strict Lyapunov function** for the dynamics away from the critical set $\mathcal{C} = \{\xi : \nabla_\xi P = 0\}$. By LaSalle's invariance principle, trajectories converge asymptotically to the largest invariant subset of $\mathcal{C}$. This establishes **asymptotic convergence toward $\mathcal{C}$**, and convergence to the isolated attractor $\xi^*$ specifically under the hypotheses of Proposition 9.1a of Ch9 (isolated strict minimum). In general — without coercivity of $P$ or uniqueness of the critical point — convergence to $\xi^*$ is not guaranteed and $\mathcal{C}$ may contain saddles, multiple minima, or a critical manifold. The two parts of the dynamics have distinct stability characters: $M$ drives asymptotic convergence toward $\mathcal{C}$; $A$ generates conservative rotation *on* level sets of $P$, which is neutral (not asymptotic) in $P$.

**The two candidates of Ch9 §9.6 resolved:**

- **Candidate 1**: $V(\Gamma) = \|\Gamma - \Gamma^*\|_F^2$ — this is a proxy for $P$ near the attractor. Since $P(\Gamma^*) = 0$ and $P$ is smooth, $P(\Gamma) \approx \frac{1}{2}(\Gamma - \Gamma^*)^T H_\Gamma (\Gamma - \Gamma^*)$ near $\Gamma^*$, where $H_\Gamma$ is the Hessian of $P$ with respect to $\Gamma$. $V(\Gamma)$ approximates $P$ when $H_\Gamma \approx I$ (isotropic Hessian). It is a valid Lyapunov function near the attractor but not globally.

- **Candidate 2**: $V(\xi) = \alpha|\text{Force}|^2 + \beta|\text{Field}|^2$ — this measures structural intensity (the magnitude of the UoC's agency and field), not distance to the attractor. It is not generally a Lyapunov function for the gradient flow: $\dot{V}(\xi) \leq 0$ holds only if the gradient of intensity aligns with $-\nabla P$, which is not guaranteed.

**Resolution**: $P(\xi)$ is primary. $V(\Gamma)$ is a local approximation valid near $\xi^*$; $V(\xi)$ is a structural diagnostic (intensity measure) but not a Lyapunov function. The hierarchy is:

$$P(\xi) \quad \text{(Lyapunov, global)} \;\supset\; V(\Gamma) \quad \text{(Lyapunov, local near }\xi^*) \;\supset\; V(\xi) \quad \text{(diagnostic only)}$$

---

## 10.5 G(3) Symmetry and the Nonlinear Terms of Ch9 §9.4 (T3 Partial)

### 10.5.1 The Taylor Expansion of f

The full evolution law $f = -(M+A)\nabla P$ requires the explicit $P(\Gamma[\xi])$. Without it, we can characterize the **structure** of $f$ by expanding $\nabla P$ in a Taylor series around $\xi^*$ and restricting to G(3)-invariant terms.

Near $\xi^*$, expanding $\nabla_\xi P$ in powers of $\delta\xi = \xi - \xi^*$:

$$(\nabla_\xi P)_i = \sum_j H_{ij}\,\delta\xi_j + \sum_{j,k} T_{ijk}\,\delta\xi_j\,\delta\xi_k + \mathcal{O}(\delta\xi^3)$$

where $H_{ij} = \partial^2 P / \partial\xi_i \partial\xi_j|_{\xi^*}$ is the Hessian and $T_{ijk}$ are the third-order coefficients. G(3)-invariance constrains which tensors $H$ and $T$ are admissible.

### 10.5.2 G(3)-Admissible Nonlinear Terms

**Notation disambiguation.** Two distinct objects named $A$ appear in this chapter: (1) $\mathbf{A} \in \mathbb{R}^3$ — Agency, the intrinsic vector attribute of the UoC (bold, sector of the state vector $\xi$); (2) $A(\rho,\xi)$ — the Onsager-Casimir antisymmetric matrix (italic, operator on $\nabla P$). These are unrelated. The context always disambiguates: $\mathbf{A}$ is a state component; $A$ is a matrix in the evolution law. Similarly, $\Gamma^i_{jk}$ in §10.3.1 denotes the Christoffel symbols of the Levi-Civita connection of the Riemannian metric $\Gamma_s$ — these are coordinate-dependent objects constructed from derivatives of $\Gamma_s$, distinct from the configuration matrix $\Gamma$ (the central object of the GSF).

The state space decomposes as $\xi = (S, \mathbf{A}, \mathbf{I}, \mathbf{R})$ with:
- $S \in \mathbb{R}$ (scalar under G(3))
- $\mathbf{A}, \mathbf{I}, \mathbf{R} \in \mathbb{R}^3$ (vectors under G(3) rotations)

**Remark on G(3) and dimension.** The symmetry group G(3) of a UoC (Ch3) contains $\text{SO}(3)$ as its rotation subgroup, acting simultaneously on all three-vector sectors $(A, I, R)$. The analysis below uses two properties that are **specific to three dimensions**: (1) cross-products $u \times v$ are $\text{SO}(3)$-equivariant vectors, and (2) any antisymmetric $3 \times 3$ operator can be written as $x \mapsto \Omega \times x$ for some axial vector $\Omega$, via the Lie algebra isomorphism $\mathfrak{so}(3) \cong \mathbb{R}^3$ (the axial-vector map). Neither property generalizes beyond three dimensions. The admissible G(3)-invariant terms in the table below are therefore a feature of the 3D attribute space of the GSF, not of a general symmetry group.

A G(3)-invariant quadratic combination of $\{A, I, R\}$ that produces a vector in the $I$-sector must be a cross-product or a scalar multiple. The admissible quadratic terms in $\nabla_I P$ are:

| Term | G(3) type | Physical interpretation |
|------|-----------|------------------------|
| $R \times I$ | Vector (from $\mathbf{b} \times \mathbf{c}$) | Register-Field coupling |
| $A \times I$ | Vector | Agency-Field coupling |
| $S(A \times R)$ | Vector (scalar-weighted cross product) | Scalar-mediated coupling |
| $(I \cdot I)I = |I|^2 I$ | Vector (self-coupling) | Field self-interaction |
| $(I \cdot R)R$ | Vector | Register-projected field |

The Ch9 §9.4 ansatz for $\dot{\mathbf{I}}$:

$$\dot{\mathbf{I}} = \alpha_\mathbf{I}(\mathbf{R} \times \mathbf{I}) + \beta_\mathbf{I}|\mathbf{I}|^2 \mathbf{I}$$

selects exactly two of these terms. Their origins in the Onsager-Casimir decomposition are structurally distinct:

- **$\mathbf{R} \times \nabla_\mathbf{I} P$** arises from the **antisymmetric (reactive) part** $A\nabla P$. In three dimensions, any antisymmetric linear operator acting on a vector $x \in \mathbb{R}^3$ can be written as:
  $$A_\mathbf{I}\,x = \Omega \times x$$
  for some axial vector $\Omega$ depending on $\xi$. The minimal G(3)-invariant choice is $\Omega = \alpha_\mathbf{I} \mathbf{R}$ — $\mathbf{R}$ is the natural candidate because it is the environmental coupling vector (the attribute governing exchange with the environment), and the $\mathbf{I} \times \mathbf{R}$ structure is precisely what generates the inherent Field variable (Ch1 §1.4). Using $\Omega \propto \mathbf{R}$ therefore preserves the Field = $\mathbf{I} \times \mathbf{R}$ structure at the level of dynamics. This gives:
  $$\boxed{A_\mathbf{I}(\nabla_\mathbf{I} P) = \alpha_\mathbf{I}\,\mathbf{R} \times \nabla_\mathbf{I} P}$$
  This is the **global** reactive term. **Near equilibrium** ($\xi \approx \xi^*$), the gradient linearizes as $\nabla_\mathbf{I} P \approx H_{\mathbf{I}\mathbf{I}}(\mathbf{I} - \mathbf{I}^*) \propto \mathbf{I}$, so the reactive term reduces to $\alpha_\mathbf{I} \mathbf{R} \times \mathbf{I}$ — the Ch9 ansatz. Away from $\xi^*$, the full term is $\mathbf{R} \times \nabla_\mathbf{I} P$, not $\mathbf{R} \times \mathbf{I}$. The cross-product structure is a kinematic consequence of antisymmetry and G(3)-invariance, not an *ad hoc* coupling. A pure symmetric gradient flow ($A = 0$) cannot generate it; the Onsager-Casimir extension of §10.3.2 is structurally necessary. **In dimensions other than 3**, the axial-vector representation $\Omega \times x$ does not exist; the reactive coupling would require a bivector or 2-form (e.g., $\omega^{ij}$ in higher dimensions), reflecting that the cross-product structure is specifically three-dimensional.

- **$|\mathbf{I}|^2 \mathbf{I}$** arises from the **nonlinearity of $\nabla P$** itself — it is a leading cubic term in the Taylor expansion of the gradient (§10.5.1). It is present in the dissipative part $M\nabla P$ and does not require $A \neq 0$.

**What the Lagrangian derivation establishes:** both terms are not *ad hoc* — they are the lowest-order G(3)-invariant contributions in their respective structural roles (reactive rotational coupling vs. dissipative self-interaction nonlinearity). The Onsager-Casimir decomposition $f = -(M+A)\nabla P$ provides the natural home for each.

**What remains open:** the coefficients $\alpha_\mathbf{I}$ and $\beta_\mathbf{I}$, the explicit form of $A(\rho, \xi)$ at the $\mathbf{I}$-sector, and which additional G(3)-invariant terms from the table are present — all require the explicit $P(\Gamma)$. This is the residual content of T3.

---

## 10.6 The Lagrangian in Terms of Γ

In the representation $\xi \to \Gamma[\xi]$ (the configuration matrix as a function of state), the structural Lagrangian becomes:

$$\mathcal{L}(\Gamma, \dot{\Gamma}) = \frac{1}{2}\,\text{Tr}\!\left(\dot{\Gamma}^T G_\Gamma\,\dot{\Gamma}\right) - P(\Gamma)$$

where $G_\Gamma$ is the **induced metric on $\Gamma$-space** — the pullback of the $\xi$-space kinetic metric through the map $\xi \mapsto \Gamma[\xi]$. Its explicit form depends on the Jacobian $\partial\Gamma/\partial\xi$ of that map. Let $J_\Gamma = \partial\Gamma/\partial\xi \in \mathbb{R}^{d \times n}$ be the Jacobian of the map $\xi \mapsto \Gamma[\xi]$, where $d = \dim(\Gamma\text{-space}) \geq n = \dim(\xi\text{-space})$. Since $d \geq n$, $J_\Gamma$ is generally **not square** and has no ordinary inverse. The metric $G_\Gamma$ on $\Gamma$-space consistent with the $\xi$-space kinetic structure must satisfy the compatibility condition:

$$J_\Gamma^T\, G_\Gamma\, J_\Gamma = \Gamma_s$$

When $J_\Gamma$ is not square, this equation has infinitely many solutions — $G_\Gamma$ is not determined by compatibility alone without additional constraints on the normal directions (directions in $\Gamma$-space not in the image of $J_\Gamma$). Determining $G_\Gamma$ uniquely requires the explicit parameterization, which is not available at this stage. In absence of this, we adopt an **effective isotropic closure ansatz**: $G_\Gamma$ is taken proportional to $\Gamma_s^{-1}$ (up to a scalar factor absorbed into $\gamma$):

$$G_\Gamma \propto \Gamma_s^{-1} \qquad \text{(effective isotropic closure ansatz)}$$

Note that $\Gamma_s$ lives in $\xi$-space while $G_\Gamma$ is a metric on $\Gamma$-space — they are objects of different tensor types, and the proportionality is adopted as an effective identification rather than a tensorial equality. **This should be understood as a closure ansatz, not an induced metric identity.** It is the most conservative (maximum-entropy) choice among $G_\Gamma$-compatible metrics: it introduces no additional structural asymmetry beyond what $\Gamma_s$ itself supplies, and assumes no preferred direction in the normal space of $J_\Gamma$. The correct $G_\Gamma$ would require the explicit parameterization $\xi \mapsto \Gamma[\xi]$.

In the overdamped limit, the Euler-Lagrange equations in this representation give, under the working isotropic approximation $G_\Gamma = \Gamma_s^{-1}$:

$$\dot{\Gamma} \approx -\frac{1}{\gamma}\,\nabla_\Gamma P$$

where the gradient is taken with respect to the $G_\Gamma$-weighted Frobenius inner product. The approximation sign reflects that the exact pullback $G_\Gamma^\text{exact}$ may differ from $\Gamma_s^{-1}$.

**Connection to the Lyapunov candidate $V(\Gamma)$**: under the closure ansatz $G_\Gamma \propto \Gamma_s^{-1}$, the effective inner product on $\Gamma$-space is $\langle \delta\Gamma_1, \delta\Gamma_2 \rangle_{G_\Gamma} \propto \text{Tr}(\delta\Gamma_1^T \Gamma_s^{-1} \delta\Gamma_2)$. The candidate $V(\Gamma) = \|\Gamma - \Gamma^*\|_F^2$ uses the unweighted Frobenius norm; the geometrically motivated distance under the ansatz is $\|\Gamma - \Gamma^*\|^2_{G_\Gamma} \propto \text{Tr}((\Gamma-\Gamma^*)^T \Gamma_s^{-1} (\Gamma-\Gamma^*))$. For configurations where $\Gamma_s \approx I$ (isotropic coupling), the two are proportional.

---

## 10.7 The Structural Constants: ρ and γ

The dissipation rate $\gamma(\rho)$ has a clear structural interpretation via the **relaxation timescale** of the UoC. Linearizing the overdamped dynamics near $\xi^*$:

$$\dot{\delta\xi} = -M H\,\delta\xi, \qquad M = \Gamma_s^{-1}/\gamma, \quad H = \nabla^2 P|_{\xi^*}$$

the dominant relaxation time is set by the smallest eigenvalue of $MH = \Gamma_s^{-1}H/\gamma$:

$$\tau_\text{relax} \sim \frac{\gamma}{\lambda_\text{min}(\Gamma_s^{-1} H)}$$

A coarser bound, obtained from $\lambda_\text{min}(\Gamma_s^{-1}H) \geq \lambda_\text{min}(H)/\|\Gamma_s\|$, gives $\tau_\text{relax} \lesssim \gamma\|\Gamma_s\|/\lambda_\text{min}(H)$. High $\gamma$ → long $\tau_\text{relax}$ → slow structural evolution toward the attractor.

**Physical motivation for $\gamma \sim \rho\|\Gamma_s\|$.** Two phenomenological heuristics suggest this scaling:

1. **Timescale separation**: we hypothesize that higher structural levels (higher $\rho$, ego) correspond to slower effective relaxation scales, and lower levels (lower $\rho$, soul) to faster ones. This is not derived from the formalism — it is a structural hypothesis motivated by the phenomenological observation that ego-level change is slower and more effortful than soul-level change. If this hypothesis holds, then $\gamma \propto \rho$.

2. **Structural stiffness (Rayleigh-type damping)**: in structural mechanics, viscous damping is often proportional to stiffness (Rayleigh proportional damping: $\gamma \propto K$). Here $\|\Gamma_s\|$ plays the role of structural stiffness — tightly coupled attributes (large $\|\Gamma_s\|$) resist change more strongly. The combination gives $\gamma \sim \rho\|\Gamma_s\|$.

With the ansatz $\gamma \sim \rho\|\Gamma_s\|$, the relaxation time scales as $\tau_\text{relax} \sim \rho\|\Gamma_s\|/\lambda_\text{min}(\Gamma_s^{-1}H)$, and the bound gives $\tau_\text{relax} \lesssim \rho\|\Gamma_s\|^2/\lambda_\text{min}(H)$. Both scale as $\rho$ for fixed coupling: ego-level UoCs ($\rho$ large) relax slowly *(candidate — see Ch11 §11.7)*; soul-level UoCs ($\rho \to 0$) relax quickly *(candidate)*. The identification of high-$\rho$ with "ego" and low-$\rho$ with "soul" is interpretive — established in Ch11, not here.

**Dimensional note.** In the GSF, $\Gamma_s$ is a Gram matrix of structural attributes and is dimensionless in natural structural units. The level variable $\rho$ is dimensionless (Ch4 §4.2), while $\gamma$ carries the dimension of inverse time (friction). The relation $\gamma \sim \rho\|\Gamma_s\|$ is therefore consistent only after identifying the proportionality constant with a reference timescale $\tau_0^{-1}$ set by the level — i.e., $\gamma = (\rho\|\Gamma_s\|)/\tau_0$ in dimensionless structural units where $\tau_0 = 1$. A complete dimensional analysis fixing $\tau_0$ requires the explicit Lagrangian.

**This remains a phenomenological scaling ansatz**, not a derived result. The proportionality constant and the functional form beyond leading order require the explicit Lagrangian (§10.9).

**Part II update (A4 — fluid operationalization).** Part II Ch15 §15.8c derives $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$ for the fluid domain (Theorem 15.5), giving the first quantitative operationalization of $\gamma$: $\gamma = c^2(\rho)/\nu_{\mathrm{kin}}$. This is consistent with $\gamma \sim \rho\|\Gamma_s\|$ under the identification $\|\Gamma_s\|_{\mathrm{fluid}} \sim c^2(\rho)/(\rho\,\nu_{\mathrm{kin}})$. The ratio $\gamma_A/\gamma_B = \nu_B/\nu_A$ is testable from viscosity tables without Hito 3 — the first empirical test of A4. See brainstorming/bitacora_ansatz.md §A4.

**Empirical confirmation 2026-05-31 (PR-24).** Air viscosity over five orders of magnitude in density ($P \in [10^{-3}, 10]$ atm) obeys $\nu_{\mathrm{kin}} \propto 1/\rho$ to 0.1% precision. Combined with the saturation result $c^2(\rho) \approx c_*^2$ in the continuum regime (see `brainstorming/pruebas_empiricas/E6xE1_cross.md` and `PR24_gases.md`), this implies $\gamma \propto \rho$ linearly across five decades at fixed $\Gamma_s$ (same gas, same $T$). A4 is no longer phenomenological in the fluid domain; it is empirically anchored in the gas continuum regime. The formal derivation from Rayleigh dissipation with explicit $\Gamma_s(\xi)$ remains Part III work, but the scaling itself is now established by data.

**Remark (missing damping-gradient terms).** The ansatz $\gamma \sim \rho\|\Gamma_s\|$ treats $\gamma$ as depending on $\xi$ only through the scalar $\|\Gamma_s(\xi)\|$. A full derivation from the Euler-Lagrange equations with position-dependent $\Gamma_s$ would generate additional terms of the form $\frac{\partial \gamma}{\partial \xi}\,\dot\xi$ (damping-gradient corrections), which are absent from the leading-order overdamped approximation. These corrections are of order $O(1/\gamma)$ relative to the dominant dissipation term and are dropped consistently with the overdamped limit, but they would modify the evolution law at next order.

### 10.7.1 Derived vs. Postulated Results

For reference, the epistemic status of each main result in this chapter:

| Result | Status | Basis |
|--------|--------|-------|
| $\dot\xi = -M\nabla P$, $M = \Gamma_s^{-1}/\gamma$ | **Derived in overdamped Rayleigh limit** | Singular reduction of Lagrangian + Rayleigh dissipation; not an exact consequence of the action |
| $P(\xi)$ is primary Lyapunov function | **Derived** | $dP/dt = -\nabla P^T M \nabla P \leq 0$; $M \succ 0$ |
| Convergence to critical set $\mathcal{C}$ | **Derived** | LaSalle's invariance principle |
| Convergence to $\xi^*$ specifically | **Conditional** | Requires $\xi^*$ isolated strict minimum (generic by Ch9 Prop 9.1a) |
| $A$ antisymmetric (reactive part) | **Postulated** | Minimal Onsager-Casimir generalization; not produced by the action |
| $R \times \nabla_I P$ rotational term | **Symmetry-admissible** | G(3) + antisymmetry of $A$ in 3D; not derived from $P$ |
| $\vert I\vert^2 I$ self-interaction | **Symmetry-admissible** | Leading nonlinear G(3)-invariant term in $\nabla_I P$ expansion |
| $G_\Gamma = \Gamma_s^{-1}$ in $\Gamma$-space | **Working approximation** | Isotropic limit of exact pullback; not derived from $J_\Gamma$ |
| $\gamma \sim \rho\,\|\Gamma_s\|$ | **Phenomenological ansatz** | Timescale hypothesis + Rayleigh-type stiffness analogy |
| Lagrangian form $\|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu\det(\Gamma)$ | **Derived in Part II** | Frobenius uniqueness + attractor condition + ghost-freedom (Ch13 Theorem 13.1–13.3) |
| $\kappa = -1$ (kinetic sign) | **Derived in Part II** | Required by ghost-freedom; $\kappa > 0$ produces negative kinetic energy in antisymmetric sector (Ch13 Theorem 13.3) |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | **Derived in Part II** | T1 scaling law + anchor $c(\rho_{\mathrm{GR}}) = 1$ (Ch14 Theorem 14.1) |
| $P(\Gamma)P(\Gamma)^T \propto I$ at attractor | **Derived in Part II** | Unique maximum of $\mathcal{C}(\Gamma) = \det(\Gamma)/(\|\Gamma\|_F^2/4)^2$ (Ch13 Theorem 13.2, Ch19 Lemma 19.1) |
| Lyapunov function for forced homeodynamics | **Derived in Part II** | $V(\Gamma,\dot\Gamma) = \|\dot\Gamma\|^2 + (1 - \mathcal{C}(\Gamma))^2$; Theorems 19.1–19.2 supersede T6 resolution here |

---

## 10.8 Closing the Tensions

| Tension | Status after Ch10 |
|---------|------------------|
| **T3** — form of $f$ | **Partially closed**: $f = -(M+A)\nabla P$ with $M = \Gamma_s^{-1}/\gamma$ (dissipative) and $A$ antisymmetric (reactive, postulated). $R\times\nabla_I P$ identified as the minimal G(3)-admissible realization of the postulated antisymmetric sector; $|I|^2 I$ from nonlinearity of $\nabla P$. Both structurally constrained by G(3) symmetry and the Onsager-Casimir decomposition. Coefficients $\alpha$, $\beta$, explicit $A(\rho,\xi)$ require $P(\Gamma)$. |
| **T6** — Lyapunov selection | **Closed**: $P(\xi)$ is the primary Lyapunov function. $V(\Gamma)$ is a local proxy; $V(\xi)$ is a diagnostic. |
| **T7** — derivation chain | **Structurally closed**: Lagrangian → $f$ (§10.3.2) → Lyapunov (§10.4) → Ch9 dynamics complete in structure. Coefficients pending explicit $P$. |

---

## 10.9 Open Questions

- **Explicit $P(\Gamma)$**: the structural potential is developed in Ch11 from G(3)-invariant polynomial constraints; this closes T3, fixes $\alpha_\mathbf{I}$ and $\beta_\mathbf{I}$, and determines $\gamma(\rho)$ up to an overall proportionality constant.

- **Inertial regime**: the overdamped limit is the working assumption of Part I. The full second-order (Euler-Lagrange) dynamics and their geometric interpretation are deferred to future work.

- **Position-dependent $\Gamma_s$**: the Christoffel correction $\frac{1}{2}(\nabla_\xi \Gamma_s)\dot{\xi}^2$ was dropped in the overdamped limit. In configurations where $\Gamma_s$ varies rapidly with $\xi$ (near structural bifurcations), this correction may be significant — it would modify $f$ with curvature-like terms in the $\Gamma$-space geometry.

- **Derivation of $\gamma(\rho)$**: the dissipation rate's $\rho$-dependence is estimated as $\gamma \sim \rho\|\Gamma_s\|$ (§10.7), but the proportionality constant requires the full Lagrangian. Its derivation is deferred to future work.

---

*End of Chapter 10*
