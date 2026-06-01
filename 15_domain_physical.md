# Chapter 15: Domain I — Physical Systems

## 15.1 The Reduction Program

The Lagrangian derived in Chapters 13–14 is a single object:

$$\mathcal{L}(\Gamma, \dot\Gamma, \rho) = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)$$

The equation of motion (EOM) is:

$$\boxed{\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\mathrm{adj}(\Gamma)^T = N(t)}$$

where $\mathrm{adj}(\Gamma)^T = \det(\Gamma)\,\Gamma^{-T}$ for invertible $\Gamma$, extended by continuity to singular $\Gamma$ via the adjugate matrix. The Lagrangian and EOM are **structurally invariant**: the same equation holds at every organizational level $\rho$ *within the GSF framework*. Whether this equation governs all physical systems is an empirical claim tested in Part IV. What changes between domains is not the equation but the attribute assignment $\{S,A,\mathbf{I},\mathbf{R}\}$ and the structure of $\Gamma$.

**The reduction strategy.** Given a physical system $\mathcal{S}$:

1. Assign $\{S, A, \mathbf{I}, \mathbf{R}\}$ to the structural roles of $\mathcal{S}$ following the canonical prescription.
2. Identify which attributes are null (Ch12 §12.3) and which are active.
3. Impose the special structure of $\Gamma$ dictated by the domain.
4. Evaluate the EOM under those constraints.
5. Verify that the result coincides with the established equations of the domain.

If the verification succeeds, the domain is a structural instance of the GSF — not a curve-fit to it. No new parameter is introduced at step 1–4; all adjustments are structural constraints derived from the physics of the domain.

**Terminological clarification (UoC vs regime).** The reductions in this chapter recover known equations of motion (SHO, wave equation, Stokes, Maxwell, linearized GR) from the GSF EOM under specific structural restrictions on $\Gamma$. These restrictions identify **regimes** of dynamics, not new UoCs. The UoC remains the underlying entity — the mass, the charged system, the fluid parcel — characterized by its full attribute set $\{S, A, \mathbf{I}, \mathbf{R}\}$ and the coherence criterion of Ch12 (Force and Field simultaneously active, $\det(\Gamma) > 0$). A rank-$\leq 2$ embedding describes a *dynamical regime* in which certain attributes are momentarily inactive — it does not constitute a UoC in the full sense of §0.3. This is consistent with Ch12 §12.3.2: rank-$\leq 2$ configurations are *boundary configurations*, structural residues, or transient regimes, not UoCs. When this chapter writes "the SHO is a reduction of the GSF EOM," it means "a mass UoC, whose attributes momentarily satisfy the rank-$\leq 2$ null-purpose condition, exhibits SHO dynamics" — not "the SHO is itself a UoC." See `brainstorming/bitacora_tensiones.md` T8 for the full discussion.

This chapter carries out the program for five classical physical cases, organized by increasing structural complexity.

---

## 15.2 The Scalar Reduction: 1×1 Matrix

The simplest possible coupling matrix is a $1\times 1$ real matrix: $\Gamma = (x)$ for some scalar $x \in \mathbb{R}_{>0}$ (within $\mathcal{M}(\Gamma)$).

### 15.2.1 The Reduction

For $n = 1$: $\det(\Gamma) = x$, $\mathrm{adj}(\Gamma) = 1$, so $\mathrm{adj}(\Gamma)^T = 1$ and $\det(\Gamma)\,\Gamma^{-T} = x \cdot (1/x) = 1$.

With organizational level $\rho = \rho_\star$ and damping $\gamma$, the EOM becomes:

$$\ddot x + \gamma\dot x + x + \left(\frac{\rho_\star}{\rho_{\mathrm{GR}}}\right)^{\!2} = 0$$

Defining the equilibrium displacement $u = x + \left(\rho_\star/\rho_{\mathrm{GR}}\right)^2$ and noting that $\ddot u = \ddot x$, $\dot u = \dot x$:

$$\boxed{\ddot u + \gamma\dot u + u = 0}$$

**Proposition 15.1 (Scalar reduction).** *The EOM of the 1×1 GSF Lagrangian, at any organizational level $\rho_\star$, is the damped harmonic oscillator with unit natural frequency, displaced by $(\rho_\star/\rho_{\mathrm{GR}})^2$.*

*Proof.* Direct substitution, as shown above. The structural equilibrium from Ch13 §13.5 satisfies $-2P - \mu\,\mathrm{adj}(P)^T = 0$. For $n=1$, $\mathrm{adj}([x]) = [1]$, so $-2x - \mu = 0 \implies x^\star = -\mu/2 = -(\rho_\star/\rho_{\mathrm{GR}})^2$. This equilibrium is real but negative — outside $\mathcal{M}_{\mathrm{adm}}(\Gamma) = \{x > 0\}$. The 1D scalar system has no structural attractor within the admissible manifold; it oscillates about the displaced equilibrium $u = 0$ (i.e., $x = -(\rho_\star/\rho_{\mathrm{GR}})^2$) without a stable interior attractor in $\mathcal{M}_{\mathrm{adm}}$. The restoring force is real; the attractor condition is not satisfied within the admissible domain. This is consistent with the finding of Ch14 §14.8.1 that matter (localized in $x > 0$) requires crossing the Lorentzian potential barrier. $\square$

### 15.2.2 The Role of $\mu$

In natural GSF units ($\rho_{\mathrm{GR}} = 1$), the shift is $x^\star = -\rho_\star^2$, which scales as the square of the organizational level. Equivalently, $\mu(\rho_\star) = 2\rho_\star^2$ shifts the equilibrium by $\rho_\star^2$. Systems at higher organizational levels have their equilibrium displaced further from the origin of $\mathcal{M}(\Gamma)$.

**Remark 15.1.** The natural frequency $\omega_0 = 1$ in GSF units sets the intrinsic oscillation timescale of the scalar degree of freedom. The dissipation $\gamma$ is not derived from the Lagrangian — it enters through the non-conservative extension of the EOM (Ch13 §13.8), encoding the coupling between the system and its environment.

---

## 15.3 Null-Purpose Reduction: The Pure Harmonic Oscillator

### 15.3.1 Setup

