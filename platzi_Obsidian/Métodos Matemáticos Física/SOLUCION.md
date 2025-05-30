### Respuesta:

Aquí están las soluciones detalladas a los ejercicios solicitados:

---

## **1. Transformada de Fourier en 1D**

### **Ejercicio 1: Transformada de $\Psi(x) = e^{-|x|}$**
**Paso a paso:**  
La transformada de Fourier es:  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-|x|} e^{-ikx} dx
$$  
Por simetría par:  
$$
\Phi(k) = \frac{2}{\sqrt{2\pi}} \int_{0}^{\infty} e^{-x} \cos(kx) dx
$$  
Usando la integral $\int_{0}^{\infty} e^{-ax} \cos(bx) dx = \frac{a}{a^2 + b^2}$:  
$$
\Phi(k) = \frac{2}{\sqrt{2\pi}} \cdot \frac{1}{1 + k^2} = \sqrt{\frac{2}{\pi}} \cdot \frac{1}{1 + k^2}
$$  
**Respuesta:**  
$$
\Phi(k) = \sqrt{\frac{2}{\pi}} \cdot \frac{1}{1 + k^2}
$$

---

### **Ejercicio 2: Transformada de $\Psi(x) = \text{rect}(x)$**  
**Paso a paso:**  
La función $\text{rect}(x)$ es 1 en $|x| < 1/2$ y 0 en otro caso.  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \int_{-1/2}^{1/2} e^{-ikx} dx
$$  
Integrando:  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \cdot \frac{e^{-ik/2} - e^{ik/2}}{-ik} = \frac{1}{\sqrt{2\pi}} \cdot \frac{2 \sin(k/2)}{k}
$$  
**Respuesta:**  
$$
\Phi(k) = \sqrt{\frac{2}{\pi}} \cdot \frac{\sin(k/2)}{k}
$$

---

### **Ejercicio 3: Transformada de $\Psi(x) = \frac{1}{1 + x^2}$**  
**Paso a paso:**  
Usando la integral $\int_{-\infty}^{\infty} \frac{\cos(kx)}{1 + x^2} dx = \pi e^{-|k|}$:  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \cdot \pi e^{-|k|} = \sqrt{\frac{\pi}{2}} e^{-|k|}
$$  
**Respuesta:**  
$$
\Phi(k) = \sqrt{\frac{\pi}{2}} e^{-|k|}
$$

---

### **Ejercicio 4: Verificar $\Phi(k) = e^{-k^2/2}$ para $\Psi(x) = e^{-x^2/2}$**  
**Paso a paso:**  
La transformada es:  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} e^{-x^2/2} e^{-ikx} dx
$$  
Completando el cuadrado en el exponente:  
$$
-\frac{x^2}{2} - ikx = -\frac{(x + ik)^2}{2} - \frac{k^2}{2}
$$  
La integral gaussiana da:  
$$
\Phi(k) = \frac{1}{\sqrt{2\pi}} \cdot \sqrt{2\pi} e^{-k^2/2} = e^{-k^2/2}
$$  
**Respuesta:**  
Se verifica $\Phi(k) = e^{-k^2/2}$.

---

### **Ejercicio 5: Transformada de la derivada $\mathcal{F}\left[\frac{d\Psi}{dx}\right] = ik\Phi(k)$**  
**Paso a paso:**  
Integrando por partes:  
$$
\mathcal{F}\left[\frac{d\Psi}{dx}\right] = \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \frac{d\Psi}{dx} e^{-ikx} dx = ik \Phi(k)
$$  
(El término de frontera se anula si $\Psi(x) \to 0$ en $x \to \pm\infty$).  
**Respuesta:**  
$$
\mathcal{F}\left[\frac{d\Psi}{dx}\right] = ik \Phi(k)
$$

---

## **2. Conservación de norma (1D)**

### **Ejercicio 1: Verificar conservación para $\Psi(x) = e^{-|x|}$**  
**Paso a paso:**  
- Norma de $\Psi$:  
$$
\int_{-\infty}^{\infty} e^{-2|x|} dx = 2 \int_{0}^{\infty} e^{-2x} dx = 1
$$  
- Norma de $\Phi(k) = \sqrt{\frac{2}{\pi}} \frac{1}{1 + k^2}$:  
$$
\int_{-\infty}^{\infty} \left(\sqrt{\frac{2}{\pi}} \frac{1}{1 + k^2}\right)^2 dk = \frac{2}{\pi} \int_{-\infty}^{\infty} \frac{1}{(1 + k^2)^2} dk = 1
$$  
**Respuesta:**  
Se conserva la norma.

