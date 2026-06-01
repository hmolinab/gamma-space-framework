# Capítulo 13: El Lagrangiano Estructural
*Versión condensada — Parte II*

---

## 13.1 El Programa

El Cap. 10 presentó un Lagrangiano "canónico mínimo", calificado explícitamente como un punto de partida, no como una derivación. Este capítulo deriva el Lagrangiano en cuatro etapas:

1. **§13.2–13.3** — Identificar la base de invariantes polinómicos admisibles bajo S1–S2 y restricciones de minimalidad.
2. **§13.4** — Seleccionar el término cinético mediante la condición de isotropía → fuerza $\kappa = -1$.
3. **§13.5** — Determinar $\mu(\rho)$ a partir de la condición de equilibrio estructural (autoconsistencia).
4. **§13.6** — Verificar la ausencia de fantasmas (clásica, signatura euclidiana).

Resultado: $\mathcal{L} = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma)$ sin parámetros libres, dada la condición de contorno gravitacional $c(\rho_{\mathrm{GR}}) = 1$.

---

## 13.2 Simetrías y Base de Invariantes

### Jerarquía de simetría

Tres niveles distintos, mantenidos por separado en todo momento:

| Nivel | Grupo | Rol |
|---|---|---|
| Físico | S1–S2 | Simetrías reales del Lagrangiano GSF |
| Clasificación | Conjugación completa | Herramienta para enumerar invariantes polinómicos (Cayley-Hamilton opera aquí) |
| Isotropía | $\mathrm{O}(4)\times\mathrm{O}(4)$ | Argumento de suficiencia para la selección de Frobenius |

El Lagrangiano es invariante solo bajo S1–S2. Los grupos más grandes aparecen como instrumentos analíticos.

### Simetrías físicas

**S1 (Conjugación ortogonal en $\{A,\mathbf{I},\mathbf{R}\}$).** $\Gamma \mapsto O\Gamma O^T$, $O \in \mathrm{SO}(3) \subset \mathrm{O}(4)$. Preserva $\mathrm{tr}(\Gamma^k)$ y $\det(\Gamma)$.

**S2 (Paridad: $\Gamma \mapsto -\Gamma$).** Elimina invariantes de grado impar ($\mathrm{tr}(\Gamma)$, $\mathrm{tr}(\Gamma^3)$). *Condicional al dominio:* válido para sistemas físicos libres de fuentes; no es universal para UoCs biológicas/económicas, que poseen asimetría intrínseca. El Lagrangiano universal mínimo asume S2.

### Base de invariantes

**Lema 13.1 (Invariantes cuadráticos).** Bajo S1, usando $\mathrm{tr}(\Gamma_s\Gamma_a) = 0$ de forma idéntica (álgebra lineal, no se requiere simetría física):
$$I_1 = \|\Gamma_s\|_F^2 - \|\Gamma_a\|_F^2 = \mathrm{tr}(\Gamma^T\Gamma), \qquad I_2 = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2 = \mathrm{tr}(\Gamma^2)$$

**Lema 13.2 (Invariante cuártico).** Cayley-Hamilton para matrices $4\times4$: $\mathrm{tr}(\Gamma^4)$ depende de $\{\mathrm{tr}(\Gamma), \mathrm{tr}(\Gamma^2), \mathrm{tr}(\Gamma^3), \det(\Gamma)\}$. La paridad S2 elimina $\mathrm{tr}(\Gamma)$ y $\mathrm{tr}(\Gamma^3)$. La base par bajo paridad que sobrevive en grado $\leq 4$ es:
$$\{I_1,\; I_2,\; \det(\Gamma)\}$$

**Observación 13.1 (Completitud bajo restricciones).** Esta base es completa bajo: (a) el grupo de conjugación ampliado utilizado para la clasificación, (b) el desacoplamiento de sectores (sin $\mathrm{tr}(\Gamma_s^2\Gamma_a^2)$ o términos mixtos similares), y (c) minimalidad (grado $\leq 4$). Los puntos (b) y (c) son postulados estructurales, no consecuencias de S1–S2 por sí solas. La unicidad se da *dentro de la clase mínima desacoplada*.

---

## 13.3 El Lagrangiano Admisible General

Bajo la normalización $\alpha_1 + \alpha_2 = 1$ con $\kappa := -\alpha_1 + \alpha_2$:
$$\mathcal{L} = \|\dot\Gamma\|_F^2 + \kappa\,\mathrm{tr}(\dot\Gamma_a^2) - \|\Gamma\|_F^2 - \kappa\,\mathrm{tr}(\Gamma_a^2) - \mu\,\det(\Gamma)$$

Tres parámetros libres a priori: $\alpha_1, \alpha_2, \mu$ (o equivalentemente: la escala global, $\kappa$, $\mu$). Dos condiciones fijan $\kappa$; una condición de autoconsistencia fija $\mu$.

*Notación:* $\kappa$ aquí es el peso del sector antisimétrico (finalmente $= -1$). Es distinto de la $\kappa_{\mathrm{GR}} = 8\pi G/c^4$ de Einstein.

---