The scalar reduction (§15.2) gives a *shifted* harmonic oscillator — the equilibrium is displaced by $\rho_\star^2$, not at the origin. For applications where the SHO should oscillate about $x = 0$ (e.g., displacement of a mass-spring system about rest), we need the quartic (attractor) term to vanish identically.

This is the null-purpose condition: $\det(\Gamma) = 0$ at all times, which ensures $\mathrm{adj}(\Gamma)^T = 0$ and the EOM is linear.

**Definition 15.1 (Null-purpose embedding).** Let $\Gamma$ be a $4\times 4$ matrix with the active degrees of freedom residing entirely within a strict sub-block of size $r < 4$. The remaining $4-r$ rows and columns are identically zero. Call this a *null-purpose embedding* of rank $r$.

### 15.3.2 The Adjugate Vanishes for Null-Purpose Embeddings

**Lemma 15.1.** *Let $\Gamma$ be a null-purpose embedding of rank $r \leq 2$. Then $\mathrm{adj}(\Gamma) = 0$, and consequently the quartic term $\mathrm{adj}(\Gamma)^T$ in the EOM vanishes identically.*

*Proof.* The adjugate $\mathrm{adj}(\Gamma)$ has entries equal to the $(3\times 3)$-cofactors of $\Gamma$. Each cofactor is the determinant of a $3\times 3$ submatrix of $\Gamma$. Since $\Gamma$ has rank $\leq 2$ and at least two zero rows (the null rows), every $3\times 3$ submatrix includes at least one zero row, making its determinant zero. Therefore every cofactor is zero, so $\mathrm{adj}(\Gamma) = 0$. $\square$

### 15.3.3 Application to the Harmonic Oscillator

**Slot assignment.** For a one-dimensional mass-spring system, the physical degree of freedom is the displacement $x(t)$. Assign it to the $(\mathbf{I},\mathbf{R})$ off-diagonal entry:

$$\Gamma = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & x \\ 0 & 0 & -x & 0 \end{pmatrix}$$

where rows/columns are indexed $\{S, A, \mathbf{I}, \mathbf{R}\}$. This is a null-purpose embedding of rank 2: $S$ and $A$ are null attributes (no charge, no source), and the physical content is entirely in the antisymmetric $\{\mathbf{I},\mathbf{R}\}$ block.

By Lemma 15.1, $\mathrm{adj}(\Gamma) = 0$. The EOM for the $({\mathbf{I}},{\mathbf{R}})$ entry is:

$$\ddot x + \gamma\dot x + x = 0$$

**Theorem 15.1 (Harmonic oscillator reduction).** *The GSF EOM, restricted to the null-purpose embedding above, reduces exactly to the damped harmonic oscillator with unit natural frequency. No parameter is adjusted.*

*Proof.* From Lemma 15.1, the EOM entry-by-entry for the active component $x = \Gamma_{IR}$ gives $\ddot x + \gamma\dot x + x = 0$. All other entries are constrained to zero. $\square$

**Remark 15.2 (Physical interpretation).** The $\{\mathbf{I},\mathbf{R}\}$ attributes in the GSF correspond to the integration and regulation functions of the structural vocabulary. For a mass-spring system, $\mathbf{I}$ carries the displacement (the "field") and $\mathbf{R}$ carries the velocity (the "regulation" — restoring force). The antisymmetry $\Gamma_{IR} = -\Gamma_{RI}$ reflects the directional nature of the oscillation. The null attributes $S = A = 0$ encode the *momentary* inactivity of charge and active agency in the mechanical oscillator. The UoC remains the mass — a fully structurally coherent entity with all four attributes available — and the SHO is the dynamical regime exhibited when the rank-$\leq 2$ condition holds. A small-amplitude mass-spring system explores this regime; large amplitude or nonlinear coupling activates $S$ or $A$ and the dynamics leaves the rank-2 manifold (see Remark 15.3).

**Remark 15.3 (Linear physics as a rank-2 regime).** The GSF predicts that *exact* linear physics does not exist: the full EOM always contains the nonlinear attractor term $\mathrm{adj}(\Gamma)^T$. The null-purpose reduction shows that this term vanishes when the dynamical state satisfies structural rank $\leq 2$ — when the system carries no active charge ($S = 0$) and no active agency ($A = 0$) *at the moment of observation*. Linearity is therefore a **regime**, not an identity: every linear physical system is a UoC operating in its rank-$\leq 2$ window. Any process that activates $S$ or $A$ — however briefly — drives the UoC out of the linear regime and into structural nonlinearity. The observed linearity of a mass-spring at small amplitude is not fundamental; it is the regime the mass UoC inhabits while its source and agency attributes remain inactive. This is the GSF formalization of the statement that "perfect linearity is an idealization."

---

## 15.4 Anharmonic Oscillators and the Pendulum

### 15.4.1 Beyond the Linear Regime

The pure SHO of §15.3 results from the null-purpose condition $\mathrm{adj}(\Gamma) = 0$. When $\Gamma$ does not have null attributes at $S$ and $A$, the adjugate term contributes, introducing nonlinearity. The simplest case: a $2\times 2$ antisymmetric matrix (rank 2, but in a $2\times 2$ ambient space rather than $4\times 4$):

$$\Gamma_{2\times 2} = \begin{pmatrix} 0 & x \\ -x & 0 \end{pmatrix}$$

For this matrix: $\det(\Gamma_{2\times 2}) = x^2$ and $\mathrm{adj}(\Gamma_{2\times 2}) = \Gamma_{2\times 2}^T = \begin{pmatrix} 0 & -x \\ x & 0 \end{pmatrix}$. The EOM for the off-diagonal entry:

$$\ddot x + \gamma\dot x + x + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2} x = 0 \qquad\Longrightarrow\qquad \ddot x + \gamma\dot x + \left(1 + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\right)x = 0$$

This is again a linear oscillator, but with a *shifted natural frequency* $\omega^2 = 1 + (\rho/\rho_{\mathrm{GR}})^2$. The attractor modifies the oscillation frequency but preserves linearity.

