# Capítulo 4: ρ y Auto-similitud Estructural
*Versión condensada — fuente: Cap. 4 del GSF completo*

---

## 4.1 Postulado Ontológico

**Postulado 4.1 (Jerarquía Recursiva Auto-similar).**
La estructura ontológica de una UdC —el objeto algebraico $G(3)$ con variables intrínsecas $\{S, \mathbf{A}, \mathbf{I}, \mathbf{R}\}$ y operaciones inherentes Fuerza = $S\mathbf{A}$ y Campo = $\mathbf{I}\times\mathbf{R}$— es invariante ante cambios en $\rho$. Esta invarianza se mantiene independientemente de si el nivel epistemológico es nulo (unidad de coherencia estructural) o positivo (unidad de conciencia). Cada UdC genera un estado organizacional de orden superior que constituye el sustrato para una UdC en el siguiente nivel. La jerarquía es **recursivamente generativa**: no repite un patrón; *produce* la siguiente iteración a partir de la anterior.

*Lectura como unidad de conciencia:* el estado organizacional de orden superior generado en cada nivel es la conciencia emergente. *Lectura como unidad de coherencia:* es la organización estructural emergente sin modulación epistemológica.

*Nota sobre la invarianza.* La invarianza del tipo algebraico ($\text{UdC}(\rho_1) \cong \text{UdC}(\rho_2)$) se deduce del Lema 3.1 del Cap. 3 — $G(3)$ no depende de $\rho$. El postulado sustantivo es únicamente la **afirmación generativa**.

*Holón / holonarquía.* Cada UdC es un **holón** (Koestler 1967): simultáneamente una unidad estructural completa y un componente del nivel superior. La jerarquía es una **holonarquía**. La jerarquía tiene un carácter fractal (mismo tipo algebraico en cada escala) pero no es fractal en el sentido métrico-geométrico.

**Lo que se postula:**
1. Invarianza estructural: la forma algebraica $G(3)$ es la misma en cada nivel de $\rho$.
2. Generatividad recursiva: cada UdC en el nivel $n$ produce el sustrato para el nivel $n+1$.

**Lo que no se postula:** la naturaleza del sustrato; la dirección de la causalidad (descendente o ascendente — ambas son compatibles); el número de niveles o la existencia de un primer o último término.

*Falsabilidad*: el postulado se falsa bajo cualquiera de tres condiciones (C1–C3, Observación 1.1 del Cap. 1): (C1) una propiedad irreducible en algún nivel se resiste al mapeo en los cuatro espacios; (C2) dos atributos son mutuamente derivables dentro de $G(3)$; (C3) una entidad coherente en algún nivel admite dos asignaciones de espacios no equivalentes que son estructuralmente indistinguibles — la correspondencia específica del nivel está subdeterminada.

*Nota terminológica*: la jerarquía se denomina "recursiva auto-similar" —no "fractal"— para evitar importar la maquinaria de espacios métricos de la teoría fractal (dimensión de Hausdorff, sistemas de funciones iteradas, invarianza de escala continua) que no se aplica aquí. La auto-similitud es algebraica y estructural, no métrica.

---

## 4.2 Formalismo Matemático

### 4.2.1 ρ como Factor de Forma Contextual

$\rho$ no es una variable intrínseca de una UdC. Es una propiedad del **contexto** —el trasfondo establecido por el nivel de organización inmediatamente superior. $\rho$ parametriza las restricciones en el espacio de configuración de la UdC impuestas por el trasfondo, sin alterar el espacio de configuración en sí mismo.

**Rango de ρ: $(0, \infty)$.** $\rho = 0$ es un ideal asintótico — ningún sistema opera sin fricción contextual. No existe un límite superior de principio: $\rho \to \infty$ describe el colapso total de los grados de libertad operativos, no un máximo fijo. Donde los capítulos escriben $\rho \in [0,1]$, se trata de una normalización operativa para implementaciones, no del dominio teórico.

Para cada variable intrínseca $X \in \{S, \mathbf{A}, \mathbf{I}, \mathbf{R}\}$, $\rho$ determina un dominio de expresión:

$$D_X(\rho) \subseteq \mathcal{V}_X$$

donde $\mathcal{V}_X$ es el espacio completo de esa variable. El mecanismo por el cual el estado de la UdC de nivel superior determina el valor específico de $\rho$ no está formalizado (§4.5).

