
## Preguntas
### Problema 1: Teorema del virial para potenciales unidimensionales [15 puntos]  
(a) Sea $\psi(x)$ un estado propio de energía. Explique por qué el valor esperado $\langle [H, \Omega] \rangle$ del conmutador de $H$ con un operador arbitrario $\Omega$ se anula en el estado $\psi$.  

(b) Elija   $\Omega = xp$, y tome  
$$
H = \frac{p^2}{2m} + V(x).
$$  
Use la afirmación del apartado (a) para encontrar una relación entre el valor esperado $\langle T \rangle$ de la energía cinética y el valor esperado de una combinación de $ x $ y la derivada $V'(x)$ del potencial respecto a su argumento. Ambos valores esperados se toman en un estado propio de energía.  

(c) ¿Qué implica su resultado en (b) para la relación entre $\langle T \rangle$ y $\langle V \rangle$ en el caso del oscilador armónico unidimensional?  

---

### Problema 2: Órbita del electrón en el átomo de hidrógeno [15 puntos]  
A lo largo de este problema, consideramos un átomo de hidrógeno con número cuántico principal fijo $n$, con $\ell = n - 1$, y $m = n - 1$. El valor de $n$ es arbitrario y posiblemente grande.  

(a) Escriba la función de onda $\psi_{n,\ell,m}(r, \theta, \phi)$ en términos del armónico esférico relevante y un factor radial completamente determinado excepto por una constante de normalización $N$.  

(b) Proporcione, salvo normalización, la densidad de probabilidad radial $P(r)$, donde $P(r)dr$ es la probabilidad de encontrar al electrón en el intervalo $(r, r + dr)$. ¿Para qué valor de $r$ es máxima $P(r)$? Para $n$ grande, esta es en realidad una máxima bastante aguda.  

(c) Se sabe que, salvo normalización,  
$$
|Y_{\ell,\ell}(\theta, \phi)|^2 \simeq \ell^\ell (\sin \theta)^\ell.
$$  
Esboce $|Y_{\ell,\ell}|^2$ como función de $\theta \in [0, \pi]$ cuando $\ell$ es un entero grande. Describa con palabras y/o dibujo el lugar geométrico donde es probable encontrar al electrón para $n$ grande y $\ell = m = n - 1$.  

---

### Problema 3: Determinación del paquete de onda saliente [15 puntos]  
En un problema de dispersión unidimensional con un potencial de alcance $R$, escribimos la solución $\psi(x)$ para $x > R$ como  
$$
\psi(x) = e^{i\delta(k)} \sin(kx + \delta(k)), \quad x > R.
$$  

(a) Descomponga este $\psi(x)$ en la suma de una onda incidente $\psi_{\text{inc}}(x)$ que viaja hacia $x = 0$ y una onda saliente $\psi_{\text{out}}(x)$ que viaja alejándose de $x = 0$.  

(b) Enviamos un paquete de onda localizado $\Psi_{\text{inc}}(x, t)$ dado por  
$$
\Psi_{\text{inc}}(x, t) = \int_0^\infty dk \, f(k) e^{-ikx} e^{-iE(k)t/\hbar}, \quad x > R,
$$  
donde $f(k)$ es una función cuya magnitud tiene un pico agudo en $k = k_0 > 0$. Escriba una expresión análoga para el paquete de onda saliente asociado $\Psi_{\text{out}}(x, t)$.  

(c) Use la aproximación de fase estacionaria para encontrar la relación entre $x$ y $t$ que describe el movimiento del paquete saliente $\Psi_{\text{out}}(x, t)$.  

---

### Problema 4: Hacia la detección perfecta de bombas [20 puntos]  
Modificamos el experimento de Mach-Zehnder para aumentar hacia el 100% la fracción de bombas Elitzur-Vaidman (EV) que pueden verificarse como funcionales sin detonarlas. Una bomba EV se activa mediante un detector de fotones: si está operativa, cualquier fotón incidente en el detector hará explotar la bomba; si está defectuosa, el detector deja pasar todos los fotones y la bomba no explota.  