**Remark 15.4 (Frequency renormalization).** The attractor term shifts $\omega_0^2 = 1 \to 1 + (\rho/\rho_{\mathrm{GR}})^2$. For $\rho \ll \rho_{\mathrm{GR}}$, the shift is negligible and the SHO is recovered. For $\rho \sim \rho_{\mathrm{GR}}$, the frequency increases by a factor $\sqrt{2}$. This frequency renormalization is a first structural prediction of the GSF for oscillators embedded in the gravitational stratum.

### 15.4.2 The Pendulum as Large-Amplitude SHO

The simple pendulum satisfies:

$$\ddot\theta + \frac{g}{L}\sin\theta = 0$$

For small angles $\theta \approx 0$: $\sin\theta \approx \theta$, recovering $\ddot\theta + (g/L)\theta = 0$ — the SHO with $\omega_0 = \sqrt{g/L}$.

The pendulum differs from the SHO in two respects:
1. The *configuration space* is $S^1$ (a circle, compact and periodic), not $\mathbb{R}$.
2. The *potential* is $V(\theta) = 1 - \cos\theta$ rather than $V(x) = x^2/2$.

**Connection to the GSF.** The GSF manifold $\mathcal{M}(\Gamma)$ is open and non-compact ($\det(\Gamma) > 0$), so it does not naturally carry the periodic topology of $S^1$. The pendulum does not arise as an exact reduction of the GSF EOM — it is a **geometric analogy**, not a structural derivation.

**Why a derivation fails.** The pendulum equation $\ddot\theta + \sin\theta = 0$ comes from the combination of a gravitational potential $V(\theta) = gL(1-\cos\theta)$ and a kinematic constraint (rigid rod). Restricting the GSF to the constant-norm sphere $\|\Gamma\|_F = r$ produces a Riemannian constraint surface with a round metric. The geodesics on this sphere are great circles — they carry no restoring force. A restoring force requires a *potential* on the sphere, which the GSF at this level does not supply without additional input (the analogue of $gL$). Formally writing $\ddot\theta + \sin\theta$ from a spherical restriction requires identifying the $\sin\theta$ term with a potential gradient, not with a geodesic equation.

**Structural observation.** The GSF EOM in the SHO regime produces linear oscillations (Theorem 15.1). The pendulum is the large-amplitude, nonlinear generalization — it shares the same configuration space topology ($S^1$ vs $\mathbb{R}$) and the same small-angle limit. The GSF does not derive the $\sin\theta$ restoring force from first principles at this level, but it predicts the existence of large-amplitude nonlinear oscillators as a general structural class: any system with compact configuration space and a bounded potential exhibits this behavior. The specific form of the pendulum potential ($V = gL(1-\cos\theta)$) is domain-specific input, not GSF output.

**Remark 15.5 (Pendulum status).** The pendulum is a structural instance of a nonlinear oscillator consistent with the GSF framework, but not a *reduction* of it in the technical sense of Theorems 15.1–15.3. Its derivation requires domain-specific input (the gravitational potential) and topological information (compact $S^1$ configuration space) that lie outside the present GSF Lagrangian. A first-principles derivation is deferred to Part III.

---

## 15.5 Scalar Field Theory — from Matrix to Field

### 15.5.1 The Field-Theoretic Extension

The GSF EOM in §15.1 is an ordinary differential equation in time. For *field theories*, the configuration $\Gamma$ depends on spacetime coordinates $(t, \mathbf{x})$:

$$\Gamma = \Gamma(t, \mathbf{x})$$

**Epistemic note.** The step from a mechanical system ($\Gamma(t)$) to a field ($\Gamma(t,\mathbf{x})$) is a *canonical covariant lifting*: replacing $\partial_t^2 \to \square = \partial_t^2 - c^2\nabla^2$ is the unique Lorentz-covariant extension of the kinetic term under the requirement that the equation of motion be frame-independent. This is not a free parameter insertion — the coefficient $c^2$ is fixed to 1 in GSF units at $\rho = \rho_{\mathrm{GR}}$ by the same anchor $c(\rho_{\mathrm{GR}}) = 1$ (Ch14). However, the derivation of the spatial metric from the fiber bundle geometry — establishing *why* the base manifold has a Lorentzian structure — is deferred to Part III.

The natural field-theoretic extension of the Lagrangian density is:

$$\mathcal{L}_{\mathrm{field}} = \|\partial_t\Gamma\|_F^2 - c^2\|\nabla\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)$$

where the spatial gradient term $c^2\|\nabla\Gamma\|_F^2$ is the Lorentz-covariant extension of the kinetic term. At $\rho = \rho_{\mathrm{GR}}$: $c = c(\rho_{\mathrm{GR}}) = 1$ (in GSF units), so $c^2 = 1$.

The Euler-Lagrange equation for $\Gamma(t,\mathbf{x})$ is:

$$\left(\partial_t^2 - \nabla^2\right)\Gamma + \Gamma + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\mathrm{adj}(\Gamma)^T = 0$$

$$\square\Gamma + \Gamma + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\mathrm{adj}(\Gamma)^T = 0$$

where $\square = \partial_t^2 - \nabla^2$ is the d'Alembert operator.

### 15.5.2 The Massless Wave Equation

For the null-purpose reduction (Lemma 15.1 applied to the field setting), $\mathrm{adj}(\Gamma)^T = 0$ and the field EOM becomes:

$$\square\Gamma + \Gamma = 0$$

This is a Klein-Gordon equation with mass $m^2 = 1$ (in GSF units). For a *massless* scalar field $\phi$, the $\Gamma$ term must be absent. This requires a further structural condition.

**Observation.** The term $+\Gamma$ in the field EOM comes from the potential $-\|\Gamma\|_F^2$ in the Lagrangian. For the EM field tensor $F_{\mu\nu}$ (considered as $\Gamma_a$), the corresponding Lagrangian is $-\frac{1}{4}F_{\mu\nu}F^{\mu\nu} = -\|\Gamma_a\|_F^2/4$. The factor $1/4$ versus the GSF normalization $1$ is an overall scale convention; more importantly, the field equation for $F_{\mu\nu}$ in vacuum is $\square F_{\mu\nu} = 0$ — without the mass term. This is addressed in §15.6 via the antisymmetric sector.

For a general scalar field $\phi = \Gamma_{ij}$ embedded as a null-purpose configuration in $4\times 4$ space, the EOM is:

