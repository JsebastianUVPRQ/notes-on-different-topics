Mientras que la Serie de Fourier se aplica a funciones periódicas, la **Transformada de Fourier** se extiende a funciones no periódicas, transformando una función en el dominio temporal o espacial en su representación en el dominio de la frecuencia. Es clave en la mecánica cuántica, donde se utiliza para pasar entre la representación en el espacio de posición y en el espacio de momento.

La Transformada de Fourier de una función $\psi(x)$ se define como:

$$\tilde{\psi} = \int_{-\infty}^{\infty} \psi_{(x)}  \exp(-ikx) \quad dx$$

Aquí, $k$ representa la frecuencia espacial (momento en mecánica cuántica). 
La inversa de esta transformada permite reconstruir la función original:

$$\psi(x) = \frac{1}{2\pi} \int_{-\infty}^{\infty} \tilde{\psi}(k) e^{ikx} \, dk$$


## 1. **Explicación intuitiva**
### **Transformada de Fourier (explicación rigurosa pero intuitiva, con prerrequisitos)**  
La **transformada de Fourier** es una operación matemática que descompone una función en sus frecuencias constituyentes, de manera análoga a cómo un prisma descompone la luz en colores. A continuación, una explicación rigurosa pero intuitiva, incluyendo prerrequisitos y conceptos clave.  

---

### **Prerrequisitos**  
1. **Cálculo**: Integración (la transformada de Fourier se define mediante una integral).  
2. **Números complejos**: Fórmula de Euler $e^{i\theta} = \cos\theta + i\sin\theta$.  
3. **Álgebra lineal**: Funciones base y productos internos (la transformada proyecta sobre una base de exponenciales complejas).  
4. **Señales básicas**: Entender representaciones en dominio del tiempo vs. dominio de la frecuencia.  

---

### **Intuición**  
Imagina analizar un acorde musical. Tu oído separa el sonido en notas individuales (frecuencias). La transformada de Fourier hace esto matemáticamente:  
- **Dominio del tiempo**: Una señal $f(t)$ (ej: voltaje vs. tiempo).  
- **Dominio de la frecuencia**: Su transformada $F(\omega)$, que muestra "cuánto" de cada frecuencia $\omega$ existe en $f(t)$.  

La transformada correlaciona $f(t)$ con infinitos osciladores (ondas seno/coseno) en todas las frecuencias $\omega$. El resultado $F(\omega)$ cuantifica la amplitud y fase de cada componente frecuencial.  

---

### **Definición Matemática**  
La transformada de Fourier de $f(t)$ es:  
$$
F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} dt
$$  
La transformada inversa reconstruye $f(t)$ desde sus frecuencias:  
$$
f(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} F(\omega) e^{i\omega t} d\omega
$$  

#### **Componentes clave**:  
1. **Exponencial compleja $e^{-i\omega t}$**:  
   - Codifica seno (parte imaginaria) y coseno (parte real) vía la fórmula de Euler.  
   - Actúa como una "sonda" para la frecuencia $\omega$; la integral mide qué tanto $f(t)$ resuena con $e^{-i\omega t}$.  

2. **Interpretación**:  
   - $F(\omega)$ es un **número complejo**:  
     - Magnitud $|F(\omega)|$: Amplitud de la frecuencia $\omega$.  
     - Fase $\arg(F(\omega))$: Retraso temporal de esa componente.  

---

### **Perspectiva Rigurosa**  
1. **Condiciones de existencia**:  
   - $f(t)$ debe ser **absolutamente integrable**: $\int_{-\infty}^\infty |f(t)| dt < \infty$.  
   - Se generaliza para funciones no integrables (ej: delta de Dirac, señales periódicas) usando distribuciones.  

2. **Principio de incertidumbre**:  
   - Una señal localizada en tiempo (ej: un pulso) tiene un espectro disperso en frecuencia, y viceversa:  
     $$
     \text{Ancho temporal} \times \text{Ancho espectral} \geq \frac{1}{2}
     $$  

3. **Dualidad de operaciones**:  
   - **Convolución** (tiempo) $\leftrightarrow$ **Multiplicación** (frecuencia).  
   - **Derivación** $\leftrightarrow$ **Multiplicación por $i\omega$**.  

4. **Espacios de funciones**:  
   - Definida para $L^1$ (funciones integrables) y extendida a $L^2$ (señales de energía finita) vía el teorema de Plancherel.  

---

### **Ejemplos**  
1. **Onda senoidal**:  
   - $f(t) = \sin(\omega_0 t)$  
   - $F(\omega) = \frac{\pi}{i} \left[ \delta(\omega - \omega_0) - \delta(\omega + \omega_0) \right]$  
   - Dos deltas en $\pm \omega_0$.  

2. **Pulso rectangular**:  
   - $f(t) = 1$ para $|t| < T/2$, sino 0.  
   - $F(\omega) = T \cdot \text{sinc}(\omega T/2)$, una **función sinc** (decaimiento oscilante).  

