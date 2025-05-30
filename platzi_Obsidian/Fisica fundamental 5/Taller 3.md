![[Pasted image 20250224233959.png]]

### Translation:

**Problem 10 — Cross-section for rigid spheres**

Consider the scattering process of rigid spheres with radius $r_A $by scattering centers consisting of rigid spheres with radius $r_B $. Find the differential cross-section and the total cross-section in this process.

---

**Problem 11 — Rutherford Model**

Derive the Rutherford formula for the scattering of positive ions by atoms according to the Rutherford model.
### Solutions:
---
#### **Problem 10 — Cross-section for rigid spheres**

**Setup:**
- Consider two rigid spheres, one with radius $r_A $(the projectile) and another with radius $r_B$(the target).
- The scattering occurs when the distance between their centers is less than or equal to$r_A + r_B $, which defines the effective "collision radius."

**Differential Cross-section:**
The differential cross-section$\frac{d\sigma}{d\Omega}$describes how the scattering depends on the solid angle $d\Omega $. For rigid spheres, the scattering is isotropic because all impact parameters $b $(the perpendicular distance between the initial trajectory of the projectile and the center of the target) are equally likely. Therefore:
$$
\frac{d\sigma}{d\Omega} = \text{constant}.
$$

To determine the constant, we integrate over all solid angles to find the total cross-section.

**Total Cross-section:**
The total cross-section $\sigma $is the effective area that the target presents to the incoming projectile. For rigid spheres, this is simply the geometric cross-sectional area of the combined sphere:
$$
\sigma = \pi (r_A + r_B)^2.
$$

Thus:
$$
\boxed{\sigma = \pi (r_A + r_B)^2}.
$$

---

#### **Problem 11 — Rutherford Model**

**Setup:**
In the Rutherford model, a positively charged α particle scatters off a positively charged nucleus due to Coulomb repulsion. The force between the α particle and the nucleus is given by Coulomb's law:
$$
F = \frac{k q_1 q_2}{r^2},
$$
where $k = \frac{1}{4\pi \epsilon_0}$ , $q_1$ and $q_2$ are the charges of the α particle and the nucleus, respectively, and $r$ is the distance between them.

The scattering angle $\theta$ depends on the impact parameter $b$ , which is related to the angular momentum of the system. Using classical mechanics, the relationship between $b$ and $\theta$ can be derived.

**Derivation:**
1. The trajectory of the α particle is hyperbolic due to the repulsive Coulomb force.
2. The scattering angle $\theta$ is related to the impact parameter $b$ by:
   $$
   \cot\left(\frac{\theta}{2}\right) = \frac{2 b E}{k q_1 q_2},
   $$
   where $E $is the kinetic energy of the α particle.

3. The differential cross-section $\frac{d\sigma}{d\Omega}$ is proportional to the probability of scattering into a given solid angle $d\Omega$. Using the relationship between $b$ and $\theta$, we find:
   $$
   \frac{d\sigma}{d\Omega} = \left(\frac{k q_1 q_2}{4 E \sin^2(\theta/2)}\right)^2.
   $$

Thus, the Rutherford formula for the differential cross-section is:
$$
\boxed{\frac{d\sigma}{d\Omega} = \left(\frac{k q_1 q_2}{4 E \sin^2(\theta/2)}\right)^2}.
$$

---

#### **Problem 12 — Size of the atomic nucleus**

**Setup:**
- A beam of α particles with kinetic energy $E = 12.75 \, \text{MeV}$ is scattered by an aluminum nucleus ($Z = 13$).
- At large angles ($\theta = 54^\circ$), deviations from pure Coulomb scattering indicate the presence of the nuclear force, which becomes significant when the α particle approaches the nucleus closely.

**Key Idea:**
The deviation occurs when the distance of closest approach $r_{\text{min}} $between the α particle and the nucleus is comparable to the sum of their radii:
$$
r_{\text{min}} \approx R_\alpha + R_{\text{nucleus}},
$$
where $R_\alpha = 2 \times 10^{-15} \, \text{m}$.

