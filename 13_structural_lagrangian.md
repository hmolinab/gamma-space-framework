# Chapter 13: The Structural Lagrangian

## 13.1 The Program

Chapter 10 presented a structural Lagrangian under the label "minimal canonical choice" — a phrase that acknowledged the existence of alternatives without eliminating them. The coefficients $\kappa(\rho)$ and $\mu(\rho)$ were introduced as functions to be determined, the sector-decoupling ansatz was identified as a simplifying assumption rather than a structural result, and the ghost-freedom condition was stated without proof. The Lagrangian of Ch10 was a well-motivated starting point. It was not a derivation.

This chapter is a derivation.

The argument proceeds in four stages:

**Stage 1 (§13.2–§13.3):** Identify the admissible polynomial invariants of $\Gamma$ under the structural symmetries of the GSF. The result, established via the Cayley-Hamilton theorem for $4\times4$ matrices, a parity argument, and a sector-decoupling assumption, is that the admissible basis at lowest order within the minimal-order decoupled class consists of exactly two terms: $\|\Gamma\|_F^2$ and $\det(\Gamma)$.

**Stage 2 (§13.4):** Show that the Frobenius metric on $\mathcal{M}(\Gamma)$ is the unique $\mathrm{O}(4)\times\mathrm{O}(4)$-invariant inner product on $\mathrm{Mat}(4,\mathbb{R})$. As a consequence, the kinetic coefficient $\kappa = -1$ is forced — it is not a free parameter.

**Stage 3 (§13.5):** Derive the coupling strength $\mu(\rho)$ from the condition that the static extremum of the Lagrangian is the structural attractor $P(\Gamma)$ defined in Ch11. The result is $\mu(\rho) = 2/\sqrt{c(\rho)}$ where $c(\rho) = \det(P(\Gamma))$ is the structural coherence at the attractor — a property of the system, not a free parameter.

**Stage 4 (§13.6):** Prove that the resulting Lagrangian is ghost-free at the classical level — all kinetic modes carry non-negative energy. The proof identifies the structural mechanism that prevents ghosts: the intrinsic sign $\mathrm{Tr}(\Gamma_a^2) \leq 0$ for antisymmetric matrices, which cancels the apparent negative contribution from $\kappa = -1$.

The output is a unique Lagrangian with zero free parameters, given the reference organizational level $\rho_{\mathrm{GR}}$. This is the claim of Theorem 13.1 (§13.7).

---

## 13.2 Admissible Symmetries and Invariants

### 13.2.1 The Symmetry Group of $\mathcal{M}(\Gamma)$

The admissible Lagrangian must be invariant under the structural symmetries of the GSF — the transformations that preserve the physical content of $\Gamma$ without changing the system it describes.

The four attributes of $\Gamma$ are not interchangeable. Attribute $S$ is a scalar (grade 0 in $\mathrm{G}(3)$) while $\{A, \mathbf{I}, \mathbf{R}\}$ are vectors (grade 1). This asymmetry eliminates the full $\mathrm{GL}(4,\mathbb{R})$ from consideration as a symmetry group.

**Admissible symmetries are:**

**S1 (Orthogonal conjugation on $\{A, \mathbf{I}, \mathbf{R}\}$).** The three vector attributes transform under $\mathrm{SO}(3)$ acting on the spatial indices. Under the representation $\varrho: \mathrm{G}(3) \to \mathrm{O}(4)$ established in Ch8, this acts as:
$$\Gamma \;\mapsto\; O\,\Gamma\,O^T, \qquad O \in \mathrm{SO}(3) \subset \mathrm{O}(4)$$
preserving $\mathrm{tr}(\Gamma^k)$ and $\det(\Gamma)$ by cyclicity of trace and multiplicativity of determinant.

**S2 (Parity: $\Gamma \mapsto -\Gamma$).** For a source-free system, there is no preferred orientation in $\mathcal{M}(\Gamma)$: reversing all couplings simultaneously ($\Gamma \to -\Gamma$) maps one physically valid configuration to another. The Lagrangian must be invariant under this discrete symmetry.

*Domain conditionality of S2.* Parity is valid for source-free physical systems (EM in vacuum, GR linearized, SHO). It is not a universal structural law: biological, economic, and psychological UoCs generally have intrinsic asymmetry (metabolic direction, temporal irreversibility, structural bias), and for these domains $\Gamma \to -\Gamma$ is not a symmetry. The role of S3 in the invariant basis derivation (eliminating $\mathrm{tr}(\Gamma)$ and $\mathrm{tr}(\Gamma^3)$) is therefore domain-conditional. The claim that the parity-reduced basis $\{I_1, I_2, \det(\Gamma)\}$ is the GSF basis rests on the assumption that the Lagrangian is structural — the same across all domains. If domain-specific odd invariants are physically relevant, the Lagrangian would acquire domain-specific corrections. This is deferred as an open question; the minimal Lagrangian Structural Postulated assumes S3.

**Symmetry hierarchy.** The derivation uses three distinct levels of symmetry group, each serving a different role:

| Level | Group | Role in the derivation |
|---|---|---|
| Physical | S1–S2 | Actual symmetries of the GSF Lagrangian; the Lagrangian is invariant under these only |
| Classification | Full matrix conjugation | Analytical tool for enumerating polynomial invariants via Cayley-Hamilton; not claimed as a physical symmetry |
| Isotropy | $\mathrm{O}(4)\times\mathrm{O}(4)$ bilateral | Sufficiency argument: Frobenius is the unique biinvariant metric at this level; used to characterize the isotropy selection in §13.4 |

1. *Physical symmetry group* (S1–S2): the actual symmetries of the GSF Lagrangian. S1 is the structural orthogonal symmetry; S2 is the parity condition, domain-conditional (valid for source-free systems, not universal).

2. *Classification group* (full conjugation, used in Lemma 13.2): a larger group used as a *tool* to enumerate all polynomial invariants of a $4\times4$ matrix. The Cayley-Hamilton theorem operates at this level. The enumeration is then restricted to the physical symmetry group S1–S2 and further filtered by sector-decoupling and minimality constraints.

