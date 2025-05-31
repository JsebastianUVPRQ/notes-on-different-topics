
---
## Órbitas y Potenciales en Mecánica Clásica

### 1. **Introducción: Potenciales Centrales y Conservación**

En mecánica clásica, uno de los escenarios más importantes y recurrentes es el del movimiento bajo la acción de una **fuerza central**. Este tipo de fuerza aparece en contextos muy diversos, desde el estudio de los planetas alrededor del Sol, hasta la dinámica de electrones en campos atómicos. Una **fuerza central** es aquella cuya dirección siempre apunta hacia (o desde) un punto fijo del espacio, denominado **centro de fuerza**, y cuya magnitud depende únicamente de la distancia al centro. Esto se traduce en que el potencial asociado a la fuerza solo depende de la coordenada radial $r$, es decir:

V(r)=V(r)V(\mathbf{r}) = V(r)

donde $r = |\mathbf{r}|$ representa la distancia entre la partícula y el centro de fuerza. Esta simetría esférica del potencial tiene consecuencias físicas y matemáticas profundas.

De acuerdo con **Goldstein (2002, Capítulo 3)**, las fuerzas derivadas de potenciales centrales cumplen con ciertas leyes de conservación fundamentales que simplifican en gran medida el análisis del sistema. Estas son:

---

#### 1.1 Conservación del Momento Angular

Una propiedad fundamental de las fuerzas centrales es que siempre son colineales con el vector de posición $\mathbf{r}$, es decir, $\mathbf{F} = f(r),\hat{\mathbf{r}}$. Por lo tanto, el **torque** (o momento de la fuerza) relativo al centro de fuerza es siempre cero:
$$
τ=r×F=r×f(r) r^=0\boldsymbol{\tau} = \mathbf{r} \times \mathbf{F} = \mathbf{r} \times f(r)\,\hat{\mathbf{r}} = \mathbf{0}
$$
Esto implica que el **momento angular** $\mathbf{L}$ es constante en el tiempo:

L=r×p=constante\mathbf{L} = \mathbf{r} \times \mathbf{p} = \text{constante}

donde $\mathbf{p} = \mu \dot{\mathbf{r}}$ es el momento lineal, y $\mu$ es la **masa reducida** del sistema. Esta conservación del momento angular tiene una consecuencia geométrica inmediata: el movimiento está **confinado a un plano perpendicular a $\mathbf{L}$**. Así, aunque el sistema es tridimensional, la dinámica se puede estudiar eficazmente en dos dimensiones.

---

#### 1.2 Conservación de la Energía Mecánica Total

Otra cantidad conservada en el movimiento bajo fuerzas conservativas es la **energía mecánica total** $E$, que se compone de la energía cinética $T$ y la energía potencial $V(r)$. Si se trabaja en coordenadas polares planas $(r, \theta)$, la energía cinética de una partícula de masa reducida $\mu$ es:

T=12μ(r˙2+r2θ˙2)T = \frac{1}{2}\mu \left( \dot{r}^2 + r^2 \dot{\theta}^2 \right)

Dado que el momento angular también puede escribirse como $L = \mu r^2 \dot{\theta}$, la energía total se puede expresar como:

E=T+V(r)=12μr˙2+L22μr2+V(r)=constanteE = T + V(r) = \frac{1}{2}\mu \dot{r}^2 + \frac{L^2}{2\mu r^2} + V(r) = \text{constante}

Aquí se distingue claramente un término radial (dependiente de $\dot{r}$) y otro angular (dependiente de $L$ y $r$), lo que permite estudiar por separado la evolución de la coordenada radial.

---

#### 1.3 Implicaciones de Estas Conservaciones

Estas dos leyes de conservación tienen consecuencias profundas en la estructura del problema:

- **Reducción de la dimensionalidad**: El hecho de que el movimiento esté contenido en un plano permite reducir el estudio a dos dimensiones, y luego, gracias a la simetría central, a una sola variable efectiva: el radio $r$.
    
- **Existencia de órbitas planas y predecibles**: La conservación del momento angular determina la geometría general de las órbitas, mientras que la conservación de la energía limita las regiones accesibles en el espacio radial.
    
- **Fundamento de leyes empíricas**: Estas propiedades son la base para derivar las **leyes de Kepler** y comprender fenómenos como la **precesión de las órbitas**, incluso más allá del marco newtoniano.
    

---

Perfecto. Continuamos ahora con la **Sección 2: Potencial Efectivo y la Ecuación Radial**, ampliando considerablemente el contenido y utilizando correctamente `$...$` para fórmulas en línea y `$$...$$` para fórmulas en bloque, como indicaste.

---

### 2. **Potencial Efectivo y la Ecuación Radial**

Cuando se analiza el movimiento de una partícula bajo un potencial central $V(r)$, es útil reescribir el problema de tal forma que toda la dinámica se reduzca a una sola coordenada, la coordenada radial $r$. Para lograrlo, se introduce el concepto de **potencial efectivo**, que combina el potencial físico original con un término adicional que incorpora los efectos de la conservación del momento angular.

