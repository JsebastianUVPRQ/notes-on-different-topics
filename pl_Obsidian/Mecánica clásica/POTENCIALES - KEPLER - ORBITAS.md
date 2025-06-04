
## Órbitas y Potenciales en Mecánica Clásica
### 1. **Introducción: Potenciales Centrales y Conservación**

En mecánica clásica, uno de los escenarios más importantes y recurrentes es el del movimiento bajo la acción de una **fuerza central**. Este tipo de fuerza aparece en contextos muy diversos, desde el estudio de los planetas alrededor del Sol, hasta la dinámica de electrones en campos atómicos. Una **fuerza central** es aquella cuya dirección siempre apunta hacia (o desde) un punto fijo del espacio, denominado **centro de fuerza**, y cuya magnitud depende únicamente de la distancia al centro. Esto se traduce en que el potencial asociado a la fuerza solo depende de la coordenada radial $r$ es decir:  
$$
V(\mathbf{r}) = V(r)
$$ 
donde $r = |\mathbf{r}|$ representa la distancia entre la partícula y el centro de fuerza. Esta simetría esférica del potencial tiene consecuencias físicas y matemáticas profundas.

De acuerdo con **Goldstein (2002, Capítulo 3)**, las fuerzas derivadas de potenciales centrales cumplen con ciertas leyes de conservación fundamentales que simplifican en gran medida el análisis del sistema. Estas son:

---

#### 1.1 Conservación del Momento Angular
Una propiedad fundamental de las fuerzas centrales es que siempre son colineales con el vector de posición $\mathbf{r}$ es decir, $\mathbf{F} = f(r) \, \hat{\mathbf{r}}$. Por lo tanto, el **torque** (o momento de la fuerza) relativo al centro de fuerza es siempre cero:
$$
\boldsymbol{\tau} = \mathbf{r} \times \mathbf{F} = \mathbf{r} \times f(r) \, \hat{\mathbf{r}} = \mathbf{0}
$$ 
Esto implica que el **momento angular** $\mathbf{L}$ es constante en el tiempo:  
$$
\mathbf{L} = \mathbf{r} \times \mathbf{p} = \text{constante}
$$ 
donde $\mathbf{p} = \mu \dot{\mathbf{r}}$es el momento lineal, y $\mu$ es la **masa reducida** del sistema. Esta conservación del momento angular tiene una consecuencia geométrica inmediata: el movimiento está **confinado a un plano perpendicular a $\mathbf{L}$**. Así, aunque el sistema es tridimensional, la dinámica se puede estudiar eficazmente en dos dimensiones.

---
#### 1.2 Conservación de la Energía Mecánica Total
Otra cantidad conservada en el movimiento bajo fuerzas conservativas es la **energía mecánica total** $E$ que se compone de la energía cinética $T$ y la energía potencial $V(r)$. Si se trabaja en coordenadas polares planas $(r, \theta)$ la energía cinética de una partícula de masa reducida $\mu$ es:  
$$
T = \frac{1}{2} \mu \left( \dot{r}^2 + r^2 \dot{\theta}^2 \right)
$$ 
Dado que el momento angular también puede escribirse como $L = \mu r^2 \dot{\theta}$ la energía total se puede expresar como:  
$$
E = T + V(r) = \frac{1}{2} \mu \dot{r}^2 + \frac{L^2}{2 \mu r^2} + V(r) = \text{constante}
$$ 
Aquí se distingue claramente un término radial (dependiente de $\dot{r}$) y otro angular (dependiente de $L$y $r$), lo que permite estudiar por separado la evolución de la coordenada radial.

---

#### 1.3 Implicaciones de Estas Conservaciones
Estas dos leyes de conservación tienen consecuencias profundas en la estructura del problema:
- **Reducción de la dimensionalidad**: El hecho de que el movimiento esté contenido en un plano permite reducir el estudio a dos dimensiones, y luego, gracias a la simetría central, a una sola variable efectiva: el radio $r$.
- **Existencia de órbitas planas y predecibles**: La conservación del momento angular determina la geometría general de las órbitas, mientras que la conservación de la energía limita las regiones accesibles en el espacio radial.
- **Fundamento de leyes empíricas**: Estas propiedades son la base para derivar las **leyes de Kepler** y comprender fenómenos como la **precesión de las órbitas**, incluso más allá del marco newtoniano.

