## 20 Ejercicios sobre Identidades de Integrales Superficie-Volumen en Teoría Electromagnética

Los siguientes ejercicios aplican identidades integrales (Teorema de la Divergencia, Teorema de Stokes) a problemas electromagnéticos, utilizando las relaciones fundamentales entre integrales de volumen, superficie y línea. Se basan en las **identidades vectoriales** presentadas en la literatura estándar y en recursos como Wikipedia .

---

### **Parte 1: Identidades Básicas y Teoremas Fundamentales**
1.  **Ley de Gauss - Carga puntual:**  
    Verifique la Ley de Gauss para una carga puntual $q$ en el origen, usando una superficie esférica $S$ de radio $R$. Calcule $\oint_S \mathbf{E} \cdot d\mathbf{S}$ y relacione el resultado con $\frac{q}{\epsilon_0}$ usando el Teorema de la Divergencia .  
    *Dificultad: Baja | Aplicación: Campo electrostático*  

2.  **Teorema de Stokes - Campo uniforme:**  
    Para un campo magnético constante $\mathbf{B} = B_0 \hat{z}$, demuestre que $\oint_C \mathbf{B} \cdot d\mathbf{l} = 0$ sobre cualquier curva cerrada $C$, usando el Teorema de Stokes y la identidad $\nabla \times \mathbf{B} = \mathbf{0}$.  
    *Dificultad: Baja | Aplicación: Campos conservativos*  

3.  **Ley de Gauss para el magnetismo:**  
    Demuestre que para cualquier superficie cerrada $S$ que encierre un volumen $V$, $\oint_S \mathbf{B} \cdot d\mathbf{S} = 0$, usando el Teorema de la Divergencia y la ecuación $\nabla \cdot \mathbf{B} = 0$.  
    *Dificultad: Baja | Aplicación: Monopolos magnéticos*  

4.  **Identidad de flujo eléctrico:**  
    Dada una región $V$ con densidad volumétrica de carga $\rho$, use el Teorema de la Divergencia para probar que $\oint_{\partial V} \mathbf{E} \cdot d\mathbf{S} = \frac{Q_{\text{int}}}{\epsilon_0}$, donde $\partial V$ es la frontera de $V$.  
    *Dificultad: Media | Aplicación: Ley de Gauss*  

5.  **Circulación de campo eléctrico estático:**  
    Para un campo electrostático $\mathbf{E}$, demuestre que $\oint_C \mathbf{E} \cdot d\mathbf{l} = 0$ sobre cualquier trayectoria cerrada $C$, usando el Teorema de Stokes y la ley de Faraday en estado estacionario.  
    *Dificultad: Media | Aplicación: Potencial eléctrico*  

---

### **Parte 2: Aplicaciones a Campos Estáticos**
6.  **Capacitancia de esfera conductora:**  
    Una esfera conductora de radio $a$ tiene carga $Q$. Use la Ley de Gauss para hallar $\mathbf{E}$ y luego calcule la diferencia de potencial $V$ entre la esfera e infinito. Finalmente, encuentre la capacitancia $C = Q/V$ .  
    *Dificultad: Media | Aplicación: Capacitancia*  

7.  **Energía en campo electrostático:**  
    Demuestre que la energía almacenada en un campo eléctrico es $U = \frac{1}{2} \int_V \epsilon_0 E^2 dV$ para una distribución de carga en un volumen $V$, usando la identidad:  
   $$
    \int_V \mathbf{E} \cdot \mathbf{D}  dV = \oint_S \phi \mathbf{D} \cdot d\mathbf{S} - \int_V \phi \nabla \cdot \mathbf{D}  dV
   $$  
    y la ecuación de Poisson.  
    *Dificultad: Alta | Aplicación: Energía electrostática*  

8.  **Fuerza entre placas de capacitor:**  
    Dos placas paralelas con cargas $+Q$ y \(-Q\) están separadas una distancia $d$. Use la relación $\mathbf{F} = \oint_S \mathbf{T} \cdot d\mathbf{S}$ (tensor de Maxwell) para calcular la fuerza de atracción, donde el tensor es $T_{ij} = \epsilon_0 \left( E_i E_j - \frac{1}{2} \delta_{ij} E^2 \right)$.  
    *Dificultad: Alta | Aplicación: Fuerzas electromagnéticas*  