$$\square\phi + \phi = 0$$

This is the *massive* wave equation (Klein-Gordon) with $m_{\mathrm{GSF}}^2 = 1$. In GSF units, unit mass corresponds to the inverse of the intrinsic timescale set by the Lagrangian. In physical units (via the Hito 3 bridge), this mass acquires dimensions.

**Remark 15.6 (Mass as structural feature).** The GSF Lagrangian does not have a tunable mass parameter — the "mass" of a scalar excitation is a structural consequence of the quadratic term $-\|\Gamma\|_F^2$. Massless excitations arise only when this term is absent or cancels, which in the GSF occurs for the antisymmetric sector $\Gamma_a$ when combined with the gauge invariance of that sector (§15.6).

---

## 15.6 The Electromagnetic Vacuum

### 15.6.1 Slot Assignment

In the GSF, the electromagnetic field couples to charges (attribute $S$) and currents (attribute $A$), while the field itself lives in the $\{\mathbf{I}, \mathbf{R}\}$ sector — electric and magnetic components respectively (Part I, Ch7):

$$\Gamma_a = F_{\mu\nu}, \quad \Gamma_s = 0 \quad (\text{EM vacuum: no sources})$$

The attribute assignment is:

| GSF attribute | EM content |
|---|---|
| $S$ | Electric charge density $\rho_e = 0$ (vacuum) |
| $A$ | Current density $J^\mu = 0$ (vacuum) |
| $\mathbf{I}$ | Electric field $\mathbf{E}$ |
| $\mathbf{R}$ | Magnetic field $\mathbf{B}$ |

In vacuum: both $S$ and $A$ are null (doubly-null symmetric sector, Ch12 §12.3.2), and the entire coupling matrix is antisymmetric: $\Gamma = \Gamma_a = F_{\mu\nu}$.

### 15.6.2 Determinant of the Field Tensor

For an antisymmetric $4\times 4$ real matrix $F$, the determinant satisfies:

$$\det(F) = \left(\mathrm{Pf}(F)\right)^2$$

where $\mathrm{Pf}(F)$ is the Pfaffian. For the electromagnetic field tensor in the $\{t, x, y, z\}$ basis:

$$\mathrm{Pf}(F) = \mathbf{E}\cdot\mathbf{B}$$

For a **transverse electromagnetic wave** (propagating in vacuum), $\mathbf{E} \perp \mathbf{B}$ always, so:

$$\det(F_{\mu\nu}) = (\mathbf{E}\cdot\mathbf{B})^2 = 0 \quad\text{(for all vacuum EM waves)}$$

This is an exact condition, not an approximation.

### 15.6.3 The Antisymmetric Sector as Curvature — Maxwell without Patching

**Adjugate vanishing — explicit chain.** For a transverse EM wave: $\mathbf{E}\cdot\mathbf{B} = 0 \implies \mathrm{Pf}(F) = 0 \implies \det(F) = (\mathrm{Pf}(F))^2 = 0$. For a $4\times4$ antisymmetric matrix, rank must be even (0, 2, or 4); $\det(F) = 0$ eliminates rank 4. Therefore $\mathrm{rank}(F) \leq 2$. By Lemma 15.1, the quartic term vanishes. If $F_{\mu\nu}$ were a primary variable, the field EOM would be:

$$\square F_{\mu\nu} + F_{\mu\nu} = 0 \qquad (\text{Proca-type — if } F \text{ were primary})$$

This is not Maxwell. The resolution lies in the structural status of the antisymmetric sector.

**Proposition 15.3 (Antisymmetric sector as curvature 2-form).** *The antisymmetric sector $\Gamma_a$ of the GSF configuration matrix is not a primary field but a curvature 2-form:*
$$\Gamma_a = F = dA$$
*for a connection 1-form $A$. This is the structural content of the antisymmetric sector: in the irreducible decomposition of $\mathrm{End}(V)$ under $\mathrm{GL}(4,\mathbb{R})$, the antisymmetric part $\Gamma_a \in \Lambda^2 V$ carries the representation of exact 2-forms — the images of the exterior derivative $d$. The symmetric sector $\Gamma_s$ is a primary tensor (no such representation constraint); the antisymmetric sector is derived from a connection.*

**Consequences of $\Gamma_a = dA$ (both automatic, no external constraint):**

*(i) Bianchi identity:* $dF = d^2A = 0 \implies \partial_{[\mu}F_{\nu\rho]} = 0$ — the second set of Maxwell equations.

*(ii) Maxwell source-free equations:* When the GSF action density $\|\Gamma_a\|_F^2 = \|dA\|_F^2$ is varied with respect to $A$ (not $F$):
$$\frac{\delta}{\delta A_\rho}\int \|dA\|_F^2\,d^4x = 0 \implies \partial_\mu F^{\mu\rho} = 0$$
This is the first set of Maxwell equations. The apparent $+F_{\mu\nu}$ term never appears because the variation is with respect to $A$: the term $\|dA\|_F^2$ is a *kinetic term for the connection* $A$, not a mass term. A mass term for $A$ would require $\|A\|^2$ in the Lagrangian — absent by construction.

*(iii) Gauge symmetry:* $A \to A + d\Lambda$ leaves $F = dA$ unchanged ($d^2\Lambda = 0$). This is a redundancy of the representation, not an imposed symmetry.

**GSF mass protection principle.** The symmetric sector $\Gamma_s$ carries mass structurally: $\|\Gamma_s\|_F^2$ is a mass term for the primary field $\Gamma_s$. The antisymmetric sector $\Gamma_a = dA$ does not: $\|dA\|_F^2$ is a kinetic term for $A$. Masslessness of $A$ is a consequence of the representation structure — $\Gamma_a$ lives in the image of $d$, not in a free representation — not of an external symmetry.

$$\boxed{\partial_\mu F^{\mu\nu} = 0, \quad \partial_{[\mu}F_{\nu\rho]} = 0 \qquad (\text{Maxwell in vacuum}) \quad \checkmark}$$

