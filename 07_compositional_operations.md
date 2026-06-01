# Chapter 7: Compositional Operations

## 7.1 Motivation

Ch5 established the configuration matrix $\Gamma$ as the central structural object of a single UoC. Physics and psychology, however, deal overwhelmingly with **composite systems**: organisms composed of cells, persons composed of ego and body, societies composed of persons. For GSF to address composite systems, we introduce formal compositional operations on the algebraic objects defined in Ch5 — not as biological or sociological claims, but as operations on configuration matrices and attribute spaces.

This chapter defines nine compositional operations. Each is specified by:
1. What happens to the attribute sets $\{S, A, I, R\}$ of the participating UoCs
2. What happens to the configuration matrix $\Gamma$
3. Whether the source UoCs remain **distinguishable** within the composite (Definition 7.1)
4. Structural directionality of the operation (reversible / irreversible / terminal)

**Epistemic status.** The operations are defined by structural role within the GSF formalism. Their identification with biological or psychological phenomena (fusion → organism, reproduction → cell division, etc.) is a correspondence, not a derivation. The structural directionality constraints of §7.9 are stated as conjectures; the algebraic structure of each operation follows from Ch5.

---

## 7.2 The Distinguishability Criterion

**Definition 7.1 (Distinguishability).** Let $C$ be a composite UoC with attribute space $V_C$ and configuration matrix $\Gamma_C$. Two UoCs $A$ and $B$ are **structurally distinguishable within $C$** if there exist linear projection operators $\pi_A, \pi_B: V_C \to V_C$ such that:

1. $\pi_A + \pi_B = \mathrm{Id}_{V_C}$ (completeness)
2. $\pi_A^2 = \pi_A$, $\pi_B^2 = \pi_B$ (idempotency)
3. $\|\pi_A \Gamma_C \pi_A^T - \Gamma_A\|_F \leq \epsilon_{AB}$ and $\|\pi_B \Gamma_C \pi_B^T - \Gamma_B\|_F \leq \epsilon_{AB}$, where $\epsilon_{AB} = \|C_{AB}\|_F$ is the Frobenius norm of the inter-UoC coupling block (structural recovery, exact when $C_{AB} = 0$; see §7.3.1)

If no such pair of projections exists, $A$ and $B$ are **structurally indistinguishable** within $C$.

**Remark.** Distinguishability is not a binary property in general — it admits degrees. A composite with large off-diagonal coupling $C_{AB}$ has partially distinguishable sub-UoCs: the projections exist but the recovered $\Gamma_A$, $\Gamma_B$ deviate significantly from the isolated values. Full distinguishability corresponds to $C_{AB} \to 0$; full indistinguishability to a $\Gamma_C$ with no block structure.

---

## 7.2.1 Structural Level Compatibility Conditions

The operations defined in §§7.3–7.8 are not unrestricted in the structural level $\rho$ of the participating UoCs. Different operations are admissible only within specific $\rho$-regimes. This section states those conditions as structural postulates. Their derivation from the explicit form of $P(\Gamma)$ and the compositional dynamics is an open question (§7.11).

*Note on ρ domain.* The theoretical domain of $\rho$ is $(0, \infty)$ (Ch4 §4.2.1). The thresholds $\delta_\rho$, $\delta_F$, $\delta_\text{nest}$ introduced below are parameters defined in the same theoretical domain; their values are independent of any operational normalization.

**Definition 7.2 (ρ-Proximity).** UoCs $A$ and $B$ are **ρ-proximate** if
$$|\rho_A - \rho_B| \leq \delta_\rho$$
for a structural threshold $\delta_\rho > 0$. The value of $\delta_\rho$ is a parameter of the compositional regime; it is expected to depend on the class of UoCs and the operation type (see Open Question OQ7.1 in §7.11).

**Postulate 7.1 (Level Conditions for Compositional Operations).**

