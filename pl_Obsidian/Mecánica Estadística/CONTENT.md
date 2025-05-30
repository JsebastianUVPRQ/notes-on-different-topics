The typical syllabi for **Statistical Mechanics 1** and **Statistical Mechanics 2** courses, based on the provided sources, are as follows:

---

### **Statistical Mechanics 1**  
This course introduces foundational concepts and tools, often bridging thermodynamics and statistical approaches:  
1. **Review of Thermodynamics**:  
   - Laws of thermodynamics, entropy, temperature, and equilibrium.  
1. **Probability Theory**:
   - Random variables, distributions, and statistical ensembles.  
1. **Classical Statistical Mechanics**:  
   - Microcanonical, canonical, and grand canonical ensembles.  
   - Partition functions and their connection to thermodynamic quantities.  
1. **Ideal Systems**:
   - Ideal gases (classical and quantum).  
   - Equipartition theorem and Maxwell-Boltzmann statistics.  
1. **Interacting Systems**:
   - Phase transitions (e.g., Ising model) and mean-field theory.  
6. **Quantum Foundations**:
   - Basics of quantum statistical mechanics (e.g., Bose-Einstein and Fermi-Dirac distributions).  

---

### **Statistical Mechanics 2**  
This course deepens the study of complex systems and modern applications:  
1. **Advanced Quantum Statistical Mechanics**:
   - Indistinguishable particles (bosons/fermions), quantum gases, and degenerate systems.  
1. **Phase Transitions and Critical Phenomena**:
   - Scaling laws, universality, and renormalization group methods.  
1. **Statistical Physics of Fields**:
   - Field-theoretic approaches to phase transitions (e.g., Landau-Ginzburg theory).  
1. **Non-Equilibrium Systems** 
   - Transport phenomena, fluctuation-dissipation theorem, and stochastic processes.  
1. **Complex Systems** 
   - Networks, polymers, or biological systems (depending on the institution).  

---

### Key Differences:  
- **SM1** focuses on **foundational principles** (thermodynamics, ensembles, ideal systems) and bridges classical/quantum ideas.  
- **SM2** explores **advanced topics** (critical phenomena, field theory, non-equilibrium dynamics) and modern applications.  

---
---
---

# Unidad Nº1: CONCEPTOS BÁSICOS DE PROBABILIDAD

Esta unidad sienta las bases matemáticas necesarias, reconociendo que el comportamiento de sistemas con muchas partículas es inherentemente estadístico.

- **Conceptos básicos y definiciones fundamentales:** Se revisarán los axiomas de la probabilidad, espacio muestral, eventos, probabilidad condicional e independencia de eventos.
- **Técnicas de conteo:** Combinatoria y permutaciones serán esenciales para determinar el número de estados posibles en un sistema. Esto es crucial para definir la multiplicidad de estados (o peso estadístico) de un macroestado.
- **Distribuciones de variables aleatorias discretas y continuas:** Se estudiarán funciones de masa de probabilidad (P(x)) y funciones de densidad de probabilidad (f(x)), herramientas para describir la probabilidad de que una variable aleatoria tome ciertos valores.
- **Valores medios y fluctuaciones (desviación estándar):** La esperanza matemática (E[X]) y la varianza (Var(X) o σ2) o desviación estándar (σ) cuantifican el valor promedio de una magnitud y su dispersión alrededor de este promedio. Estos conceptos son análogos a las propiedades termodinámicas promedio y sus fluctuaciones en sistemas macroscópicos.
- **Función característica de una distribución:** Esta herramienta matemática, relacionada con la transformada de Fourier de la función de densidad de probabilidad, es útil para caracterizar distribuciones y calcular momentos.
- **Algunas distribuciones importantes de probabilidad: Binomial, Gauss, Poisson:** Se analizarán estas distribuciones fundamentales que aparecen en diversos contextos de la física estadística, como el número de partículas en un subvolumen (Poisson) o las fluctuaciones alrededor de un valor medio (Gauss, aplicable para grandes números).
- **Marcha aleatoria en una dimensión:** Un modelo simple pero potente para introducir ideas de procesos estocásticos y difusión, relevante para entender el movimiento de partículas en un medio.
- **Distribuciones de probabilidad de varias variables:** Se extiende el formalismo a sistemas con múltiples grados de libertad, considerando distribuciones de probabilidad conjunta.

