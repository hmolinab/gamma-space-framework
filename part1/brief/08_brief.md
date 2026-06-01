# Chapter 8: The Configuration Map
*Condensed version — source: Ch8 of the full GSF*

---

## 8.1 The Open Question from Ch5

Ch5 established the structural form of Γ — the 4×4/10×10 coupling matrix, the Sym-Antisym decomposition, and the degenerate configurations — but left one question explicitly open (§5.8):

> *"What determines the inner product $\langle\text{attr}_i, \text{attr}_j\rangle$ that defines $\Gamma_{ij}$?"*

Until this is answered: (1) Γ_{ij} are free parameters with no dependence on ξ; (2) the Jacobian ∂Γ/∂ξ cannot be computed; (3) the transformation law of Γ under G(3) cannot be verified; (4) the tensor vs. matrix question (Ch5 §5.3) cannot be resolved.

**Ch8 closes this gap** by identifying the G(3) scalar inner product on the paravector M = S + **A** + **I** + **R** as the natural structural metric. The result is an explicit polynomial Gram map ξ ↦ Γ(ξ).

---

## 8.2 The G(3) Inner Product on Attribute Space

The G(3) algebra defines the canonical scalar inner product via grade-0 projection of the geometric product:

$$\langle u, v \rangle_{G(3)} := \langle u\tilde{v} \rangle_0$$

| $u$ | $v$ | $\langle u, v \rangle_{G(3)}$ |
|-----|-----|-------------------------------|
| $S$ (grade 0) | $S'$ (grade 0) | $S \cdot S'$ |
| $\mathbf{u}$ (grade 1) | $\mathbf{v}$ (grade 1) | $\mathbf{u} \cdot \mathbf{v}$ |
| $S$ (grade 0) | $\mathbf{v}$ (grade 1) | $0$ |

**Grade-mismatch theorem:** the scalar inner product between elements of different grades vanishes identically — a structural consequence of the G(3) grade filtration, not an assumption. This makes the S-sector structurally decoupled from the vector sector in Γ_s.

---

## 8.3 The Gram Construction: Explicit Γ_s(ξ)

**Definition 8.1 (Gram Configuration Map).**

$$\boxed{\Gamma_s(\xi) = \begin{pmatrix} S^2 & 0 & 0 & 0 \\ 0 & |\mathbf{A}|^2 & \mathbf{A}\cdot\mathbf{I} & \mathbf{A}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{I} & |\mathbf{I}|^2 & \mathbf{I}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{R} & \mathbf{I}\cdot\mathbf{R} & |\mathbf{R}|^2 \end{pmatrix}}$$

Block structure (grade-mismatch theorem):
- **[S²]**: S self-coherence — decoupled from vectors
- **3×3 bottom-right block**: Gram matrix of {**A**, **I**, **R**} under ℝ³ dot product

**Proposition 8.1 (Operative condition in Gram form).** $\Gamma_s(\xi) \succ 0$ iff:
1. $S \neq 0$
2. $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ linearly independent in $\mathbb{R}^3$

This is strictly stronger than **I** ∦ **R** (Field operative) — positive-definiteness implies Field operative, not conversely.

---

## 8.4 The Antisymmetric Part: Γ_a(ξ)

The antisymmetric coupling uses the G(3) outer (wedge) product. In the **10×10 expanded form**, the natural coupling between two vectors **u**, **v** ∈ ℝ³ is:

$$[\mathbf{u} \wedge \mathbf{v}]_\times = \tfrac{1}{2}(\mathbf{u}\mathbf{v}^T - \mathbf{v}\mathbf{u}^T) \in \mathfrak{so}(3)$$

which via the Levi-Civita isomorphism corresponds exactly to **u** × **v**.

**The Field block** — exact recovery:
$$(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R}} = [\mathbf{I} \wedge \mathbf{R}]_\times \;\longleftrightarrow\; \mathbf{I} \times \mathbf{R} = \mathbf{Field}$$

Field is algebraically *encoded* in the (I,R) antisymmetric block — exact, not parameterized.

**The Force block** — direct encoding:
$$(\Gamma_a^{(10)})_{S\mathbf{A}} = S\mathbf{A} = \mathbf{Force}$$