### 4.2.2 Contracción del Dominio

**Postulado 4.2 (Contracción del Dominio).** El dominio de expresión se contrae monótonamente a medida que $\rho$ aumenta:

$$\rho_1 < \rho_2 \implies D_X(\rho_1) \supseteq D_X(\rho_2) \quad \forall X$$

Este es un postulado, no un resultado derivado. La contracción monótona es la hipótesis mínima consistente con el gradiente fenomenológico de la libertad al determinismo; la dependencia no monótona o discontinua no está excluida y requeriría revisión.

**Casos límite:**
- $\rho \to 0$: $D_X(\rho) \to \mathcal{V}_X$ — dominio completo, sin restricción contextual.
- $\rho \to \infty$: $D_X(\rho) \to \{x_0\}$ — el dominio colapsa a un punto fijo $x_0$ determinado por el contexto; no quedan grados de libertad operativos.

Una medida independiente de la libertad operativa es el volumen $\text{vol}(D_X(\rho))$, que es monótonamente decreciente según este postulado.

### 4.2.3 Isomorfismo Estructural

Dado que $G(3)$ es invariante bajo $\rho$, cualquier par de UdCs en diferentes niveles de $\rho$ son estructuralmente isomorfos **como tipos algebraicos**:

$$\text{UdC}(\rho_1) \cong \text{UdC}(\rho_2) \quad \forall \rho_1, \rho_2$$

$\phi_{\rho_1,\rho_2}$ es un isomorfismo de la estructura algebraica $G(3)$ — no de los estados. Dos UdCs en diferentes niveles instancian el mismo tipo algebraico con diferentes valores de variables en diferentes dominios, como dos programas con la misma firma de tipo ejecutándose con diferentes entradas.

*Lo que rompe la simetría entre niveles*: no es el álgebra (invariante) sino el dominio $D_X(\rho)$. En $\rho_{\text{alma}}$ las variables oscilan sobre el $\mathcal{V}_X$ completo; en $\rho_{\text{cuerpo}}$ están restringidas a un $D_X(\rho_{\text{cuerpo}})$ mucho más pequeño. La diferencia entre un alma y una célula reside en el rango operativo, no en el tipo algebraico.

El isomorfismo preserva las cuatro variables, la Fuerza, el Campo y la clausura algebraica. No preserva los valores de las variables, las expresiones cualitativas o los atractores teleológicos.

**Lo invariante es el tipo algebraico; lo variante es el dominio de instanciación.**

### 4.2.4 El Operador Recursivo

El operador recursivo **$\Omega$** mapea una UdC en el nivel $n$ a la UdC en el nivel $n+1$:

$$\Omega: \text{UdC}_n \mapsto \text{UdC}_{n+1}$$

$$C_{n+1} = \mathcal{R}(\text{UdC}_n), \qquad \text{UdC}_{n+1} = \text{UdC}(C_{n+1},\, \rho_{n+1})$$

La cadena recursiva:

$$C_0 \xrightarrow{\Omega} \text{UdC}_1 \xrightarrow{\mathcal{R}} C_1 \xrightarrow{\Omega} \text{UdC}_2 \xrightarrow{\mathcal{R}} C_2 \xrightarrow{\Omega} \cdots$$

*Nota notacional*: $C_0$ es una conveniencia notacional, no un postulado de un primer término.

**Sobre $\mathcal{R}$.** Como firma de tipo mínima: $\mathcal{R}: \text{UdC}_n \to C_{n+1}$, donde $C_{n+1}$ es un sustrato capaz de soportar una UdC en el siguiente nivel. Lo que $\mathcal{R}$ computa a partir de $\text{UdC}_n$ —ya sea un funcional de $\xi$, de $\Gamma(\xi)$, o del nivel teleológico— es la cuestión estructural que $\Gamma_E$ (Cap. 1 §1.5.1) y la función de propósito (Cap. 1) están diseñadas para recibir. Su constitución interna permanece abierta (§4.5).

$\Omega$ preserva la estructura: $\text{UdC}_n \cong \text{UdC}_{n+1}$ para todo $n$ (§4.2.3). La jerarquía reproduce el mismo tipo algebraico $G(3)$ en cada aplicación. *Esto es descriptivo, no un teorema de punto fijo* — si $\Omega$ tiene puntos fijos formales es una pregunta abierta (§4.5).