## 13.4 Frobenius fija $\kappa = -1$

**Teorema 13.1 (Frobenius como término cinético isotrópico mínimo).** Bajo S1–S2 únicamente, el término cinético admite una familia de dos parámetros $a\|\dot\Gamma_s\|_F^2 + b\|\dot\Gamma_a\|_F^2$. El **postulado de isotropía** ($a = b$, sin peso de sector preferente) selecciona $a = b = 1$, es decir, la métrica de Frobenius:
$$T = \mathrm{tr}(\dot\Gamma^T\dot\Gamma) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$

Esto obliga a $\alpha_1 = 1$, $\alpha_2 = 0$, $\kappa = -1$.

Hecho algebraico clave: para una $\Gamma_a$ antisimétrica, los autovalores son pares puramente imaginarios $\pm i\lambda_k$, por lo que $\mathrm{tr}(\Gamma_a^2) = -2\sum_k\lambda_k^2 \leq 0$, resultando en $\mathrm{tr}(\dot\Gamma_a^T\dot\Gamma_a) = -\mathrm{tr}(\dot\Gamma_a^2) = \|\dot\Gamma_a\|_F^2 \geq 0$.

**Nota sobre EM.** Frobenius da $\|\Gamma_a\|_F^2 = \mathbf{E}^2 + \mathbf{B}^2$ (Euclidiano). El EM estándar requiere $\mathbf{E}^2 - \mathbf{B}^2$ (Lorentziano). El Lagrangiano GSF es una *restricción de consistencia* con la estructura EM, no todavía una derivación. La signatura lorentziana se pospone a la Parte III.

---

## 13.5 La Condición de Atractor Fija $\mu$ de Manera Autoconsistente

### 13.5.1 Equilibrio Estructural

$P(\Gamma)$ es el **equilibrio** estructural — el mínimo de la función de propósito. En el sistema conservativo es un centro (Liouville: no hay atractores en dinámicas que preservan el volumen); se convierte en un atractor en el régimen disipativo ($\gamma > 0$). La condición de punto crítico es:

$$\frac{\partial\mathcal{L}}{\partial\Gamma}\bigg|_{P(\Gamma)} = 0 \implies -2P - \mu\det(P)\cdot P^{-T} = 0$$

Multiplicando por la derecha por $P^T$:
$$\boxed{P(\Gamma)P(\Gamma)^T = -\frac{\mu}{2}\det(P(\Gamma))\cdot\mathbf{1}_4}$$

**Proposición 13.1.** El equilibrio satisface $P(\Gamma)P(\Gamma)^T \propto \mathbf{1}_4$ — todos los valores singulares son iguales. Esto es una **consecuencia** de la condición de extremo, no un postulado. Implica que la UoC se acopla por igual a todas las direcciones de salida en el equilibrio estructural.

### 13.5.2 Derivación de $\mu$ por Autoconsistencia

Escribamos $P(\Gamma)P(\Gamma)^T = \lambda\mathbf{1}_4$ con $\lambda = -\tfrac{\mu}{2}\det(P)$.

**Paso 1 (LHS):** $\det(PP^T) = \det(P)^2$

**Paso 2 (RHS):** $\det(\lambda\mathbf{1}_4) = \lambda^4 = \left(\frac{\mu}{2}\right)^4\!\det(P)^4$

**Paso 3 (Igualar, dividir por $\det(P)^4 > 0$):** $\det(P)^{-2} = \left(\frac{\mu}{2}\right)^4$, por lo tanto $\det(P) = \frac{4}{\mu^2}$.