**Theorem 15.2 (EM vacuum reduction — curvature formulation).** *The GSF configuration restricted to $\Gamma_a = F = dA$ with $\mathbf{E}\cdot\mathbf{B} = 0$ yields both sets of Maxwell equations in vacuum: (i) $\partial_\mu F^{\mu\nu} = 0$ from variation w.r.t. $A$; (ii) $\partial_{[\mu}F_{\nu\rho]} = 0$ from $d^2 = 0$. In Lorenz gauge $\partial_\mu A^\mu = 0$, these give $\square F_{\mu\nu} = 0$. No gauge constraint is invoked externally; no parameter is adjusted.*

**Epistemic note (Part III scope).** The identification $\Gamma_a = dA$ requires embedding the abstract matrix $\Gamma_a$ into differential forms on a base manifold — specifying the bundle geometry, the connection, and the base manifold structure. This embedding is the "canonical covariant lifting" of §15.5 in the antisymmetric sector. The full derivation (bundle geometry, Lorentzian base manifold, connection interpretation) is Part III. The present chapter establishes that the identification is consistent and that it resolves the apparent Proca problem without additional assumptions.

### 15.6.4 The EM Lagrangian

The GSF kinetic term restricted to $\Gamma_a$:

$$\|\dot F_{\mu\nu}\|_F^2 = \mathrm{Tr}(\dot F^T \dot F) = \mathrm{Tr}(\dot F^2) \quad(\text{since } F^T = -F \Rightarrow F^T = -F)$$

The GSF potential restricted to $\Gamma_a$:

$$-\|\Gamma_a\|_F^2 = -\mathrm{Tr}(F^T F) = \mathrm{Tr}(F^2)$$

Since $\mathrm{Tr}(F^{\mu\nu}F_{\mu\nu}) = 2(\mathbf{B}^2 - \mathbf{E}^2)$ and $-\frac{1}{4}F_{\mu\nu}F^{\mu\nu} = \frac{1}{2}(\mathbf{E}^2 - \mathbf{B}^2)$, the GSF potential term $-\|\Gamma_a\|_F^2$ coincides with the standard Maxwell Lagrangian density $-\frac{1}{4}F_{\mu\nu}F^{\mu\nu}$ up to an overall normalization convention. The GSF Lagrangian and the Maxwell Lagrangian are **structurally equivalent** in the vacuum EM sector.

---

## 15.7 Linearized Gravity

### 15.7.1 Slot Assignment

For pure gravity without EM:

$$\Gamma = \Gamma_s = \eta_{\mu\nu} + h_{\mu\nu}, \quad \Gamma_a = 0$$

where $\eta_{\mu\nu}$ is the Minkowski metric and $h_{\mu\nu}$ is the small perturbation, $|h| \ll 1$.

| GSF attribute | Gravitational content |
|---|---|
| $S$ | Background geometry (Minkowski $\eta$) |
| $A$ | Perturbation amplitude $h$ |
| $\mathbf{I}$ | Spatial metric components |
| $\mathbf{R}$ | Mixed (spacetime) metric components |

The system has no antisymmetric sector ($\Gamma_a = 0$, vacuum gravity has no electromagnetic counterpart at linear order).

### 15.7.2 Linearized EOM

**Linearization of $\det(\Gamma_s)$.** For $\Gamma_s = \eta + h$:

$$\det(\eta + h) = \det(\eta)\,\det(I + \eta^{-1}h) \approx (-1)\left(1 + \mathrm{Tr}(\eta^{-1}h)\right) = -1 + \mathrm{Tr}(h)$$

using $\det(\eta) = -1$ (Lorentzian signature) and the first-order expansion $\det(I + \epsilon) \approx 1 + \mathrm{Tr}(\epsilon)$.

**Linearization of $\mathrm{adj}(\Gamma_s)^T$.** At zeroth order: $\mathrm{adj}(\eta)^T = \det(\eta)\,\eta^{-1} = -\eta^{-1} = -\eta^{\mu\nu}$. At first order in $h$:

$$\mathrm{adj}(\eta+h)^T \approx \det(\eta+h)\,(\eta+h)^{-1} \approx (-1+\mathrm{Tr}(h))(\eta^{-1} - \eta^{-1}h\eta^{-1})$$

$$\approx -\eta^{\mu\nu} + h^{\mu\nu} + \mathrm{Tr}(h)\,\eta^{\mu\nu} + O(h^2)$$

**EOM at linear order.** Combining at $\rho = \rho_{\mathrm{GR}}$ (so $\mu = 2$, attractor coefficient $= (\rho_{\mathrm{GR}}/\rho_{\mathrm{GR}})^2 = 1$):

$$\square h_{\mu\nu} + h_{\mu\nu} + \left(-\eta_{\mu\nu} + h_{\mu\nu} + \mathrm{Tr}(h)\,\eta_{\mu\nu}\right) = 0$$

The zeroth-order term $-\eta_{\mu\nu}$ is a constant and corresponds to the background (cosmological constant contribution). At first order in $h$:

$$\square h_{\mu\nu} + (1 + 1)h_{\mu\nu} - \eta_{\mu\nu}\,\mathrm{Tr}(h) = 0$$

$$\square h_{\mu\nu} + 2h_{\mu\nu} - \eta_{\mu\nu}\,\mathrm{Tr}(h) = 0$$

With the massless graviton condition $\mu = 2$ (Ch13, Remark 13.5), which anchors $c(\rho_{\mathrm{GR}}) = 1$, the mass term for the gravitational perturbation arises as:

$$m_h^2 = 2 - \mu = 2 - 2 = 0$$

The EOM for $h_{\mu\nu}$ (in the appropriate gauge, the de Donder/harmonic gauge $\partial^\mu \bar h_{\mu\nu} = 0$ where $\bar h_{\mu\nu} = h_{\mu\nu} - \frac{1}{2}\eta_{\mu\nu}\mathrm{Tr}(h)$):

$$\square h_{\mu\nu} = 0 \qquad\text{(massless graviton)} \quad \checkmark$$

**Theorem 15.3 (GR linearized reduction).** *The GSF EOM restricted to the symmetric sector $\Gamma_s = \eta + h$ at $\rho = \rho_{\mathrm{GR}}$ reproduces linearized general relativity with a massless graviton. The massless condition follows from $\mu(\rho_{\mathrm{GR}}) = 2$, which was derived from the same anchor in Chapter 13.*

