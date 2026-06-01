# Capítulo 12: La geometría del acoplamiento
*Versión condensada — Parte II*

---

## 12.1 El cambio: de la álgebra a la geometría

La Parte I operó en el espacio de atributos $\mathcal{M}_\xi$ — el espacio de estados $\xi = (S, A, \mathbf{I}, \mathbf{R})$. La Parte II opera directamente en $\mathcal{M}(\Gamma)$ — el espacio de matrices de acoplamiento. El movimiento refleja el cambio de lo *declarativo* (qué son los objetos) a lo *derivativo* (por qué deben ser como son). Dos preguntas abiertas de la Parte I impulsan este capítulo:

- **Q1 (Forma).** El atractor $P(\Gamma)$ quedó sin especificar en el Cap. 11.
- **Q2 (Dinámica).** Los coeficientes lagrangianos $\kappa(\rho)$, $\mu(\rho)$ se dejaron como funciones por determinar.

---

## 12.2 El manifold de configuración

**Definición 12.1 (Manifold base).**

$$\mathcal{M}(\Gamma) := \mathrm{GL}^+(4,\mathbb{R}) = \{\Gamma \in \mathrm{Mat}(4,\mathbb{R}) \mid \det(\Gamma) > 0\}$$

Esta igualdad es exacta — no es una relación de subconjunto.

**Definición 12.1a (Manifold admisible).**

$$\mathcal{M}_{\mathrm{adm}}(\Gamma) := \{\Gamma \in \mathcal{M}(\Gamma) \mid \Gamma_s \succ 0\}$$

$\mathcal{M}_{\mathrm{adm}}$ es un subconjunto abierto propio de $\mathrm{GL}^+(4,\mathbb{R})$. El término "manifold de configuración" en la Parte II se refiere a $\mathcal{M}_{\mathrm{adm}}$ a menos que se indique lo contrario.

**Consecuencia 12.2 (Admisibilidad — derivada del Cap. 5 Observación 5.1 + Cap. 10 Teorema 10.1).** $\Gamma_s \succ 0$ se deduce del requisito de que $M = \Gamma_s^{-1}/\gamma \succ 0$ (dinámica de Lyapunov). Esto no es un postulado independiente. Las configuraciones con $\Gamma_s \not\succ 0$ (modos taquiónicos) son inadmisibles a nivel clásico.

**Topología.** $\mathcal{M}(\Gamma)$ es un subconjunto abierto denso de $\mathbb{R}^{16}$, conexo. Los grupos de homotopía precisos (vía retracción por descomposición polar a SO(4)) se posponen para la Parte III.

**Descomposición de Frobenius.** $\|\Gamma\|_F^2 = \|\Gamma_s\|_F^2 + \|\Gamma_a\|_F^2$ — ortogonal, exacta (no es un ansatz):

$$\mathcal{M}_{\mathrm{adm}}(\Gamma) \subset \mathrm{Sym}(4) \oplus \mathfrak{so}(4)$$

---

## 12.3 Atributos intrínsecos nulos — Degeneración y transformación de la UoC

**Definición 12.2 (Atributo intrínseco nulo).** El atributo $X$ es nulo si $\kappa_X = \Gamma_{XX} = 0$ y $\gamma_{Xj} = 0$ para todo $j \neq X$ (toda la fila y columna $X$-ésima son cero). Notación: $\kappa_X$ para la autocoherencia — distinta de $c$ (velocidad de la luz, Cap. 15).

**Proposición 12.1.** Atributo intrínseco nulo $\Rightarrow$ $\det(\Gamma) = 0$ $\Rightarrow$ UoC en $\partial\mathcal{M}(\Gamma)$.

**Interpretación.** Un atributo nulo no produce un estado especial de la *misma* UoC — destruye la UoC. Lo que sigue es una entidad *diferente*, que puede heredar los atributos supervivientes (no nulos) como condiciones iniciales.

**Observación 12.2 (Herencia de la UoC).** Tras el colapso del atributo $X$, el sucesor tiene un acoplamiento inicial $\Gamma_{\mathrm{new}}(t=0) = \pi_{\hat{X}}(\Gamma_{\mathrm{old}})$.

**Observación 12.5 (Estratificación de la frontera).** $\partial\mathcal{M}(\Gamma)$ está estratificada por $\mathrm{rank}(\Gamma) \in \{0,1,2,3\}$. El rango 3 (un atributo nulo) es el cruce de frontera genérico. La estratificación completa pertenece a la Parte III.

**Observación 12.3 (Admisibilidad del salto).** No toda proyección $\pi_{\hat{X}}(\Gamma_{\mathrm{old}})$ produce un sucesor estable. La admisibilidad requiere que la $\Gamma_{\mathrm{new}}(t=0)$ heredada no conduzca inmediatamente a $\det(\Gamma_{\mathrm{new}}) \to 0$. El criterio formal requiere la teoría de Morse de $\mathcal{C}(\Gamma)$ en $\partial\mathcal{M}(\Gamma)$ — Parte III.

