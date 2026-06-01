# Capítulo 10: El Lagrangiano Estructural
*Versión condensada — fuente: Cap. 10 del GSF completo*

---

## 10.1 El Programa

El Cap. 9 presentó la ley de evolución $f(\xi,\rho)$ y la función de propósito $P$ como postulados. El Cap. 10 aborda los orígenes variacionales de estos objetos en dos partes estructuralmente distintas:

- **Sector disipativo** (§10.3): $\dot\xi = -M\nabla P$, $M = \Gamma_s^{-1}/\gamma$ — *derivado* del Lagrangiano estructural + disipación de Rayleigh en el límite sobreamortiguado.
- **Sector reactivo** (§10.3.2): $-A\nabla P$ — *no* producido por el Lagrangiano; introducido como el **postulado mínimo de Onsager-Casimir** para la dinámica rotacional.

"Cierra la estructura variacional disipativa" no significa completitud formal: (1) la forma explícita de $P(\Gamma)$ permanece abierta; (2) la clase de Lagrangianos admisibles no está totalmente clasificada; (3) el sector antisimétrico es postulado.

**Tensiones cerradas:** T3 (estructura de $f$, parcial), T6 (selección de Lyapunov), T7 (cadena de derivación).

**Resumen del estatus epistémico:** el sector disipativo y la selección de Lyapunov son derivados (límite sobreamortiguado); el sector reactivo es postulado; los coeficientes $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$, $\gamma(\rho)$ están pendientes de una $P(\Gamma)$ explícita.

---

## 10.2 La Acción Estructural

### 10.2.1 Requisitos Mínimos

Tres requisitos sobre $\mathcal{L}(\xi, \dot\xi)$:

1. **Invariancia G(3)** — escalar bajo el grupo de simetría de la UoC.
2. **Término cinético canónico** — cuadrático en $\dot\xi$ (orden más bajo, problema de Cauchy bien planteado).
3. **Consistencia de la métrica de acoplamiento** — métrica cinética $K_{ij}$ inducida por la $\Gamma_s$ del Cap. 5.

### 10.2.2 El Lagrangiano Estructural

$$\boxed{\mathcal{L}(\xi, \dot{\xi}) = \frac{1}{2}\,\dot{\xi}^T \Gamma_s(\xi)\,\dot{\xi} - P\!\left(\Gamma[\xi]\right)}$$

- $\Gamma_s(\xi)$: métrica cinética (parte simétrica de la matriz de configuración del Cap. 5).
- $P(\Gamma[\xi])$: potencial estructural (función de propósito, Cap. 9 §9.5).
- Acción: $\mathcal{A}[\xi] = \int \mathcal{L}\,dt$ (notación $\mathcal{A}$ para evitar colisión con $S$ = Singularidad).

Esta es la **elección canónica mínima al orden más bajo** — existen términos cruzados adicionales invariantes ante G(3) y términos cinéticos de orden superior tipo Born-Infeld, pero se excluyen. La clase admisible de Lagrangianos no está totalmente clasificada.

---

## 10.3 Ecuaciones de Euler-Lagrange y el Límite Sobreamortiguado

### 10.3.1 Las Ecuaciones de Euler-Lagrange Completas

**Postulado 10.1 (Γ_s como Métrica de Riemann).** $\Gamma_s(\xi)$ se promueve a una métrica de Riemann definida positiva en la variedad de estados. De los tres requisitos:
1. **Ley de transformación**: $\Gamma_s \mapsto J^T\Gamma_s J$ bajo $G(3)$ — **derivada en Cap. 8 §8.8**, no es una suposición.
2. **Suavidad**: $\Gamma \in C^\infty(\mathcal{V})$ — **derivada en Cap. 8 §8.5** (el mapa de Gram es polinómico), no es una suposición.
3. **Elección de la conexión** *(postulado genuino)*: Levi-Civita (sin torsión, compatible con la métrica) — elección mínima.

Las ecuaciones de Euler-Lagrange dan la **ecuación geodésica estructural con forzamiento**:

$$\nabla_{\dot\xi}\dot\xi = -\operatorname{grad}_{\Gamma_s} P$$

En coordenadas: $\ddot\xi^i + \Gamma^i_{jk}\dot\xi^j\dot\xi^k = -(\Gamma_s^{-1})^{ij}\partial_j P$, donde $\Gamma^i_{jk}$ son los símbolos de Christoffel de $\Gamma_s$ (distintos de la matriz de configuración $\Gamma$ — ver nota de notación en §10.5.2).

### 10.3.2 El Límite Sobreamortiguado

