# Chapter 18: Postulate and Ansatz Status — What Part II Closed

*A retrospective inventory: which structural assumptions have been derived, which remain postulated, and which have been partially constrained by physical evidence.*

---

## 18.1 Purpose

Part I opened with a set of structural assumptions — postulates about the form of the Lagrangian, the scaling of $\Gamma$ with $\rho$, and the behavior of the damping parameter $\gamma$. Part II either derived these from more fundamental requirements or exposed them as genuine residual freedom. This chapter gives the definitive status of each, organized by outcome.

The complete bitácora is in brainstorming/bitacora_postulados.md (postulates) and brainstorming/bitacora_ansatz.md (ansatz). This chapter gives the structured summary with precise references.

---

## 18.2 Closed by Derivation — No Longer Postulates

These claims were postulated in Part I and have been derived in Part II without additional assumptions.

### 18.2.1 The Structural Lagrangian (Ch13 Theorems 13.1–13.4)

**Was postulated:** a Lagrangian of the form $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu\det(\Gamma)$ was presented in Ch10 as a "minimal canonical choice" with undetermined coefficients.

**Now derived:** given (i) G(3)-invariance and parity, (ii) Frobenius as the unique isotropic kinetic term, (iii) the attractor self-consistency condition, and (iv) ghost-freedom, the Lagrangian is the unique form at minimal polynomial order. Zero free parameters given $\rho_{\mathrm{GR}}$.

| Coefficient | Status | Derivation |
|---|---|---|
| Kinetic = $\|\dot\Gamma\|_F^2$ | Derived | Frobenius uniqueness under isotropy condition (Theorem 13.1) |
| Potential = $-\|\Gamma\|_F^2$ | Derived | Normalization + potential sign convention (Ch13 §13.3) |
| $\kappa = -1$ | Derived | Ghost-freedom + Frobenius (Corollary 13.1) |
| $\mu(\rho) = 2/\sqrt{c(\rho)}$ | Derived | Attractor self-consistency (Theorem 13.2) |
| $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ | Derived | T1 scaling law + anchor $c(\rho_{\mathrm{GR}})=1$ (Ch14) |

### 18.2.2 The Scaling Law T1 (Ch14 Theorem 14.1)

**Was postulated:** that $\Gamma$ scales with $\rho$ was assumed without derivation in Part I.

**Now derived:** the unique continuous solution to the group composition requirement (Cauchy functional equation, Lemma 14.1) is $\Gamma(\rho) = \Gamma_0/\rho$. The form (power law) is necessary, not optional. The exponent $\alpha = -1$ is selected by C2 (coordination cost, $\alpha < 0$) and C3 (minimal invariant section, Lemma 14.2).

### 18.2.3 Admissibility Condition $\Gamma_s \succ 0$ (Ch12 Consequence 12.2)

**Was postulated:** $\Gamma_s \succ 0$ appeared as a requirement in Ch5 without derivation.

**Now derived:** $M = \Gamma_s^{-1}/\gamma \succ 0$ is required for the Lyapunov dynamics (Ch10 Theorem 10.1). This forces $\Gamma_s \succ 0$. The postulate is a consequence of the stability requirement.

### 18.2.4 C4 — Γ-Factorization of the Purpose Function (Ch11 Proposition 11.0)

**Was postulated:** that $P = P(\Gamma)$ (the purpose depends on $\xi$ only through $\Gamma(\xi)$).

**Now derived:** the orbit map $\xi \to \Gamma(\xi)$ of G(3) on $V$ (Ch8 §8.3) and G(3)-invariance of $P$ jointly force $P$ to be constant on orbits, hence $P = \tilde{P} \circ \Gamma$. C4 follows from C1.

### 18.2.5 Null Attribute → System Collapse (Ch12 Proposition 12.1)

**Was assumed:** that losing an attribute destroys the UoC.