# Unidad No 2: DESCRIPCIÓN ESTADÍSTICA DE UN SISTEMA FÍSICO

Aquí se comienza a aplicar la probabilidad a sistemas físicos.

- **Especificación microscópica del estado de un sistema y estados accesibles:** Se define el microestado como una descripción completa del estado de cada partícula (posiciones y momentos en mecánica clásica, o estado cuántico en mecánica cuántica). Los estados accesibles son aquellos compatibles con las restricciones macroscópicas.
- **Descripción macroscópica de un sistema y parámetros macroscópicos:** Se define el macroestado por variables macroscópicas (como energía total, volumen, número de partículas) que describen el sistema en promedio, sin detallar cada partícula.
- **Estados en equilibrio, estacionarios y fuera del equilibrio:** Se distingue entre estados donde las variables macroscópicas no cambian con el tiempo (equilibrio y estacionario) y aquellos en evolución. La mecánica estadística se centra principalmente en el equilibrio.
- **Interacciones mecánica y térmica entre sistemas:** Se analizan cómo los sistemas intercambian energía en forma de trabajo (mecánica) o calor (térmica), lo que lleva a la definición de diferentes ensambles estadísticos.
- **Definición de ensamble estadístico:** Un ensamble es una colección hipotética de réplicas de un sistema en un macroestado dado, cada réplica en un microestado posible. Los promedios sobre el ensamble corresponden a los promedios temporales de un sistema real en equilibrio.
- **Número y densidad de estados de un sistema:** Se cuantifica el número de microestados accesibles a un sistema con una energía dada (número de estados) o dentro de un rango de energía (densidad de estados). Esto es fundamental para conectar la descripción microscópica con la entropía.

# Unida Nª 3: ENSAMBLE MICROCANÓNICO

Este ensamble es la base para sistemas aislados, donde la energía total, el volumen y el número de partículas son constantes.

- **Sistemas totalmente aislados:** Se modelan sistemas que no intercambian energía ni partículas con su entorno.
- **Conexión entre el ensamble microcanónico y la termodinámica: Entropía en función del número de estados accesibles:** La relación fundamental aquí es la fórmula de Boltzmann para la entropía: S=kB​lnΩ(E,V,N), donde kB​ es la constante de Boltzmann y Ω es el número de microestados accesibles para un macroestado con energía E, volumen V y número de partículas N. Esta es la primera conexión profunda entre lo microscópico (Ω) y lo macroscópico (S).
- **Aplicaciones del ensamble microcanónico:** Se aplicará a sistemas simples para calcular su entropía y otras propiedades termodinámicas derivadas.

# Unidad Nº 4: ENSAMBLE CANÓNICO

Este ensamble describe sistemas en contacto térmico con un reservorio a temperatura constante (T), con volumen (V) y número de partículas (N) fijos.

- **Definición de ensamble Canónico:** La probabilidad de que un sistema en contacto térmico con un reservorio a temperatura T se encuentre en un microestado con energía Ei​ está dada por la distribución de Boltzmann: P(Ei​)∝e−βEi​, donde β=1/(kB​T).
- 
- **Función de partición canónica:** La función de partición (Z) es la suma sobre todos los microestados accesibles de los factores de Boltzmann: Z(T,V,N)=∑i​e−βEi​. Esta función es central ya que a partir de ella se pueden derivar todas las propiedades termodinámicas macroscópicas.
- 
- **Cálculo de valores medios en el ensamble canónico:** El valor promedio de una observable O se calcula como ⟨O⟩=Z1​∑i​Oi​e−βEi​.
- **Cantidades termodinámicas en términos de la función de partición:** Relaciones clave como la energía libre de Helmholtz (F) se obtienen directamente de la función de partición: F(T,V,N)=−kB​TlnZ. A partir de la energía libre, se pueden obtener otras cantidades termodinámicas como la entropía, la presión y la energía interna mediante derivadas parciales. Por ejemplo, S=−(∂F/∂T)V,N​ y P=−(∂F/∂V)T,N​.
- **Teorema de equipartición de la energía:** Para sistemas clásicos en equilibrio térmico, este teorema establece que cada grado de libertad cuadrático en la energía contribuye con 21​kB​T a la energía promedio del sistema.
- **Paradoja de Gibbs:** Una aparente inconsistencia en el cálculo de la entropía para gases ideales clásicos al considerar partículas indistinguibles, que se resuelve dividiendo por N! en el espacio fase debido a la indistinguibilidad cuántica.
- **Distribución de velocidades de Maxwell:** Describe la distribución de las magnitudes de las velocidades de las partículas en un gas ideal clásico en equilibrio térmico.
- **Aplicaciones: Gas ideal monoatómico y diatómico:** Se aplicará el formalismo canónico para derivar las propiedades termodinámicas de gases simples.

