# Capítulo 15b: Análisis Espectral del GSF
*Versión condensada — Parte II*

---

## 15b.1 Modos de Propagación vs. Modos Ligados

La estructura espectral de la dinámica linealizada revela una distinción fundamental:

| Régimen | Condición | Autovalor espectral | Significado físico |
|---|---|---|---|
| Propagación (onda) | $S = A = 0$, $\mathrm{rank}(\Gamma) \leq 2$ | $\lambda = 0$ | Sin fuerza restauradora; el sistema se propaga sin atractor |
| Ligado (partícula) | $S \neq 0$ o $A \neq 0$, $\det(\Gamma) > 0$ | $\lambda > 0$ o $\lambda < 0$ | Fuerza restauradora o inestabilidad; existe un atractor |

**Operador de masa efectiva.** Linearizar las EOM alrededor de un fondo estático $\Gamma_0 = \sigma I$ (homogéneo, isotrópico) produce:

$$\mathcal{M}_{\Gamma_0}[\delta\Gamma] = \delta\Gamma + \mu\det(\Gamma_0)\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-T} - \Gamma_0^{-T}\delta\Gamma^T\Gamma_0^{-T}\right]$$

Para el fondo escalar $\Gamma_0 = \sigma I$, se separan tres sectores de modos:

| Sector | Modo | Autovalor $\lambda$ |
|---|---|---|
| Traza | Escalamiento uniforme | $\lambda_{\mathrm{tr}} = 1 + 3\mu\sigma^2$ |
| Simétrico sin traza | Deformación de forma | $\lambda_{\mathrm{sym}} = 1 - \mu\sigma^2$ |
| Antisimétrico | Campo de gauge | $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2$ |

---

## 15b.2 El Punto Crítico: Umbral Espectral = Umbral de Creación de Materia

El autovalor del sector simétrico $\lambda_{\mathrm{sym}} = 0$ en:

$$\sigma^* = \sqrt{1/\mu} = \rho_{\mathrm{GR}}/\rho$$

**Teorema 15b.1.** Este punto crítico coincide exactamente con el umbral de creación de materia $\sigma^*$ del Cap. 14 §14.8.1. La misma ecuación derivada desde dos perspectivas independientes (espectral vs. termodinámica).

**Consecuencia:** El atractor $P(\Gamma) \sim \sigma^* I$ es equivalente a la transición de fase donde el modo simétrico sin traza transiciona de estable a taquiónico (de masa nula a masa imaginaria).

| Régimen | $\sigma < \sigma^*$ | $\sigma = \sigma^*$ | $\sigma > \sigma^*$ |
|---|---|---|---|
| **Traza** | $\lambda_{\mathrm{tr}} > 1$ (estable) | $\lambda_{\mathrm{tr}} = 4$ | $> 4$ (desacoplado) |
| **Simétrico** | $\lambda_{\mathrm{sym}} > 0$ (estable) | $\lambda_{\mathrm{sym}} = 0$ (crítico) | $< 0$ (taquiónico) |
| **Antisimétrico** | $\lambda_{\mathrm{anti}} > 1$ | $\lambda_{\mathrm{anti}} = 2$ | $> 2$ (siempre estable) |
| **Física** | Sin materia, todos los modos se propagan | Umbral; el modo se vuelve de masa nula | Materia condensada; inestabilidad |

---

## 15b.3 Protección de Masa en el Sector Antisimétrico

El autovalor antisimétrico $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2 > 0$ para todo $\sigma > 0$.

**Consecuencia:** Ningún modo en el sector antisimétrico se vuelve taquiónico. Este es el origen estructural de la carencia de masa del fotón: el sector de curvatura $\Gamma_a = dA$ mantiene su término cinético y nunca desarrolla un término de masa, independientemente de la configuración del fondo.

---

## 15b.4 Conexión con la Parte III

La estructura espectral es la puerta de entrada a tres problemas abiertos:

1. **Signatura Lorentziana** ($\det < 0$): El signo de $\mu\det(\Gamma_0)$ se invierte. ¿cómo se desplaza el punto crítico? ¿Cambia la jerarquía de los umbrales?

2. **Más allá de fondos homogéneos:** El cálculo $\Gamma_0 = \sigma I$ es estructuralmente completo pero cubre solo fondos isotrópicos. La generalización a fondos anisotrópicos y evolución cosmológica requiere la Parte III.

3. **Estructura topológica del espectro:** El espacio de moduli de las soluciones homogéneas y sus bifurcaciones está determinado por la topología de $\mathcal{M}(\Gamma) = \mathrm{SO}(4)$. Esta es la conexión con el análisis topológico del Capítulo 20.

---

## Estado Epistémico

| Afirmación | Estado |
|---|---|
| Operador de masa efectiva $\mathcal{M}_{\Gamma_0}$ | Derivado (Lema 15b.1) |
| Descomposición espectral de tres sectores | Exacta para $\Gamma_0 = \sigma I$ |
| Teorema 15b.1 (coincidencia del punto crítico) | Probado; validado por Cap. 14 |
| Protección de masa del sector antisimétrico | Estructural; consecuencia del rango de la adjunta |
| Evolución espectral completa ($\Gamma_0$ general) | Abierto; requiere Parte III |

El patrón: El mismo Lagrangiano GSF analizado desde la perspectiva espectral revela que el umbral de creación de materia no es una entrada fenomenológica, sino una bifurcación estructural del espectro de fluctuaciones.
