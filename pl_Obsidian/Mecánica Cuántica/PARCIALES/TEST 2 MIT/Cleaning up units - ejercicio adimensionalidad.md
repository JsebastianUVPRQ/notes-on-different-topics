Claro, aquí está la solución al problema con una explicación detallada del procedimiento.

Para adimensionar la ecuación radial de Schrödinger, introducimos una coordenada sin unidades, u, y una energía sin unidades, $\xi$. 
El objetivo es reescribir la ecuación original eliminando las constantes físicas ($ℏ,m,e^2$) y dejando solo variables y operadores adimensionales.

---

### (a) ¿Cómo se relacionan $r$ y $u$?

La relación se establece utilizando la escala de longitud natural del problema, que es el **radio de Bohr ($a_0$​)**. Definimos la coordenada adimensional $u$ como la razón entre el radio r y el radio de Bohr.

La relación es:

$$u=\dfrac{a_0}{​r}​$$de forma equivalente,
$$r=a_0​u$$

Para poder sustituir en la ecuación, también necesitamos transformar el operador de la segunda derivada. Usando la regla de la cadena.

Aplicando esto dos veces, obtenemos la segunda derivada:

$$\dfrac{d^2}{dr^2}​=\dfrac{1}{a_{0​}^2}\dfrac{​d^2}{du^2}​$$

---

### (b) ¿Cómo se relacionan E y E?

La energía adimensional E se relaciona con la energía física E a través de la escala de energía característica del átomo de hidrógeno, que es la energía de Rydberg, $$E_R​=\dfrac{2~
a_0}{​e^2}​$$.

La relación es:

$$\xi =E\Bigg( \dfrac{2a_0}{e^2}\Bigg)$$

Esta relación se deriva del procedimiento que se muestra a continuación en la parte (c).

---

### (c) Complete la ecuación anterior

Para encontrar la forma final de la ecuación y las relaciones anteriores, seguimos estos pasos:

1. Sustituir $r$ y $\dfrac{d^2}{dr^2}$ en la ecuación original.
    
    La ecuación original es:
    
    $$\left(-\frac{\hbar^2}{2m} \frac{d^2}{dr^2} + \frac{\hbar^2\ell(\ell+1)}{2mr^2} - \frac{e^2}{r}\right)\psi(r) = E\psi(r)
    
    $$
    
    Sustituyendo r=a0​u y dr2d2​=a02​1​du2d2​:
    
    $$
    
    \left(-\frac{\hbar^2}{2m} \frac{1}{a_0^2}\frac{d^2}{du^2} + \frac{\hbar^2\ell(\ell+1)}{2m(a_0u)^2} - \frac{e^2}{a_0u}\right)\psi(u) = E\psi(u)
    
    $$
    
2. Factorizar para aislar d2/du2.
    
    El objetivo es tener un término ($\dfrac{−d^2}{du^2}$+  $\dots$  ). Para lograr esto, multiplicamos toda la ecuación por el factor $\dfrac{2m~a_0^2}{ℏ^2}$​​:
    
    $$
3. \frac{2ma_0^2}{\hbar^2} \left[-\frac{\hbar^2}{2ma_0^2}\frac{d^2}{du^2} + \frac{\hbar^2\ell(\ell+1)}{2ma_0^2u^2} - \frac{e^2}{a_0u}\right]\psi(u) = \frac{2ma_0^2}{\hbar^2} E\psi(u)
    
    $$
    
    Distribuyendo el factor dentro del paréntesis:
    
    $$
    
    \left(-\frac{d^2}{du^2} + \frac{\ell(\ell+1)}{u^2} - \frac{2ma_0^2e^2}{\hbar^2a_0u}\right)\psi(u) = E\left(\frac{2ma_0^2}{\hbar^2}\right)\psi(u)
    
    $$
    
4. Simplificar usando la definición de a0​.
    
    Recordemos que a0​=me2ℏ2​. Podemos reorganizar esto como ℏ2=a0​me2. Sustituyamos esta expresión en el último término dentro del paréntesis:
    
    $$
    
    \frac{2ma_0e^2}{\hbar^2u} = \frac{2ma_0e^2}{(a_0me^2)u} = \frac{2}{u}
    
    $$
    
    Esta simplificación es la clave del proceso.
    
5. Escribir la ecuación final y comparar.
    
    Sustituyendo el término simplificado, obtenemos la ecuación adimensional completa:
    
    $$
    
    \left(-\frac{d^2}{du^2} + \frac{\ell(\ell+1)}{u^2} - \frac{2}{u}\right)\psi(u) = E\left(\frac{2ma_0^2}{\hbar^2}\right)\psi(u)
    
    $$
    
    Al comparar esta ecuación con la forma objetivo $\Bigg(\dfrac{−du^2}{du^2}​+…\Bigg)\psi(u)=E ψ(u)$, podemos identificar los términos faltantes.
    

La ecuación completa es:

$$
\left(-\frac{d^2}{du^2} + \frac{\ell(\ell+1)}{2mr^2} - \frac{2}{r}\right)\psi_{(u)} =
\xi~\psi_{(u)}$$
De esta comparación, también confirmamos la relación para la energía de la parte $(b)$:
$$
\xi = E\Bigg(\dfrac{2m~a_0^2}{\hbar^2}\Bigg)
$$