Función de disipación de Rayleigh: $\mathcal{R} = \frac{\gamma}{2}\dot\xi^T\Gamma_s\dot\xi$, añadiendo la fuerza disipativa $-\gamma\Gamma_s\dot\xi$.

**Argumento de escala:** los términos de Christoffel escalan como $O(1/\gamma^2)$, la disipación como $O(1/\gamma)$ — la relación $O(1/\gamma)\to 0$ cuando $\gamma\to\infty$. Por lo tanto, en el límite sobreamortiguado:

$$\boxed{\dot{\xi} = -M(\rho, \xi)\,\nabla_\xi P, \qquad M = \frac{1}{\gamma(\rho)}\,\Gamma_s^{-1}(\xi)} \qquad \text{(derivado, límite de Rayleigh sobreamortiguado)}$$

**Extensión de Onsager-Casimir (postulada):**

$$\boxed{\dot{\xi} = -(M + A)\,\nabla_\xi P} \qquad \text{(postulado)}$$

$A^T = -A$ — parte reactiva. Genera movimiento rotacional en los conjuntos de nivel de $P$ sin descenso de $P$. Requerido para explicar el acoplamiento $\mathbf{R}\times\nabla_\mathbf{I}P$ del Cap. 9 §9.4; no es producido por la estructura Lagrangiano + Rayleigh.

---

## 10.4 La Selección de Lyapunov (T6 Cerrada)

**Teorema 10.1 (Función de Lyapunov Primaria).** *Hipótesis:* (H1) $M \succ 0$ (se cumple por $\Gamma_s \succ 0$, $\gamma > 0$); (H2) $f$ localmente Lipschitz; (H3) $D_\xi(\rho)$ compacto (Cap. 9 Prop 9.1a H1) o $P$ coercitivo.

Bajo $\dot\xi = -(M+A)\nabla P$:

$$\frac{dP}{dt} = -\nabla_\xi P^T M\,\nabla_\xi P = -\frac{1}{\gamma}\|\nabla_\xi P\|^2_{\Gamma_s^{-1}} \leq 0$$

La contribución antisimétrica se anula: $x^T A x = 0$ para todo $x$ cuando $A^T = -A$. Descenso estricto fuera de $\mathcal{C} = \{\nabla P = 0\}$. Por LaSalle, las trayectorias convergen al subconjunto invariante más grande de $\mathcal{C}$; la convergencia a $\xi^*$ específicamente requiere un mínimo estricto aislado (genérico bajo Cap. 9 Prop 9.1a).

**Nota sobre la circularidad constructiva:** la dinámica está *construida* de modo que $\dot P \leq 0$ — este es el ansatz de flujo de gradiente. El Teorema 10.1 establece la tasa de descenso específica y la convergencia de LaSalle, no la propiedad de Lyapunov como una verificación independiente.

**Resolución candidata (Cap. 9 §9.6):**
- $V(\Gamma) = \|\Gamma - \Gamma^*\|_F^2$: proxy local para $P$ cerca de $\xi^*$ (válido cuando el Hessiano de $P$ es isotrópico).
- $V(\xi) = \alpha|\text{Fuerza}|^2 + \beta|\text{Campo}|^2$: diagnóstico de intensidad estructural — **no** es una función de Lyapunov.
- Jerarquía: $P(\xi)$ (Lyapunov global) $\supset$ $V(\Gamma)$ (proxy local) $\supset$ $V(\xi)$ (solo diagnóstico).

---

## 10.5 Simetría G(3) y los Términos No Lineales del Cap. 9 §9.4 (T3 Parcial)

### 10.5.1 Expansión de Taylor de f

Cerca de $\xi^*$: $(\nabla_\xi P)_i = H_{ij}\delta\xi_j + T_{ijk}\delta\xi_j\delta\xi_k + \mathcal{O}(\delta\xi^3)$. La invariancia G(3) restringe los tensores admisibles $H$, $T$.

### 10.5.2 Términos No Lineales G(3)-Admisibles

**Desambiguación de notación:**
- $\mathbf{A} \in \mathbb{R}^3$: Agencia (negrita, atributo de estado intrínseco).
- $A(\rho,\xi)$: Matriz antisimétrica de Onsager-Casimir (cursiva, operador sobre $\nabla P$).
- $\Gamma^i_{jk}$: Símbolos de Christoffel de la conexión de Levi-Civita de $\Gamma_s$ — distinto de la matriz de configuración $\Gamma$.

**Observación sobre G(3) y la dimensión.** Los productos vectoriales $\mathbf{u}\times\mathbf{v}$ son SO(3)-equivariantes, y cualquier operador antisimétrico $3\times3$ es $x\mapsto\Omega\times x$ — ambas propiedades son **específicas de tres dimensiones** vía $\mathfrak{so}(3)\cong\mathbb{R}^3$. Los términos G(3)-admisibles a continuación son características 3D.

