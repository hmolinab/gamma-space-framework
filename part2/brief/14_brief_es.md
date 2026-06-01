# Capítulo 14: La Ley de Escalamiento — T1
*Versión condensada — Parte II*

---

## 14.1 El Problema Residual

El Cap. 13 derivó $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma)$ con $\mu(\rho) = 2/\sqrt{c(\rho)}$, pero dejó $c(\rho)$ abierto excepto en el anclaje $c(\rho_{\mathrm{GR}}) = 1$. El Cap. 14 deriva $c(\rho)$ para todo $\rho$ a través de la **ley de escalamiento T1**: $\Gamma(\rho) \propto \rho^{-1}$.

**Avance de resultados:**
$$c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4, \qquad \mu(\rho) = 2\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^2, \qquad \kappa(\rho) = -1 \;\text{(universal)}$$

**Nota sobre dimensionalidad.** $\rho$ es adimensional (índice organizacional); $\Gamma$ porta la dimensión $\rho^{-1}$ — también adimensional en unidades naturales de GSF. El Lagrangiano $\mathcal{L}$ es, por lo tanto, adimensional: mide el *costo estructural relativo*, no la energía en Joules. La correspondencia con unidades físicas requiere una constante de escalamiento global (Hito 3, Parte III). Los Capítulos 15–18 verifican la recuperación estructural (misma forma funcional), no cuantitativa (mismos coeficientes SI), de los resultados conocidos.

---

## 14.2 Triangulación Estructural

T1 se establece mediante tres roles estructurales, no tres derivaciones independientes:

| Argumento | Rol | Resultado |
|---|---|---|
| 1 — Estructura de grupo | Establece la forma | $\Gamma \propto \rho^\alpha$; $\alpha$ libre |
| 2 — Covarianza Lagrangiana | **Selecciona** $\alpha$ | C2: $\alpha < 0$; C3 (Lema 14.2): $\alpha = -1$ |
| 3 — Covarianza de las EOM | Confirma + extrae $\delta = 0$ | $\alpha = -1$ consistente; tiempo absoluto |

---

## 14.3 Argumento 1 — Estructura de Grupo

Los cambios de nivel se componen: $f(\lambda_1\lambda_2) = f(\lambda_1)f(\lambda_2)$.

**Lema 14.1.** La única solución continua es $f(\lambda) = \lambda^\alpha$ (Cauchy en $\mathbb{R}_{>0}$).

Resultado: $\Gamma(\rho) = \Gamma_0\cdot\rho^\alpha$. Forma establecida; $\alpha$ libre.

---

## 14.4 Argumento 2 — Covarianza Lagrangiana

El escalamiento uniforme $(\rho \to \lambda\rho,\; \Gamma \to \lambda^\alpha\Gamma)$ fuerza $\mathrm{deg}(\mu) = -2\alpha$.

**Restricción C2 (Costo de coordinación).** Los sistemas organizacionalmente más complejos requieren más "pegamento" estructural para mantener su patrón de acoplamiento $\Gamma$ frente a las perturbaciones — no rigidez conductual, sino un mayor *costo de coordinación*. Formalmente: $\mu(\rho)$ debe ser creciente en $\rho$:
$$\frac{d\mu}{d\rho} > 0 \implies \alpha < 0$$

**Restricción C3 (Sección mínima invariante ante la representación).** El objeto estructural invariante de nivel $\mathcal{I}(\rho,\Gamma)$ debe:
- *(a) G-invariancia:* $\mathcal{I}(\lambda\rho, \lambda^\alpha\Gamma) = \mathcal{I}(\rho,\Gamma)$
- *(b) H-covarianza:* transformarse en la misma representación del grupo estructural que $\Gamma$