**Step 1: Calculate $r_{\text{min}}$:**
The distance of closest approach for pure Coulomb scattering is given by:
$$
r_{\text{min}} = \frac{k q_1 q_2}{E},
$$
where:
- $k = \frac{1}{4\pi \epsilon_0} = 8.99 \times 10^9 \, \text{N·m}^2/\text{C}^2$,
- $q_1 = 2e$(charge of α particle),
- $q_2 = 13e$(charge of aluminum nucleus),
- $e = 1.6 \times 10^{-19} \, \text{C}$,
- $E = 12.75 \, \text{MeV} = 12.75 \times 10^6 \times 1.6 \times 10^{-19} \, \text{J} = 2.04 \times 10^{-12} \, \text{J}$.

Substitute these values:
$$
r_{\text{min}} = \frac{(8.99 \times 10^9) (2 \cdot 1.6 \times 10^{-19}) (13 \cdot 1.6 \times 10^{-19})}{2.04 \times 10^{-12}}.
$$

Simplify:
$$
r_{\text{min}} = \frac{(8.99 \times 10^9) (2 \cdot 13 \cdot (1.6 \times 10^{-19})^2)}{2.04 \times 10^{-12}}.
$$

$$
r_{\text{min}} = \frac{(8.99 \times 10^9) (2 \cdot 13 \cdot 2.56 \times 10^{-38})}{2.04 \times 10^{-12}}.
$$

$$
r_{\text{min}} = \frac{(8.99 \times 10^9) (66.56 \times 10^{-38})}{2.04 \times 10^{-12}}.
$$

$$
r_{\text{min}} = \frac{5.98 \times 10^{-26}}{2.04 \times 10^{-12}}.
$$

$$
r_{\text{min}} \approx 2.93 \times 10^{-14} \, \text{m}.
$$

**Step 2: Solve for $R_{\text{nucleus}}$:**
Using $r_{\text{min}} \approx R_\alpha + R_{\text{nucleus}}$, we have:
$$
R_{\text{nucleus}} = r_{\text{min}} - R_\alpha.
$$

Substitute $r_{\text{min}} = 2.93 \times 10^{-14} \, \text{m}$and $R_\alpha = 2 \times 10^{-15} \, \text{m}$:
$$
R_{\text{nucleus}} = 2.93 \times 10^{-14} - 2 \times 10^{-15}.
$$

$$
R_{\text{nucleus}} \approx 2.73 \times 10^{-14} \, \text{m}.
$$

Thus, the radius of the aluminum nucleus is:
$$
\boxed{R_{\text{nucleus}} \approx 2.73 \times 10^{-14} \, \text{m}}.
$$

### Solución al Problema 13

#### Parte (a): Energía media por modo a temperatura  $T$

La energía media por modo se define como:

 $$
\bar{\omega}_{\nu} = \sum_{n=0}^{\infty} n h \nu p(n h \nu),
 $$

donde  $p(n h \nu)$ es la probabilidad de que un modo contenga $n$ fotones, dada por:

 $$
p(n h \nu) = \frac{e^{-n h \nu / k_B T}}{\sum_{j=0}^{\infty} e^{-j h \nu / k_B T}}.
 $$

Primero, calculamos el denominador de  $p(n h \nu)$, que es la función de partición  $Z$:

 $$
Z = \sum_{j=0}^{\infty} e^{-j h \nu / k_B T}.
 $$

Esta es una serie geométrica con razón  $e^{-h \nu / k_B T}$, por lo que:

 $$
Z = \frac{1}{1 - e^{-h \nu / k_B T}}.
 $$

Ahora, la probabilidad  $p(n h \nu)$ se puede escribir como:

 $$
p(n h \nu) = \frac{e^{-n h \nu / k_B T}}{Z} = \left(1 - e^{-h \nu / k_B T}\right) e^{-n h \nu / k_B T}.
 $$

Sustituyendo  $p(n h \nu)$ en la expresión para  $\bar{\omega}_{\nu}$:

 $$
\bar{\omega}_{\nu} = \sum_{n=0}^{\infty} n h \nu \left(1 - e^{-h \nu / k_B T}\right) e^{-n h \nu / k_B T}.
 $$

