# Chapter 12: The Geometry of Coupling
*Condensed version — Part II*

---

## 12.1 The Shift: from Algebra to Geometry

Part I operated in attribute space $\mathcal{M}_\xi$ — the space of states $\xi = (S, A, \mathbf{I}, \mathbf{R})$. Part II operates directly in $\mathcal{M}(\Gamma)$ — the space of coupling matrices. The move reflects the shift from *declarative* (what the objects are) to *derivational* (why they must be as they are). Two open questions from Part I drive this chapter:

- **Q1 (Form).** $P(\Gamma)$ attractor left unspecified in Ch11.
- **Q2 (Dynamics).** Lagrangian coefficients $\kappa(\rho)$, $\mu(\rho)$ left as functions to determine.

---

## 12.2 The Configuration Manifold

**Definition 12.1 (Base manifold).**

$$\mathcal{M}(\Gamma) := \mathrm{GL}^+(4,\mathbb{R}) = \{\Gamma \in \mathrm{Mat}(4,\mathbb{R}) \mid \det(\Gamma) > 0\}$$

This equality is exact — not a subset relation.

**Definition 12.1a (Admissible manifold).**

$$\mathcal{M}_{\mathrm{adm}}(\Gamma) := \{\Gamma \in \mathcal{M}(\Gamma) \mid \Gamma_s \succ 0\}$$

$\mathcal{M}_{\mathrm{adm}}$ is a proper open subset of $\mathrm{GL}^+(4,\mathbb{R})$. "Configuration manifold" in Part II refers to $\mathcal{M}_{\mathrm{adm}}$ unless stated otherwise.

**Consequence 12.2 (Admissibility — derived from Ch5 Remark 5.1 + Ch10 Thm 10.1).** $\Gamma_s \succ 0$ follows from the requirement that $M = \Gamma_s^{-1}/\gamma \succ 0$ (Lyapunov dynamics). This is not an independent postulate. Configurations with $\Gamma_s \not\succ 0$ (tachyonic modes) are inadmissible at the classical level.

**Topology.** $\mathcal{M}(\Gamma)$ is an open dense subset of $\mathbb{R}^{16}$, connected. Precise homotopy groups (via polar decomposition retraction to SO(4)) deferred to Part III.

**Frobenius decomposition.** $\|\Gamma\|_F^2 = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2$ — orthogonal, exact (not an ansatz):

$$\mathcal{M}_{\mathrm{adm}}(\Gamma) \subset \mathrm{Sym}(4) \oplus \mathfrak{so}(4)$$

---

## 12.3 Null Intrinsic Attributes — Degeneracy and UoC Transformation

**Definition 12.2 (Null intrinsic attribute).** Attribute $X$ is null if $\kappa_X = \Gamma_{XX} = 0$ and $\gamma_{Xj} = 0$ for all $j \neq X$ (entire $X$-th row and column zero). Notation: $\kappa_X$ for self-coherence — distinct from $c$ (speed of light, Ch15).

**Proposition 12.1.** Null intrinsic attribute $\Rightarrow$ $\det(\Gamma) = 0$ $\Rightarrow$ UoC at $\partial\mathcal{M}(\Gamma)$.

**Interpretation.** A null attribute does not produce a special state of the *same* UoC — it destroys the UoC. What follows is a *different* entity, which may inherit surviving (non-null) attributes as initial conditions.

**Remark 12.2 (UoC inheritance).** Upon collapse of attribute $X$, the successor has initial coupling $\Gamma_{\mathrm{new}}(t=0) = \pi_{\hat{X}}(\Gamma_{\mathrm{old}})$.

**Remark 12.5 (Boundary stratification).** $\partial\mathcal{M}(\Gamma)$ is stratified by $\mathrm{rank}(\Gamma) \in \{0,1,2,3\}$. Rank-3 (one null attribute) is the generic boundary crossing. Full stratification belongs to Part III.

**Remark 12.3 (Jump admissibility).** Not every projection $\pi_{\hat{X}}(\Gamma_{\mathrm{old}})$ yields a stable successor. Admissibility requires the inherited $\Gamma_{\mathrm{new}}(t=0)$ to not immediately drive $\det(\Gamma_{\mathrm{new}}) \to 0$. Formal criterion requires Morse theory of $\mathcal{C}(\Gamma)$ on $\partial\mathcal{M}(\Gamma)$ — Part III.

