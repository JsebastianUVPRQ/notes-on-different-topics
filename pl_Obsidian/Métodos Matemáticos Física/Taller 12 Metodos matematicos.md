A continuación se extraen los enunciados de todos los problemas y ejercicios del archivo **Taller 12 Métodos Matemáticos de la Física**:

---

### **Problema 17 — PROBLEMA PARA ENTREGAR: Operador $\hat{D} = \frac{d^2}{dx^2}$ (15 puntos)**

#### Enunciado:
Considere al operador $\hat{D} = \frac{d^2}{dx^2}$ actuando sobre el espacio de funciones $\varphi$ del espacio $H = L^2[0, L]$ con condiciones de frontera $\varphi(0) = \varphi(L) = 0$.

##### Partes:
- **(a)** Encuentre los valores propios y las correspondientes funciones propias normalizadas de $\hat{D}$.
- **(b)** Considere la función $f(x) = N x (L - x)$ de $H$. Encuentre el coeficiente de normalización $N$ y los coeficientes de la expansión de $f$ en la base de funciones propias de $\hat{D}$.

---

### **Ejercicio 1**

#### Enunciado:
Sea $\hat{A}$ un operador lineal que actúa sobre un espacio de Hilbert $H$. Sean $A_{ij}$ los elementos matriciales de la representación $A$ de $\hat{A}$ en la base ortonormal $\{\|e_j\rangle\}_{j=1}^\infty$ de $H$. Demuestre que los elementos matriciales de la representación de $\hat{A}^\dagger$ son $A_{ji}^*$, es decir, la representación matricial de $\hat{A}^\dagger$ es $(A^*)^\top$.

---

### **Ejercicio 2**

#### Enunciado:
Sean $\{\|u_j\rangle\}_{j=1}^\infty$ y $\{\|v_j\rangle\}_{j=1}^\infty$ dos bases ortonormales del espacio de Hilbert $H$. Sean $A_u$ y $A_v$ las respectivas representaciones matriciales en estas bases del operador lineal dado $\hat{A}$ que actúa sobre $H$. Demuestre que esta transformación de base está mediada por la matriz $S$, es decir,

$$
A_u = S A_v S^\dagger,
$$

donde los elementos matriciales de $S$ son $S_{ij} = \langle u_i \| v_j \rangle$.

Demuestre también que

$$
S S^\dagger = S^\dagger S = I,
$$

con $I$ la matriz identidad.

Observación: Una matriz que satisface la identidad anterior se llama matriz unitaria. Más generalmente, un operador lineal $\hat{U}$ que satisface $\hat{U} \hat{U}^\dagger = \hat{U}^\dagger \hat{U} = \hat{1}$ se dice que es un operador unitario.

---

### **Ejercicio 3**

#### Enunciado:
Considere el espacio de Hilbert bidimensional generado por la base ortonormal $\{\|1\rangle, \|2\rangle\}$. Se definen los operadores

$$
\hat{\sigma}_x = \|1\rangle \langle 2\| + \|2\rangle \langle 1\|,
$$
$$
\hat{\sigma}_y = -i \|1\rangle \langle 2\| + i \|2\rangle \langle 1\|,
$$
$$
\hat{\sigma}_z = \|1\rangle \langle 1\| - \|2\rangle \langle 2\|.
$$

##### Partes:
- **(a)** Encuentre la representación matricial de estos operadores.
- **(b)** Encuentre los valores y vectores propios de estos operadores.
- **(c)** Encuentre la representación matricial de $\hat{\sigma}_z$ en la base de estados propios de $\hat{\sigma}_x$.

---

### **Ejercicio 4**

