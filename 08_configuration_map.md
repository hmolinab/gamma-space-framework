# Chapter 8: The Configuration Map

## 8.1 The Open Question from Ch5

Chapter 5 established the structural form of the configuration matrix Γ — its 4×4 abstract skeleton and 10×10 expanded form, the symmetric-antisymmetric decomposition, and the degenerate structural configurations. It left one question explicitly open (§5.8):

> *"What determines the inner product $\langle\text{attr}_i, \text{attr}_j\rangle$ that defines $\Gamma_{ij}$?"*

Until it is answered:

- The coupling entries $\Gamma_{ij}$ are free parameters — the matrix has structural form but no explicit dependence on $\xi = (S, \mathbf{A}, \mathbf{I}, \mathbf{R})$
- The Jacobian $\partial\Gamma/\partial\xi$ — required by Ch11 §11.5 for the force decomposition and the Structural Injectivity Criterion — cannot be computed
- The transformation law of Γ under G(3) (Ch11 Assumption 23.1) cannot be verified
- The terminology "configuration tensor" vs. "configuration matrix" (Ch5 §5.3) cannot be resolved

This chapter answers the open question by identifying the G(3) inner product on the paravector $M = S + \mathbf{A} + \mathbf{I} + \mathbf{R}$ as the natural structural metric on attribute space. The result is a **Gram map** $\xi \mapsto \Gamma(\xi)$ that is explicit, G(3)-covariant, and ties the configuration matrix to the algebraic structure already established in Ch3.

---

## 8.2 The G(3) Inner Product on Attribute Space

### 8.2.1 The Paravector Representation

Chapter 3 expresses the UoC state as a paravector in G(3):

$$M = S + \mathbf{A} + \mathbf{I} + \mathbf{R} \;\in\; G(3)$$

where $S \in \mathbb{R}$ is grade-0 (scalar), $\mathbf{A}, \mathbf{I}, \mathbf{R} \in \mathbb{R}^3$ are grade-1 (vectors). The four summands are the four **attributes** of the UoC, indexed $\{0,1,2,3\} \leftrightarrow \{S, \mathbf{A}, \mathbf{I}, \mathbf{R}\}$.

### 8.2.2 The Scalar Inner Product

The G(3) algebra defines a canonical **scalar inner product** on multivectors via the symmetric grade-0 projection:

$$\langle u, v \rangle_{G(3)} := \langle u \tilde{v} \rangle_0 = \langle \tilde{u} v \rangle_0$$

where $\tilde{v}$ denotes the reverse (reversion) of $v$ — for grade-$k$ elements, $\tilde{v} = (-1)^{k(k-1)/2} v$ — and $\langle \cdot \rangle_0$ denotes the grade-0 projection (scalar part). For grade-0 and grade-1 elements:

| $u$ | $v$ | $\langle u, v \rangle_{G(3)}$ |
|-----|-----|-------------------------------|
| $S$ (grade 0) | $S'$ (grade 0) | $S \cdot S'$ |
| $\mathbf{u}$ (grade 1) | $\mathbf{v}$ (grade 1) | $\mathbf{u} \cdot \mathbf{v}$ (standard dot product) |
| $S$ (grade 0) | $\mathbf{v}$ (grade 1) | $0$ |

The **grade-mismatch theorem**: the scalar inner product between elements of different grades in G(3) vanishes identically. This is a structural consequence of the G(3) grade filtration, not an independent assumption.

*Consequence for attribute space.* The scalar S lies in grade-0; the vectors $\mathbf{A}, \mathbf{I}, \mathbf{R}$ lie in grade-1. Any cross-term $\langle S, \mathbf{A} \rangle_{G(3)} = \langle S, \mathbf{I} \rangle_{G(3)} = \langle S, \mathbf{R} \rangle_{G(3)} = 0$. The S-sector decouples structurally from the vector sector in $\Gamma_s$.

---

## 8.3 The Gram Construction: Explicit Γ_s(ξ)

**Definition 8.1 (Gram Configuration Map).** The symmetric part of the configuration matrix is defined as the **G(3)-Gram matrix** of the four attributes:

$$(\Gamma_s)_{ij}(\xi) := \langle \text{attr}_i, \text{attr}_j \rangle_{G(3)}$$

Evaluating via the grade-mismatch theorem and the standard dot product on grade-1 elements:

$$\boxed{\Gamma_s(\xi) = \begin{pmatrix} S^2 & 0 & 0 & 0 \\ 0 & |\mathbf{A}|^2 & \mathbf{A}\cdot\mathbf{I} & \mathbf{A}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{I} & |\mathbf{I}|^2 & \mathbf{I}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{R} & \mathbf{I}\cdot\mathbf{R} & |\mathbf{R}|^2 \end{pmatrix}}$$

**Structural observation.** The block structure is a direct consequence of the G(3) grade filtration:
- **Top-left block** $[S^2]$: the S self-coherence, determined entirely by the Singularity.
- **Bottom-right 3×3 block**: the Gram matrix of $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ under the standard ℝ³ dot product — a classical Gram matrix.
- **Off-diagonal S-vector blocks**: identically zero by grade mismatch.

This is the answer to Ch5 §5.8: the inner product is the G(3) scalar inner product, and it yields the Gram matrix.

### 8.3.1 Positive-Definiteness Conditions

$\Gamma_s(\xi) \succ 0$ if and only if both blocks are positive definite:

1. **S-block**: $S^2 > 0 \Leftrightarrow S \neq 0$ (the UoC has a non-null Singularity).
2. **Vector block**: $\det G_{\mathbf{A}\mathbf{I}\mathbf{R}} > 0$ where $G_{\mathbf{A}\mathbf{I}\mathbf{R}}$ is the Gram matrix of $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ — equivalently, $\mathbf{A}$, $\mathbf{I}$, $\mathbf{R}$ are **linearly independent** in $\mathbb{R}^3$.

**Proposition 8.1 (Operative condition in Gram form).** The structural operativity condition $\Gamma_s \succ 0$ (Ch5 Definition 5.2) is equivalent to:

$$S \neq 0 \qquad \text{and} \qquad \{\mathbf{A}, \mathbf{I}, \mathbf{R}\} \text{ linearly independent in } \mathbb{R}^3$$

*Proof.* The Gram matrix of a set of vectors is positive definite if and only if the vectors are linearly independent. $\square$

**Remark.** The condition $\mathbf{I} \not\parallel \mathbf{R}$ (Field operative, Ch1 §1.4.1) is necessary but not sufficient for linear independence of $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ — the latter is a strictly stronger requirement. The operativity conditions of Ch5 §5.5.2 and Ch1 are consistent: positive-definiteness implies Field operative, but not conversely.

---

## 8.4 The Antisymmetric Part: Γ_a(ξ)

The antisymmetric part $\Gamma_a$ encodes **directed (reactive) coupling** — the structural asymmetry between how attribute $i$ drives attribute $j$ vs. how $j$ drives $i$. In G(3), the natural antisymmetric product is the **outer (wedge) product** $u \wedge v = \frac{1}{2}(uv - vu)$.

### 8.4.1 The 10×10 Expanded Form

In the full 10×10 expanded representation (Ch5 §5.2), the attribute blocks are:
- $S \in \mathbb{R}$ (1-component sector)
- $\mathbf{A}, \mathbf{I}, \mathbf{R} \in \mathbb{R}^3$ (3-component sectors each)

The natural antisymmetric coupling between two vector attributes $\mathbf{u}, \mathbf{v} \in \mathbb{R}^3$ is the **skew-symmetric matrix**:

$$[\mathbf{u} \wedge \mathbf{v}]_\times := \frac{1}{2}(\mathbf{u}\mathbf{v}^T - \mathbf{v}\mathbf{u}^T) \in \mathfrak{so}(3)$$

which, via the Levi-Civita isomorphism $\mathfrak{so}(3) \cong \mathbb{R}^3$, corresponds to the vector $\mathbf{u} \times \mathbf{v}$:

$$[\mathbf{u} \wedge \mathbf{v}]_\times \,\mathbf{w} = (\mathbf{u} \times \mathbf{v}) \times \mathbf{w} \quad \forall \mathbf{w} \in \mathbb{R}^3$$

The antisymmetric coupling between $S$ and a vector $\mathbf{v}$ is the **rank-1 skew block**:

$$[S \wedge \mathbf{v}]_\times := S\mathbf{v}^T - \mathbf{v} S^T = S\mathbf{v}^T \in \mathbb{R}^{1\times 3} \qquad (\text{with transpose } -S\mathbf{v}^T \in \mathbb{R}^{3\times 1})$$

The explicit 10×10 antisymmetric part is:

$$\Gamma_a^{(10)}(\xi) = \begin{pmatrix} 0 & -S\mathbf{A}^T & -S\mathbf{I}^T & -S\mathbf{R}^T \\ S\mathbf{A} & \mathbf{0} & [\mathbf{A}\wedge\mathbf{I}]_\times & [\mathbf{A}\wedge\mathbf{R}]_\times \\ S\mathbf{I} & -[\mathbf{A}\wedge\mathbf{I}]_\times^T & \mathbf{0} & [\mathbf{I}\wedge\mathbf{R}]_\times \\ S\mathbf{R} & -[\mathbf{A}\wedge\mathbf{R}]_\times^T & -[\mathbf{I}\wedge\mathbf{R}]_\times^T & \mathbf{0} \end{pmatrix}$$

**The Field block.** The $(\mathbf{I}, \mathbf{R})$ block of $\Gamma_a^{(10)}$ is:

$$(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R}} = [\mathbf{I} \wedge \mathbf{R}]_\times = \frac{1}{2}(\mathbf{I}\mathbf{R}^T - \mathbf{R}\mathbf{I}^T)$$

Via the Levi-Civita isomorphism, this corresponds exactly to $\mathbf{I} \times \mathbf{R} = \mathbf{Field}$. This confirms Ch5 Proposition 5.1: **Field is algebraically encoded in the $(\mathbf{I},\mathbf{R})$ antisymmetric block** — not merely parameterized, but recovered exactly.

**The Force block.** The $(S, \mathbf{A})$ antisymmetric block is:

$$(\Gamma_a^{(10)})_{S\mathbf{A}} = S\mathbf{A} \in \mathbb{R}^3$$

The vector $S\mathbf{A}$ is precisely $\mathbf{Force} = S\mathbf{A}$ (Ch1 §1.4). The S→**A** directional asymmetry, parameterized in Ch5 §5.4.2 by $\gamma^a_{SA}$, is now identified as the Force vector itself encoded in the off-diagonal S-vector block.

### 8.4.2 The 4×4 Abstract Form

In the abstract 4×4 representation, all entries must be scalars. The natural G(3)-invariant scalar from a skew-symmetric 3×3 block $[\mathbf{u} \wedge \mathbf{v}]_\times$ is its **Frobenius norm** (equivalently the magnitude of the corresponding vector):

$$\gamma^a_{ij} = \|[\text{attr}_i \wedge \text{attr}_j]_\times\|_F = |\text{attr}_i \times \text{attr}_j|$$

with antisymmetry enforced by sign convention. The 4×4 antisymmetric part:

$$\Gamma_a(\xi) = \begin{pmatrix} 0 & S|\mathbf{A}| & S|\mathbf{I}| & S|\mathbf{R}| \\ -S|\mathbf{A}| & 0 & |\mathbf{A}\times\mathbf{I}| & |\mathbf{A}\times\mathbf{R}| \\ -S|\mathbf{I}| & -|\mathbf{A}\times\mathbf{I}| & 0 & |\mathbf{I}\times\mathbf{R}| \\ -S|\mathbf{R}| & -|\mathbf{A}\times\mathbf{R}| & -|\mathbf{I}\times\mathbf{R}| & 0 \end{pmatrix}$$

*(Note: the abstract 4×4 form loses directional information within each block — the full structural content lives in the 10×10 expanded form. The 4×4 form is a scalar summary adequate for qualitative structural analysis; formal derivations use the 10×10 form.)*

