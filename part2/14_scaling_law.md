# Chapter 14: The Scaling Law — T1

## 14.1 The Residual Problem

Chapter 13 derived the structural Lagrangian up to one undetermined function:

$$\mathcal{L}(\Gamma, \dot\Gamma, \rho) = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \frac{2}{\sqrt{c(\rho)}}\det(\Gamma)$$

The function $c(\rho) = \det(P(\Gamma|\rho))$ — the structural coherence at the attractor at organizational level $\rho$ — was left open. The only value derived was the anchor $c(\rho_{\mathrm{GR}}) = 1$ from the massless graviton condition (Ch13, Remark 13.5). All other values of $c$ required additional input.

This chapter supplies that input. The *scaling law* T1 — derived from three independent structural arguments — establishes how $\Gamma$ transforms under changes of organizational level. The transformation law determines $c(\rho)$ for all $\rho$, completing the Lagrangian with no further assumptions.

**The result previewed.** T1 states that $\Gamma$ scales inversely with $\rho$:
$$\Gamma(\rho) = \frac{\Gamma(\rho_{\mathrm{ref}})\cdot\rho_{\mathrm{ref}}}{\rho} \qquad\Longleftrightarrow\qquad \frac{d\Gamma}{d\rho} = -\frac{\Gamma}{\rho}$$

From this single law, all residual functions follow:
$$c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4, \qquad \mu(\rho) = 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^2, \qquad \kappa(\rho) = -1 \;\text{(universal)}$$

The Lagrangian becomes explicit, parameter-free, and valid at every organizational level simultaneously.

---

## 14.2 Setup — The Scaling Problem

### 14.2.1 What T1 Must Determine

