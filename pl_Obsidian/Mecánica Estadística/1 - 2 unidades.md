
## Unidad Nº1: Conceptos Básicos de Probabilidad

Esta unidad constituye el pilar fundamental para comprender el comportamiento colectivo de sistemas con un número elevado de constituyentes. Dado que la mecánica estadística se ocupa de predecir propiedades macroscópicas a partir de leyes microscópicas, es indispensable recurrir a herramientas probabilísticas para manejar la inmensa cantidad de grados de libertad.

### 1. Conceptos básicos y definiciones fundamentales.

Se inicia con la revisión de la teoría axiomática de la probabilidad. Dado un espacio muestral $\Omega$, que representa el conjunto de todos los posibles resultados de un experimento aleatorio (en nuestro contexto, los posibles microestados de un sistema), se define un evento $A$ como cualquier subconjunto de $\Omega$. La probabilidad de un evento $A$, denotada por $P(A)$, satisface los axiomas de Kolmogorov:

* $P(A) \ge 0$ para todo evento $A$.
* $P(\Omega) = 1$.
* Para una secuencia de eventos mutuamente excluyentes $A_1, A_2, \dots$, la probabilidad de su unión es la suma de sus probabilidades: $P(\cup_{i=1}^\infty A_i) = \sum_{i=1}^\infty P(A_i)$.

Conceptos como la probabilidad condicional, $P(A|B) = P(A \cap B) / P(B)$ (siempre que $P(B) > 0$), y la independencia de eventos, donde $P(A \cap B) = P(A)P(B)$, son cruciales para analizar la correlación entre diferentes aspectos del estado de un sistema.

### 2. Técnicas de conteo.

Las técnicas combinatorias son esenciales para determinar el número de microestados accesibles bajo ciertas condiciones macroscópicas. El número de formas de seleccionar $k$ objetos de un conjunto de $n$ objetos sin importar el orden es dado por las combinaciones $\binom{n}{k} = \frac{n!}{k!(n-k)!}$. Si importa el orden, se utilizan las permutaciones $P(n, k) = \frac{n!}{(n-k)!}$. Estas fórmulas son la base para calcular la multiplicidad de un macroestado, que es el número de microestados correspondientes a ese macroestado. Por ejemplo, en un sistema de $N$ partículas idénticas distribuido en diferentes estados de energía, el número de maneras de distribuir las partículas en los estados es un problema de combinatoria.

### 3. Distribuciones de variables aleatorias discretas y continuas.

Una variable aleatoria $X$ asigna un valor numérico a cada resultado en el espacio muestral. Si los valores posibles de $X$ son contables, $X$ es discreta y su distribución de probabilidad se describe por la función de masa de probabilidad $P(x) = P(X=x)$. Si los valores posibles forman un intervalo, $X$ es continua y su distribución se describe por la función de densidad de probabilidad $f(x)$, tal que $P(a \le X \le b) = \int_a^b f(x) dx$. La condición de normalización es $\sum_x P(x) = 1$ para distribuciones discretas y $\int_{-\infty}^\infty f(x) dx = 1$ para distribuciones continuas.

### 4. Valores medios y fluctuaciones (desviación estándar).

El valor esperado o media de una variable aleatoria $X$ se define como:
$$ \mathbb{E}[X] = \sum_x x P(x) \quad (\text{discreta}) $$
$$ \mathbb{E}[X] = \int_{-\infty}^\infty x f(x) dx \quad (\text{continua}) $$
Esto representa el promedio de la variable en un gran número de repeticiones del experimento. La varianza, $\text{Var}(X) = \mathbb{E}[(X - \mathbb{E}[X])^2] = \mathbb{E}[X^2] - (\mathbb{E}[X])^2$, cuantifica la dispersión de los valores alrededor de la media. La desviación estándar $\sigma = \sqrt{\text{Var}(X)}$ es una medida de la amplitud típica de las fluctuaciones. En mecánica estadística, los valores medios de variables microscópicas se relacionan con las variables macroscópicas termodinámicas, y las fluctuaciones están relacionadas con la estabilidad y el comportamiento de los sistemas cerca de puntos críticos.