### 12.3.1 Clasificación por atributo colapsado

| Atributo nulo | Destruido | El sucesor hereda | Caso paradigmático |
|---|---|---|---|
| $S$ | Centro organizador, identidad propia | $\{A, \mathbf{I}, \mathbf{R}\}$ | Plasma neutro |
| $A$ | Agencia, cambio autogestionado | $\{S, \mathbf{I}, \mathbf{R}\}$ | Célula muerta (retiene forma, sin metabolismo) |
| $\mathbf{I}$ | Coherencia del campo interno | $\{S, A, \mathbf{R}\}$ | Gas ideal no rotatorio |
| $\mathbf{R}$ | Acoplamiento ambiental | $\{S, A, \mathbf{I}\}$ | Subsistema termodinámicamente aislado |

### 12.3.2 El campo EM en el vacío

Cuando se eliminan las cargas: tanto $S$ (densidad de carga) como $A$ (corriente) colapsan. El resultado **no** es un estado especial de la UoC cargada — es una *configuración de frontera con contenido estructural heredado* (no es una UoC completa según el criterio del §0.3, que requiere Fuerza y Campo activos simultáneamente).

$$\Gamma_{\mathrm{EM}} = \begin{pmatrix} 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & \gamma_{IR} \\ 0 & 0 & -\gamma_{IR} & 0 \end{pmatrix}, \qquad \det = 0, \quad \mathrm{rank} = 2$$

Onda plana: $\mathbf{E}\cdot\mathbf{B} = 0 \Rightarrow \det(F_{\mu\nu}) = 0 \Rightarrow \mathrm{adj}(\Gamma) = 0 \Rightarrow \square F_{\mu\nu} = 0$ (Cap. 15).

### 12.3.3 Propósito nulo — Tres rutas

**Proposición 12.2.** Propósito nulo a través de exactamente uno de:
- *(i)* Atributo intrínseco nulo ($\det = 0$, UoC destruida)
- *(ii)* Puramente antisimétrico con Pfaffiano nulo ($\Gamma_s = 0$, $\mathrm{Pf}(\Gamma_a) = 0$) — el caso de la onda plana EM
- *(iii)* $\mu(\rho) = 0$ — nivel organizacional en el que el paisaje de propósito se aplana

En los tres casos: $\mathcal{L} \to \|\dot\Gamma\|_F^2 - \|\Gamma\|_F^2$ (dinámica armónica, sin atractor).

**Observación 12.4 (Desacoplamiento parcial).** Atributo parcialmente desacoplado: $\kappa_X > 0$ pero $\gamma_{Xj} = 0$ para $j \neq X$. Entonces $\det(\Gamma) = \kappa_X \cdot \det(\Gamma_{\hat{X}}) > 0$ — la UoC sobrevive, pero $X$ es estructuralmente inerte. Distinto de un atributo nulo.

### 12.3.4 Conexión con el Propósito a través de regímenes (Cap. 11 §11.7b)

Las configuraciones de frontera descritas anteriormente son el régimen en el que $P(\Gamma)$ es *latente*: definido en $\overline{\mathcal{M}}(\Gamma)$, pero con fuerza dinámica nula porque el término adjunto $\mathrm{adj}(\Gamma)^T$ es cero para $\mathrm{rank}(\Gamma) \leq 2$ (Lema 15.1). Cuando la frontera es cruzada transversalmente por una UoC coherente que pierde un atributo, $P$ no desaparece — se reinstancia como el propósito del sucesor, con $\Gamma^*_{\mathrm{new}}$ generalmente distinto de $\Gamma^*_{\mathrm{old}}$ (Cap. 11 §11.7b, rol generativo).

La misma UoC, por lo tanto, atraviesa tres regímenes de propósito:
- **Activo** ($\det\Gamma > 0$): $P$ impulsa la dinámica hacia $\Gamma^*$;
- **Latente** ($\det\Gamma = 0$): $P$ está definido pero inactivo; el sistema se propaga como régimen de onda (Cap. 15 §15.1);
- **Generativo** (cruce de frontera): $P$ se reinstancia como el potencial del sucesor.

Esto unifica la tensión aparente entre "propósito como atractor" (EOM activas) y "propósito en la frontera" (configuraciones con $\det\Gamma=0$ como ondas planas EM u osciladores de rango 2). El propósito es el *paisaje de potencial en todos los regímenes*; el régimen determina si actúa y cómo lo hace.

**Conexión con Cap. 15 §15.1 (UoC vs régimen, lectura T8 (D)).** Las configuraciones de rango $\leq 2$ describen **regímenes** de UoCs, no nuevas UoCs. La onda plana EM, el oscilador mecánico de rango 2 y la onda acústica son regímenes de UoCs subyacentes (sistema de fuente cargada, masa, parcela de fluido) en los que los atributos de fuente/agencia están momentáneamente inactivos. La estratificación de frontera de $\partial\mathcal{M}(\Gamma)$ cataloga qué regímenes puede ocupar una UoC sin perder su identidad como tal; el cruce completo de la frontera (transición a un sucesor) es un evento distinto de la reducción de rango dentro de $\overline{\mathcal{M}}$.

