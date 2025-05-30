# Transformadas de Fourier: Contextos y Propiedades

La razón por la que existen **varias formas de escribir la transformada de Fourier** radica en sus aplicaciones en diferentes contextos: funciones unidimensionales o multidimensionales, espacios físicos o de momentum, y dimensiones variables. A continuación, se analizan las versiones **1D y 3D**, junto con sus propiedades clave.

---

## 1. Transformada de Fourier en 1D
### Definición:
$$
\Psi(x) = \frac{1}{\sqrt{2\pi}} \int dk\ \Phi(k) e^{ikx}, \quad 
\Phi(k) = \frac{1}{\sqrt{2\pi}} \int dx\ \Psi(x) e^{-ikx}
$$
- **$\Psi(x)$**: Función en el **espacio físico** (posición).
- **$\Phi(k)$**: Transformada en el **espacio de momentum/frecuencia**.
- **Simetría**: El factor $1/\sqrt{2\pi}$ garantiza que la transformada y su inversa tengan el mismo peso.

---

## 2. Conservación de Norma (1D)
$$
\int dx\ |\Psi(x)|^2 = \int dk\ |\Phi(k)|^2
$$
- **Unitaridad**: La transformada preserva la norma, esencial en física cuántica para conservar la probabilidad total.

---

## 3. Transformada de Fourier en 3D
### Definición:
$$
\Psi(\mathbf{x}) = \frac{1}{(2\pi)^{3/2}} \int d^3k\ \Phi(\mathbf{k}) e^{i\mathbf{k}\cdot\mathbf{x}}, \quad 
\Phi(\mathbf{k}) = \frac{1}{(2\pi)^{3/2}} \int d^3x\ \Psi(\mathbf{x}) e^{-i\mathbf{k}\cdot\mathbf{x}}
$$
- **$\Psi(\mathbf{x})$**: Función en espacio tridimensional.
- **$\Phi(\mathbf{k})$**: Transformada en el espacio de momentum vectorial.
- **Aplicaciones**: Electromagnetismo, mecánica cuántica multidimensional.

---

## 4. Conservación de Norma (3D)
$$
\int d^3x\ |\Psi(\mathbf{x})|^2 = \int d^3k\ |\Phi(\mathbf{k})|^2
$$
- **Generalización**: La norma se conserva en espacios multidimensionales.

---

## 5. Delta de Dirac como Transformada
### Representación:
$$
\frac{1}{2\pi} \int_{-\infty}^{+\infty} e^{ikx} dx = \delta(k), \quad 
\frac{1}{(2\pi)^3} \int_{-\infty}^{+\infty} e^{i\mathbf{k}\cdot\mathbf{x}} d^3x = \delta^{(3)}(\mathbf{k})
$$
- **Interpretación**: La transformada de una función constante es una delta de Dirac.
- **Utilidad**: Diagonización de operadores lineales en física teórica.

---

## 6. Integral Gaussiana con Término Lineal
### Fórmula:
$$
\int_{-\infty}^{+\infty} dx\ \exp\left(-ax^2 + bx\right) = \sqrt{\frac{\pi}{a}} \exp\left(\frac{b^2}{4a}\right), \quad \Re(a) > 0
$$
- **Aplicación**: Cálculo de transformadas de Fourier para funciones cuadráticas.
- **Invariancia**: Las gaussianas son invariantes bajo transformadas de Fourier.

---

## Resumen Tabular
| **Forma**                             | **Dimensión** | **Contexto**              | **Comentario**          |
| ------------------------------------- | ------------- | ------------------------- | ----------------------- |
| $\Psi(x), \Phi(k)$                    | 1D            | Espacio y momentum        | Transformada estándar   |
| $\int \Psi^2 = \int\Phi^2$            | 1D y 3D       | Conservación de norma     | Unitariedad             |
| $\Psi(\mathbf{x}), \Phi(\mathbf{k})$  | 3D            | Espacios tridimensionales | Sistemas físicos reales |
| $\delta(k), \delta^{(3)}(\mathbf{k})$ | 1D y 3D       | Funciones ideales         | Herramienta matemática  |
| Integral Gaussiana                    | 1D            | Cálculo técnico           | Útil en transformadas   |

