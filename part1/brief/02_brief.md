# Chapter 2: The Vectorial Formulation
*Condensed version — source: Ch2 of the full GSF*

---

## 2.1 The Question

Chapter 1 assigned mathematical types to the four intrinsic variables — S as scalar, **A**, **I**, **R** as vectors — without justification. This chapter argues for that assignment from the variables' functional roles and from the formal requirement that the inherent variables (Force, Field) be well-defined. The argument is a rational reconstruction under a minimality criterion, not a formal derivation.

Two steps: (1) grade argument — what type does each variable's structural role require? (2) space argument — what is the minimal dimension of the configuration space?

---

## 2.2 Grade Argument: What Type Must Each Variable Be?

### 2.2.1 Singularity is a Scalar

S answers: *to what degree does this UoC distinguish itself from its environment?* This is a question of magnitude without direction — the boundary between self and non-self has extent, not orientation. S is assigned grade 0 (scalar).

*Note*: the ordering of S as logically prior to **A**, **I**, **R** is a design choice: self-demarcation is treated as a precondition for directed activity. A framework that reversed this ordering cannot be excluded on purely formal grounds.

### 2.2.2 Agency, Impulse, and Relation are Vectors

Force and Field are **inherent variables** of every operative UoC (Ch1 §1.4) — constitutive operations that cannot be absent when the UoC exists. Because they are inherent, their being well-defined is a structural requirement, not a desirable property. This is what makes the grade argument binding.

The argument is not that a scalar Agency would mean no capacity — a scalar could represent capacity uniform across all directions. The argument is that scalar type is incompatible with well-defined Force and Field:

- **If A were scalar**: Force = S·**A** would be a scalar (product of two scalars). A scalar Force carries no direction; the UoC could not produce oriented transformations.
- **If I were scalar**: Field = **I** × **R** would require a cross product between a scalar and a vector — undefined in standard vector algebra.
- **If R were scalar**: same — Field = **I** × **R** undefined.

Grade-1 (vector) is also the minimal type for a directional variable: higher-grade objects (tensors of order ≥ 2) encode relations *between* directions, introducing structure not required at the ontological level.

> **A, I, R are vectors (grade 1): the minimal type for which Force and Field are well-typed.**

---

## 2.3 Space Argument: What is the Minimal Dimension?

### 2.3.1 Force = S·A Does Not Constrain Dimension

Scalar multiplication is defined in any vector space of any dimension. Force places no constraint on the dimension of V.

### 2.3.2 Field = I × R Constrains the Dimension to 3

**Postulate 2.1 (Field Homogeneity)**: Field lives in the same grade-1 subspace as **I** and **R**.

The natural geometric product of two vectors is the wedge product **I**∧**R** — a bivector of grade 2, living in a distinct subspace. If Field were a bivector, it would be well-defined in any dimension ≥ 2, eliminating the dimensionality constraint entirely. Postulate 2.1 requires Field to be grade-1, which forces the cross product **I**×**R** as the Hodge dual of **I**∧**R**. This restriction is a design postulate — the load-bearing hypothesis of the entire space argument.

Under Postulate 2.1, the cross product must map V × V → V. The classical result (Eckmann, 1943) establishes that such a product — bilinear, antisymmetric, and norm-preserving — exists only in dimensions 1, 3, and 7:

| Dimension | Result | Status |
|-----------|--------|--------|
| 1 | Cross product trivially zero | Degenerate ✗ |
| 2 | Cross product produces a scalar | Not in V ✗ |
| **3** | **Unique vector perpendicular to both I and R** | **✓** |
| 7 | Vector in V, but not unique (octonionic G₂ structure) | Ambiguous ✗ |
| > 7 | No such product exists | ✗ |

The minimal unambiguous dimension is **3**.

### 2.3.3 The Perpendicularity of Field