---

### 2. **Potencial Efectivo y la Ecuación Radial**
Cuando se analiza el movimiento de una partícula bajo un potencial central $V(r)$ es útil reescribir el problema de tal forma que toda la dinámica se reduzca a una sola coordenada, la coordenada radial $r$. Para lograrlo, se introduce el concepto de **potencial efectivo**, que combina el potencial físico original con un término adicional que incorpora los efectos de la conservación del momento angular.

---

#### 2.1 De la Energía Total a la Energía Radial
Como ya vimos en la sección anterior, la energía total del sistema puede escribirse en coordenadas polares como:  
$$
E = \frac{1}{2} \mu \dot{r}^2 + \frac{L^2}{2 \mu r^2} + V(r)
$$ 
Aquí, $\frac{1}{2} \mu \dot{r}^2$ representa la energía cinética radial, $\frac{L^2}{2 \mu r^2}$ corresponde a la energía cinética asociada al movimiento angular (aunque se comporta como un potencial respecto a $r$), y $V(r)$ es la energía potencial central real.  

El segundo término, $\frac{L^2}{2 \mu r^2}$ no está presente en el potencial físico, pero aparece en la energía total debido a la transformación de coordenadas. Por esta razón se introduce el **potencial efectivo** $V_{\text{eff}}(r)$como:  
$$
V_{\text{eff}}(r) = \frac{L^2}{2 \mu r^2} + V(r)
$$ 
Con esta redefinición, la energía total toma la forma:  
$$
E = \frac{1}{2} \mu \dot{r}^2 + V_{\text{eff}}(r)
$$ 
Este resultado tiene una interpretación fundamental: el problema radial se puede estudiar como si fuera el movimiento unidimensional de una partícula de masa $\mu$ en el **potencial efectivo** $V_{\text{eff}}(r)$. Esto permite utilizar la intuición desarrollada para problemas de una sola dimensión.

---

#### 2.2 Ecuación del Movimiento Radial
La ecuación de movimiento para la coordenada radial se deduce directamente de la energía total. Derivando con respecto al tiempo la ecuación de energía, y usando el hecho de que $E$ es constante, se obtiene la segunda ley de Newton aplicada a la dirección radial:  
$$
\mu \ddot{r} = -\frac{dV_{\text{eff}}}{dr}
$$ 
Esta ecuación es formalmente idéntica a la ecuación de Newton para una partícula en una dimensión bajo el potencial $V_{\text{eff}}(r)$.

---

#### 2.3 Forma del Potencial Efectivo
La forma del potencial efectivo depende tanto del momento angular $L$ como del tipo de potencial físico $V(r)$. Veamos dos casos comunes:
- Para un potencial de tipo **ley de potencias**, por ejemplo $V(r) = -\frac{k}{r^n}$ el potencial efectivo será:  
  $$
  V_{\text{eff}}(r) = \frac{L^2}{2 \mu r^2} - \frac{k}{r^n}
  $$
- Para el caso particular de la **gravitación newtoniana** ($V(r) = -\frac{G M m}{r}$), que corresponde a $n = 1$ el potencial efectivo es:   

$$
V_{\text{eff}}(r) = \frac{L^2}{2 \mu r^2} - \frac{G M m}{r}
$$ 
Este potencial efectivo tiene una estructura característica: la primera parte $\frac{L^2}{2 \mu r^2}$ actúa como una **repulsión centrífuga**, y la segunda como una **atracción gravitatoria**.

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
- El término centrífugo impide que la partícula alcance $r = 0$ cuando $L \neq 0$.
- El equilibrio entre la fuerza centrífuga y la atracción central define las condiciones para una órbita circular.
- El análisis cualitativo del gráfico de $V_{\text{eff}}(r)$ permite determinar si el sistema admite órbitas acotadas (como en el caso planetario), órbitas elípticas, parabólicas o hiperbólicas.

---

### 4. **Solución para la Fuerza Inversa al Cuadrado**
En esta sección, nos enfocaremos en el caso donde la partícula se mueve bajo una fuerza central atractiva cuya magnitud es inversamente proporcional al cuadrado de la distancia. Este es el caso tanto de la **gravitación newtoniana** como del **campo eléctrico de una carga puntual**, y está dado por:  
$$
\mathbf{F}(r) = -\frac{k}{r^2} \hat{\mathbf{r}}
$$ 
donde $k > 0$ representa una fuerza atractiva (por ejemplo, $k = G M m$ en gravitación, o $k = \frac{1}{4\pi\varepsilon_0} q_1 q_2$ en electrostática).

