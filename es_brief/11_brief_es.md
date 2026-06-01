# Capítulo 11: La Función de Propósito
*Versión condensada — fuente: Cap. 1 del GSF completo*

---

## 11.1 Motivación: Cerrando el Bucle Estructural

El Cap. 9 introdujo $P$ como no especificada; el Cap. 10 derivó la ley de evolución disipativa $\dot\xi = -M\nabla P$ pero dejó la propia $P$ abierta. El Cap. 11 pregunta: **¿qué es $P$ explícitamente?**

La forma de $P$ determina:
1. La fuerza $f(\xi,\rho)$ y los coeficientes $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$, $\gamma(\rho)$ indeterminados en el Cap. 10 (T3).
2. Si $\xi^*$ es única o admite degeneraciones (T4).
3. Las predicciones observables del GSF.

**Nota conceptual.** "Propósito" = potencial estructural cuyos mínimos codifican estados atractores coherentes. No se refiere a intencionalidad o causalidad final — es un candidato de Lyapunov para el flujo de gradiente del Cap. 10.

---

## 11.2 Restricciones sobre la Función de Propósito

**Configuración.** $P: \mathcal{M}_\xi(\rho) \to \mathbb{R}_{\geq 0}$, evaluada a través de $\Gamma(\xi)$.

**Resultado establecido (anteriormente Supuesto 23.1).** G(3) admite una representación ortogonal fiel $\varrho: G(3)\to O(4)$; específicamente $\varrho(g) = \mathrm{diag}(1, R_g^{\oplus 3})$, ortogonal por construcción — **establecido en el Cap. 8 §8.5–8.8**, no es un supuesto. Si G(3) incluyera transformaciones no ortogonales, la norma de Frobenius no sería invariante y la base del §11.3 requeriría revisión.

**C1 (Invarianza bajo G(3)).** $P(g\cdot\xi) = P(\xi)$ para todo $g \in G(3)$. G(3) actúa sobre $\Gamma$ por conjugación ortogonal: $\Gamma \mapsto \varrho(g)\Gamma\varrho(g)^T$. La traza, el determinante y la norma de Frobenius son todos invariantes bajo esta acción.

**C2 (Positividad/alcanzabilidad).** $P \geq 0$; $P(\xi^*) = 0$ para algún $\xi^*$.

**C3 (No degeneración).** $\nabla P|_{\xi^*} = 0$, $H_P(\xi^*) \succ 0$. Se cumple para $\rho \neq \rho_c$; falla en la densidad crítica.

**C4 (Factorización-Γ).** $P(\xi) = \widetilde{P}(\Gamma(\xi))$ — el propósito mide la coordinación, no las magnitudes brutas de los atributos.

**Proposición 11.0 (C4 derivada de C1).** C4 no es un postulado independiente — se deduce de C1 y del Cap. 8. El mapa de configuración $\xi \mapsto \Gamma(\xi)$ es el mapa de órbita de G(3) en $\mathcal{V}$ (Cap. 8 §8.3, §8.10): $\Gamma(\xi_1) = \Gamma(\xi_2)$ si y solo si $\xi_1$ y $\xi_2$ están en la misma órbita de G(3). Por C1, $P$ es invariante bajo G(3), por lo tanto constante en las órbitas, y por ende se factoriza a través de $\Gamma$. El contenido estructural de C4 —que el propósito mide la coordinación— es la expresión precisa de la invarianza bajo G(3) en el espacio de estados.

---

## 11.3 Invariantes de G(3) de Γ

Invariantes de $\Gamma_s$ (real simétrica $4\times4$): polinomios simétricos elementales de los autovalores — equivalentemente trazas de potencias $\mathrm{tr}(\Gamma_s^k)$, $k=1,\ldots,4$.

Invariantes de $\Gamma_a$ (real antisimétrica): $\mathrm{tr}(\Gamma_a^2)$, $\mathrm{tr}(\Gamma_a^4)$, $\mathrm{Pf}(\Gamma_a)$ (raíz cuadrada con signo de $\det\Gamma_a$; $\mathrm{Pf}(\Gamma_a) = 0$ cuando el rango de $\Gamma_a < 4$).

