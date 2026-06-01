# Capítulo 8: El Mapa de Configuración
*Versión condensada — fuente: Cap. 8 del GSF completo*

---

## 8.1 La Pregunta Abierta del Cap. 5

El Cap. 5 estableció la forma estructural de Γ — la matriz de acoplamiento de 4×4/10×10, la descomposición Sim-Antisim y las configuraciones degeneradas — pero dejó una pregunta explícitamente abierta (§5.8):

> *"¿Qué determina el producto interno $\langle\text{attr}_i, \text{attr}_j\rangle$ que define $\Gamma_{ij}$?"*

Hasta que esto se responda: (1) los $\Gamma_{ij}$ son parámetros libres sin dependencia de ξ; (2) el Jacobiano ∂Γ/∂ξ no puede ser computado; (3) la ley de transformación de Γ bajo G(3) no puede ser verificada; (4) la cuestión tensor vs. matriz (Cap. 5 §5.3) no puede ser resuelta.

**El Cap. 8 cierra esta brecha** identificando el producto interno escalar G(3) en el paravector M = S + **A** + **I** + **R** como la métrica estructural natural. El resultado es un mapa de Gram polinomial explícito ξ ↦ Γ(ξ).

---

## 8.2 El Producto Interno G(3) en el Espacio de Atributos

El álgebra G(3) define el producto interno escalar canónico mediante la proyección de grado 0 del producto geométrico:

$$\langle u, v \rangle_{G(3)} := \langle u\tilde{v} \rangle_0$$

| $u$ | $v$ | $\langle u, v \rangle_{G(3)}$ |
|-----|-----|-------------------------------|
| $S$ (grado 0) | $S'$ (grado 0) | $S \cdot S'$ |
| $\mathbf{u}$ (grado 1) | $\mathbf{v}$ (grado 1) | $\mathbf{u} \cdot \mathbf{v}$ |
| $S$ (grado 0) | $\mathbf{v}$ (grado 1) | $0$ |

**Teorema del desajuste de grados:** el producto interno escalar entre elementos de diferentes grados se anula idénticamente — una consecuencia estructural de la filtración de grados de G(3), no una suposición. Esto hace que el sector S esté estructuralmente desacoplado del sector vectorial en Γ_s.

---

## 8.3 La Construcción de Gram: Γ_s(ξ) Explícita

**Definición 8.1 (Mapa de Configuración de Gram).**

$$\boxed{\Gamma_s(\xi) = \begin{pmatrix} S^2 & 0 & 0 & 0 \\ 0 & |\mathbf{A}|^2 & \mathbf{A}\cdot\mathbf{I} & \mathbf{A}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{I} & |\mathbf{I}|^2 & \mathbf{I}\cdot\mathbf{R} \\ 0 & \mathbf{A}\cdot\mathbf{R} & \mathbf{I}\cdot\mathbf{R} & |\mathbf{R}|^2 \end{pmatrix}}$$

Estructura de bloques (teorema del desajuste de grados):
- **[S²]**: autocoherencia de S — desacoplada de los vectores.
- **Bloque 3×3 inferior derecho**: matriz de Gram de {**A**, **I**, **R**} bajo el producto punto en ℝ³.

**Proposición 8.1 (Condición operativa en forma de Gram).** $\Gamma_s(\xi) \succ 0$ si y solo si:
1. $S \neq 0$
2. $\{\mathbf{A}, \mathbf{I}, \mathbf{R}\}$ son linealmente independientes en $\mathbb{R}^3$

Esto es estrictamente más fuerte que **I** ∦ **R** (Campo operativo) — la definición positiva implica Campo operativo, pero no a la inversa.

---

## 8.4 La Parte Antisimétrica: Γ_a(ξ)

El acoplamiento antisimétrico utiliza el producto exterior (wedge) de G(3). En la **forma expandida 10×10**, el acoplamiento natural entre dos vectores **u**, **v** ∈ ℝ³ es:

$$[\mathbf{u} \wedge \mathbf{v}]_\times = \tfrac{1}{2}(\mathbf{u}\mathbf{v}^T - \mathbf{v}\mathbf{u}^T) \in \mathfrak{so}(3)$$

que, mediante el isomorfismo de Levi-Civita, corresponde exactamente a **u** × **v**.

**El bloque de Campo (Field)** — recuperación exacta:
$$(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R}} = [\mathbf{I} \wedge \mathbf{R}]_\times \;\longleftrightarrow\; \mathbf{I} \times \mathbf{R} = \mathbf{Field}$$

El Campo está algebraicamente *codificado* en el bloque antisimétrico (I,R) — de forma exacta, no parametrizada.

**El bloque de Fuerza (Force)** — codificación directa:
$$(\Gamma_a^{(10)})_{S\mathbf{A}} = S\mathbf{A} = \mathbf{Force}$$