Factorizando  $h \nu \left(1 - e^{-h \nu / k_B T}\right)$:

 $$
\bar{\omega}_{\nu} = h \nu \left(1 - e^{-h \nu / k_B T}\right) \sum_{n=0}^{\infty} n e^{-n h \nu / k_B T}.
 $$

La suma  $\sum_{n=0}^{\infty} n x^n$ (donde  $x = e^{-h \nu / k_B T}$) es conocida y su valor es  $\frac{x}{(1 - x)^2}$. Por lo tanto:

 $$
\sum_{n=0}^{\infty} n e^{-n h \nu / k_B T} = \frac{e^{-h \nu / k_B T}}{\left(1 - e^{-h \nu / k_B T}\right)^2}.
 $$

Sustituyendo esta suma en la expresión para  $\bar{\omega}_{\nu}$:

 $$
\bar{\omega}_{\nu} = h \nu \left(1 - e^{-h \nu / k_B T}\right) \frac{e^{-h \nu / k_B T}}{\left(1 - e^{-h \nu / k_B T}\right)^2} = \frac{h \nu e^{-h \nu / k_B T}}{1 - e^{-h \nu / k_B T}}.
 $$

Simplificando:

 $$
\bar{\omega}_{\nu} = \frac{h \nu}{e^{h \nu / k_B T} - 1}.
 $$

#### Parte (b): Densidad de potencia de radiación espectral

La densidad de potencia de radiación espectral  $S_{\nu}^{*}$ se relaciona con la energía media por modo  $\bar{\omega}_{\nu}$ y el número de modos por unidad de volumen y frecuencia. La densidad de modos en una cavidad es:

 $$
\frac{8 \pi \nu^2}{c^3}.
 $$

Por lo tanto, la densidad de potencia espectral es:

 $$
S_{\nu}^{*} = \frac{8 \pi \nu^2}{c^3} \bar{\omega}_{\nu}.
 $$

Sustituyendo  $\bar{\omega}_{\nu}$:

 $$
S_{\nu}^{*} = \frac{8 \pi \nu^2}{c^3} \frac{h \nu}{e^{h \nu / k_B T} - 1} = \frac{2 h \nu^3}{c^2} \frac{1}{e^{h \nu / k_B T} - 1}.
 $$

#### Límite clásico  $h \nu \ll k_B T$

En el límite  $h \nu \ll k_B T$, podemos aproximar  $e^{h \nu / k_B T} \approx 1 + \frac{h \nu}{k_B T}$. Sustituyendo en  $S_{\nu}^{*}$:

 $$
S_{\nu}^{*} \approx \frac{2 h \nu^3}{c^2} \frac{1}{1 + \frac{h \nu}{k_B T} - 1} = \frac{2 h \nu^3}{c^2} \frac{k_B T}{h \nu} = \frac{2 \nu^2 k_B T}{c^2}.
 $$

Este es el resultado clásico de Rayleigh-Jeans.

### Solución al Problema 14

#### Parte (a): Ecuaciones clásicas de movimiento y soluciones

El hamiltoniano del oscilador armónico unidimensional es:

 $$
H = \frac{p^2}{2m} + \frac{m}{2} \omega^2 q^2.
 $$

Las ecuaciones de Hamilton son:

 $\dot{q} = \frac{\partial H}{\partial p} = \frac{p}{m}$
 $$
\dot{p} = -\frac{\partial H}{\partial q} = -m \omega^2 q.
 $$

De la primera ecuación,  $p = m \dot{q}$. Sustituyendo en la segunda ecuación:

 $$
m \ddot{q} = -m \omega^2 q \implies \ddot{q} + \omega^2 q = 0.
 $$

Esta es la ecuación diferencial del oscilador armónico, cuya solución general es:

 $$
q(t) = A \cos(\omega t) + B \sin(\omega t),
 $$

donde  $A$ y  $B$ son constantes determinadas por las condiciones iniciales.

El momento  $p(t)$ se obtiene derivando  $q(t)$:

 $$
p(t) = m \dot{q}(t) = -m \omega A \sin(\omega t) + m \omega B \cos(\omega t).
 $$

Estas son las soluciones clásicas del oscilador armónico.