#### Enunciado:
Para cada una de las ecuaciones diferenciales ordinarias (EDO) dadas, encontrar la función peso $w(x)$ que se necesita para transformar el operador diferencial respectivo en un operador autoadjunto. Además, indicar en cada caso los rangos de integración $(a, b)$ que garantizan que las condiciones de frontera se satisfagan.
##### Partes:
- **(a)** EDO de Hermite: $y'' - 2xy' + 2\alpha y = 0$.
- **(b)** EDO del oscilador armónico simple: $y'' + \omega^2 y = 0$.
- **(c)** EDO de Laguerre: $xy'' + (1 - x)y' + ay = 0$.

---

### **Resumen de Enunciados**
1. **Problema 17**: Encontrar valores propios y funciones propias de $\hat{D} = \frac{d^2}{dx^2}$, y expandir una función $f(x)$ en dicha base.
2. **Ejercicio 1**: Demostrar la relación entre los elementos matriciales de $\hat{A}$ y $\hat{A}^\dagger$.
3. **Ejercicio 2**: Demostrar la transformación de bases mediante una matriz unitaria $S$.
4. **Ejercicio 3**: Representación matricial, valores y vectores propios de los operadores $\hat{\sigma}_x$, $\hat{\sigma}_y$, y $\hat{\sigma}_z$.
5. **Ejercicio 4**: Encontrar la función peso $w(x)$ para hacer operadores diferenciales autoadjuntos y determinar los rangos de integración.
---
---
# SOLUCIONES - ANSWERS - RESPUESTAS

### PUNTO 4
To transform each given differential operator into a self-adjoint operator, we need to determine the appropriate weight function $w(x)$ and the interval of integration \((a, b)\) that ensures the boundary conditions are satisfied.

### Part (a): Hermite Equation
The Hermite equation is $y'' - 2xy' + 2\alpha y = 0$.

1. **Weight Function**: 
   - To convert the equation into Sturm-Liouville form, we use the integrating factor $\mu(x) = e^{-x^2}$.
   - Multiplying the equation by $\mu(x)$ gives $e^{-x^2} y'' - 2x e^{-x^2} y' + 2\alpha e^{-x^2} y = 0$.
   - This can be written as $(e^{-x^2} y')' + 2\alpha e^{-x^2} y = 0$, identifying the weight function $w(x) = e^{-x^2}$.

2. **Integration Interval**:
   - The interval is $(-\infty, \infty)$ because the weight function $e^{-x^2}$ ensures boundary terms vanish at infinity.

### Part (b): Simple Harmonic Oscillator Equation
The equation is $y'' + \omega^2 y = 0$.

1. **Weight Function**:
   - The equation is already in Sturm-Liouville form with $p(x) = 1$, $q(x) = 0$, and $w(x) = 1$.

2. **Integration Interval**:
   - The interval is typically a finite interval such as $[0, \pi]$ with boundary conditions like Dirichlet ( $y(0) = y(\pi) = 0$ ) or Neumann ( $y'(0) = y'(\pi) = 0$ ).

### Part (c): Laguerre Equation
The Laguerre equation is $xy'' + (1 - x)y' + ay = 0$.

1. **Weight Function**:
   - Converting to Sturm-Liouville form, we use the integrating factor $\mu(x) = x e^{-x}$.
   - Multiplying the equation by $\mu(x)$ gives $x e^{-x} y'' + (1 - x) e^{-x} y' + a e^{-x} y = 0$.
   - This can be written as $ e^{-x} y')' + a e^{-x} y = 0$, identifying the weight function $w(x) = e^{-x}$.

2. **Integration Interval**:
   - The interval is $(0, \infty)$ecause the weight function $e^{-x}$ ensures boundary terms vanish at 0 and infinity.

### Final Answers

- **(a)** Weight function: $\boxed{e^{-x^2}}$, Interval: $\boxed{(-\infty, \infty)}$
- **(b)** Weight function: $\boxed{1}$, Interval: $\boxed{[0, \pi]}$ (or any finite interval with suitable boundary conditions)
- **(c)** Weight function: $\boxed{e^{-x}}$, Interval: $\boxed{(0, \infty)}$