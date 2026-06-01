# Capítulo 9: Dinámica Estructural No Lineal
*Versión condensada — fuente: Cap. 9 del GSF completo*

---

## 9.1 De la Estructura a la Dinámica

Los capítulos 1 al 8 establecieron la ontología estructural de una UoC. Este capítulo desarrolla la dinámica formalmente. La ley de evolución es:

$$\frac{d\xi}{dt} = f(\xi,\, \Gamma_E,\, \rho)$$

La interpretación estructural: el nivel teleológico **corresponde** al atractor estructural de la dinámica; el nivel epistemológico es el mecanismo por el cual la UoC participa en la convergencia hacia o divergencia de dicho atractor. Esta es una correspondencia, no una derivación — las matemáticas establecen un funcional de Lyapunov $P$ y un punto fijo $\xi^*$; la identificación de $\xi^*$ con el "propósito" es un paso interpretativo, declarado explícitamente aquí.

---

## 9.2 La Representación Dual: ξ(t) y Γ(t)

**Estado primario.** $\xi(t) = (S(t), \mathbf{A}(t), \mathbf{I}(t), \mathbf{R}(t)) \in \mathcal{V} = \mathbb{R} \times \mathbb{R}^3 \times \mathbb{R}^3 \times \mathbb{R}^3$ (10D). La ley de evolución gobierna $\dot{\xi}(t)$.

**Estructura derivada.** $\Gamma(t) = \Gamma[\xi(t)]$ es un funcional suave ($\Gamma \in C^\infty(\mathcal{V})$ — suavidad asumida explícitamente; esencial para la regla de la cadena, los argumentos de Lyapunov y la teoría de Morse). No tiene dinámica independiente:

$$\Gamma(t) = \Gamma[\xi(t)], \qquad \frac{d\Gamma}{dt} = \frac{\partial\Gamma}{\partial\xi}\,\dot{\xi}(t)$$

Las condiciones de salud (Cap. 5) son condiciones sobre $\Gamma[\xi]$, no sobre $\xi$ directamente.

---

## 9.3 El Espacio de Estados

**Convención terminológica.** $\mathcal{V}$ es el **espacio de estados** (sistema de primer orden — sin sector de momento separado en la formulación actual; trabajos posteriores pueden extenderlo al fibrado cotangente). El término "configuración" se reserva para $\Gamma(\xi)$.

La existencia y unicidad de las trayectorias se asume a partir de la continuidad local de Lipschitz de $f$ (requerida para las definiciones de cuenca del §9.9). Los observables derivados mediante la proyección $\Pi: \mathcal{V} \to \mathbb{R}^3 \times \mathbb{R}^3$: $\Pi(\xi) = (\text{Fuerza}, \text{Campo})$.

---

## 9.4 La Ley de Evolución

$$\frac{d\xi}{dt} = f(\xi,\, \rho), \qquad \frac{dP}{dt} = \nabla_\xi P \cdot f(\xi,\rho) \leq 0 \quad \text{(condición de orientación teleológica)}$$

$P$ no es un argumento de $f$ — restringe la clase admisible de $f$ a través de la desigualdad. El jacobiano $J(\xi) = Df(\xi)$ determina la estabilidad local (§9.11).

**Ansatz no lineal mínimo** *(opción de modelado fenomenológico — no es una consecuencia única de G(3); el Cap. 10 §10.3.2 deriva la forma general $\dot\xi = -(M+A)\nabla P$; los coeficientes $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$ requieren un $P(\Gamma)$ explícito del Cap. 11)*:

$$\frac{dS}{dt} = f_S(S), \quad \frac{d\mathbf{A}}{dt} = f_\mathbf{A}(\mathbf{A}, S)$$
$$\frac{d\mathbf{I}}{dt} = \alpha_\mathbf{I}(\mathbf{R} \times \mathbf{I}) + \beta_\mathbf{I}|\mathbf{I}|^2\mathbf{I} + f^{(\nabla P)}_\mathbf{I}, \quad \frac{d\mathbf{R}}{dt} = f_\mathbf{R}(\mathbf{R}, \rho)$$

La estabilidad requiere $\beta_\mathbf{I} < 0$ (no linealidad saturante). El término $\mathbf{R} \times \mathbf{I}$ es el acoplamiento compatible con G(3) de menor orden; el término cúbico es el auto-acoplamiento invariante ante rotaciones de menor orden. Ambos son elecciones de modelado.

---

## 9.5 La Función de Propósito

**Postulado 9.1 (Función de Propósito).** Para cada UoC a un $\rho$ dado, existe $P: \mathcal{V} \to \mathbb{R}^+_0$ con:
1. $P(\xi) \geq 0$
2. $P(\xi^*) = 0$ para algún $\xi^*$ con $f(\xi^*, \rho) = 0$ (atractor estructural — existencia postulada)
3. $\frac{dP}{dt} \leq 0$ a lo largo de trayectorias autónomas