# Unidad Nº 5: ENSAMBLE GRAN CANÓNICO

Este ensamble es apropiado para sistemas que pueden intercambiar tanto energía como partículas con un reservorio a temperatura (T) y potencial químico (μ) constantes, manteniendo el volumen (V) fijo.

- **Definición de ensamble gran canónico:** La probabilidad de encontrar el sistema con N partículas en un microestado de energía Ei​ está dada por P(N,Ei​)∝e−βEi​+βμN.
- **Función de partición gran canónica:** La función de partición gran canónica (Z) es la suma sobre todos los posibles números de partículas (N) y todos los microestados (i) para cada N: Z(T,V,μ)=∑N​∑i​e−βEi​(N)+βμN.
- **Cantidades termodinámicas en términos de la función de gran partición:** El gran potencial termodinámico (ΩG​) es fundamental en este ensamble: ΩG​(T,V,μ)=−kB​TlnZ. Relaciones como P=−(∂ΩG​/∂V)T,μ​ y ⟨N⟩=−(∂ΩG​/∂μ)T,V​ permiten obtener la presión y el número promedio de partículas.
- **Aplicaciones:** Útil para sistemas donde el número de partículas fluctúa, como en la descripción de gases en equilibrio con una fase líquida o sólida.
- **Conexión entre los diferentes ensambles estadísticos:** Se explorará cómo los diferentes ensambles (microcanónico, canónico, gran canónico) son equivalentes en el límite termodinámico (para sistemas muy grandes), aunque describen diferentes condiciones experimentales.

# Unidad Nº 6: SISTEMAS DE PARTÍCULAS INTERACTUANTES

Esta unidad aborda la complejidad de las interacciones entre partículas, que no pueden tratarse como libres como en los gases ideales.

- **Fluidos simples en equilibrio:**
    - **Función de partición configuracional:** Separación de la función de partición total en una parte cinética y una parte configuracional que depende de las interacciones.
    - **Funciones de correlación y función de correlación de pares g(r):** Describen cómo la posición de una partícula influye en la probabilidad de encontrar otra partícula a una cierta distancia (r). La función de correlación de pares g(r) es crucial para entender la estructura de fluidos.
    - **Cantidades termodinámicas a partir de g(r):** Relaciones formales conectan la función de correlación de pares con la presión y la energía interna.
    - **Expansión virial:** Un método para calcular las propiedades de gases reales como una expansión en potencias de la densidad, donde los coeficientes viriales dependen de las interacciones entre pares, tríos, etc., de partículas.
    - **Aplicaciones: gas de Van der Waals, gas de esferas duras, etc.:** Modelos simples que incluyen interacciones para explicar desviaciones del comportamiento ideal. La ecuación de estado de Van der Waals es un ejemplo clásico que incorpora atracción y repulsión efectiva entre partículas.
    - **Modelo simple de un sólido: sistemas de osciladores acoplados:** Introducción a la descripción vibracional de sólidos mediante modelos de osciladores armónicos acoplados, base para entender propiedades térmicas de sólidos.
- **Sistemas clásicos de espines interactuantes:** Modelos para describir materiales magnéticos, donde las "partículas" son espines localizados que interactúan.
    - **Modelo de Ising clásico:** Un modelo fundamental en una, dos o tres dimensiones para estudiar transiciones de fase en sistemas magnéticos, donde los espines pueden apuntar hacia arriba o hacia abajo.
    - **Aproximación de campo medio:** Un método aproximado para resolver modelos de espines interactuantes reemplazando la interacción compleja con vecinos por un campo promedio producido por ellos.
    - **Paramagnetismo:** Descripción de materiales cuyos espines se alinean débilmente con un campo magnético externo.

# Unidad Nª 7: ESTADÍSTICA CUÁNTICA