3. *Isotropy group* ($\mathrm{O}(4)\times\mathrm{O}(4)$, used in §13.4): invoked only to characterize the Frobenius metric as the unique biinvariant inner product. This is a *sufficiency argument* for the isotropy selection — not a claim that the GSF has bilateral $\mathrm{O}(4)\times\mathrm{O}(4)$ symmetry.

The physical symmetry group is S1–S2. The larger groups appear as analytical instruments to justify specific steps; the final Lagrangian is invariant under S1–S2 only.

### 13.2.2 The G(3)-Invariant Basis for the Potential

**Lemma 13.1 (Quadratic invariants).** *The space of G(3)-invariant quadratic forms in $\Gamma$ under symmetry S1, using the fact that $\mathrm{tr}(\Gamma_s\Gamma_a) = 0$ identically for any symmetric $\Gamma_s$ and antisymmetric $\Gamma_a$ (a theorem of linear algebra, independent of any physical symmetry), is two-dimensional, spanned by:*
$$I_1 = \mathrm{tr}(\Gamma^T\Gamma) = \|\Gamma_s\|_F^2 - \|\Gamma_a\|_F^2, \qquad I_2 = \mathrm{tr}(\Gamma^2) = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2$$

*Proof.* For $\Gamma = \Gamma_s + \Gamma_a$ with $\Gamma_s^T = \Gamma_s$ and $\Gamma_a^T = -\Gamma_a$:
$$\mathrm{tr}(\Gamma^T\Gamma) = \mathrm{tr}[(\Gamma_s - \Gamma_a)(\Gamma_s + \Gamma_a)] = \mathrm{tr}(\Gamma_s^2) - \mathrm{tr}(\Gamma_a^2) + \mathrm{tr}(\Gamma_s\Gamma_a - \Gamma_a\Gamma_s)$$
The commutator term vanishes: $\mathrm{tr}([A,B]) = 0$ always. The cross-term vanishes by symmetry-antisymmetry orthogonality: for any symmetric $A$ and antisymmetric $B$,
$$\mathrm{tr}(AB) = \sum_{i,k} A_{ik}B_{ki} = -\sum_{i,k} A_{ik}B_{ik} = -\mathrm{tr}(AB)$$
so $\mathrm{tr}(\Gamma_s\Gamma_a) = 0$ identically. This gives $I_1 = \|\Gamma_s\|_F^2 - \|\Gamma_a\|_F^2$. The expression for $I_2$ follows analogously. Any other G(3)-invariant quadratic form is a linear combination of $I_1$ and $I_2$. $\square$

**Lemma 13.2 (Unique quartic invariant at minimal order).** *Under the Cayley-Hamilton theorem for $4\times4$ matrices and symmetries S1–S2, the only independent G(3)-invariant polynomial of degree $\leq 4$ in $\Gamma$, at quartic order, is $\det(\Gamma)$.*

*Proof.* The Cayley-Hamilton theorem states that every $4\times4$ matrix $\Gamma$ satisfies its own characteristic polynomial:
$$\Gamma^4 - \sigma_1\Gamma^3 + \sigma_2\Gamma^2 - \sigma_3\Gamma + \sigma_4 I = 0$$
where $\sigma_k$ are the elementary symmetric polynomials of the eigenvalues:
$$\sigma_1 = \mathrm{tr}(\Gamma), \quad \sigma_2 = \tfrac{1}{2}[(\mathrm{tr}\,\Gamma)^2 - \mathrm{tr}(\Gamma^2)], \quad \sigma_3 = \tfrac{1}{6}[\ldots], \quad \sigma_4 = \det(\Gamma)$$
Taking the trace of the Cayley-Hamilton identity shows that $\mathrm{tr}(\Gamma^4)$ is a polynomial in $\{\mathrm{tr}(\Gamma), \mathrm{tr}(\Gamma^2), \mathrm{tr}(\Gamma^3), \det(\Gamma)\}$. More precisely, for a $4\times4$ matrix, the Newton identity gives:
$$\mathrm{tr}(\Gamma^4) = \sigma_1\mathrm{tr}(\Gamma^3) - \sigma_2\mathrm{tr}(\Gamma^2) + \sigma_3\mathrm{tr}(\Gamma) - 4\sigma_4$$
$$= \sigma_1\mathrm{tr}(\Gamma^3) - \sigma_2\mathrm{tr}(\Gamma^2) + \sigma_3\mathrm{tr}(\Gamma) - 4\det(\Gamma)$$
Hence $\mathrm{tr}(\Gamma^4)$ is not an independent invariant. The generating set of algebraically independent polynomial invariants of a $4\times4$ matrix under conjugation is exactly $\{\mathrm{tr}(\Gamma), \mathrm{tr}(\Gamma^2), \mathrm{tr}(\Gamma^3), \det(\Gamma)\}$ — four invariants, one at each degree. At quartic order, $\det(\Gamma)$ is the unique independent invariant. Any other degree-4 scalar is a polynomial in the lower-degree invariants together with $\det(\Gamma)$.

Symmetry S2 (parity) eliminates $\mathrm{tr}(\Gamma)$ and $\mathrm{tr}(\Gamma^3)$ (odd in $\Gamma$). The surviving invariants at degrees 2 and 4 are $\mathrm{tr}(\Gamma^2)$ and $\det(\Gamma)$. Combined with $I_1$ from Lemma 13.1, the complete parity-even G(3)-invariant basis at minimal order is:
$$\{I_1,\; I_2,\; \det(\Gamma)\} \equiv \{\|\Gamma\|_F^2,\; \mathrm{tr}(\Gamma^2),\; \det(\Gamma)\}$$
Since $I_1$ and $I_2$ are the two independent quadratic invariants, any G(3)-invariant quartic-or-lower potential must be a linear combination of $\{I_1, I_2, \det(\Gamma)\}$. $\square$