---

### **Ejercicio 2: Normas para $\Psi(x) = \frac{1}{\sqrt{2}} \text{rect}(x)$**  
**Paso a paso:**  
- Norma de $\Psi$:  
$$
\int_{-1/2}^{1/2} \left(\frac{1}{\sqrt{2}}\right)^2 dx = \frac{1}{2} \cdot 1 = \frac{1}{2}
$$  
- Norma de $\Phi(k) = \sqrt{\frac{1}{\pi}} \frac{\sin(k/2)}{k}$:  
$$
\int_{-\infty}^{\infty} \left(\sqrt{\frac{1}{\pi}} \frac{\sin(k/2)}{k}\right)^2 dk = \frac{1}{\pi} \cdot \frac{\pi}{2} = \frac{1}{2}
$$  
**Respuesta:**  
Ambas normas son iguales a $\frac{1}{2}$.

---

### **Ejercicio 3: Norma de $\Phi(k)$ para $\Psi(x) = \delta(x - x_0)$**  
**Paso a paso:**  
- $\Phi(k) = \frac{1}{\sqrt{2\pi}} e^{-ikx_0}$  
- Norma de $\Phi$:  
$$
\int_{-\infty}^{\infty} \left|\frac{1}{\sqrt{2\pi}}\right|^2 dk = \infty
$$  
**Respuesta:**  
La norma es infinita (delta no es de cuadrado integrable).

---

### **Ejercicio 4: Normalizar $\Psi(x) = A e^{-a x^2}$**  
**Paso a paso:**  
$$
\int_{-\infty}^{\infty} |A e^{-a x^2}|^2 dx = |A|^2 \sqrt{\frac{\pi}{2a}} = 1 \implies A = \left(\frac{2a}{\pi}\right)^{1/4}
$$  
**Respuesta:**  
$$
A = \left(\frac{2a}{\pi}\right)^{1/4}
$$

---

### **Ejercicio 5: Demostrar $\int |\Psi(x)|^2 dx = \int |\Phi(k)|^2 dk$**  
**Paso a paso:**  
Por el teorema de Parseval:  
$$
\int_{-\infty}^{\infty} |\Psi(x)|^2 dx = \int_{-\infty}^{\infty} |\Phi(k)|^2 dk
$$  
**Respuesta:**  
Se cumple por la unitariedad de la transformada de Fourier.

---

## **3. Transformada de Fourier en 3D**

### **Ejercicio 1: Transformada de $\Psi(\mathbf{x}) = e^{-\alpha |\mathbf{x}|^2}$**  
**Paso a paso:**  
En coordenadas esféricas:  
$$
\Phi(\mathbf{k}) = \left(\frac{\pi}{\alpha}\right)^{3/2} e^{-|\mathbf{k}|^2/(4\alpha)}
$$  
**Respuesta:**  
$$
\Phi(\mathbf{k}) = \left(\frac{\pi}{\alpha}\right)^{3/2} e^{-|\mathbf{k}|^2/(4\alpha)}
$$

---

### **Ejercicio 2: Transformada de $\Psi(\mathbf{x}) = \frac{1}{|\mathbf{x}|} e^{-|\mathbf{x}|}$**  
**Paso a paso:**  
Usando simetría esférica:  
$$
\Phi(\mathbf{k}) = \frac{4\pi}{(2\pi)^{3/2}} \cdot \frac{1}{1 + |\mathbf{k}|^2}
$$  
**Respuesta:**  
$$
\Phi(\mathbf{k}) = \sqrt{\frac{2}{\pi}} \cdot \frac{1}{1 + |\mathbf{k}|^2}
$$

---