**Now derived:** null attribute $\Rightarrow$ entire row/column of $\Gamma$ zero $\Rightarrow$ $\det(\Gamma)=0$ $\Rightarrow$ system on $\partial\mathcal{M}(\Gamma)$ $\Rightarrow$ no attractor $P(\Gamma)$ exists. The "destruction" is the algebraic consequence of the viability condition, not a separate assumption.

---

## 18.3 Closed by Physical Correspondence — Domain-Specific Derivations

These were structural predictions verified against known physical equations in Ch15–17.

### 18.3.1 Massless Graviton (Ch15 Theorem 15.3)

**Was assumed:** the graviton is massless (standard GR).

**Now derived within GSF:** at $\rho = \rho_{\mathrm{GR}}$, $\mu(\rho_{\mathrm{GR}}) = 2$ (from T1 + anchor). The mass term for the gravitational perturbation is $m_h^2 = 2 - \mu = 0$ exactly. Masslessness is an algebraic consequence of the anchor choice, not an independent postulate.

### 18.3.2 Photon and Phonon Masslessness (Ch15 Theorems 15.2, 15.4)

**Was assumed:** photons and acoustic phonons propagate without mass.

**Now derived:** both are connections (gauge potentials) in the antisymmetric sector of $\Gamma$. The variational principle applied to the potential $A$ (not to $F=dA$ directly) gives the massless wave equation $\square A = 0$. Masslessness is a representation-theoretic consequence, not imposed.

### 18.3.3 Stokes Flow as Overdamped GSF (Ch15 Theorem 15.5)

**Was an ansatz (A4):** $\gamma \sim \rho\|\Gamma_s\|$ was phenomenological.

**Now partially derived:** the Stokes limit ($\gamma \gg 1$, Re $\to 0$) of the GSF EOM gives $\partial_t v_i = \nu_{\mathrm{kin}}\nabla^2 v_i$ with $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$. This operationalizes $\gamma$ for the fluid domain: $\gamma = c^2(\rho)/\nu_{\mathrm{kin}}$. The ratio $\gamma_A/\gamma_B = \nu_B/\nu_A$ is testable from viscosity tables — the first quantitative constraint on A4.

---

## 18.4 Remaining Postulates — Genuine Residual Freedom

These have not been derived and represent the true structural freedom of the GSF.

### 18.4.1 The Four-Attribute Structure $\{S, A, \mathbf{I}, \mathbf{R}\}$

**Why four:** Cayley-Hamilton for $4\times4$ matrices gives exactly one independent quartic invariant ($\det$). Any smaller matrix lacks this invariant; any larger matrix is not minimal. So $n=4$ is structurally necessary.

**Why these four:** the assignment of physical or biological content to the four slots is domain-specific input, not derived from the Lagrangian. The Lagrangian operates on $\Gamma$ without knowing whether $S$ is "charge" or "oxygen nucleus." This is vulnerability F3 of Ch19.

### 18.4.2 The Isotropy Condition $a = b$ (Ansatz A5)

**Status:** structural postulate — the weakest additional assumption sufficient to select the Frobenius kinetic term uniquely from the two-parameter family $a\|\dot\Gamma_s\|_F^2 + b\|\dot\Gamma_a\|_F^2$.

**First test path (from Ch15 §15.8c and Ch16 §16.3):** water is the first domain where $\Gamma_s \neq 0$ and $\Gamma_a \neq 0$ are simultaneously active. The relaxation timescales suggest $a \neq b$ for biological fluids (see Ch13 §13.4 update note). Ultrafast spectroscopy of water (or MD simulations) can test this directly. If $a \neq b$, the minimal Lagrangian requires domain-specific corrections for biological systems.

### 18.4.3 The Field-Theoretic Extension $\partial_t^2 \to \square$ (Ansatz A6)

**Status:** postulated — the spatial gradient term $c^2\|\nabla\Gamma\|_F^2$ in the field Lagrangian is introduced by analogy with relativistic field theory, not derived from the fiber bundle geometry of $\mathcal{M}(\Gamma;\rho)$ over spacetime.