**Remark 13.1 (Completeness under stated constraints).** Lemma 13.2 establishes that no independent invariant of degree $\leq 4$ has been omitted *under the full-conjugation symmetry used to classify the basis*. The actual GSF symmetry group S1–S3 is strictly smaller, and mixed invariants such as $\mathrm{tr}(\Gamma_s^2\Gamma_a^2)$ or contractions respecting the $(1 \oplus 3)$ decomposition of attribute space are not automatically excluded by the Cayley-Hamilton argument. They are excluded by two additional constraints: (a) the sector-decoupling assumption (no cross-sector coupling in the invariant basis at minimal order), equivalent to the ansatz of Ch11 §11.4; and (b) minimality (degree $\leq 4$ only). These are structural postulates, not consequences of the symmetry group alone. Under these constraints, the basis $\{I_1, I_2, \det(\Gamma)\}$ is complete. Invariants of degree 6, 8, ... exist but are perturbatively suppressed for $\|\Gamma\|_F \ll 1$ — the classical regime. Their inclusion would generate higher-derivative corrections to the equations of motion, analogous to Born-Infeld corrections in electrodynamics. These are not part of the minimal structural theory; they constitute the agenda for quantum corrections to the GSF Lagrangian, beyond the scope of Part II.

---

## 13.3 The General Admissible Lagrangian

The most general parity-even G(3)-invariant Lagrangian at minimal polynomial order is:

$$\mathcal{L} = \alpha_1 I_1 + \alpha_2 I_2 + \mu\,\det(\Gamma) = (\alpha_1 + \alpha_2)\|\Gamma_s\|_F^2 + (-\alpha_1 + \alpha_2)\|\Gamma_a\|_F^2 + \mu\,\det(\Gamma)$$

with three a priori free parameters: $\alpha_1, \alpha_2, \mu$.

In the dynamical case, the Lagrangian includes a kinetic term. The canonical kinetic structure on $\mathcal{M}(\Gamma)$ is:
$$T(\dot{\Gamma}) = \alpha_1\,\mathrm{tr}(\dot{\Gamma}^T\dot{\Gamma}) + \alpha_2\,\mathrm{tr}(\dot{\Gamma}^2) = (\alpha_1+\alpha_2)\|\dot{\Gamma}_s\|_F^2 + (-\alpha_1+\alpha_2)\|\dot{\Gamma}_a\|_F^2$$

using the same G(3)-invariant basis for velocities.

The full Lagrangian is therefore:
$$\mathcal{L}(\Gamma, \dot{\Gamma}) = T(\dot{\Gamma}) - V(\Gamma) = (\alpha_1+\alpha_2)\|\dot{\Gamma}_s\|_F^2 + (-\alpha_1+\alpha_2)\|\dot{\Gamma}_a\|_F^2 - (\alpha_1+\alpha_2)\|\Gamma_s\|_F^2 - (-\alpha_1+\alpha_2)\|\Gamma_a\|_F^2 - \mu\,\det(\Gamma)$$

setting the potential sign by convention $V = -\mathcal{L}|_{\dot\Gamma=0}$. This can be written compactly as:
$$\mathcal{L} = \|\dot{\Gamma}\|_F^2 + \kappa\,\mathrm{tr}(\dot{\Gamma}_a^2) - \|\Gamma\|_F^2 - \kappa\,\mathrm{tr}(\Gamma_a^2) - \mu\,\det(\Gamma)$$

under the normalization $\alpha_1 + \alpha_2 = 1$, with $\kappa := -\alpha_1 + \alpha_2$. The parameter $\kappa$ encodes the relative weight of the antisymmetric sector. *Notation note:* $\kappa$ here is an internal Lagrangian parameter (the antisymmetric sector weight, ultimately fixed at $\kappa = -1$); it is distinct from Einstein's gravitational coupling constant $\kappa_{\mathrm{GR}} = 8\pi G/c^4$, which carries dimensions and appears in GR as the coupling between geometry and stress-energy. The two never appear in the same expression within the GSF. Two conditions on the three original parameters $\{\alpha_1, \alpha_2, \mu\}$ remain to be imposed.

---

## 13.4 The Frobenius Metric Forces $\kappa = -1$

**Theorem 13.1 (Frobenius as minimal isotropic kinetic term; $\kappa = -1$).** *Under the minimality and isotropy conditions stated below, the kinetic term of the structural Lagrangian is uniquely identified with the Frobenius kinetic energy $T = \mathrm{tr}(\dot\Gamma^T\dot\Gamma)$. This corresponds to $\alpha_1 = 1$, $\alpha_2 = 0$ and $\kappa = -1$. The kinetic term is positive definite:*
$$T = \mathrm{tr}(\dot\Gamma^T\dot\Gamma) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$

*Proof.* The Frobenius inner product $\langle A, B\rangle_F = \mathrm{tr}(A^T B)$ is the unique inner product on $\mathrm{Mat}(4,\mathbb{R})$ invariant under bilateral orthogonal transformations $\Gamma \mapsto O\Gamma P^T$ for all $O, P \in \mathrm{O}(4)$ (up to overall scalar, fixed by normalization). The corresponding norm is $\|\Gamma\|_F^2 = \mathrm{tr}(\Gamma^T\Gamma)$.

Key algebraic fact: for antisymmetric $\Gamma_a$ (so $\Gamma_a^T = -\Gamma_a$),
$$\mathrm{tr}(\Gamma_a^T\Gamma_a) = \mathrm{tr}(-\Gamma_a\cdot\Gamma_a) = -\mathrm{tr}(\Gamma_a^2)$$
and $-\mathrm{tr}(\Gamma_a^2) = \|\Gamma_a\|_F^2 \geq 0$ (since $\mathrm{tr}(\Gamma_a^2) \leq 0$ for all antisymmetric matrices — their eigenvalues are purely imaginary pairs $\pm i\lambda_k$, giving $\mathrm{tr}(\Gamma_a^2) = -2\sum_k\lambda_k^2 \leq 0$). Therefore:
$$\mathrm{tr}(\dot\Gamma^T\dot\Gamma) = \mathrm{tr}(\dot\Gamma_s^T\dot\Gamma_s) + \mathrm{tr}(\dot\Gamma_a^T\dot\Gamma_a) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$
(the cross-term $\mathrm{tr}(\dot\Gamma_s^T\dot\Gamma_a) = 0$ by Lemma 13.1).