Las condiciones (1)–(3) son condiciones de la función de Lyapunov. **Nota sobre la circularidad:** la estabilidad está integrada en el postulado (no se deriva de la dinámica) — $P$ es un postulado de existencia, no una derivación. La forma explícita de $P$ no se postula; se deriva en el Cap. 11. La unicidad de $\xi^*$ no se postula — ver Prop 9.1a.

**Proposición 9.1a (Unicidad Genérica).** Bajo supuestos topológicos sobre $D_\xi(\rho)$:
- *H1* — Compacto; *H2* — Conexo; *H3* — Contraíble

...y para $\rho \neq \rho_\text{crítico}$, la función $P$ Morse-genérica tiene un único mínimo local $\xi^*(\rho)$ por componente conexa. *H1 (compacidad) es plausiblemente derivable del Postulado 4.2 del Cap. 4 (la contracción del dominio acota $D_X(\rho)$ para $\rho > 0$ finito); H2–H3 permanecen como supuestos de trabajo.* En $\rho_\text{crítico}$, la multiplicidad es el mecanismo de transición de fase estructural, no una patología.

---

## 9.6 Estabilidad de Lyapunov

**Candidato 1** — Distancia de configuración: $V_1(\Gamma) = \|\Gamma - \Gamma^*\|_F^2$. Mide la distancia de la estructura de acoplamiento respecto al atractor.

**Candidato 2** — Intensidad estructural: $V_2(\xi) = c_1|\text{Fuerza}|^2 + c_2|\text{Campo}|^2$ ($c_1, c_2 > 0$, distintos de $\alpha_\mathbf{I}, \beta_\mathbf{I}$). Mide la actividad estructural, no la convergencia a $\xi^*$.

El Teorema 10.1 del Cap. 10 establece a $P$ como el funcional de Lyapunov primario. $V_1$ es un proxy local cerca de $\xi^*$; $V_2$ es un diagnóstico de intensidad estructural.

---

## 9.7 Tipos de Atractores por Nivel de ρ — Interpretaciones Candidatas

| Nivel de ρ | Contenido del atractor *(candidato)* | Tipo de atractor *(candidato)* | Carácter termodinámico |
| :--- | :--- | :--- | :--- |
| Alma — $\rho \to 0$ | Máxima coherencia estructural | Punto fijo estable | No se requiere $F_{ext}$ para sostener ρ |
| Ego | Mantenimiento de la identidad | Punto fijo de dinámica autónoma a ρ alto | Requiere $F_{ext} \neq 0$ para sostener el nivel de ρ |
| Cuerpo | Equilibrio homeostático | Punto fijo estable o ciclo límite | Flujo metabólico |
| Célula | Viabilidad bioquímica | Punto fijo estable o ciclo límite | Flujo metabólico |

**Aclaración crítica — atractor del ego vs. estado forzado.** Tanto el atractor del alma como el del ego satisfacen $f(\xi^*, \rho) = 0$ — ambos son puntos fijos de la dinámica autónoma en sus respectivos niveles de ρ (Postulado 9.1). La distinción es **estructural** (si se requiere un impulso externo), no dinámica:

- **Atractor del alma** *(candidato — Hipótesis 34.1 de trabajos posteriores)*: el régimen $\rho \to 0$ es consistente con el cuasi-equilibrio; no se requiere impulso externo.
- **Atractor del ego** *(candidato — Hipótesis 34.1 de trabajos posteriores)*: mantener un $\rho$ alto requiere $F_{ext} \neq 0$ (trabajos posteriores). Sin ello, $\rho$ decae y el atractor del ego se disuelve — no porque $\xi^*_{ego}$ sea dinámicamente inestable dentro de su nivel de ρ, sino porque el nivel de ρ en sí mismo es estructuralmente abierto (requiere impulso externo).

"Estructuralmente abierto" en este contexto significa que requiere un impulso estructural externo para sostener $\rho$ — no que el atractor sea un ciclo límite o un NESS en el sentido de los sistemas dinámicos.

---

## 9.8 El Rol del Nivel Epistemológico

Tres modos de acción de $\Gamma_E$ sobre $\dot{\xi} = f(\xi, \Gamma_E, \rho)$:
1. **Facilitación de la convergencia** — trayectoria alineada con la cuenca $B(\xi^*)$
2. **Resistencia estructural** — trayectoria desviada de $B(\xi^*)$
3. **Atractores aparentes** — mínimos locales efectivos $\xi_{app} \neq \xi^*$ bajo un $\Gamma_E$ sostenido