---

## 4.3 Ejemplos Interpretativos

### 4.3.1 La Jerarquía Personal

$$\text{Persona} = \text{UdC}(\rho_{\text{alma}}) \oplus \text{UdC}(\rho_{\text{ego}}) \oplus \text{UdC}(\rho_{\text{cuerpo}})$$

donde $\oplus$ denota co-presencia (Notación 5.1 — marcador de posición; formalizado en el Cap. 7).

| Componente | S | **A** | **I** | **R** | Fuerza | Campo | Propósito |
|-----------|---|-------|-------|-------|-------|-------|---------|
| UdC($\rho_{\text{alma}}$) | Presencia pura | Libre albedrío puro | Creativo | Inter-evolución | Voluntad | Amor | Sabiduría |
| UdC($\rho_{\text{ego}}$) | Identidad referenciada | Elección condicionada | Polaridad reactiva | Búsqueda de seguridad | Control | Miedo | Autopreservación |
| UdC($\rho_{\text{cuerpo}}$) | Organismo | Regulación instintiva | Impulso homeostático | Simbiosis | Homeostasis | Campo vital | Supervivencia |

**Importante**: Las etiquetas de las columnas Fuerza, Campo y Propósito (voluntad, amor, sabiduría; control, miedo; homeostasis, supervivencia) son **interpretaciones fenomenológicas** de las variables estructurales en cada nivel de $\rho$ — no son propiedades derivadas algebraicamente. La estructura algebraica $G(3)$ es idéntica en todas las filas; lo que varía es el dominio $D_X(\rho)$ y la expresión cualitativa en el nivel epistemológico.

### 4.3.2 La Jerarquía Cósmica *(Especulativa)*

Una posible lectura de $\Omega$ a través de las escalas:

$$C_0 \;\xrightarrow{\Omega}\; \text{UdC}_{\text{alma}} \;\xrightarrow{\Omega}\; \text{UdC}_{\text{espaciotiempo}} \;\xrightarrow{\Omega}\; \text{UdC}_{\text{cosmos}} \;\xrightarrow{\Omega}\; \text{UdC}_{\text{biología}} \;\xrightarrow{\Omega}\; \text{UdC}_{\text{persona}} \;\xrightarrow{\Omega}\; \cdots$$

La misma jerarquía recorrida a la inversa —desde la materia hacia arriba hasta el alma— es igualmente compatible. El formalismo describe la estructura en cada nivel y las relaciones generativas entre niveles adyacentes; no fija una dirección de causalidad.

---

## 4.4 El Gradiente de ρ y Desarrollo Futuro

Dos direcciones para formalizar el gradiente:

**Termodinámica**: $\rho$ como fuerza de acoplamiento entre una UdC y su entorno. $\rho$ alto = acoplamiento fuerte, comportamiento determinado en gran medida por el baño térmico. Conecta la contracción del dominio con la energía libre y los estados restringidos.

**Relatividad**: la UdC del espaciotiempo genera el gradiente de $\rho$ de fondo. Un tratamiento relativista en el que $\rho$ sea una cantidad de campo que varía a través del espaciotiempo puede formalizar la geometría del gradiente.

---

## 4.5 Preguntas Abiertas

- **Constitución de $\mathcal{R}$**: ¿qué funcional de $\xi(t)$ o $\Gamma(\xi)$ computa $\mathcal{R}$? Esta es la cuestión central no resuelta de la jerarquía generativa.
- **$\Omega$**: su naturaleza matemática formal (¿funtor? ¿mónada? ¿endomorfismo categórico?) y si posee puntos fijos están abiertos.
- **Operador $\oplus$**: la co-presencia de múltiples UdCs en un compuesto requiere una definición formal. Se espera que se desarrolle a partir de los objetos algebraicos de los Cap. 5/Cap. 7.
- **Mecanismo que fija $\rho$**: ¿cómo determina el estado $\xi_{n-1}$ de la UdC de nivel superior a $\rho_n$? No se ha resuelto si $\rho$ es continuo o discreto.
- **Dominio operativo mínimo**: ¿en qué umbral de $D_X(\rho)$ la UdC deja de generar un Campo o Fuerza no triviales?
- **Profundidad de la jerarquía**: ¿termina? ¿Tiene $\Omega$ puntos fijos?

---

*Fin del Capítulo 4 (condensado)*