### 12.3.1 Classification by Collapsing Attribute

| Null attribute | Destroyed | Successor inherits | Paradigmatic case |
|---|---|---|---|
| $S$ | Organizing center, self-identity | $\{A, \mathbf{I}, \mathbf{R}\}$ | Neutral plasma |
| $A$ | Agency, self-driven change | $\{S, \mathbf{I}, \mathbf{R}\}$ | Dead cell (retains form, no metabolism) |
| $\mathbf{I}$ | Internal field coherence | $\{S, A, \mathbf{R}\}$ | Ideal non-rotating gas |
| $\mathbf{R}$ | Environmental coupling | $\{S, A, \mathbf{I}\}$ | Thermodynamically isolated sub-system |

### 12.3.2 The EM Field in Vacuum

When charges are removed: both $S$ (charge density) and $A$ (current) collapse. The result is **not** a special state of the charged UoC — it is a *boundary configuration with inherited structural content* (not a full UoC by §0.3 criterion, which requires Force and Field simultaneously active).

$$\Gamma_{\mathrm{EM}} = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & \gamma_{IR} \\ 0 & 0 & -\gamma_{IR} & 0 \end{pmatrix}, \qquad \det = 0, \quad \mathrm{rank} = 2$$

Plane wave: $\mathbf{E}\cdot\mathbf{B} = 0 \Rightarrow \det(F_{\mu\nu}) = 0 \Rightarrow \mathrm{adj}(\Gamma) = 0 \Rightarrow \square F_{\mu\nu} = 0$ (Ch15).

### 12.3.3 Null Purpose — Three Routes

**Proposition 12.2.** Null purpose through exactly one of:
- *(i)* Null intrinsic attribute ($\det = 0$, UoC destroyed)
- *(ii)* Purely antisymmetric with vanishing Pfaffian ($\Gamma_s = 0$, $\mathrm{Pf}(\Gamma_a) = 0$) — the EM plane wave case
- *(iii)* $\mu(\rho) = 0$ — organizational level at which the purpose landscape flattens

In all three: $\mathcal{L} \to \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2$ (harmonic dynamics, no attractor).

**Remark 12.4 (Partial decoupling).** Attribute partially decoupled: $\kappa_X > 0$ but $\gamma_{Xj} = 0$ for $j \neq X$. Then $\det(\Gamma) = \kappa_X \cdot \det(\Gamma_{\hat{X}}) > 0$ — UoC survives, but $X$ is structurally inert. Distinct from null attribute.

### 12.3.4 Connection to Purpose Across Regimes (Ch11 §11.7b)

The boundary configurations described above are the regime in which $P(\Gamma)$ is *latent*: defined on $\overline{\mathcal{M}}(\Gamma)$, but with vanishing dynamical force because the adjugate term $\mathrm{adj}(\Gamma)^T$ is zero for $\mathrm{rank}(\Gamma) \leq 2$ (Lemma 15.1). When the boundary is crossed transversely by a coherent UoC that loses an attribute, $P$ does not vanish — it re-instantiates as the purpose of the successor, with $\Gamma^*_{\mathrm{new}}$ generally distinct from $\Gamma^*_{\mathrm{old}}$ (Ch11 §11.7b, generative role).

The same UoC therefore traverses three purpose regimes:
- **Active** ($\det\Gamma > 0$): $P$ drives the dynamics toward $\Gamma^*$;
- **Latent** ($\det\Gamma = 0$): $P$ is defined but inactive; the system propagates as wave regime (Ch15 §15.1);
- **Generative** (boundary crossing): $P$ re-instantiates as the successor's potential.

This unifies the apparent tension between "purpose as attractor" (active EOM) and "purpose at the boundary" (configurations with $\det\Gamma=0$ such as EM plane waves or rank-2 oscillators). Purpose is the *potential landscape across all regimes*; the regime determines whether and how it acts.

**Connection to Ch15 §15.1 (UoC vs regime, T8 reading (D)).** Rank-$\leq 2$ configurations describe **regimes** of UoCs, not new UoCs. The EM plane wave, the rank-2 mechanical oscillator, and the acoustic wave are regimes of underlying UoCs (charged source system, mass, fluid parcel) in which the source/agency attributes are momentarily inactive. The boundary stratification of $\partial\mathcal{M}(\Gamma)$ catalogues which regimes a UoC can occupy without losing its identity as that UoC; full crossing of the boundary (transition to a successor) is a distinct event from the rank reduction within $\overline{\mathcal{M}}$.