Para mejorar la detección, usamos un divisor de haz de alta reflectividad (BS), representado por una matriz unitaria $U$ de la forma
$$
U = \begin{pmatrix} \cos\left(\frac{\pi}{2N}\right) & i \sin\left(\frac{\pi}{2N}\right) \\ i \sin\left(\frac{\pi}{2N}\right) & \cos\left(\frac{\pi}{2N}\right) \end{pmatrix},
$$  
donde $N$ es un entero positivo fijo y grande. La reflectividad $R$ y transmitancia $T$ de BS son:  
$$
R = \cos^2\left(\frac{\pi}{2N}\right), \quad T = \sin^2\left(\frac{\pi}{2N}\right), \quad R + T = 1.
$$  
Imaginamos el BS colocado verticalmente, con un fotón a la izquierda de BS representado por $\begin{pmatrix} 1 \\ 0 \end{pmatrix}$ y a la derecha por $\begin{pmatrix} 0 \\ 1 \end{pmatrix}$. Esto se cumple tanto para fotones moviéndose hacia o alejándose de BS.  

Fórmula útil:  
$$
\begin{pmatrix} \cos \alpha & i \sin \alpha \\ i \sin \alpha & \cos \alpha \end{pmatrix} \begin{pmatrix} \cos \beta & i \sin \beta \\ i \sin \beta & \cos \beta \end{pmatrix} = \begin{pmatrix} \cos(\alpha + \beta) & i \sin(\alpha + \beta) \\ i \sin(\alpha + \beta) & \cos(\alpha + \beta) \end{pmatrix}.
$$  

(a) Calcule la $k$-ésima potencia  $U^k$ de la matriz $U$.  

(b) Construimos una cavidad colocando BS entre espejos perfectamente reflectantes $M_1$ y $M_2$ a distancias iguales a la izquierda y derecha. Un fotón se envía desde la izquierda y golpea BS, dividiéndose. Las componentes reflejada y transmitida rebotan en los espejos y vuelven a golpear BS, y así sucesivamente.  

Después de $k$ impactos en BS, ¿cuál es la probabilidad $p_L(k)$ de que el fotón se encuentre en el lado izquierdo de la cavidad y cuál es la probabilidad $p_R(k)$ de que se encuentre en el derecho? ¿Cuáles son estas probabilidades para $k = N$?  

(c) Se inserta un detector de fotones en el lado derecho de la cavidad, de modo que cualquier fotón que llegue allí será detectado (y absorbido). Como antes, se envía un fotón desde la izquierda. Después de esperar el tiempo necesario para $N$ impactos en BS, ¿cuál es la probabilidad $P_L(N)$ de que el fotón se encuentre en el lado izquierdo de la cavidad? ¿Cuál es la probabilidad $P_D(N)$ de que el fotón haya sido detectado?  

(d) Estime $P_L(N)$ y $P_D(N)$ en el límite $N \to \infty$. Fórmulas útiles: $\cos \epsilon \approx 1 - \frac{1}{2} \epsilon^2$, $(1 + \epsilon)^k \approx 1 + k\epsilon$ para $\epsilon$ suficientemente pequeño.  

(e) Dada una bomba EV, la insertamos en el lado derecho de la cavidad. Enviamos un fotón desde la izquierda y esperamos el tiempo necesario para $N$ impactos en BS. En ese momento, si el laboratorio no explota, buscamos el fotón.  

i. ¿Qué podemos concluir si el fotón se encuentra en el lado izquierdo de la cavidad?  
ii. ¿Cuál es la probabilidad $P_E(N)$ de que una bomba EV operativa explote en este experimento? Dé un valor aproximado para $N = 250$.
## Solucion 1
### Problema 1: Teorema del virial para potenciales unidimensionales [15 puntos]  
(a) **Demostración de que $\langle [H, \Omega] \rangle = 0$:**  
Para un estado propio de energía $\psi(x)$, el conmutador $[H, \Omega]$ satisface:  
$$
\langle \psi | [H, \Omega] | \psi \rangle = \langle \psi | H\Omega - \Omega H | \psi \rangle = (E - E)\langle \psi | \Omega | \psi \rangle = 0.
$$  
Por lo tanto, $\langle [H, \Omega] \rangle = 0$.  

(b) **Relación entre $\langle T \rangle$ y $\langle x V'(x) \rangle$:**  
Con $\Omega = xp$, el conmutador es:  
$$
[H, xp] = \frac{p^2}{2m}xp - xp\frac{p^2}{2m} + V(x)xp - xpV(x).
$$  
Usando $[p^2, x] = -2i\hbar p$ y $[V(x), xp] = i\hbar x V'(x)$, se obtiene:  
$$
\langle T \rangle = \frac{1}{2} \langle x V'(x) \rangle.
$$  

