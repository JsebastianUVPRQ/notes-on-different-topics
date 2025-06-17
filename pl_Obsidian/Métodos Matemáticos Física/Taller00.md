![[Pasted image 20250614183610.png]]

### **Problema 19: Determine si la serie es absolutamente convergente, condicionalmente convergente o divergente**  

#### **(a)** $$\sum_{n=1}^{\infty} \frac{\cos(n\pi/3)}{n!}$$  

**Solución paso a paso:**  
1. **Análisis de convergencia absoluta:**  
   Consideramos la serie de valores absolutos:  
   $$\sum_{n=1}^{\infty} \left| \frac{\cos(n\pi/3)}{n!} \right| = \sum_{n=1}^{\infty} \frac{|\cos(n\pi/3)|}{n!}.$$  
   Como $|\cos(n\pi/3)| \leq 1$ para todo $n$, se cumple:  
   $$\frac{|\cos(n\pi/3)|}{n!} \leq \frac{1}{n!}.$$  
   La serie $\sum_{n=1}^{\infty} \frac{1}{n!}$ es convergente (es la serie de la exponencial evaluada en 1, menos el término $n=0$, y $e^1 = e$). Por el criterio de comparación directa, la serie de valores absolutos converge.  

2. **Conclusión:**  
   Como la serie de valores absolutos converge, la serie original es **absolutamente convergente**.  
   **Nota:** La convergencia absoluta implica convergencia condicional, pero en este caso no es necesario analizar por separado.  

**Respuesta final:**  
La serie es **absolutamente convergente**.  

---  

#### **(b)** $$\sum_{n=1}^{\infty} \frac{(-2)^n}{n^n}$$  

**Solución paso a paso:**  
1. **Análisis de convergencia absoluta:**  
   Consideramos la serie de valores absolutos:  
   $$\sum_{n=1}^{\infty} \left| \frac{(-2)^n}{n^n} \right| = \sum_{n=1}^{\infty} \frac{2^n}{n^n}.$$  
   Aplicamos el criterio de la raíz:  
   $$\lim_{n \to \infty} \sqrt[n]{\frac{2^n}{n^n}} = \lim_{n \to \infty} \frac{2}{n} = 0 < 1.$$  
   Como el límite es menor que 1, la serie de valores absolutos converge.  

2. **Conclusión:**  
   La serie original es **absolutamente convergente**.  

**Respuesta final:**  
La serie es **absolutamente convergente**.  

---  

#### **(c)** $$\sum_{n=1}^{\infty} \left( \frac{n^2 + 1}{2n^2 + 1} \right)^n$$  

**Solución paso a paso:**  
1. **Análisis de convergencia:**  
   Observamos que $a_n = \left( \frac{n^2 + 1}{2n^2 + 1} \right)^n > 0$ para todo $n$, por lo que la serie es de términos positivos.  
   Aplicamos el criterio de la raíz:  
   $$\lim_{n \to \infty} \sqrt[n]{a_n} = \lim_{n \to \infty} \frac{n^2 + 1}{2n^2 + 1} = \frac{1}{2} < 1.$$  
   Como el límite es menor que 1, la serie converge.  

2. **Conclusión:**  
   Al ser una serie de términos positivos y convergente, es **absolutamente convergente**.  

**Respuesta final:**  
La serie es **absolutamente convergente**.  

---  

#### **(d)** $$\sum_{n=2}^{\infty} \left( \frac{-2n}{n+1} \right)^{5n}$$  

**Solución paso a paso:**  
1. **Análisis del término general:**  
   Expresamos el término general como:  
   $$a_n = \left( \frac{-2n}{n+1} \right)^{5n} = (-1)^{5n} \left( \frac{2n}{n+1} \right)^{5n} = (-1)^n \left( \frac{2n}{n+1} \right)^{5n},$$  
   ya que $(-1)^{5n} = [(-1)^5]^n = (-1)^n$.  
   El valor absoluto es:  
   $$|a_n| = \left( \frac{2n}{n+1} \right)^{5n}.$$  

2. **Análisis de convergencia absoluta:**  
   Simplificamos:  
   $$\frac{2n}{n+1} = 2 \left(1 - \frac{1}{n+1}\right), \quad \text{así que} \quad |a_n| = \left[ 2 \left(1 - \frac{1}{n+1}\right) \right]^{5n} = 32^n \left(1 - \frac{1}{n+1}\right)^{5n}.$$  
   Calculamos el límite usando el criterio de la raíz:  
   $$\lim_{n \to \infty} \sqrt[n]{|a_n|} = \lim_{n \to \infty} 32 \cdot \left(1 - \frac{1}{n+1}\right)^5.$$  
   Como $\lim_{n \to \infty} \left(1 - \frac{1}{n+1}\right)^5 = 1^5 = 1$, entonces:  
   $$\lim_{n \to \infty} \sqrt[n]{|a_n|} = 32 \cdot 1 = 32 > 1.$$  
   Por el criterio de la raíz, la serie de valores absolutos $\sum |a_n|$ diverge.  

3. **Análisis de convergencia condicional:**  
   Verificamos si $a_n \to 0$:  
   $$|a_n| = 32^n \left(1 - \frac{1}{n+1}\right)^{5n}.$$  
   Como $\lim_{n \to \infty} \left(1 - \frac{1}{n+1}\right)^{n+1} = e^{-1}$, entonces:  
   $$\left(1 - \frac{1}{n+1}\right)^{5n} = \left[ \left(1 - \frac{1}{n+1}\right)^{n+1} \right]^{\frac{5n}{n+1}} \to (e^{-1})^5 = e^{-5} > 0.$$  
   Así, $|a_n| \sim 32^n \cdot e^{-5}$. Como $32^n$ crece exponencialmente, $|a_n| \to \infty$ cuando $n \to \infty$. Por tanto, $a_n$ no tiende a 0.  

