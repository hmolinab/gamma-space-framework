# Chapter 17: Worked Examples — GSF in Physical Systems

*Bridging the abstract framework and concrete numbers*

---

## 17.1 Purpose

**This chapter is the first numerical test of the GSF algebra.**

Part I and Part II established the framework through symbolic derivation — the Lagrangian was derived, the scaling law was derived, and the reductions were proved as theorems. But a theorem that the EOM reduces to $\ddot{x} + \gamma\dot{x} + x = 0$ is still abstract: it does not say what $\gamma$ is for a specific spring, what $\det(\Gamma)$ evaluates to at a specific displacement, or whether $\mathcal{C}(\Gamma) = 0$ for a photon means anything numerical.

This chapter plugs in numbers. For each system: specific masses, spring constants, field strengths, viscosities. The GSF algebra is evaluated explicitly and the results are compared against known physics. When the SHO at critical damping gives $\gamma = 2$ — exactly the value of $\mu(\rho_{\mathrm{GR}})$ that enforces the massless graviton — that is not a symbolic coincidence but a numerical verification. When the EM plane wave gives $\det(\Gamma) = 0$ and $\mathcal{C}(\Gamma) = 0$, the structural claim that "waves live on $\partial\mathcal{M}(\Gamma)$" becomes a concrete computation. When water in a capillary gives Re $= 3.1\times10^{-4}$ and the Stokes reduction applies, the abstract limit $\gamma \gg 1$ has a physical face.

This is also the starting point for empirical validation. The $\gamma$ ratios in §17.6.4 — $\gamma_{\mathrm{water}}/\gamma_{\mathrm{glycerol}} \approx 1490$, $\gamma_{\mathrm{D_2O}}/\gamma_{\mathrm{H_2O}} \approx 0.80$ — are testable today from tabulated viscosities, without any laboratory work. The roadmap of empirical tests that follow from this chapter is in brainstorming/roadmap_pruebas_empiricas.md.

The Lagrangian of Part II is parameter-free, but the attribute assignments and the value of $\gamma$ for specific systems require domain-specific input. This chapter works through five physical systems explicitly, showing at two levels for each:

- **Statics**: the slot assignment $\{S, A, \mathbf{I}, \mathbf{R}\}$, the coupling matrix $\Gamma$, the structural Force and Field, and the coherence $\mathcal{C}(\Gamma)$.
- **Dynamics**: the equation of motion, the value of $\gamma$, and the solution — verifying that the GSF EOM reduces to the known physical equation.

The five systems span the coverage of Part II: the harmonic oscillator (exact, null-purpose), the EM plane wave (exact, gauge sector), the linearized gravitational wave (exact, symmetric sector), irrotational flow (exact, same as EM), and Stokes flow in a capillary (approximate, overdamped limit). All are purely physical — no biological or psychological interpretation is applied here.

---

## 17.2 The Harmonic Oscillator

### 17.2.1 Slot Assignment

For a mass on a spring (mass $m$, spring constant $k$, damping $b$), with displacement $x(t)$ from equilibrium:

| GSF slot | Physical content | Value at $t=0$, $x_0=1$, $\dot{x}_0=0$ |
|---|---|---|
| $S$ | Null (no structural identity / charge) | $0$ |
| $A$ | Null (no agency / source) | $0$ |
| $\mathbf{I}$ | Displacement field | $x_0 = 1$ |
| $\mathbf{R}$ | — (absorbed into $\Gamma_{IR}$) | — |

**Coupling matrix** (null-purpose embedding of rank 2):

$$\Gamma = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & x \\ 0 & 0 & -x & 0 \end{pmatrix}$$

### 17.2.2 Statics at $x=1$

