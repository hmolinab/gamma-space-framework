# Capítulo 17: Ejemplos Resueltos — GSF en Sistemas Físicos
*Versión condensada — Parte II*

---

Cinco sistemas físicos analizados explícitamente en dos niveles (estática + dinámica). Todos utilizan el mismo Lagrangiano; lo que cambia es la asignación de ranuras (*slots*) y $\gamma$.

## Sistemas y Números Clave

| Sistema | $\gamma$ | $\det(\Gamma)$ | $\mathcal{C}$ | EOM | Exactitud |
|---|---|---|---|---|---|
| SHO no amortiguado | $0$ | $0$ | $0$ | $\ddot x + x = 0$ | Exacto |
| SHO amortiguado ($b=0.5$) | $0.5$ | $0$ | $0$ | $\ddot x + 0.5\dot x + x = 0$ | Exacto |
| SHO crítico | $2$ | $0$ | $0$ | $\ddot x + 2\dot x + x = 0$ | Exacto |
| Onda plana EM ($E_0=1$ V/m) | $0$ | $0$ | $0$ | $\square F = 0$ | Exacto |
| Onda gravitacional ($h=10^{-21}$) | $0$ | $-1+O(h)$ | $-1+O(h)$ | $\square h = 0$ | Exacto (lineal) |
| Acústico (440 Hz) | $0$ | $0$ | $0$ | $\square\phi = 0$ | Exacto |
| Capilar de Stokes (agua, Re=$3\times10^{-4}$) | $c^2/\nu \gg 1$ | $0$ (rango 2) | $0$ | $\partial_tv = \nu\nabla^2v$ | Aprox. |

## Observaciones Clave

**$\gamma = 2$ es estructuralmente especial**: amortiguamiento crítico para el SHO Y la condición del gravitón sin masa ($\mu(\rho_{\mathrm{GR}}) = 2$). No es una coincidencia — ambos surgen de la misma condición estructural.

**Todos los sistemas de tipo onda tienen $\mathcal{C}=0$**: fotón, fonón, SHO, gravitón. Viven en $\partial\mathcal{M}(\Gamma)$. La coherencia estructural $> 0$ requiere $\det(\Gamma) > 0$, lo que exige que las cuatro ranuras (*slots*) estén activas simultáneamente.

**PR-18 confirmado numéricamente**: Los modos EM y acústicos en un conducto rectangular tienen una topología espectral idéntica — mismos enteros $(m,n)$, misma estructura de modos, diferente velocidad de propagación ($c$ vs $c_s$). Mismo objeto estructural, diferente $\rho$.

**Tabla de relación de $\gamma$ (agua = referencia):**

| Fluido | $\gamma_{\mathrm{rel}}$ |
|---|---|
| Mercurio | $8.4$ |
| Agua | $1$ (referencia; absoluto: $\gamma_{\mathrm{agua}} \approx 9\times10^{22}\,\mathrm{s^{-1}}$) |
| Plasma sanguíneo | $0.77$ (umbral inferior de la ventana biológica) |
| D₂O | $0.80$ (25% más amortiguado → biológicamente inerte por encima de ~25% v/v) |
| Sangre completa (alto cizallamiento) | $0.29$ |
| Glicerol | $6.7\times10^{-4}$ |
| Hielo glacial | $\sim10^{-18}$ (régimen conservativo) |
| Manto terrestre | $\sim5\times10^{-24}$ |

**25 órdenes de magnitud** de $\gamma_{\mathrm{rel}}$ desde el mercurio hasta el manto — una sola ecuación, cero ajustes (E1, E9, E10).

## Anclaje empírico (2026-05-31)

**§17.6.5 Calibración absoluta (E6×E1).** La comparación $\nu_{\mathrm{manto}}/\nu_{\mathrm{agua}} = 2\times10^{23}$ frente a la fórmula ingenua $(\rho_{\mathrm{agua}}/\rho_{\mathrm{manto}})^4 \cdot (\gamma_{\mathrm{agua}}/\gamma_{\mathrm{manto}}) = 7.8\times10^{20}$ muestra una discrepancia de factor 256 → el factor $(\rho_{GR}/\rho)^4$ está **inactivo** en el régimen denso. $c^2(\rho)$ se satura a $c_*^2 \approx c_{\mathrm{luz}}^2$. El anclaje de esto da $\gamma_{\mathrm{agua}}^{\mathrm{abs}} \approx 9\times10^{22}\,\mathrm{s^{-1}}$; el recíproco $1/\gamma \approx 10^{-23}\,\mathrm{s}$ es una escala de tiempo de relajación estructural (PR-25, espectroscopía ultrafásica).

**§17.6.5 PR-24 confirmación de A4.** La viscosidad del aire obedece a $\nu \propto 1/\rho$ al 0.1% sobre $P \in [10^{-3}, 10]$ atm. Combinado con $c^2$ saturado, esto implica que $\gamma \propto \rho$ linealmente a través de **5 décadas** a $\Gamma_s$ fija. El Ansatz A4 es ahora una **ley empírica**, no un postulado. Cota: $\rho_{GR} \ll 10^{-3}\,\mathrm{kg/m^3}$ (la lectura cosmológica sigue siendo viable como asíntota, no como fórmula global).

**§17.6.6 Crecimiento transitorio al orden $1/\gamma$ (PR-22).** Retener el término inercial $\ddot\Gamma$ en la EOM produce un sistema linealizado estructuralmente no normal. La amplificación no modal máxima $G_{\max} \sim \mathrm{Re}^2 / \mathcal{C}$. Verificación numérica: Poiseuille plano recupera Reddy-Henningson 1993 con 4 cifras significativas ($G_{\max} = 196$ en Re=1000, $\beta=2.0$); Poiseuille de tubería aplazado para el seguimiento (Artículo 7). El caso G1 (transición en tubería $\mathrm{Re}_c \approx 2040$) que quedó fuera de la prueba E6 de orden principal se recupera al orden $1/\gamma$ — un **segundo régimen** de la misma UoC de fluido (cf. aclaración terminológica §15.1).