4. **Conclusión:**  
   Como $\lim_{n \to \infty} a_n \neq 0$ (de hecho, $|a_n| \to \infty$), la serie diverge por el criterio del término general.  

**Respuesta final:**  
La serie es **divergente**.  

---  

### **Problema 20: ¿Para cuáles enteros positivos $k$ la serie $\sum_{n=1}^{\infty} \frac{(n!)^2}{(kn)!}$ es convergente?**  

**Solución paso a paso:**  
1. **Aplicamos el criterio del cociente:**  
   Sea $a_n = \frac{(n!)^2}{(kn)!}$. Calculamos:  
   $$\frac{a_{n+1}}{a_n} = \frac{\frac{[(n+1)!]^2}{[k(n+1)]!}}{\frac{(n!)^2}{(kn)!}} = \frac{[(n+1)!]^2}{(n!)^2} \cdot \frac{(kn)!}{(kn + k)!} = (n+1)^2 \cdot \frac{(kn)!}{(kn + k)(kn + k-1) \cdots (kn + 1)(kn)!}.$$  
   Simplificamos:  
   $$\frac{a_{n+1}}{a_n} = \frac{(n+1)^2}{(kn + k)(kn + k-1) \cdots (kn + 1)}.$$  
   El denominador tiene $k$ factores, cada uno asintóticamente equivalente a $kn$ cuando $n \to \infty$. Así:  
   $$\frac{a_{n+1}}{a_n} \sim \frac{(n+1)^2}{(kn)^k} \sim \frac{n^2}{k^k n^k} = \frac{1}{k^k} n^{2-k}.$$  
   Tomamos el límite:  
   $$L = \lim_{n \to \infty} \frac{a_{n+1}}{a_n} = \lim_{n \to \infty} \frac{1}{k^k} n^{2-k}.$$  

2. **Casos según $k$:**  
   - **Si $k = 1$:**  
     $L = \lim_{n \to \infty} \frac{1}{1^1} n^{2-1} = \lim_{n \to \infty} n = \infty > 1$.  
     Además, $a_n = \frac{(n!)^2}{n!} = n!$, y $\sum n!$ diverge.  
   - **Si $k = 2$:**  
     $L = \lim_{n \to \infty} \frac{1}{4} n^{0} = \frac{1}{4} < 1$.  
     Por el criterio del cociente, la serie converge.  
   - **Si $k > 2$:**  
     $L = \lim_{n \to \infty} \frac{1}{k^k} n^{2-k} = 0 < 1$ (pues $2-k < 0$).  
     Por el criterio del cociente, la serie converge.  

3. **Conclusión:**  
   La serie converge para $k \geq 2$.  
   **Nota:** $k$ es entero positivo, por lo que $k = 2, 3, 4, \ldots$.  

**Respuesta final:**  
La serie converge para **enteros positivos $k \geq 2$**.  

---  

### **Problema 21:**  

#### **(a)** Demuestre que $\sum_{n=0}^{\infty} \frac{x^n}{n!}$ converge para toda $x$.  

**Solución paso a paso:**  
1. **Aplicamos el criterio del cociente:**  
   Sea $a_n = \frac{x^n}{n!}$. Calculamos:  
   $$\left| \frac{a_{n+1}}{a_n} \right| = \left| \frac{\frac{x^{n+1}}{(n+1)!}}{\frac{x^n}{n!}} \right| = \left| \frac{x^{n+1} n!}{x^n (n+1)!} \right| = \left| \frac{x}{n+1} \right|.$$  
   Tomamos el límite:  
   $$L = \lim_{n \to \infty} \left| \frac{x}{n+1} \right| = |x| \lim_{n \to \infty} \frac{1}{n+1} = 0 < 1 \quad \text{para todo } x \in \mathbb{R}.$$  

2. **Conclusión:**  
   Como $L < 1$ para todo $x$, la serie converge absolutamente (y por tanto converge) para todo $x$ real.  

**Respuesta final:**  
La serie converge para toda $x$.  

---  

#### **(b)** Deduzca que $\lim_{n \to \infty} \frac{x^n}{n!} = 0$ para toda $x$.  

**Solución paso a paso:**  
1. **Relación con la serie convergente:**  
   Por el apartado (a), $\sum_{n=0}^{\infty} a_n$ con $a_n = \frac{x^n}{n!}$ converge para todo $x$.  

2. **Propiedad de convergencia de series:**  
   Si una serie $\sum_{n=0}^{\infty} b_n$ converge, entonces $\lim_{n \to \infty} b_n = 0$.  
   Aquí, $b_n = a_n$, así que:  
   $$\lim_{n \to \infty} \frac{x^n}{n!} = 0 \quad \text{para todo } x.$$  

3. **Caso particular $x = 0$:**  
   Si $x = 0$, $\frac{0^n}{n!} = 0$ para $n \geq 1$, y el límite es 0.  

**Respuesta final:**  
Se cumple $\lim_{n \to \infty} \frac{x^n}{n!} = 0$ para toda $x$.  

---  

Espero que estas soluciones detalladas sean útiles. Si necesita más aclaraciones, no dude en preguntar.