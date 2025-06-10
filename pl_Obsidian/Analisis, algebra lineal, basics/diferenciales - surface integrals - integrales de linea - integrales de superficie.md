
 ### Simplificación de Integrales de Línea y Superficie  
En integrales de línea y superficie, los diferenciales ($dx$, $dy$, $dz$, $dr$, $d\theta$, $d\phi$) se anulan según la **geometría del camino o superficie**, cuando una variable es **constante** o su variación es **nula**. A continuación se detallan los casos:

---

### **1. Integrales de Línea** ($d\mathbf{l}$)  
#### **a) Segmentos rectos paralelos a ejes:**  
- **Paralelo a $x$**:  
  $y = \text{cte}$, $z = \text{cte}$ $\implies$ $dy=0$, $dz=0$ $\implies$ Solo $dx$.  
- **Paralelo a $y$**:  
  $x = \text{cte}$, $z = \text{cte}$ $\implies$ $dx=0$, $dz=0$ $\implies$ Solo $dy$.  
- **Paralelo a $z$**:  
  $x = \text{cte}$, $y = \text{cte}$ $\implies$ $dx=0$, $dy=0$ $\implies$ Solo $dz$.  

#### **b) Coordenadas curvilíneas:**  
- **Cilíndricas ($r,\theta,z$)**:  
  - $r = \text{cte}$ (arco circular) $\implies$ $dr=0$.  
  - $\theta = \text{cte}$ (línea radial) $\implies$ $d\theta=0$.  
  - $z = \text{cte}$ (plano horizontal) $\implies$ $dz=0$.  
- **Esféricas ($r,\theta,\phi$)**:  
  - $r = \text{cte}$ (esfera) $\implies$ $dr=0$.  
  - $\theta = \text{cte}$ (cono) $\implies$ $d\theta=0$.  
  - $\phi = \text{cte}$ (semiplano) $\implies$ $d\phi=0$.  

#### **c) Parametrización $\mathbf{r}(t) = (x(t),y(t),z(t))$**:  
Los diferenciales no nulos dependen de $\frac{dx}{dt}$, $\frac{dy}{dt}$, $\frac{dz}{dt}$.  
**Ejemplo**: Si $y=x$, $z=x^2$ con $x=t$:  
$dx=dt$, $dy=dt$, $dz=2t\,dt$ (ninguno anulado).  

---

### **2. Integrales de Superficie** ($d\mathbf{a}$)  
#### **a) Planos coordenados:**  

- **Plano $xy$ ($z=\text{cte}$)**:  
  $dz=0$ $\implies$ $d\mathbf{a} = dx\,dy\,\hat{\mathbf{e_z}}$.  
- 
- **Plano $xz$ ($y=\text{cte}$)**:  
  $dy=0$ $\implies$ $d\mathbf{a} = dx\,dz\,\hat{\mathbf{e_y}}$.  
- 
- **Plano $yz$ ($x=\text{cte}$)**:  
  $dx=0$ $\implies$ $d\mathbf{a} = dy\,dz\,\hat{\mathbf{e_x}}$.  

#### **b) Superficies curvilíneas:**  
- **Cilíndricas**:  
  - $r=\text{cte}$ (cilindro) $\implies$ $dr=0$ $\implies$ $d\mathbf{a} = r\,d\theta\,dz\,\hat{\mathbf{r}}$.  
  - $z=\text{cte}$ (tapa) $\implies$ $dz=0$ $\implies$ $d\mathbf{a} = r\,dr\,d\theta\,\hat{\mathbf{z}}$.  
- **Esféricas**:  
  - $r=\text{cte}$ (esfera) $\implies$ $dr=0$ $\implies$ $d\mathbf{a} = r^2 \sin\theta\,d\theta\,d\phi\,\hat{\mathbf{r}}$.  
  - $\theta=\text{cte}$ (cono) $\implies$ $d\theta=0$ $\implies$ $d\mathbf{a} = r \sin\theta\,dr\,d\phi\,\hat{\boldsymbol{\theta}}$.  
  - $\phi=\text{cte}$ (semiplano) $\implies$ $d\phi=0$ $\implies$ $d\mathbf{a} = r\,dr\,d\theta\,\hat{\boldsymbol{\phi}}$.  