9.  **Inductancia de un solenoide:**  
    Para un solenoide infinito con $n$ vueltas por unidad y corriente $I$, calcule el flujo magnético $\Phi_B$ a través de una sección transversal. Luego, use $\Phi_B = LI$ para encontrar la inductancia $L$. Verifique que $\frac{1}{2} LI^2 = \int \frac{B^2}{2\mu_0} dV$ en su volumen.  
    *Dificultad: Media | Aplicación: Inductancia*  

10. **Campo magnético de alambre infinito:**  
    Un alambre recto infinito lleva corriente $I$. Use la Ley de Ampère para hallar $\mathbf{B}$ y luego aplique el Teorema de Stokes a $\oint_C \mathbf{B} \cdot d\mathbf{l} = \mu_0 I$ para mostrar que $\nabla \times \mathbf{B} = \mu_0 \mathbf{J}$.  
    *Dificultad: Media | Aplicación: Ley de Ampère*  

11. **Teorema de Poynting estático:**  
    Demuestre que en condiciones estacionarias, $\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} = 0$, usando el Teorema de la Divergencia y las ecuaciones de Maxwell.  
    *Dificultad: Media | Aplicación: Conservación de energía*  

12. **Vector de potencial magnético:**  
    Para un campo magnético $\mathbf{B} = \nabla \times \mathbf{A}$, demuestre que $\oint_S \mathbf{B} \cdot d\mathbf{S} = 0$ usando el Teorema de Stokes sobre $\nabla \cdot (\nabla \times \mathbf{A}) = 0$.  
    *Dificultad: Baja | Aplicación: Potencial vectorial*  

13. **Relación entre flujo y corriente:**  
    En un cable cilíndrico de radio $R$ con densidad de corriente uniforme $\mathbf{J}$, calcule $\oint_C \mathbf{A} \cdot d\mathbf{l}$ alrededor del borde del cable y relácionelo con $\int_S \mathbf{B} \cdot d\mathbf{S}$ usando el Teorema de Stokes .  
    *Dificultad: Alta | Aplicación: Ley de Ampère*  

14. **Campo en cavidad esférica:**  
    Una esfera de radio $R$ tiene carga uniforme $\rho$. Al remover una cavidad esférica concéntrica de radio $a$, use la Ley de Gauss para hallar $\mathbf{E}$ dentro de la cavidad.  
    *Dificultad: Media | Aplicación: Campo en medios con huecos*  

15. **Momento dipolar eléctrico:**  
    Para una esfera uniformemente cargada con densidad $\rho$, demuestre que el momento dipolar es cero usando $\mathbf{p} = \int_V \mathbf{r} \rho  dV$ y argumentos de simetría.  
    *Dificultad: Baja | Aplicación: Multipolos*  

---

### **Parte 3: Campos Dinámicos y Ondas**
16. **Ley de Faraday - Solenoide variable:**  
    Un solenoide largo con radio $R$ tiene un campo magnético $\mathbf{B}(t) = B_0 \cos(\omega t) \hat{z}$. Calcule $\oint_C \mathbf{E} \cdot d\mathbf{l}$ para un anillo de radio $r > R$ usando la Ley de Faraday:  
   $$
    \oint_C \mathbf{E} \cdot d\mathbf{l} = -\frac{d}{dt} \int_S \mathbf{B} \cdot d\mathbf{S}
   $$  
    *Dificultad: Media | Aplicación: Inducción electromagnética*  

17. **Ecuación de continuidad:**  
    Partiendo de la Ley de Ampère-Maxwell $\nabla \times \mathbf{B} = \mu_0 \mathbf{J} + \mu_0 \epsilon_0 \frac{\partial \mathbf{E}}{\partial t}$, use el Teorema de la Divergencia para demostrar la ecuación de continuidad: $\nabla \cdot \mathbf{J} + \frac{\partial \rho}{\partial t} = 0$ .  
    *Dificultad: Alta | Aplicación: Conservación de carga*  