The organizational level $\rho > 0$ was introduced in Ch12 as a smooth parameter indexing the fiber bundle $\mathcal{M}(\Gamma;\rho)$ over $\mathbb{R}_{>0}$. Postulate 12.1 established that $\rho$ modulates only the coefficients $\mu(\rho)$ and $\kappa(\rho)$ of the Lagrangian, not the Frobenius geometry of the fibers. What was not specified: the *connection* between fibers — the rule that maps the configuration $\Gamma(\rho)$ at one level to the configuration $\Gamma(\rho')$ at another.

This connection is T1. Without it, configurations at different $\rho$ levels are unrelated — the framework has no rule for comparing, say, a biological coupling matrix ($\rho_{\mathrm{biol}}$) to the gravitational reference ($\rho_{\mathrm{GR}}$). With T1, the entire fiber bundle is trivialized: any $\Gamma(\rho)$ is determined from any other $\Gamma(\rho')$ via a simple rescaling.

### 14.2.2 Ansatz — Power-Law Scaling

The natural candidate for the scaling law is a power-law:
$$\Gamma(\lambda\rho) = \lambda^\alpha\,\Gamma(\rho) \qquad \forall\,\lambda > 0, \;\rho > 0$$

for some exponent $\alpha \in \mathbb{R}$. This is not assumed arbitrarily — it is the only form compatible with the group structure of level changes, as established in §14.3 (Argument 1). The three arguments of §14.3–§14.5 together determine $\alpha = -1$ uniquely.

---

## 14.3 Argument 1 — Group Structure of Level Changes

### 14.3.1 The Group Requirement

Level changes must compose consistently: changing $\rho \to \lambda_1\rho$ and then $\lambda_1\rho \to \lambda_2(\lambda_1\rho)$ must yield the same result as a direct change $\rho \to \lambda_1\lambda_2\rho$. If the scaling function is $f(\lambda)$ — so that $\Gamma(\lambda\rho) = f(\lambda)\Gamma(\rho)$ — this requires:

$$f(\lambda_1\lambda_2) = f(\lambda_1)\,f(\lambda_2) \qquad \forall\,\lambda_1, \lambda_2 > 0$$

**Lemma 14.1 (Cauchy's functional equation on $\mathbb{R}_{>0}$).** *The only continuous solutions of $f(\lambda_1\lambda_2) = f(\lambda_1)f(\lambda_2)$ for $f: \mathbb{R}_{>0} \to \mathbb{R}_{>0}$ are the power functions $f(\lambda) = \lambda^\alpha$ for $\alpha \in \mathbb{R}$.*

*Proof.* Taking logarithms: $\log f(\lambda_1\lambda_2) = \log f(\lambda_1) + \log f(\lambda_2)$. Setting $g = \log f$ and $x = \log\lambda$, this becomes $g(x_1 + x_2) = g(x_1) + g(x_2)$ — Cauchy's additive functional equation on $\mathbb{R}$. The only continuous solutions are $g(x) = \alpha x$, hence $f(\lambda) = e^{\alpha\log\lambda} = \lambda^\alpha$. $\square$

**Corollary 14.1.** *The scaling law must take the form $\Gamma(\rho) = \Gamma_0 \cdot \rho^\alpha$ for some $\alpha \in \mathbb{R}$, where $\Gamma_0 = \Gamma(\rho_0)\cdot\rho_0^{-\alpha}$ is an integration constant.*

Argument 1 establishes the *form* of the scaling law but not the exponent $\alpha$. The following two arguments determine $\alpha = -1$.

---

## 14.4 Argument 2 — Lagrangian Covariance

### 14.4.1 The Covariance Requirement

The structural Lagrangian $\mathcal{L}(\Gamma, \rho)$ describes the dynamics of a UoC at organizational level $\rho$. This description must be *covariant* under changes of $\rho$: the physics cannot depend on the choice of reference level $\rho_{\mathrm{ref}}$. Formally, under $\rho \to \lambda\rho$ (equivalently $\Gamma \to \lambda^\alpha\Gamma$), the Lagrangian may scale, but must scale *uniformly*:

$$\mathcal{L}(\Gamma(\lambda\rho),\,\lambda\rho) = \lambda^\beta\,\mathcal{L}(\Gamma(\rho),\,\rho)$$

for some degree of homogeneity $\beta$ (which can be zero — the Lagrangian could be scale-invariant, or non-zero — it scales consistently).

### 14.4.2 Scaling of Each Term

Under $\Gamma \to \lambda^\alpha\Gamma$ and $\mu(\rho) \to \mu(\lambda\rho) = \lambda^{\mathrm{deg}(\mu)}\mu(\rho)$:

**Kinetic term:** $\|\dot\Gamma\|_F^2 \to \lambda^{2\alpha}\|\dot\Gamma\|_F^2$

**Quadratic potential:** $\|\Gamma\|_F^2 \to \lambda^{2\alpha}\|\Gamma\|_F^2$

**Quartic term:** $\mu(\rho)\det(\Gamma) \to \lambda^{\mathrm{deg}(\mu)}\mu(\rho)\cdot\lambda^{4\alpha}\det(\Gamma) = \lambda^{\mathrm{deg}(\mu)+4\alpha}\,\mu(\rho)\det(\Gamma)$

For the Lagrangian to scale uniformly (all terms with the same power of $\lambda$), the quadratic and quartic terms must have the same total degree:

$$2\alpha = \mathrm{deg}(\mu) + 4\alpha$$

$$\boxed{\mathrm{deg}(\mu) = -2\alpha}$$

The Lagrangian then scales as $\beta = 2\alpha$ uniformly.

### 14.4.3 Fixing $\alpha$ from Physical Constraints

Covariance forces $\mathrm{deg}(\mu) = -2\alpha$, giving the power-law form:
$$\mu(\rho) = \mu_0\cdot\rho^{-2\alpha}$$

Two physical constraints determine $\alpha$:

**Constraint C1 (Anchor).** From Ch13 Remark 13.5: $\mu(\rho_{\mathrm{GR}}) = 2$. This fixes $\mu_0 = 2\rho_{\mathrm{GR}}^{2\alpha}$, giving:
$$\mu(\rho) = 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{-2\alpha}$$

**Constraint C2 (Coordination cost).** Systems at higher organizational levels (larger $\rho$) must maintain their identity against a larger space of perturbations — more attributes are coupled, more boundary conditions must be satisfied simultaneously. This does not mean such systems are rigid in their behavior; a neural network has more behavioral flexibility than a crystal. Rather, it means the *structural cost of maintaining identity* — the "glue" required to preserve the coupling pattern $\Gamma$ against perturbations — must be larger. In Ch13 §13.5, the coupling strength $\mu$ is precisely this structural glue. Therefore $\mu(\rho)$ must be *increasing* in $\rho$:

$$\frac{d\mu}{d\rho} > 0 \implies -2\alpha > 0 \implies \alpha < 0$$

The exponent must be negative. Constraint C2 restricts to $\alpha < 0$ but does not select among the infinitely many negative values. The unique selection comes from a representation-theoretic argument:

**Constraint C3 (Minimal representation-invariant section).** The level-invariant structural object $\mathcal{I}(\rho,\Gamma)$ must satisfy two conditions:

*(a) G-invariance:* $\mathcal{I}(\lambda\rho, \lambda^\alpha\Gamma) = \mathcal{I}(\rho,\Gamma)$ — the object is unchanged by level rescaling.

*(b) H-covariance:* $\mathcal{I}(\rho, R(h)\Gamma) = R(h)\mathcal{I}(\rho,\Gamma)$ — the object transforms in the same representation of the structural group $H$ (frame changes, $\mathrm{GL}(4,\mathbb{R})$ congruence) as $\Gamma$ itself.

Condition (b) forces $\mathcal{I}$ to be *linear* in $\Gamma$: nonlinear functions such as $\det(\Gamma)$ are scalars (wrong representation), $\|\Gamma\|_F$ is metric-dependent (not purely structural), and $\mathrm{adj}(\Gamma)$ transforms with a different weight. The most general H-covariant linear map is $\mathcal{I}(\rho,\Gamma) = f(\rho)\Gamma$.

G-invariance then requires $f(\lambda\rho)\lambda^\alpha = f(\rho)$, which forces $f(\rho) \propto \rho^{-\alpha}$. So every $\alpha$ yields a candidate section $\mathcal{I} = \rho^{-\alpha}\Gamma$.

**Lemma 14.2 (Fixed section and $\alpha = -1$).** *The scaling generator $\rho\,d/d\rho$ acts on the candidate section $\rho^k\Gamma$ as:*
$$\rho\,\frac{d}{d\rho}(\rho^k\Gamma) = \rho\!\left[k\rho^{k-1}\Gamma + \rho^k\frac{\alpha\Gamma}{\rho}\right] = (k+\alpha)\,\rho^k\Gamma$$
*A fixed section (eigenvalue $0$ of the scaling generator) requires $k = -\alpha$. The minimum positive power $k$ for which the section involves $\rho$ non-trivially and the coupling "dilutes" with increasing level is $k = 1$. This forces $\alpha = -1$.*

*Proof.* $k > 0$ ensures $\rho$ appears in the numerator, encoding that coupling is suppressed at higher $\rho$ (C2). Among $k \in \{1, 2, 3, \ldots\}$, $k=1$ is minimal — it introduces the fewest powers of $\rho$ into the invariant, making $\rho\Gamma$ the primitive level-invariant object. $k=1 \implies \alpha = -1$. $\square$

The section $\mathcal{I} = \rho\Gamma$ is therefore the **unique minimal-order level-invariant structural object in the representation of $\Gamma$**, and $\alpha = -1$ is the unique exponent consistent with it.

$$\boxed{\alpha = -1}$$

\*\*Remark 14.1 (Dimensionality of $\mathcal{L}$).** Under T1, $\rho$ is dimensionless (an organizational index, not a physical length) and $\Gamma$ carries dimension $\rho^{-1}$ — also dimensionless in GSF natural units. The Lagrangian $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma)$ is therefore dimensionless: it measures *relative structural cost*, not energy in Joules. The correspondence to physical energy units — required to recover Newton's laws in §15.3, Maxwell's Lagrangian in §15.4, and the Einstein-Hilbert action in §15.5 — requires a global scaling constant with dimensions of energy. This constant is provided by the stratum bridge (Hito 3, Part III). In Chapters 15–18, all recoveries are structural (same equations of motion, same functional form) rather than quantitative (same coefficients in SI units).

---

## 14.5 Argument 3 — Covariance of the Equation of Motion

### 14.5.1 The EOM Covariance Requirement

The equation of motion of Ch13 §13.8:
$$\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\det(\Gamma)\,\Gamma^{-T} = N(t)$$

must be covariant under $(\rho, \Gamma) \to (\lambda\rho, \lambda^\alpha\Gamma)$: each term must transform with the same power of $\lambda$. If any term scales differently, the equation of motion would take a different form at different $\rho$ — violating the structural invariance of the GSF. Whether all physical systems satisfy this invariance is an empirical question addressed in Part IV.

### 14.5.2 EOM Covariance and Time-Scale Invariance

Under $(\rho, \Gamma) \to (\lambda\rho, \lambda^{-1}\Gamma)$ and $\mu(\lambda\rho) = \lambda^{2}\mu(\rho)$ (from $\mathrm{deg}(\mu) = -2\alpha = 2$):

**Term 1:** $\ddot\Gamma \to \lambda^{-1}\ddot\Gamma$ ✓

**Term 2:** $\gamma\dot\Gamma \to \lambda^{-1}\gamma\dot\Gamma$ ✓

**Term 3:** $\Gamma \to \lambda^{-1}\Gamma$ ✓

**Term 4:** $\frac{\mu(\lambda\rho)}{2}\det(\lambda^{-1}\Gamma)(\lambda^{-1}\Gamma)^{-T}$:
$$= \frac{\lambda^2\mu}{2}\cdot\lambda^{-4}\det(\Gamma)\cdot\lambda\,\Gamma^{-T} = \lambda^{2-4+1}\frac{\mu}{2}\det(\Gamma)\,\Gamma^{-T} = \lambda^{-1}\frac{\mu}{2}\det(\Gamma)\,\Gamma^{-T} \quad\checkmark$$

(using $\det(\lambda^{-1}\Gamma) = \lambda^{-4}\det(\Gamma)$ for a $4\times4$ matrix, and $(\lambda^{-1}\Gamma)^{-T} = \lambda\Gamma^{-T}$).

All four terms scale as $\lambda^{-1}$. The EOM is covariant under the scaling $(\rho,\Gamma) \to (\lambda\rho, \lambda^{-1}\Gamma)$.

**Remark 14.2 (EOM covariance does not uniquely fix $\alpha$ — scope clarification).** A direct computation shows that, for general $\alpha$ with $\mathrm{deg}(\mu) = -2\alpha$ (from Argument 2), all four EOM terms scale as $\lambda^\alpha$ simultaneously: the equation is covariant for *any* $\alpha$. Argument 3 therefore cannot fix $\alpha$ independently — it is a consistency check, not an additional constraint.

Argument 3 does, however, reveal a structural requirement through the *time-scale invariance* postulate:

**Postulate 14.1 (Time-Scale Invariance).** *The time parameter $t$ of GSF dynamics is structurally invariant — it does not rescale under changes of organizational level in the GSF equations. Formally: the joint rescaling $(t \to \lambda^\delta t,\; \rho \to \lambda\rho,\; \Gamma \to \lambda^\alpha\Gamma)$ must have $\delta = 0$ for the Lagrangian to maintain its form. Whether time is truly absolute in all physical systems is an empirical question not addressed here.*

*Derivation of $\delta = 0$.* Under joint rescaling with $\delta \neq 0$, terms 1–3 scale as:
$$\ddot\Gamma \to \lambda^{\alpha - 2\delta}, \quad \gamma\dot\Gamma \to \lambda^{\alpha - \delta}, \quad \Gamma \to \lambda^\alpha$$
EOM covariance requires all three to coincide: $\alpha - 2\delta = \alpha - \delta = \alpha \implies \delta = 0$. The time scale is forced to be absolute. $\square$

**Proposition 14.1 (EOM consistency of $\alpha = -1$).** *With $\delta = 0$ (Postulate 14.1), the EOM is covariant for any $\alpha$ with $\mathrm{deg}(\mu) = -2\alpha$. The value $\alpha = -1$ is confirmed consistent and is selected uniquely by the combined constraints of Arguments 1–2 (C2: $\alpha < 0$; C3: minimal invariant section $\to \alpha = -1$). The case $\alpha = -2$ is excluded by C3: it would require $k = 2$ in the minimal invariant section (i.e., $\rho^2\Gamma$) — a second-order coupling that violates the minimality requirement of Lemma 14.2. The case $\alpha = -1/2$ gives a non-integer $k$, placing $\mathcal{I}$ outside the polynomial representation of $\Gamma$.*

---

## 14.6 Convergence — T1 Derived

The three arguments establish $\alpha = -1$ by independent routes:

| Argument | Role | Output |
|---|---|---|
| 1 — Group structure | Establishes form | $\Gamma \propto \rho^\alpha$; $\alpha$ free |
| 2 — Lagrangian covariance | **Selects** $\alpha$ | C2: $\alpha < 0$; C3 (Lemma 14.2): $\alpha = -1$ |
| 3 — EOM covariance | Confirms + extracts $\delta = 0$ | $\alpha = -1$ consistent; time absolute |

The three arguments form a **structural triangulation**: Argument 1 constrains the form, Argument 2 (with C2+C3) selects $\alpha = -1$, and Argument 3 independently establishes that time does not rescale with organizational level. This is not three independent derivations of the same value — it is one selection argument supported by two structural consistency structures.

**Theorem 14.1 (The Scaling Law T1).** *The unique power-law scaling of $\Gamma$ under changes of organizational level consistent with (i) group composition of level changes, (ii) covariance of the structural Lagrangian, and (iii) covariance of the equation of motion is:*

$$\boxed{T1:\quad\Gamma(\rho) = \frac{\Gamma(\rho_{\mathrm{ref}})\cdot\rho_{\mathrm{ref}}}{\rho} \qquad\Longleftrightarrow\qquad \frac{d\Gamma}{d\rho} = -\frac{\Gamma}{\rho}}$$

*The configuration matrix scales inversely with the organizational level. Structural coupling decreases as the system ascends in organizational complexity.*

**Remark 14.3 (Interpretation of T1).** The inverse scaling $\Gamma \propto \rho^{-1}$ has a structural reading: at higher organizational levels (larger $\rho$), the system operates under more constraints — physical, biological, psychological — and the available coupling range per degree of freedom is reduced. A bacterium ($\rho_{\mathrm{biol}}$) has less structural freedom than a quantum field ($\rho_{\mathrm{quantum}}$), not because it is simpler in terms of component count, but because its organizational constraints are more restrictive. T1 makes this hierarchy precise and quantitative.

**Remark 14.4 (Epistemic status of $\alpha = -1$).** The selection of $\alpha = -1$ rests entirely on Argument 2: C2 narrows to $\alpha < 0$, and C3 (Lemma 14.2) selects $\alpha = -1$ via the minimal invariant section. Argument 3 provides an independent structural result (time-scale invariance, $\delta = 0$) and confirms consistency, but does not supply an independent constraint on $\alpha$. The previous framing of "three independent arguments" overstated the case; the accurate description is *structural triangulation* — one selection chain and two consistency checks — as stated in the convergence table above.

---

## 14.7 Consequences of T1

### 14.7.1 The Structural Coherence $c(\rho)$

From T1 with $\Gamma(\rho) = \Gamma_0\rho^{-1}$:

$$\det(\Gamma(\rho)) = \det\!\left(\frac{\Gamma_0}{\rho}\right) = \frac{\det(\Gamma_0)}{\rho^4}$$

The structural coherence at the attractor is $c(\rho) = \det(P(\Gamma|\rho))$. The attractor condition from Ch13 §13.5 is $P(\Gamma)P(\Gamma)^T = -(\mu/2)\det(P(\Gamma))\cdot\mathbf{1}_4$ — a relation homogeneous of degree 2 in $P$ on both sides (left: degree 2; right: $\mu \cdot \det(P) \cdot \mathbf{1}$, also degree 2 via the fixed-point relation $\mu = 2/\sqrt{\det(P)}$). This homogeneity means: if $\Gamma \to \lambda^{-1}\Gamma$ (T1 with $\lambda = \rho/\rho_{\mathrm{ref}}$), then $P \to \lambda^{-1}P$, and $\det(P) \to \lambda^{-4}\det(P)$. Thus $c(\rho) = \det(P(\Gamma|\rho))$ inherits the $\rho^{-4}$ scaling of $\det(\Gamma)$ directly. Using the anchor $c(\rho_{\mathrm{GR}}) = 1$:

$$\boxed{c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4}$$

**Corollary 14.2 (Hierarchy of coherence).** *The structural coherence $c(\rho)$ is a strictly decreasing function of $\rho$ for $\rho > \rho_{\mathrm{GR}}$ and strictly increasing for $\rho < \rho_{\mathrm{GR}}$:*
- $\rho < \rho_{\mathrm{GR}}$: $c(\rho) > 1$ — sub-gravitational levels (quantum physics) have structural coherence exceeding the gravitational reference. Quantum superposition and entanglement are manifestations of $c > 1$.
- $\rho = \rho_{\mathrm{GR}}$: $c = 1$ — the gravitational anchor.
- $\rho > \rho_{\mathrm{GR}}$: $c(\rho) < 1$ — supra-gravitational levels (matter, biology, mind) have lower structural coherence. Decoherence is the process of increasing $\rho$ beyond $\rho_{\mathrm{GR}}$.

### 14.7.2 The Coupling Strength $\mu(\rho)$

From $\mu(\rho) = 2/\sqrt{c(\rho)}$:

$$\boxed{\mu(\rho) = 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^2}$$

This is an exact, parameter-free function of $\rho$. Key values:

| $\rho$ | System | $\mu(\rho)$ | Physical meaning |
|---|---|---|---|
| $\rho \to 0$ | Fundamental limit | $\mu \to 0$ | No structural attractor; maximally free |
| $\rho_{\mathrm{GR}}$ | Gravity | $\mu = 2$ | The unique anchor; massless graviton |
| $\rho_{\mathrm{biol}} \gg \rho_{\mathrm{GR}}$ | Living systems | $\mu \gg 2$ | Strong homeostatic attractor |
| $\rho_{\mathrm{psych}} \gg \rho_{\mathrm{biol}}$ | Psychological systems | $\mu$ largest | Highest coordination cost; strongest identity maintenance |

The monotone increase of $\mu$ with $\rho$ encodes a structural fact: more organizationally complex systems require more structural "glue" to maintain their identity — not that they are behaviorally rigid, but that the *cost of preserving their coupling pattern* against perturbations is higher. A neural network is behaviorally flexible but structurally expensive to reorganize; a quantum field is structurally free but organizationally primitive. This is the GSF formalization of organizational coordination cost (Constraint C2).

### 14.7.3 Structural Invariance of $\kappa = -1$

The Frobenius metric $\|\Gamma\|_F^2 = \mathrm{tr}(\Gamma^T\Gamma)$ is invariant under uniform rescaling in the following sense: under $\Gamma \to \lambda^{-1}\Gamma$, the metric scales as $\lambda^{-2}$ — the *shape* of the metric (its sectional curvatures, its ratio of symmetric to antisymmetric sector weights) does not change. Only the overall scale changes. Therefore, within the GSF framework:

$$\boxed{\kappa(\rho) = -1 \quad\forall\,\rho}$$

The kinetic structure of the Lagrangian is structurally invariant: the "grammar" of how $\Gamma$ changes in time is identical at every organizational level *within the GSF equations*. What changes between levels is only the strength of the attractor $\mu(\rho)$ — the "vocabulary" varies while the "syntax" remains fixed. Empirically, whether this holds for all physical systems is Part IV's domain.

### 14.7.4 The Complete Lagrangian

Combining Ch13 (structure) with T1 (scaling):

$$\boxed{\mathcal{L}(\Gamma, \dot\Gamma, \rho) = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)}$$

$$\boxed{\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\!\det(\Gamma)\,\Gamma^{-T} = N(t)}$$

**Zero free parameters given $\rho_{\mathrm{GR}}$.** Every term is determined: the kinetic coefficient by Frobenius, the quadratic potential by normalization, the quartic coefficient by $\mu(\rho)$ from T1 and the anchor $c(\rho_{\mathrm{GR}})=1$. The single reference $\rho_{\mathrm{GR}}$ — the organizational level at which the gravitational coupling has unit coherence — is the only input.

---

## 14.8 Structural Predictions from T1

T1 produces the first genuinely predictive content of the GSF — results that follow from the Lagrangian without domain-specific input.

### 14.8.1 The Matter Creation Threshold $\rho_{\mathrm{mat}}$

The effective potential of the structural Lagrangian along the isotropic direction $\Gamma = \sigma\cdot I$ (proportional to identity, capturing the "amplitude" of coupling):

$$V_{\mathrm{eff}}(\sigma, \rho) = \|\sigma I\|_F^2 + \mu(\rho)\det(\sigma I) = 4\sigma^2 + 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\!\sigma^4$$

This potential has a single minimum at $\sigma = 0$ for all $\rho$ in the isotropic case. However, for configurations with $\det(\Gamma) < 0$ (Lorentzian-signature coupling, natural in the relativistic sector), the quartic term contributes negatively:

$$V_{\mathrm{eff}}(\sigma, \rho)\big|_{\det < 0} = 4\sigma^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\!\sigma^4$$

This potential has a local maximum at $\sigma = 0$ and a barrier of height:

$$\Delta V(\rho) = V(\sigma_{\mathrm{crit}}) - V(0) = 2\!\left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^{\!2}$$

where $\sigma_{\mathrm{crit}} = \rho_{\mathrm{GR}}/\rho$ is the critical amplitude. The barrier decreases with increasing $\rho$.

**Definition 14.1 (Matter creation threshold).** The organizational level $\rho_{\mathrm{mat}}$ is defined by the condition that the potential barrier $\Delta V(\rho_{\mathrm{mat}})$ equals the characteristic fluctuation energy $E_{\mathrm{fluct}}$ available at that level:

$$\Delta V(\rho_{\mathrm{mat}}) = E_{\mathrm{fluct}} \implies \boxed{\rho_{\mathrm{mat}} = \rho_{\mathrm{GR}}\sqrt{\frac{2}{E_{\mathrm{fluct}}}}}$$

**Interpretation.** Below the barrier ($\rho < \rho_{\mathrm{mat}}$, fluctuation energy insufficient), the system remains in the $\sigma = 0$ vacuum — pure field, no localized matter. Above the barrier ($\rho \geq \rho_{\mathrm{mat}}$, fluctuation energy sufficient), the system can nucleate into a non-zero $\sigma$ configuration — localized matter. The level $\rho_{\mathrm{mat}}$ is the organizational threshold for the field-to-matter transition.

**Consequence.** Since $\Delta V(\rho_{\mathrm{GR}}) = 2$ and $\Delta V(\rho) = 2(\rho_{\mathrm{GR}}/\rho)^2 < 2$ for $\rho > \rho_{\mathrm{GR}}$, the barrier at the gravitational level equals 2. Matter nucleates above $\rho_{\mathrm{GR}}$ — i.e., $\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$ — *provided* $E_{\mathrm{fluct}} < 2$. This is an explicit premise: if $E_{\mathrm{fluct}} \geq 2$, the barrier is already overcome at $\rho = \rho_{\mathrm{GR}}$ and the threshold ordering changes. Under the assumption $E_{\mathrm{fluct}} < 2$, matter is *structurally more complex than pure geometry* — it exists at a higher organizational level — consistent with the physical hierarchy: spacetime geometry (GR) is more fundamental than the matter content that inhabits it.

**Connection to cosmology.** If $E_{\mathrm{fluct}} = k_B T$, then $\rho_{\mathrm{mat}} = \rho_{\mathrm{GR}}\sqrt{2/(k_BT)}$. High $T$ means large $E_{\mathrm{fluct}}$ and smaller $\rho_{\mathrm{mat}}$: the barrier is overcome more easily. As the universe cools ($T$ decreasing), $\rho_{\mathrm{mat}}$ increases — the nucleation threshold rises. This is the GSF picture of the field-to-matter transition as a thermal phase transition. The precise value of $E_{\mathrm{fluct}}$ in terms of fundamental scales remains to be identified (see §14.9).

**Remark 14.5 (Global instability of the Lorentzian potential).** The potential $V_{\mathrm{eff}} = 4\sigma^2 - 2(\rho/\rho_{\mathrm{GR}})^2\sigma^4$ has no global minimum: once the barrier at $\sigma_{\mathrm{crit}}$ is overcome, the system rolls to $\sigma \to \infty$. This is a genuine limitation of the degree-4 minimal Lagrangian. Two resolutions are possible within the GSF:

*(a) Higher-order terms:* A degree-6 term $+\nu\sigma^6$ (arising from higher-order invariants beyond the minimal basis of Ch13) would stabilize the matter state. Such terms are not part of the minimal Lagrangian but would appear naturally in a quantum extension (renormalization group corrections, Remark 14.6).

*(b) Metastable interpretation:* The "matter" configuration is a long-lived metastable state — stable on cosmological timescales due to the large barrier $\Delta V$ at astrophysically accessible $\rho$, but ultimately transient. This interpretation is consistent with the observation that matter, at the largest scales, does eventually decohere.

The present chapter does not resolve this; the stability of the matter state under the degree-4 Lagrangian is an open question for Part III.

### 14.8.2 The Cosmological Constant

From Ch13 Remark 13.5, the effective cosmological constant in the linearized GR limit is:
$$\Lambda_{\mathrm{eff}} \propto \mu(\rho_{\mathrm{GR}}) - 2 = 0$$

The exact value $c(\rho_{\mathrm{GR}}) = 1$ implies $\mu(\rho_{\mathrm{GR}}) = 2$ exactly, giving $\Lambda_{\mathrm{eff}} = 0$ in the GSF natural units. The observed cosmological constant $\Lambda_{\mathrm{obs}} \approx 10^{-52}\,\mathrm{m}^{-2}$ is non-zero but extremely small.

T1 reframes the cosmological constant problem. The question "why is $\Lambda$ so small?" becomes "why is $c(\rho_{\mathrm{GR}})$ so close to 1?" — which has a structural answer: $c(\rho_{\mathrm{GR}}) = 1$ exactly because the massless graviton condition is exact. The deviation $\varepsilon = c(\rho_{\mathrm{GR}}) - 1$ encodes the degree to which the massless graviton approximation breaks down — equivalently, the degree to which diffeomorphism invariance is exact. If diffeomorphism invariance is a fundamental symmetry (as in standard GR), then $\varepsilon = 0$ exactly and $\Lambda_{\mathrm{eff}} = 0$ in the GSF.

The observed $\Lambda_{\mathrm{obs}} \approx 10^{-52}\,\mathrm{m}^{-2} \neq 0$ is therefore a genuine tension with the GSF in its present form. Two interpretations are possible:

*(i) Structural deviation:* $c(\rho_{\mathrm{GR}}) = 1 - \varepsilon$ with $\varepsilon \neq 0$ — a small but nonzero deviation from the exact massless graviton condition. This would imply that diffeomorphism invariance is only approximate, generating $\Lambda_{\mathrm{eff}} \propto \varepsilon$. The precise mechanism for $\varepsilon \neq 0$ is not yet derived within the GSF.

*(ii) Quantum corrections:* The classical GSF predicts $\Lambda_{\mathrm{eff}} = 0$; quantum corrections to T1 (logarithmic terms, see Remark 14.6) could generate a small nonzero $\Lambda$. This route is open for the quantum extension of the GSF.

**Caution.** The statement "$\Lambda_{\mathrm{obs}} \neq 0$ can be explained by unit conversion" is not correct — a quantity that is exactly zero in any consistent unit system remains zero in any other unit system. The discrepancy between $\Lambda_{\mathrm{eff}} = 0$ and $\Lambda_{\mathrm{obs}} \neq 0$ is a genuine open problem for the GSF, not an artifact of unit choice. It is declared here as an open question.

**Structural observation (sign consistency).** Although the GSF in its minimal classical form predicts $\Lambda_{\mathrm{eff}} = 0$, route (i) above — a deviation $\varepsilon = c(\rho_{\mathrm{GR}}) - 1 < 0$ — produces $\mu(\rho_{\mathrm{GR}}) = 2/\sqrt{1-|\varepsilon|} > 2$, i.e., $\Delta\mu = \mu(\rho_{\mathrm{GR}}) - 2 > 0$. The effective cosmological constant $\Lambda_{\mathrm{eff}} \propto \Delta\mu > 0$ would then be *positive* — consistent with the observed sign of $\Lambda_{\mathrm{obs}} > 0$. This is a structural qualitative prediction, not a quantitative one: the GSF identifies which deviation from the exact massless graviton condition would produce a positive $\Lambda$, without yet determining its magnitude.

---

## 14.9 Epistemic Status and Open Questions

T1 completes the classical GSF Lagrangian but opens a set of well-posed questions for further work.

| Result | Status | Notes |
|---|---|---|
| Scaling law $\alpha = -1$ | Structural triangulation: form (Arg 1) + selection (Arg 2: C2+C3) + consistency (Arg 3) | See Remark 14.4 |
| C3 — minimal invariant section | Representation-theoretic (Lemma 14.2) | H-covariance → linearity; fixed section → $\alpha=-1$ |
| $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ | Derived: T1 + attractor homogeneity + anchor $c(\rho_{\mathrm{GR}})=1$ | Exact within power-law assumption |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | Derived from $c(\rho)$ via Ch13 §13.5 | Explicit, parameter-free |
| $\kappa(\rho) = -1$ universal | Derived — Frobenius shape invariance | Universal across all $\rho$ |
| $[\mathcal{L}] = 1$ (dimensionless) | Structural | Physical units require Hito 3 scaling constant |
| Complete $\mathcal{L}$ — zero free parameters | Structural Lagrangian only | $\gamma$, $N(t)$ open in dissipative EOM |
| $\delta = 0$ (time-scale invariance) | Derived — Postulate 14.1 | Universal time parameter |
| $\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$ | Conditional | Requires $E_{\mathrm{fluct}} < 2$ (open) |
| Matter state stability | Open | $-\sigma^4$ globally unstable; degree-6 or metastable interpretation (Part III) |
| $\Lambda_{\mathrm{eff}} = 0$ (classical GSF) | Derived | Tension with $\Lambda_{\mathrm{obs}} \neq 0$; $\Delta\mu > 0$ qualitatively consistent with positive sign |
| Higher-order corrections to T1 | Open | Is $\alpha = -1$ exact or leading order? |
| $c(\rho)$ for $\rho < \rho_{\mathrm{GR}}$ | Derived but unverified | $c > 1$ — physical meaning in quantum domain? |
| Absolute scale of $\rho_{\mathrm{GR}}$ | Open | Hito 3 (Planck bridge) |

**The central open question.** T1 derives $c(\rho)$ as a function, but $\rho$ remains dimensionless — it has no absolute scale within the GSF. The statement "$\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$" establishes a relative ordering, but the statement "$\rho_{\mathrm{mat}} = 10^3\,\rho_{\mathrm{GR}}$" requires knowing the conversion between $\rho$ and a physical quantity. This conversion — the stratum bridge — is Hito 3. Until it is established, the predictions of §14.8 are structural (qualitative ordering, functional form) rather than numerical (specific values).

**Remark 14.6 (On logarithmic corrections).** Argument 2 and 3 derived $\alpha = -1$ under the assumption of exact power-law scaling. It is possible in principle that the exact scaling law takes the form $\Gamma(\rho) = \Gamma_0/(\rho\,h(\rho))$ with $h(\rho) = 1 + a\log(\rho/\rho_0) + \ldots$ — logarithmic corrections that vanish for $\rho \approx \rho_0$ but become important at extreme scales. Such corrections would arise naturally from a renormalization group analysis of the GSF action, where $\rho$ plays the role of the energy scale. The derivation of T1 at this level of precision requires the quantum extension of the GSF Lagrangian, beyond the scope of Part II.

---

## 14.10 Summary — The Completed Lagrangian

The structural Lagrangian of the GSF, in its final form after T1:

$$\boxed{\mathcal{L}(\Gamma, \dot\Gamma, \rho) = \underbrace{\|\dot\Gamma\|_F^2}_{\text{kinetic}} - \underbrace{\|\Gamma\|_F^2}_{\text{quadratic}} - \underbrace{2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)}_{\text{quartic (attractor)}}}$$