Force = S**A** appears directly as the (S, **A**) off-diagonal antisymmetric block.

**4×4 abstract form** (scalar entries via Frobenius norms of the 3×3 blocks — loses orientation, retains topology):

$$\Gamma_a(\xi) = \begin{pmatrix} 0 & S|\mathbf{A}| & S|\mathbf{I}| & S|\mathbf{R}| \\ -S|\mathbf{A}| & 0 & |\mathbf{A}\times\mathbf{I}| & |\mathbf{A}\times\mathbf{R}| \\ -S|\mathbf{I}| & -|\mathbf{A}\times\mathbf{I}| & 0 & |\mathbf{I}\times\mathbf{R}| \\ -S|\mathbf{R}| & -|\mathbf{A}\times\mathbf{R}| & -|\mathbf{I}\times\mathbf{R}| & 0 \end{pmatrix}$$

*(Full structural content lives in the 10×10 form; 4×4 is a scalar summary.)*

---

## 8.5 The Full Map Γ(ξ)

**Definition 8.2 (Configuration Map).**

$$\Gamma: \mathcal{V} \to \mathrm{Sym}^+(4) \oplus \mathfrak{so}(4), \qquad \xi \mapsto \Gamma_s(\xi) + \Gamma_a(\xi)$$

- **Smoothness:** entries are polynomials of degree ≤ 2 in components of ξ → $\Gamma \in C^\infty(\mathcal{V})$. Not an assumption — a consequence. Confirms Ch9 §9.2.
- **G(3)-equivariance:** under G(3) rotation $g$, with $J_g = \mathrm{diag}(1, R_g, R_g, R_g)$:
$$\Gamma_s(g\cdot\xi) = J_g^T\,\Gamma_s(\xi)\,J_g$$
This is the covariant transformation law of a $(0,2)$ tensor. The explicit representation is $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3}) \in O(10)$ — orthogonal by construction. Confirms Ch10 Postulate 10.1 and Ch11 Assumption 23.1.

---

## 8.6 The Jacobian DΓ(ξ)

Polynomial entries → Jacobian is linear in ξ (explicitly computable). Key non-zero blocks:

$$\frac{\partial(\Gamma_s)_{00}}{\partial S} = 2S, \quad \frac{\partial(\Gamma_s)_{12}}{\partial A_k} = I_k, \quad \frac{\partial(\Gamma_s)_{12}}{\partial I_k} = A_k$$

$$\frac{\partial(\Gamma_a^{(10)})_{S\mathbf{A}}}{\partial S} = \mathbf{A}, \quad \frac{\partial(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R},jk}}{\partial I_l} = \tfrac{1}{2}(\delta_{jl}R_k - \delta_{kl}R_j)$$

The full sparse structure mirrors the coupling topology of the UoC. Now available for: chain-rule force decomposition (Ch11 §11.5), induced mobility $M_\Gamma = D\Gamma \cdot M \cdot D\Gamma^T$ (Ch11 §11.5).

---

## 8.7 Verification of the Structural Injectivity Criterion

**Proposition 8.2 (SIC at operative configurations).** At any operative $\xi^*$ ($S^* \neq 0$, $\{\mathbf{A}^*, \mathbf{I}^*, \mathbf{R}^*\}$ linearly independent):

$$\mathrm{rank}(D\Gamma(\xi^*)) = 10 = \dim(\mathcal{V})$$

**Corollary 8.1.** The SIC of Ch11 §11.5 holds for all operative UoCs under the Gram map. Local uniqueness of $\xi^*$ as a preimage of $\Gamma^*$ follows.

---

## 8.8 Resolution: Tensor or Matrix?

| Object | Status | Transformation law |
|--------|--------|--------------------|
| $\Gamma_s(\xi)$ | $(0,2)$ covariant **tensor** on $\mathcal{V}$ under G(3) | $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ |
| $\Gamma_a^{(10)}(\xi)$ | $(0,2)$ antisymmetric **tensor** under SO(3) | $\Gamma_a \mapsto J_g^T \Gamma_a J_g$ |
| $\Gamma(\xi)$ total | $(0,2)$ **tensor** on $\mathcal{V}$ under G(3) | $\Gamma \mapsto J_g^T \Gamma J_g$ |
| 4×4 abstract form | Scalar coupling summary — not tensorial in general | — |