Aquí se incorporan los principios de la mecánica cuántica a la descripción estadística de sistemas de muchas partículas.

- **Fundamentos Estadísticos:**
    - **Estadística de Maxwell-Boltzmann:** Se revisa como límite clásico de las estadísticas cuánticas cuando la densidad de partículas es baja y la temperatura es alta.
    - **Gases ideales monoatómicos y diatómicos en la estadística de Maxwell-Boltzmann:** Aplicación del formalismo clásico.
- **Microestados y Macroestados cuánticos:** Los microestados se describen mediante funciones de onda del sistema completo, y los macroestados por valores esperados de observables macroscópicas.
- **Matriz densidad y ensambles cuánticos:** La matriz densidad (ρ) es la herramienta fundamental para describir el estado de un sistema cuántico en equilibrio térmico o en un estado mixto. Los ensambles cuánticos (microcanónico cuántico, canónico cuántico, gran canónico cuántico) se definen análogamente a los clásicos, pero sumando sobre estados cuánticos.
- **Sistemas de partículas idénticas:** La indistinguibilidad de partículas en mecánica cuántica lleva a dos tipos fundamentales: bosones (función de onda simétrica bajo intercambio de partículas) y fermiones (función de onda antisimétrica).
- **Bosones:** Partículas con espín entero (fotones, fonones, átomos de He-4).
    - **Estados simetrizados de Bosones:** La función de onda de un sistema de bosones idénticos es simétrica bajo la permutación de cualesquiera dos partículas.
    - **Traza del operador densidad y valor medio de operadores:** Cálculo de valores esperados de observables en el formalismo cuántico.
    - **Gas ideal de bosones y límite clásico:** Aplicación del formalismo a bosones no interactuantes.
    - **Condensación de Bose-Einstein:** Un fenómeno cuántico donde una fracción macroscópica de bosones ocupa el estado de menor energía a temperaturas bajas.
    - **Gas de fotones y radiación del cuerpo negro:** Aplicación a un gas de bosones sin masa (fotones), explicando la distribución de energía de la radiación emitida por un cuerpo negro.
- **Fermiones:** Partículas con espín semientero (electrones, protones, neutrones, átomos de He-3).
    - **Estados antisimetrizados de fermiones:** La función de onda de un sistema de fermiones idénticos es antisimétrica bajo la permutación de cualesquiera dos partículas, lo que lleva al principio de exclusión de Pauli.
    - **Traza del operador densidad y valor medio de operadores:** Cálculos análogos a los de bosones.
    - **Gas ideal de fermiones y límite clásico:** Aplicación del formalismo a fermiones no interactuantes, relevante para entender el comportamiento de electrones en metales o nucleones en núcleos atómicos.
- **Sistemas cuánticos de espines interactuantes:** Extensión de los modelos de espines a la descripción cuántica, relevante para entender el ferromagnetismo y otros fenómenos magnéticos cuánticos.

# Unidad Nº8: TÓPICOS ESPECIALES

Esta unidad introduce temas más avanzados que extienden los conceptos básicos de la mecánica estadística de equilibrio.

- **Transiciones de fase:** Estudio de los cambios de estado de la materia (sólido a líquido, líquido a gas, transiciones magnéticas), incluyendo la clasificación de transiciones (primer orden, segundo orden) y fenómenos críticos cerca del punto de transición.
- **Introducción a la mecánica estadística fuera de equilibrio:** Nociones básicas sobre cómo describir sistemas que no están en equilibrio termodinámico, abordando conceptos como transporte (conducción de calor, difusión) y relajación hacia el equilibrio.
- **Métodos computacionales, tales como Montecarlo, entre otros:** Introducción a técnicas numéricas utilizadas para simular sistemas de muchas partículas, especialmente cuando los métodos analíticos son intratables. Los métodos de Monte Carlo utilizan muestreo aleatorio para estimar propiedades promedio.

Este recorrido formativo busca dotar al estudiante con la capacidad de modelar, analizar y comprender una vasta gama de fenómenos físicos desde una perspectiva probabilística y estadística, aplicando las herramientas tanto de la mecánica clásica como cuántica a sistemas macroscópicos. La evaluación a través de exámenes escritos, quices y exposiciones permitirá medir la comprensión teórica y la capacidad de aplicar los conceptos a la resolución de problemas y la argumentación de ideas.