---

#### 4.1 Potencial Asociado
Recordamos que toda fuerza central es conservativa, por lo que existe un potencial $V(r)$ tal que:  
$$
\mathbf{F}(r) = -\nabla V(r)
$$ 
En coordenadas radiales, esto se reduce a:  
$$
F(r) = -\frac{dV}{dr}
$$ 
Integrando la expresión de la fuerza, obtenemos el potencial:  
$$
V(r) = -\int F(r) \, dr = -\int \left( -\frac{k}{r^2} \right) dr = \frac{k}{r} + C
$$ 
Como el potencial tiene libertad en una constante aditiva, tomamos $C = 0$ sin pérdida de generalidad. Entonces:  
$$
V(r) = \frac{k}{r}
$$ 

---

#### 4.2 Ecuación de la Órbita
Usamos la ecuación general de la órbita que ya habíamos deducido en términos de $u = \frac{1}{r}$:  
$$
\frac{d^2 u}{d\theta^2} + u = -\frac{1}{\mu L^2 u^2} \frac{dV}{du}
$$ 
Ya que $V(r) = \frac{k}{r} = k u$ podemos escribir:  
$$
\frac{dV}{du} = k
$$ 
Sustituyendo en la ecuación:  
$$
\frac{d^2 u}{d\theta^2} + u = -\frac{1}{\mu L^2 u^2} (k) = -\frac{k}{\mu L^2 u^2}
$$ 
Multiplicando ambos lados por $u^2$ para simplificar:  
$$
u^2 \frac{d^2 u}{d\theta^2} + u^3 = -\frac{k}{\mu L^2}
$$ 
Sin embargo, es más conveniente mantener la forma original para su resolución:  
$$
\frac{d^2 u}{d\theta^2} + u = -\frac{k}{\mu L^2 u^2} \quad \text{(ECUACIÓN CENTRAL)}
$$ 
> Esta es una **ecuación diferencial lineal de segundo orden con coeficientes constantes**, cuya solución es bien conocida.

---

#### 4.3 Solución General: Ecuación de una Cónica
La solución general de la ecuación:  
$$
\frac{d^2 u}{d\theta^2} + u = \frac{k}{\mu L^2}
$$ 
es la suma de la solución homogénea y una particular.
1. **Solución homogénea**:  
   $$
   \frac{d^2 u}{d\theta^2} + u = 0 \quad \Rightarrow \quad u_h(\theta) = A \cos(\theta - \theta_0)
   $$ 
   donde $A$ y $\theta_0$ son constantes de integración.
2. **Solución particular**: cualquier solución constante que satisfaga la ecuación:  
   $$
   u_p = \frac{k}{\mu L^2}
   $$ 
Por lo tanto, la **solución general** es:  
$$
u(\theta) = \frac{1}{r(\theta)} = A \cos(\theta - \theta_0) + \frac{k}{\mu L^2}
$$ 
Redefiniendo $e = \frac{A \mu L^2}{k}$ (llamado **excentricidad**) y tomando $\theta_0 = 0$ para simplicidad (podemos redefinir el eje angular), obtenemos:  
$$
\frac{1}{r(\theta)} = \frac{k}{\mu L^2} \left( 1 + e \cos\theta \right)
$$ 
Finalmente, despejamos $r(\theta)$:  
$$
r(\theta) = \frac{\mu L^2 / k}{1 + e \cos\theta}
$$ 
Esta es la ecuación de una **cónica con un foco en el origen**:
- Si $0 \leq e < 1$ , la órbita es una **elipse**.
- Si $e = 1$a órbita es una **parábola**.
- Si $e > 1$ la órbita es una **hipérbola**.

#### 4.4 Interpretación Física

- La forma de la órbita depende del valor de la **excentricidad $e$**, que a su vez depende de la energía total y el momento angular.
    
- En el caso particular de una órbita cerrada (elipse), esta es la base de las **leyes de Kepler**.
    