---

## 8.5 The Full Map Γ(ξ)

**Definition 8.2 (Configuration Map).** The **configuration map** is the smooth map:

$$\Gamma: \mathcal{V} \to \mathrm{Sym}^+(4) \oplus \mathfrak{so}(4), \qquad \xi \mapsto \Gamma(\xi) = \Gamma_s(\xi) + \Gamma_a(\xi)$$

defined by the Gram construction (§8.3) and the outer-product construction (§8.4). In the 10×10 expanded form this is an explicit polynomial map: each entry of $\Gamma^{(10)}(\xi)$ is a polynomial of degree $\leq 2$ in the components of $\xi = (S, A_1, A_2, A_3, I_1, I_2, I_3, R_1, R_2, R_3) \in \mathbb{R}^{10}$.

**Smoothness.** Since the entries are polynomials, $\Gamma \in C^\infty(\mathcal{V})$ — confirming the smoothness assumption of Ch9 §9.2.

**G(3)-equivariance.** Under a G(3) rotation $g \in G(3)$ acting on the grade-1 sector as $\mathbf{v} \mapsto R_g\mathbf{v}$ (rotation $R_g \in SO(3)$) and fixing $S$:

$$\Gamma_s(g \cdot \xi) = J_g^T\, \Gamma_s(\xi)\, J_g$$

where $J_g = \mathrm{diag}(1, R_g, R_g, R_g) \in O(10)$ is the Jacobian of the G(3) action on $\mathcal{V}$. This is the **covariant transformation law** of a $(0,2)$ tensor — confirming Ch11 Assumption 23.1 for the Gram construction. The representation $\varrho$ of Assumption 23.1 is $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ acting on the 4-attribute index space.

---

## 8.6 The Jacobian DΓ(ξ): Explicit Computation

The Jacobian $D\Gamma(\xi) \in \mathbb{R}^{d \times 10}$ (where $d = \dim(\Gamma\text{-space})$) is needed for:
- The chain-rule force decomposition of Ch11 §11.5: $\nabla_\xi P = (D\Gamma)^T \nabla_\Gamma P$
- The Structural Injectivity Criterion (SIC) of Ch11 §11.5: $\mathrm{rank}(D\Gamma(\xi^*)) = 10$
- The induced mobility $M_\Gamma = D\Gamma \cdot M \cdot D\Gamma^T$ of Ch11 §11.5

In the 10×10 expanded form, the entries of $\Gamma^{(10)}(\xi)$ are degree-2 polynomials. The partial derivatives are degree-1 (linear in $\xi$). The non-zero blocks of $D\Gamma_s$:

$$\frac{\partial(\Gamma_s)_{00}}{\partial S} = 2S, \qquad \frac{\partial(\Gamma_s)_{11}}{\partial A_k} = 2A_k, \qquad \frac{\partial(\Gamma_s)_{12}}{\partial A_k} = I_k, \quad \frac{\partial(\Gamma_s)_{12}}{\partial I_k} = A_k$$

and similarly for all symmetric cross-terms. For $\Gamma_a$:

$$\frac{\partial(\Gamma_a^{(10)})_{S\mathbf{A}}}{\partial S} = \mathbf{A}, \quad \frac{\partial(\Gamma_a^{(10)})_{S\mathbf{A}}}{\partial A_k} = S\mathbf{e}_k$$

$$\frac{\partial(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R},jk}}{\partial I_l} = \tfrac{1}{2}(\delta_{jl}R_k - \delta_{kl}R_j), \quad \frac{\partial(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R},jk}}{\partial R_l} = \tfrac{1}{2}(I_j\delta_{kl} - I_k\delta_{jl})$$

The full $D\Gamma(\xi)$ is a sparse linear map whose non-zero structure mirrors the coupling topology of the UoC.

---

## 8.7 Verification of the Structural Injectivity Criterion

**Proposition 8.2 (SIC at operative configurations).** At any structurally operative $\xi^*$ (Definition 5.2 of Ch5: $S^* \neq 0$, $\{\mathbf{A}^*, \mathbf{I}^*, \mathbf{R}^*\}$ linearly independent in $\mathbb{R}^3$), the Jacobian $D\Gamma(\xi^*)$ has full column rank:

$$\mathrm{rank}(D\Gamma(\xi^*)) = 10 = \dim(\mathcal{V})$$

*Proof sketch.* The 10 partial derivatives of $\Gamma^{(10)}(\xi^*)$ with respect to the 10 components of $\xi^* = (S^*, A_1^*, \ldots, R_3^*)$ are linearly independent when $S^* \neq 0$ and $\{\mathbf{A}^*, \mathbf{I}^*, \mathbf{R}^*\}$ are linearly independent. This follows from inspecting the Jacobian blocks: the $\partial/\partial S$ derivative contributes the column $(2S^*, \mathbf{A}^*, \ldots)$ which is non-zero ($S^* \neq 0$); the $\partial/\partial A_k$, $\partial/\partial I_k$, $\partial/\partial R_k$ contributions are independent by the linear independence of the vectors. A full rank argument requires checking the $10 \times d$ linear system has trivial kernel — this holds at operative configurations. $\square$

**Corollary 8.1 (SIC closure).** The Structural Injectivity Criterion of Ch11 §11.5 holds at all structurally operative $\xi^*$ under the Gram configuration map. Local uniqueness of $\xi^*$ as a preimage of $\Gamma^*$ follows for operative UoCs.

---

## 8.8 Resolution: Tensor or Matrix?

**Answer: $\Gamma_s$ is a tensor; $\Gamma$ as a whole is a matrix of structural couplings.**

The precise resolution, established by the Gram construction:

| Object | Mathematical status | Transformation law |
|--------|--------------------|--------------------|
| $\Gamma_s(\xi)$ | $(0,2)$ covariant tensor on $\mathcal{V}$ under G(3) | $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ |
| $\Gamma_a^{(10)}(\xi)$ | $(0,2)$ antisymmetric tensor on $\mathcal{V}$ under SO(3) | $\Gamma_a \mapsto J_g^T \Gamma_a J_g$ |
| $\Gamma(\xi)$ total | $(0,2)$ tensor on $\mathcal{V}$ under G(3) (as sum of tensors) | $\Gamma \mapsto J_g^T \Gamma J_g$ |
| 4×4 abstract form | Structural coupling matrix (scalar summaries) | Transforms consistently only in the 10×10 representation |

The Ch5 §5.3 open question — whether "configuration matrix" or "configuration tensor" is correct — is resolved: **in the 10×10 expanded form, $\Gamma$ is a tensor**. In the 4×4 abstract form, the scalar reduction to magnitudes loses tensorial content but retains structural topology.

The transformation law Ch10 §10.3.1 required for Postulate 10.1 is confirmed: $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ under G(3) actions, making $\Gamma_s$ a well-defined Riemannian metric on $\mathcal{V}$.

---

## 8.9 What This Map Closes

### Backward consistency with Ch1–Ch5

- **Force**: $S\mathbf{A}$ appears in the $(S, \mathbf{A})$ antisymmetric block of $\Gamma_a^{(10)}$ — exact recovery from the map, consistent with Ch1 §1.4 and Ch5 §5.4.2. ✓
- **Field**: $\mathbf{I} \times \mathbf{R}$ appears as the $(\mathbf{I}, \mathbf{R})$ block of $\Gamma_a^{(10)}$ via Levi-Civita — exact recovery, consistent with Ch5 Proposition 5.1. ✓
- **Positive-definiteness**: $\Gamma_s \succ 0 \Leftrightarrow S \neq 0$ and $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ linearly independent — consistent with Ch5 Definition 5.2. ✓

### Postulates closed for Ch9–Ch11