**Resolution (Ch5 §5.3):** "configuration tensor" is correct in the 10×10 expanded form. The transformation law required by Ch10 Postulate 10.1 is established here — not just postulated.

---

## 8.9 What This Map Provides to Part II

### Backward consistency (Ch1–Ch5)
- **Force** = S**A** encoded in (S,**A**) antisymmetric block ✓
- **Field** = **I**×**R** encoded exactly via Levi-Civita in (I,R) block ✓
- **Γ_s ≻ 0** ↔ S ≠ 0, {**A**,**I**,**R**} lin. independent — consistent with Ch5 Def. 5.2 ✓

### Forward deliverables for Ch9–Ch11
- **Ch9 §9.2 smoothness:** not an assumption — polynomial map → $C^\infty$ ✓
- **Ch10 Postulate 10.1 transformation law:** $\Gamma_s \mapsto J_g^T\Gamma_s J_g$ established here ✓
- **Ch11 Assumption 23.1:** $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ orthogonal — verified here ✓
- **Ch11 §11.5 Jacobian:** $D\Gamma(\xi)$ explicitly computed in §8.6 ✓
- **Ch11 Corollary 11.1 SIC:** verified by Proposition 8.2 ✓

### What the map does NOT close
- Coefficients $\kappa, \mu, \nu$ of $P(\Gamma)$ — depend on the potential, not the map
- Explicit $P(\Gamma)$ — still open
- Global injectivity — $\mathbb{Z}_2$ ambiguity identified (§8.10); full analysis open

---

## 8.10 Open Questions

- **Global injectivity ($\mathbb{Z}_2$ ambiguity):** $\Gamma_s$ is even under global sign flip $(\mathbf{A},\mathbf{I},\mathbf{R}) \mapsto (-\mathbf{A},-\mathbf{I},-\mathbf{R})$; $\Gamma_a$ is odd — the antisymmetric part resolves the $\mathbb{Z}_2$ at the level of the full Γ. Full analysis on $D_\xi(\rho)$ open.

- **Pseudo-Riemannian extension:** the G(3) inner product is Euclidean. At extreme ρ values, the attribute metric may require a pseudo-Riemannian (indefinite) analog. This generalization is deferred to future work.

- **4×4 sign convention for $\Gamma_a$:** magnitudes $|\mathbf{u}\times\mathbf{v}|$ lose orientation. The G(3) pseudoscalar $I_3 = \mathbf{e}_1\mathbf{e}_2\mathbf{e}_3$ provides a natural orientation, replacing $|\mathbf{u}\times\mathbf{v}|$ with a signed scalar — but this requires a canonical reference frame derivable from the UoC state.

- **Cross-sector coupling in $\Gamma_a$:** the blocks $[\mathbf{A}\wedge\mathbf{I}]_\times$ and $[\mathbf{A}\wedge\mathbf{R}]_\times$ encode couplings beyond Force and Field. Phenomenological interpretation is an open correspondence (candidate: subsequent work).

---

## 8.11 Status Summary

| Open question (Ch5 §5.8) | Status after Ch8 |
|---------------------------|-------------------|
| What determines $\langle\text{attr}_i, \text{attr}_j\rangle$? | **Closed** — G(3) scalar inner product → Gram map |
| Transformation law of Γ | **Established** — $\Gamma \mapsto J_g^T\Gamma J_g$ under G(3) |
| Tensor vs. matrix | **Resolved** — tensor in 10×10; scalar summary in 4×4 |
| Jacobian $\partial\Gamma/\partial\xi$ | **Computed** — explicit linear map from polynomial entries |
| SIC (Ch1 Corollary 11.1) | **Verified** — Proposition 8.2: holds at all operative $\xi^*$ |
| Smoothness (Ch9 §9.2) | **Derived** — polynomial map → $C^\infty$ (not an assumption) |
| Ch10 Postulate 10.1 transformation law | **Established** — not postulated |
| Ch11 Assumption 23.1 orthogonality | **Established** — $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ verified |
| Global injectivity | **Partial** — $\mathbb{Z}_2$ identified; full analysis open |

---

*End of Chapter 8 (condensed)*