- Este resultado demuestra que **las trayectorias en un campo gravitacional (o coulombiano) son secciones cónicas**, un resultado profundo que conecta la mecánica clásica con la geometría.

---
### 5. **Relación entre Energía, Excentricidad y Clasificación de Órbitas**
La forma geométrica de la órbita está directamente vinculada a la energía total $E$ del sistema y al momento angular $L$. Recordemos que la energía total en un potencial central se expresa como:  
$$
E = \frac{1}{2} \mu \dot{r}^2 + \frac{L^2}{2 \mu r^2} + V(r)
$$  
Con el potencial gravitacional:  
$$
V(r) = -\frac{k}{r}
$$  

---

#### 5.1. **Expresión de la Excentricidad**
De la solución de la órbita, definimos la excentricidad $e$ mediante:  
$$
e = \sqrt{1 + \frac{2 E L^2}{\mu k^2}}
$$  
Esta fórmula se obtiene al combinar las condiciones energéticas con la ecuación de la órbita, considerando el balance entre la energía cinética y potencial .

---

#### 5.2. **Clasificación de las Órbitas según $E$ y $e$**
La relación anterior nos permite clasificar el tipo de órbita según el valor de la energía total $E$:  

- **Órbitas Elípticas (Ligadas):**  
  $$
  E < 0 \quad \Longrightarrow \quad 0 \leq e < 1
  $$  
  En este caso, la órbita es cerrada y el cuerpo se mueve en una trayectoria elíptica alrededor del foco .  

- **Órbitas Parabólicas (Marginalmente Ligadas):**  
  $$
  E = 0 \quad \Longrightarrow \quad e = 1
  $$  
  La trayectoria es una parábola que corresponde al límite entre órbitas ligadas y no ligadas .  

- **Órbitas Hiperbólicas (No Ligadas):**  
  $$
  E > 0 \quad \Longrightarrow \quad e > 1
  $$  
  La órbita es abierta y el cuerpo escapa al infinito siguiendo una hipérbola .  

---

#### 5.3. **Parámetros Orbitales Importantes**
El semilatus rectum $p$ y el semieje mayor $a$ de la elipse están relacionados con los parámetros físicos:  

- **Semilatus rectum:**  
  $$
  p = \frac{L^2}{\mu k}
  $$  
- **Semieje mayor:**  
  $$
  a = -\frac{k}{2E}
  $$  
  donde $a > 0$ para órbitas elípticas ($E < 0$) .  

---

#### 5.4. **Derivación de las Leyes de Kepler**
Partiendo de la ecuación de la órbita:  
$$
r(\theta) = \frac{p}{1 + e \cos \theta}
$$  
y utilizando la conservación del momento angular, podemos deducir las leyes clásicas de Kepler:  

- **Primera Ley (Órbitas Elípticas):**  
  Los planetas se mueven en órbitas elípticas con el Sol en uno de los focos .  

- **Segunda Ley (Áreas):**  
  $$
  \frac{dA}{dt} = \frac{L}{2\mu} = \text{constante}
  $$  
  El radio vector barre áreas iguales en tiempos iguales .  

- **Tercera Ley (Periodo):**  
  $$
  T = 2 \pi \sqrt{\frac{a^3 \mu}{k}}
  $$  
  Esta ley implica que el cuadrado del período es proporcional al cubo del semieje mayor, lo que fue confirmado por observaciones empíricas y explicado posteriormente por la mecánica newtoniana .  

---

### 6. **Estabilidad de Órbitas Circulares**
Una órbita circular corresponde a un punto de equilibrio en el movimiento radial, es decir, a un radio fijo $r_0$ tal que la fuerza neta radial es nula y el movimiento en esa dirección está estacionario. Este punto se obtiene encontrando un mínimo del potencial efectivo:  
$$
\left. \frac{d V_{\text{eff}}}{d r} \right|_{r=r_0} = 0
$$  

---

#### 6.1. **Condición para un Mínimo Local**
Para que esta órbita circular sea estable, no basta con que la derivada primera se anule; es necesario que el punto sea un mínimo local del potencial efectivo, lo que matemáticamente se expresa como:  
$$
\left. \frac{d^2 V_{\text{eff}}}{d r^2} \right|_{r=r_0} > 0
$$  
Esta condición garantiza que pequeñas perturbaciones radiales alrededor de $r_0$ producirán fuerzas restauradoras que tienden a regresar el sistema a la órbita circular, evitando que la partícula se aleje indefinidamente .  