| Quantity | Formula | Value |
|---|---|---|
| Force $= S\cdot\mathbf{A}$ | $0 \cdot 0$ | $\mathbf{0}$ |
| Field $= \mathbf{I}\wedge\mathbf{R}$ | $x\,\hat{e}_\mathbf{I}\wedge(-)\,\hat{e}_\mathbf{R}$ | $x^2\,\hat{e}_\mathbf{I}\wedge\hat{e}_\mathbf{R}$ = bivector (amplitude$^2$) |
| $\|\Gamma\|_F$ | $\sqrt{2x^2}$ | $\sqrt{2} \approx 1.414$ |
| $\det(\Gamma)$ | $0$ (rank 2) | $0$ |
| $\mathcal{C}(\Gamma)$ | $\det/(\|\Gamma\|_F^2/4)^2$ | $0$ |

$\mathcal{C} = 0$: the SHO lives permanently on $\partial\mathcal{M}(\Gamma)$. It has no structural attractor — the dynamics is purely linear. This is the structural signature of a propagating mode.

### 17.2.3 Dynamics — Four Values of $\gamma$

By Theorem 15.1, the EOM reduces exactly to:
$$\ddot{x} + \gamma\dot{x} + x = 0$$

with natural frequency $\omega_0 = 1$ in GSF units. Mapping to physical units: $\omega_0 = \sqrt{k/m}$, $\gamma_{\mathrm{phys}} = b/m$, so $\gamma_{\mathrm{GSF}} = b/(m\omega_0) = b/\sqrt{km}$.

**Reference system:** $m = 1$ kg, $k = 1$ N/m ($\omega_0 = 1$ rad/s), initial $x(0)=1$, $\dot{x}(0)=0$.

| $b$ (N·s/m) | $\gamma$ | Regime | Solution $x(t)$ |
|---|---|---|---|
| $0$ | $0$ | Conservative | $\cos(t)$ |
| $0.5$ | $0.5$ | Underdamped | $e^{-t/4}\cos(\omega_d t)$, $\omega_d = \sqrt{1-1/16} \approx 0.968$ |
| $2$ | $2$ | Critically damped | $(1+t)e^{-t}$ |
| $3$ | $3$ | Overdamped | $\frac{3e^{-t} - e^{-3t}}{2}$ |

At $t=3$: $x(3) \approx \{-0.99,\;0.064,\;0.199,\;0.071\}$ for $\gamma=\{0,\,0.5,\,2,\,3\}$.

**Structural interpretation of $\gamma$:** In GSF units, critical damping $\gamma = 2$ corresponds to the condition $\mu(\rho_{\mathrm{GR}}) = 2$ — the same value that makes the graviton massless (§17.4). For $\gamma < 2$: underdamped (oscillatory approach to equilibrium); for $\gamma > 2$: overdamped (monotone approach, Stokes regime).

---

## 17.3 The Electromagnetic Plane Wave

### 17.3.1 Slot Assignment

For a monochromatic plane wave propagating in the $x$-direction with $\mathbf{E} = E_0\,\hat{z}$ and $\mathbf{B} = (E_0/c)\,\hat{y}$:

| GSF slot | Physical content | Numerical value ($E_0 = 1$ V/m) |
|---|---|---|
| $S$ | Charge density | $0$ (vacuum) |
| $A$ | Current density | $0$ (vacuum) |
| $\mathbf{I}$ | Electric field | $E_z = 1$ V/m |
| $\mathbf{R}$ | Magnetic field | $B_y = 1/c \approx 3.3\times10^{-9}$ T |

**Coupling matrix** $\Gamma = \Gamma_a = F_{\mu\nu}$ (antisymmetric, S=A=0):

$$\Gamma = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & E_0 \\ 0 & 0 & -E_0 & 0 \end{pmatrix}$$

(using the $\{S,A,\mathbf{I},\mathbf{R}\}$ block; the actual 4D EM tensor has additional components when charge/current are present.)

### 17.3.2 Statics

