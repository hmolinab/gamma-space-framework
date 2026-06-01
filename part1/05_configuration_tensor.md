# Chapter 5: The Configuration Matrix

## 5.1 From Postulate to Formalization

Ch1 introduced Γ as a postulate:

> **Postulate 1.1**: The complete state of a UoC at any moment is encoded in a structured mathematical object Γ, called the **configuration tensor**. [...] The full algebraic constitution of Γ is deferred to future development.

Ch2 partially specified it — Γ must encode the metric of ℝ³ and the operations Force and Field — but left the internal structure open (§2.7). Ch3 expressed the state as a paravector M = S + V in G(3), which captured the algebraic generation of Force and Field but did not formalize the relational structure between variables.

This chapter provides a structural parameterization of Γ at the coupling level: **Γ encodes not the values of the intrinsic variables but the structural couplings between them**. The explicit functional form Γ(ξ) — how the coupling structure is determined by the state — is derived in Ch8 via the Gram construction.

---

## 5.2 The Attribute Space

A UoC has four intrinsic variables: S (Singularity), **A** (Agency), **I** (Impulse), **R** (Relation). For the purpose of the coupling structure, these are treated as the four **attributes** of the UoC, indexed as:

$$\{0, 1, 2, 3\} \leftrightarrow \{S,\, \mathbf{A},\, \mathbf{I},\, \mathbf{R}\}$$

**Abstract vs. expanded form.** In the abstract 4-index form, each attribute is treated as a single unit regardless of its internal dimension (S is scalar, **A**, **I**, **R** are vectors in ℝ³). In the full expanded form, the actual dimensionalities are respected: S contributes 1 component and each vector contributes 3, yielding a 10-dimensional configuration space 𝒱 = ℝ¹ × ℝ³ × ℝ³ × ℝ³. The 4×4 abstract matrix is the conceptual skeleton; the 10×10 expanded matrix is its full realization. Both are presented below; the 4×4 form is primary for structural analysis, the 10×10 for formal derivations.

---

## 5.3 Definition: The Configuration Matrix

**Definition 5.1 (Configuration Matrix).** The configuration matrix Γ of a UoC is a matrix whose entry Γ_ij encodes the **structural coupling** between attribute *i* and attribute *j*:

*Terminological note*: Prior chapters used "configuration tensor" (Postulate 1.1, Ch1) as a forward reference to this object. The term "tensor" is retained in that context for its intuitive connotation of structured, relational content. In the strict mathematical sense, a tensor requires a specified transformation law under change of basis (Γ' = TΓT⁻¹ or equivalent); this transformation law is not established in the current chapter and is deferred to future development. "Configuration matrix" is used throughout this chapter for precision; the two terms refer to the same object.

$$\Gamma_{ij} = \text{coupling between attribute } i \text{ and attribute } j$$


**Abstract 4×4 form:**

$$\Gamma = \begin{pmatrix} c_S & \gamma_{SA} & \gamma_{SI} & \gamma_{SR} \\ \gamma_{AS} & c_A & \gamma_{AI} & \gamma_{AR} \\ \gamma_{IS} & \gamma_{IA} & c_I & \gamma_{IR} \\ \gamma_{RS} & \gamma_{RA} & \gamma_{RI} & c_R \end{pmatrix}$$

where the diagonal entries $c_S, c_A, c_I, c_R > 0$ represent the **self-coherence** (or self-intensity) of each attribute — the degree to which each attribute is internally coherent — and each off-diagonal entry $\gamma_{ij} \in \mathbb{R}$ is the coupling coefficient between attributes $i$ and $j$. *For a structurally operative UoC, the diagonal entries are assumed positive ($c_X > 0$ for all $X$); the degenerate case $c_X \to 0$ is analyzed in §5.6.* The sign of off-diagonal entries is given a semantic interpretation — positive coupling is constructive (synergistic), negative is destructive (antagonistic), zero is structural independence — this is a postulate of interpretation, not a derived result.

**Full 10×10 expanded form.** When the vector structure of **A**, **I**, **R** is respected, each scalar coupling γ_ij between vector attributes expands into a 3×3 block **Γ**_ij, and each coupling between S and a vector attribute expands into a 1×3 block. The full tensor is:

$$\Gamma^{(10)} = \begin{pmatrix} \Gamma_{SS} & \boldsymbol{\Gamma}_{SA}^T & \boldsymbol{\Gamma}_{SI}^T & \boldsymbol{\Gamma}_{SR}^T \\ \boldsymbol{\Gamma}_{SA} & \mathbf{\Gamma}_{AA} & \mathbf{\Gamma}_{AI} & \mathbf{\Gamma}_{AR} \\ \boldsymbol{\Gamma}_{SI} & \mathbf{\Gamma}_{IA} & \mathbf{\Gamma}_{II} & \mathbf{\Gamma}_{IR} \\ \boldsymbol{\Gamma}_{SR} & \mathbf{\Gamma}_{RA} & \mathbf{\Gamma}_{RI} & \mathbf{\Gamma}_{RR} \end{pmatrix}$$

where **Γ**_SA ∈ ℝ³, **Γ**_AA, **Γ**_AI, **Γ**_IR, ... ∈ ℝ^{3×3}, and Γ_SS ∈ ℝ.

**Note on completeness.** The abstract 4×4 form captures coupling structure at the attribute level. The 10×10 form captures the full internal geometry, including how Agency couples to each component of Impulse, etc. The 4×4 form is the conceptual skeleton for qualitative structural analysis; the 10×10 form is required for formal derivations involving the internal vector geometry of each attribute. Qualitative structural interpretations (coupling patterns, symmetry-antisymmetry decomposition, degenerate configurations) carry over from 4×4 to 10×10, but spectral and rank properties — eigenvalues, determinant, positive-definiteness conditions — must be re-evaluated in the expanded representation, as block expansion can alter these significantly. Unless otherwise noted, results in this chapter use the 4×4 form.

---

## 5.4 The Symmetric-Antisymmetric Decomposition

Any square matrix admits a unique decomposition into symmetric and antisymmetric parts:

$$\Gamma = \Gamma_s + \Gamma_a$$

$$\Gamma_s = \frac{\Gamma + \Gamma^T}{2} \qquad \Gamma_a = \frac{\Gamma - \Gamma^T}{2}$$

with $\Gamma_s^T = \Gamma_s$ and $\Gamma_a^T = -\Gamma_a$ (diagonal of Γ_a is identically zero).

These two parts have distinct structural roles.

### 5.4.1 The Symmetric Part: Structural Coordination

Γ_s captures **mutual coordination** between attributes — the degree to which each pair of attributes supports each other's expression, without directionality. Γ_s_ij = Γ_s_ji: the coordination of *i* with *j* equals the coordination of *j* with *i*.

$$\Gamma_s = \begin{pmatrix} c_S & \gamma^s_{SA} & \gamma^s_{SI} & \gamma^s_{SR} \\ \gamma^s_{SA} & c_A & \gamma^s_{AI} & \gamma^s_{AR} \\ \gamma^s_{SI} & \gamma^s_{AI} & c_I & \gamma^s_{IR} \\ \gamma^s_{SR} & \gamma^s_{AR} & \gamma^s_{IR} & c_R \end{pmatrix}$$

$\Gamma_s$ may be interpreted as a measure of structural coherence of the UoC — how coherently all four attributes are coordinated. *(Candidate phenomenological label: "structural health matrix"; this is an interpretive analogy, not a mathematical property.)* A $\Gamma_s$ close to a diagonal matrix (small off-diagonals) corresponds to weak inter-attribute coordination and high structural independence — attributes act largely without mutual support. High coordination corresponds to large coherent off-diagonal structure: each attribute's expression is strongly modulated by the others. A low-rank $\Gamma_s$ corresponds to strongly correlated or collapsed structural modes — the attribute space has collapsed to a lower-dimensional subspace. The intermediate range — non-trivially correlated but full-rank — characterizes the operationally rich UoC.

### 5.4.2 The Antisymmetric Part: Field Generation

Γ_a captures **directed coupling** between attributes — the degree to which attribute *i* drives attribute *j* in a way that is not reciprocated symmetrically. Γ_a_ij = −Γ_a_ji.

$$\Gamma_a = \begin{pmatrix} 0 & \gamma^a_{SA} & \gamma^a_{SI} & \gamma^a_{SR} \\ -\gamma^a_{SA} & 0 & \gamma^a_{AI} & \gamma^a_{AR} \\ -\gamma^a_{SI} & -\gamma^a_{AI} & 0 & \gamma^a_{IR} \\ -\gamma^a_{SR} & -\gamma^a_{AR} & -\gamma^a_{IR} & 0 \end{pmatrix}$$

**Force and Field are structurally associated with the principal entries of Γ_a, but the nature of that association differs between the two:**

- **γ^a_{SA}**: parameterizes the directional asymmetry of the S–**A** relationship. S acts on **A** to generate Force; **A** does not act symmetrically on S. The entry γ^a_{SA} = −γ^a_{AS} encodes this structural directionality within Γ_a. In the 10×10 form, the S–**A** block of Γ_a is a 1×3 vector whose direction aligns with the generated Force. The underlying algebraic operation is Force = S·**A** (Ch1 §1.4); γ^a_{SA} represents the matrix encoding of that asymmetry, not the operation itself.

- **$\Gamma^a_{IR}$**: the antisymmetric 3×3 block of the **I**–**R** coupling. Here the connection to Field is algebraically exact: every 3×3 antisymmetric matrix corresponds uniquely to a vector in ℝ³ via the Levi-Civita isomorphism, $(\Gamma^a_{IR})_{jk} = \sum_{i=1}^{3} \varepsilon_{jki}\, F_i$, equivalently written $\Gamma^a_{IR} = [\mathbf{F}]_\times$ where $[\cdot]_\times$ denotes the skew-symmetric matrix operator. This gives $\Gamma^a_{IR} \leftrightarrow \mathbf{Field} = \mathbf{I} \times \mathbf{R}$ directly. The cross product is encoded in the antisymmetric block, not merely parameterized by it.

*Note on the asymmetry between Force and Field.* Force (grade-0 acting on grade-1) and Field (grade-1 × grade-1 via cross product) are algebraically distinct operations, and their representation in Γ_a reflects this: γ^a_{SA} parameterizes the S→A asymmetry, while Γ^a_{IR} encodes Field exactly. This asymmetry is resolved in Ch8 §8.4, where the 10×10 Gram map shows that (Γ_a^(10))_{SA} = S·**A** = Force exactly — closing the gap noted in Proposition 5.1.

**Proposition 5.1.** *In the structurally operative regime (Definition 5.2), Force and Field are independently determined by the intrinsic variables and cannot both be absent. Both are encoded in $\Gamma_a$: Field via the exact Levi-Civita isomorphism ($\Gamma^a_{IR} \leftrightarrow$ **I**×**R**); Force via the directional asymmetry of the S–**A** block, recovered exactly as $S\cdot\mathbf{A}$ in the 10×10 Gram form (Ch8 §8.4). Neither can be absent when the UoC is structurally operative — they vanish only in the degenerate configurations of §5.6.*

This result formalizes the claim of Ch1 that Force and Field are *inherent* variables: they cannot be absent when the UoC is operative because they are determined by the intrinsic variables, which exist whenever the UoC exists.

---

## 5.5 Structural Properties

### 5.5.1 Determinant

The determinant of Γ is a scalar indicator of whether all four attributes span a non-degenerate configuration. *(Candidate interpretive label: "structural generativity"; this is a semantic assignment, not a derived property of det.)*

$$\det(\Gamma) > 0: \text{ necessary condition for structural operativity (not sufficient — see §5.5.2)}$$
$$\det(\Gamma) = 0: \text{ sufficient condition for at least one degenerate structural mode}$$

*Note*: det(Γ) > 0 alone does not guarantee operativity — an indefinite matrix can have positive determinant while having negative eigenvalues. The complete criterion is given by the eigenvalue conditions of §5.5.2; det(Γ) is a useful scalar summary, not the full diagnostic.

det(Γ) = 0 can arise from three structurally distinct causes:

| Cause | Mechanism | Phenomenological expression |
|-------|-----------|----------------------------|
| $c_S \to 0$ | S decoupled from all attributes → S-row/column collapses | *(candidate)* UoC cannot express identity |
| **I** ∥ **R** | $\Gamma^a_{IR} \to 0$ → Field block vanishes | *(candidate)* UoC cannot orient toward purpose |
| Linear dependence in S–**A** coupling | $\gamma^a_{SA}$ becomes linearly dependent with other columns | Force–Field decoupling *(mechanism requires case-specific argument; listed as a candidate cause, not a derived result)* |

The first two collapse modes have clear matrix-level mechanisms (row/column collapse and antisymmetric block collapse). The third requires a specific configuration to force $\det(\Gamma) = 0$ and is listed as a candidate structural cause. A UoC can collapse via any one while the others remain operative.

### 5.5.2 Eigenvalues and Structural Modes

Since $\Gamma = \Gamma_s + \Gamma_a$ with $\Gamma_a$ antisymmetric, the full matrix $\Gamma$ is generally non-symmetric and has complex eigenvalues (the antisymmetric part contributes purely imaginary eigenvalues). The real structural content is carried by the symmetric part $\Gamma_s$.

The eigenvalues $\lambda_1, \lambda_2, \lambda_3, \lambda_4$ of **$\Gamma_s$** are the **structural modes** of the UoC. Being eigenvalues of a real symmetric matrix, they are real. Each eigenvalue measures the strength of an independent mode of attribute coordination.

$$\det(\Gamma_s) = \prod_{i=1}^{4} \lambda_i$$

*Note*: The sign semantics — "all $\lambda_i > 0$ means four fully active structural modes" — is an interpretive postulate linking spectral positivity to operational activity; it is not derived from the dynamical equations (developed in subsequent chapters).

A $\Gamma_s$ with all $\lambda_i > 0$ (i.e., $\Gamma_s \succ 0$) has four fully active structural modes — all four attributes participate in independent coordination patterns. A $\Gamma_s$ with some $\lambda_i \approx 0$ has degenerate modes: the corresponding degrees of freedom are structurally collapsed.

The eigenvectors identify *which combinations of attributes* constitute each structural mode. This is the formal basis for future work on structural decomposition of complex UoC configurations (e.g., the ego-soul-body co-presence of Ch4).

---

## 5.6 Operative and Degenerate Structural Configurations

*Notational convention.* In this chapter: $\gamma_{ij} \in \mathbb{R}$ denotes a scalar coupling coefficient between two attributes; $\Gamma^a_{IR}$ (capital Γ with superscript) denotes a matrix block. This distinction is maintained throughout.

**Definition 5.2 (Structurally Operative UoC).** A UoC is structurally operative if and only if:

1. $\Gamma_s \succ 0$ — the symmetric coordination matrix is positive definite (no degenerate coordination modes); this condition is stated for $\Gamma_s$, not for $\Gamma$ total, since the antisymmetric part $\Gamma_a$ has purely imaginary eigenvalues and does not contribute to real positive-definiteness
2. **I** ∦ **R** — Field is operative (Operativity Condition, Ch1 §1.4.1)

*Note on invertibility*: $\Gamma_s \succ 0$ implies $\operatorname{rank}(\Gamma) = 4$ — i.e., $\Gamma$ is automatically invertible. *Note on linear independence*: by the Gram construction of Ch8, $\Gamma_s \succ 0$ is equivalent to $S \neq 0$ and $\{\mathbf{A},\mathbf{I},\mathbf{R}\}$ linearly independent (Ch8 Proposition 8.1). The operative condition therefore subsumes the linear independence assumption of Ch2 §2.6 — it is a consequence, not an additional hypothesis. Proof: suppose $\Gamma v = 0$. Then $(\Gamma_s + \Gamma_a)v = 0$. Taking the inner product with $v$: $v^T\Gamma_s v + v^T\Gamma_a v = 0$. Since $\Gamma_a$ is antisymmetric, $v^T\Gamma_a v = 0$. Therefore $v^T\Gamma_s v = 0$. Since $\Gamma_s \succ 0$, this forces $v = 0$. Hence $\Gamma$ is invertible. The rank condition is listed explicitly in some expositions for conceptual clarity but follows from condition 1.

*Note*: $\operatorname{det}(\Gamma_s) > 0$ follows from condition 1 and is a necessary consequence, not an independent condition.

**Definition 5.3 (Degenerate Structural Configuration).** A UoC is in a degenerate structural configuration if any of the above conditions fails. The term "degenerate" refers to the structural state of the matrix, not to a clinical or normative judgment about the UoC.

**Remark 5.1 (Necessity of $\Gamma_s \succ 0$ from Ch10 — forward reference).** The condition $\Gamma_s \succ 0$ is not merely a structural definition — it is a necessary consequence of the UoC having well-defined purpose-oriented dynamics. Ch10 Theorem 10.1 establishes the overdamped evolution law:

$$\dot\xi = -M\,\nabla P, \qquad M = \frac{1}{\gamma}\,\Gamma_s^{-1}$$

For $M$ to be the Onsager mobility tensor — positive definite, ensuring Lyapunov descent $\dot P \leq 0$ — one needs $M \succ 0$. Since $\gamma > 0$, this requires $\Gamma_s \succ 0$. A UoC with singular or indefinite $\Gamma_s$ cannot sustain gradient-flow dynamics toward $\xi^*$: the mobility $M$ is undefined or loses its dissipative character, and the purpose function $P$ ceases to be a Lyapunov function.

The operative condition is therefore the structural translation of the requirement that the UoC have attractor dynamics. This also closes the interpretive postulate of §5.5.2: $\lambda_i(\Gamma_s) > 0$ for all $i$ is not an interpretive label — it is the spectral expression of the condition that $M$ exists and drives $\xi$ toward $\xi^*$.

### 5.6.1 Case Analysis

The configuration matrix makes precise the structural signature of each degenerate state. Each case describes a configuration of Γ — a structural state of the UoC. Epistemological modulation (Γ_E) is one mechanism that can produce these states; external contextual forcing is another. The structural signatures are cause-agnostic.

**Singularity-suppressed configuration:**

S_eff approaches zero while **A**, **I**, **R** remain structurally intact.

- Γ_SS_eff → 0, all S-coupling blocks → 0
- γ^a_SA → 0 → **Force**_eff → 0
- Γ^a_IR remains nonzero → **Field**_eff intact

*Structural signature:* $\operatorname{rank}(\Gamma_{\text{eff}}) < 4$ via collapse of the S-row and S-column. The I–R structural coupling (Field) remains operative; the S–A coupling (Force) does not. *(Candidate phenomenological interpretation: the UoC retains orienting capacity but cannot act; epistemological suppression of S makes Force inaccessible.)*

---

**Identity-overcoupled configuration (S–R overcoupling):**

S_eff inflated and anomalously coupled to R: $\text{S\_eff} \approx S + k|\mathbf{R}|$.

- γ_SR >> normal: S-R coupling anomalously large relative to S-intrinsic
- S_eff large → **Force**_eff amplified beyond structural capacity
- **I**_eff and **R**_eff redirect toward the self (identity validation) → tend toward parallel → **Field**_eff → 0

*Structural signature:* Γ exhibits a large γ_SR off-diagonal entry and a near-zero Γ^a_IR determinant. Force is amplified but Field collapses. The UoC acts powerfully (high Force) but generates no structural field — no genuine relational tension, no field in the structural sense.

*Diagnostic criterion in Γ:* γ_SR / γ_SS > threshold, with simultaneous γ^a_IR → 0.

---

**Agency-suppressed configuration:**

**A**_eff near-zero while S, **I**, **R** remain structurally intact.

- Γ_AA → near-zero or decoupled from **I** and **R**
- γ^a_SA → 0 via **A**_eff → 0 → **Force**_eff → 0
- **I**, **R** intact → **Field**_eff intact

*Structural signature:* S-self-coherence $c_S$ remains intact; only $c_A$ and its couplings collapse. The S–**A** Force pathway is severed while the **I**–**R** Field remains operative. *(Candidate phenomenological interpretation: ontological identity intact but agency cannot generate force; diagnosable by non-zero $c_S$ alongside near-zero $c_A$ entries.)*

---

**Field-collapsed configuration:**

**I**_eff and **R**_eff become parallel: the impulse toward one's own direction aligns with (or collapses onto) the relational mode.

- **Field**_eff = **I**_eff × **R**_eff → 0
- Γ^a_IR → 0 → the I-R block of Γ_a loses its cross-product content
- **Force** may remain intact

*Structural signature:* the $\operatorname{rank}$ of the antisymmetric I–R block $\Gamma^a_{IR}$ decreases — since $\Gamma^a_{IR}$ is a $3\times3$ antisymmetric matrix, its rank is either 2 (generic, Field operative) or 0 (Field collapsed). The collapse $\operatorname{rank}(\Gamma^a_{IR}) = 0$ is precisely the degenerate configuration of Ch1 §1.4.1 expressed in matrix form. The UoC can apply Force (act, respond) but cannot orient itself toward its structural attractor — the gradient-flow dynamics of Ch10 cannot drive $\xi$ toward $\xi^*$ in the absence of a Field direction.

---

**Summary table:**

| Configuration | S_eff | **A**_eff | Field_eff | Force_eff | $\lambda_{\min}$ | Signature in Γ |
|---------------|-------|-----------|-----------|-----------|--------|----------------|
| Soul (ρ → 0) | ≈ S | free | maximum | authentic | large | all modes active |
| Operative ego | referenced | conditioned | operative | moderate | positive | $\gamma_{SR}$ moderate |
| Singularity-suppressed | << S | intact | intact | ≈ 0 | → 0 | S-row collapsed |
| Identity-overcoupled | >> S, f(R) | redirected | → 0 | amplified | → 0 | $\gamma_{SR} \gg c_S$, $\Gamma^a_{IR} \to 0$ |
| Agency-suppressed | intact | << A | intact | ≈ 0 | → 0 | $\Gamma_{AA}$ decoupled |
| Field-collapsed | variable | intact | → 0 | variable | may decrease | $\operatorname{rank}(\Gamma^a_{IR}) = 0$ |

*Candidate phenomenological interpretations.* The configurations above are structural signatures in Γ; their identification with specific psychological states (ego, soul, depression, etc.) is a correspondence, not a derivation.

*Observation*: The singularity-suppressed and identity-overcoupled configurations both produce $\lambda_{\min} \to 0$ (one or more eigenvalues of $\Gamma_s$ approach zero), but through orthogonal structural mechanisms — S collapse vs. Field collapse. These are structurally distinct degenerate configurations with different eigenvector decompositions.

---

## 5.7 Relation to Prior Chapters

**Partially resolves Ch1 Postulate 1.1.** Γ is now structurally parameterized at the coupling level: the 4×4 (or 10×10) coupling matrix whose entries encode relationships between intrinsic variables. Force and Field are associated with the principal entries of Γ_a (Proposition 5.1). The explicit functional form Γ(ξ) and its transformation law are derived in Ch8; the full resolution of Postulate 1.1 is there.

**Resolves Ch2 §2.7.** "The full tensorial structure of Γ: Γ must encode the metric of ℝ³ and the operations it supports." The 10×10 expansion may encode metric-like couplings (via the 3×3 diagonal blocks Γ_AA, Γ_II, Γ_RR) and the cross product operation (via the antisymmetric off-diagonal blocks Γ^a_IR); whether these blocks constitute a proper metric requires establishing bilinearity, non-degeneracy, and basis covariance — not established in this chapter.

**Relation to G(3).** The paravector $M = S + \mathbf{A} + \mathbf{I} + \mathbf{R} \in G(3)$ (Ch3) encodes the state variables as a single algebraic object. The configuration matrix Γ is a distinct but related object: it encodes the effective bilinear coupling structure between the four intrinsic variables — analogous to a Gram-type matrix when the couplings arise from an inner product, but defined here as an abstract coupling structure (Definition 5.1) that need not derive from a fixed inner product form. These two representations are complementary: $M$ captures the algebraic generation of Force and Field; Γ captures the structural coordination between all pairs of variables.

**Dependence on ρ.** By the domain contraction of §4.2.2, each intrinsic variable X is constrained to D_X(ρ) ⊆ 𝒱_X. The configuration matrix inherits this dependence: Γ(ρ) is the coupling matrix of the variables as constrained by the contextual form factor. Higher ρ → smaller D_X(ρ) → more constrained coupling structure → Γ(ρ) approaches a lower-rank limit.

---

## 5.8 Open Questions

- **Dynamics of Γ**: how does the coupling matrix evolve over time? The state-space dynamics $d\xi/dt = f(\xi, \Gamma_E, \rho)$ of Ch1 §1.6 drive the intrinsic variables; the induced dynamics on $\Gamma$-space — how $\Gamma(\xi(t))$ evolves as $\xi$ moves — is the natural next step. This connects to attractor theory: what is the fixed point of $\Gamma(t)$ for a UoC at a given structural level $\rho$? (Ch10 addresses the state-space dynamics; the induced dynamics on Γ-space via $M_\Gamma$ of Ch11 §11.5 is the relevant object.)

- **The attribute metric**: what determines the inner product ⟨attr_i, attr_j⟩ that defines Γ_ij? This is equivalent to asking what determines the geometry of the attribute space. Thermodynamic coupling strength and the ρ gradient (§4.4) are candidate answers.

- **Transformation law**: under what change of basis does Γ transform as a proper tensor? Establishing this law — Γ' = TΓT⁻¹ or a more general covariant form — is the step that would promote the configuration matrix to a configuration tensor in the strict mathematical sense.

---

*End of Chapter 5*