### 5. Función característica de una distribución.

La función característica de una variable aleatoria $X$ se define como $\phi_X(t) = \mathbb{E}[e^{itX}]$. Para una distribución continua con densidad $f(x)$, $\phi_X(t) = \int_{-\infty}^\infty e^{itx} f(x) dx$, que es la transformada de Fourier de $f(x)$. La función característica es útil para determinar propiedades de la distribución, como los momentos, ya que $\mathbb{E}[X^n] = (-i)^n \phi_X^{(n)}(0)$.

### 6. Algunas distribuciones importantes de probabilidad: Binomial, Gauss, Poisson.

* **Distribución Binomial:** Describe la probabilidad de obtener $k$ éxitos en $n$ ensayos independientes de Bernoulli, cada uno con probabilidad de éxito $p$.
    $$ P(k) = \binom{n}{k} p^k (1-p)^{n-k} $$
    Relevante en sistemas con dos posibles estados por partícula.
* **Distribución de Gauss (Normal):** Dada por:
    $$ f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{(x-\mu)^2}{2\sigma^2}} $$
    donde $\mu$ es la media y $\sigma^2$ la varianza. Aparece frecuentemente en mecánica estadística debido al teorema del límite central, que establece que la suma de un gran número de variables aleatorias independientes tiende a una distribución normal. Las fluctuaciones de variables macroscópicas en sistemas grandes suelen seguir una distribución gaussiana.
* **Distribución de Poisson:** Describe la probabilidad de un número dado de eventos que ocurren en un intervalo fijo de tiempo o espacio si estos eventos ocurren con una tasa promedio constante e independiente del tiempo desde el último evento.
    $$ P(k) = \frac{\lambda^k e^{-\lambda}}{k!} $$
    donde $\lambda$ es la tasa promedio. Es aplicable a situaciones como el número de partículas en un pequeño volumen de un gas diluido.

### 7. Marcha aleatoria en una dimensión.

Un modelo estocástico simple donde una partícula se mueve dando pasos aleatorios discretos. La posición después de $N$ pasos es una suma de variables aleatorias independientes, lo que permite analizar la distancia promedio recorrida y la dispersión, introduciendo conceptos relacionados con la difusión.

### 8. Distribuciones de probabilidad de varias variables.

Se extiende el formalismo a vectores aleatorios $\mathbf{X} = (X_1, X_2, \dots, X_n)$, con funciones de masa de probabilidad conjunta $P(x_1, \dots, x_n)$ o funciones de densidad de probabilidad conjunta $f(x_1, \dots, x_n)$. Esto es fundamental para describir sistemas con múltiples grados de libertad y analizar correlaciones entre diferentes variables.

## Unidad No 2: Descripción Estadística de un Sistema Físico

Esta unidad establece el marco conceptual para aplicar la probabilidad a la física, definiendo cómo se describen los sistemas a nivel microscópico y macroscópico y sentando las bases para la introducción de los ensambles estadísticos.

### 1. Especificación microscópica del estado de un sistema y estados accesibles.

En mecánica clásica, el microestado de un sistema de $N$ partículas en un espacio de fase de $6N$ dimensiones se especifica por el conjunto de posiciones y momentos de todas las partículas: $(q_1, \dots, q_{3N}, p_1, \dots, p_{3N})$. En mecánica cuántica, el microestado se describe por la función de onda del sistema, $|\psi\rangle$, o el estado cuántico específico si los niveles de energía están cuantizados. Los estados accesibles son aquellos microestados que son consistentes con las restricciones macroscópicas impuestas al sistema (por ejemplo, energía total, volumen, número de partículas).

### 2. Descripción macroscópica de un sistema y parámetros macroscópicos.