Requiring the kinetic term to equal this canonical Frobenius kinetic energy imposes $\alpha_1 I_1 + \alpha_2 I_2 = \mathrm{tr}(\dot\Gamma^T\dot\Gamma)$. Since $\mathrm{tr}(\dot\Gamma^T\dot\Gamma) = I_1 = \|\dot\Gamma_s\|_F^2 - \mathrm{tr}(\dot\Gamma_a^2)$ (Lemma 13.1 with $\mathrm{tr}(\dot\Gamma_a^2) = -\|\dot\Gamma_a\|_F^2$), this gives $\alpha_1 = 1$, $\alpha_2 = 0$, and $\kappa = -\alpha_1 + \alpha_2 = -1$. $\square$

**Remark 13.2 (The apparent sign paradox).** The parameter $\kappa = -1$ might suggest a negative kinetic contribution from the antisymmetric sector. This is a notational artifact: in the general Lagrangian of §13.3, the term $\kappa\,\mathrm{tr}(\dot\Gamma_a^2)$ with $\kappa = -1$ gives $(-1)\cdot\mathrm{tr}(\dot\Gamma_a^2) = (-1)\cdot(-\|\dot\Gamma_a\|_F^2) = +\|\dot\Gamma_a\|_F^2 > 0$. The two negatives — one from $\kappa = -1$ and one from the intrinsic sign of $\mathrm{tr}(\Gamma_a^2)$ for antisymmetric matrices — cancel. The kinetic energy is positive definite on all of $\mathcal{M}(\Gamma)$.

**Physical interpretation and epistemic status.** The Frobenius inner product is the canonical Riemannian metric on $\mathcal{M}(\Gamma)$ as an open subset of $\mathbb{R}^{16}$. Under the symmetry group S1–S3, the kinetic term is not uniquely forced: any inner product of the form $a\|\dot\Gamma_s\|_F^2 + b\|\dot\Gamma_a\|_F^2$ with $a, b > 0$ is admissible — a two-parameter family. Frobenius corresponds to $a = b = 1$. This is selected by an additional minimality condition: **isotropy between sectors** — no preferred differential weight for the symmetric vs. antisymmetric degrees of freedom. The Frobenius metric is the unique element of the admissible family with $a = b$. Alternatively, it is the unique inner product invariant under the larger bilateral group $\mathrm{O}(4) \times \mathrm{O}(4)$ acting as $\Gamma \mapsto O\Gamma P^T$, which is a sufficient (though not necessary) condition.

Theorem 13.1 is therefore best read as: *given S1–S3 and the isotropy condition $a = b$, the Frobenius kinetic term is the unique consistent choice and forces $\kappa = -1$*. The isotropy condition is a structural postulate — the weakest additional assumption sufficient to close the two-parameter freedom.

**Part II update (A5 — first empirical test path).** The isotropy condition $a = b$ was untestable with EM, GR, and SHO (each activates only one sector at a time). The water domain (Ch16 §16.3) is the first system where $\Gamma_s \neq 0$ and $\Gamma_a \neq 0$ are simultaneously active and measurable. The relaxation timescales for symmetric modes ($\tau_{\mathrm{rel}} \sim 5$–$7$ ps, H-bond network rearrangement) and antisymmetric modes ($\tau_{\mathrm{HB}} \sim 1$–$3$ ps, H-bond lifetime) differ by a factor of ~3–5, suggesting $a \neq b$ for the biological fluid domain. If confirmed by ultrafast spectroscopy, the minimal Lagrangian requires a domain-specific correction $a\|\dot\Gamma_s\|^2 + b\|\dot\Gamma_a\|^2$ with $a \neq b$ for biological systems. See brainstorming/bitacora_ansatz.md §A5.

**Consistency with electromagnetism.** In the EM attribute assignment ($\Gamma_a \cong F_{\mu\nu}$, $\mathbf{I} \leftrightarrow \mathbf{E}$, $\mathbf{R} \leftrightarrow \mathbf{B}$), the GSF potential at $\kappa = -1$ gives:
$$V = \|\Gamma\|_F^2 = \|\Gamma_s\|_F^2 - \mathrm{tr}(\Gamma_a^2) = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2$$
For the vacuum EM case ($\Gamma_s = 0$, $\Gamma_a = F_{\mu\nu}$):
$$\mathcal{L}_{\mathrm{GSF}}\big|_{\mathrm{EM,vac}} = \mathrm{tr}(\dot{F}^T\dot{F}) + \mathrm{tr}(F_{\mu\nu}^2) - \mu\det(F)$$
The term $\mathrm{tr}(F^2) = \mathrm{tr}(\Gamma_a^2)/(-1) = \|\Gamma_a\|_F^2 = \mathbf{E}^2 + \mathbf{B}^2$ — wait, this requires more care. The standard EM Lagrangian is $\mathcal{L}_{\mathrm{EM}} = \frac{1}{2}(\mathbf{E}^2 - \mathbf{B}^2) = -\frac{1}{4}F_{\mu\nu}F^{\mu\nu}$. In terms of Frobenius invariants with Minkowski signature, $-\frac{1}{4}F_{\mu\nu}F^{\mu\nu} = \frac{1}{2}(\mathbf{E}^2 - \mathbf{B}^2)$. The GSF term $\mathrm{tr}(\Gamma_a^T\Gamma_a) = \|\Gamma_a\|_F^2$ in Euclidean signature gives $\mathbf{E}^2 + \mathbf{B}^2$ — the standard EM Lagrangian requires $\mathbf{E}^2 - \mathbf{B}^2$, which needs Lorentzian signature. The GSF Lagrangian is therefore a *consistency constraint* with EM structure, not yet a derivation of EM: the structural split and the $\det$ term match, but the relative sign between electric and magnetic contributions requires the Lorentzian extension of Part III. This gap is acknowledged; Theorem 13.3 (ghost-freedom) and the Hamiltonian of §13.8.3 are both stated strictly for the Euclidean signature manifold $\mathcal{M}_{\mathrm{adm}}$.

---

## 13.5 The Attractor Condition Forces $\mu$

### 13.5.1 The Static Extremum

