# Chapter 7: Compositional Operations
*Condensed version — source: Ch7 of the full GSF*

---

## 7.1 Motivation

Ch5 established $\Gamma$ as the structural object of a single UoC. Most systems of interest — organisms, persons, societies — are composites. This chapter introduces nine formal operations on configuration matrices and attribute spaces. Each operation specifies: (1) what happens to attribute spaces $\{S, A, I, R\}$; (2) what happens to $\Gamma$; (3) whether sub-UoCs remain **distinguishable** (Definition 7.1); (4) structural directionality (reversible / irreversible / terminal).

**Epistemic status.** Identifications with biological or psychological phenomena (fusion → organism, reproduction → cell division, etc.) are correspondences, not derivations. Thermodynamic constraints (§7.9) are structural conjectures pending explicit $P(\Gamma)$; the algebraic structure of each operation follows from Ch5.

*Note on future reduction.* The nine operations may reduce to a smaller core set under deeper analysis. Empirically, nature shows primarily fusion/integration (cell → organism); social systems show primarily union/sum. The remaining operations may be special cases or limit regimes of two or three primitives. This reduction is deferred to Part III.

---

## 7.2 The Distinguishability Criterion

**Definition 7.1 (Distinguishability).** $A$, $B$ are **structurally distinguishable within** composite $C$ if there exist projections $\pi_A, \pi_B: V_C \to V_C$ satisfying:
1. $\pi_A + \pi_B = \mathrm{Id}_{V_C}$ (completeness)
2. $\pi_A^2 = \pi_A$, $\pi_B^2 = \pi_B$ (idempotency)
3. $\|\pi_A \Gamma_C \pi_A^T - \Gamma_A\|_F \leq \epsilon_{AB} = \|C_{AB}\|_F$ and same for $B$ (structural recovery — exact when $C_{AB} = 0$)

Distinguishability admits degrees: large $C_{AB}$ means the recovered $\Gamma_A, \Gamma_B$ deviate significantly from isolated values.

---

## 7.2.1 Structural Level Compatibility Conditions

**Definition 7.2 (ρ-Proximity).** $|\rho_A - \rho_B| \leq \delta_\rho$ for structural threshold $\delta_\rho > 0$.

**Postulate 7.1 (Level Conditions).** *(Structural postulates; derivation from $P(\Gamma)$ is open — OQ7.1.)*

