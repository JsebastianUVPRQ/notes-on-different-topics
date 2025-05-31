TAMBIÉN NECESITO QUE REEMPLACES LOS \[ ECIACION ]\ HACIA $$ ECUACION $$ Y LOS \( ECUACION \) HACIA $ECUACION$

Perfecto. Comenzaré con las **secciones 1 a 3** totalmente expandidas, detalladas y con formato LaTeX corregido (doble dólar para ecuaciones en bloque, simple dólar para ecuaciones en línea), basándome en los contenidos y estilo de los libros de **Goldstein** y **Dieter Strauch**.

---

## Órbitas y Potenciales en Mecánica Clásica

### 1. **Introducción: Potenciales Centrales y Conservación**

En mecánica clásica, el estudio de las fuerzas centrales es crucial para entender numerosos sistemas físicos, desde los movimientos planetarios en astronomía hasta las interacciones entre partículas en física atómica y molecular. Una **fuerza central** es aquella cuya magnitud depende exclusivamente de la distancia entre dos cuerpos y cuya dirección está siempre orientada a lo largo del vector que une dichos cuerpos. Formalmente, una fuerza central $\mathbf{F}(\mathbf{r})$ satisface:

F(r)=f(r) r^,donde r=∥r∥\mathbf{F}(\mathbf{r}) = f(r) \, \hat{\mathbf{r}}, \quad \text{donde } r = \|\mathbf{r}\|

Esto implica que el campo de fuerzas es **esféricamente simétrico**, es decir, no depende de los ángulos, sino solo de la magnitud del vector posición. Tales fuerzas derivan de un potencial escalar que también depende únicamente de $r$:

V(r)=V(r)V(\mathbf{r}) = V(r)

Goldstein enfatiza que este tipo de simetría conlleva importantes consecuencias en términos de leyes de conservación. Específicamente, los sistemas sometidos a fuerzas centrales conservan tanto el **momento angular** como la **energía mecánica total**.

#### Conservación del momento angular

La conservación del momento angular se deriva de la simetría rotacional del sistema. El momento angular se define como:

L=r×p\mathbf{L} = \mathbf{r} \times \mathbf{p}

donde $\mathbf{p} = \mu \mathbf{v}$ es el momento lineal, y $\mu$ es la masa reducida del sistema. Dado que el torque neto asociado a una fuerza central es cero (porque $\mathbf{r} \times \mathbf{F} = 0$), se cumple:

dLdt=r×F=0⇒L=constante\frac{d\mathbf{L}}{dt} = \mathbf{r} \times \mathbf{F} = 0 \Rightarrow \mathbf{L} = \text{constante}

Esta conservación implica que el vector posición y el vector velocidad del cuerpo en movimiento permanecen confinados a un plano perpendicular al vector constante $\mathbf{L}$. Esto permite reducir el problema tridimensional a uno bidimensional.

#### Conservación de la energía total

La segunda consecuencia de la simetría es la conservación de la energía mecánica total:

E=T+V=12μr˙2+L22μr2+V(r)=constanteE = T + V = \frac{1}{2} \mu \dot{r}^2 + \frac{L^2}{2 \mu r^2} + V(r) = \text{constante}

Aquí se ha utilizado la representación del movimiento en coordenadas polares, donde la energía cinética tiene dos términos: uno radial $\frac{1}{2} \mu \dot{r}^2$ y otro angular $\frac{L^2}{2 \mu r^2}$ (el llamado término de la barrera centrífuga). Esta conservación proporciona una poderosa herramienta para determinar las trayectorias y tipos de órbitas posibles.

---

### 2. **Potencial Efectivo y Ecuación Radial**

Una de las estrategias más efectivas para estudiar el movimiento en un campo central consiste en **reformular la energía total como un sistema unidimensional** en la variable radial $r$. Para ello, se introduce el concepto de **potencial efectivo**, que tiene en cuenta tanto la interacción central como el efecto centrífugo que surge del movimiento angular:

Veff(r)=V(r)+L22μr2\boxed{V_{\text{eff}}(r) = V(r) + \frac{L^2}{2\mu r^2}}

Este potencial total "efectivo" permite tratar el movimiento radial como si se tratara de una partícula ficticia moviéndose en una dimensión bajo la influencia de $V_{\text{eff}}(r)$. La ecuación que rige la evolución de $r(t)$ se deduce entonces de la conservación de la energía total:

E=12μr˙2+Veff(r)E = \frac{1}{2} \mu \dot{r}^2 + V_{\text{eff}}(r)

Esta es formalmente equivalente a la ecuación de energía para un sistema unidimensional, lo cual simplifica el análisis. **Dieter Strauch (2009)** enfatiza esta reducción como uno de los pilares fundamentales de la mecánica clásica central: se transforma un sistema en 3D en uno efectivo en 1D.

#### 2.1. **Puntos de Equilibrio y Órbitas Circulares**

Las **órbitas circulares** ocurren cuando el radio permanece constante: $\dot{r} = 0$ y $\ddot{r} = 0$. Esto solo es posible si el radio corresponde a un **punto crítico** del potencial efectivo, es decir:

dVeffdr∣r=r0=0\left. \frac{dV_{\text{eff}}}{dr} \right|_{r = r_0} = 0

Derivando explícitamente:

dVeffdr=dVdr−L2μr3\frac{dV_{\text{eff}}}{dr} = \frac{dV}{dr} - \frac{L^2}{\mu r^3}

y entonces la condición de órbita circular se convierte en:

dVdr=L2μr3\frac{dV}{dr} = \frac{L^2}{\mu r^3}

**Ejemplo: Potencial gravitatorio**

Consideremos el caso del potencial gravitacional clásico:

V(r)=−kr,con k=GMmV(r) = -\frac{k}{r}, \quad \text{con } k = G M m

La derivada del potencial es:

dVdr=kr2\frac{dV}{dr} = \frac{k}{r^2}

Sustituyendo en la condición de equilibrio:

kr02=L2μr03⇒r0=L2μk\frac{k}{r_0^2} = \frac{L^2}{\mu r_0^3} \Rightarrow r_0 = \frac{L^2}{\mu k}

Por tanto, para un momento angular dado, existe un único radio en el cual se puede obtener una órbita circular bajo este potencial.

---

### 3. **Ecuación de la Órbita: La Fórmula de Binet**

Para determinar la forma precisa de la órbita $r(\theta)$, se utiliza una transformación matemática clave conocida como la **ecuación de Binet**, que recurre al cambio de variable $u = \frac{1}{r}$. Esta transformación convierte la ecuación de movimiento en una ecuación diferencial de segundo orden en términos de $u(\theta)$, permitiendo así determinar la trayectoria en coordenadas polares.

La ecuación de Binet se deduce a partir de las leyes de Newton y la conservación del momento angular. El resultado final es:

d2udθ2+u=−μL2u2F(1u)\boxed{ \frac{d^2u}{d\theta^2} + u = -\frac{\mu}{L^2 u^2} F\left(\frac{1}{u}\right) }

donde $F(r) = -\frac{dV}{dr}$ es la fuerza central.

#### 3.1. **Solución para Potencial Gravitatorio**

Volviendo al potencial gravitatorio $V(r) = -\frac{k}{r}$, cuya fuerza es:

F(r)=−dVdr=−(kr2)F(r) = -\frac{dV}{dr} = -\left( \frac{k}{r^2} \right)

Sustituyendo en la ecuación de Binet:

d2udθ2+u=μkL2\frac{d^2u}{d\theta^2} + u = \frac{\mu k}{L^2}

Esta es una ecuación diferencial lineal de segundo orden con coeficientes constantes, cuya solución general es:

u(θ)=μkL2+Acos⁡(θ−θ0)u(\theta) = \frac{\mu k}{L^2} + A \cos(\theta - \theta_0)

Reescribiendo en términos de $r(\theta)$:

r(θ)=1u(θ)=p1+ecos⁡(θ−θ0)r(\theta) = \frac{1}{u(\theta)} = \frac{p}{1 + e \cos(\theta - \theta_0)}

donde los parámetros son:

p=L2μk,e=1+2EL2μk2p = \frac{L^2}{\mu k}, \quad e = \sqrt{1 + \frac{2EL^2}{\mu k^2}}

Esta es la ecuación general de una **cónica** en coordenadas polares, donde $e$ es la **excentricidad** y $p$ el **semilatus rectum**. Dependiendo del valor de $e$, la trayectoria puede ser una elipse, parábola o hipérbola.

---

¿Deseas que continúe con las **secciones 4 a 6**? También puedo generarte un archivo `.md` o `.tex` al final si lo necesitas.