Each coefficient has a derivational origin:
- **Kinetic coefficient = 1:** from Frobenius uniqueness (Ch13 §13.4 / Theorem 13.1)
- **Quadratic coefficient = −1:** from normalization and potential sign (Ch13 §13.3)
- **Quartic coefficient = $2(\rho/\rho_{\mathrm{GR}})^2$:** from T1 ($\alpha = -1$) + anchor $c(\rho_{\mathrm{GR}}) = 1$

No coefficient of the structural Lagrangian is adjusted to fit data. No free parameter remains in $\mathcal{L}(\Gamma, \dot\Gamma, \rho)$ given the single reference $\rho_{\mathrm{GR}}$.

**Scope of "zero free parameters."** This claim applies strictly to the conservative structural Lagrangian. The dissipative EOM $\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \mu(\rho)\,\mathrm{adj}(\Gamma)^T/2 = N(t)$ retains two open inputs: the damping coefficient $\gamma$ (organizational rigidity — domain-dependent) and the forcing $N(t)$ (environmental input — context-dependent). These are not free parameters of the *structural theory* but physical inputs describing the specific UoC and its environment. Their determination requires domain-specific modeling beyond the GSF Lagrangian.

The framework has arrived at the condition it needs to be a theory rather than a language: it can be wrong.