**Definición 9.1 (Atractor Aparente).** $\xi_{app} \neq \xi^*$ con $\lim_{t\to\infty}\xi(t) = \xi_{app}$ bajo un $\Gamma_E \neq 0$ sostenido. Se disuelve cuando $\Gamma_E \to 0$.

**Nota sobre la circularidad de Γ_E.** $\Gamma_E$ se trata como una entrada de control externa — no se deriva de la dinámica ontológica. Su constitución interna pertenece al nivel epistemológico (explícitamente abierto en este trabajo).

---

## 9.9 Cuencas de Atracción

$$B(\xi^*) = \{\xi(0) \in \mathcal{V} \mid \lim_{t\to\infty}\xi(t) = \xi^*\}$$

A un $\rho$ alto, $D_\xi(\rho)$ puede no contener a $B(\xi^*_\text{alma})$ — el atractor de bajo $\rho$ es estructuralmente inaccesible. A medida que $\rho$ disminuye, $D_\xi(\rho)$ se expande. *(La interpretación fenomenológica de esto como "libertad contextual" es una correspondencia candidata, no una derivación).*

---

## 9.10 Bifurcaciones y Transiciones Estructurales

### Tipos

**Tipo I (supercrítica):** a medida que $\rho$ cruza $\rho_\text{crítico}$, el atractor del ego se transforma suavemente en el atractor del alma. Sin histéresis.

**Tipo II (subcrítica):** coexistencia de los atractores del ego y del alma cerca de $\rho_\text{crítico}$, separados por el límite de la cuenca. Histéresis posible. Transición súbita cuando se cruza el límite.

### Modelo Reducido Canónico

Sea $x$ = parámetro de orden, $\mu = \rho - \rho_\text{crítico}$:

$$\dot{x} = \mu x - x^3$$

- $\mu < 0$: $x = 0$ estable *(candidato: atractor del alma)*; ramas de alto ρ inestables.
- $\mu > 0$: $x = 0$ inestable; $x = \pm\sqrt{\mu}$ estables *(candidato: atractores del ego)*.

Las dos ramas simétricas son candidatos a atractores del ego — no derivados como tales de la forma normal. La conexión con la estructura de Landau del Cap. 11 §11.7 es **formalmente análoga** (misma estructura de parámetro de bifurcación, no linealidad cúbica, estabilizador cuártico); se requeriría un mapeo formal de parámetros para que sea exacta.

---

## 9.11 Análisis de Estabilidad Local y la Matriz de Configuración

*(Nota: "estabilidad estructural" en sistemas dinámicos = estabilidad de f bajo perturbaciones de la propia f — un concepto diferente. Esta sección analiza la estabilidad de Lyapunov de ξ*.)*

Estabilidad local mediante los autovalores $\lambda_i$ de $J(\xi^*) = Df|_{\xi^*}$: todos los $\text{Re}(\lambda_i) < 0$ → estable; cualquier $\text{Re}(\lambda_i) > 0$ → inestable; puramente imaginarios → oscilatorio.

**Conjetura de Investigación 9.1.** La degeneración en $\Gamma$ ($\det\Gamma \to 0$) puede inducir la pérdida de estabilidad dinámica a través de cambios en el espectro de $J$. El espectro estructural $\{\lambda_i(\Gamma)\}$ y el espectro dinámico $\{\mu_i(Df|_{\xi^*})\}$ son distintos y generalmente no son iguales. Establecer una conexión formal requiere la forma explícita de $f$ y una derivación de cómo $J(\xi^*)$ depende de $\Gamma[\xi^*]$. Degradada de "hipótesis de trabajo" a conjetura de investigación a la espera de dicha derivación.

---

## 9.12 Preguntas Abiertas

- **Forma explícita de $f$**: El Cap. 10 §10.3.2 deriva $\dot\xi = -(M+A)\nabla P$. Los coeficientes $\alpha_\mathbf{I}, \beta_\mathbf{I}$ requieren un $P(\Gamma)$ explícito del Cap. 11.
- **Espectro estructural vs. dinámico**: Conjetura de Investigación 9.1 — requiere una $f$ explícita.
- **Forma explícita de $P(\Gamma)$**: a partir de la misma derivación variacional.
- **Verificación topológica de H1–H3** para $D_\xi(\rho)$: requiere una $\Gamma(\xi)$ explícita.
- **Determinación del tipo** de bifurcación ego-alma (I o II): requiere una $P$ explícita.
- **Selección de la función de Lyapunov**: cuál de entre $V_1$, $V_2$ o $P$ es primaria y cómo se relacionan.
- **Dinámica de UoCs copresentes**: dinámica conjunta de UoCs de alma + ego copresentes.
- **Conexión termodinámica**: puente formal entre $P$ y los potenciales termodinámicos (trabajos posteriores).

---

*Fin del Capítulo 9 (condensado)*