---

#### 2.1 De la Energía Total a la Energía Radial

Como ya vimos en la sección anterior, la energía total del sistema puede escribirse en coordenadas polares como:

E=12μr˙2+L22μr2+V(r)E = \frac{1}{2}\mu \dot{r}^2 + \frac{L^2}{2\mu r^2} + V(r)

Aquí, $\frac{1}{2}\mu \dot{r}^2$ representa la energía cinética radial, $\frac{L^2}{2\mu r^2}$ corresponde a la energía cinética asociada al movimiento angular (aunque se comporta como un potencial respecto a $r$), y $V(r)$ es la energía potencial central real.

El segundo término, $\frac{L^2}{2\mu r^2}$, no está presente en el potencial físico, pero aparece en la energía total debido a la transformación de coordenadas. Por esta razón se introduce el **potencial efectivo** $V_{\text{eff}}(r)$ como:

Veff(r)=L22μr2+V(r)V_{\text{eff}}(r) = \frac{L^2}{2\mu r^2} + V(r)

Con esta redefinición, la energía total toma la forma:

E=12μr˙2+Veff(r)E = \frac{1}{2}\mu \dot{r}^2 + V_{\text{eff}}(r)

Este resultado tiene una interpretación fundamental: el problema radial se puede estudiar como si fuera el movimiento unidimensional de una partícula de masa $\mu$ en el **potencial efectivo** $V_{\text{eff}}(r)$. Esto permite utilizar la intuición desarrollada para problemas de una sola dimensión.

---

#### 2.2 Ecuación del Movimiento Radial

La ecuación de movimiento para la coordenada radial se deduce directamente de la energía total. Derivando con respecto al tiempo la ecuación de energía, y usando el hecho de que $E$ es constante, se obtiene la segunda ley de Newton aplicada a la dirección radial:

μr¨=−dVeffdr\mu \ddot{r} = -\frac{dV_{\text{eff}}}{dr}

Esta ecuación es formalmente idéntica a la ecuación de Newton para una partícula en una dimensión bajo el potencial $V_{\text{eff}}(r)$.

---

#### 2.3 Forma del Potencial Efectivo

La forma del potencial efectivo depende tanto del momento angular $L$ como del tipo de potencial físico $V(r)$. Veamos dos casos comunes:

- Para un potencial de tipo **ley de potencias**, por ejemplo $V(r) = -\frac{k}{r^n}$, el potencial efectivo será:
    
    Veff(r)=L22μr2−krnV_{\text{eff}}(r) = \frac{L^2}{2\mu r^2} - \frac{k}{r^n}
- Para el caso particular de la **gravitación newtoniana** ($V(r) = -\frac{G M m}{r}$), que corresponde a $n = 1$, el potencial efectivo es:
    
    Veff(r)=L22μr2−GMmrV_{\text{eff}}(r) = \frac{L^2}{2\mu r^2} - \frac{G M m}{r}

Este potencial efectivo tiene una estructura característica: la primera parte $\frac{L^2}{2\mu r^2}$ actúa como una **repulsión centrífuga**, y la segunda como una **atracción gravitatoria**.

---

#### 2.4 Equilibrios y Movimiento Radial

El estudio cualitativo del movimiento radial se basa en la forma del potencial efectivo:

- Los **puntos de equilibrio** del movimiento radial ocurren donde $\frac{dV_{\text{eff}}}{dr} = 0$.
    
- Un **mínimo local** de $V_{\text{eff}}(r)$ corresponde a una **órbita circular estable**.
    
- Un **máximo local** corresponde a una **órbita circular inestable**.
    

Además, la partícula puede oscilar alrededor del punto de equilibrio si su energía total es ligeramente mayor al mínimo del potencial efectivo. Estas oscilaciones corresponden a órbitas **no perfectamente circulares**, pero **cerradas** o **precesantes**, dependiendo del tipo de potencial.

---

#### 2.5 Interpretación Física

La introducción del potencial efectivo no es solo una técnica matemática, sino que permite una **interpretación física clara** del movimiento:

- El término centrífugo impide que la partícula alcance $r = 0$ cuando $L \ne 0$.
    
- El equilibrio entre la fuerza centrífuga y la atracción central define las condiciones para una órbita circular.
    
- El análisis cualitativo del gráfico de $V_{\text{eff}}(r)$ permite determinar si el sistema admite órbitas acotadas (como en el caso planetario), órbitas elípticas, parabólicas o hiperbólicas.
    

---

Perfecto. Continuamos con la **Sección 4: Solución para la Fuerza Inversa al Cuadrado**, profundizando en el caso clásico de una fuerza central atractiva de tipo gravitacional o coulombiana. En este contexto, resolveremos explícitamente la ecuación de la órbita y mostraremos cómo se obtiene una **cónica** (elipse, parábola o hipérbola) como trayectoria.

---

### 4. **Solución para la Fuerza Inversa al Cuadrado**