#### **c) Parametrización $\mathbf{r}(u,v) = (x(u,v),y(u,v),z(u,v))$**:  
**Ejemplo**: Superficie $z=f(x,y)$:  
$d\mathbf{a} = \left(-\frac{\partial f}{\partial x}, -\frac{\partial f}{\partial y}, 1\right) dx\,dy$ (sin anulaciones).  

---

### **Regla general**  
- **Línea**: Un diferencial ($dx$, $dy$, $dz$, $dr$, $d\theta$, $d\phi$) se anula si su variable es **constante** en el camino.  
- **Superficie**: Un diferencial se anula si su variable es **constante** en la superficie, y $d\mathbf{a}$ es normal a la superficie.  

**Nota**: Estas simplificaciones son esenciales en electromagnetismo, mecánica de fluidos y teoría de campos.

---
---
# **20 Ejemplos de Caminos y Superficies con Parametrización y Diferenciales Anulados**  
Se presenta cada caso con parametrización, condiciones geométricas, diferenciales anulados y elemento diferencial. Las ecuaciones se expresan en LaTeX.

---
---

### **I. Integrales de Línea**  
#### **1. Segmento recto paralelo al eje $x$**  
- **Descripción**: $(0,0,0) \to (5,0,0)$  
- **Parametrización**: $\mathbf{r}(t) = (t, 0, 0)$, $t \in [0,5]$  
- **Diferenciales anulados**: $dy = 0$, $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (dx, 0, 0) = (dt, 0, 0)$$  

#### **2. Segmento recto paralelo al eje $y$**  
- **Descripción**: $(0,0,0) \to (0,3,0)$  
- **Parametrización**: $\mathbf{r}(t) = (0, t, 0)$, $t \in [0,3]$  
- **Diferenciales anulados**: $dx = 0$, $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (0, dy, 0) = (0, dt, 0)$$  

#### **3. Segmento recto paralelo al eje $z$**  
- **Descripción**: $(1,1,0) \to (1,1,4)$  
- **Parametrización**: $\mathbf{r}(t) = (1, 1, t)$, $t \in [0,4]$  
- **Diferenciales anulados**: $dx = 0$, $dy = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (0, 0, dz) = (0, 0, dt)$$  

#### **4. Camino circular en plano $xy$ ($z = 0$)**  
- **Descripción**: $x^2 + y^2 = 4$, $z = 0$  
- **Parametrización**: $\mathbf{r}(t) = (2\cos t, 2\sin t, 0)$, $t \in [0, \pi]$  
- **Diferenciales anulados**: $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (-2\sin t  dt, 2\cos t  dt, 0)$$  

#### **5. Línea radial en cilíndricas ($\theta$ fijo)**  
- **Descripción**: $\theta = \pi/3$, $z = 0$, $r: 0 \to 2$  
- **Parametrización**: $\mathbf{r}(t) = (t \cos \tfrac{\pi}{3}, t \sin \tfrac{\pi}{3}, 0)$, $t \in [0,2]$  
- **Diferenciales anulados**: $d\theta = 0$, $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (\cos\tfrac{\pi}{3}  dt, \sin\tfrac{\pi}{3}  dt, 0)$$  

#### **6. Arco en cilíndricas ($r$ fijo, $z$ fijo)**  
- **Descripción**: $r = 3$, $z = 1$, $\theta: 0 \to \pi/2$  
- **Parametrización**: $\mathbf{r}(t) = (3\cos t, 3\sin t, 1)$, $t \in [0, \pi/2]$  
- **Diferenciales anulados**: $dr = 0$, $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (-3\sin t  dt, 3\cos t  dt, 0)$$  