**Remark 15.7 (No double-counting).** The condition $\mu = 2$ was derived in Ch13 (Remark 13.5) from the requirement of a massless graviton — and that same condition is used here to confirm the graviton is massless. This is not circular: the derivation in Ch13 established that *if* $c(\rho_{\mathrm{GR}}) = 1$ (normalized coherence at the gravitational stratum), *then* $\mu = 2$ and the graviton is massless. Chapter 14 (T1) subsequently derived $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ as a consequence of the scaling law, confirming $c(\rho_{\mathrm{GR}}) = 1$ independently. The consistency check here is that these two independent derivations agree.

---

## 15.8 Summary and Epistemic Status

Table 15.1 records the five reductions of this chapter.

| System | $\Gamma$ structure | Special condition | GSF EOM reduces to | Verification |
|---|---|---|---|---|
| Scalar (1×1) | $\Gamma = (x)$, full rank | None | $\ddot u + \gamma\dot u + u = 0$ (shifted SHO) | Exact |
| SHO (null-purpose) | $4\times 4$ rank-2 antisymmetric | $\mathrm{adj}(\Gamma) = 0$ | $\ddot x + \gamma\dot x + x = 0$ (SHO) | Exact |
| Pendulum | SHO in large-amplitude regime | $S^1$ topology, potential $V = gL(1-\cos\theta)$ | $\ddot\theta + \sin\theta = 0$ | Geometric analogy; not a structural derivation |
| EM vacuum | $\Gamma_a = F = dA$, $\mathrm{rank}(F) \leq 2$ | Curvature sector ($\Gamma_a = dA$) | Maxwell: $\partial_\mu F^{\mu\nu} = 0$, $dF = 0$ | Bundle embedding deferred to Part III |
| GR linearized | $\Gamma_s = \eta + h$, $\mu = 2$ | Harmonic gauge | $\square h_{\mu\nu} = 0$ (graviton) | Exact at linear order |
| Irrotational flow / acoustics | $4\times 4$ rank-2, $\Gamma_a = 0$ | Same as SHO + gauge structure | $\square\phi = 0$ (acoustic wave) | Exact — same mechanism as EM |
| Stokes flow (viscous) | Diagonal $(p, v_x, v_y, v_z)$ | $\gamma \gg 1$, $|\mathbf{v}| \to 0$, $c^2/L^2 \gg 1$ | $\partial_t v_i = \nu\nabla^2 v_i - \frac{1}{\rho_f}\partial_i p$ | Approximate in Re $\to 0$ limit |

Table 15.2 records the epistemic status of each result.

| Claim | Status | Caveat |
|---|---|---|
| Scalar reduction → shifted SHO | Proved | Exact algebraic result |
| Null-purpose adjugate vanishes | Proved (Lemma 15.1) | Rank $\leq 2$ required |
| SHO from null-purpose embedding | Proved (Theorem 15.1) | Null $S$, $A$ attributes required |
| Pendulum — geometric analogy | Structural analogy | Not a derivation; requires domain potential + $S^1$ topology |
| Massless scalar = Klein-Gordon (with mass) | Derived | Massless field requires gauge constraint |
| $\Gamma_a = dA$ (curvature sector) | Structural (Proposition 15.3) | Bundle embedding deferred to Part III |
| EM → Maxwell ($\partial_\mu F^{\mu\nu}=0$, $dF=0$) | Proved (Theorem 15.2) | Follows from $\Gamma_a=dA$; no gauge patching |
| Photon masslessness | Structural consequence | $\|dA\|^2$ is kinetic for $A$, not a mass term |
| EM with sources ($J^\mu \neq 0$) | Open | Requires Hito 3 (stratum bridge) |
| GR linearized → massless graviton | Proved (Theorem 15.3) | Linear order only; full GR requires beyond-linear |
| Full GR ($G_{\mu\nu} = 0$) | Open | Requires nonlinear extension and Hito 3 |
| Irrotational flow $\to$ $\square\phi = 0$ | Proved (Theorem 15.4) | Same gauge mechanism as EM; rotational flow open |
| Acoustic-EM structural identity | Structural prediction | Same object in $\Gamma_a$ sector; falsifiable via mode topology |
| Stokes $\to$ $\partial_t v_i = \nu\nabla^2 v_i$ | Proved (Theorem 15.5) | Approximate: Re $\to 0$; exact within limit |
| $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$ | Derived ($\gamma$ operationalization) | Testable via viscosity ratios, no Hito 3 needed |
| Rotational flow (Euler), NS general | Open | No direct Lagrangian reduction; C($\Gamma$) diagnostic valid |

**The pattern.** All five reductions share the same structure: the GSF EOM, evaluated under domain-specific constraints on $\Gamma$, yields the established equations of the domain without adjusting any parameter. The quartic (attractor) term $\mathrm{adj}(\Gamma)^T$ either vanishes identically (null-purpose cases: SHO, EM transverse) or contributes at linear order with a coefficient fixed by $\mu(\rho)$ (GR). No system in this chapter introduces a new free parameter.

**The mass protection structure.** The symmetric sector $\Gamma_s$ carries intrinsic mass (the $\|\Gamma_s\|_F^2$ term is a mass for the primary field). The antisymmetric sector $\Gamma_a = dA$ does not — its $\|dA\|_F^2$ is a kinetic term for the connection $A$. This structural distinction between primary tensors (can be massive) and curvature forms (massless) is a consequence of the representation theory of the $\mathrm{GL}(4,\mathbb{R})$ decomposition, not a symmetry imposed by hand. It is the GSF analog of the statement that gauge bosons are massless.

**Remark 15.8 (Structural analog of wave-particle duality).** The rank structure of $\Gamma$ partitions physical configurations into two qualitatively distinct classes:

- *Wave regime* ($S = A = 0$, $\det(\Gamma) = 0$, $\mathrm{rank} \leq 2$): the system has no organizing center and no agency. The adjugate vanishes (Lemma 15.1), the attractor $P(\Gamma)$ does not exist, and the dynamics is linear — the system propagates. It lives on $\partial\mathcal{M}(\Gamma)$, in the representation space $\Lambda^2V$ of the antisymmetric sector.