(c) **Caso del oscilador armónico unidimensional:**  
Para $V(x) = \frac{1}{2}m\omega^2 x^2$, $V'(x) = m\omega^2 x$. Entonces:  
$$
\langle T \rangle = \frac{1}{2} \langle x \cdot m\omega^2 x \rangle = \frac{1}{2} \langle V(x) \rangle \Rightarrow \langle T \rangle = \langle V \rangle.
$$  
Esto implica que $\langle T \rangle = \langle V \rangle$, como se esperaba para el oscilador armónico.  

---

### Problema 2: Órbita del electrón en el átomo de hidrógeno [15 puntos]  
(a) **Función de onda $\psi_{n,\ell,m}(r, \theta, \phi)$:**  
Para $\ell = n - 1$ y $m = n - 1$, la función de onda es:  
$$
\psi_{n,n-1,n-1}(r, \theta, \phi) = N r^{n-1} e^{-r/(na_0)} Y_{n-1,n-1}(\theta, \phi),
$$  
donde $ N $ es una constante de normalización.  

(b) **Densidad de probabilidad radial $P(r)$:**  
La densidad radial es:  
$$
P(r) = r^2 |R_{n,n-1}(r)|^2 \propto r^{2n} e^{-2r/(na_0)}.
$$  
El máximo ocurre en $r \approx n^2 a_0$, que para $n \gg 1$ es un pico agudo.  

(c) **Aproximación de $|Y_{\ell,\ell}|^2$ para $\ell \gg 1$:**  
Para $\ell = n - 1 \gg 1$, $|Y_{\ell,\ell}(\theta, \phi)|^2 \propto \sin^{2\ell} \theta$. Esto se concentra en $\theta = \frac{\pi}{2}$, formando un anillo en el plano ecuatorial. Para $n \gg 1$, el electrón se encuentra en una órbita casi clásica alrededor del núcleo.  

---

### Problema 3: Determinación del paquete de onda saliente [15 puntos]  
(a) **Descomposición de $\psi(x)$ en ondas incidente y saliente:**  
Para $x > R$:  
$$
\psi(x) = e^{i\delta(k)} \sin(kx + \delta(k)) = \frac{1}{2i} \left( e^{i(kx + \delta(k))} - e^{-i(kx + \delta(k))} \right).
$$  
Entonces:  
- Onda incidente: $\psi_{\text{inc}}(x) = \frac{1}{2i} e^{i(kx + \delta(k))}$,  
- Onda saliente: $\psi_{\text{out}}(x) = -\frac{1}{2i} e^{-i(kx + \delta(k))}$.  

(b) **Paquete de onda saliente $\Psi_{\text{out}}(x, t)$:**  
$$
\Psi_{\text{out}}(x, t) = \int_0^\infty dk \, f(k) e^{-ikx} e^{-iE(k)t/\hbar} \cdot e^{2i\delta(k)}.
$$  

(c) **Aproximación de fase estacionaria para $\Psi_{\text{out}}(x, t)$:**  
La fase $\phi(k) = -kx - \frac{E(k)t}{\hbar} + 2\delta(k)$. La condición $\frac{d\phi}{dk} = 0$ da:  
$$
x = \frac{dE}{dk} \cdot \frac{t}{\hbar} + \frac{d}{dk}(2\delta(k)) \Rightarrow x \approx v_g t,
$$  
donde $v_g = \frac{1}{\hbar} \frac{dE}{dk}$ es la velocidad del grupo.  

---

### Problema 4: Detección perfecta de bombas [20 puntos]  
(a) **Cálculo de $ U^k$:**  
$$
U^k = \begin{pmatrix} \cos\left(\frac{k\pi}{2N}\right) & i \sin\left(\frac{k\pi}{2N}\right) \\ i \sin\left(\frac{k\pi}{2N}\right) & \cos\left(\frac{k\pi}{2N}\right) \end{pmatrix}.
$$  