La condición (b) fuerza a que $\mathcal{I}$ sea *lineal* en $\Gamma$ — los escalares ($\det$), normas (dependientes de la métrica) y la adjunta ($\mathrm{adj}$) están en representaciones diferentes. El mapeo lineal H-covariante más general es $\mathcal{I} = f(\rho)\Gamma$; la G-invariancia fuerza $f(\rho) \propto \rho^{-\alpha}$.

**Lema 14.2 (Sección fija y $\alpha = -1$).** El generador de escalamiento $\rho\,d/d\rho$ actúa sobre $\rho^k\Gamma$ como $(k+\alpha)\rho^k\Gamma$. Una sección fija (autovalor 0) requiere $k = -\alpha$. Con C2 forzando $\alpha < 0$ (por lo que $k > 0$), el $k$ positivo *mínimo* es $k=1$, dando el objeto primitivo invariante de nivel $\rho\Gamma$ y forzando:
$$\boxed{\alpha = -1}$$

El caso $\alpha = -2$ requiere $k = 2$ — una sección de segundo orden, excluida por minimalidad. El caso $\alpha = -1/2$ da $k = 1/2$, fuera de la representación polinómica.

---

## 14.5 Argumento 3 — Covarianza de las EOM e Invariancia de Escala Temporal

Bajo un $\alpha$ general con $\mathrm{deg}(\mu) = -2\alpha$, los cuatro términos de las EOM escalan como $\lambda^\alpha$ — la covarianza de las EOM se mantiene para *cualquier* $\alpha$. El Argumento 3 no puede fijar $\alpha$; es una comprobación de consistencia.

**Postulado 14.1 (Invariancia de Escala Temporal).** Bajo un reescalamiento conjunto $(t \to \lambda^\delta t,\; \rho \to \lambda\rho,\; \Gamma \to \lambda^\alpha\Gamma)$, la covarianza de las EOM fuerza $\delta = 0$: los términos $\ddot\Gamma$, $\dot\Gamma$, $\Gamma$ escalan como $\lambda^{\alpha-2\delta}$, $\lambda^{\alpha-\delta}$, $\lambda^\alpha$ respectivamente — iguales solo si $\delta = 0$.

**Proposición 14.1.** Con $\delta = 0$, las EOM confirman que $\alpha = -1$ es consistente. $\alpha = -2$ queda excluido por C3 (sección mínima, no solo por el Cap. 13 — evitando la circularidad).

---

## 14.6 Teorema 14.1 — T1

$$\boxed{T1:\quad\Gamma(\rho) = \frac{\Gamma(\rho_{\mathrm{ref}})\cdot\rho_{\mathrm{ref}}}{\rho} \qquad\Longleftrightarrow\qquad \frac{d\Gamma}{d\rho} = -\frac{\Gamma}{\rho}}$$

---

## 14.7 Consecuencias de T1

**Coherencia estructural.** La condición de atractor $P(\Gamma)P(\Gamma)^T \propto \det(P(\Gamma))\cdot\mathbf{1}_4$ es homogénea de grado 2 en $P$ — por lo que $\Gamma \to \lambda^{-1}\Gamma$ implica $P \to \lambda^{-1}P$ y $\det(P) \to \lambda^{-4}\det(P)$. La proyección del atractor hereda el escalamiento $\rho^{-4}$ de $\det(\Gamma)$:
$$\boxed{c(\rho) = \left(\frac{\rho_{\mathrm{GR}}}{\rho}\right)^4}$$

**Fuerza de acoplamiento:** $\mu(\rho) = 2/\sqrt{c(\rho)} \implies \mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$.

El incremento monótono codifica el *costo de coordinación*: a mayor $\rho$, mantener la identidad requiere más "pegamento" estructural. Una red neuronal es conductualmente flexible pero estructuralmente costosa de reorganizar.

**$\kappa = -1$ universal:** La forma de Frobenius (razón de sectores) es invariante bajo $\Gamma \to \lambda^{-1}\Gamma$ — la gramática cinética es universal a través de todo $\rho$.

**Lagrangiano completo:**
$$\boxed{\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)}$$

---