#### **7. Hélice cilíndrica ($r$ fijo)**  
- **Descripción**: $r = 2$, $z = t$, $\theta = t$  
- **Parametrización**: $\mathbf{r}(t) = (2\cos t, 2\sin t, t)$, $t \in [0, 4\pi]$  
- **Diferenciales anulados**: $dr = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (-2\sin t  dt, 2\cos t  dt, dt)$$  

#### **8. Meridiano esférico ($\phi$ fijo)**  
- **Descripción**: $\phi = \pi/4$, $r = 1$, $\theta: 0 \to \pi$  
- **Parametrización**: $\mathbf{r}(t) = (\sin t \cos \tfrac{\pi}{4}, \sin t \sin \tfrac{\pi}{4}, \cos t)$, $t \in [0, \pi]$  
- **Diferenciales anulados**: $dr = 0$, $d\phi = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (\cos t \cos\tfrac{\pi}{4}  dt, \cos t \sin\tfrac{\pi}{4}  dt, -\sin t  dt)$$  

#### **9. Paralelo esférico ($\theta$ fijo)**  
- **Descripción**: $\theta = \pi/3$, $r = 2$, $\phi: 0 \to 2\pi$  
- **Parametrización**: $\mathbf{r}(t) = (2 \sin \tfrac{\pi}{3} \cos t, 2 \sin \tfrac{\pi}{3} \sin t, 2 \cos \tfrac{\pi}{3})$, $t \in [0, 2\pi]$  
- **Diferenciales anulados**: $dr = 0$, $d\theta = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (-2 \sin\tfrac{\pi}{3} \sin t  dt, 2 \sin\tfrac{\pi}{3} \cos t  dt, 0)$$  

#### **10. Camino parabólico $y = x^2$, $z = 0$**  
- **Descripción**: $(0,0,0) \to (2,4,0)$  
- **Parametrización**: $\mathbf{r}(t) = (t, t^2, 0)$, $t \in [0,2]$  
- **Diferenciales anulados**: $dz = 0$  
- **Elemento**:  
  $$d\mathbf{l} = (dt, 2t  dt, 0)$$  

---

### **II. Integrales de Superficie**  
#### **11. Plano $xy$ ($z = 0$)**  
- **Descripción**: $x \in [0,1]$, $y \in [0,1]$, $z = 0$  
- **Parametrización**: $\mathbf{r}(u,v) = (u, v, 0)$, $u,v \in [0,1]$  
- **Diferenciales anulados**: $dz = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = (0,0,1)  du  dv$$  

#### **12. Plano $xz$ ($y = 1$)**  
- **Descripción**: $x \in [0,2]$, $z \in [0,3]$, $y = 1$  
- **Parametrización**: $\mathbf{r}(u,v) = (u, 1, v)$, $u \in [0,2]$, $v \in [0,3]$  
- **Diferenciales anulados**: $dy = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = (0,-1,0)  du  dv$$  

#### **13. Cilindro $r = 4$ (cilíndricas)**  
- **Descripción**: $r = 4$, $\theta \in [0,2\pi]$, $z \in [0,5]$  
- **Parametrización**: $\mathbf{r}(u,v) = (4 \cos u, 4 \sin u, v)$, $u \in [0,2\pi]$, $v \in [0,5]$  
- **Diferenciales anulados**: $dr = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = (4 \cos u, 4 \sin u, 0)  du  dv$$  

#### **14. Tapa superior cilíndrica ($z = 5$)**  
- **Descripción**: $z = 5$, $r \in [0,3]$, $\theta \in [0,2\pi]$  
- **Parametrización**: $\mathbf{r}(u,v) = (u \cos v, u \sin v, 5)$, $u \in [0,3]$, $v \in [0,2\pi]$  
- **Diferenciales anulados**: $dz = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = (0,0,u)  du  dv$$  

#### **15. Esfera $r = 2$ (esféricas)**  
- **Descripción**: $r = 2$, $\theta \in [0,\pi]$, $\phi \in [0,2\pi]$  
- **Parametrización**: $\mathbf{r}(u,v) = (2 \sin u \cos v, 2 \sin u \sin v, 2 \cos u)$, $u \in [0,\pi]$, $v \in [0,2\pi]$  
- **Diferenciales anulados**: $dr = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = 4 \sin u  (\sin u \cos v, \sin u \sin v, \cos u)  du  dv$$  