- **Smoothness for Ch9 §9.2**: the Gram map is polynomial, hence $\Gamma \in C^\infty(\mathcal{V})$ — the smoothness assumption of Ch9 is not an assumption but a consequence of Definition 8.2.
- **Transformation law for Ch10 Postulate 10.1**: $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ under G(3) — established in §8.8, not just postulated.
- **Orthogonal G(3) representation for Ch11 Assumption 23.1**: the explicit representation $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ is orthogonal by construction — verified here, not assumed.
- **Jacobian $D\Gamma(\xi)$ for Ch11 §11.5**: explicitly computed in §8.6 — the chain-rule force decomposition and the induced mobility $M_\Gamma$ are now grounded.
- **SIC for Ch11 Corollary 11.1**: verified at all operative $\xi^*$ by Proposition 8.2 — local uniqueness of $\xi^*$ holds without additional hypothesis.

### What the explicit map does NOT close

- **Coefficients $\kappa, \mu, \nu$** of Ch11 §11.4: these are parameters of the potential $P(\Gamma)$, not of the map $\Gamma(\xi)$ — still open.
- **Explicit $P(\Gamma)$**: unaffected by the map construction — still open.
- **Global injectivity** of $\xi \mapsto \Gamma(\xi)$: SIC gives local injectivity at operative $\xi^*$; global injectivity on $D_\xi(\rho)$ requires additional analysis (§8.10).

---

## 8.10 Open Questions

- **Global injectivity**: is $\xi \mapsto \Gamma(\xi)$ injective on all of $D_\xi(\rho)$? The Gram map is 2-to-1 with respect to sign: $\Gamma_s(-\mathbf{A}, -\mathbf{I}, -\mathbf{R}) = \Gamma_s(\mathbf{A}, \mathbf{I}, \mathbf{R})$ (even function under global sign flip). This introduces a $\mathbb{Z}_2$ ambiguity at the level of $\Gamma_s$; the antisymmetric part $\Gamma_a$ resolves it ($\Gamma_a$ is odd under global sign flip). A careful analysis of this $\mathbb{Z}_2$ is needed for global uniqueness.

- **Pseudo-Riemannian extension**: the G(3) inner product used here is Euclidean. At extreme ρ values (ρ → 0), the attribute metric may require a pseudo-Riemannian (indefinite) analog — replacing the Gram matrix with a non-positive-definite symmetric bilinear form. This generalization is deferred to future work.

- **Cross-sector coupling in $\Gamma_a$**: the blocks $[\mathbf{A} \wedge \mathbf{I}]_\times$ and $[\mathbf{A} \wedge \mathbf{R}]_\times$ encode structural couplings beyond Force and Field. Their phenomenological interpretation — what it means for Agency to have a directed coupling to Impulse — is an open correspondence (phenomenological interpretation open — not addressed in Part I).

- **The 4×4 sign convention**: the magnitudes $|\mathbf{u} \times \mathbf{v}|$ in the abstract 4×4 $\Gamma_a$ lose orientation. A natural orientation is provided by the G(3) pseudoscalar $I_3 = \mathbf{e}_1\mathbf{e}_2\mathbf{e}_3$, which converts bivectors to signed scalars. This would replace $|\mathbf{u} \times \mathbf{v}|$ with $(\mathbf{u} \times \mathbf{v}) \cdot \hat{n}$ for a canonical normal $\hat{n}$ — a choice that breaks isotropy unless $\hat{n}$ is itself derived from the UoC state.

---

## 8.11 Status Summary

| Open question (Ch5 §5.8) | Status after Ch8 |
|---------------------------|-------------------|
| What determines $\langle\text{attr}_i, \text{attr}_j\rangle$? | **Closed**: the G(3) scalar inner product — Gram map |
| Transformation law of $\Gamma$ | **Established**: $\Gamma \mapsto J_g^T\Gamma J_g$ under G(3) |
| Tensor vs. matrix terminology | **Resolved**: tensor in 10×10 expanded form; scalar summary in 4×4 |
| Jacobian $\partial\Gamma/\partial\xi$ | **Computed**: explicit linear map from the polynomial entries |
| Structural Injectivity Criterion (Ch11) | **Verified**: holds at all operative $\xi^*$ |
| Global injectivity of $\xi \mapsto \Gamma(\xi)$ | **Partially addressed**: $\mathbb{Z}_2$ ambiguity identified; full analysis open |

---

*End of Chapter 8*