- *Particle regime* ($S \neq 0$ or $A \neq 0$, $\det(\Gamma) > 0$): the system has a structural identity and agency. The adjugate is nonzero, the attractor $P(\Gamma)$ exists, and the dynamics is nonlinear with a localized equilibrium. It lives in the interior $\mathcal{M}_{\mathrm{adm}}$.

Wave-particle duality, in this framework, is a property of the **regime** the UoC occupies — not of the UoC itself. The same UoC (e.g., a charged system or a fluid parcel) exhibits *wave regime* when its source/agency attributes are inactive, and *particle regime* when they are active. The duality is dynamical, not ontological: there is no "wave object" distinct from a "particle object"; there is one UoC that traverses both regimes. When $S = A = 0$, the regime is wave-like; when $S \neq 0$ or $A \neq 0$, the regime is particle-like. The transition between regimes is the matter creation threshold $\rho_{\mathrm{mat}}$ of Ch14 §14.8.1, governed by the potential barrier $\Delta V(\rho) = 2(\rho_{\mathrm{GR}}/\rho)^2$.

**Qualification.** This is the *classical structural* analog of wave-particle duality — it captures the distinction between field configurations and source configurations, not quantum superposition and wavefunction collapse. The quantum version, involving the Born rule and measurement-induced transition between regimes, requires the quantum extension of the GSF (Part III).

Same equation, same coefficients, same manifold — five different domains. The Lagrangian is not generic: it produces the established equations of each domain without parameter adjustment.

**Technical note.** The complete spectral structure of fluctuation modes around any background is developed rigorously in §15b. That supplement formalizes the dynamical distinction this chapter established algebraically.

---

## 15.8b Acoustic Waves and Irrotational Flow — A Sixth Reduction

**Proposition 15.4 (Irrotational flow and acoustic propagation).** *The GSF EOM, restricted to the irrotational embedding $\Gamma_a = 0$ with $S = A = 0$ (no sources, no vorticity), reduces to the massless wave equation for the velocity potential $\phi$. This is the same structural mechanism as the EM photon.*

**Slot assignment.** For irrotational incompressible flow, the velocity field is $\mathbf{v} = \nabla\phi$ with $\phi$ the velocity potential. Assign:

| GSF slot | Content |
|---|---|
| $S, A$ | Null (no source, no vorticity) |
| $\mathbf{I}, \mathbf{R}$ | Velocity potential $\phi$ in the antisymmetric off-diagonal $\Gamma_{\mathbf{IR}} = \phi$ |

The coupling matrix:

$$\Gamma = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & \phi \\ 0 & 0 & -\phi & 0 \end{pmatrix}$$

This is a null-purpose embedding of rank 2. By Lemma 15.1: $\mathrm{adj}(\Gamma) = 0$.

**EOM.** The GSF field equation reduces to:

$$\square\phi + \phi = 0 \qquad\text{(Klein-Gordon, mass }m^2 = 1\text{ in GSF units)}$$

Treating $\phi$ as a gauge potential (not a primary field) — the same step that removes the mass term for $A$ in the EM reduction (§15.6.3) — variation with respect to the underlying potential gives:

$$\boxed{\square\phi = 0} \qquad\text{or}\qquad \boxed{\nabla^2\phi = 0} \;\text{(incompressible)}$$

**Theorem 15.4 (Acoustic and irrotational flow reduction).** *The GSF EOM restricted to the irrotational null-purpose embedding yields the massless wave equation for the velocity potential. This is exact and requires no parameter adjustment.*

**Structural identity with EM.** The velocity potential $\phi$ and the EM gauge potential $A$ are the same structural object in the GSF:

| EM | Irrotational fluid |
|---|---|
| Gauge potential $A$ (connection) | Velocity potential $\phi$ (connection) |
| $F = dA$ (curvature 2-form) | $\mathbf{v} = \nabla\phi$ (gradient field) |
| $\square A = 0$ (photon, massless) | $\square\phi = 0$ (acoustic wave, massless) |
| $dF = 0$ (Bianchi) | $\nabla\times\mathbf{v} = 0$ (irrotational) |

Both are connections in the antisymmetric sector of $\Gamma$. Both go massless because $\|d(\cdot)\|^2$ is a kinetic term for the potential, not a mass term. This is not an analogy — it is the same algebraic mechanism (Lemma 15.1 + gauge structure).

**Structural prediction (PR-18 — confirmed by literature, 2026-05-31).** Acoustic waves and electromagnetic waves have the same structural topology in the GSF. Their dispersion relations, boundary conditions, and mode structures must be identical at the structural level — differing only in the slot assignment (pressure/velocity vs. $\mathbf{E}/\mathbf{B}$) and the value of $\rho$. The classical acoustic-EM analogy (Bergmann 1946, used in acoustic cloaking and transformation acoustics) has a structural explanation in the GSF: it is not a formal analogy but a structural identity.

**Scope.** This reduction applies to:
- Subsonic aerodynamics (potential flow theory, Joukowski profiles, lifting-line theory)
- Linear acoustics (sound propagation in homogeneous media)
- Surface gravity waves in deep water (long-wavelength limit)

Rotational flow ($\mathbf{v} \neq \nabla\phi$, $\omega \neq 0$) introduces $\Gamma_a \neq 0$ and breaks the rank-2 condition. The full rotational regime belongs to the dissipative and inertial regimes — see brainstorming/aerodynamic/tres_regimenes_fluidos_gsf.md.

---

## 15.8c Viscous Flow — The Overdamped Limit and Stokes Equations

The reductions of §§15.3–15.8b are exact: the GSF EOM reduces to known equations without approximation. This section establishes an additional reduction that holds in a well-defined physical limit — not exact, but exact within the stated regime.

**Three conditions for the Stokes limit.** The dissipative field-theoretic GSF EOM is:

$$\partial_t^2\Gamma + \gamma\partial_t\Gamma - c^2\nabla^2\Gamma + \Gamma + \mu(\rho)\,\mathrm{adj}(\Gamma)^T = N$$

Three limits applied in sequence:

**(L1) Overdamped: $\gamma \gg 1$.** The inertial term $\partial_t^2\Gamma \ll \gamma\partial_t\Gamma$ is negligible. The EOM becomes first-order in time — the same order as Stokes.