| Operation | Required $\rho$-condition | Level of composite/output |
|-----------|--------------------------|---------------------------|
| Union | $\rho$-proximity: $|\rho_A - \rho_B| \leq \delta_\rho$ | $\rho_U = \max(\rho_A, \rho_B)$ |
| Coupling | $\rho$-proximity (preferred); admissible at all $\rho$ with $\|C_{AB}\| \to 0$ as $|\rho_A - \rho_B| \to \infty$ | — (each retains its own $\rho$) |
| Fusion | $\rho$-proximity: $|\rho_A - \rho_B| \leq \delta_F$ | $\rho_F \geq \max(\rho_A, \rho_B)$ |
| Nesting | Strict level gap: $\rho_A - \rho_B \geq \delta_\text{nest} > 0$ (host is at strictly higher level) | — ($B$ retains $\rho_B$ under host $\rho_A$) |
| Absorption | $\rho_A \geq \rho_B$ (host at same or higher level) | $\rho_{A'} \geq \rho_A$ |
| Reproduction | None required ($A$ generates $B$ at the same level) | $\rho_B^{(0)} \approx \rho_A$ |
| Resonance | $\rho$-proximity is necessary: $|\rho_A - \rho_B| \leq \delta_\rho$ | — (each retains its own $\rho$) |
| Fission | None required (sub-UoCs inherit from parent) | $\rho_i \leq \rho_C$ |
| Decoupling | None required | — |
| Dissolution | None required | — |

**Rationale** *(anticipated — not yet derived)*. The ρ-proximity conditions are structural postulates; their derivation is open (OQ7.1). The anticipated mechanism: the coupling block $C_{AB}$ is expected to decay with ρ-separation, because the structural modes of UoCs at widely different levels do not overlap — a result expected from the G(3)-invariant structure of $P(\Gamma)$ (Ch11 §11.4). A minimal sketch: if $C_{AB}(\rho_A, \rho_B) \sim e^{-|\rho_A - \rho_B|/\delta_\rho}$ (or some monotone-decreasing function of ρ-separation), then the threshold $\delta_\rho$ marks the scale below which interaction is structurally non-negligible. This scaling law is a hypothesis to be derived from the explicit form of $P(\Gamma)$. Operations that establish a hierarchical relationship (nesting, absorption) require a level gap: without $\rho_A > \rho_B$, there is no host-subordinate distinction. Resonance requires proximity because attractor alignment ($\Gamma_A(\xi^*_A) \approx \Gamma_B(\xi^*_B)$) requires compatible structural scales.

**Mediation postulate.** For operations between UoCs at levels separated by more than $\delta_\rho$, a UoC at an intermediate level acting as mediator is required to bridge the $\rho$-gap. Direct operations across large $\rho$-separations are not structurally admissible without mediation. The formal characterization of the mediating UoC is left for future development.

---

## 7.3 Operations Preserving Distinguishability

### 7.3.1 Union

**Definition 7.3 (Union).** A **union** of UoCs $A$ and $B$ is a composite UoC $U = A \cup B$ such that:
- $V_U = V_A \oplus V_B$ (direct sum of attribute spaces, assuming $V_A$ and $V_B$ are finite-dimensional vector spaces over the same field with compatible G(3) structure)
- $\Gamma_U$ is a block-diagonalizable matrix of the form $\Gamma_U = \begin{pmatrix} \Gamma_A & C_{AB} \\ C_{BA} & \Gamma_B \end{pmatrix}$ with $C_{AB} = C_{BA}^T$ (symmetric coupling block), where $\Gamma_A$, $\Gamma_B$ are the blocks recovered by the canonical projections onto $V_A$ and $V_B$ respectively

*Note on ordering*: the matrix $\Gamma_U$ is the primary object; $\Gamma_A = \pi_A \Gamma_U \pi_A^T$ and $\Gamma_B = \pi_B \Gamma_U \pi_B^T$ are defined as the recovered blocks (avoiding circularity: we do not presuppose $\Gamma_A$, $\Gamma_B$ independently).

*Note on projections*: for a direct sum $V_U = V_A \oplus V_B$, the canonical projections $\pi_A(v_A, v_B) = v_A$ and $\pi_B(v_A, v_B) = v_B$ are well-defined and satisfy Definition 7.1 conditions 1–2 identically.

- $A$ and $B$ are structurally distinguishable within $U$ (Definition 7.1)

The coupling block $C_{AB}$ encodes the inter-UoC structural coupling — the degree to which the attributes of $A$ and $B$ are correlated within the composite. At $C_{AB} = 0$, the union is purely formal (no structural interaction); at large $|C_{AB}|$, the sub-UoCs are strongly coupled but remain distinguishable.

**Properties:**
- Symmetric: $A \cup B \cong B \cup A$ (up to permutation of the block structure)
- Reversible: the composite can separate into $A$ and $B$ if $C_{AB}$ is reduced to zero
- Level condition (Postulate 7.1): requires $\rho$-proximity ($|\rho_A - \rho_B| \leq \delta_\rho$); the composite level is $\rho_U = \max(\rho_A, \rho_B)$

**Examples:** Two persons in conversation; cells in a tissue; temporary coalitions.

### 7.3.2 Nesting

**Definition 7.4 (Nesting).** UoC $B$ is **nested within** UoC $A$ (written $B \triangleleft A$) if:
- $V_B \subsetneq V_A$ as a proper sub-space, with $V_B$ a **stable subspace** under $\Gamma_A$ — i.e., $\Gamma_A V_B \subseteq V_B$; this ensures the restriction $\Gamma_A\big|_{V_B}$ is well-defined and preserves the G(3) algebraic structure required for $B$ to remain a valid UoC
- $\Gamma_B = \Gamma_A\big|_{V_B}$ — the configuration of $B$ is the restriction of $A$'s configuration to $B$'s stable sub-attribute-space
- $\rho_B$ is structurally subordinate to $\rho_A$: changes in $\rho_A$ modulate the boundary conditions of $\rho_B$
- Level condition (Postulate 7.1): $\rho_A - \rho_B \geq \delta_\text{nest} > 0$ — the host is at a strictly higher structural level than the nested UoC

Nesting is **asymmetric**: $B \triangleleft A$ does not imply $A \triangleleft B$. The host UoC $A$ provides the structural environment within which the nested $B$ evolves — its epistemological modulation $\Gamma_E^{(A \to B)}$ acts as a boundary condition on $B$'s dynamics.

**Distinction from union:** In union, $V_U = V_A \oplus V_B$ (additive); in nesting, $V_B \subsetneq V_A$ (contained). Union is between peers; nesting is between a host and a subordinate.

**Examples:** Organ within body ($\rho_\text{organ} \triangleleft \rho_\text{body}$); sub-unit within organization. *Candidate example*: ego as dissipative structure nested within the soul-body composite — but whether the person is a nesting, a union, or a fusion of its soul/ego/body level UoCs is an open structural question (OQ7.2).

### 7.3.3 Coupling

**Definition 7.5 (Coupling).** UoCs $A$ and $B$ are **structurally coupled** (written $A \rightleftharpoons B$) if they exert mutual epistemological modulation:
$$\Gamma_E^{(A \to B)} \neq 0, \qquad \Gamma_E^{(B \to A)} \neq 0$$
without forming a composite UoC. Each remains a separate UoC with its own $\Gamma$, $\rho$, and attractor $\xi^*$; the coupling modifies each one's effective $P(\Gamma)$ via the modulation terms of Ch9 §9.8.

Coupling is a **persistent state** (not an event): it requires ongoing interaction to be maintained. It is the weakest form of structural interaction — UoCs remain fully distinguishable and separately identified.

**Coupling strength:** The magnitude $\|C_{AB}\|$ of the effective cross-modulation characterizes the coupling strength. At zero coupling, $A$ and $B$ evolve independently. At maximum coupling, $A$ and $B$ approach the union regime.

**Examples:** Sustained interpersonal relationship; two coupled oscillators. *Candidate example*: predator-prey ecological coupling — whether the mutual modulation is symmetric enough to qualify as structural coupling in the GSF sense depends on the specific ρ-levels involved.

---

## 7.4 Merging Operations

### 7.4.1 Fusion

**Definition 7.6 (Fusion).** A **fusion** of UoCs $A$ and $B$ is a new UoC $F$ such that:
- $\{S, A, I, R\}_F$ are new variables — not the direct sums of $A$'s and $B$'s attributes but emergent attributes of the composite
- $\Gamma_F$ has no block-decomposition recovering $\Gamma_A$ and $\Gamma_B$ (i.e., $A$ and $B$ are structurally indistinguishable within $F$)
- The source UoCs $A$ and $B$ cease to exist as separate entities upon fusion

Fusion is **irreversible in general**: recovering $A$ and $B$ from $F$ requires more information than $F$ alone provides (the fusion destroyed the sub-UoC structure).

**Symmetric vs asymmetric fusion.** If the roles of $A$ and $B$ in determining $F$'s structure are equivalent, the fusion is symmetric; if one dominates, it shades into absorption (§7.4.2).

**Examples:** Fertilization (two gametes → one zygote); formation of a novel organizational unit whose identity is not reducible to its founding members. *Candidate example*: formation of a person as a UoC not reducible to its organs — but see OQ7.2 for the open question of which operation best describes the psychological composite.

### 7.4.2 Absorption

**Definition 7.7 (Absorption).** UoC $A$ **absorbs** UoC $B$ (written $A \leftarrow B$) if:
- $A$ persists as a UoC but with a modified configuration: $\Gamma_A \to \Gamma_{A'}$ where $\Gamma_{A'} \neq \Gamma_A$
- $B$ loses structural identity: its attributes are incorporated into $A'$ but $B$ no longer exists as a separate UoC
- The operation is **asymmetric**: $A \leftarrow B \not\cong B \leftarrow A$

Absorption is the asymmetric limit of fusion: one UoC is the host (survives modified) and the other is the absorbed (disappears). It differs from nesting in that the absorbed UoC does not retain its own $\Gamma_B$ — it is fully dissolved into the host's structure.

**Examples:** Phagocytosis; assimilation of a cultural practice into a worldview; mitochondrial endosymbiosis (historically).

---

## 7.5 Separating Operations

### 7.5.1 Fission

**Definition 7.8 (Fission).** A **fission** of UoC $C$ is its separation into two or more UoCs $\{A, B, \ldots\}$ such that:
- $V_A \oplus V_B \oplus \cdots = V_C$ (the sub-UoCs' attribute spaces exhaust $C$'s — fission is exhaustive; any modes not assigned to a sub-UoC are released as unstructured contributions to the environment, consistent with partial dissolution)
- $\Gamma_A, \Gamma_B, \ldots$ are derived from $\Gamma_C$ by **restriction** ($\Gamma_A = \pi_A \Gamma_C \pi_A^T$, the principal submatrix on $V_A$) and **diagonal normalization** to ensure $c_X > 0$ for each retained attribute (Ch5 §5.3); the cross-block coupling terms $C_{AB}$ are discarded upon separation
- $C$ ceases to exist as a UoC after fission

Fission is the partial inverse of fusion, but not in general its exact inverse: $\text{fission}(\text{fusion}(A, B)) \neq (A, B)$ unless the fusion was trivial (i.e., a union with $C_{AB} \to 0$).

**Structural conservation** *(structural conjecture — not derived here)*. Under the subadditivity of $P$, the sub-UoCs' configurations are expected to satisfy:
$$\sum_i P(\Gamma_i) \leq P(\Gamma_C) \qquad \text{(free-energy non-increase under fission)}$$
The inequality relies on subadditivity of $P(\Gamma)$ under block restriction — a property not established in Part I. It is stated here as a structural constraint, not a derived theorem.

**Examples:** Cell division; organizational split; conceptual differentiation of a unified framework into specialized sub-theories.

### 7.5.2 Decoupling

**Definition 7.9 (Decoupling).** A **decoupling** of coupled UoCs $A \rightleftharpoons B$ is the reduction of mutual modulation to zero: $\Gamma_E^{(A \to B)} \to 0$ and $\Gamma_E^{(B \to A)} \to 0$. Both $A$ and $B$ persist; the coupling is dissolved.

Decoupling is the reverse of coupling (§7.3.3). It does not create new UoCs or modify their internal configurations — it only removes the interaction.

---

## 7.6 Generative Operations

### 7.6.1 Reproduction

**Definition 7.10 (Reproduction).** UoC $A$ **reproduces** to generate UoC $B$ if:
- $B$ is a new UoC (not previously existing) with initial configuration $\Gamma_B^{(0)} \approx \Gamma_A$ or $\Gamma_B^{(0)} \approx \Gamma_A(\xi^*_A)$ (the coupling matrix evaluated at $A$'s state-space attractor $\xi^*_A$; note that the attractor in $\Gamma$-space is not yet formalized — see Ch5 §5.8 open question)
- $A$ persists after reproduction (with possibly modified $\Gamma_{A'}$)
- After generation, $B$ evolves **independently** under its own dynamics

Reproduction is distinct from fission in that the parent $A$ persists; it is distinct from copying in that $B$'s subsequent evolution is autonomous — $B$ is not constrained to remain a copy of $A$.

**Inheritance.** The degree to which $\Gamma_B^{(0)}$ approximates $\Gamma_A$ is the **structural inheritance** of the reproduction. Perfect inheritance ($\Gamma_B^{(0)} = \Gamma_A$) is a special case; partial inheritance allows for structural variation (the GSF analog of mutation).

**Examples:** Cell division (parent cell persists as modified daughter); generation of a new habit pattern; training a student.

---

## 7.7 Terminal Operation

### 7.7.1 Dissolution

**Definition 7.11 (Dissolution).** A UoC $A$ **dissolves** if it loses the capacity to maintain positive structural entropy production at its attractor:

$$F_\text{ext}(\xi^*_A, \rho_A) \to 0 \qquad \Longrightarrow \qquad \sigma_\text{struct}\big|_{\xi^*_A} \to 0$$

where $\sigma_\text{struct}$ denotes the structural entropy production rate *(defined formally in subsequent work; stated here as a structural constraint)*. Without the external drive $F_\text{ext}$, the autonomous gradient flow $\dot{\xi} = -M\nabla P$ brings $\xi$ toward the global minimum of $P$ — a low-ρ structural configuration identified as the "soul attractor" $\xi^*(\rho \to 0^+)$ *(candidate phenomenological label; the global minimum is a structural postulate, not derived in Part I)*. The UoC's local attractor $\xi^*_A$ is no longer maintained, and its attributes disperse into the environment.

Dissolution is **terminal and non-generative**: unlike fission, it does not produce new identifiable UoCs — the attributes of $A$ are released as unstructured contributions to the next level up.

**Distinction from fission:** Fission produces identifiable sub-UoCs with their own attractors. Dissolution produces no new attractors — the structural free energy $P(\Gamma)$ approaches its global minimum, not a new local minimum.

**Examples:** Death of an organism; collapse of an organization; dissolution of a belief system.

---

## 7.8 Synchronic States

### 7.8.1 Resonance

**Definition 7.12 (Structural Resonance).** UoCs $A$ and $B$ are in **structural resonance** if:
1. They are $\rho$-proximate: $|\rho_A - \rho_B| \leq \delta_\rho$ (Postulate 7.1; necessary for attractor alignment across compatible scales)
2. Their attractors temporarily align:
$$\Gamma^*_A(t) \approx \Gamma^*_B(t) \qquad \text{for } t \in [t_0, t_1]$$
without merging (both remain separate UoCs with $\Gamma_A \neq \Gamma_B$ in general) and without forming a persistent coupling ($\Gamma_E \to 0$ outside the resonance window).

Resonance is **transient and reversible**: it is a temporary coordination of attractors driven by mutual coupling that falls below the threshold of Definition 7.5. When the resonance window closes, $A$ and $B$ return to their independent attractor dynamics.

**Thermodynamic signature** *(anticipated — not derived here)*. Attractor alignment ($\Gamma^*_A \approx \Gamma^*_B$) is the defining criterion; it is not equivalent by definition to co-minimization of structural free energies. The conjecture that resonance implies mutual entropy production is minimized — i.e., that attractor alignment entails $\sigma_\text{struct}^{(A)} + \sigma_\text{struct}^{(B)}$ is locally minimal — requires establishing the relationship between attractor proximity and entropy production (not derived in Part I). That derivation would make this a **candidate GSF formalization** of coherence, synchrony, or empathy; at present it is a structural postulate, not a consequence.

**Examples:** Phase-locking of biological oscillators; collective flow states; coordinated action. *Candidate example*: momentary empathy between persons — whether attractor alignment captures the phenomenology of empathy is a correspondence to be established, not a derivation.

---

## 7.9 Thermodynamic Constraints on Compositional Operations

Structural directionality constrains which operations are admissible. The following proposition is **stated as a structural conjecture** — it is not derived within Part I. The entries below are structural constraints pending formal derivation from the explicit form of $P(\Gamma)$.

**Proposition 7.1 (Structural Directionality Constraints — conjectured).** Under autonomous gradient-flow dynamics:

1. **Fusion and absorption**: conjectured irreversible — the structural entropy of the composite is expected to satisfy $\sigma_\text{struct}(F) \geq \sigma_\text{struct}(A) + \sigma_\text{struct}(B)$ (structural entropy non-decreasing under merging). *(Structural conjecture — not derived in Part I.)*

2. **Fission**: conjectured to require $P(\Gamma_C)$ to exceed the sum of the sub-UoC free energies — fission driven by a structural free-energy gradient (not spontaneous for stable UoCs). *(Not derived in Part I.)*

3. **Union**: reversible if $C_{AB}$ is small — follows directly from Definition 7.3: when $C_{AB} \to 0$ the composite separates into independent $A$ and $B$. As $\|C_{AB}\|$ grows, the union approaches the irreversible fusion regime.

4. **Reproduction**: conjectured to require structural work from $A$ (entropy export). The cost is bounded below by $\Delta P = P(\Gamma_B^{(0)}) - P(\Gamma_A(\xi^*_A))$ *(structural constraint — not derived in Part I).*

5. **Dissolution**: admissible under autonomous dynamics — follows from Ch10 Theorem 10.1: the gradient flow $\dot\xi = -M\nabla P$ drives $\xi$ toward $\nabla P = 0$, and under coercivity of $P$ (Ch9 §9.5 hypothesis H3), every closed UoC converges to the critical set. Dissolution is the terminal state of this convergence when the external drive $F_\text{ext} \to 0$. The specific identification of the global minimum with the "soul attractor" is a candidate correspondence (Ch9 §9.7), not a formal result.

**Remark** *(structural conjecture)*. Operations requiring external structural drive $F_\text{ext} \neq 0$ — reproduction, nesting maintenance, sustained coupling — are conjectured to be non-spontaneous, requiring structural energy input from the level above.

---

## 7.10 Summary Table

| Operation | Source UoCs persist | Target UoCs distinguishable | Reversible | Thermodynamic character |
|-----------|---|---|---|---|
| Union | Yes (both) | Yes | Yes | Reversible if $\|C_{AB}\|$ small |
| Nesting | Yes (both) | Yes | Yes | Requires host drive $F_\text{ext}$ |
| Coupling | Yes (both) | Yes | Yes | Requires mutual $\Gamma_E \neq 0$ |
| Fusion | No (both merge) | No | No (general) | Entropy non-decreasing |
| Absorption | Yes (host only) | No | No | Entropy non-decreasing |
| Fission | No (parent splits) | Yes (new sub-UoCs) | No (general) | Requires $\Delta P > 0$ |
| Decoupling | Yes (both) | Yes | Yes | Autonomous if $F_\text{ext} \to 0$ |
| Reproduction | Yes (parent) | Yes (new UoC) | — | Costs structural work from parent |
| Dissolution | No (ceases) | — | No | Terminal; spontaneous at $F_\text{ext} = 0$ |
| Resonance | Yes (both) | Yes | Yes | Attractor alignment; $\sigma$ co-minimization conjectured (not derived) |

---

## 7.11 Open Questions

- **OQ7.1 — Level thresholds**: Postulate 7.1 introduces three structural thresholds ($\delta_\rho$, $\delta_F$, $\delta_\text{nest}$) that determine which operations are admissible at a given $\rho$-separation. These are not derived from Ch5 or Ch1 alone; their values are expected to depend on the form of $P(\Gamma)$ and the spectral structure of $\Gamma_s$ near the operative regime. Deriving them from the explicit Lagrangian (Ch10) is an open problem.

- **Composition of $\rho$**: how does $\rho_U$ (union), $\rho_F$ (fusion), or $\rho_\text{nested}$ relate to $\rho_A$ and $\rho_B$? The explicit formula requires the derivation of $P(\Gamma)$ (open question T3 — not addressed in Part I).

- **Fusion criterion**: the formal condition under which a union transitions to a fusion — as $\|C_{AB}\|$ increases, at what point does distinguishability break down? This is a structural phase transition in the space of composite configurations (not characterized in Part I).

- **Inheritance fidelity**: the structural inheritance $\|\Gamma_B^{(0)} - \Gamma_A\|_F$ in reproduction is a GSF-internal notion of hereditary fidelity. Its relationship to biological mutation rates or cultural transmission fidelity is a correspondence to be established in the biological instantiation chapter.

- **Higher-order compositions**: this chapter treats binary operations ($A \circ B$). Multi-UoC compositions (union of $n$ UoCs, simultaneous fission into $k$ sub-UoCs) require extension to $n$-ary operations and conservation laws on the resulting $\Gamma$ structure.

- **Resonance duration**: the temporal extent of the resonance window $[t_0, t_1]$ is not characterized in Part I — it requires explicit stochastic dynamics and noise characterization $D(\rho)$.

- **OQ7.2 — The psychological composite UoC**: The framework provides soul (ρ → 0), ego, and body as UoCs at different ρ levels. How they combine into the psychological person is unresolved: the options are structurally distinct.

  *If union*: the person is $\text{Soul} \cup \text{Ego} \cup \text{Body}$ — each sub-UoC remains distinguishable within the composite. But union raises the phenomenological question of why the person does not experience itself as three separate components. The answer may lie in the epistemological level: the perceived unity might be a property of $\Gamma_E$ modulation rather than of the ontological structure — but this requires developing the epistemological level, which is outside the scope of this work.

  *If fusion*: the person is an emergent UoC $F$ with no block-decomposition recovering the sub-UoCs. But fusion raises the structural question of what happens at dissolution (death): if the sub-UoCs are indistinguishable within $F$, there are no identifiable components to persist or disperse after $F$ dissolves — and whether this is the correct structural model of death is itself an open empirical question.

  *If nesting*: ego and body are nested within the soul UoC. This is the most structurally natural reading, for the following reason. Ch4 Postulate 4.2 (domain contraction) establishes $D_X(\rho_\text{body}) \subsetneq D_X(\rho_\text{ego}) \subsetneq D_X(\rho_\text{soul}) = \mathcal{V}_X$ for all intrinsic variables $X$. This is precisely the stable subspace condition of Definition 7.4: the operative domain of the body UoC is a proper subset of the ego's, which is a proper subset of the soul's. Nesting is therefore not one option among three — it is the operation that the domain contraction structure of Ch4 naturally induces.

  **Remark 7.1 (⊕ defined as iterated nesting).** The co-presence operator ⊕ introduced in Ch4 Notation 5.1 can now be given a formal definition: $\text{person} = \text{UoC}(\rho_\text{soul}) \oplus \text{UoC}(\rho_\text{ego}) \oplus \text{UoC}(\rho_\text{body})$ is iterated nesting,

  $$\text{UoC}(\rho_\text{body}) \triangleleft \text{UoC}(\rho_\text{ego}) \triangleleft \text{UoC}(\rho_\text{soul})$$

  where $\triangleleft$ is Definition 7.4 with the stable subspace structure provided by $D_X(\rho)$ from Ch4 §4.2.2. The ρ-gap condition of Postulate 7.1 ($\rho_A - \rho_B \geq \delta_\text{nest}$) is satisfied by construction: $\rho_\text{soul} < \rho_\text{ego} < \rho_\text{body}$.

  What remains open is the phenomenological reading: why does the person not experience itself as three nested levels rather than as a unity? The answer likely lies in the epistemological modulation $\Gamma_E$ — the perceived unity is a property of how the soul-level UoC processes its own structure — but this requires formalizing the epistemological level, which is outside the scope of this work.

---

*End of Chapter 7*