---

## 12.4 Organizational Level $\rho$ as Geometric Parameter

**Notation note.** $\rho$ = organizational level (GSF). Distinct from $\rho_m$ = mass density (physics). When both appear (Ch15), the physical density carries the subscript.

**Postulate 12.1 ($\rho$ as smooth parameter).** $\rho > 0$ indexes a family $\mathcal{M}(\Gamma; \rho)$. Frobenius metric and G(3)-symmetry are $\rho$-independent; only $\kappa(\rho)$, $\mu(\rho)$ depend on $\rho$.

This makes $\mathcal{M}_{\mathrm{adm}}$ a fiber bundle over $\mathbb{R}_{>0}$ with fiber $\cong \mathrm{GL}^+(4,\mathbb{R})$.

**Why $\rho^{-1}$ and not $\log\rho$ or $e^\rho$.** $\rho$-changes form a multiplicative group. Cauchy's functional equation restricts continuous solutions to power laws $\Gamma \propto \rho^\alpha$. The specific exponent $\alpha = -1$ is selected by EOM covariance — established in Ch14 Theorem 14.1.

---

## 12.5 Derivational Program of Part II

| Chapter | Task | Key constraint |
|---|---|---|
| Ch13 | Derive $\kappa = -1$, $\mu = 2/\sqrt{c(\rho)}$ | Frobenius isotropy + attractor self-consistency |
| Ch14 | Derive $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$, T1 scaling | Three independent structural requirements |
| Ch15–18 | Domain tests: physics, information, biology, water | Structural verification, not parameter fitting |
| Ch19 | Coherence $\mathcal{C}(\Gamma)$, Lyapunov, homeodynamics | AM-GM bound, Theorem 19.1–19.2 |
| Ch20–21 | Topology, inventory, derivability | $\pi_1(\mathcal{M}) = \mathbb{Z}_2$, what Part II did/did not derive |

---

## 12.6 Epistemic Note: Metric Signature

The Frobenius metric on $\mathcal{M}_{\mathrm{adm}}$ is **Riemannian** (positive-definite). GSF dynamics in Part II is Euclidean in configuration space — $t$ is a parametric evolution variable. Lorentzian signature (causal structure, light cones) emerges in Ch15 via the postulated extension $\partial_t^2 \to \square$, not from the Riemannian structure of $\mathcal{M}_{\mathrm{adm}}$. Whether Lorentzian signature can be derived from a pseudo-Riemannian structure on a larger manifold is open for Part III.

---

## Summary Table

| Object | Status |
|---|---|
| $\mathcal{M}(\Gamma) = \mathrm{GL}^+(4,\mathbb{R})$ | Definition (exact equality) |
| $\mathcal{M}_{\mathrm{adm}} \subset \mathcal{M}(\Gamma)$ | Definition + Consequence 12.2 ($\Gamma_s \succ 0$) |
| $\Gamma_s \succ 0$ justification | Structural: necessary for $P(\Gamma)$ bounded below |
| Homotopy of $\mathcal{M}(\Gamma)$ | Deferred to Part III |
| Null attribute $\Rightarrow$ det = 0 | Proved (Proposition 12.1) |
| Null attribute $\Rightarrow$ UoC destroyed | Interpretive layer (GSF) |
| EM vacuum as "boundary successor" | Not a full UoC; boundary configuration with inherited $\{\mathbf{I},\mathbf{R}\}$ |
| Purpose role across regimes (active / latent / generative) | Articulated in §12.3.4; full statement Ch11 §11.7b |
| Rank-$\leq 2$ as regime, not new UoC (T8 reading D) | Stated in Ch15 §15.1; consistent with §12.3.2 |
| Jump admissibility condition | Open — Part III (Morse theory of $\mathcal{C}$) |
| $\rho$ as conformal parameter | Postulate 12.1 — derived in Ch14 |
| Lorentzian signature | Postulated in Ch15, not derived from $\mathcal{M}_{\mathrm{adm}}$ |

---

*Part I declared the grammar. Ch12 defines the space in which grammar evolves. Ch13 derives the law of evolution.*