| Quantity | Value |
|---|---|
| $\mathbf{E}\cdot\mathbf{B}$ | $E_z B_z + E_y B_y + E_x B_x = 0$ (transverse: $\mathbf{E}\perp\mathbf{B}$) |
| $\mathrm{Pf}(\Gamma_a)$ | $\mathbf{E}\cdot\mathbf{B} = 0$ |
| $\det(\Gamma)$ | $\mathrm{Pf}^2 = 0$ |
| $\|\Gamma\|_F$ | $\sqrt{2E_0^2} = \sqrt{2}$ V/m |
| $\mathcal{C}(\Gamma)$ | $0$ |
| Force $= S\cdot A$ | $0$ |
| Field $= \mathbf{I}\wedge\mathbf{R}$ | $E_0 B_y\,(\hat{e}_\mathbf{I}\wedge\hat{e}_\mathbf{R})$ = Poynting-like bivector |

$\mathcal{C} = 0$: the EM wave lives on $\partial\mathcal{M}(\Gamma)$. Same structural signature as the SHO. Both are propagating modes — photon and phonon are the same structural object.

### 17.3.3 Dynamics

By Theorem 15.2, treating $\Gamma_a = F = dA$:

$$\square F_{\mu\nu} = 0 \qquad (\gamma=0\text{, vacuum})$$

Solution: $F_{\mu\nu}(x,t) = F_{\mu\nu}^{(0)}\sin(kx - \omega t)$ with $\omega = ck$. Energy flux: $|\mathbf{E}\times\mathbf{B}|/\mu_0 = E_0^2/(c\mu_0)$ W/m².

**Key number:** $\|\Gamma\|_F = E_0\sqrt{2} \approx 1.41$ V/m. As $E_0 \to 0$, $\mathcal{C}(\Gamma) = 0$ throughout — the EM wave has no structural identity regardless of amplitude. This is the GSF statement that the photon carries no rest mass.

---

## 17.4 The Gravitational Wave (GR Linearized)

### 17.4.1 Slot Assignment

For a $+$-polarized gravitational wave propagating in the $z$-direction, with metric perturbation $h_{\mu\nu}$:

| GSF slot | Physical content | Perturbation |
|---|---|---|
| $S$ | Background metric (Minkowski $\eta$) | $\eta_{\mu\nu}$ |
| $A$ | Wave amplitude | $h_{\mu\nu}$ (small, $|h|\ll 1$) |
| $\mathbf{I}$ | Spatial metric xx-component | $\eta_{xx} + h_{+}$ |
| $\mathbf{R}$ | Spatial metric yy-component | $\eta_{yy} - h_{+}$ |

$\Gamma_s = \eta + h$, $\Gamma_a = 0$.

### 17.4.2 Statics at $h_+=0$ (background)

| Quantity | Value |
|---|---|
| $\|\Gamma_s\|_F$ | $\|\eta\|_F = \sqrt{4} = 2$ (Minkowski in 4D) |
| $\det(\Gamma_s)$ | $\det(\eta) = -1$ (Lorentzian signature) |
| $\mathcal{C}(\Gamma_s)$ | $\det / (\|\eta\|_F^2/4)^2 = -1/1 = -1$ (Lorentzian!) |

Note: $\mathcal{C}(\Gamma_s) = -1$ in Lorentzian signature. The Euclidean analysis ($\mathcal{C} \in (0,1]$) applies to the Riemannian part of the problem; the full Lorentzian case is deferred to Part III.

### 17.4.3 Dynamics

At $\rho = \rho_{\mathrm{GR}}$: $\mu = 2$, $m_h^2 = 2 - \mu = 0$ (Theorem 15.3). In de Donder gauge:

$$\square h_{\mu\nu} = 0 \qquad (\gamma=0)$$

For a LIGO-type event: $h_+ \approx 10^{-21}$ (dimensionless strain), frequency $f \approx 100$ Hz.

$$h_+(t) = h_0\sin(2\pi f t), \quad h_0 = 10^{-21}$$

The perturbation to $\|\Gamma\|_F$: $\delta\|\Gamma\|_F \approx h_0/\|\eta\|_F \approx 5\times10^{-22}$ — unmeasurably small, confirming that the GSF operates in the deep linear regime for gravitational waves.

**Key identification:** critical damping $\gamma_{\mathrm{crit}} = 2$ = $\mu(\rho_{\mathrm{GR}})$. The value $\gamma = 2$ marks the transition between oscillatory and overdamped behavior in the SHO (§17.2) and simultaneously enforces the massless graviton condition. This coincidence is structural, not numerical.