Fuerza = S**A** aparece directamente como el bloque antisimétrico fuera de la diagonal (S, **A**).

**Forma abstracta 4×4** (entradas escalares mediante normas de Frobenius de los bloques 3×3 — pierde orientación, conserva topología):

$$\Gamma_a(\xi) = \begin{pmatrix} 0 & S|\mathbf{A}| & S|\mathbf{I}| & S|\mathbf{R}| \\ -S|\mathbf{A}| & 0 & |\mathbf{A}\times\mathbf{I}| & |\mathbf{A}\times\mathbf{R}| \\ -S|\mathbf{I}| & -|\mathbf{A}\times\mathbf{I}| & 0 & |\mathbf{I}\times\mathbf{R}| \\ -S|\mathbf{R}| & -|\mathbf{A}\times\mathbf{R}| & -|\mathbf{I}\times\mathbf{R}| & 0 \end{pmatrix}$$

*(El contenido estructural completo reside en la forma 10×10; la 4×4 es un resumen escalar).*

---

## 8.5 El Mapa Completo Γ(ξ)

**Definición 8.2 (Mapa de Configuración).**

$$\Gamma: \mathcal{V} \to \mathrm{Sym}^+(4) \oplus \mathfrak{so}(4), \qquad \xi \mapsto \Gamma_s(\xi) + \Gamma_a(\xi)$$

- **Suavidad:** las entradas son polinomios de grado ≤ 2 en las componentes de ξ → $\Gamma \in C^\infty(\mathcal{V})$. No es una suposición — es una consecuencia. Confirma el Cap. 9 §9.2.
- **G(3)-equivarianza:** bajo una rotación $g$ de G(3), con $J_g = \mathrm{diag}(1, R_g, R_g, R_g)$:
$$\Gamma_s(g\cdot\xi) = J_g^T\,\Gamma_s(\xi)\,J_g$$
Esta es la ley de transformación covariante de un tensor $(0,2)$. La representación explícita es $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3}) \in O(10)$ — ortogonal por construcción. Confirma el Postulado 10.1 del Cap. 10 y el Supuesto 23.1 del Cap. 11.

---

## 8.6 El Jacobiano DΓ(ξ)

Entradas polinomiales → el Jacobiano es lineal en ξ (explícitamente computable). Bloques clave no nulos:

$$\frac{\partial(\Gamma_s)_{00}}{\partial S} = 2S, \quad \frac{\partial(\Gamma_s)_{12}}{\partial A_k} = I_k, \quad \frac{\partial(\Gamma_s)_{12}}{\partial I_k} = A_k$$

$$\frac{\partial(\Gamma_a^{(10)})_{S\mathbf{A}}}{\partial S} = \mathbf{A}, \quad \frac{\partial(\Gamma_a^{(10)})_{\mathbf{I}\mathbf{R},jk}}{\partial I_l} = \tfrac{1}{2}(\delta_{jl}R_k - \delta_{kl}R_j)$$

La estructura dispersa completa refleja la topología de acoplamiento de la UdC. Ahora disponible para: descomposición de fuerza por regla de la cadena (Cap. 11 §11.5), movilidad inducida $M_\Gamma = D\Gamma \cdot M \cdot D\Gamma^T$ (Cap. 11 §11.5).

---

## 8.7 Verificación del Criterio de Inyectividad Estructural (SIC)

**Proposición 8.2 (SIC en configuraciones operativas).** En cualquier $\xi^*$ operativo ($S^* \neq 0$, $\{\mathbf{A}^*, \mathbf{I}^*, \mathbf{R}^*\}$ linealmente independientes):

$$\mathrm{rank}(D\Gamma(\xi^*)) = 10 = \dim(\mathcal{V})$$

**Corolario 8.1.** El SIC del Cap. 11 §11.5 se cumple para todas las UdC operativas bajo el mapa de Gram. Se deduce la unicidad local de $\xi^*$ como preimagen de $\Gamma^*$.

---

## 8.8 Resolución: ¿Tensor o Matriz?

| Objeto | Estatus | Ley de transformación |
|--------|--------|--------------------|
| $\Gamma_s(\xi)$ | **Tensor** covariante $(0,2)$ en $\mathcal{V}$ bajo G(3) | $\Gamma_s \mapsto J_g^T \Gamma_s J_g$ |
| $\Gamma_a^{(10)}(\xi)$ | **Tensor** antisimétrico $(0,2)$ bajo SO(3) | $\Gamma_a \mapsto J_g^T \Gamma_a J_g$ |
| $\Gamma(\xi)$ total | **Tensor** $(0,2)$ en $\mathcal{V}$ bajo G(3) | $\Gamma \mapsto J_g^T \Gamma J_g$ |
| Forma abstracta 4×4 | Resumen de acoplamiento escalar — no tensorial en general | — |