**Paso 4:** Definamos $c(\rho) := \det(P(\Gamma|\rho))$:
$$c(\rho) = \frac{4}{\mu(\rho)^2} \implies \boxed{\mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

**Teorema 13.2 (Determinación de $\mu$ por autoconsistencia).** Esta es una **condición de punto fijo**: $P(\Gamma)$ depende de la dinámica (que contiene a $\mu$), y $\mu$ se extrae de $\det(P(\Gamma))$. La derivación cierra el círculo de forma autoconsistente dentro de la estructura declarada del Lagrangiano. No es una derivación independiente de $\mu$ desde primeros principios.

**Observación 13.5 (Condición de contorno gravitacional).** $\mu(\rho)$ requiere un anclaje de calibración. La RG lo proporciona: la propagación del gravitón sin masa obliga a $\mu(\rho_{\mathrm{GR}}) = 2$, por lo tanto $c(\rho_{\mathrm{GR}}) = 1$. Esta es una **condición de contorno gravitacional** — la escala GSF se calibra contra la realidad física en un nivel de referencia. No es un ajuste de parámetro libre (la restricción de espín-2 sin masa es estructural, no sintonizable), pero SÍ es una calibración: sin ella, $c(\rho)$ se determina solo hasta una escala global.

---

## 13.6 Ausencia de Fantasmas (Clásica, Signatura Euclidiana)

**Teorema 13.3 (Ausencia de fantasmas clásica — Signatura euclidiana).** Para todo $\dot\Gamma \in T_\Gamma\mathcal{M}_{\mathrm{adm}}$:
$$T(\dot\Gamma) = \|\dot\Gamma_s\|_F^2 + \|\dot\Gamma_a\|_F^2 \geq 0$$

**Proposición 13.2 (Mecanismo de doble negativa).** El fantasma aparente de $\kappa = -1$:
- Cinético: $(-1)\cdot\mathrm{tr}(\dot\Gamma_a^2) = +\|\dot\Gamma_a\|_F^2 > 0$ ✓
- Potencial: $-(-1)\cdot\mathrm{tr}(\Gamma_a^2) = -\|\Gamma_a\|_F^2 < 0$ (pozo de potencial, no colina) ✓

Dos negativos se cancelan. No hay fantasma.

**Alcance.** La ausencia de fantasmas se mantiene estrictamente en signatura euclidiana ($\mathcal{M}_{\mathrm{adm}}$, métrica de Frobenius). Una extensión lorentziana (Parte III) introduce $ds^2 < 0$ para modos de tipo tiempo y requiere su propia prueba de ausencia de fantasmas. El resultado clásico es necesario pero no suficiente para la ausencia de fantasmas cuántica (el análisis de restricciones de Dirac se pospone).

---

## 13.7 Resultado Principal

$$\boxed{\mathcal{L}(\Gamma,\dot\Gamma,\rho) = \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2 - \mu(\rho)\det(\Gamma), \qquad \mu(\rho) = \frac{2}{\sqrt{c(\rho)}}}$$

**Teorema 13.4.** Único *dentro* de la clase definida por: paridad S2 + invariancia G(3) + isotropía + desacoplamiento de sectores + minimalidad (grado $\leq 4$) + autoconsistencia del atractor + ausencia de fantasmas. Cada restricción está motivada de forma independiente; su conjunción no deja parámetros libres dado $c(\rho_{\mathrm{GR}}) = 1$.

---

## 13.8 Ecuaciones de Movimiento

**Conservativo ($\gamma = 0$, $N = 0$):**
$$\ddot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\,\mathrm{adj}(\Gamma)^T = 0$$

(Escrito como $\frac{\mu}{2}\det(\Gamma)\Gamma^{-T}$ para $\det > 0$, pero la forma de la adjunta es suave en todas partes).

**Disipativo (régimen físico):**
$$\boxed{\ddot\Gamma + \gamma\dot\Gamma + \Gamma + \frac{\mu(\rho)}{2}\,\mathrm{adj}(\Gamma)^T = N(t)}$$

| Término | Lectura estructural |
|---|---|
| $\ddot\Gamma$ | Inercia del cambio estructural |
| $\gamma\dot\Gamma$ | Amortiguamiento estructural ($\gamma$ = rigidez organizacional) |
| $\Gamma$ | Fuerza restauradora lineal hacia $\Gamma = 0$ |
| $\frac{\mu}{2}\mathrm{adj}(\Gamma)^T$ | Fuerza de propósito hacia el equilibrio $P(\Gamma)$; la fuerza que hace del sistema una UoC |

**Observación 13.8 (Sin singularidad en el límite).** $\det(\Gamma)\cdot\Gamma^{-T} = \mathrm{adj}(\Gamma)^T$ por la identidad de cofactores. La adjunta es un polinomio en $\Gamma$ — suave en todas partes, incluyendo $\det(\Gamma) = 0$. La singularidad aparente es un artefacto de la representación.

**Hamiltoniano (conservativo):** $H = T + \|\Gamma\|_F^2 + \mu\det(\Gamma)$ — definido positivo en $\mathcal{M}_{\mathrm{adm}}$.

---

## 13.10 Estatus Epistémico

| Afirmación | Estatus | Condiciones |
|---|---|---|
| Base de invariantes $\{I_1, I_2, \det\}$ | Derivada | Bajo S1–S2 + desacoplamiento de sectores + minimalidad |
| $\kappa = -1$ | Derivada bajo postulado | Requiere isotropía $a=b$; bajo S1–S2 solo existe una familia de 2 parámetros |
| $\mu = 2/\sqrt{c(\rho)}$ | Condición de autoconsistencia | Punto fijo; no es una derivación independiente |
| Ausencia de fantasmas (clásica) | Probada | Solo signatura euclidiana; caso lorentziano abierto |
| Ausencia de fantasmas (cuántica) | Abierto | Análisis de restricciones de Dirac pospuesto |
| $c(\rho_{\mathrm{GR}}) = 1$ | Condición de contorno gravitacional | Calibración contra RG, no geometría pura |
| $c(\rho)$ para todo $\rho$ | Cap. 14 | Requiere la ley de escala T1 |
| Correspondencia EM | Restricción de consistencia | Brecha de signatura euclidiana vs lorentziana; Hito 3 |
| Correspondencia RG | Parcial | Gravitón sin masa confirmado; RG completa requiere Hito 3 |
| Correcciones de orden superior | Abierto | Extensión cuántica |

---

*El Cap. 10 declaró el Lagrangiano. El Cap. 13 deriva por qué debe tener esta forma — condicionado a los postulados establecidos. El Cap. 14 determina $c(\rho)$ para todos los niveles organizacionales.*
