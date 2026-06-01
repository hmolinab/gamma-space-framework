# Capítulo 15: Dominio I — Sistemas Físicos
*Versión condensada — Parte II*

---

## 15.1 El Programa de Reducción

El Lagrangiano y las EOM de la GSF son estructuralmente invariantes (mantienen la misma forma en todos los niveles organizacionales):

$$\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - 2\!\left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\det(\Gamma)$$

$$\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \left(\frac{\rho}{\rho_{\mathrm{GR}}}\right)^{\!2}\mathrm{adj}(\Gamma)^T = N(t)$$

El Ch15 lleva a cabo el **programa de reducción**: asignar atributos $\{S, A, \mathbf{I}, \mathbf{R}\}$, imponer restricciones de dominio sobre $\Gamma$, evaluar las EOM y verificar frente a las ecuaciones establecidas. Cinco dominios físicos; cero parámetros nuevos.

**Clarificación terminológica (UoC vs. régimen).** Cada reducción identifica un **régimen dinámico** de una UoC subyacente, no una nueva UoC. La UoC sigue siendo la entidad (masa, sistema cargado, parcela de fluido); las reducciones de rango $\leq 2$ caracterizan el régimen en el que ciertos atributos están momentáneamente inactivos. Esto es consistente con el Ch12 §12.3.2 (las configuraciones de frontera no son UoCs en el sentido pleno). La dualidad onda-partícula es, por lo tanto, una dualidad de *regímenes* de la misma UoC subyacente — ver Observación 15.8.

---

## 15.2 Herramienta Estructural Central — Lema 15.1

**Lema 15.1.** Si $\Gamma$ es una matriz de $4\times 4$ con $\mathrm{rank}(\Gamma) \leq 2$, entonces $\mathrm{adj}(\Gamma) = 0$.

*Prueba.* Cada entrada de $\mathrm{adj}(\Gamma)$ es un cofactor de $3\times3$. Si el rango es $\leq 2$, cada submatriz de $3\times3$ contiene una fila de ceros — cofactor = 0. $\square$

Este lema es la clave para todas las reducciones lineales. Cuando $S = A = 0$, la matriz de acoplamiento tiene rango $\leq 2$ y el término atractor no lineal desaparece idénticamente.

---

## 15.3 Cinco Reducciones

### Escalar (1×1)

$\Gamma = (x)$: La EOM se convierte en $\ddot u + \gamma\dot u + u = 0$ donde $u = x + (\rho_\star/\rho_{\mathrm{GR}})^2$.

**Proposición 15.1.** El equilibrio estructural es $x^\star = -(\rho_\star/\rho_{\mathrm{GR}})^2$ — real, negativo, fuera de $\mathcal{M}_{\mathrm{adm}} = \{x > 0\}$. No existe un atractor interior estable para el escalar 1D. Consistente con el Ch14: la materia requiere cruzar la barrera de potencial lorentziana.

### Oscilador Armónico Simple (SHO)

Inserción de propósito nulo: $S = A = 0$, contenido físico en el bloque $(\mathbf{I},\mathbf{R})$:

$$\Gamma = \mathrm{diag}_{SA=0}\begin{pmatrix} 0 & x \\ -x & 0 \end{pmatrix}_{\mathbf{IR}}$$

Por el Lema 15.1, $\mathrm{adj}(\Gamma) = 0$. La EOM da:

$$\boxed{\ddot x + \gamma\dot x + x = 0} \quad\checkmark$$

**Teorema 15.1.** Exacto — cero ajuste de parámetros. Los atributos $S, A$ nulos codifican la ausencia de carga y agencia.

**Observación 15.3.** La física lineal es exacta cuando $\mathrm{rank} \leq 2$. Cualquier sistema que desarrolle un $S$ o $A$ distinto de cero —por pequeño que sea— sale del régimen lineal. La linealidad observada es una consecuencia de la simplicidad organizacional, no una propiedad fundamental.

### Péndulo

**Estatus: analogía geométrica, no derivación.** Las geodésicas en $\|\Gamma\|_F = r$ son círculos máximos — sin fuerza restauradora. La ecuación del péndulo $\ddot\theta + \sin\theta = 0$ requiere (i) un espacio de configuración compacto $S^1$ y (ii) un potencial gravitatorio $V(\theta) = gL(1-\cos\theta)$ — entradas específicas del dominio fuera del presente Lagrangiano. Diferido a la Parte III.