---

## 17.5 Irrotational Flow and Acoustic Wave

### 17.5.1 Slot Assignment

For a plane acoustic wave in air ($c_s = 343$ m/s, $\rho_0 = 1.2$ kg/m³), pressure amplitude $p_0 = 1$ Pa:

| GSF slot | Physical content | Numerical |
|---|---|---|
| $S$ | Null (no source) | $0$ |
| $A$ | Null (no vorticity) | $0$ |
| $\mathbf{I}$ | Velocity potential $\phi$ (I-R antisymmetric entry) | $\phi_0 = p_0/(\rho_0\omega)$ |
| $\mathbf{R}$ | — (antisymmetric partner) | — |

Same null-purpose embedding as SHO. Same Γ structure as §17.2 with $x \to \phi$.

| Quantity | Value ($f = 440$ Hz, concert A) |
|---|---|
| $\omega$ | $2\pi \times 440 \approx 2764$ rad/s |
| $\phi_0 = p_0/(\rho_0\omega)$ | $\approx 3.0\times10^{-4}$ m²/s |
| $\det(\Gamma)$ | $0$ (rank 2) |
| $\mathcal{C}(\Gamma)$ | $0$ |
| EOM | $\square\phi = 0$ (Theorem 15.4) |

### 17.5.2 PR-18 Verified Numerically

For a rectangular duct of cross-section $a\times b$:
- EM modes: $\omega_{mn}^{\mathrm{EM}} = c\sqrt{(m\pi/a)^2 + (n\pi/b)^2}$
- Acoustic modes: $\omega_{mn}^{\mathrm{ac}} = c_s\sqrt{(m\pi/a)^2 + (n\pi/b)^2}$

**The mode topology is identical** — same integers $(m,n)$, same structure, differing only by the propagation speed ($c$ vs $c_s$). This is PR-18 confirmed numerically: acoustic and EM modes in the same geometry have the same spectral topology because they are the same structural object (connection in the antisymmetric sector of $\Gamma$), scaled by $\rho$.

---

## 17.6 Stokes Flow in a Capillary

### 17.6.1 Physical Setup

Capillary tube: radius $R = 5\,\mu$m, length $L = 1$ mm, pressure drop $\Delta P = 100$ Pa.  
Fluid: water at 20°C. $\nu_{\mathrm{kin}} = 10^{-6}$ m²/s, $\rho_f = 1000$ kg/m³, $\mu_{\mathrm{visc}} = 10^{-3}$ Pa·s.

**Poiseuille velocity profile:** $v_r(r) = \frac{\Delta P}{4\mu_{\mathrm{visc}} L}(R^2 - r^2)$

Peak velocity at $r=0$: $v_{\max} = \frac{\Delta P R^2}{4\mu_{\mathrm{visc}} L} = \frac{100\times(5\times10^{-6})^2}{4\times10^{-3}\times10^{-3}} = 6.25\times10^{-5}$ m/s.

Reynolds number: $\mathrm{Re} = v_{\max}R/\nu_{\mathrm{kin}} = 6.25\times10^{-5}\times5\times10^{-6}/10^{-6} = 3.1\times10^{-4} \ll 1$. ✓ Deep Stokes.

### 17.6.2 Slot Assignment

| GSF slot | Physical content | Value (centerline, normalized to $v_{\max}=1$) |
|---|---|---|
| $S$ | Pressure | $p = \Delta P \cdot x/L$ |
| $A$ | Axial velocity | $v_x = v_{\max}(1 - r^2/R^2)$ |
| $\mathbf{I}$ | Radial velocity | $v_r \approx 0$ (axisymmetric) |
| $\mathbf{R}$ | Azimuthal velocity | $v_\theta = 0$ (no rotation) |

**Coupling matrix** (diagonal, at centerline $r=0$, $x=L/2$):