Field is perpendicular to both **I** and **R** — a new structural direction that emerges from their tension but is not reducible to either. Field vanishes when **I** ∥ **R** and is maximized when **I** ⊥ **R**.


---

## 2.4 The Configuration Space

$$\mathcal{V} = \mathbb{R} \times \mathbb{R}^3 \times \mathbb{R}^3 \times \mathbb{R}^3$$

A state of a UoC is a point $\xi = (S, \mathbf{A}, \mathbf{I}, \mathbf{R}) \in \mathcal{V}$ — the primary state vector. From $\xi$, the configuration matrix $\Gamma(\xi) \in \mathrm{Sym}(4) \oplus \mathfrak{so}(4)$ encodes the pairwise coupling structure (Ch5). These are two distinct objects: $\xi$ is the state; $\Gamma(\xi)$ is the derived coupling structure.

$\mathcal{V}$ is not physical space. Its three dimensions are modes of agency, orientation, and exchange — not spatial coordinates.

---

## 2.5 Summary of the Vectorial Structure

| Variable | Type | Grade argument | Dimension |
|----------|------|----------------|-----------|
| S | Scalar (ℝ) | Magnitude without direction | — |
| **A** | Vector (ℝ³) | Force requires vector type | §2.3.2 |
| **I** | Vector (ℝ³) | Field requires vector operands | §2.3.2 |
| **R** | Vector (ℝ³) | Field requires vector operands | §2.3.2 |
| Force = S**A** | Vector (ℝ³) | Scalar scaling preserves grade | — |
| Field = **I**×**R** | Vector (ℝ³) | Hodge dual of **I**∧**R**; grade 1 by Postulate 2.1 | Requires ℝ³ |

---

## 2.6 The Geometric Algebra Structure

The four variables span the full grade structure of **G(3)** — the geometric algebra of 3-dimensional space:

| Grade | Dimension | Relation to UoC |
|-------|-----------|-----------------|
| 0 (scalar) | 1 | S |
| 1 (vectors) | 3 | **A**, **I**, **R** (assumed linearly independent basis) |
| 2 (bivectors) | 3 | **A**∧**I**, **A**∧**R**, **I**∧**R** (= Field via Hodge dual) |
| 3 (pseudoscalar) | 1 | **A**∧**I**∧**R** (oriented volume) |
| **Total** | **8 = 2³** | |

*Clarification*: **A**, **I**, **R** are grade-1 *elements* of G(3), not generators. The generators are the orthonormal basis vectors {**e**₁, **e**₂, **e**₃}. The G(3) structure applies under the assumption that **A**, **I**, **R** are linearly independent and the configuration space carries the standard Euclidean metric — both minimal hypotheses. The Hodge dual (Field = **I**×**R**) presupposes this metric.

The sufficiency argument — that no fifth ontological variable is needed — follows from the fact that {S, **A**, **I**, **R**} already span all 8 dimensions of G(3), leaving no room for a fifth variable to add expressive power (Ch3).

---

## 2.7 Scope and Open Questions

- **Why a vector Field and not a bivector?** This is the central open question of the chapter. If Field were allowed to be a bivector (**I**∧**R**, grade 2), the dimension constraint of §2.3.2 would collapse — bivectors are well-defined in any dimension ≥ 2. Postulate 2.1 (grade-1 Field) is the load-bearing hypothesis; its revision would require rethinking the dimensionality derivation from the ground up.
- **Why ℝ³ and not ℝ⁷?** ℝ³ is the minimal dimension under Postulate 2.1. The 7D case is not formally excluded but introduces non-uniqueness (octonionic structure); excluded by parsimony.
- **Degenerate configurations**: the linear independence of **A**, **I**, **R** is assumed, not derived. Configurations where two variables are parallel (e.g., **I** ∥ **R**) are not excluded from $\mathcal{V}$ but may correspond to pathological UoC states (Field = 0).
- **Sufficiency of four variables**: formal argument in Ch3.

---

*End of Chapter 2 (condensed)*