18. **Teorema de Poynting en onda plana:**  
    Para una onda plana en el vacío con $\mathbf{E} = E_0 \cos(kz - \omega t) \hat{x}$ y $\mathbf{B} = \frac{E_0}{c} \cos(kz - \omega t) \hat{y}$, calcule el vector de Poynting $\mathbf{S} = \frac{1}{\mu_0} \mathbf{E} \times \mathbf{B}$. Demuestre que $\oint_{\partial V} \mathbf{S} \cdot d\mathbf{S} = -\frac{dU}{dt}$ en un volumen cúbico.  
    *Dificultad: Alta | Aplicación: Radiación electromagnética*  

19. **Impedancia de onda:**  
    En una guía de ondas, la potencia media se calcula como $P = \frac{1}{2} \int_S \text{Re}(\mathbf{E} \times \mathbf{H}^*) \cdot d\mathbf{S}$Relacione esta integral con la densidad de energía media usando el Teorema de Poynting complejo.  
    *Dificultad: Alta | Aplicación: Guías de onda*  

20. **Pérdidas por calor en conductor óhmico:**  
    En un material con conductividad $igma$, demuestre que la potencia disipada es $P = \int_V \mathbf{J} \cdot \mathbf{E}  dV$. Use el Teorema de Poynting para escribir esto como $\oint_S (\mathbf{E} \times \mathbf{H}) \cdot d\mathbf{S} + \frac{d}{dt} \int_V u  dV$, donde $u$ es la densidad de energía .  
    *Dificultad: Alta | Aplicación: Disipación de energía*  

---

### **Tabla Resumen de Ejercicios**
| Ejercicio | Dificultad | Teorema/Identidad Principal         | Aplicación                     |
|-----------|------------|-------------------------------------|--------------------------------|
| 1         | Baja       | Teorema de la Divergencia           | Ley de Gauss                   |
| 2         | Baja       | Teorema de Stokes                   | Campos conservativos           |
| 3         | Baja       | Teorema de la Divergencia           | Monopolos magnéticos           |
| 4         | Media      | Teorema de la Divergencia           | Ley de Gauss                   |
| 5         | Media      | Teorema de Stokes                   | Potencial eléctrico            |
| 6         | Media      | Ley de Gauss                        | Capacitancia                   |
| 7         | Alta       | Identidad energética                | Energía electrostática         |
| 8         | Alta       | Tensor de Maxwell                   | Fuerzas electromagnéticas      |
| 9         | Media      | Conservación de energía             | Inductancia                    |
| 10        | Media      | Teorema de Stokes                   | Ley de Ampère                  |
| 11        | Media      | Teorema de la Divergencia           | Conservación de energía        |
| 12        | Baja       | Teorema de Stokes                   | Potencial vectorial            |
| 13        | Alta       | Teorema de Stokes                   | Ley de Ampère                  |
| 14        | Media      | Ley de Gauss                        | Campos en cavidades            |
| 15        | Baja       | Integral de volumen                 | Multipolos                     |
| 16        | Media      | Ley de Faraday                      | Inducción                      |
| 17        | Alta       | Teorema de la Divergencia           | Conservación de carga          |
| 18        | Alta       | Teorema de Poynting                 | Radiación                      |
| 19        | Alta       | Teorema de Poynting complejo        | Guías de onda                  |
| 20        | Alta       | Teorema de Poynting                 | Disipación                     |

---

### **Clave Pedagógica**
- **Teorema de la Divergencia (Gauss):**  
  Relaciona integrales de volumen con flujo superficial:  
 $$  \int_V \nabla \cdot \mathbf{F}  dV = \oint_S \mathbf{F} \cdot d\mathbf{S}
 $$ 
  Usado en Ley de Gauss, conservación de carga, y energía .  

- **Teorema de Stokes:**  
  Relaciona circulación con flujo del rotacional:  
 $$
  \oint_C \mathbf{F} \cdot d\mathbf{l} = \int_S (\nabla \times \mathbf{F}) \cdot d\mathbf{S}
 $$  
  Fundamental para Ley de Faraday y Ampère .  

- **Teorema de Poynting:**  
  Describe conservación de energía electromagnética:  
 $$
  \oint_S \mathbf{S} \cdot d\mathbf{S} = -\frac{dU}{dt} - P_{\text{dis}}
 $$  
  Aplicado en radiación, disipación y guías de onda .  

Estos ejercicios integran identidades de superficie-volumen con leyes físicas, consolidando la comprensión matemática y física del electromagnetismo. Para más detalles, consulte las fuentes citadas.