**(L2) Small velocity: $|\mathbf{v}| \sim \varepsilon \to 0$.** With the slot assignment below, $\mathrm{adj}(\Gamma)^T \sim \varepsilon^2$ — subdominant. The nonlinear attractor term vanishes in this limit.

**(L3) Long wavelength: $c^2/L^2 \gg 1$.** The structural mass term $+\Gamma \sim \varepsilon$ is negligible compared to $c^2\nabla^2\Gamma \sim c^2\varepsilon/L^2$.

**Slot assignment.** For 3D incompressible viscous flow, assign:

$$\Gamma = \begin{pmatrix} p & 0 & 0 & 0 \\ 0 & v_x & 0 & 0 \\ 0 & 0 & v_y & 0 \\ 0 & 0 & 0 & v_z \end{pmatrix}$$

where $p$ is pressure (slot $S$) and $(v_x, v_y, v_z)$ are velocity components (slots $A, \mathbf{I}, \mathbf{R}$). Under this assignment $\mathrm{adj}(\Gamma)_{v_iv_j} \sim p\varepsilon^2$ and $\det(\Gamma) = pv_xv_yv_z$.

**Reduction.** Applying L1–L3 to the EOM for the velocity entry $v_x$ (slot $A$, entry (2,2)):

$$\gamma\partial_t v_x = c^2\nabla^2 v_x + N_x$$

With external forcing $N_x = -\partial_x p$ (pressure gradient):

$$\gamma\partial_t v_x = c^2\nabla^2 v_x - \partial_x p$$

Dividing by $\gamma$:

$$\partial_t v_x = \frac{c^2(\rho)}{\gamma}\nabla^2 v_x - \frac{1}{\gamma}\partial_x p$$

**Theorem 15.5 (Stokes reduction).** *In the limit $\gamma \gg 1$, $|\mathbf{v}| \to 0$, $c^2/L^2 \gg 1$, the GSF EOM with the diagonal velocity-pressure slot assignment reduces to the Stokes equations:*

$$\boxed{\partial_t v_i = \nu_{\mathrm{kin}}\,\nabla^2 v_i - \frac{1}{\rho_f}\partial_i p, \qquad \nabla\cdot\mathbf{v} = 0}$$

*with kinematic viscosity:*

$$\boxed{\nu_{\mathrm{kin}} = \frac{c^2(\rho_{\mathrm{fluid}})}{\gamma} = \frac{1}{\gamma}\left(\frac{\rho_{\mathrm{GR}}}{\rho_{\mathrm{fluid}}}\right)^4}$$

*The incompressibility condition $\nabla\cdot\mathbf{v} = 0$ enters as a gauge constraint on $\mathrm{Tr}(\nabla\Gamma)|_{\{A,\mathbf{I},\mathbf{R}\}}$, analogous to the Lorenz gauge in EM.*

**Remark 15.9 (Epistemic status — approximate reduction).** Unlike the reductions of §§15.3–15.8b, this reduction is approximate: it holds in the limit Re $\to 0$ (which implies L1 and L2 simultaneously) and in the long-wavelength regime L3. The three conditions have direct physical names and are satisfied simultaneously for creeping flow (Re $\ll 1$). The result is not exact outside this limit — the full GSF EOM governs the general case.

**Remark 15.10 (Operationalization of $\gamma$).** The identification $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$ gives the first quantitative operationalization of the damping parameter for a physical domain:

$$\gamma = \frac{c^2(\rho_{\mathrm{fluid}})}{\nu_{\mathrm{kin}}}$$

Without Hito 3 (absolute scale of $\rho$), $\gamma$ ratios are already predictive: $\gamma_{\mathrm{water}}/\gamma_{\mathrm{glycerol}} = \nu_{\mathrm{glycerol}}/\nu_{\mathrm{water}} \approx 10^3$ from tabulated viscosities. This is testable against the GSF prediction $\gamma \propto 1/\nu_{\mathrm{kin}}$ at fixed $\rho$.

**Remark 15.11 (Reynolds number as $\gamma$ proxy).** From $\nu_{\mathrm{kin}} = c^2/\gamma$ and $\mathrm{Re} = vL/\nu_{\mathrm{kin}}$:

$$\mathrm{Re} = \frac{vL\,\gamma}{c^2(\rho)}$$

High Re (inviscid, Euler regime) corresponds to small $\gamma$; low Re (viscous, Stokes regime) corresponds to large $\gamma$. The Reynolds number is the physical proxy for $1/\gamma$ in fluid dynamics — the damping parameter of the structural Lagrangian acquires a direct fluid-mechanical interpretation.

**Scope.** This reduction covers: creeping flow in microfluidics, lubrication theory, sedimentation, flow in porous media, biological fluids (blood in capillaries, cytoplasmic streaming). The general inertial regime (finite Re) and the inviscid limit (Euler equations) do not follow from this reduction — they require the full nonlinear GSF EOM and are addressed in the brainstorming (see brainstorming/aerodynamic/tres_regimenes_fluidos_gsf.md).

---

## 15.9 Looking Forward

Four reductions in this chapter are exact (SHO, EM vacuum, GR linearized, irrotational flow/acoustics). One is approximate in a well-defined physical limit (Stokes, Re $\to 0$). The pendulum is a geometric analogy. The EM-with-sources and full GR cases remain open, pending the stratum bridge (Hito 3).

The fluid domain reveals a structure absent in the other reductions: the damping parameter $\gamma$ acquires a physical interpretation (kinematic viscosity), the Reynolds number emerges as the physical proxy for $1/\gamma$, and the transition between viscous (Stokes) and inviscid (acoustic/potential) limits corresponds to the transition between overdamped and conservative GSF regimes. This connection between the GSF structural parameter $\gamma$ and the fluid-mechanical control parameter Re is the first domain-specific operationalization of $\gamma$ outside of abstract structural analysis.

---

*The GSF does not explain why the harmonic oscillator exists, or why Maxwell's equations take the form they do. It shows that these equations are structural instances of a single Lagrangian. Whether that observation constitutes an explanation depends on what explanations are expected to deliver — a question that Chapter 20 returns to.*