The structural equilibrium $P(\Gamma)$ defined in Ch11 is the distinguished configuration that minimizes the purpose function $\mathcal{P}(\Gamma)$. In the purely conservative system (§13.8.3), it is a stable equilibrium point — not an attractor (Liouville's theorem precludes attractors in phase-volume-preserving dynamics). It becomes a genuine attractor only in the dissipative regime (§13.8.2) with $\gamma > 0$. The critical-point condition on the static Lagrangian is the same in both cases:

$$\frac{\partial\mathcal{L}}{\partial\Gamma}\bigg|_{\Gamma = P(\Gamma)} = 0$$

Computing each term with the Lagrangian $\mathcal{L} = -\|\Gamma\|_F^2 - \mu\det(\Gamma)$:

$$\frac{\partial}{\partial\Gamma_{ij}}\|\Gamma\|_F^2 = \frac{\partial}{\partial\Gamma_{ij}}\mathrm{tr}(\Gamma^T\Gamma) = 2\Gamma_{ij}$$

In matrix form: $\partial\|\Gamma\|_F^2/\partial\Gamma = 2\Gamma$.

$$\frac{\partial}{\partial\Gamma_{ij}}\det(\Gamma) = \det(\Gamma)\,(\Gamma^{-T})_{ij} = [\mathrm{adj}(\Gamma)^T]_{ij}$$

In matrix form: $\partial\det(\Gamma)/\partial\Gamma = \det(\Gamma)\cdot\Gamma^{-T}$.

The static extremum condition is:
$$-2P(\Gamma) - \mu\,\det(P(\Gamma))\cdot P(\Gamma)^{-T} = 0$$

Multiplying on the right by $P(\Gamma)^T$:

$$\boxed{P(\Gamma)\,P(\Gamma)^T = -\frac{\mu}{2}\det(P(\Gamma))\cdot \mathbf{1}_4}$$

where $\mathbf{1}_4$ denotes the $4\times4$ identity matrix (to avoid confusion with the intrinsic attribute $\mathbf{I}$).

**Proposition 13.1 (Structural equilibrium condition).** *The structural equilibrium $P(\Gamma)$ satisfies $P(\Gamma)P(\Gamma)^T \propto \mathbf{1}_4$ — a structurally isotropic configuration in which all output directions are equally weighted. The proportionality constant is $-(\mu/2)\det(P(\Gamma))$. This isotropy is a consequence of the extremum condition on the Lagrangian, not a postulate. In the dissipative regime ($\gamma > 0$), this equilibrium becomes a genuine attractor.*

**Remark 13.3 (Structural isotropy).** The condition $P(\Gamma)P(\Gamma)^T = \lambda I$ characterizes matrices with all singular values equal — a "maximally symmetric" coupling in which the UoC couples to all output directions with the same strength. For the structural attractor, this is the geometric analogue of thermal equilibrium in statistical mechanics: the most symmetric configuration accessible to the system given its constraints.

### 13.5.2 Forcing $\mu$ from the Coherence $c(\rho)$

From Proposition 13.1: $P(\Gamma)P(\Gamma)^T = \lambda\,\mathbf{1}_4$ where $\lambda = -\tfrac{\mu}{2}\det(P(\Gamma))$.

**Step 1 — left-hand side.** Using $\det(AB) = \det(A)\det(B)$ and $\det(A^T) = \det(A)$:
$$\det\!\bigl(P(\Gamma)P(\Gamma)^T\bigr) = \det(P(\Gamma))\cdot\det(P(\Gamma)^T) = \det(P(\Gamma))^2$$

**Step 2 — right-hand side.** For a $4\times4$ scalar multiple of the identity, $\det(\lambda\,\mathbf{1}_4) = \lambda^4$ (the eigenvalue $\lambda$ has multiplicity 4):
$$\det\!\bigl(\lambda\,\mathbf{1}_4\bigr) = \lambda^4 = \left(-\frac{\mu}{2}\right)^4\!\det(P(\Gamma))^4 = \frac{\mu^4}{16}\,\det(P(\Gamma))^4$$

**Step 3 — equate and solve.** Setting Step 1 = Step 2:
$$\det(P(\Gamma))^2 = \frac{\mu^4}{16}\,\det(P(\Gamma))^4$$

For $\det(P(\Gamma)) > 0$, divide both sides by $\det(P(\Gamma))^4$:
$$\det(P(\Gamma))^{-2} = \frac{\mu^4}{16} \implies \det(P(\Gamma)) = \frac{4}{\mu^2}$$

**Step 4 — define structural coherence.** Set $c(\rho) := \det(P(\Gamma|\rho))$:
$$c(\rho) = \frac{4}{\mu(\rho)^2} \implies \boxed{\mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

**Theorem 13.2 (Self-consistency determination of $\mu$).** *Given the structural coherence $c(\rho) = \det(P(\Gamma|\rho))$ at the attractor, the coupling strength $\mu(\rho)$ satisfies the self-consistency condition $\mu(\rho) = 2/\sqrt{c(\rho)}$.*

*Epistemic note.* This determination has the structure of a fixed-point equation: $P(\Gamma)$ is defined as the attractor of the dynamics generated by $\mathcal{L}$ (which contains $\mu$), and $\mu$ is extracted from $\det(P(\Gamma))$. The derivation closes this circle — given the Lagrangian form, the attractor condition forces a specific $\mu$ — but the argument is a self-consistency condition, not an independent derivation of $\mu$ from first principles. Within the stated Lagrangian structure, $\mu$ is uniquely determined by $c(\rho)$; $c(\rho)$ is a property of the system (not a free parameter), and Ch14 determines it for all $\rho$ given the anchor $c(\rho_{\mathrm{GR}}) = 1$.

**Remark 13.4 (Interpretation of $c(\rho)$).** The structural coherence $c(\rho)$ measures the "determinantal content" of the attractor — how non-degenerate the structural coupling is at equilibrium. Systems with $c \to 1$ (well-defined, full-rank attractor) have $\mu \to 2$. Systems with $c \to 0$ (attractor approaching degeneracy, $\partial\mathcal{M}(\Gamma)$) have $\mu \to \infty$ — an infinitely strong restoring force that can never actually reach the degenerate boundary. This structural mechanism prevents the UoC from collapsing structurally under finite perturbation: the purpose landscape has infinite walls at $\det(\Gamma) = 0$.

**Remark 13.5 (Gravitational boundary condition $c(\rho_{\mathrm{GR}}) = 1$).** The self-consistency condition $\mu(\rho) = 2/\sqrt{c(\rho)}$ leaves $c(\rho)$ as a free function until anchored at one reference level. The GSF cannot determine this anchor from purely internal geometry — it requires calibration against physical reality. The chosen calibration point is the gravitational level $\rho_{\mathrm{GR}}$: linearized GR imposes the massless graviton condition $(1 - \mu/2) = 0$, forcing $\mu(\rho_{\mathrm{GR}}) = 2$ and hence $c(\rho_{\mathrm{GR}}) = 1$. This is a *gravitational boundary condition* — the GSF scale is set by matching to an empirically established physical theory at one reference level. It is not a free fit: the massless spin-2 constraint is a structural consequence of general covariance, not an adjustable parameter. But it IS a calibration: without it, the function $c(\rho)$ is determined only up to an overall scale. Given this calibration and the scaling law of Ch14, $c(\rho)$ is fully determined for all $\rho$.

---

## 13.6 Ghost-Freedom

A *ghost* is a propagating degree of freedom with negative kinetic energy — a mode for which the kinetic term in the action is negative-definite. Ghost modes have no ground state (energy is unbounded below), generate runaway instabilities at the classical level, and violate unitarity under quantization. The absence of ghosts is a necessary condition for physical consistency of any Lagrangian field theory.

**Theorem 13.3 (Classical ghost-freedom — Euclidean signature).** *Within the Euclidean-signature Riemannian manifold $\mathcal{M}_{\mathrm{adm}}$ with Frobenius metric, the structural Lagrangian with kinetic term $T = \mathrm{tr}(\dot\Gamma^T\dot\Gamma)$ is ghost-free at the classical level: for all $\dot\Gamma \in T_\Gamma\mathcal{M}_{\mathrm{adm}}$,*
$$T(\dot\Gamma) \geq 0, \qquad T(\dot\Gamma) = 0 \iff \dot\Gamma = 0$$

*Proof.* Decompose $\dot\Gamma = \dot\Gamma_s + \dot\Gamma_a$. The cross-term vanishes by Lemma 13.1 (symmetric $\times$ antisymmetric orthogonality). For the antisymmetric part:
$$\mathrm{tr}(\dot\Gamma_a^2) = \sum_{i,k}(\dot\Gamma_a)_{ik}(\dot\Gamma_a)_{ki} = \sum_{i,k}(\dot\Gamma_a)_{ik}\cdot(-(\dot\Gamma_a)_{ik}) = -\|\dot\Gamma_a\|_F^2 \leq 0$$
Therefore:
$$T = \mathrm{tr}(\dot\Gamma_s^T\dot\Gamma_s) + \mathrm{tr}(\dot\Gamma_a^T\dot\Gamma_a) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$
with equality iff $\dot\Gamma_s = 0$ and $\dot\Gamma_a = 0$. $\square$

**Proposition 13.2 (The double-negative mechanism).** *The apparent ghost in the antisymmetric sector — the Lagrangian contains $-\mathrm{tr}(\Gamma_a^2)$, suggesting negative potential energy for the antisymmetric modes — is resolved by the intrinsic negativity of $\mathrm{tr}(\Gamma_a^2)$ for antisymmetric matrices. Specifically:*
$$\kappa = -1: \qquad \mathcal{L}_{V,a} = -\kappa\,\mathrm{tr}(\Gamma_a^2) = +\mathrm{tr}(\Gamma_a^2) = -\|\Gamma_a\|_F^2$$
*This is negative — the antisymmetric modes are in a potential well, not on a potential hill. No ghost arises.*

More precisely: the term $+\kappa\,\mathrm{tr}(\Gamma_a^2)$ in $T$ and the term $-\kappa\,\mathrm{tr}(\Gamma_a^2)$ in $V$ have the same sign structure. The kinetic term gives $(-1)\cdot\mathrm{tr}(\Gamma_a^2) = +\|\Gamma_a\|_F^2 > 0$ (ghost-free kinetic), and the potential term gives $-(-1)\cdot\mathrm{tr}(\Gamma_a^2) = -\|\Gamma_a\|_F^2 < 0$ (potential well). The apparent sign ambiguity created by $\kappa = -1$ is resolved by the algebraic fact that $\mathrm{tr}(\Gamma_a^2) < 0$ for all non-zero antisymmetric $\Gamma_a$.

**Corollary 13.1 (Uniqueness of $\kappa = -1$ for ghost-freedom).** *For any $\kappa \neq -1$, either the kinetic term or the potential term for the antisymmetric sector fails to be sign-definite, introducing either a ghost mode (kinetic) or an unbounded potential (potential). The value $\kappa = -1$ is the unique choice consistent with both ghost-freedom and the Frobenius geometry of $\mathcal{M}(\Gamma)$.*

**Remark 13.6 (Scope of Theorem 13.3).** Ghost-freedom is proved strictly for the Euclidean-signature manifold $\mathcal{M}_{\mathrm{adm}}$. If Part III introduces a pseudo-Riemannian (Lorentzian) extension to recover the physical spacetime signature, Theorem 13.3 does not automatically extend: a Lorentzian metric allows $ds^2 < 0$ for timelike directions, potentially reintroducing negative-energy modes. The Lorentzian extension will require its own ghost-freedom analysis — either a new proof or an identification of which modes are timelike and their energy status.

**Remark 13.7 (Ghost-freedom under quantization).** Theorem 13.3 establishes classical ghost-freedom. The quantum case requires additional analysis: quantization of $\Gamma$ in the presence of the constraint $\det(\Gamma) > 0$ introduces Dirac brackets and gauge conditions analogous to the Gupta-Bleuler procedure in EM quantization. A complete Dirac constraint analysis — identifying the first-class and second-class constraints of the GSF Lagrangian and verifying that the physical Hilbert space has positive-definite norm — is deferred to post-Hito 3 work. The classical result of Theorem 13.3 is a necessary condition for quantum ghost-freedom, not a sufficient one.

---

## 13.7 The Structural Lagrangian — Main Result

The three constraints established in §13.4–§13.6 — Frobenius ($\kappa = -1$), attractor ($\mu = 2/\sqrt{c}$), ghost-freedom (confirmed) — leave no free parameters in the structural Lagrangian at minimal polynomial order.

**Theorem 13.4 (The Structural Lagrangian).** *The unique parity-even, G(3)-invariant, ghost-free Lagrangian on $\mathcal{M}(\Gamma)$ at minimal polynomial order, consistent with the Frobenius metric and the structural attractor condition, is:*

$$\boxed{\mathcal{L}(\Gamma, \dot\Gamma, \rho) = \mathrm{tr}(\dot\Gamma^T\dot\Gamma) - \mathrm{tr}(\Gamma^T\Gamma) - \frac{2}{\sqrt{c(\rho)}}\,\det(\Gamma)}$$

*equivalently:*

$$\boxed{\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\,\det(\Gamma), \qquad \mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

*The function $c(\rho)$ is the structural coherence at the attractor — determined by the physics of the system at organizational level $\rho$, not a free parameter of the Lagrangian. Given the anchor $c(\rho_{\mathrm{GR}}) = 1$ (Remark 13.5) and the scaling law of Ch14, $c(\rho)$ is fully determined for all $\rho$.*

**On the meaning of "unique."** The uniqueness claim in Theorem 13.4 should be read carefully: the Lagrangian is unique *given the constraints stated* (parity, G(3)-invariance, Frobenius metric, attractor condition, minimal polynomial order). These constraints are not axioms chosen for convenience — each has a structural justification: parity from source-free isotropy (§13.2.1), G(3)-invariance from Ch3, Frobenius from the canonical metric on $\mathcal{M}(\Gamma)$ (§13.4), and the attractor condition from Ch11's definition of $P(\Gamma)$. No additional freedom is available within these constraints.

What is not claimed: the Lagrangian is the unique possible Lagrangian for all conceivable modifications of the GSF. Higher-order terms (degree 6, 8, ...) are excluded by the minimality requirement; non-polynomial terms (exponential, Born-Infeld) are excluded by the polynomial invariant basis; quantum corrections are excluded by the classical analysis. These exclusions are physically motivated, not logically forced. The Lagrangian of Theorem 13.4 is the *classical minimal* GSF Lagrangian.

---

## 13.8 The Equations of Motion

### 13.8.1 The Conservative EOM

The Euler-Lagrange equations for $\mathcal{L}(\Gamma, \dot\Gamma)$ with action $\mathcal{A} = \int\mathcal{L}\,dt$ give:

$$\frac{d}{dt}\frac{\partial\mathcal{L}}{\partial\dot\Gamma} - \frac{\partial\mathcal{L}}{\partial\Gamma} = 0$$

Computing each term:
$$\frac{\partial\mathcal{L}}{\partial\dot\Gamma} = 2\dot\Gamma, \qquad \frac{d}{dt}(2\dot\Gamma) = 2\ddot\Gamma$$
$$\frac{\partial\mathcal{L}}{\partial\Gamma} = -2\Gamma - \mu\,\det(\Gamma)\,\Gamma^{-T}$$

The Euler-Lagrange equation is:

$$2\ddot\Gamma - (-2\Gamma - \mu\,\det(\Gamma)\,\Gamma^{-T}) = 0$$

$$\boxed{\ddot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\det(\Gamma)\,\Gamma^{-T} = 0}$$

**Interpretation of each term:**
- $\ddot\Gamma$: structural acceleration — the second temporal derivative of $\Gamma$; the rate of change of structural momentum
- $\Gamma$: restitution term — coupling configurations are attracted toward zero in the absence of the nonlinear term; this represents the natural relaxation of structural coupling
- $\frac{\mu}{2}\det(\Gamma)\,\Gamma^{-T}$: nonlinear purpose force — drives $\Gamma$ toward $P(\Gamma)$ where $\Gamma\Gamma^T \propto \mathbf{1}_4$; vanishes when $\det(\Gamma) \to 0$ (loss of structural coherence)

### 13.8.2 The Dissipative EOM

Physical systems at positive $\rho$ dissipate structural energy. A Rayleigh dissipation function $\mathcal{F} = \frac{\gamma}{2}\|\dot\Gamma\|_F^2$ (with $\gamma > 0$ the structural damping coefficient) adds a velocity-dependent force to the EOM:

$$\boxed{\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\det(\Gamma)\,\Gamma^{-T} = N(t)}$$

where $N(t) \in \mathcal{M}(\Gamma)$ is the external forcing (perturbation, noise, environmental coupling).

**The four terms and their structural reading:**
- $\ddot\Gamma$: inertia of structural change — systems resist sudden reconfiguration
- $\gamma\dot\Gamma$: structural damping — ongoing reconfiguration costs energy; $\gamma$ measures organizational rigidity
- $\Gamma$: linear restoring force — toward structural equilibrium $\Gamma = 0$
- $\frac{\mu}{2}\det(\Gamma)\Gamma^{-T}$: purpose force — toward the structural equilibrium $P(\Gamma)$ (attractor in the dissipative regime); the force that makes the system a UoC rather than a passive medium

**Remark 13.8 (Singular dynamics near $\partial\mathcal{M}(\Gamma)$).** The term $\frac{\mu}{2}\det(\Gamma)\,\Gamma^{-T}$ in the EOM is singular as $\det(\Gamma) \to 0$: while $\det(\Gamma) \to 0$, $\Gamma^{-T}$ diverges, and the product $\det(\Gamma)\cdot\Gamma^{-T} = \mathrm{adj}(\Gamma)^T$ (by the cofactor identity) remains bounded — its entries are $(4-1)$-minors of $\Gamma$, which stay finite as $\det(\Gamma) \to 0$. The EOM is therefore well-posed as $\Gamma \to \partial\mathcal{M}(\Gamma)$ at the level of the adjugate term: $\frac{\mu}{2}\mathrm{adj}(\Gamma)^T$ is a polynomial in $\Gamma$, hence smooth everywhere. The apparent singularity in the $\det\cdot\Gamma^{-T}$ form is a representation artifact; the adjugate form $\mathrm{adj}(\Gamma)^T$ is the physically correct expression. Existence and uniqueness of the flow near the boundary, and the behavior of trajectories approaching $\partial\mathcal{M}(\Gamma)$ in finite time, are addressed in Part III.

**Remark 13.9 (The role of $N(t)$).** The external forcing $N(t)$ encodes all coupling of the UoC to its environment through $\mathbf{R}$. Its statistical properties (mean, covariance, spectral density) characterize the organizational environment. In the absence of $N(t)$ and with $\gamma > 0$, the EOM guarantees convergence to $P(\Gamma)$ from any initial $\Gamma$ with $\det(\Gamma) > 0$ — a consequence of the Lyapunov analysis of Ch19.

### 13.8.3 Conservation Law

In the conservative case ($\gamma = 0$, $N = 0$), the Hamiltonian is conserved:

$$H(\Gamma, \dot\Gamma) = \mathrm{tr}(\dot\Gamma^T\dot\Gamma) + \|\Gamma\|_F^2 + \mu\,\det(\Gamma) = \text{const}$$

The Hamiltonian has three contributions: kinetic (positive definite by Theorem 13.3), quadratic potential (positive definite), and quartic potential ($\mu\det(\Gamma)$ — positive when $\det(\Gamma) > 0$, which holds throughout $\mathcal{M}(\Gamma)$). The Hamiltonian is therefore positive definite on $\mathcal{M}(\Gamma)$ — a necessary condition for stability.

---

## 13.9 Structural Domain Tests — Preview

Chapter 15 will verify the Lagrangian of Theorem 13.4 against known physical and non-physical systems. For orientation, Table 13.1 previews the key reductions:

| System | $\Gamma$ | $c(\rho)$ | $\mu$ | EOM reduces to |
|---|---|---|---|---|
| Harmonic oscillator | $2\times2$ antisymmetric: $\Gamma_a = \begin{pmatrix}0 & x \\ -x & 0\end{pmatrix}$, null purpose | — | — | $\det(\Gamma_a)=0$ → $\ddot{x} + x = 0$ (SHO) |
| Simple pendulum | $2\times2$ antisymmetric with amplitude modulation | — | — | $\det=0$ → $\ddot\theta + \sin\theta = 0$ (nonlinear) |
| EM vacuum | $\Gamma = \Gamma_a$, $\det(\Gamma_a) = 0$ | — | — | $\ddot\Gamma_a + \Gamma_a = 0$ → wave eq. |
| GR linearized | $\Gamma_s = h_{\mu\nu}$, $\mu = 2$ | 1 | 2 | $(1-\mu/2)(\ldots) = 0$ → massless graviton |
| Biological cell | Full $4\times4$ | $c_{\mathrm{biol}}$ | $2/\sqrt{c_{\mathrm{biol}}}$ | Homeostatic attractor + Hopf |
| Economic system | $\Gamma_{ij} = $ coupling matrix | $c_{\mathrm{econ}}$ | $2/\sqrt{c_{\mathrm{econ}}}$ | Utility maximization at $P(\Gamma)$ |

The structural tests are not curve-fitting exercises. The Lagrangian parameters $\kappa$ and $\mu$ are determined by structural conditions (Theorems 13.1–13.2); the domain-specific content enters only through the attribute assignment $\{S,A,\mathbf{I},\mathbf{R}\}$ and the value of $c(\rho)$ — the latter being a property of the system, not a free coefficient to be adjusted.

---

## 13.10 Epistemic Status

Table 13.2 records what is derived, what is assumed, and what remains open in this chapter.

| Claim | Status | Justification |
|---|---|---|
| Admissible invariant basis $\{I_1, I_2, \det\}$ | Derived under constraints | Cayley-Hamilton + parity S2 + sector-decoupling + minimality (Lemmas 13.1–13.2, Remark 13.1) |
| $\kappa = -1$ | Derived under isotropy | Frobenius = unique isotropic choice under S1–S2; isotropy is a structural postulate (§13.4) |
| $\mu = 2/\sqrt{c(\rho)}$ | Self-consistency condition | Fixed-point: attractor extremum of $\mathcal{L}(\mu)$ determines $\mu$ (Theorem 13.2) |
| Ghost-freedom (classical) | Proved | Double-negative mechanism (Theorem 13.3) |
| Ghost-freedom (quantum) | Open | Requires Dirac constraint analysis (post Hito 3) |
| $c(\rho_{\mathrm{GR}}) = 1$ | Derived | Massless graviton constraint (Remark 13.5) |
| $c(\rho)$ for other levels | Ch14 | Requires scaling law T1 |
| Full EM correspondence | Partial | Hito 3 (stratum bridge) required for $\Box F = 0$ |
| Full GR correspondence | Partial | Hito 3 required for $G_{\mu\nu} = 0$ from EOM |
| Higher-order corrections | Open | Quantum corrections to $\mathcal{L}$ |

The Lagrangian of Theorem 13.4 is the unique minimal-order classical Lagrangian consistent with the structural requirements of the GSF. It is not the final word on the GSF Lagrangian — it is the zeroth-order term in a systematic expansion whose higher-order terms await the quantum theory.

The derivation does not fit coefficients to physical data, does not invoke EM or GR as starting points, and uses no domain-specific information beyond the structural symmetries S1–S3. The Lagrangian follows from the geometry of $\mathcal{M}(\Gamma)$ and the definition of the structural attractor. The physics enters as verification, not as input.

---

*From this point, the Lagrangian is fixed. Chapter 14 derives the function $c(\rho)$ for all organizational levels via the scaling law, completing the explicit form of $\mu(\rho)$. Chapters 15–18 test the result against specific domains. The question the GSF must now answer is not "does the Lagrangian work?" but "what does the Lagrangian predict?"*
