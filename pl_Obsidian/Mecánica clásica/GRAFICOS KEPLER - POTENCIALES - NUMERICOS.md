## Ejemplos Numéricos y Gráficos: Estabilidad de Órbitas Circulares y Oscilaciones Radiales

---

### Ejemplo 1: Potencial Gravitacional Newtoniano

### Datos:
- Constante gravitacional combinada:  
  $$
  k = GM\mu = 1.0 \times 10^5\, \mathrm{J \cdot m}
  $$
- Masa reducida:  
  $$
  \mu = 1.0\, \mathrm{kg}
  $$
- Momento angular:  
  $$
  L = 2.0 \times 10^3\, \mathrm{kg \cdot m^2/s}
  $$

---

#### Paso 1: Encontrar el radio de la órbita circular estable
Recordamos la fórmula:  
$$
r_0 = \frac{L^2}{\mu k}
$$  
Calculamos:  
$$
r_0 = \frac{(2.0 \times 10^3)^2}{1.0 \times 1.0 \times 10^5} = \frac{4.0 \times 10^6}{1.0 \times 10^5} = 40\, \mathrm{m}
$$

---

#### Paso 2: Comprobar estabilidad (segunda derivada)
La segunda derivada es:  
$$
\left. \frac{d^2 V_{\text{eff}}}{dr^2} \right|_{r_0} = \frac{k}{r_0^3} = \frac{1.0 \times 10^5}{40^3} = \frac{1.0 \times 10^5}{64\,000} \approx 1.56\, \mathrm{J/m^2}
$$

---

#### Paso 3: Calcular frecuencia de oscilación radial
$$
\omega_r = \sqrt{\frac{k_{\text{eff}}}{\mu}} = \sqrt{\frac{1.56}{1.0}} \approx 1.25\, \mathrm{rad/s}
$$

---

#### Paso 4: Graficar $V_{\text{eff}}(r)$ alrededor de $r_0$
- Rango: $r \in [30,\, 50]\, \mathrm{m}$  
- Evaluar:  
  $$
  V_{\text{eff}}(r) = -\frac{k}{r} + \frac{L^2}{2 \mu r^2}
  $$

### Código para generar el gráfico en Python (Matplotlib):

```python
import numpy as np
import matplotlib.pyplot as plt

# Parámetros
k = 1e5
mu = 1.0
L = 2e3
r0 = (L**2) / (mu * k)

# Función potencial efectivo
def V_eff(r):
    return -k / r + (L**2) / (2 * mu * r**2)

# Rango de r cerca de r0
r = np.linspace(30, 50, 400)
V = V_eff(r)

plt.figure(figsize=(8,5))
plt.plot(r, V, label='$V_{eff}(r)$')
plt.axvline(r0, color='r', linestyle='--', label='$r_0$')
plt.title('Potencial efectivo $V_{eff}(r)$ con órbita circular estable')
plt.xlabel('$r$ (m)')
plt.ylabel('Energía (J)')
plt.legend()
plt.grid(True)
plt.show()
```

---

### Interpretación:

- El gráfico muestra un **mínimo claro en $r_0 = 40\, \mathrm{m}$**, indicando estabilidad.  
- Si la partícula se aleja un poco de $r_0$, siente una fuerza restauradora.  
- La frecuencia radial $\omega_r \approx 1.25\, \mathrm{rad/s}$ determina la rapidez de las oscilaciones.
    

---

### Ejemplo 2: Potencial de Yukawa con parámetros

- $k = 1.0 \times 10^5\, \mathrm{J \cdot m}$  
- $\alpha = 0.05\, \mathrm{m^{-1}}$  
- $\mu = 1.0\, \mathrm{kg}$  
- $L = 2.0 \times 10^3\, \mathrm{kg \cdot m^2/s}$  

**Función del potencial efectivo Yukawa**:  
$$
V_{\text{eff}}(r) = -\frac{k e^{-\alpha r}}{r} + \frac{L^2}{2 \mu r^2}
$$
---
#### Gráfico del potencial efectivo

```python
import numpy as np
import matplotlib.pyplot as plt

k = 1e5
alpha = 0.05
mu = 1.0
L = 2e3

def V_eff_yukawa(r):
    return -k * np.exp(-alpha * r) / r + (L**2) / (2 * mu * r**2)

r = np.linspace(10, 60, 500)
V = V_eff_yukawa(r)

plt.figure(figsize=(8,5))
plt.plot(r, V, label='$V_{eff}(r)$ Yukawa')
plt.title('Potencial efectivo Yukawa con $\\alpha=0.05$')
plt.xlabel('$r$ (m)')
plt.ylabel('Energía (J)')
plt.legend()
plt.grid(True)
plt.show()
```

---

#### Interpretación:

- Para ciertos valores de α\alpha, el mínimo local puede desaparecer o cambiar su posición.
    
- Esto afecta la **estabilidad** de las órbitas circulares.
    
- Se recomienda calcular numéricamente la derivada segunda para verificar estabilidad.
    

---

### Aplicación común en exámenes:

1. **Calcular $r_0$ para una órbita circular dada $L$, $\mu$, $k$**.  
2. **Evaluar la estabilidad comprobando el signo de $\frac{d^2 V_{\text{eff}}}{dr^2}$**.  
3. **Encontrar la frecuencia de pequeñas oscilaciones radiales $\omega_r$**.  
4. Graficar $V_{\text{eff}}$ para ilustrar los puntos de equilibrio y estabilidad.