En esta sección, nos enfocaremos en el caso donde la partícula se mueve bajo una fuerza central atractiva cuya magnitud es inversamente proporcional al cuadrado de la distancia. Este es el caso tanto de la **gravitación newtoniana** como del **campo eléctrico de una carga puntual**, y está dado por:

F(r)=−kr2F(r) = -\frac{k}{r^2}

donde $k > 0$ representa una fuerza atractiva (por ejemplo, $k = G M m$ en gravitación, o $k = \frac{1}{4\pi\varepsilon_0} q_1 q_2$ en electrostática).

---

#### 4.1 Potencial Asociado

Recordamos que toda fuerza central es conservativa, por lo que existe un potencial $V(r)$ tal que:

F(r)=−dVdrF(r) = -\frac{dV}{dr}

Integrando la expresión de la fuerza, obtenemos el potencial:

V(r)=−∫F(r) dr=−∫(−kr2)dr=−kr+CV(r) = -\int F(r) \, dr = -\int \left( -\frac{k}{r^2} \right) dr = -\frac{k}{r} + C

Como el potencial tiene libertad en una constante aditiva, tomamos $C = 0$ sin pérdida de generalidad. Entonces:

V(r)=−krV(r) = -\frac{k}{r}

---

#### 4.2 Ecuación de la Órbita

Usamos la ecuación general de la órbita que ya habíamos deducido en términos de $u = \frac{1}{r}$:

d2udθ2+u=−1μL2u2dVdu\frac{d^2 u}{d\theta^2} + u = -\frac{1}{\mu L^2 u^2} \frac{dV}{du}

Ya que $V(r) = -\frac{k}{r} = -k u$, podemos escribir:

dVdu=−k\frac{dV}{du} = -k

Entonces:

−1μL2u2dVdu=kμL2u2-\frac{1}{\mu L^2 u^2} \frac{dV}{du} = \frac{k}{\mu L^2 u^2}

Sustituyendo en la ecuación:

d2udθ2+u=kμL2u2\frac{d^2 u}{d\theta^2} + u = \frac{k}{\mu L^2 u^2}

Multiplicamos ambos lados por $u^2$ para simplificar:

u2d2udθ2+u3=kμL2u^2 \frac{d^2 u}{d\theta^2} + u^3 = \frac{k}{\mu L^2}

Sin embargo, es más conveniente mantener la forma original para su resolución:

d2udθ2+u=kμL2(ECUACIOˊN CENTRAL)\frac{d^2 u}{d\theta^2} + u = \frac{k}{\mu L^2} \qquad \text{(ECUACIÓN CENTRAL)}

> Esta es una **ecuación diferencial lineal de segundo orden con coeficientes constantes**, cuya solución es bien conocida.

---

#### 4.3 Solución General: Ecuación de una Cónica

La solución general de la ecuación:

d2udθ2+u=kμL2\frac{d^2 u}{d\theta^2} + u = \frac{k}{\mu L^2}

es la suma de la solución homogénea y una particular.

1. **Solución homogénea**:
    
    d2udθ2+u=0⇒uh(θ)=Acos⁡(θ−θ0)\frac{d^2 u}{d\theta^2} + u = 0 \quad \Rightarrow \quad u_h(\theta) = A \cos(\theta - \theta_0)
    
    donde $A$ y $\theta_0$ son constantes de integración.
    
2. **Solución particular**: cualquier solución constante que satisfaga la ecuación:
    
    up=kμL2u_p = \frac{k}{\mu L^2}

Por lo tanto, la **solución general** es:

u(θ)=1r(θ)=Acos⁡(θ−θ0)+kμL2u(\theta) = \frac{1}{r(\theta)} = A \cos(\theta - \theta_0) + \frac{k}{\mu L^2}

Redefiniendo $e = \frac{A \mu L^2}{k}$ (llamado **excentricidad**) y tomando $\theta_0 = 0$ para simplicidad (podemos redefinir el eje angular), obtenemos:

1r(θ)=kμL2(1+ecos⁡θ)\frac{1}{r(\theta)} = \frac{k}{\mu L^2} \left(1 + e \cos\theta \right)

Finalmente, despejamos $r(\theta)$:

r(θ)=μL2/k1+ecos⁡θr(\theta) = \frac{\mu L^2 / k}{1 + e \cos\theta}

Esta es la ecuación de una **cónica con un foco en el origen**:

- Si $0 \le e < 1$, la órbita es una **elipse**.
    
- Si $e = 1$, la órbita es una **parábola**.
    
- Si $e > 1$, la órbita es una **hipérbola**.
    

---

#### 4.4 Interpretación Física

- La forma de la órbita depende del valor de la **excentricidad $e$**, que a su vez depende de la energía total y el momento angular.
    
- En el caso particular de una órbita cerrada (elipse), esta es la base de las **leyes de Kepler**.
    
- Este resultado demuestra que **las trayectorias en un campo gravitacional (o coulombiano) son secciones cónicas**, un resultado profundo que conecta la mecánica clásica con la geometría.
    

---