(b) **Probabilidades $ p_L(k) $ y $ p_R(k) $:**  
$$
p_L(k) = \cos^2\left(\frac{k\pi}{2N}\right), \quad p_R(k) = \sin^2\left(\frac{k\pi}{2N}\right).
$$  
Para $ k = N $:  
$$
p_L(N) = 0, \quad p_R(N) = 1.
$$  

(c) **Probabilidades con detector en el lado derecho:**  
Para $ N \gg 1 $:  
$$
P_D(N) \approx \frac{N}{2}, \quad P_L(N) \approx 1 - \frac{N}{2}.
$$  

(d) **Límite para $ N \to \infty $:**  
$$
P_L(N) \approx 1 - \frac{\pi^2}{8N}, \quad P_D(N) \approx \frac{\pi^2}{8N}.
$$  

(e) **Conclusión con bomba EV operativa:**  
i. Si el fotón está en la izquierda, la bomba no detonó, pero su presencia afectó la trayectoria.  
ii. Para $ N = 250 $:  
$$
P_E(250) \approx \frac{\pi^2}{2000} \approx 0.005.
$$

### Problema 4: Hacia la detección perfecta de bombas [20 puntos]  
(a) **Cálculo de la $k$-ésima potencia $U^k$ de la matriz $U$:**  
La matriz $U$  está dada por:  
$$
U = \begin{pmatrix} \cos\left(\frac{\pi}{2N}\right) & i \sin\left(\frac{\pi}{2N}\right) \\ i \sin\left(\frac{\pi}{2N}\right) & \cos\left(\frac{\pi}{2N}\right) \end{pmatrix}.
$$ 
Utilizando la identidad:  
$$
\begin{pmatrix} \cos\alpha & i \sin\alpha \\ i \sin\alpha & \cos\alpha \end{pmatrix}^k = \begin{pmatrix} \cos(k\alpha) & i \sin(k\alpha) \\ i \sin(k\alpha) & \cos(k\alpha) \end{pmatrix},
$$ 
se obtiene:  
$$
U^k = \begin{pmatrix} \cos\left(\frac{k\pi}{2N}\right) & i \sin\left(\frac{k\pi}{2N}\right) \\ i \sin\left(\frac{k\pi}{2N}\right) & \cos\left(\frac{k\pi}{2N}\right) \end{pmatrix}.
$$ 

(b) **Probabilidades $p_L(k)$    y     $p_R(k)$:**  
Después de $k$ interacciones con el divisor de haz (BS), las probabilidades de encontrar el fotón en la izquierda ($p_L$) y derecha ($p_R$) son:  
$$
p_L(k) = \cos^2\left(\frac{k\pi}{2N}\right), \quad p_R(k) = \sin^2\left(\frac{k\pi}{2N}\right).
$$ 
Para $k = N$:  
$$
p_L(N) = \cos^2\left(\frac{\pi}{2}\right) = 0, \quad p_R(N) = \sin^2\left(\frac{\pi}{2}\right) = 1.
$$ 

(c) **Probabilidades con detector en el lado derecho:**  
Si se inserta un detector en el lado derecho, la probabilidad de que el fotón sea detectado ($P_D$) es:  
$$
P_D(N) = \sum_{k=1}^N p_R(k) \approx \int_0^N \sin^2\left(\frac{\pi x}{2N}\right) dx.
$$ 
Para $N \gg 1$, usando $\cos\epsilon \approx 1 - \frac{\epsilon^2}{2}$:  
$$
P_D(N) \approx \frac{N}{2}, \quad P_L(N) \approx 1 - \frac{N}{2}.
$$ 

(d) **Límite para $N \to \infty$:**  
$$
P_L(N) \approx 1 - \frac{\pi^2}{8N}, \quad P_D(N) \approx \frac{\pi^2}{8N}.
$$ 

(e) **Conclusión con bomba EV operativa:**  
i. Si el fotón se encuentra en la izquierda, la bomba no detonó, pero su presencia afectó la trayectoria del fotón.  
ii. La probabilidad de que una bomba EV operativa explote es:  
$$
P_E(N) \approx \frac{\pi^2}{8N}.
$$ 
Para $N = 250$:  
$$
P_E(250) \approx \frac{\pi^2}{2000} \approx 0.005.
$$ 

---

