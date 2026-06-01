# Chapter 2: Attribute Space and Grade Structure

## 2.1 The Question

Chapter 1 introduced the four intrinsic variables S, **A**, **I**, **R** and labeled S as a scalar and the rest as vectors, without justification. This chapter argues for that structure from the variables' functional roles and from the operations that must be well-defined for the UoC to exist as described. The argument does not constitute a formal derivation in the mathematical sense; it is a rational reconstruction — a demonstration that the chosen types are the minimal ones consistent with the structural requirements. The grade and dimension assignments are the preferred hypothesis under a minimality criterion, not theorems.

The argument proceeds in two steps:

1. **Grade argument**: the structural role of each variable determines its mathematical type (scalar vs. vector).
2. **Space argument**: the operations required to produce the inherent variables determine the minimal dimension of the configuration space.

---

## 2.2 Grade Argument: What Type Must Each Variable Be?

Each intrinsic variable answers a structural question. The mathematical type of each variable is determined by the kind of answer that question requires.

### 2.2.1 Singularity is a Scalar

S answers: *to what degree does this UoC distinguish itself from its environment?*

This is a question of **magnitude without direction**. The boundary between self and non-self has extent — it can be stronger or weaker — but it does not point anywhere in configuration space. There is no privileged direction for self-differentiation; it is a property of degree, not of orientation.

Formally: if S had a direction, one would need to ask "the boundary points toward what?" — but there is no structural referent for that direction prior to the other variables being defined. S is logically prior to directionality.

*Note*: The ordering — S as logically prior to A, I, R — is a structural design choice, not a formal derivation. It reflects the intuition that self-demarcation is a precondition for any directed activity. A framework that treated directionality as prior and boundary as derived could not be excluded on purely formal grounds; the present ordering is adopted as the minimal generative sequence consistent with the UoC's structural definition (§1.2).

> **S is a scalar (grade 0).**

### 2.2.2 Agency, Impulse, and Relation are Vectors

Each of **A**, **I**, **R** answers a directional question:

- **A**: *toward what can this UoC act?* — not just "can it act" (magnitude) but "act in which directions" (orientation in the space of possible transformations).
- **I**: *toward where does this UoC tend by its own nature?* — intrinsic orientation presupposes a direction, not just a magnitude of motivation.
- **R**: *with what and in what mode does this UoC exchange?* — exchange has a target and a mode; it is oriented.

Force and Field are **inherent variables** of every operative UoC (Ch1 §1.4): they are not optional derived quantities but constitutive operations that cannot be absent when the UoC exists. Because they are inherent, their being well-defined is not a desirable property — it is a structural requirement. This is what makes the grade argument binding.

The argument for grade-1 (vector) type is not that a scalar Agency would mean no capacity — a scalar could represent capacity without a preferred direction, uniform across all orientations. The argument is that scalar type is structurally incompatible with well-defined Force and Field:

- **If A were scalar**: Force = S·**A** would be the product of two scalars — a scalar. A scalar Force has no direction; the UoC could not produce oriented transformations in its configuration space. The directional information that Force must carry (toward what the UoC acts) would be structurally absent.
- **If I were scalar**: Field = **I** × **R** would require a cross product between a scalar and a vector — an operation that is not defined in standard vector algebra. Field would be undefined.
- **If R were scalar**: same — Field = **I** × **R** would be undefined.

A scalar type for any of these three variables is therefore not merely insufficient but structurally incompatible with the requirement that Force and Field be well-defined. The requirement is not that agency "has direction" in the semantic sense — it is that the formal operations defining the inherent variables must be well-typed.

**Why grade-1 vectors and not higher-order tensors?** Grade-1 (vectors) is the minimal mathematical structure that supports direction. Higher-grade objects (tensors of order 2 or above) encode relations *between* directions — they describe how one direction maps onto another, which introduces structure that is not required at the level of the four intrinsic variables. A tensor of order 2 for Agency would mean Agency has internal relational structure between its components; there is no structural argument for this at the ontological level. Grade-1 is the minimum sufficient type for a property that has magnitude and direction but no internal directional relations.

> **A, I, R are vectors (grade 1): the minimal mathematical type for a directional intrinsic variable.**

---

## 2.3 Space Argument: What is the Minimal Dimension?

Given that **A**, **I**, **R** are vectors, they must live in some vector space V. The dimension of V is constrained by the operations required to produce the inherent variables.

### 2.3.1 Force = S**A** constrains nothing about dimension

Force is a scalar multiplication: S scales **A** without changing its direction. This operation is defined in any vector space of any dimension. Force does not constrain the dimension of V.

### 2.3.2 Field = I × R constrains the dimension to 3