Invariantes cruzados: $\mathrm{tr}(\Gamma_s^j \Gamma_a^k)$.

**Base de orden mínimo** (cuadrática en desviaciones $\delta\Gamma = \Gamma - \Gamma^*$, bajo el ansatz de conjugación isotrópica):
$$[\mathrm{tr}(\delta\Gamma_s)]^2, \qquad \|\delta\Gamma_s\|_F^2, \qquad \|\delta\Gamma_a\|_F^2$$

El término cruzado $\mathrm{tr}(\delta\Gamma_s\,\delta\Gamma_a) = 0$ idénticamente (simétrico × antisimétrico). Estos tres son independientes; la exhaustividad dentro del ansatz isotrópico depende de la descomposición completa de la representación de G(3) (reservado para el Cap. 3).

---

## 11.4 La Forma Admisible Mínima

**Proposición 11.1 (Forma cuadrática mínima admisible bajo G(3)).** *Una* forma admisible mínima bajo la representación ortogonal establecida de G(3) (Cap. 8 §8.8) + ansatz de conjugación isotrópica + desacoplamiento de sectores (no es una consecuencia única de C1–C4 por sí solos):

$$\boxed{P(\Gamma) \;=\; \frac{\kappa}{2}\,[\mathrm{tr}(\delta\Gamma_s)]^2 \;+\; \frac{\mu}{2}\,\|\delta\Gamma_s\|_F^2 \;+\; \frac{\nu}{2}\,\|\delta\Gamma_a\|_F^2}$$

con $\kappa \geq 0$, $\mu > 0$, $\nu \geq 0$.

**Observación sobre $\Gamma^*(\rho)$.** El objetivo $\Gamma^*$ depende de $\rho$ — en este capítulo se asume dado. **Derivado en la Parte II**: El Teorema 14.1 del Cap. 14 da $\Gamma^*(\rho) = \Gamma_0/\rho$ (ley de escala T1).

**Ansatz de desacoplamiento de sectores:** $\mathcal{K}$ preserva la descomposición $\mathrm{Sym}^+(4)\oplus\mathfrak{so}(4)$. Este es un supuesto simplificador (análogo a excluir efectos piezoeléctricos), no una restricción fundamental del GSF. Los términos cruzados $\mathcal{K}_{sa}$ entre sectores son posibles en principio; se excluyen como el modelo mínimo más conservador.

*Identificación bajo ansätze:* $\mu > 0$ por C3; $\kappa, \nu \geq 0$ por C2. Los coeficientes $\kappa, \mu, \nu$ son parámetros estructurales específicos de la clase, no constantes universales del GSF.

**Esta es la Aproximación Armónica** — válida solo para pequeñas desviaciones $\|\delta\Gamma\| \ll 1$. Se rompe cerca de $\rho_c$ y lejos de $\xi^*$.

**Casos especiales:** $\kappa=\nu=0$: estructuralmente mínima (solo sector simétrico). $\nu > 0$: penaliza las desviaciones del campo. $\kappa > 0$: distingue los modos volumétricos (bulk) de los de cizalla (shear).

---

## 11.5 Consecuencias para la Ley de Evolución

**Gradiente de P:**
$$\nabla_{\Gamma_s} P = \kappa\,\mathrm{tr}(\delta\Gamma_s)\cdot I + \mu\,\delta\Gamma_s, \qquad \nabla_{\Gamma_a} P = \nu\,\delta\Gamma_a$$

**Regla de la cadena al espacio $\xi$:**
$$\nabla_\xi P = \left(\frac{\partial\Gamma}{\partial\xi}\right)^T \nabla_\Gamma P$$

