# Chapter 17: Worked Examples — GSF in Physical Systems
*Condensed version — Part II*

---

Five physical systems worked through explicitly at two levels (statics + dynamics). All use the same Lagrangian; what changes is the slot assignment and $\gamma$.

## Systems and Key Numbers

| System | $\gamma$ | $\det(\Gamma)$ | $\mathcal{C}$ | EOM | Exactness |
|---|---|---|---|---|---|
| SHO undamped | $0$ | $0$ | $0$ | $\ddot x + x = 0$ | Exact |
| SHO damped ($b=0.5$) | $0.5$ | $0$ | $0$ | $\ddot x + 0.5\dot x + x = 0$ | Exact |
| SHO critical | $2$ | $0$ | $0$ | $\ddot x + 2\dot x + x = 0$ | Exact |
| EM plane wave ($E_0=1$ V/m) | $0$ | $0$ | $0$ | $\square F = 0$ | Exact |
| Gravitational wave ($h=10^{-21}$) | $0$ | $-1+O(h)$ | $-1+O(h)$ | $\square h = 0$ | Exact (linear) |
| Acoustic (440 Hz) | $0$ | $0$ | $0$ | $\square\phi = 0$ | Exact |
| Stokes capillary (water, Re=$3\times10^{-4}$) | $c^2/\nu \gg 1$ | $0$ (rank 2) | $0$ | $\partial_tv = \nu\nabla^2v$ | Approx. |

## Key Observations

**$\gamma = 2$ is structurally special**: critical damping for the SHO AND the massless graviton condition ($\mu(\rho_{\mathrm{GR}}) = 2$). Not a coincidence — both arise from the same structural condition.

**All wave-like systems have $\mathcal{C}=0$**: photon, phonon, SHO, graviton. They live on $\partial\mathcal{M}(\Gamma)$. Structural coherence $> 0$ requires $\det(\Gamma) > 0$, which requires all four slots simultaneously active.

**PR-18 confirmed numerically**: EM and acoustic modes in a rectangular duct have identical spectral topology — same integers $(m,n)$, same mode structure, different propagation speed ($c$ vs $c_s$). Same structural object, different $\rho$.

**$\gamma$ ratio table (water = reference):**

| Fluid | $\gamma_{\mathrm{rel}}$ |
|---|---|
| Mercury | $8.4$ |
| Water | $1$ (reference; absolute: $\gamma_{\mathrm{water}} \approx 9\times10^{22}\,\mathrm{s^{-1}}$) |
| Blood plasma | $0.77$ (lower threshold of biological window) |
| D₂O | $0.80$ (25% more damped → biologically inert above ~25% v/v) |
| Whole blood (high shear) | $0.29$ |
| Glycerol | $6.7\times10^{-4}$ |
| Glacial ice | $\sim10^{-18}$ (conservative regime) |
| Earth's mantle | $\sim5\times10^{-24}$ |

**25 orders of magnitude** of $\gamma_{\mathrm{rel}}$ from mercury to mantle — single equation, zero adjustments (E1, E9, E10).

## Empirical anchoring (2026-05-31)

**§17.6.5 Absolute calibration (E6×E1).** Comparison $\nu_{\mathrm{mantle}}/\nu_{\mathrm{water}} = 2\times10^{23}$ vs the naïve formula $(\rho_{\mathrm{water}}/\rho_{\mathrm{mantle}})^4 \cdot (\gamma_{\mathrm{water}}/\gamma_{\mathrm{mantle}}) = 7.8\times10^{20}$ shows a factor 256 discrepancy → the $(\rho_{GR}/\rho)^4$ factor is **inactive** in the dense regime. $c^2(\rho)$ is saturated to $c_*^2 \approx c_{\mathrm{light}}^2$. Anchoring this gives $\gamma_{\mathrm{water}}^{\mathrm{abs}} \approx 9\times10^{22}\,\mathrm{s^{-1}}$; reciprocal $1/\gamma \approx 10^{-23}\,\mathrm{s}$ is a structural relaxation timescale (PR-25, ultrafast spectroscopy).

**§17.6.5 PR-24 confirmation of A4.** Air viscosity obeys $\nu \propto 1/\rho$ to 0.1% over $P \in [10^{-3}, 10]$ atm. Combined with $c^2$ saturated, this implies $\gamma \propto \rho$ linearly across **5 decades** at fixed $\Gamma_s$. Ansatz A4 is now an **empirical law**, not a postulate. Cota: $\rho_{GR} \ll 10^{-3}\,\mathrm{kg/m^3}$ (cosmological reading remains viable as asymptote, not as global formula).

**§17.6.6 Transient growth at order $1/\gamma$ (PR-22).** Retaining the inertial term $\ddot\Gamma$ in the EOM yields a structurally non-normal linearized system. Max non-modal amplification $G_{\max} \sim \mathrm{Re}^2 / \mathcal{C}$. Numerical verification: plane Poiseuille recovers Reddy-Henningson 1993 to 4 sig figs ($G_{\max} = 196$ at Re=1000, $\beta=2.0$); pipe Poiseuille deferred to follow-up (Paper 7). The case G1 (pipe transition $\mathrm{Re}_c \approx 2040$) that fell outside the leading-order E6 test is recovered at order $1/\gamma$ — a **second regime** of the same fluid UoC (cf. §15.1 terminological clarification).