**Postulate 2.1 (Field Homogeneity)**: Field is a structural property of the UoC that lives in the same space as the intrinsic variables **I** and **R**. That is, Field ∈ ℝⁿ for the same n as **I** and **R**.

*Motivation*: Field characterizes the structural atmosphere in which the UoC operates (§1.4). For it to act on the same configuration space as the other variables — for the UoC to be able to orient itself with respect to its own field — Field must be an element of the same grade-1 subspace as **I** and **R**.

The natural product of two vectors in geometric algebra is the wedge product **I**∧**R**, a *bivector* of grade 2. A bivector represents an oriented plane element and lives in a subspace distinct from the grade-1 vectors. If Field were a bivector, it would (i) be well-defined in any dimension ≥ 2, which would eliminate the dimensionality constraint of §2.3.2, and (ii) require the UoC to have a grade-2 capacity for self-orientation at the ontological level — a richer structure not justified at this stage.

Postulate 2.1 restricts Field to grade 1 by requiring homogeneity with the intrinsic vectors. This is a design postulate, not a derived result. Under this postulate, Field = **I**×**R** is the Hodge dual of the bivector **I**∧**R** — a grade-1 object in the same space as **A**, **I**, **R**. The postulate can be revised if a more general structure (e.g., a bivector Field) proves necessary.

Given Postulate 2.1, the cross product must map V × V → V.

This is a non-trivial constraint. The classical result (Eckmann, 1943) states that a bilinear, antisymmetric, norm-preserving product V × V → V — i.e., a product that is (i) bilinear, (ii) antisymmetric, (iii) satisfies |u×v|² = |u|²|v|² − (u·v)², and (iv) maps into the same space V — exists only in dimensions **1**, **3**, and **7**.

- **Dimension 1**: a cross product u×v is trivially zero for all u, v (no perpendicular direction exists). Field = 0 identically — degenerate. ✗
- **Dimension 2**: the "cross product" of two vectors produces a scalar (the component out of the plane) — Field would not be a vector in V. ✗
- **Dimension 3**: the cross product produces a unique vector perpendicular to both **I** and **R**, within V. ✓
- **Dimension 7**: the cross product also maps V × V → V, but it is not unique — there are multiple inequivalent cross products, related to the imaginary units of the octonions (G₂ structure). This introduces ambiguity in the definition of Field. ✗ (by parsimony)
- **Dimension > 7**: no such product exists. ✗

The minimal dimension in which Field is a well-defined, unambiguous vector is **3**, given Postulate 2.1.

> **The configuration space V is 3-dimensional: A, I, R ∈ ℝ³.**

### 2.3.3 The Perpendicularity of Field

An immediate consequence of Field being a cross product in ℝ³ is that **Field is perpendicular to both I and R**. This means:

- Field points in a direction that is neither the direction of impulse nor the direction of relation.
- Field represents a *new structural direction* — one that emerges from the tension between **I** and **R** but is not reducible to either.

This is the geometric content of the "structural atmosphere" introduced in §1.4: the UoC's field operates in a direction orthogonal to both its intrinsic motivation and its relational mode.

---

## 2.4 The Configuration Space

The configuration space of a UoC is the space of all possible states of its intrinsic variables. Given the derivation above:

$$\mathcal{V} = \mathbb{R} \times \mathbb{R}^3 \times \mathbb{R}^3 \times \mathbb{R}^3$$

where:
- S ∈ ℝ (scalar)
- **A** ∈ ℝ³ (vector)
- **I** ∈ ℝ³ (vector)
- **R** ∈ ℝ³ (vector)

A specific state of a UoC is a point $\xi = (S, \mathbf{A}, \mathbf{I}, \mathbf{R}) \in \mathcal{V}$ — the primary state vector introduced in Ch1 §1.5. The state vector $\xi$ encodes the point in $\mathcal{V}$; from it, the configuration matrix $\Gamma(\xi) \in \mathrm{Sym}(4) \oplus \mathfrak{so}(4)$ encodes the pairwise coupling structure between the intrinsic variables (defined in Ch5). These are two distinct objects: $\xi$ is the primary state; $\Gamma(\xi)$ is the derived coupling structure.

**Important clarification**: 𝒱 is not physical space. The three dimensions of each vector are dimensions of the UoC's *configuration space* — modes of agency, orientation, and exchange — not spatial coordinates.

---

## 2.5 Summary of the Vectorial Structure