#### **16. Cono $\theta = \pi/6$ (esféricas)**  
- **Descripción**: $\theta = \pi/6$, $r \in [0,4]$, $\phi \in [0,2\pi]$  
- **Parametrización**: $\mathbf{r}(u,v) = (u \sin \tfrac{\pi}{6} \cos v, u \sin \tfrac{\pi}{6} \sin v, u \cos \tfrac{\pi}{6})$, $u \in [0,4]$, $v \in [0,2\pi]$  
- **Diferenciales anulados**: $d\theta = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = \left( \tfrac{\sqrt{3}}{2} u \cos v, \tfrac{\sqrt{3}}{2} u \sin v, -\tfrac{1}{2} u \right) du  dv$$  

#### **17. Semiplanos meridionales ($\phi = \pi/2$)**  
- **Descripción**: $\phi = \pi/2$, $r \in [0,1]$, $\theta \in [0,\pi]$  
- **Parametrización**: $\mathbf{r}(u,v) = (0, u \sin v, u \cos v)$, $u \in [0,1]$, $v \in [0,\pi]$  
- **Diferenciales anulados**: $d\phi = 0$  
- **Elemento de área**:  
  $$d\mathbf{a} = (0, u \cos v, -u \sin v)  du  dv$$  

#### **18. Paraboloide $z = x^2 + y^2$**  
- **Descripción**: $x \in [-1,1]$, $y \in [-1,1]$  
- **Parametrización**: $\mathbf{r}(u,v) = (u, v, u^2 + v^2)$, $u,v \in [-1,1]$  
- **Diferenciales anulados**: Ninguno  
- **Elemento de área**:  
  $$d\mathbf{a} = (-2u, -2v, 1)  du  dv$$  

#### **19. Cono de revolución $y = \sqrt{x^2 + z^2}$**  
- **Descripción**: $x \in [0,2]$, $z \in [-1,1]$  
- **Parametrización**: $\mathbf{r}(u,v) = (u, \sqrt{u^2 + v^2}, v)$, $u \in [0,2]$, $v \in [-1,1]$  
- **Diferenciales anulados**: Ninguno  
- **Elemento de área**:  
  $$d\mathbf{a} = \left( -\tfrac{u}{\sqrt{u^2+v^2}}, 1, -\tfrac{v}{\sqrt{u^2+v^2}} \right) du  dv$$  

#### **20. Plano inclinado $x + y + z = 1$**  
- **Descripción**: Vértices $(1,0,0)$, $(0,1,0)$, $(0,0,1)$  
- **Parametrización**: $\mathbf{r}(u,v) = (u, v, 1 - u - v)$, $u \in [0,1]$, $v \in [0,1-u]$  
- **Diferenciales anulados**: Ninguno  
- **Elemento de área**:  
  $$d\mathbf{a} = (1,1,1)  du  dv$$  

---

### **Clave de simplificación**  
- **Diferenciales anulados en caminos**:  
  - $dx = 0$ si $x$ constante (ej: segmentos paralelos a $y$ o $z$).  
  - $d\theta = 0$ en líneas radiales (cilíndricas/esféricas).  
  - $dr = 0$ en trayectorias con radio fijo (circunferencias, hélices).  

- **Diferenciales anulados en superficies**:  
  - $dz = 0$ en planos horizontales ($xy$).  
  - $dr = 0$ en superficies radiales fijas (esferas, cilindros).  
  - $d\theta = 0$ en conos ($\theta$ constante).  

- **Parametrización**:  
  - **Caminos**: $t$ como parámetro único.  
  - **Superficies**: $(u,v)$ como parámetros independientes.  

> **Nota**: Las integrales se simplifican al eliminar términos con diferenciales nulos, reduciendo el cálculo a las variables activas.