---
# Ejercicios

# Transformadas de Fourier — Ejemplos y Ejercicios

## 1. Transformada de Fourier en 1D

### ✅ Ejemplos

1. $\Psi(x) = e^{-a x^2} \Rightarrow \Phi(k) = \sqrt{\frac{\pi}{a}} e^{-k^2/(4a)}$
2. $\Psi(x) = \delta(x - x_0) \Rightarrow \Phi(k) = \frac{1}{\sqrt{2\pi}} e^{-i k x_0}$
3. $\Psi(x) = \cos(k_0 x) \Rightarrow \Phi(k) = \frac{1}{\sqrt{2\pi}}[\delta(k - k_0) + \delta(k + k_0)]$
4. $\Psi(x) = \frac{\sin(\alpha x)}{\pi x} \Rightarrow \Phi(k) = \frac{1}{\sqrt{2\pi}} \chi_{[-\alpha, \alpha]}(k)$
5. $\Psi(x) = e^{i k_0 x} \Rightarrow \Phi(k) = \sqrt{2\pi} \delta(k - k_0)$

### 📝 Ejercicios

1. Calcula la transformada de Fourier de $\Psi(x) = e^{-|x|}$
2. Calcula la transformada de $\Psi(x) = \text{rect}(x)$
3. Encuentra $\Phi(k)$ si $\Psi(x) = \frac{1}{1 + x^2}$
4. Sea $\Psi(x) = e^{-x^2/2}$. Verifica que $\Phi(k) = e^{-k^2/2}$
5. Demuestra que:
   \[
   \mathcal{F}\left[\frac{d\Psi}{dx}\right](k) = i k \Phi(k)
   \]

---

## 2. Conservación de norma (1D)

### ✅ Ejemplos

1. $\Psi(x) = e^{-x^2/2} \Rightarrow \int |\Psi(x)|^2 dx = \int |\Phi(k)|^2 dk = \sqrt{\pi}$
2. $\Psi(x) = \delta(x) \Rightarrow \Phi(k) = \frac{1}{\sqrt{2\pi}}$
3. $\Psi(x) = \cos(k_0 x)$
4. $\Psi(x)$ escalonada normalizada
5. $\Psi(x) = \frac{1}{\pi(1 + x^2)} \Rightarrow \Phi(k) = e^{-|k|}$

### 📝 Ejercicios

1. Verifica que se conserva la norma para $\Psi(x) = e^{-|x|}$
2. Calcula normas para $\Psi(x) = \frac{1}{\sqrt{2}} \text{rect}(x)$
3. ¿Cuánto vale la norma de $\Phi(k)$ si $\Psi(x) = \delta(x - x_0)$?
4. Normaliza: $\Psi(x) = A e^{-a x^2}$
5. Usa Parseval para demostrar:
   \[
   \int |\Psi(x)|^2 dx = \int |\Phi(k)|^2 dk
   \]

---

## 3. Transformada de Fourier en 3D

### ✅ Ejemplos

1. $\Psi(\mathbf{x}) = e^{-a|\mathbf{x}|^2} \Rightarrow \Phi(\mathbf{k}) = \left(\frac{\pi}{a}\right)^{3/2} e^{-|\mathbf{k}|^2/(4a)}$
2. $\Psi(\mathbf{x}) = \delta^{(3)}(\mathbf{x} - \mathbf{x}_0) \Rightarrow \Phi(\mathbf{k}) = \frac{1}{(2\pi)^{3/2}} e^{-i\mathbf{k} \cdot \mathbf{x}_0}$
3. $\Psi(\mathbf{x}) = \frac{1}{|\mathbf{x}|^2 + 1}$
4. $\Psi(\mathbf{x}) = \cos(k_0 z)$
5. $\Psi(\mathbf{x}) = e^{i \mathbf{k}_0 \cdot \mathbf{x}}$