**Resolución (Cap. 5 §5.3):** "tensor de configuración" es correcto en la forma expandida 10×10. La ley de transformación requerida por el Postulado 10.1 del Cap. 10 queda establecida aquí — no solo postulada.

---

## 8.9 Lo que este Mapa Aporta a la Parte II

### Consistencia retrospectiva (Cap. 1–Cap. 5)
- **Fuerza** = S**A** codificada en el bloque antisimétrico (S,**A**) ✓
- **Campo** = **I**×**R** codificado exactamente vía Levi-Civita en el bloque (I,R) ✓
- **Γ_s ≻ 0** ↔ S ≠ 0, {**A**,**I**,**R**} lin. independientes — consistente con Cap. 5 Def. 5.2 ✓

### Entregables prospectivos para Cap. 9–Cap. 11
- **Suavidad Cap. 9 §9.2:** no es una suposición — mapa polinomial → $C^\infty$ ✓
- **Ley de transformación Cap. 10 Postulado 10.1:** $\Gamma_s \mapsto J_g^T\Gamma_s J_g$ establecida aquí ✓
- **Supuesto 23.1 Cap. 11:** $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ ortogonal — verificado aquí ✓
- **Jacobiano Cap. 11 §11.5:** $D\Gamma(\xi)$ computado explícitamente en §8.6 ✓
- **SIC Corolario 11.1 Cap. 11:** verificado por la Proposición 8.2 ✓

### Lo que el mapa NO cierra
- Coeficientes $\kappa, \mu, \nu$ de $P(\Gamma)$ — dependen del potencial, no del mapa.
- $P(\Gamma)$ explícito — aún abierto.
- Inyectividad global — ambigüedad $\mathbb{Z}_2$ identificada (§8.10); análisis completo abierto.

---

## 8.10 Preguntas Abiertas

- **Inyectividad global (ambigüedad $\mathbb{Z}_2$):** $\Gamma_s$ es par bajo la inversión de signo global $(\mathbf{A},\mathbf{I},\mathbf{R}) \mapsto (-\mathbf{A},-\mathbf{I},-\mathbf{R})$; $\Gamma_a$ es impar — la parte antisimétrica resuelve el $\mathbb{Z}_2$ al nivel de la Γ completa. El análisis completo sobre $D_\xi(\rho)$ permanece abierto.

- **Extensión pseudo-riemanniana:** el producto interno G(3) es euclidiano. En valores extremos de ρ, la métrica de atributos puede requerir un análogo pseudo-riemanniano (indefinido). Esta generalización se pospone para trabajos futuros.

- **Convención de signos 4×4 para $\Gamma_a$:** las magnitudes $|\mathbf{u}\times\mathbf{v}|$ pierden la orientación. El seudoescalar de G(3) $I_3 = \mathbf{e}_1\mathbf{e}_2\mathbf{e}_3$ proporciona una orientación natural, reemplazando $|\mathbf{u}\times\mathbf{v}|$ con un escalar con signo — pero esto requiere un marco de referencia canónico derivable del estado de la UdC.

- **Acoplamiento intersectorial en $\Gamma_a$:** los bloques $[\mathbf{A}\wedge\mathbf{I}]_\times$ y $[\mathbf{A}\wedge\mathbf{R}]_\times$ codifican acoplamientos más allá de la Fuerza y el Campo. La interpretación fenomenológica es una correspondencia abierta (candidata para trabajos posteriores).

---

## 8.11 Resumen de Estatus

| Pregunta abierta (Cap. 5 §5.8) | Estatus tras Cap. 8 |
|---------------------------|-------------------|
| ¿Qué determina $\langle\text{attr}_i, \text{attr}_j\rangle$? | **Cerrado** — producto interno escalar G(3) → mapa de Gram |
| Ley de transformación de Γ | **Establecida** — $\Gamma \mapsto J_g^T\Gamma J_g$ bajo G(3) |
| Tensor vs. matriz | **Resuelto** — tensor en 10×10; resumen escalar en 4×4 |
| Jacobiano $\partial\Gamma/\partial\xi$ | **Computado** — mapa lineal explícito de entradas polinomiales |
| SIC (Cap. 11 Corolario 11.1) | **Verificado** — Proposición 8.2: se cumple en todo $\xi^*$ operativo |
| Suavidad (Cap. 9 §9.2) | **Derivada** — mapa polinomial → $C^\infty$ (no es una suposición) |
| Ley de transformación Postulado 10.1 | **Establecida** — no postulada |
| Ortogonalidad Supuesto 23.1 | **Establecida** — $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$ verificada |
| Inyectividad global | **Parcial** — $\mathbb{Z}_2$ identificada; análisis completo abierto |

---

*Fin del Capítulo 8 (condensado)*