## 14.8 Predicciones Estructurales

### Umbral de creación de materia

Potencial de signatura lorentziana: $V_{\mathrm{eff}} = 4\sigma^2 - 2(\rho/\rho_{\mathrm{GR}})^2\sigma^4$. Umbral de nucleación (requiere explícitamente $E_{\mathrm{fluct}} < 2$):
$$\rho_{\mathrm{mat}} = \rho_{\mathrm{GR}}\sqrt{2/E_{\mathrm{fluct}}} > \rho_{\mathrm{GR}}$$

**Inestabilidad global.** El potencial $-\sigma^4$ no tiene un mínimo global — una vez que se cruza la barrera, el sistema rueda hacia $\sigma \to \infty$. Dos resoluciones: (a) término estabilizador de grado 6 proveniente de invariantes de orden superior (más allá del Lagrangiano mínimo), o (b) la materia como un estado metaestable de larga duración. Abierto para la Parte III.

### Constante cosmológica

Predicción clásica de GSF: $\Lambda_{\mathrm{eff}} = 0$ (a partir de $c(\rho_{\mathrm{GR}}) = 1$ exactamente).

**Tensión:** $\Lambda_{\mathrm{obs}} > 0$ es un problema abierto genuino. La conversión de unidades no puede rescatar el cero: 0 × (cualquier factor) = 0.

**Observación estructural (signo).** Una desviación $c(\rho_{\mathrm{GR}}) = 1 - \varepsilon < 1$ da $\Delta\mu = \mu(\rho_{\mathrm{GR}}) - 2 > 0$, produciendo $\Lambda_{\mathrm{eff}} \propto \Delta\mu > 0$ — cualitativamente consistente con el signo *positivo* observado de $\Lambda_{\mathrm{obs}}$. No es una predicción cuantitativa; es un resultado de consistencia de signo estructural.

---

## 14.9 Estatus Epistémico

| Resultado | Estatus | Notas |
|---|---|---|
| Forma de escalamiento $\Gamma \propto \rho^\alpha$ | Derivado | Ecuación funcional de Cauchy |
| C2: $\alpha < 0$ | Derivado | Costo de coordinación → $\mu$ creciente |
| C3: $\alpha = -1$ | Derivado — Lema 14.2 | Sección fija mínima invariante ante la representación |
| $\delta = 0$ (tiempo absoluto) | Derivado — Postulado 14.1 | Covarianza de las EOM bajo reescalamiento conjunto |
| Escalamiento del atractor hereda $\rho^{-4}$ | Derivado | Homogeneidad de la condición de atractor |
| $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$ | Derivado | Exacto dentro del supuesto de ley de potencia |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | Derivado | Libre de parámetros |
| $\kappa = -1$ universal | Derivado | Invariancia de la forma de Frobenius |
| $[\mathcal{L}] = 1$ (adimensional) | Estructural | Unidades físicas vía Hito 3 |
| "Cero parámetros libres" ($\mathcal{L}$) | Solo estructural | $\gamma$, $N(t)$ abiertos en EOM disipativas |
| $\rho_{\mathrm{mat}} > \rho_{\mathrm{GR}}$ | Condicional | Requiere $E_{\mathrm{fluct}} < 2$ (abierto) |
| Estabilidad global del estado de materia | Abierto | Inestabilidad $-\sigma^4$; Parte III |
| $\Lambda_{\mathrm{eff}} = 0$ vs $\Lambda_{\mathrm{obs}} > 0$ | Abierto | Signo de $\Delta\mu$ cualitativamente consistente |
| Correcciones logarítmicas a T1 | Abierto | Extensión cuántica |
| Escala absoluta de $\rho_{\mathrm{GR}}$ | Abierto | Hito 3 (puente de Planck) |

---

*El Cap. 14 completa el Lagrangiano clásico de GSF. Los Capítulos 15–18 verifican la consistencia estructural a través de cinco dominios.*