*Part II now proceeds to test it.*

---

---

## 14.11 The ρ Anchor Catalog — Known, Calibratable, Blocked

$c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ is structurally complete, but $\rho$ itself has no absolute numerical value within the GSF — it is dimensionless and measured relative to $\rho_{\mathrm{GR}}$. The correspondence between $\rho_{\mathrm{GR}}$ and a physical scale (Planck energy, Planck length) requires Hito 3 (stratum bridge, Part III). Until then, ρ values fall into three operational categories:

| Category | Domain | ρ value | Basis | What it enables |
|---|---|---|---|---|
| **Derived** | Gravity (GR) | $\rho_{\mathrm{GR}}$ (reference = 1) | Massless graviton condition: $\mu(\rho_{\mathrm{GR}}) = 2$ — exact | $c = 1$; Lagrangian fully fixed |
| **Structural ratio** | Matter threshold | $\rho_{\mathrm{mat}} = \rho_{\mathrm{GR}}\sqrt{2/E_{\mathrm{fluct}}}$ | §14.8.1 — conditional on $E_{\mathrm{fluct}}$ | Ordering $\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$; not SI value |
| **Structurally constrained** | EM | $\rho_{\mathrm{EM}}$ by SO(3,1) → U(1) symmetry breaking | Hypothesis H1 (cuantizacion_rho.md) | Blocked until stratum bridge fixes $\alpha$ |
| **Empirically calibratable** | Living systems ($\rho_{\mathrm{biol}}$) | Domain-specific proxy | E.g., viability index, homeostatic margin | $\mu(\rho_{\mathrm{biol}})$ can be fitted from data |
| **Empirically calibratable** | Economics ($\rho_{\mathrm{econ}}$) | Domain-specific proxy | E.g., inverse of Herfindahl index, sector diversity | $\mu(\rho_{\mathrm{econ}})$ fitted; see §14.11.1 |
| **Empirically calibratable** | Psychology ($\rho_{\mathrm{psych}}$) | Domain-specific proxy | E.g., EEG coherence, HeartMath HRV | $\mu(\rho_{\mathrm{psych}})$ fitted |
| **Limit** | Fundamental ($\rho \to 0$) | $c \to \infty$, $\mu \to 0$ | Structural limit of T1 | No attractor; maximally free |