Términos cuadráticos G(3)-admisibles en $\nabla_\mathbf{I}P$:

| Término | Tipo G(3) |
|------|-----------|
| $\mathbf{R}\times\mathbf{I}$ | Vector |
| $\mathbf{A}\times\mathbf{I}$ | Vector |
| $S(\mathbf{A}\times\mathbf{R})$ | Vector |
| $|\mathbf{I}|^2\mathbf{I}$ | Vector (auto-acoplamiento cúbico) |
| $(\mathbf{I}\cdot\mathbf{R})\mathbf{R}$ | Vector |

El **ansatz del Cap. 9** $\dot{\mathbf{I}} = \alpha_\mathbf{I}(\mathbf{R}\times\mathbf{I}) + \beta_\mathbf{I}|\mathbf{I}|^2\mathbf{I}$ selecciona dos:

- **$\mathbf{R}\times\nabla_\mathbf{I}P$**: de la parte antisimétrica (reactiva) $A\nabla P$. En 3D: $A_\mathbf{I}\,x = \Omega\times x$; la elección mínima invariante ante G(3) es $\Omega = \alpha_\mathbf{I}\mathbf{R}$ — $\mathbf{R}$ es el vector de acoplamiento ambiental, preservando la estructura Campo = $\mathbf{I}\times\mathbf{R}$. Cerca del equilibrio: $\nabla_\mathbf{I}P \propto \mathbf{I}$, por lo que el término completo se reduce a $\alpha_\mathbf{I}\mathbf{R}\times\mathbf{I}$. En dim $\neq 3$, este acoplamiento requeriría un bivector/2-forma.

- **$|\mathbf{I}|^2\mathbf{I}$**: de la no linealidad de $\nabla P$ — término cúbico principal en la expansión de Taylor; presente en la parte disipativa $M\nabla P$, no requiere $A\neq 0$.

**Abierto:** coeficientes $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$, $A(\rho,\xi)$ explícita, términos G(3)-invariantes adicionales — todos requieren $P(\Gamma)$.

---

## 10.6 El Lagrangiano en Términos de Γ

$$\mathcal{L}(\Gamma, \dot\Gamma) = \frac{1}{2}\text{Tr}(\dot\Gamma^T G_\Gamma\,\dot\Gamma) - P(\Gamma)$$

$G_\Gamma$ = métrica inducida en el espacio $\Gamma$. El Jacobiano $J_\Gamma = \partial\Gamma/\partial\xi$ no es cuadrado ($d\geq n$), por lo que la condición de consistencia $J_\Gamma^T G_\Gamma J_\Gamma = \Gamma_s$ tiene infinitas soluciones.

**Ansatz de clausura isotrópica efectiva:** $G_\Gamma \propto \Gamma_s^{-1}$ — la elección más conservadora (máxima entropía), que no introduce asimetría adicional más allá de lo que suministra $\Gamma_s$ y asume que no hay una dirección preferida en el espacio normal de $J_\Gamma$. Esta es una identificación efectiva entre diferentes tipos de tensores (no una igualdad tensorial). Da en el límite sobreamortiguado: $\dot\Gamma \approx -\frac{1}{\gamma}\nabla_\Gamma P$.

---

## 10.7 Las Constantes Estructurales: ρ y γ

Tiempo de relajación linealizado cerca de $\xi^*$: $\tau_\text{relax} \sim \gamma/\lambda_\text{min}(\Gamma_s^{-1}H)$.

**Ansatz de escala fenomenológico** $\gamma \sim \rho\|\Gamma_s\|$ a partir de dos heurísticas:
1. Mayor $\rho$ → relajación más lenta *(hipótesis estructural, no derivada)*.
2. Amortiguamiento proporcional de Rayleigh: $\gamma\propto\|\Gamma_s\|$ (analogía de rigidez — correspondencia heurística).

Con este ansatz: las UoCs de nivel ego ($\rho$ grande) se relajan lentamente *(candidato)*; las UoCs de nivel alma ($\rho\to 0$) se relajan rápidamente *(candidato)*. La identificación de los niveles de $\rho$ con ego/alma se establece en el Cap. 11 §11.7, no aquí.

**Observación (términos de gradiente de amortiguamiento ausentes):** si $\gamma$ depende de $\xi$ a través de $\|\Gamma_s(\xi)\|$, una derivación completa generaría correcciones $\frac{\partial\gamma}{\partial\xi}\dot\xi$. Estas son $O(1/\gamma)$ en relación con la disipación y se descartan consistentemente con el límite sobreamortiguado.

