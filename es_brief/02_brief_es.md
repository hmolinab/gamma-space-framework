# Capítulo 2: La Formulación Vectorial
*Versión condensada — fuente: Cap. 2 del GSF completo*

---

## 2.1 La Cuestión

El Capítulo 1 asignó tipos matemáticos a las cuatro variables intrínsecas — S como escalar, **A**, **I**, **R** como vectores — sin justificación. Este capítulo argumenta a favor de esa asignación a partir de los roles funcionales de las variables y del requisito formal de que las variables inherentes (Fuerza, Campo) estén bien definidas. El argumento es una reconstrucción racional bajo un criterio de minimalidad, no una derivación formal.

Dos pasos: (1) argumento de grado: ¿qué tipo requiere el rol estructural de cada variable? (2) argumento de espacio: ¿cuál es la dimensión mínima del espacio de configuración?

---

## 2.2 Argumento de Grado: ¿De qué tipo debe ser cada variable?

### 2.2.1 La Singularidad es un Escalar

S responde a: *¿en qué grado se distingue esta UoC de su entorno?* Esta es una cuestión de magnitud sin dirección; la frontera entre el sí-mismo y el no-sí-mismo tiene extensión, no orientación. A S se le asigna el grado 0 (escalar).

*Nota*: el ordenamiento de S como lógicamente anterior a **A**, **I**, **R** es una elección de diseño: la demarcación propia se trata como una precondición para la actividad dirigida. Un marco que invirtiera este orden no puede excluirse por motivos puramente formales.

### 2.2.2 Agencia, Impulso y Relación son Vectores

La Fuerza y el Campo son **variables inherentes** de toda UoC operativa (Cap. 1 §1.4) — operaciones constitutivas que no pueden estar ausentes cuando la UoC existe. Debido a que son inherentes, el hecho de que estén bien definidas es un requisito estructural, no una propiedad deseable. Esto es lo que hace que el argumento de grado sea vinculante.

El argumento no es que una Agencia escalar significaría falta de capacidad — un escalar podría representar una capacidad uniforme en todas las direcciones. El argumento es que el tipo escalar es incompatible con una Fuerza y un Campo bien definidos:

- **Si A fuera escalar**: Fuerza = S·**A** sería un escalar (producto de dos escalares). Una Fuerza escalar no posee dirección; la UoC no podría producir transformaciones orientadas.
- **Si I fuera escalar**: Campo = **I** × **R** requeriría un producto cruz entre un escalar y un vector — indefinido en el álgebra vectorial estándar.
- **Si R fuera escalar**: lo mismo — Campo = **I** × **R** estaría indefinido.

El grado 1 (vector) es también el tipo mínimo para una variable direccional: los objetos de grado superior (tensores de orden ≥ 2) codifican relaciones *entre* direcciones, introduciendo una estructura no requerida en el nivel ontológico.

> **A, I, R son vectores (grado 1): el tipo mínimo para el cual la Fuerza y el Campo están bien definidos.**

---

## 2.3 Argumento de Espacio: ¿Cuál es la Dimensión Mínima?

### 2.3.1 Fuerza = S·A no restringe la dimensión

La multiplicación escalar está definida en cualquier espacio vectorial de cualquier dimensión. La Fuerza no impone restricciones sobre la dimensión de V.

### 2.3.2 Campo = I × R restringe la dimensión a 3

**Postulado 2.1 (Homogeneidad del Campo)**: El Campo habita en el mismo subespacio de grado 1 que **I** y **R**.

El producto geométrico natural de dos vectores es el producto cuña (wedge) **I**∧**R** — un bivector de grado 2, que habita en un subespacio distinto. Si el Campo fuera un bivector, estaría bien definido en cualquier dimensión ≥ 2, eliminando por completo la restricción de dimensionalidad. El Postulado 2.1 requiere que el Campo sea de grado 1, lo que fuerza al producto cruz **I**×**R** como el dual de Hodge de **I**∧**R**. Esta restricción es un postulado de diseño — la hipótesis fundamental de todo el argumento espacial.

Bajo el Postulado 2.1, el producto cruz debe mapear V × V → V. El resultado clásico (Eckmann, 1943) establece que tal producto —bilineal, antisimétrico y que preserva la norma— existe solo en dimensiones 1, 3 y 7:

| Dimensión | Resultado | Estatus |
|-----------|-----------|---------|
| 1 | Producto cruz trivialmente cero | Degenerado ✗ |
| 2 | El producto cruz produce un escalar | No está en V ✗ |
| **3** | **Vector único perpendicular tanto a I como a R** | **✓** |
| 7 | Vector en V, pero no es único (estructura G₂ octoniónica) | Ambiguo ✗ |
| > 7 | No existe tal producto | ✗ |