---

## 12.4 El nivel organizacional $\rho$ como parámetro geométrico

**Nota de notación.** $\rho$ = nivel organizacional (GSF). Distinto de $\rho_m$ = densidad de masa (física). Cuando ambos aparecen (Cap. 15), la densidad física lleva el subíndice.

**Postulado 12.1 ($\rho$ como parámetro suave).** $\rho > 0$ indexa una familia $\mathcal{M}(\Gamma; \rho)$. La métrica de Frobenius y la simetría G(3) son independientes de $\rho$; solo $\kappa(\rho)$, $\mu(\rho)$ dependen de $\rho$.

Esto convierte a $\mathcal{M}_{\mathrm{adm}}$ en un fibrado sobre $\mathbb{R}_{>0}$ con fibra $\cong \mathrm{GL}^+(4,\mathbb{R})$.

**Por qué $\rho^{-1}$ y no $\log\rho$ o $e^\rho$.** Los cambios en $\rho$ forman un grupo multiplicativo. La ecuación funcional de Cauchy restringe las soluciones continuas a leyes de potencia $\Gamma \propto \rho^\alpha$. El exponente específico $\alpha = -1$ es seleccionado por la covarianza de las EOM — establecido en el Cap. 14 Teorema 14.1.

---

## 12.5 Programa derivativo de la Parte II

| Capítulo | Tarea | Restricción clave |
|---|---|---|
| Cap. 13 | Derivar $\kappa = -1$, $\mu = 2/\sqrt{c(\rho)}$ | Isotropía de Frobenius + autoconsistencia del atractor |
| Cap. 14 | Derivar $c(\rho) = (\rho_{\mathrm{GR}}/\rho)^4$, escalamiento T1 | Tres requisitos estructurales independientes |
| Cap. 15–18 | Pruebas de dominio: física, información, biología, agua | Verificación estructural, no ajuste de parámetros |
| Cap. 19 | Coherencia $\mathcal{C}(\Gamma)$, Lyapunov, homeodinámica | Límite AM-GM, Teoremas 19.1–19.2 |
| Cap. 20–21 | Topología, inventario, derivabilidad | $\pi_1(\mathcal{M}) = \mathbb{Z}_2$, qué derivó/no derivó la Parte II |

---

## 12.6 Nota epistémica: Signatura de la métrica

La métrica de Frobenius en $\mathcal{M}_{\mathrm{adm}}$ es **riemanniana** (definida positiva). La dinámica GSF en la Parte II es euclidiana en el espacio de configuración — $t$ es una variable de evolución paramétrica. La signatura lorentziana (estructura causal, conos de luz) emerge en el Cap. 15 a través de la extensión postulada $\partial_t^2 \to \square$, no de la estructura riemanniana de $\mathcal{M}_{\mathrm{adm}}$. Si la signatura lorentziana puede derivarse de una estructura pseudoriemanniana en un manifold mayor es una cuestión abierta para la Parte III.

---

## Tabla de resumen

| Objeto | Estatus |
|---|---|
| $\mathcal{M}(\Gamma) = \mathrm{GL}^+(4,\mathbb{R})$ | Definición (igualdad exacta) |
| $\mathcal{M}_{\mathrm{adm}} \subset \mathcal{M}(\Gamma)$ | Definición + Consecuencia 12.2 ($\Gamma_s \succ 0$) |
| Justificación de $\Gamma_s \succ 0$ | Estructural: necesaria para $P(\Gamma)$ acotado inferiormente |
| Homotopía de $\mathcal{M}(\Gamma)$ | Pospuesta para la Parte III |
| Atributo nulo $\Rightarrow$ det = 0 | Demostrado (Proposición 12.1) |
| Atributo nulo $\Rightarrow$ UoC destruida | Capa interpretativa (GSF) |
| Vacío EM como "sucesor de frontera" | No es una UoC completa; configuración de frontera con $\{\mathbf{I},\mathbf{R}\}$ heredados |
| Rol del propósito en regímenes (activo / latente / generativo) | Articulado en §12.3.4; declaración completa Cap. 11 §11.7b |
| Rango $\leq 2$ como régimen, no nueva UoC (T8 lectura D) | Establecido en Cap. 15 §15.1; consistente con §12.3.2 |
| Condición de admisibilidad del salto | Abierta — Parte III (teoría de Morse de $\mathcal{C}$) |
| $\rho$ como parámetro conformal | Postulado 12.1 — derivado en Cap. 14 |
| Signatura lorentziana | Postulada en Cap. 15, no derivada de $\mathcal{M}_{\mathrm{adm}}$ |

---

*La Parte I declaró la gramática. El Cap. 12 define el espacio en el que la gramática evoluciona. El Cap. 13 deriva la ley de evolución.*