La fuerza $\dot\xi = -M\nabla_\xi P$ se descompone en: corrección volumétrica ($\propto \kappa\,\mathrm{tr}(\delta\Gamma_s)$), corrección selectiva de modo ($\propto \mu\,\delta\Gamma_s$), y corrección de campo ($\propto \nu\,\Gamma_s^{-1}(\partial\Gamma_a/\partial\xi)^T\delta\Gamma_a$). La dependencia formal de $\alpha_\mathbf{I}$, $\beta_\mathbf{I}$ (Cap. 10 §10.5.2) respecto a $\kappa,\mu,\nu$ es ahora expresable a través de $\partial\Gamma/\partial\xi$ — pero los coeficientes no están identificados numéricamente (Jacobiano abierto).

**Corolario 11.1 (Cierre de T4 — unicidad local).** El Hessiano de $\widetilde{P}$ en el sector simétrico es el operador:
$$H_{\widetilde{P},s}[X] = \kappa\,\mathrm{tr}(X)\cdot I + \mu\,X \;=\; \mu\,I_{\mathrm{op}} + 4\kappa\,\Pi_{\mathrm{tr}}$$
donde $\Pi_{\mathrm{tr}}[X] = \frac{\mathrm{tr}(X)}{4}I$. *(Factor 4: para una matriz $4\times4$, $\mathrm{tr}(I_4) = 4$, por lo que $H[I_4] = (4\kappa+\mu)I_4$.)*

Autovalores: $\mu + 4\kappa$ en el subespacio de la traza (1D), $\mu$ en el subespacio simétrico sin traza (9D). Ambos estrictamente positivos ($\mu > 0$, $\kappa \geq 0$) ⟹ $H_{\widetilde{P},s} \succ 0$ ⟹ $\xi^*$ es genéricamente el único mínimo local en $\rho \neq \rho_c$.

*Advertencia sobre la unicidad global:* **Criterio de Inyectividad Estructural (SIC)** — se requiere que $D\Gamma(\xi^*)$ sea de rango completo (inmersión local inyectiva) para inferir la unicidad local en el espacio $\xi$ a partir de la convexidad en el espacio $\Gamma$. La unicidad global requiere adicionalmente la inyectividad de $\Gamma(\xi)$ en $D_\xi(\rho)$ — depende del mapa explícito; la inyectividad local se verificó en el Cap. 8 Prop. 8.2; el análisis global (ambigüedad $\mathbb{Z}_2$) permanece abierto — Cap. 8 §8.10.

**Proposición 11.1a (Monotonía de Lyapunov).** *(Consecuencia del Cap. 10 Teo. 10.1 — reformulada para la $P$ específica de la Prop. 11.1; no es un resultado independiente).*

Bajo $\dot\xi = -M\nabla_\xi P$, $M \succ 0$: $\dot P = -\nabla P^T M\nabla P \leq 0$, con igualdad si y solo si $\nabla P = 0$. Bajo las condiciones de LaSalle (H3 del Cap. 10 Teo. 10.1), las trayectorias convergen a $\{\xi^*\}$ genéricamente en $\rho \neq \rho_c$.

**Observación geométrica.** El paisaje de propósito en el espacio $\xi$ es inducido desde el espacio $\Gamma$ vía $P = \widetilde{P} \circ \Gamma$. La movilidad inducida en el espacio $\Gamma$:
$$M_\Gamma := D\Gamma(\xi)\,M\,D\Gamma(\xi)^T$$
es distinta de $\mathcal{K}$ (curvatura del potencial). Las propiedades globales de $P$ en el espacio $\xi$ no pueden leerse de las propiedades locales de $\widetilde{P}$ en el espacio $\Gamma$ sin conocer $\Gamma(\cdot)$.

---

## 11.6 Estatus Epistémico de los Parámetros

$P$, como se define en la Prop. 11.1, es un postulado estructural al nivel del propósito (no derivado de un Lagrangiano). Se justifica por: (1) selección por simetría (forma mínima invariante bajo G(3) a orden cuadrático), (2) corrección estructural (C1–C4 satisfechos por construcción), (3) compatibilidad con el Cap. 10 (la estructura de Lyapunov del Teo. 10.1 se mantiene para cualquier $P$ que satisfaga C3).