---

#### 6.2. **Interpretación Física**
- Si la segunda derivada es positiva, el potencial efectivo es convexo y el sistema actúa como un oscilador armónico para pequeñas oscilaciones radiales.  
- Si la segunda derivada es negativa, el punto es un máximo o un punto de silla, y la órbita circular es inestable frente a perturbaciones pequeñas .  

---

#### 6.3. **Ejemplo: Potencial Gravitatorio Newtoniano**
Para el caso del potencial gravitatorio clásico:  
$$
V(r) = -\frac{k}{r}
$$  
El potencial efectivo es:  
$$
V_{\text{eff}}(r) = -\frac{k}{r} + \frac{L^2}{2 \mu r^2}
$$  
Calculamos las derivadas:  
$$
\frac{d V_{\text{eff}}}{d r} = \frac{k}{r^2} - \frac{L^2}{\mu r^3} = 0 \quad \Rightarrow \quad r_0 = \frac{L^2}{\mu k}
$$  
y  
$$
\frac{d^2 V_{\text{eff}}}{d r^2} = -\frac{2k}{r^3} + \frac{3 L^2}{\mu r^4}
$$  
Evaluando en $r_0$:  
$$
\left. \frac{d^2 V_{\text{eff}}}{d r^2} \right|_{r_0} = \frac{k}{r_0^3} > 0
$$  
Por lo que la órbita circular en el potencial gravitacional newtoniano es **estable** .  

---

#### 6.4. **Ejemplo: Potencial de Yukawa**
Consideremos un potencial más general que introduce un término de pantalla (como ocurre en interacciones nucleares o en medios con efecto de apantallamiento):  
$$
V(r) = -\frac{k e^{-\alpha r}}{r}
$$  
donde $\alpha$ es un parámetro que controla la longitud de pantalla. El potencial efectivo se vuelve:  
$$
V_{\text{eff}}(r) = -\frac{k e^{-\alpha r}}{r} + \frac{L^2}{2 \mu r^2}
$$  
La condición para estabilidad implica analizar la segunda derivada:  
$$
\frac{d^2 V_{\text{eff}}}{d r^2} = \frac{L^2}{\mu r^4} + \frac{k e^{-\alpha r}}{r^3} (\alpha^2 r^2 + 2 \alpha r + 2)
$$  
La presencia del término con $\alpha$ puede modificar la estabilidad de la órbita circular dependiendo de la magnitud de $\alpha$ y $L$. Este ejemplo muestra cómo la estabilidad puede verse afectada por detalles finos del potencial .  

---

#### 6.5. **Pequeñas Oscilaciones Radiales**
Al perturbar la órbita circular $r = r_0 + \epsilon$ con $|\epsilon| \ll r_0$, el movimiento radial se puede aproximar por un oscilador armónico:  
$$
V_{\text{eff}}(r) \approx V_{\text{eff}}(r_0) + \frac{1}{2} \left. \frac{d^2 V_{\text{eff}}}{d r^2} \right|_{r_0} \epsilon^2
$$  
La ecuación de movimiento para la perturbación radial $\epsilon$ es:  
$$
\mu \ddot{\epsilon} = -k_{\text{eff}} \epsilon, \quad k_{\text{eff}} = \left. \frac{d^2 V_{\text{eff}}}{d r^2} \right|_{r_0}
$$  
Lo que describe un movimiento oscilatorio con frecuencia:  
$$
\omega_r = \sqrt{\frac{k_{\text{eff}}}{\mu}}
$$  
Esta frecuencia caracteriza las oscilaciones radiales alrededor de la órbita circular estable y es un parámetro clave para estudiar la estabilidad dinámica del sistema .  

---

### Notas técnicas:
1. Se corrigieron errores de sintaxis en LaTeX (uso de `\dot{}`, `\ddot{}`, `\frac{}{}`, `\sqrt{}`).  
2. Se normalizó la notación física (ej: $V_{\text{eff}}$ en lugar de $V_{\text{efectiva}}$).  
3. Se añadieron referencias cruzadas a las fuentes proporcionadas (ej: , ).  
4. Se ajustaron espacios y alineaciones para mejorar la legibilidad.