La dimensión mínima no ambigua es **3**.

### 2.3.3 La Perpendicularidad del Campo

El Campo es perpendicular tanto a **I** como a **R** — una nueva dirección estructural que emerge de su tensión pero que no es reducible a ninguna de las dos. El Campo desaparece cuando **I** ∥ **R** y se maximiza cuando **I** ⊥ **R**.

---

## 2.4 El Espacio de Configuración

$$\mathcal{V} = \mathbb{R} \times \mathbb{R}^3 \times \mathbb{R}^3 \times \mathbb{R}^3$$

Un estado de una UoC es un punto $\xi = (S, \mathbf{A}, \mathbf{I}, \mathbf{R}) \in \mathcal{V}$ — el vector de estado primario. A partir de $\xi$, la matriz de configuración $\Gamma(\xi) \in \mathrm{Sym}(4) \oplus \mathfrak{so}(4)$ codifica la estructura de acoplamiento por pares (Cap. 5). Estos son dos objetos distintos: $\xi$ es el estado; $\Gamma(\xi)$ es la estructura de acoplamiento derivada.

$\mathcal{V}$ no es el espacio físico. Sus tres dimensiones son modos de agencia, orientación e intercambio — no coordenadas espaciales.

---

## 2.5 Resumen de la Estructura Vectorial

| Variable | Tipo | Argumento de grado | Dimensión |
|----------|------|--------------------|-----------|
| S | Escalar (ℝ) | Magnitud sin dirección | — |
| **A** | Vector (ℝ³) | La Fuerza requiere tipo vectorial | §2.3.2 |
| **I** | Vector (ℝ³) | El Campo requiere operandos vectoriales | §2.3.2 |
| **R** | Vector (ℝ³) | El Campo requiere operandos vectoriales | §2.3.2 |
| Fuerza = S**A** | Vector (ℝ³) | El escalamiento escalar preserva el grado | — |
| Campo = **I**×**R** | Vector (ℝ³) | Dual de Hodge de **I**∧**R**; grado 1 por Postulado 2.1 | Requiere ℝ³ |

---

## 2.6 La Estructura de Álgebra Geométrica

Las cuatro variables abarcan la estructura de grado completa de **G(3)** — el álgebra geométrica del espacio tridimensional:

| Grado | Dimensión | Relación con la UoC |
|-------|-----------|---------------------|
| 0 (escalar) | 1 | S |
| 1 (vectores) | 3 | **A**, **I**, **R** (asumiendo base linealmente independiente) |
| 2 (bivectores) | 3 | **A**∧**I**, **A**∧**R**, **I**∧**R** (= Campo vía dual de Hodge) |
| 3 (pseudoscalar) | 1 | **A**∧**I**∧**R** (volumen orientado) |
| **Total** | **8 = 2³** | |

*Aclaración*: **A**, **I**, **R** son *elementos* de grado 1 de G(3), no generadores. Los generadores son los vectores de la base ortonormal {**e**₁, **e**₂, **e**₃}. La estructura G(3) se aplica bajo el supuesto de que **A**, **I**, **R** son linealmente independientes y el espacio de configuración porta la métrica euclidiana estándar — ambas hipótesis minimalistas. El dual de Hodge (Campo = **I**×**R**) presupone esta métrica.

El argumento de suficiencia —que no se necesita una quinta variable ontológica— se sigue del hecho de que {S, **A**, **I**, **R**} ya abarcan las 8 dimensiones de G(3), no dejando espacio para que una quinta variable añada poder expresivo (Cap. 3).

---

## 2.7 Alcance y Preguntas Abiertas

- **¿Por qué un Campo vectorial y no un bivector?** Esta es la cuestión abierta central del capítulo. Si se permitiera que el Campo fuera un bivector (**I**∧**R**, grado 2), la restricción de dimensión de §2.3.2 colapsaría — los bivectores están bien definidos en cualquier dimensión ≥ 2. El Postulado 2.1 (Campo de grado 1) es la hipótesis fundamental; su revisión requeriría repensar la derivación de la dimensionalidad desde cero.
- **¿Por qué ℝ³ y no ℝ⁷?** ℝ³ es la dimensión mínima bajo el Postulado 2.1. El caso 7D no está formalmente excluido pero introduce no-unicidad (estructura octoniónica); se excluye por parsimonia.
- **Configuraciones degeneradas**: la independencia lineal de **A**, **I**, **R** se asume, no se deriva. Las configuraciones donde dos variables son paralelas (ej. **I** ∥ **R**) no están excluidas de $\mathcal{V}$ pero pueden corresponder a estados patológicos de la UoC (Campo = 0).
- **Suficiencia de cuatro variables**: argumento formal en el Cap. 3.

---

*Fin del Capítulo 2 (condensado)*