**Abierto:** valores de $\kappa, \mu, \nu$ para clases específicas de UoC; términos de orden superior para el análisis de bifurcación; principio variacional del cual $P$ podría derivarse (por encima del nivel Lagrangiano del Cap. 10).

---

## 11.7 Conexión con la Termodinámica Estructural

La expansión cuadrática de $P$ cerca de $\Gamma^*$ es formalmente análoga a una expansión de energía libre de Landau. La analogía es estructural — la producción de entropía y el promediado (coarse-graining) no se abordan en la Parte I. La ausencia de términos de orden impar es una característica del truncamiento cuadrático, no una simetría $\mathbb{Z}_2$ derivada.

**Proposición 11.2 (Forma crítica de Landau).** *(Escenario candidato — hipótesis de transición de segundo orden; no derivada de C1–C4. Los escenarios de primer orden son compatibles con C1–C4; ver Observación abajo).*

Se asume que el coeficiente $\mu = \mu(\rho)$ satisface $\mu(\rho) > 0$ para $\rho \neq \rho_c$ y $\mu(\rho_c) = 0$. En $\rho_c$: $H_{\widetilde{P},s}$ pierde su definición positiva, C3 falla, $\xi^*$ puede bifurcar. Expansión completa cerca de $\rho_c$ (escenario de segundo orden, $b > 0$):

$$P(\Gamma;\rho) \approx \frac{\mu(\rho)}{2}\|\delta\Gamma_s\|_F^2 + \frac{b}{4}\|\delta\Gamma_s\|_F^4 + \cdots$$

**Observación (escenario de primer orden).** Si $b < 0$, se necesita un término de sexto orden $c\|\delta\Gamma_s\|_F^6$ ($c>0$) — estructura de doble pozo, salto tipo calor latente. Si la transición ego→soul es de primer o segundo orden es una cuestión empírica específica de la clase. Nota: $b>0$ es un postulado de Landau oculto (no derivado de C1–C4).

**Condiciones de regularidad requeridas:** $\mu \in C^1$ cerca de $\rho_c$; transversalidad $\mu'(\rho_c) \neq 0$ (el término de masa cruza el cero a una tasa no nula). Sin transversalidad, el tipo de bifurcación no está determinado por la expansión $|\delta\Gamma_s|^2$–$|\delta\Gamma_s|^4$.

**Susceptibilidad estructural.** $\chi_s \sim 1/\mu(\rho)$. A medida que $\rho \to \rho_c$: $\chi_s \to \infty$ — la UoC se vuelve infinitamente susceptible a modulaciones infinitesimales de $\Gamma_E$. Análogo estructural de la ralentización crítica (critical slowing-down).

---

## 11.7b El Propósito Fuera del Estado de Coherencia

Tres roles distintos de $P(\Gamma)$ según el régimen:

- **(i) Rol de atractor** — interior de $\mathcal{M}_{\mathrm{adm}}$, $\det(\Gamma) > 0$: $P$ es Lyapunov; el sistema desciende $\nabla P$ hacia $\Gamma^*$. El propósito es *activo* en la EOM.
- **(ii) Rol latente** — frontera $\partial\mathcal{M}(\Gamma)$, $\det(\Gamma) = 0$: el término adjugate se anula (Lemma 15.1, Parte II), la fuerza atractora desaparece, la dinámica está gobernada por $\|\Gamma\|_F^2$ solo (régimen de onda, Cap. 15 §15.1). $P$ permanece definido pero no impulsa la evolución. El propósito es *latente* — presente en el paisaje del potencial, inactivo en las ecuaciones de movimiento.
- **(iii) Rol generativo** — transición entre UdCs: cuando una UdC coherente se degenera y se forma una sucesora (Cap. 12 §12.3.2 de Parte II), $P$ se re-instancia con el atractor de la sucesora $\Gamma^*_{\mathrm{new}}$ — típicamente distinto del predecesor. El propósito no es propiedad permanente de una identidad UdC sino característica estructural de cada configuración de coherencia que el sustrato sostiene.