**The key structural point:** $c(\rho)$ is fully determined as a *function* of $\rho/\rho_{\mathrm{GR}}$. What is not determined is the absolute correspondence between the ratio $\rho/\rho_{\mathrm{GR}}$ and any measurable physical quantity in SI units. This gap is Hito 3.

### 14.11.1 Operational ρ for Non-Physical Domains

For domains where no independent derivation of ρ is available, ρ can be operationalized as a **structural diversity index** — a dimensionless measure of the effective degrees of freedom in the coupling matrix $\Gamma$:

$$\rho_{\mathrm{domain}} \;\propto\; \frac{\mathrm{rank}(\Gamma)}{\dim(\Gamma)} \cdot \sqrt{\frac{\det(\Gamma)}{\|\Gamma\|_F^4/n^2}}$$

This proxy satisfies T1 qualitatively: systems with more active structural dimensions (higher rank, closer to isotropic) have lower ρ-like coupling cost; systems with collapsed rank (near monopoly, near-degenerate channels) have higher effective ρ. It is not derived from the GSF Lagrangian — it is a calibration strategy for domains outside the physics correspondence.

**Consequence for quantitative predictions.** In non-physical domains, the GSF makes:
- **Qualitative structural predictions** (which configurations are attractors, which are fragile) — independent of ρ calibration.
- **Comparative predictions** (domain A is structurally more fragile than domain B) — requires only relative ρ.
- **Absolute quantitative predictions** (specific timescales, thresholds in SI units) — blocked until Hito 3 or empirical ρ calibration from domain data.

The reductions of Chapters 16–17 operate in the first two categories. The third category is explicitly deferred.

---

*Chapters 15–18 apply the Lagrangian of Theorem 14.1 to five structurally distinct domains — mechanics, scalar fields, information theory, economics, and living systems — and verify in each case that the GSF equations of motion reduce to known results without any further parameter adjustment. The tests are not demonstrations of fit; they are proofs of structural consistency.*
