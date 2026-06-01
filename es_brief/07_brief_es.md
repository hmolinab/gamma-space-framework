# Capítulo 7: Operaciones Composicionales
*Versión condensada — fuente: Cap. 7 del GSF completo*

---

## 7.1 Motivación

El Cap. 5 estableció $\Gamma$ como el objeto estructural de una sola UoC. La mayoría de los sistemas de interés —organismos, personas, sociedades— son compuestos. Este capítulo introduce nueve operaciones formales sobre matrices de configuración y espacios de atributos. Cada operación especifica: (1) qué sucede con los espacios de atributos $\{S, A, I, R\}$; (2) qué sucede con $\Gamma$; (3) si las sub-UoCs permanecen **distinguibles** (Definición 7.1); (4) la direccionalidad estructural (reversible / irreversible / terminal).

**Estatus epistémico.** Las identificaciones con fenómenos biológicos o psicológicos (fusión → organismo, reproducción → división celular, etc.) son correspondencias, no derivaciones. Las restricciones termodinámicas (§7.9) son conjeturas estructurales pendientes de un $P(\Gamma)$ explícito; la estructura algebraica de cada operación se sigue del Cap. 5.

*Nota sobre la reducción futura.* Las nueve operaciones pueden reducirse a un conjunto central más pequeño bajo un análisis más profundo. Empíricamente, la naturaleza muestra principalmente fusión/integración (célula → organismo); los sistemas sociales muestran principalmente unión/suma. Las operaciones restantes pueden ser casos especiales o regímenes límite de dos o tres primitivas. Esta reducción se pospone para la Parte III.

---

## 7.2 El Criterio de Distinguibilidad

**Definición 7.1 (Distinguibilidad).** $A$, $B$ son **estructuralmente distinguibles dentro** del compuesto $C$ si existen proyecciones $\pi_A, \pi_B: V_C \to V_C$ que satisfacen:
1. $\pi_A + \pi_B = \mathrm{Id}_{V_C}$ (completitud)
2. $\pi_A^2 = \pi_A$, $\pi_B^2 = \pi_B$ (idempotencia)
3. $\|\pi_A \Gamma_C \pi_A^T - \Gamma_A\|_F \leq \epsilon_{AB} = \|C_{AB}\|_F$ y lo mismo para $B$ (recuperación estructural — exacta cuando $C_{AB} = 0$)

La distinguibilidad admite grados: un $C_{AB}$ grande significa que las $\Gamma_A, \Gamma_B$ recuperadas se desvían significativamente de sus valores aislados.

---

## 7.2.1 Condiciones de Compatibilidad de Nivel Estructural

**Definición 7.2 ($\rho$-Proximidad).** $|\rho_A - \rho_B| \leq \delta_\rho$ para un umbral estructural $\delta_\rho > 0$.

**Postulado 7.1 (Condiciones de Nivel).** *(Postulados estructurales; la derivación a partir de $P(\Gamma)$ está abierta — OQ7.1.)*