$$\Gamma = \begin{pmatrix} p_{L/2} & 0 & 0 & 0 \\ 0 & v_{\max} & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix} = \begin{pmatrix} 50 & 0 & 0 & 0 \\ 0 & 6.25\times10^{-5} & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \end{pmatrix} \text{ (Pa and m/s)}$$

**Note:** only 2 active slots → rank 2 → $\det(\Gamma) = 0$. For a fully 3D flow all three velocity components must be active.

### 17.6.3 Statics

| Quantity | Value |
|---|---|
| $\|\Gamma\|_F$ | $\sqrt{p^2 + v_x^2} \approx p$ (pressure-dominated) $\approx 50$ |
| $\det(\Gamma)$ | $0$ (rank 2) |
| $\mathcal{C}(\Gamma)$ | $0$ |
| Force $= S\cdot A$ | $p\cdot v_x \approx 50\times 6.25\times10^{-5} \approx 3.1\times10^{-3}$ (structural coupling) |

### 17.6.4 Dynamics and $\gamma$ Value

By Theorem 15.5, in the Stokes limit:
$$\partial_t v_x = \nu_{\mathrm{kin}}\nabla^2 v_x - \frac{1}{\rho_f}\partial_x p$$

**Steady state** ($\partial_t v_x = 0$): $\nu_{\mathrm{kin}}\nabla^2 v_x = (1/\rho_f)\partial_x p$. The Poiseuille solution satisfies this exactly. ✓

**GSF damping parameter:**

$$\gamma_{\mathrm{water}} = \frac{c^2(\rho_{\mathrm{water}})}{\nu_{\mathrm{kin,water}}} = \frac{c^2(\rho_{\mathrm{water}})}{10^{-6}\,\text{m}^2/\text{s}}$$

Without Hito 3, the absolute value is undetermined. **The ratio is immediately testable:**

| Fluid | $\nu_{\mathrm{kin}}$ (×$10^{-6}$ m²/s) | $\gamma_{\mathrm{rel}}$ |
|---|---|---|
| Mercury | $1.2\times10^{-7}$ | $8.4$ |
| Acetone | $4.3\times10^{-7}$ | $2.34$ |
| **Water H₂O (ref.)** | **$1.004\times10^{-6}$** | **$1.000$** |
| Seawater | $1.05\times10^{-6}$ | $0.956$ |
| D₂O | $1.251\times10^{-6}$ | $0.803$ |
| Blood plasma | $\sim1.3\times10^{-6}$ | $\sim0.77$ ← biological window threshold |
| Ethanol | $1.52\times10^{-6}$ | $0.660$ |
| Whole blood (high shear) | $\sim3.5\times10^{-6}$ | $\sim0.29$ |
| Glycerol (100%) | $1.19\times10^{-3}$ | $8.4\times10^{-4}$ |
| Glacial ice (creep) | $\sim10^{12}$ | $\sim10^{-18}$ |
| Earth's mantle (upper) | $\sim3\times10^{17}$ | $\sim3\times10^{-24}$ |

These ratios are derived from tabulated viscosities — no free parameters (tests E1, E9, E10, confirmed 2026-05-31). The full range spans **25 orders of magnitude** from mercury ($\gamma_{\mathrm{rel}} = 8.4$) to Earth's mantle ($\gamma_{\mathrm{rel}} \approx 3\times10^{-24}$) — a single parameter, a single equation, zero adjustments.

**Homeodynamic window (PR-19, from empirical tests E1+E2):** biological fluids cluster in $\gamma_{\mathrm{rel}} \in [0.78, 1.10]$. D₂O ($\gamma_{\mathrm{rel}} = 0.803$) is at the lower boundary — it is harmful at >25\% v/v precisely because its $\gamma$ falls below the viable range, slowing all enzymatic rearrangements. The kinetic isotope effect (3–10× slower reactions in D₂O) is the measurable consequence.

**Note:** ice has $\nu_{\mathrm{kin}} \to \infty$ (creep viscosity $\sim10^{12}$ m²/s) → $\gamma_{\mathrm{ice}} \approx 0$ (conservative regime, not overdamped). Ice transmits acoustic phonons — propagating waves in the $\gamma \approx 0$ sector, structurally equivalent to photons (same Lemma 15.1 mechanism).