**Por qué el Lagrangiano GSF no puede derivar el péndulo — declaración precisa.** El fallo es geométrico, no físico. La GSF vive en $\mathrm{GL}(4,\mathbb{R})$ — una variedad abierta y no compacta. Para un sistema escalar ($1\times 1$), $\mathrm{adj}(\Gamma) = 1$ (constante), por lo que la EOM se reduce a un oscilador armónico desplazado, no a un péndulo. La fuerza restauradora $\sin\theta$ requiere (a) la órbita compacta $S^1 \subset \mathrm{GL}(4,\mathbb{R})$ generada por la acción de SO(4) sobre $P(\Gamma)$, y (b) un acoplamiento al sector gravitatorio ($\Gamma_s \sim g_{\mu\nu}$, Ch31) que produzca la energía potencial gravitatoria $gL(1-\cos\theta)$. Ninguno de los dos está disponible dentro del Lagrangiano actual restringido a $\mathrm{GL}(4,\mathbb{R})$ sin estructura de fibrado.

**Hoja de ruta de la Parte III (B4).** Dos pasos: (1) identificar $\theta$ como el ángulo que parametriza la órbita de SO(4) de $P(\Gamma)$ — una subvariedad compacta de $\mathcal{M}(\Gamma)$; (2) derivar $V(\theta)$ como un término de acoplamiento cruzado $\rho_{\mathrm{grav}} \cdot gL(1-\cos\theta)$ a partir de la reducción gravitatoria de los Ch31–Ch32. El péndulo emerge como la reducción dimensional de la dinámica GSF a la órbita compacta, acoplada al sector gravitatorio.

### Vacío Electromagnético — Formulación de Curvatura

**Asignación de atributos:** $S = A = 0$ (vacío), $\Gamma = \Gamma_a = F_{\mu\nu}$ (antisimétrico, $\mathbf{E}$ y $\mathbf{B}$ en el sector $\mathbf{I},\mathbf{R}$).

**Cadena de la adjunta:** EM transversal $\implies$ $\mathbf{E}\cdot\mathbf{B} = 0 \implies \mathrm{Pf}(F) = 0 \implies \det(F) = 0$. Para una matriz antisimétrica de $4\times4$, el rango debe ser par; $\det = 0$ elimina el rango 4, por lo que $\mathrm{rank}(F) \leq 2$. Por el Lema 15.1: $\mathrm{adj}(F) = 0$.

**Proposición 15.3 (Sector antisimétrico como curvatura).** $\Gamma_a \in \Lambda^2V$ — no es una variable primaria sino una 2-forma de curvatura $\Gamma_a = F = dA$. Consecuencias:

| | Consecuencia | Origen |
|---|---|---|
| Bianchi | $dF = d^2A = 0$ | $d^2 = 0$ |
| Maxwell | $\partial_\mu F^{\mu\nu} = 0$ | $\delta\|dA\|^2/\delta A = 0$ |
| Gauge | Redundancia $A \to A + d\Lambda$ | $d^2\Lambda = 0$ |

**Protección de masa.** $\Gamma_s$ (tensor primario) admite masa: $\|\Gamma_s\|_F^2$ es un término de masa. $\Gamma_a = dA$ (curvatura) no tiene masa: $\|dA\|_F^2$ es cinético para $A$, no un término de masa. La ausencia de masa es una consecuencia de la representación, no una simetría impuesta.

**Teorema 15.2.** $\Gamma_a = F = dA$ con $\mathbf{E}\cdot\mathbf{B} = 0$ produce ambos conjuntos de ecuaciones de Maxwell. Sin parcheo de gauge. *(Inserción en fibrado diferida a la Parte III).*

$$\boxed{\partial_\mu F^{\mu\nu} = 0, \quad \partial_{[\mu}F_{\nu\rho]} = 0} \quad\checkmark$$

### Gravedad Linealizada

**Asignación de atributos:** $\Gamma_s = \eta_{\mu\nu} + h_{\mu\nu}$, $\Gamma_a = 0$.

Linealizando $\mathrm{adj}(\Gamma_s)^T$ a primer orden en $h$, con $\rho = \rho_{\mathrm{GR}}$ (por lo tanto $\mu = 2$):

$$\square h_{\mu\nu} + \underbrace{(1+1)}_{m_h^2}h_{\mu\nu} - \eta_{\mu\nu}\mathrm{Tr}(h) = 0$$

La masa: $m_h^2 = 2 - \mu(\rho_{\mathrm{GR}}) = 2 - 2 = 0$. En el gauge de de Donder:

$$\boxed{\square h_{\mu\nu} = 0} \quad\checkmark$$

**Teorema 15.3.** El gravitón sin masa es una consecuencia exacta de $\mu(\rho_{\mathrm{GR}}) = 2$, derivado independientemente en el Ch13 a partir del anclaje de normalización $c(\rho_{\mathrm{GR}}) = 1$.