**Esto sigue siendo un ansatz de escala fenomenológico.** La constante de proporcionalidad y la forma funcional completa requieren el Lagrangiano explícito.

### 10.7.1 Tabla de Estatus Epistémico

| Resultado | Estatus |
|--------|--------|
| $\dot\xi = -M\nabla P$, $M = \Gamma_s^{-1}/\gamma$ | **Derivado** (límite de Rayleigh sobreamortiguado, orden principal en $1/\gamma$) |
| $P(\xi)$ función de Lyapunov primaria | **Derivado** ($\dot P = -\nabla P^T M\nabla P\leq 0$, $M\succ 0$) |
| Convergencia a $\mathcal{C}$ | **Derivado** (LaSalle, bajo H1–H3) |
| Convergencia a $\xi^*$ específicamente | **Condicional** (mínimo estricto aislado, genérico por Cap. 9 Prop 9.1a) |
| $A$ antisimétrica (parte reactiva) | **Postulado** (mínimo de Onsager-Casimir) |
| Término rotacional $\mathbf{R}\times\nabla_\mathbf{I}P$ | **Admisible por simetría** (G(3) + antisimetría 3D; no derivado de $P$) |
| Auto-interacción $|\mathbf{I}|^2\mathbf{I}$ | **Admisible por simetría** (no lineal G(3)-invariante principal en $\nabla_\mathbf{I}P$) |
| $G_\Gamma = \Gamma_s^{-1}$ en el espacio $\Gamma$ | **Aproximación de trabajo** (ansatz de clausura isotrópica) |
| $\gamma\sim\rho\|\Gamma_s\|$ | **Ley empírica** (PR-24, 2026-05-31): $\gamma \propto \rho$ confirmado en aire sobre 5 décadas a 0.1% de precisión; con $c^2(\rho)$ saturado (E6×E1). Derivación formal desde disipación de Rayleigh queda para Part III. |
| Forma del Lagrangiano $\|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu\det(\Gamma)$ | **Derivado en Parte II** (Cap. 13: unicidad de Frobenius + condición de atractor + ausencia de fantasmas) |
| $\kappa = -1$ | **Derivado en Parte II** (Cap. 13: la ausencia de fantasmas requiere $\kappa < 0$; $\kappa = -1$ por normalización de Frobenius) |
| $\mu(\rho) = 2(\rho/\rho_{\mathrm{GR}})^2$ | **Derivado en Parte II** (Cap. 14: ley de escala T1 + anclaje del gravitón sin masa) |
| $P(\Gamma)P(\Gamma)^T \propto I$ en el atractor | **Derivado en Parte II** (Cap. 13 Teo 13.2 + Cap. 19 Lema 19.1: máximo único de $\mathcal{C}(\Gamma)$) |
| Función de Lyapunov homeodinámica | **Derivado en Parte II** (Cap. 19 Teo 19.1: $V = \|\dot\Gamma\|^2 + (1-\mathcal{C})^2$; reemplaza a T6 aquí) |

---

## 10.8 Cerrando las Tensiones

| Tensión | Estatus |
|---------|--------|
| **T3** — forma de $f$ | **Parcialmente cerrada**: $f = -(M+A)\nabla P$; $M$ derivado; $A$ postulado; $\mathbf{R}\times\nabla_\mathbf{I}P$ y $|\mathbf{I}|^2\mathbf{I}$ son G(3)-admisibles. Coeficientes pendientes de $P(\Gamma)$. |
| **T6** — selección de Lyapunov | **Cerrada**: $P(\xi)$ primaria; $V(\Gamma)$ proxy local; $V(\xi)$ solo diagnóstico. |
| **T7** — cadena de derivación | **Estructuralmente cerrada**: Lagrangiano → $f$ (§10.3.2) → Lyapunov (§10.4). Coeficientes pendientes de $P$. |

---

## 10.9 Preguntas Abiertas

- **$P(\Gamma)$ explícita**: desarrollada en el Cap. 11 a partir de restricciones polinómicas G(3)-invariantes; coeficientes $\kappa=-1$, $\mu(\rho)$ derivados en la Parte II (Caps. 13–14).
- **Régimen inercial**: la ecuación completa de segundo orden se pospone para trabajos futuros.
- **$\Gamma_s$ dependiente de la posición**: las correcciones de Christoffel pueden ser significativas cerca de bifurcaciones estructurales.
- **Derivación de $\gamma(\rho)$**: la constante de proporcionalidad requiere el Lagrangiano explícito desde primeros principios.

---

*Fin del Capítulo 10 (condensado)*