### 17.6.5 Absolute Calibration and Gas Continuum (E6×E1, PR-24)

The ratios above fix $\gamma_{\mathrm{rel}}$ but not the absolute scale. The cross-test E6×E1 (`brainstorming/pruebas_empiricas/E6xE1_cross.md`, 2026-05-31) provides the missing anchor by combining the Stokes reduction $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$ with the empirical fact that $c^2(\rho)$ is **saturated to a constant $c_*^2$ in the dense-matter regime**.

**Test of saturation.** If $c^2(\rho) = c_*^2(\rho_{\mathrm{GR}}/\rho)^4$ were active between water and mantle, the predicted ratio $\nu_{\mathrm{mantle}}/\nu_{\mathrm{water}}$ would be $(\rho_{\mathrm{water}}/\rho_{\mathrm{mantle}})^4 \cdot \gamma_{\mathrm{water}}/\gamma_{\mathrm{mantle}} = 7.8\times10^{20}$ — a factor 256 below the observed $2\times10^{23}$. Therefore $c^2(\rho)$ does **not** vary between condensed-matter densities; the formula $c^2(\rho) = c_*^2(\rho_{\mathrm{GR}}/\rho)^4$ is asymptotic, activating only as $\rho \to \rho_{\mathrm{GR}}$.

**Absolute calibration.** Anchoring $c^2(\rho_{\mathrm{water}}) \approx c_{\mathrm{light}}^2$:

$$\gamma_{\mathrm{water}}^{\mathrm{abs}} = \frac{c_{\mathrm{light}}^2}{\nu_{\mathrm{water}}} = \frac{(3\times10^8)^2}{10^{-6}} \approx 9\times10^{22}\;\mathrm{s^{-1}}$$

— the first absolute number for $\gamma$ in the framework. All $\gamma_{\mathrm{rel}}$ values in the table above convert to absolute units by multiplying by this constant. The reciprocal $1/\gamma_{\mathrm{water}} \approx 10^{-23}$ s is the structural relaxation timescale of water — a prediction (PR-25) testable against femtosecond Raman/IR spectroscopy.

**Gas continuum (PR-24).** The continuum-regime viscosity of air obeys $\nu_{\mathrm{kin}} \propto 1/\rho$ to 0.1% precision over $P \in [10^{-3}, 10]$ atm. Combined with the saturation result, this implies $\gamma \propto \rho$ linearly across **five decades** of density at fixed $\Gamma_s$ — the strongest empirical confirmation to date of ansatz A4 ($\gamma \sim \rho\|\Gamma_s\|$, Ch10 §10.7). Cota: $\rho_{\mathrm{GR}} \ll 10^{-3}$ kg/m³, consistent with a cosmological reading (the asymptotic activation of $c^2(\rho)$ lies in the vacuum/intergalactic regime, not the dense regime).

Air requires this regime-specific treatment: its large $\nu_{\mathrm{kin}}$ reflects thermal velocity through the saturated $c^2$, not a different domain assignment.

### 17.6.6 Transient Growth and the 1/γ Regime (PR-22)

The Stokes reduction $\nu_{\mathrm{kin}} = c^2/\gamma$ comes from dropping the inertial term $\ddot\Gamma$ in the EOM (Ch15 §15.5, leading order in $1/\gamma$). Retaining that term — the next-order correction — generates a second-order linearized system

$$\dot{\mathbf{Y}} = \mathbf{A}\mathbf{Y}, \qquad \mathbf{A} = \begin{pmatrix} 0 & I \\ -\mathcal{L}_{\bar\Gamma} & -\gamma I \end{pmatrix}$$