El macroestado se define por un pequeño número de variables macroscópicas observables, como la energía interna ($U$), el volumen ($V$), la presión ($P$), la temperatura ($T$), el número de partículas ($N$), la magnetización ($M$), etc. Un solo macroestado corresponde a un gran número de microestados posibles. La tarea de la mecánica estadística es relacionar estas propiedades macroscópicas promedio con la distribución de probabilidad de los microestados.

### 3. Estados en equilibrio, estacionarios y fuera del equilibrio.

Un sistema en equilibrio termodinámico es aquel cuyas propiedades macroscópicas no cambian con el tiempo y no hay flujos netos de energía o materia. Un estado estacionario también tiene propiedades macroscópicas constantes, pero puede haber flujos (por ejemplo, un sistema bajo un gradiente de temperatura mantenido externamente). Un estado fuera del equilibrio es aquel en el que las propiedades macroscópicas están cambiando con el tiempo. La mecánica estadística de equilibrio se enfoca en los sistemas en equilibrio termodinámico.

### 4. Interacciones mecánica y térmica entre sistemas.

Dos sistemas pueden interactuar intercambiando energía. Una interacción mecánica implica la realización de trabajo (cambio de volumen, por ejemplo), mientras que una interacción térmica implica el intercambio de calor debido a una diferencia de temperatura. Estas interacciones definen el tipo de contacto de un sistema con su entorno y son cruciales para la elección del ensamble estadístico apropiado para su descripción.

### 5. Definición de ensamble estadístico.

Un ensamble estadístico es una colección hipotética de un gran número de réplicas idénticas del sistema de interés, cada una representando un microestado posible del sistema compatible con las restricciones macroscópicas. La distribución de los microestados en el ensamble define el ensamble estadístico. Los promedios de las propiedades microscópicas sobre este ensamble (promedios de ensamble) se postula que son iguales a los valores promediados en el tiempo de las propiedades macroscópicas de un único sistema real en equilibrio (hipótesis ergódica).

### 6. Número y densidad de estados de un sistema.

Para un sistema con energía $E$, el número de estados $\Omega(E)$ es el número de microestados distintos (discretos en mecánica cuántica) o el volumen del espacio de fase (continuo en mecánica clásica) que son consistentemente con esta energía. La densidad de estados $\rho(E)$ se define tal que $\rho(E) dE$ es el número de microestados en el rango de energía $[E, E+dE]$. Para sistemas clásicos, el número de estados accesibles en el espacio de fase con energía en el rango $[E, E+\Delta E]$ es proporcional al volumen del espacio de fase en ese rango, dividido por $h^{3N}$ (donde $h$ es la constante de Planck) para hacer las unidades correctas y por $N!$ para partículas idénticas. El número de estados y la densidad de estados son fundamentales para el ensamble microcanónico y para conectar la descripción microscópica con la entropía.

Estos dos primeros temas establecen el lenguaje y los conceptos fundamentales para abordar el estudio de sistemas de muchas partículas desde una perspectiva estadística. A partir de aquí, las siguientes unidades desarrollarán los diferentes ensambles estadísticos (microcanónico, canónico, gran canónico) como herramientas para calcular las propiedades termodinámicas de diversos sistemas físicos, aplicando los principios de probabilidad y las descripciones microscópica y macroscópica introducidas en estas unidades iniciales.

Los resultados más importantes que emergen de esta base incluyen la comprensión de cómo las propiedades macroscópicas son promedios sobre estados microscópicos y la introducción de la multiplicidad de estados ($\Omega$) como una medida del desorden microscópico, precursora del concepto de entropía ($S = k_B \ln \Omega$). Además, se establecen las herramientas matemáticas (probabilidad, estadísticas) y conceptuales (microestado, macroestado, ensamble) necesarias para derivar las leyes de la termodinámica a partir de principios microscópicos, lo cual es el objetivo central de la mecánica estadística.