| Operation | Required ρ-condition | Level of output |
|-----------|---------------------|-----------------|
| Union | ρ-proximity | $\rho_U = \max(\rho_A, \rho_B)$ |
| Coupling | ρ-proximity preferred; $\|C_{AB}\| \to 0$ at large ρ-gap | each retains own ρ |
| Fusion | ρ-proximity ($\delta_F$) | $\rho_F \geq \max(\rho_A, \rho_B)$ |
| Nesting | strict gap: $\rho_A - \rho_B \geq \delta_\text{nest} > 0$ | $B$ retains $\rho_B$ under host $\rho_A$ |
| Absorption | $\rho_A \geq \rho_B$ | $\rho_{A'} \geq \rho_A$ |
| Reproduction | none | $\rho_B^{(0)} \approx \rho_A$ |
| Resonance | ρ-proximity | each retains own ρ |
| Fission, Decoupling, Dissolution | none | — |

**Rationale**: $C_{AB}$ is expected to decay with ρ-separation (hypothesis: $C_{AB} \sim e^{-|\rho_A-\rho_B|/\delta_\rho}$), from the G(3)-invariant structure of $P(\Gamma)$ (Ch11 §11.4). Hierarchical operations (nesting, absorption) require a host-subordinate level gap. A **mediation postulate** states that operations across $|\rho_A - \rho_B| > \delta_\rho$ require an intermediate UoC mediator.

---

## 7.3 Operations Preserving Distinguishability

### 7.3.1 Union

**Definition 7.3 (Union).** Composite $U = A \cup B$ with:
- $V_U = V_A \oplus V_B$ (finite-dimensional, compatible G(3) structure)
- $\Gamma_U = \begin{pmatrix} \Gamma_A & C_{AB} \\ C_{BA} & \Gamma_B \end{pmatrix}$, $C_{AB} = C_{BA}^T$ — primary object; $\Gamma_A, \Gamma_B$ recovered via canonical projections
- $A, B$ structurally distinguishable within $U$

Symmetric; reversible when $C_{AB}$ small — follows from the definition: $C_{AB} \to 0$ recovers two independent UoCs.

### 7.3.2 Nesting

**Definition 7.4 (Nesting).** $B \triangleleft A$ if:
- $V_B \subsetneq V_A$ is a **stable subspace**: $\Gamma_A V_B \subseteq V_B$
- $\Gamma_B = \Gamma_A\big|_{V_B}$
- $\rho_A - \rho_B \geq \delta_\text{nest} > 0$

Asymmetric; host modulates boundary conditions of nested UoC. *The domain contraction of Ch4 §4.2.2 provides the natural nesting structure: $D_X(\rho_B) \subsetneq D_X(\rho_A)$ for $\rho_B > \rho_A$ — see Remark 7.1 in §7.11.*

### 7.3.3 Coupling

**Definition 7.5 (Coupling).** $A \rightleftharpoons B$ if $\Gamma_E^{(A \to B)} \neq 0$ and $\Gamma_E^{(B \to A)} \neq 0$ without forming a composite. Each retains its own $\Gamma$, $\rho$, $\xi^*$.

Weakest structural interaction. At zero coupling: independent evolution. At maximum coupling: approaches union regime.

---

## 7.4 Merging Operations

### 7.4.1 Fusion

**Definition 7.6 (Fusion).** New UoC $F$ from $A$, $B$ such that:
- $\{S,A,I,R\}_F$ are emergent attributes (not direct sums of originals)
- $\Gamma_F$ has no block-decomposition recovering $\Gamma_A, \Gamma_B$ ($A, B$ indistinguishable within $F$)
- $A, B$ cease to exist as separate UoCs

Irreversible in general.

### 7.4.2 Absorption

**Definition 7.7 (Absorption).** $A \leftarrow B$: $A$ persists modified ($\Gamma_A \to \Gamma_{A'}$); $B$ loses structural identity. Asymmetric limit of fusion.

---

## 7.5 Separating Operations

### 7.5.1 Fission

**Definition 7.8 (Fission).** $C$ separates into $\{A, B, \ldots\}$: $V_A \oplus V_B \oplus \cdots = V_C$ (exhaustive); $\Gamma_A = \pi_A \Gamma_C \pi_A^T$ plus diagonal normalization; $C$ ceases to exist.

**Structural conservation** *(conjecture)*: $\sum_i P(\Gamma_i) \leq P(\Gamma_C)$ — subadditivity of $P$ under block restriction. Not derived in Part I.

### 7.5.2 Decoupling

**Definition 7.9 (Decoupling).** $\Gamma_E^{(A \to B)} \to 0$ and $\Gamma_E^{(B \to A)} \to 0$; both persist. Reverse of coupling.

---

## 7.6 Generative Operations

### 7.6.1 Reproduction

**Definition 7.10 (Reproduction).** $A$ generates new UoC $B$ with $\Gamma_B^{(0)} \approx \Gamma_A(\xi^*_A)$. $A$ persists. $B$ evolves independently.

**Structural inheritance**: $\|\Gamma_B^{(0)} - \Gamma_A\|_F$ measures fidelity; partial inheritance = structural variation (GSF analog of mutation).

---

## 7.7 Terminal Operation

### 7.7.1 Dissolution

**Definition 7.11 (Dissolution).** $A$ dissolves when $F_\text{ext} \to 0$: the gradient flow $\dot\xi = -M\nabla P$ (Ch10 Theorem 10.1) drives $\xi$ toward the critical set of $P$. Under coercivity (Ch9 §9.5 H3), the UoC converges to the global minimum of $P$. Terminal and non-generative: no new attractors produced.

*(The identification of the global minimum with "soul attractor" at low ρ is a candidate correspondence — Ch9 §9.7 — not a formal result.)*

---

## 7.8 Synchronic States

### 7.8.1 Resonance

**Definition 7.12 (Structural Resonance).** $A, B$ in **structural resonance** if:
1. $\rho$-proximate: $|\rho_A - \rho_B| \leq \delta_\rho$
2. Attractors temporarily align: $\Gamma^*_A(t) \approx \Gamma^*_B(t)$ for $t \in [t_0, t_1]$ — without merging or persistent coupling

Transient and reversible. The conjecture that attractor alignment entails co-minimization of structural entropy production requires establishing the link between attractor proximity and $\sigma_\text{struct}$ — not derived in Part I.

---

## 7.9 Thermodynamic Constraints

**Proposition 7.1 (Structural Directionality — partial derivation).**

1. **Fusion/absorption**: entropy non-decreasing under merging *(conjecture — requires $\sigma_\text{struct}$)*.
2. **Fission**: requires $P(\Gamma_C) > \sum_i P(\Gamma_i)$ *(conjecture)*.
3. **Union**: reversible at small $\|C_{AB}\|$ — *derived from Definition 7.3*.
4. **Reproduction**: costs structural work from $A$ *(conjecture)*.
5. **Dissolution**: admissible under autonomous dynamics — *derived from Ch10 Theorem 10.1* (gradient flow to critical set under coercivity).

**Remark**: Non-spontaneous operations (reproduction, nesting maintenance, sustained coupling) require $F_\text{ext} \neq 0$ *(structural conjecture)*.

---

## 7.10 Summary Table

| Operation | Source UoCs persist | Distinguishable | Reversible | Thermodynamic character |
|-----------|---|---|---|---|
| Union | Yes (both) | Yes | Yes | Reversible if $\|C_{AB}\|$ small — derived |
| Nesting | Yes (both) | Yes | Yes | Requires host drive $F_\text{ext}$ |
| Coupling | Yes (both) | Yes | Yes | Requires mutual $\Gamma_E \neq 0$ |
| Fusion | No (both merge) | No | No (general) | Entropy non-decreasing (conjectured) |
| Absorption | Yes (host only) | No | No | Entropy non-decreasing (conjectured) |
| Fission | No (parent splits) | Yes (new sub-UoCs) | No (general) | Requires $\Delta P > 0$ (conjectured) |
| Decoupling | Yes (both) | Yes | Yes | Autonomous if $F_\text{ext} \to 0$ |
| Reproduction | Yes (parent) | Yes (new UoC) | — | Costs structural work (conjectured) |
| Dissolution | No (ceases) | — | No | Terminal; derived from Ch10 Thm 10.1 |
| Resonance | Yes (both) | Yes | Yes | Attractor alignment; σ co-minimization conjectured |

---

## 7.11 Open Questions

- **OQ7.1 — Level thresholds**: $\delta_\rho$, $\delta_F$, $\delta_\text{nest}$ not derived; depend on $P(\Gamma)$ and $\Gamma_s$ spectrum. Deriving from Ch10 Lagrangian is an open problem.
- **Fusion criterion**: formal condition for union-to-fusion transition as $\|C_{AB}\|$ grows — structural phase transition.
- **Higher-order compositions**: $n$-ary operations and conservation laws on composite $\Gamma$.
- **Resonance duration**: $[t_0, t_1]$ window requires explicit stochastic dynamics and noise $D(\rho)$.
- **OQ7.2 — The psychological composite UoC**: soul (ρ→0⁺), ego, and body at different ρ levels.

  **Remark 7.1 (⊕ as iterated nesting — derived).** The co-presence operator ⊕ of Ch4 Notation 5.1 can be defined as iterated nesting: $\text{UoC}(\rho_\text{body}) \triangleleft \text{UoC}(\rho_\text{ego}) \triangleleft \text{UoC}(\rho_\text{soul})$. The stable subspace structure is provided by Ch4 Postulate 4.2 (domain contraction): $D_X(\rho_\text{body}) \subsetneq D_X(\rho_\text{ego}) \subsetneq D_X(\rho_\text{soul}) = \mathcal{V}_X$ for all $X$. The ρ-gap condition of Postulate 7.1 is satisfied by construction. What remains open: the phenomenology of perceived unity (likely a property of $\Gamma_E$ modulation).

---

*End of Chapter 7 (condensed)*