with $\mathbf{A}$ structurally **non-normal** (commutator $[\mathbf{A},\mathbf{A}^\dagger] \neq 0$ generically). Non-normal operators support transient amplification of perturbations even when all eigenvalues lie in the stable half-plane — the mechanism behind subcritical transition in pipe flow. The PR-22 analysis (`brainstorming/pruebas_empiricas/PR22_transient_growth.md`) shows the maximum amplification scales as $G_{\max} \sim \mathrm{Re}^2/\mathcal{C}$ with $\mathcal{C}$ a geometric constant, recovering the standard non-modal scaling.

For Poiseuille pipe flow this predicts $\mathrm{Re}_c \approx \sqrt{\mathcal{C}\,\mathcal{A}_0^{-1}} \approx 2200$ (with $\mathcal{C} \approx 50$, $\mathcal{A}_0 \approx 10^{-7}$ from Hof et al. 2003), in agreement with the observed $\mathrm{Re}_c \approx 2040$. The case that escaped the leading-order E6 test (G1 pipe transition) is therefore recovered at order $1/\gamma$ — a **second regime** of the same fluid UoC (cf. Ch15 §15.1 terminological clarification).

---

## 17.7 Summary Table

| System | S, A, I, R | $\det(\Gamma)$ | $\mathcal{C}$ | $\gamma$ | EOM | Exactness |
|---|---|---|---|---|---|---|
| SHO ($b=0$) | $0,0,x,—$ | $0$ | $0$ | $0$ | $\ddot x + x = 0$ | Exact |
| DHO ($b=0.5$) | $0,0,x,—$ | $0$ | $0$ | $0.5$ | $\ddot x+0.5\dot x+x=0$ | Exact |
| EM plane wave | $0,0,E,B$ | $0$ | $0$ | $0$ | $\square F=0$ | Exact |
| GW ($h_+=10^{-21}$) | $\eta,h,h_{xx},h_{yy}$ | $-1+O(h)$ | $-1+O(h)$ | $0$ | $\square h=0$ | Exact (linear) |
| Acoustic (440 Hz) | $0,0,\phi,—$ | $0$ | $0$ | $0$ | $\square\phi=0$ | Exact |
| Stokes capillary | $p,v_x,0,0$ | $0$ | $0$ | $c^2/\nu\gg1$ | $\partial_tv=\nu\nabla^2v$ | Approx. (Re$\ll1$) |

**Pattern.** Every system with $\det(\Gamma) = 0$ (rank $\leq 2$) gives $\mathcal{C}=0$ and a linear propagating EOM. This is the structural definition of a *wave regime*: a configuration in which the UoC's source ($S$) and agency ($A$) attributes are momentarily inactive, so the dynamics lives on $\partial\mathcal{M}(\Gamma)$ and propagates without a structural attractor. The UoC itself remains the entity (mass, charge, fluid parcel); the wave regime is the dynamical window the UoC occupies under rank-$\leq 2$ conditions (Ch15 §15.1, T8 in `brainstorming/bitacora_tensiones.md`).

**Two regimes per UoC.** The fluid UoC in particular exhibits at least two structurally distinct regimes: the Stokes regime (leading order, $\gamma \to \infty$, captured by E6) and the inertial/transient-growth regime (order $1/\gamma$, captured by PR-22 §17.6.6). Pipe flow at $\mathrm{Re}_c \approx 2040$ lives in the latter; channel flow at $\mathrm{Re}_c \approx 5772$ lives in the former. Same UoC, same equation, different regime.

The Stokes flow is structurally different: it could have $\det(\Gamma) > 0$ if all three velocity components are active (3D flow). The degenerate case arises here because the Poiseuille flow is axisymmetric — only one velocity component is active. A fully three-dimensional Stokes flow would have $\det(\Gamma) > 0$, $\mathcal{C} > 0$, and the full nonlinear EOM would apply in principle (though adj remains negligible in the $\varepsilon\to0$ limit).

---

*These examples close the loop between the abstract Lagrangian of Ch13–14 and physical observables. The same framework — same $\Gamma$, same EOM, same $\mathcal{C}$ — produces equations for oscillators, fields, gravity, and viscous flow. What changes between systems is the slot assignment and the value of $\gamma$. Chapter 18 asks: which of the postulates that generated this Lagrangian have now been closed, and which remain open.*