| Operación | Condición $\rho$ requerida | Nivel de salida |
|-----------|---------------------|-----------------|
| Unión | $\rho$-proximidad | $\rho_U = \max(\rho_A, \rho_B)$ |
| Acoplamiento | $\rho$-proximidad preferida; $\|C_{AB}\| \to 0$ con gran brecha de $\rho$ | cada una retiene su propia $\rho$ |
| Fusión | $\rho$-proximidad ($\delta_F$) | $\rho_F \geq \max(\rho_A, \rho_B)$ |
| Anidamiento | brecha estricta: $\rho_A - \rho_B \geq \delta_\text{nest} > 0$ | $B$ retiene $\rho_B$ bajo el anfitrión $\rho_A$ |
| Absorción | $\rho_A \geq \rho_B$ | $\rho_{A'} \geq \rho_A$ |
| Reproducción | ninguna | $\rho_B^{(0)} \approx \rho_A$ |
| Resonancia | $\rho$-proximidad | cada una retiene su propia $\rho$ |
| Fisión, Desacoplamiento, Disolución | ninguna | — |

**Justificación**: Se espera que $C_{AB}$ decaiga con la separación de $\rho$ (hipótesis: $C_{AB} \sim e^{-|\rho_A-\rho_B|/\delta_\rho}$), a partir de la estructura invariante bajo $G(3)$ de $P(\Gamma)$ (Cap. 11 §11.4). Las operaciones jerárquicas (anidamiento, absorción) requieren una brecha de nivel anfitrión-subordinado. Un **postulado de mediación** establece que las operaciones a través de $|\rho_A - \rho_B| > \delta_\rho$ requieren un mediador UoC intermedio.

---

## 7.3 Operaciones que Preservan la Distinguibilidad

### 7.3.1 Unión

**Definición 7.3 (Unión).** Compuesto $U = A \cup B$ con:
- $V_U = V_A \oplus V_B$ (dimensión finita, estructura $G(3)$ compatible)
- $\Gamma_U = \begin{pmatrix} \Gamma_A & C_{AB} \\ C_{BA} & \Gamma_B \end{pmatrix}$, $C_{AB} = C_{BA}^T$ — objeto primario; $\Gamma_A, \Gamma_B$ recuperadas mediante proyecciones canónicas
- $A, B$ estructuralmente distinguibles dentro de $U$

Simétrica; reversible cuando $C_{AB}$ es pequeño — se sigue de la definición: $C_{AB} \to 0$ recupera dos UoCs independientes.

### 7.3.2 Anidamiento

**Definición 7.4 (Anidamiento).** $B \triangleleft A$ si:
- $V_B \subsetneq V_A$ es un **subespacio estable**: $\Gamma_A V_B \subseteq V_B$
- $\Gamma_B = \Gamma_A\big|_{V_B}$
- $\rho_A - \rho_B \geq \delta_\text{nest} > 0$

Asimétrica; el anfitrión modula las condiciones de contorno de la UoC anidada. *La contracción de dominio del Cap. 4 §4.2.2 proporciona la estructura de anidamiento natural: $D_X(\rho_B) \subsetneq D_X(\rho_A)$ para $\rho_B > \rho_A$ — ver Observación 7.1 en §7.11.*

### 7.3.3 Acoplamiento

**Definición 7.5 (Acoplamiento).** $A \rightleftharpoons B$ si $\Gamma_E^{(A \to B)} \neq 0$ y $\Gamma_E^{(B \to A)} \neq 0$ sin formar un compuesto. Cada una retiene su propia $\Gamma$, $\rho$, $\xi^*$.

Interacción estructural más débil. En acoplamiento cero: evolución independiente. En acoplamiento máximo: se aproxima al régimen de unión.

---

## 7.4 Operaciones de Fusión

### 7.4.1 Fusión

**Definición 7.6 (Fusión).** Nueva UoC $F$ a partir de $A, B$ tal que:
- $\{S,A,I,R\}_F$ son atributos emergentes (no sumas directas de los originales)
- $\Gamma_F$ no tiene descomposición en bloques que recupere $\Gamma_A, \Gamma_B$ ($A, B$ indistinguibles dentro de $F$)
- $A, B$ dejan de existir como UoCs separadas

Irreversible en general.

### 7.4.2 Absorción

**Definición 7.7 (Absorción).** $A \leftarrow B$: $A$ persiste modificada ($\Gamma_A \to \Gamma_{A'}$); $B$ pierde su identidad estructural. Límite asimétrico de la fusión.

---

## 7.5 Operaciones de Separación

### 7.5.1 Fisión

**Definición 7.8 (Fisión).** $C$ se separa en $\{A, B, \ldots\}$: $V_A \oplus V_B \oplus \cdots = V_C$ (exhaustivo); $\Gamma_A = \pi_A \Gamma_C \pi_A^T$ más normalización diagonal; $C$ deja de existir.

**Conservación estructural** *(conjetura)*: $\sum_i P(\Gamma_i) \leq P(\Gamma_C)$ — subaditividad de $P$ bajo restricción de bloques. No derivada en la Parte I.

### 7.5.2 Desacoplamiento

**Definición 7.9 (Desacoplamiento).** $\Gamma_E^{(A \to B)} \to 0$ y $\Gamma_E^{(B \to A)} \to 0$; ambas persisten. Inversa del acoplamiento.

---

## 7.6 Operaciones Generativas

### 7.6.1 Reproducción

**Definición 7.10 (Reproducción).** $A$ genera una nueva UoC $B$ con $\Gamma_B^{(0)} \approx \Gamma_A(\xi^*_A)$. $A$ persiste. $B$ evoluciona independientemente.

**Herencia estructural**: $\|\Gamma_B^{(0)} - \Gamma_A\|_F$ mide la fidelidad; herencia parcial = variación estructural (análogo GSF de la mutación).

---

## 7.7 Operación Terminal

### 7.7.1 Disolución

**Definición 7.11 (Disolución).** $A$ se disuelve cuando $F_\text{ext} \to 0$: el flujo de gradiente $\dot\xi = -M\nabla P$ (Cap. 10 Teorema 10.1) conduce a $\xi$ hacia el conjunto crítico de $P$. Bajo coercitividad (Cap. 9 §9.5 H3), la UoC converge al mínimo global de $P$. Terminal y no generativa: no se producen nuevos atractores.

*(La identificación del mínimo global con el "atractor del alma" a bajo $\rho$ es una correspondencia candidata — Cap. 9 §9.7 — no un resultado formal.)*

---

## 7.8 Estados Sincrónicos

### 7.8.1 Resonancia

**Definición 7.12 (Resonancia Estructural).** $A, B$ en **resonancia estructural** si:
1. Son $\rho$-próximas: $|\rho_A - \rho_B| \leq \delta_\rho$
2. Los atractores se alinean temporalmente: $\Gamma^*_A(t) \approx \Gamma^*_B(t)$ para $t \in [t_0, t_1]$ — sin fusión ni acoplamiento persistente

Transitoria y reversible. La conjetura de que la alineación de atractores implica la co-minimización de la producción de entropía estructural requiere establecer el vínculo entre la proximidad de atractores y $\sigma_\text{struct}$ — no derivado en la Parte I.

---

## 7.9 Restricciones Termodinámicas

**Proposición 7.1 (Direccionalidad Estructural — derivación parcial).**

1. **Fusión/absorción**: la entropía no decrece bajo la mezcla *(conjetura — requiere $\sigma_\text{struct}$)*.
2. **Fisión**: requiere $P(\Gamma_C) > \sum_i P(\Gamma_i)$ *(conjetura)*.
3. **Unión**: reversible con $\|C_{AB}\|$ pequeño — *derivado de la Definición 7.3*.
4. **Reproducción**: cuesta trabajo estructural de $A$ *(conjetura)*.
5. **Disolución**: admisible bajo dinámica autónoma — *derivado del Cap. 10 Teorema 10.1* (flujo de gradiente al conjunto crítico bajo coercitividad).

**Observación**: Las operaciones no espontáneas (reproducción, mantenimiento del anidamiento, acoplamiento sostenido) requieren $F_\text{ext} \neq 0$ *(conjetura estructural)*.

---

## 7.10 Tabla Resumen

| Operación | UoCs de origen persisten | Distinguible | Reversible | Carácter termodinámico |
|-----------|---|---|---|---|
| Unión | Sí (ambas) | Sí | Sí | Reversible si $\|C_{AB}\|$ es pequeño — derivado |
| Anidamiento | Sí (ambas) | Sí | Sí | Requiere impulso del anfitrión $F_\text{ext}$ |
| Acoplamiento | Sí (ambas) | Sí | Sí | Requiere $\Gamma_E \neq 0$ mutuo |
| Fusión | No (ambas se funden) | No | No (general) | Entropía no decreciente (conjeturado) |
| Absorción | Sí (solo anfitrión) | No | No | Entropía no decreciente (conjeturado) |
| Fisión | No (el padre se divide) | Sí (nuevas sub-UoCs) | No (general) | Requiere $\Delta P > 0$ (conjeturado) |
| Desacoplamiento | Sí (ambas) | Sí | Sí | Autónomo si $F_\text{ext} \to 0$ |
| Reproducción | Sí (padre) | Sí (nueva UoC) | — | Cuesta trabajo estructural (conjeturado) |
| Disolución | No (cesa) | — | No | Terminal; derivado del Cap. 10 Teo. 10.1 |
| Resonancia | Sí (ambas) | Sí | Sí | Alineación de atractores; co-minimización de σ conjeturada |

---

## 7.11 Preguntas Abiertas

- **OQ7.1 — Umbrales de nivel**: $\delta_\rho$, $\delta_F$, $\delta_\text{nest}$ no derivados; dependen de $P(\Gamma)$ y del espectro de $\Gamma_s$. Derivarlos del Lagrangiano del Cap. 10 es un problema abierto.
- **Criterio de fusión**: condición formal para la transición de unión a fusión a medida que $\|C_{AB}\|$ crece — transición de fase estructural.
- **Composiciones de orden superior**: operaciones $n$-arias y leyes de conservación sobre $\Gamma$ compuesto.
- **Duración de la resonancia**: la ventana $[t_0, t_1]$ requiere dinámica estocástica explícita y ruido $D(\rho)$.
- **OQ7.2 — La UoC compuesta psicológica**: alma ($\rho \to 0^+$), ego y cuerpo en diferentes niveles de $\rho$.

  **Observación 7.1 ($\oplus$ como anidamiento iterado — derivado).** El operador de copresencia $\oplus$ de la Notación 5.1 del Cap. 4 puede definirse como un anidamiento iterado: $\text{UoC}(\rho_\text{cuerpo}) \triangleleft \text{UoC}(\rho_\text{ego}) \triangleleft \text{UoC}(\rho_\text{alma})$. La estructura de subespacio estable es proporcionada por el Postulado 4.2 del Cap. 4 (contracción de dominio): $D_X(\rho_\text{cuerpo}) \subsetneq D_X(\rho_\text{ego}) \subsetneq D_X(\rho_\text{alma}) = \mathcal{V}_X$ para todo $X$. La condición de brecha de $\rho$ del Postulado 7.1 se satisface por construcción. Lo que permanece abierto: la fenomenología de la unidad percibida (probablemente una propiedad de la modulación de $\Gamma_E$).

---

*Fin del Capítulo 7 (condensado)*