| Variable | Type | Space | Grade argument (§2.2) | Dimension argument (§2.3) |
|----------|------|-------|-----------------------|--------------------------|
| S | Scalar | ℝ | Magnitude without direction; logically prior | — |
| **A** | Vector | ℝ³ | Force = S·**A** requires vector type | ℝ³ by §2.3.2 |
| **I** | Vector | ℝ³ | Field = **I**×**R** requires vector operands | ℝ³ by §2.3.2 |
| **R** | Vector | ℝ³ | Field = **I**×**R** requires vector operands | ℝ³ by §2.3.2 |
| Force = S**A** | Vector | ℝ³ | Scalar scaling of **A**; preserves grade | — |
| Field = **I**×**R** | Vector | ℝ³ | Hodge dual of bivector **I**∧**R**; grade 1 by Postulate 2.1 | Requires ℝ³ by §2.3.2 |

*Note*: The grade-1 assignment for **A**, **I**, **R** follows from §2.2 alone. The ℝ³ assignment requires §2.3 additionally (specifically Postulate 2.1 and the cross-product constraint).

---

## 2.6 The Geometric Algebra Structure

The combination of one scalar and three vectors in ℝ³ is not arbitrary. It is precisely the grade structure of the **geometric algebra G(3)** — the Clifford algebra of 3-dimensional space.

**Clarification on generators vs. elements.** The generators of G(3) are the three orthonormal basis vectors {**e**₁, **e**₂, **e**₃} of ℝ³. **A**, **I**, **R** are not generators — they are grade-1 *elements* of G(3), expressible as linear combinations of {**e**₁, **e**₂, **e**₃}. S is a grade-0 element (a scalar multiple of the identity). For the algebraic structure of G(3) to apply, **A**, **I**, **R** are assumed to be linearly independent — forming a basis for the grade-1 subspace — and the configuration space is assumed to carry the standard Euclidean metric, which is a minimal hypothesis. Under this hypothesis, the four intrinsic variables span all grades of G(3):

| Grade | Elements | Dimension | Relation to UoC |
|-------|----------|-----------|-----------------|
| 0 | 1 scalar | 1 | S |
| 1 | 3 vectors | 3 | **A**, **I**, **R** (assumed basis) |
| 2 | 3 bivectors | 3 | **A**∧**I**, **A**∧**R**, **I**∧**R** (= Field via Hodge dual) |
| 3 | 1 pseudoscalar | 1 | **A**∧**I**∧**R** (oriented volume) |
| **Total** | | **8 = 2³** | |

The cross product **I**×**R** is the Hodge dual of the wedge product **I**∧**R** — a grade-2 bivector mapped to a grade-1 vector using the Euclidean metric and orientation of ℝ³ (the Hodge dual presupposes both). This is why Field is a vector in ℝ³ under Postulate 2.1: the metric structure of the configuration space supports the duality between grade-2 and grade-1 objects.

*Observation*: Under the linear independence assumption, the four intrinsic variables span the full grade structure of G(3) — every grade is occupied. The sufficiency argument (no fifth variable is needed at the ontological level) is developed in Ch3.

---

## 2.7 Scope and Open Questions

- **Why ℝ³ and not ℝ⁷?** The 3-dimensional configuration space is adopted as the minimal hypothesis under Postulate 2.1. The 7-dimensional case — where the cross product also maps V×V → V, via the octonionic G₂ structure — is not formally excluded. A 7-dimensional extension would be the natural next step if ℝ³ proves insufficient for the full range of UoC configurations. This is left as an open question for future investigation.

- **Why a vector Field and not a bivector?** Under Postulate 2.1, Field is required to be grade-1 (a vector in the same space as **I** and **R**). The natural geometric product of two vectors is the bivector **I**∧**R** (grade 2). If Field were allowed to be a bivector, the dimensionality constraint of §2.3.2 would collapse — bivectors are well-defined in any dimension ≥ 2. The restriction to grade-1 is therefore the load-bearing hypothesis of the entire space argument; its revision would require rethinking the dimension derivation from the ground up.

- **Why ℝ³ and not a curved 3-manifold?** The configuration space is assumed flat (ℝ³) as the minimal hypothesis. Curvature could be introduced if the dynamics of ξ(t) require it; this is left for future work.

- **Linear independence of A, I, R**: assumed in §2.6 but not derived. Whether the configuration space can support degenerate configurations (e.g., **A** ∥ **I**) is a structural question; such configurations are not excluded from 𝒱 but may correspond to pathological UoC states (Field = 0; see §2.3.3 and Ch1 §1.4.1).

- **Construction of Γ(ξ)**: the explicit form of the configuration matrix as a functional of the state vector is developed in Ch5.


- **Sufficiency of the four variables**: the grade structure in §2.6 suggests that {S, **A**, **I**, **R**} span all of G(3). The formal sufficiency argument (no fifth ontological variable adds expressive power) is Ch3.

---

*End of Chapter 2*