**What is derived:** the coefficient $c^2 = c^2(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ from T1 (Ch14) and the anchor $c(\rho_{\mathrm{GR}}) = 1$. So once the lifting is accepted, the coefficient is fixed. The lifting itself — why the base manifold is Lorentzian and not Riemannian — is Part III.

### 18.4.4 The Sector-Decoupling Assumption (Ansatz A2)

**Status:** structural postulate — mixed invariants like $\mathrm{tr}(\Gamma_s^2\Gamma_a^2)$ are excluded from the Lagrangian basis by assumption (not by the symmetry group alone).

**Plausible derivation route:** the $(1\oplus 3)$ decomposition of attribute space (S scalar, $\{A,\mathbf{I},\mathbf{R}\}$ vectors in G(3)) may force the sectors to decouple in the irreducible representation of G(3). Not yet derived.

### 18.4.5 The Absolute Scale of $\rho$ (Hito 3)

**Status:** open. T1 establishes the relative hierarchy ($\rho_{\mathrm{quantum}} \ll \rho_{\mathrm{GR}} \ll \rho_{\mathrm{biol}}$) and fixes the functional form $c(\rho)$, but the absolute correspondence between $\rho$ and physical units (meters, Planck scale, eV) requires the stratum bridge. All quantitative predictions depending on absolute $\rho$ values are blocked until Hito 3.

---

## 18.5 Ansatz Status Summary

| Ansatz | Description | Status after Part II | Test path |
|---|---|---|---|
| A1 — Minimal EOM ansatz | Ch9 nonlinear evolution form | **Closed** — Ch13 derives exact form | ✓ |
| A2 — Sector-decoupling | No mixed $\Gamma_s^2\Gamma_a^2$ invariants | Active postulate | G(3) irreducible decomp. (Part III) |
| A3 — $G_\Gamma \propto \Gamma_s^{-1}$ | Metric closure on $\Gamma$-space | Active — requires parameterization | Part III |
| A4 — $\gamma \sim \rho\|\Gamma_s\|$ | Damping scaling | **Partially constrained**: $\gamma = c^2/\nu_{\mathrm{kin}}$ for fluids | Viscosity ratios (testable now) |
| A5 — Isotropy $a = b$ | Equal sector weights in kinetic term | Active — first test path via water | Ultrafast spectroscopy / MD |
| A6 — $\partial_t^2 \to \square$ | Covariant field lifting | Active — coefficient fixed by T1 | Bundle geometry (Part III) |
| A7 — $\Gamma_a = dA$ | Antisymmetric sector as curvature | Active — consistent, not derived | Bundle geometry (Part III) |
| A8 — Power-law scaling T1 | Form of $\Gamma(\rho)$ | **Closed** — Cauchy functional equation | ✓ |

---

## 18.6 The Core Remaining Debt

Part II leaves two genuinely open structural questions that are not resolvable by more algebra within the current framework:

**Question 1 — Slot assignment uniqueness (F3).** Is the mapping from physical observables to GSF slots ($S \leftrightarrow$ charge, $\mathbf{I} \leftrightarrow$ electric field, etc.) uniquely forced by Conditions C1–C3, or are there multiple admissible assignments that give structurally indistinguishable predictions? If multiple assignments exist, the GSF domain reductions are formally convenient but not physically unique.

**Question 2 — Lorentzian extension.** The GSF Lagrangian lives on $\mathcal{M}_{\mathrm{adm}}(\Gamma)$ with Euclidean (Riemannian) signature. Physical spacetime is Lorentzian. The Lorentzian extension — establishing that the base manifold has causal structure, that the Frobenius ghost-freedom carries over, and that the full nonlinear GR emerges from the nonlinear EOM — is the central technical task of Part III.

Both questions are addressed in Ch19.

---

*Part II began with a Lagrangian and derived equations that reproduce five physical theories. It ends with a precise account of what was derived (§18.2–18.3), what was constrained (§18.4, §18.5), and what remains open (§18.6). The ratio of derived to postulated content has improved substantially. The remaining postulates are fewer, more precisely stated, and each has an identified derivation route or empirical test.*
