**1. Lagrangiano del sistema:**  
Utilizando coordenadas polares $(r, \theta)$, donde $r$ es la distancia radial desde el origen y $\theta$ es el ángulo con respecto al eje vertical $y$, el Lagrangiano $L = T - V$ queda:  
$$
L = \frac{1}{2}m\left(\dot{r}^2 + r^2 \dot{\theta}^2\right) - \left[\frac{1}{2}k(r - \ell)^2 + mgr\cos\theta\right],
$$  
donde:  
- $T = \frac{1}{2}m(\dot{r}^2 + r^2 \dot{\theta}^2)$ es la energía cinética en coordenadas polares .  
- $V = \frac{1}{2}k(r - \ell)^2 + mgr\cos\theta$ incluye la energía potencial elástica del resorte y la gravitatoria .  

---

**2. Fuerzas generalizadas asociadas a la fuerza viscosa:**  
La fuerza viscosa $\mathbf{f} = -\mu \mathbf{v}$ se expresa en coordenadas generalizadas mediante:  
$$
Q_r = -\mu \dot{r}, \quad Q_\theta = -\mu r^2 \dot{\theta}.
$$  
**Explicación:**  
- **Componente radial $Q_r$:**  
  Se obtiene proyectando $\mathbf{f}$ sobre la derivada parcial de la posición respecto a $r$:  
  $$
  Q_r = \mathbf{f} \cdot \frac{\partial \mathbf{r}}{\partial r} = -\mu (\dot{r} \sin\theta + r \cos\theta \, \dot{\theta}) \cdot \sin\theta - \mu (\dot{r} \cos\theta - r \sin\theta \, \dot{\theta}) \cdot \cos\theta = -\mu \dot{r} \quad .
  $$  
- **Componente angular $Q_\theta$:**  
  Proyectando $\mathbf{f}$ sobre la derivada parcial de la posición respecto a $\theta$:  
  $$
  Q_\theta = \mathbf{f} \cdot \frac{\partial \mathbf{r}}{\partial \theta} = -\mu (\dot{r} \sin\theta + r \cos\theta \, \dot{\theta}) \cdot r \cos\theta + \mu (\dot{r} \cos\theta - r \sin\theta \, \dot{\theta}) \cdot r \sin\theta = -\mu r^2 \dot{\theta} \quad .
  $$  

**Respuestas finales:**  
1. $\boxed{L = \frac{1}{2}m\left(\dot{r}^2 + r^2 \dot{\theta}^2\right) - \frac{1}{2}k(r - \ell)^2 - mgr\cos\theta}$  
2. $\boxed{Q_r = -\mu \dot{r}}, \quad \boxed{Q_\theta = -\mu r^2 \dot{\theta}}$