Conexión con T8 lectura (D): la misma UdC atraviesa regímenes (propósito activo → latente → re-instanciado) sin que su identidad se identifique con ningún régimen. El potencial estructural es uno; el régimen determina cómo actúa.

---

## 11.8 Tabla de Resumen

| Ítem | Estatus |
|------|--------|
| Base cuadrática invariante bajo G(3) (§11.3) | **Identificada** — bajo rep-G(3) establecida (Cap. 8) + conjugación isotrópica |
| Forma admisible mínima Prop. 11.1 | **Seleccionada** — bajo C1–C4 + isotropía + desacoplamiento de sectores; no es única solo por C1–C4 |
| Coeficientes $\kappa, \mu, \nu$ | $\kappa=-1$: **Derivado en la Parte II** (Cap. 13, ausencia de fantasmas). $\mu(\rho)=2(\rho/\rho_{\mathrm{GR}})^2$: **Derivado en la Parte II** (Cap. 14, T1). $\nu$: aún postulado |
| Representación ortogonal $\varrho$ de G(3) | **Establecida** — Cap. 8 §8.5–8.8 (no es un supuesto) |
| Desacoplamiento de sectores de $\mathcal{K}$ | **Ansatz** — simplificador; acoplamiento entre sectores posible en principio |
| Dependencia de $\Gamma^*(\rho)$ respecto a $\rho$ | **Derivada en la Parte II** — T1 da $\Gamma(\rho) = \Gamma_0/\rho$ (Cap. 14 Teo. 14.1) |
| Jacobiano Atributo-a-Γ $\partial\Gamma/\partial\xi$ | **Abierto** — requiere dinámica de atributos explícita |
| Modo de traza de autovalores de $H_{\widetilde{P},s}$ | $\mu + 4\kappa$ (1D); $\mu$ (9D sin traza) — ambos > 0 |
| Unicidad local de $\xi^*$ en el espacio $\Gamma$ | **Condicional** — requiere SIC (rango completo de $D\Gamma(\xi^*)$) |
| Unicidad global de $\xi^*$ en el espacio $\xi$ | **Abierto** — requiere inyectividad de $\Gamma(\xi)$ en $D_\xi(\rho)$ |
| Dependencia formal de $\alpha_\mathbf{I}, \beta_\mathbf{I}$ (T3 parcial) | **Expresada** — no identificada numéricamente (Jacobiano abierto) |
| Landau: $\mu(\rho_c)=0$ | **Se localiza en $\rho_c \to 0$** dada la derivada $\mu(\rho)=2(\rho/\rho_{\mathrm{GR}})^2$ — el punto crítico es el límite $\rho \to 0$, no un nivel interior finito |
| Landau: $b > 0$ (escenario de segundo orden) | **Postulado** (supuesto de Landau oculto; aún abierto) |
| Validez de la Aproximación Armónica | **Solo para $\delta\Gamma$ pequeño** — se rompe cerca de $\rho_c$ y lejos de $\xi^*$ |
| Cierre de T4 (unicidad) | **Localmente condicional** (SIC verificado Cap. 8 Prop. 8.2 + rep-G(3) establecida Cap. 8); global abierto |

---

## 11.9 Preguntas Abiertas

- **Derivación variacional de $P$**: ¿existe un principio de acción de nivel superior del cual se pueda derivar $P$?
- **Correcciones no lineales cerca de $\rho_c$**: se necesitan términos cúbicos/cuárticos para determinar el orden de la transición.
- **Propósito multi-UoC**: $P_U(\Gamma_U)$ para un compuesto $U = A \cup B$ no es $P_A + P_B$ en general — requiere extensión a sistemas composicionales (Cap. 7).
- **Restricciones empíricas**: la relación $\mu/\kappa$ (error de coordinación de cizalla vs. volumétrico) es en principio medible a partir de la dinámica estructural.
- **Identificabilidad del objetivo**: ¿bajo qué condiciones es $\Gamma^*(\rho)$ inferible de manera única a partir de las trayectorias observadas?

---

*Fin del Capítulo 11 (condensado)*