---

## 15.4 Dualidad Onda-Partícula como Bifurcación Estructural

**Observación 15.8.** La estructura de rango de $\Gamma$ particiona las configuraciones en dos regímenes:

| Régimen | Condición | Geometría | Dinámica |
|---|---|---|---|
| Onda | $S = A = 0$, $\det = 0$, $\mathrm{rank} \leq 2$ | $\partial\mathcal{M}(\Gamma)$, en $\Lambda^2V$ | Lineal, propagante, sin atractor |
| Partícula | $S \neq 0$ o $A \neq 0$, $\det > 0$ | Interior de $\mathcal{M}_{\mathrm{adm}}$ | No lineal, localizada, existe el atractor $P(\Gamma)$ |

La dualidad onda-partícula es una propiedad del **estado de los atributos** $S$ y $A$, no del objeto. Transición gobernada por el umbral de creación de materia $\rho_{\mathrm{mat}}$ (Ch14 §14.8.1).

**Calificación.** Este es el análogo estructural clásico — propagación de campo vs. localización de fuente. La versión cuántica (regla de Born, colapso de la función de onda) requiere la extensión cuántica de la GSF (Parte III).

---

## 15.5 Estatus Epistémico

| Afirmación | Estatus | Salvedad |
|---|---|---|
| Lema 15.1 (adj=0 para rango≤2) | Probado | Algebraico exacto |
| Escalar → SHO desplazado | Probado | Sin atractor interior en 1D |
| SHO desde inserción de propósito nulo | Probado — Teorema 15.1 | Se requiere $S, A$ nulos |
| Péndulo | Analogía geométrica — GL(4,ℝ) no compacto; se necesita órbita S¹ + acoplamiento gravitatorio | Parte III B4: órbita SO(4) + acoplamiento Ch31 |
| $\Gamma_a = dA$ (sector de curvatura) | Estructural — Proposición 15.3 | Inserción en fibrado: Parte III |
| EM → Maxwell (ambos conjuntos) | Probado — Teorema 15.2 | Sin parcheo de gauge; base lorentziana: Parte III |
| Ausencia de masa del fotón | Consecuencia estructural | Estructura de representación, no simetría impuesta |
| GR linealizada → $\square h = 0$ | Probado — Teorema 15.3 | Solo orden lineal |
| Flujo irrotacional → $\square\phi = 0$ | Probado — Teorema 15.4 | Mismo mecanismo de gauge que el fotón EM |
| Identidad estructural Acústico-EM | Predicción estructural (PR-18) | Falsable mediante comparación de topología de modos |
| Flujo de Stokes → $\partial_t v_i = \nu\nabla^2 v_i$ | Probado — Teorema 15.5 | Aproximado (Re $\to 0$); $\nu_{\mathrm{kin}} = c^2(\rho)/\gamma$ |
| $\gamma$ operacionalizado: $\gamma = c^2(\rho)/\nu_{\mathrm{kin}}$ | Consecuencia derivada | Testable mediante ratios de viscosidad sin Hito 3 |
| Mapeo Re $\leftrightarrow$ $1/\gamma$ | Identificación estructural | Re = $vL\gamma/c^2$; Re $\to 0$ ↔ $\gamma \to \infty$ |
| GR completa, EM con fuentes | Abierto | Requiere Hito 3 (puente de estratos) |
| Onda-partícula como bifurcación $S,A$ | Observación estructural | Análogo clásico; versión cuántica: Parte III |

**El patrón.** Mismo Lagrangiano, misma EOM, cero parámetros nuevos — cinco dominios. El término atractor cuártico desaparece para configuraciones de propósito nulo (lineales) y contribuye exactamente para perturbaciones gravitatorias en $\rho_{\mathrm{GR}}$. El principio de protección de masa ($\Gamma_s$ masivo, $\Gamma_a = dA$ sin masa) es una consecuencia estructural de la descomposición de $\mathrm{GL}(4,\mathbb{R})$.

---

## 15.6 Espectro de Modos — Análisis Lineal (Ch15b)

Linealizar el EOM alrededor de un fondo homogéneo $\Gamma_0 = \sigma \cdot I$ con $\sigma > 0$ produce el operador de masa efectiva:

$$\mathcal{M}_{\Gamma_0}[\delta\Gamma] = \delta\Gamma + \mu\det(\Gamma_0)\left[\mathrm{Tr}(\Gamma_0^{-1}\delta\Gamma)\,\Gamma_0^{-T} - \Gamma_0^{-T}\delta\Gamma^T\Gamma_0^{-T}\right]$$

Para $\Gamma_0 = \sigma I$, los modos se clasifican en tres sectores con autovalores exactos:

| Sector | Modo | Autovalor $\lambda$ |
|---|---|---|
| Traza ($\delta\Gamma \propto I$) | Escalado uniforme | $\lambda_{\mathrm{tr}} = 1 + 3\mu\sigma^2$ |
| Simétrico sin traza | Deformación de forma | $\lambda_{\mathrm{sym}} = 1 - \mu\sigma^2$ |
| Antisimétrico | Campo gauge | $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2$ |

**Clasificación espectral:** $\lambda = 0$ (propagante), $\lambda > 0$ (ligado), $\lambda < 0$ (inestable).

**Punto crítico espectral.** $\lambda_{\mathrm{sym}} = 0$ ocurre en $\sigma^\star = \sqrt{1/\mu} = \rho_{\mathrm{GR}}/\rho$.

**Teorema 15b.1 (Umbral espectral = umbral de creación de materia).** El punto $\sigma^\star$ donde $\lambda_{\mathrm{sym}} = 0$ coincide exactamente con el umbral de creación de materia $\sigma^\star = \rho_{\mathrm{GR}}/\rho$ del Ch14 §14.8.1. Mismo cálculo desde dos perspectivas independientes.

**Proposición 15b.1 (El atractor es la transición de fase).** El atractor $P(\Gamma) \sim \sigma^\star I$ es equivalente, vía rotación $O(4)$, al punto donde el sector simétrico sin traza se hace sin masa — la transición de fase espectral.

**Retrato espectral:**

| Régimen | $\lambda_{\mathrm{tr}}$ | $\lambda_{\mathrm{sym}}$ | $\lambda_{\mathrm{anti}}$ | Física |
|---|---|---|---|---|
| $\sigma < \sigma^\star$ | $> 1$ | $> 0$ | $> 1$ | Todos los modos estables; sin materia |
| $\sigma = \sigma^\star$ | $4$ | $0$ | $2$ | Modo simétrico sin masa = umbral de creación |
| $\sigma > \sigma^\star$ | $> 4$ | $< 0$ | $> 2$ | Inestabilidad simétrica; materia condensada |

**Conexión con los regímenes de Ch15.** El sector antisimétrico tiene $\lambda_{\mathrm{anti}} = 1 + \mu\sigma^2 > 0$ siempre — consistente con la protección de masa de $\Gamma_a = dA$ (ningún modo antisimétrico se hace inestable). El sector simétrico sin traza cruza cero en $\sigma^\star$ — este es el mecanismo dinámico detrás de la bifurcación onda-partícula de la Observación 15.8.

| Afirmación | Estatus | Salvedad |
|---|---|---|
| Operador $\mathcal{M}_{\Gamma_0}$ explícito | Derivado (Lema 15b.1) | Válido para $\Gamma_0$ invertible, $\det > 0$ |
| Autovalores $\lambda_{\mathrm{tr}}, \lambda_{\mathrm{sym}}, \lambda_{\mathrm{anti}}$ | Exactos para $\Gamma_0 = \sigma I$ | Fondo general: problema espectral completo |
| Teorema 15b.1 (umbral espectral = Ch14) | Demostrado | Misma ecuación desde dos direcciones |
| Proposición 15b.1 (atractor = transición) | Demostrado | Para fondo $O(4)$-simétrico |
| Extensión a firma Lorentziana ($\det < 0$) | Abierto | Signo de $\mu\det$ se invierte — Parte III |

---

---

## Cierre: El Programa de Universalidad

El Ch15 demuestra la universalidad del Lagrangiano y la EOM de la GSF a través de cinco dominios físicos: cada dominio asigna atributos $\{S,A,\mathbf{I},\mathbf{R}\}$, impone restricciones sobre $\Gamma$ y recupera las ecuaciones establecidas a partir del mismo Lagrangiano único con cero parámetros nuevos.

Esto cierra la Parte II de la GSF. La Parte III abordará:
- **Hito 3 (Puente de Estratos):** La correspondencia entre las unidades naturales de la GSF y las unidades del SI; cuantización de $\rho$.
- **Dominios extendidos:** Teoría de la información, economía y sistemas vivos — donde no existe un Lagrangiano previo, y las identificaciones estructurales guían nuevas predicciones. Estas se preservan en la lluvia de ideas para el desarrollo futuro a un ritmo impulsado por la validación empírica (no forzado por la estructura narrativa).
- **Cuestiones topológicas:** Geometría de fibrados, extensiones no abelianas y el papel de la estructura de twistores en el formalismo completo.

La universalidad del Lagrangiano clásico de la GSF ha sido establecida. Lo que queda es el refinamiento, la cuantización y el anclaje experimental.