### Problema 5: Pozo cuadrado infinito con dimensión extra truncada [20 puntos]  
(a) **Separación de variables en la ecuación de Schrödinger (ES):**  
La ES bidimensional es:  
$$
-\frac{\hbar^2}{2m} \left( \frac{\partial^2 \psi}{\partial x^2} + \frac{\partial^2 \psi}{\partial y^2} \right) = E \psi.
$$ 
Suponiendo $\psi(x, y) = X(x)Y(y)$, se obtienen las ecuaciones:  
$$
-\frac{\hbar^2}{2m} \frac{d^2 X}{dx^2} = E_x X, \quad -\frac{\hbar^2}{2m} \frac{d^2 Y}{dy^2} = E_y Y,
$$ 
con $E = E_x + E_y$. Las condiciones de frontera son:  
- $X(0) = X(a) = 0$(pozo infinito en $x$),  
- $Y(y + L) = Y(y)$(condición periódica en $y$).  

(b) **Valores propios y estados normalizados:**  
$$
E_{n\ell} = \frac{\hbar^2 \pi^2 n^2}{2ma^2} + \frac{\hbar^2 \ell^2}{2mL^2}, \quad \psi_{n\ell}(x, y) = \sqrt{\frac{2}{a}} \sin\left(\frac{n\pi x}{a}\right) \cdot \frac{1}{\sqrt{L}} e^{i \frac{2\pi \ell y}{L}},
$$ 
donde $n = 1, 2, \dots$, $\ell = 0, \pm 1, \pm 2, \dots$.  

(c) **Energía del estado fundamental:**  
$$
E_{1,0} = \frac{\hbar^2 \pi^2}{2ma^2}.
$$ 

(d) **Valores propios coincidentes con el segmento 1D:**  
Los niveles $E_{n\ell}$     coinciden con los del segmento 1D cuando $\ell = 0$:  
$$
E_{n,0} = \frac{\hbar^2 \pi^2 n^2}{2ma^2}.
$$ 

(e) **Niveles más bajos en el cilindro sin equivalente en el segmento:**  
Los primeros niveles con $\ell \neq 0$:  
$$
E_{1,\pm1} = \frac{\hbar^2 \pi^2}{2ma^2} + \frac{\hbar^2}{2mL^2}.
$$ 

(f) **Estimación de energía mínima para detectar la dimensión extra:**  
Dado $L \ll a$y $\frac{\hbar^2}{2ma^2} = 1 \, \text{eV}$, la energía mínima requerida es:  
$$
\Delta E = \frac{\hbar^2}{2mL^2} = \frac{\hbar^2}{2m (a/1000)^2} = 10^6 \cdot \frac{\hbar^2}{2ma^2} = 1 \, \text{MeV}.
$$ 

---

### Problema 6: Transmisión resonante a través de dos deltas [20 puntos]  
(a) **Constante que debe anularse para transmisión perfecta:**  
Para transmisión perfecta ($T = 1$), el coeficiente de reflexión $B$debe ser cero.  

(b) **Ecuaciones de condiciones de frontera:**  
Con $B = 0$, las condiciones de continuidad en $x = \pm a$dan:  
$$
\begin{cases}
C + D = A e^{-ik a} + F e^{ik a}, \\
C - D = A e^{-ik a} - F e^{ik a}, \\
C e^{ik a} + D e^{-ik a} = F e^{ik a}, \\
C e^{ik a} - D e^{-ik a} = F e^{ik a}.
\end{cases}
$$ 

(c) **Gráfico de $\xi \cot \xi$      y valores de    $ka$:**  
- Para $\lambda \ll 1$: $\xi \cot \xi \approx -2\lambda \Rightarrow ka \approx \frac{n\pi}{2}$.  
- Para $\lambda \gg 1$: $\xi \cot \xi \approx -2\lambda \Rightarrow ka \approx \frac{(2n+1)\pi}{4}$.  

(d) **Aproximación de $\psi(x)$    para $\lambda \gg 1$:**  
Bajo resonancia ($\xi = 2ka$), se tiene $C = -D/\lambda$. La función de onda en $|x| < a$es:  
$$
\psi(x) \approx \frac{A}{1 + ika} \left( e^{ikx} - \frac{1}{\lambda} e^{-ikx} \right).
$$ 
El módulo al cuadrado $|\psi(x)|^2$muestra un máximo en $x = 0$debido a la interferencia constructiva entre las ondas incidentes y reflejadas.