---

### **¿Por qué números complejos?**  
- **Eficiencia**: Una sola exponencial $e^{-i\omega t}$ codifica seno y coseno.  
- **Información de fase**: El argumento de $F(\omega)$ captura retardos, cruciales para reconstruir la señal.  

---

### **Analogías intuitivas**  
1. **Ecualizador musical**: Visualiza $|F(\omega)|$ como barras de amplitud.  
2. **Prisma**: Separa luz (señal) en colores (frecuencias).  

---

### **Errores comunes**  
- **Frecuencias negativas**: Para señales reales, $F(-\omega) = \overline{F(\omega)}$. Son necesarias para que la transformada inversa sea real.  
- **Factores de escala**: Hay convenciones distintas (ej: $\frac{1}{2\pi}$ en la inversa).  

---

### **Resumen**  
La transformada de Fourier es un **cambio de base**:  
- **Funciones base**: Exponenciales complejas $e^{i\omega t}$.  
- **Proyección**: La integral $\int f(t)e^{-i\omega t} dt$ mide "solapamiento" entre $f(t)$ y $e^{i\omega t}$.  
- **Aplicaciones**: Filtrado de señales, compresión de imágenes (JPEG), ecuaciones diferenciales, mecánica cuántica.  

Las ecuaciones son inevitables, pero su intuición radica en **descomponer complejidad en simplicidad**—una frecuencia a la vez.  

--- 

### **Respuesta final**  
La transformada de Fourier descompone señales en frecuencias, combinando rigor matemático con intuición física. Su poder reside en convertir operaciones complicadas (como derivadas o convoluciones) en multiplicaciones simples en el dominio de la frecuencia.  

**Ecuaciones clave**:  
$$
\boxed{F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} dt}, \quad \boxed{f(t) = \frac{1}{2\pi} \int_{-\infty}^{\infty} F(\omega) e^{i\omega t} d\omega}
$$
## 3. **Aplicación en Mecánica Cuántica**

En mecánica cuántica, la Transformada de Fourier es fundamental para resolver la ecuación de Schrödinger y para analizar el comportamiento de las partículas. La función de onda $\psi(x)$ en el espacio de posición describe la probabilidad de encontrar una partícula en un punto específico. La Transformada de Fourier de $\psi(x)$, $\tilde{\psi}(k)$, proporciona la representación en el espacio de momentos, permitiendo conocer la distribución de momento de la partícula.

Por ejemplo, en el caso de una partícula libre, la ecuación de Schrödinger en el espacio de momentos es más fácil de resolver que en el espacio de posición, ya que se convierte en una ecuación algebraica al aplicarle la Transformada de Fourier.

## 4. **Propiedades de la Transformada de Fourier**

Algunas propiedades clave de la Transformada de Fourier incluyen:

- **Linealidad**: $$\mathcal{F}{a f(x) + b g(x)} = a \mathcal{F}{f(x)} + b \mathcal{F}{g(x)}$$
- **Desplazamiento en el tiempo**: Un desplazamiento en el tiempo de $f(x - x_0)$ resulta en una fase multiplicativa en el dominio de la frecuencia.
- **Teorema de Parseval**: La energía total de la señal se conserva en ambos dominios.

Estas propiedades son esenciales en la resolución de problemas complejos de análisis de señales, física y matemáticas aplicadas.

## 5. **Ejemplos de Cálculo de la Transformada de Fourier**

A continuación, se presentan tres ejemplos prácticos de cálculo de la Transformada de Fourier.

### Ejemplo 1: Transformada de Fourier de una Función Delta de Dirac

La función Delta de Dirac $\delta(x)$ tiene una Transformada de Fourier igual a 1 en todo el dominio de la frecuencia:

$$\tilde{\delta}(k) = \int_{-\infty}^{\infty} \delta(x) e^{-ikx} \, dx $$

Esta propiedad es útil en mecánica cuántica para representar estados de momento puro.


### Ejemplo 2: Transformada de Fourier de una Función Gaussiana

Para una función gaussiana $\psi(x) = e^{-\alpha x^2}$, su Transformada de Fourier es otra gaussiana en el dominio de la frecuencia:

$$\tilde{\psi}(k) = \sqrt{\dfrac{\pi}{\alpha}}~\exp\Big(\dfrac{k^2}{4\alpha}\Big)\psi​(k)$$​

Esto es relevante en el estudio de paquetes de ondas en mecánica cuántica, donde la localización en el espacio de posición se corresponde con una dispersión en el espacio de momento.

### Ejemplo 3: Transformada de Fourier de una Función Escalonada

Para una función escalonada, como la función de Heaviside $H(x)$, su Transformada de Fourier se define como:

$$\tilde{H}(k) = \int_{0}^{\infty} e^{-ikx} \, dx = \frac{1}{ik} + \pi \delta(k)$$

Esta transformación se usa en el análisis de señales para estudiar la respuesta de sistemas lineales a señales de entrada discontinuas.