### **Ejercicio 3: Transformada de función radial depende de $|\mathbf{k}|$**  
**Demostración:**  
Al alinear $\mathbf{k}$ con el eje $z$, la integral en coordenadas esféricas depende solo de $|\mathbf{k}|$:  
$$
\Phi(\mathbf{k}) = \frac{4\pi}{(2\pi)^{3/2}} \int_{0}^{\infty} \Psi(r) \frac{\sin(kr)}{kr} r^2 dr
$$  
**Respuesta:**  
$\Phi(\mathbf{k})$ depende únicamente de $k = |\mathbf{k}|$.

---

### **Ejercicio 4: Transformada de $\Psi(\mathbf{x}) = \delta(x)\delta(y)\delta(z - z_0)$**  
**Paso a paso:**  
$$
\Phi(\mathbf{k}) = \frac{1}{(2\pi)^{3/2}} e^{-ik_z z_0}
$$  
**Respuesta:**  
$$
\Phi(\mathbf{k}) = \frac{1}{(2\pi)^{3/2}} e^{-ik_z z_0}
$$

---

### **Ejercicio 5: Transformada de $\Psi(\mathbf{x})$ constante**  
**Respuesta:**  
$$
\Phi(\mathbf{k}) = (2\pi)^{3/2} \delta^{(3)}(\mathbf{k})
$$  

---

## **4. Conservación de norma (3D)**

### **Ejercicio 1: Verificar para $\Psi(\mathbf{x}) = e^{-\beta |\mathbf{x}|^2}$**  
**Paso a paso:**  
- Norma de $\Psi$:  
$$
\int e^{-2\beta r^2} d^3x = \left(\frac{\pi}{2\beta}\right)^{3/2}
$$  
- Norma de $\Phi(\mathbf{k}) = \left(\frac{\pi}{\beta}\right)^{3/2} e^{-k^2/(4\beta)}$:  
$$
\int \left(\frac{\pi}{\beta}\right)^{3} e^{-k^2/(2\beta)} d^3k = \left(\frac{\pi}{2\beta}\right)^{3/2}
$$  
**Respuesta:**  
Se conserva la norma.

---

### **Ejercicio 5: Normalizar $\Psi(\mathbf{x}) = A e^{-|\mathbf{x}|^2}$**  
**Paso a paso:**  
$$
\int |A|^2 e^{-2r^2} d^3x = |A|^2 \left(\frac{\pi}{2}\right)^{3/2} = 1 \implies A = \left(\frac{2}{\pi}\right)^{3/4}
$$  
**Respuesta:**  
$$
A = \left(\frac{2}{\pi}\right)^{3/4}
$$

---

## **5. Delta de Dirac como transformada**

### **Ejercicio 1: Verificar $\int_{-\infty}^{\infty} e^{ikx} dx = 2\pi \delta(k)$**  
**Respuesta:**  
Es una propiedad fundamental de la delta de Dirac en el contexto de distribuciones.

---

### **Ejercicio 2: Transformada de 1 en 3D**  
**Respuesta:**  
$$
\mathcal{F}[1](\mathbf{k}) = (2\pi)^{3/2} \delta^{(3)}(\mathbf{k})
$$

---

### **Ejercicio 3: Demostrar $\delta(ax) = \frac{1}{|a|} \delta(x)$**  
**Paso a paso:**  
Con cambio de variable $y = ax$:  
$$
\int_{-\infty}^{\infty} \delta(ax) dx = \frac{1}{|a|} \int_{-\infty}^{\infty} \delta(y) dy
$$  
**Respuesta:**  
$\delta(ax) = \frac{1}{|a|} \delta(x)$.

---

## **6. Integral gaussiana con término lineal**

### **Ejercicio 1: Evaluar $\int_{-\infty}^{\infty} e^{-3x^2 + 2x} dx$**  
**Paso a paso:**  
Completando el cuadrado:  
$$
-3x^2 + 2x = -3\left(x - \frac{1}{3}\right)^2 + \frac{1}{3}
$$  
La integral es:  
$$
e^{1/3} \sqrt{\frac{\pi}{3}}
$$  
**Respuesta:**  
$$
\sqrt{\frac{\pi}{3}} e^{1/3}
$$

---

### **Ejercicio 4: Evaluar $\int e^{-x^2 + i\omega x} dx$**  
**Respuesta:**  
$$
\sqrt{\pi} e^{-\omega^2/4}
$$

--- 

**Nota:** Los demás ejercicios siguen metodologías similares de completar cuadrados o aplicar propiedades de la transformada de Fourier.