### 📝 Ejercicios

1. Calcula $\mathcal{F}[\Psi(\mathbf{x}) = e^{-\alpha |\mathbf{x}|^2}]$
2. $\Psi(\mathbf{x}) = \frac{1}{|\mathbf{x}|} e^{-|\mathbf{x}|}$
3. Demuestra que una función radial da transformada radial
4. $\Psi(\mathbf{x}) = \delta(x)\delta(y)\delta(z - z_0)$
5. ¿Qué forma tiene $\Phi(\mathbf{k})$ si $\Psi(\mathbf{x}) = \text{constante}?$

---

## 4. Conservación de norma (3D)

### ✅ Ejemplos

1. $\Psi(\mathbf{x}) = e^{-|\mathbf{x}|^2}$
2. $\Psi(\mathbf{x}) = \delta^{(3)}(\mathbf{x})$
3. $\Psi(\mathbf{x}) = e^{i \mathbf{k}_0 \cdot \mathbf{x}}$
4. $\Psi(\mathbf{x}) = A e^{-\alpha |\mathbf{x}|^2}$
5. $\Psi(\mathbf{x}) = \chi_{B(0,R)}(\mathbf{x})$

### 📝 Ejercicios

1. Verifica norma para $\Psi(\mathbf{x}) = e^{-\beta |\mathbf{x}|^2}$
2. ¿Norma finita para $\Psi(\mathbf{x}) = \frac{1}{(1 + |\mathbf{x}|^2)^2}$?
3. Usa Parseval para campo escalar
4. Si $\Psi$ está normalizada, demuestra que $\Phi$ también
5. Normaliza: $\Psi(\mathbf{x}) = A e^{-|\mathbf{x}|^2}$

---

## 5. Delta de Dirac como transformada

### ✅ Ejemplos

1. $\int e^{ikx} dx = 2\pi \delta(k)$
2. $\int e^{i\mathbf{k} \cdot \mathbf{x}} d^3x = (2\pi)^3 \delta^{(3)}(\mathbf{k})$
3. $\mathcal{F}[1](k) = \sqrt{2\pi} \delta(k)$
4. $\mathcal{F}[e^{i k_0 x}] = \sqrt{2\pi} \delta(k - k_0)$
5. $\mathcal{F}^{-1}[\delta(k - k_0)] = \frac{1}{\sqrt{2\pi}} e^{i k_0 x}$

### 📝 Ejercicios

1. Verifica: $\int_{-\infty}^{\infty} e^{ikx} dx = 2\pi \delta(k)$
2. Calcula $\mathcal{F}[1](\mathbf{k})$
3. Demuestra: $\delta(ax) = \frac{1}{|a|} \delta(x)$
4. Evalúa: $\int_{-\infty}^{\infty} f(k) \delta(k - k_0) dk$
5. Usa propiedades de delta para transformar $\cos(k_0 x)$

---

## 6. Integral gaussiana con término lineal

### ✅ Ejemplos

1. $\int e^{-x^2 + 2x} dx = \sqrt{\pi} e^1$
2. $\int e^{-a x^2} dx = \sqrt{\pi/a}$
3. $\int e^{-x^2 + bx} dx = \sqrt{\pi} e^{b^2/4}$
4. $\int e^{-2x^2 + 3x} dx = \sqrt{\pi/2} e^{9/16}$
5. $\int_{-\infty}^{\infty} e^{-ax^2 + i k x} dx = \sqrt{\pi/a} e^{-k^2/(4a)}$

### 📝 Ejercicios

1. Evalúa: $\int_{-\infty}^{\infty} e^{-3x^2 + 2x} dx$
2. Usa para calcular $\mathcal{F}[e^{-a x^2}](k)$
3. Demuestra la fórmula completando el cuadrado
4. Evalúa: $\int e^{-x^2 + i\omega x} dx$
5. Aplica para obtener $\mathcal{F}[e^{-a x^2}](k)$

---

¿Quieres exportar esto como PDF o seguir resolviendo ejemplos?
