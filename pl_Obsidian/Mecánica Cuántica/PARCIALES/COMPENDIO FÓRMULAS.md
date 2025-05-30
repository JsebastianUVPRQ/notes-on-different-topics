### Texto y ecuaciones extraídos de las primeras 6 páginas:

---

#### **Página 1**  
Texto:  
- "8.04, Quantum Physics I, Fall 2015"  
- "FINAL EXAM"  
- "Friday December 18, 1:30-4:30 pm"  
- Instrucciones para el examen.  

---

#### **Página 2**  
**Fórmulas**:  
1. Constantes físicas:  
   \( \hbar c \simeq 197.3 \, \text{MeV} \cdot \text{fm}, \, m_e c^2 \simeq 0.511 \, \text{MeV}, \, m_p c^2 = 938 \, \text{MeV}, \, \frac{e^2}{\hbar c} \simeq \frac{1}{137} \).  

2. Relatividad:  
   \( p = \gamma mv, \, E = \gamma mc^2, \, E^2 = p^2 c^2 + m^2 c^4, \, \gamma = \frac{1}{\sqrt{1 - \beta^2}}, \, \beta = \frac{v}{c} \).  

3. Fotones:  
   \( E = h\nu, \, p = \frac{h}{\lambda}, \, \text{o} \, E = \hbar \omega, \, p = \hbar k \).  

4. Longitudes de onda:  
   \( \lambda = \frac{h}{p} \) (de Broglie), \( \lambda_C = \frac{h}{mc} \) (Compton).  

5. Operadores de momento y posición:  
   $$
   p = \frac{\hbar}{i} \frac{\partial}{\partial x}, \, [x, p] = i\hbar, \, p = \frac{\hbar}{i} \nabla, \, [x_i, p_j] = i\hbar \delta_{ij}, \, [p_i, f(x)] = \frac{\hbar}{i} \frac{\partial f}{\partial x_i}.
   $$  

6. Ecuación de Schrödinger:  
   $$
   i\hbar \frac{\partial \Psi}{\partial t}(x, t) = \left( -\frac{\hbar^2}{2m} \nabla^2 + V(x, t) \right) \Psi(x, t),
   $$  
   $$
   \frac{\partial}{\partial t} \rho(x, t) + \nabla \cdot J(x, t) = 0,
   $$  
   $$
   \rho(x, t) = |\Psi(x, t)|^2; \, J(x, t) = \frac{\hbar}{m} \text{Im} [\Psi^* \nabla \Psi].
   $$  

7. Transformadas de Fourier:  
   $$
   \Psi(x) = \frac{1}{\sqrt{2\pi}} \int dk \Phi(k) e^{ikx}, \, \Phi(k) = \frac{1}{\sqrt{2\pi}} \int dx \Psi(x) e^{-ikx}, \, \int dx |\Psi(x)|^2 = \int dk |\Phi(k)|^2,
   $$  
   $$
   \Psi(x) = \frac{1}{(2\pi)^{\frac{3}{2}}} \int d^3 k \Phi(k) e^{ikx}, \, \Phi(k) = \frac{1}{(2\pi)^{\frac{3}{2}}} \int d^3 x \Psi(x) e^{-ikx}, \, \int d^3 x |\Psi(x)|^2 = \int d^3 k |\Phi(k)|^2.
   $$  

8. Integrales útiles:  
   $$
   \frac{1}{2\pi} \int_{-\infty}^{\infty} e^{ikx} dx = \delta(k), \, \frac{1}{(2\pi)^3} \int_{-\infty}^{\infty} e^{ikx} d^3 x = \delta^{(3)}(k),
   $$  
   $$
   \int_{-\infty}^{+\infty} dx \exp\left(-ax^2 + bx\right) = \sqrt{\frac{\pi}{a}} \exp\left(\frac{b^2}{4a}\right), \, \text{cuando Re}(a) > 0.
   $$  

9. Paquetes de onda:  
   $$
   v_{group} = \frac{d\omega}{dk}, \, \Delta k \Delta x \simeq 1, \, \text{forma preservada:} \, t \Delta v \leq \Delta x.
   $$  

10. Conjugación hermítica:  
    $$
    \int dx (K \Psi(x, t))^* \Psi(x, t) = \int dx \Psi^*(x, t) (K^\dagger \Psi(x, t)).
    $$  

---

#### **Página 3**  
**Fórmulas**:  
1. Valores esperados:  
   $$
   \langle Q\rangle(t)~{}=~{}\int dx\,\Psi^{*}(x,t)(Q\Psi(x,t)).
   $$  

2. Evolución temporal del valor esperado:  
   $$
   i\hbar\frac{d}{dt}\langle Q\rangle~{}=~{}\big{\langle}[Q,H]\big{\rangle}.
   $$  

3. Identidad de conmutadores:  
   $$
   [A,BC]=[A,B]C+B[A,C].
   $$  

4. Incertidumbre:  
   $$
   (\Delta Q)^{2}~{}=~{}\langle Q^{2}\rangle-\langle Q\rangle^{2}~{}=~{}\big{\langle}(Q-\langle Q\rangle)^{2}\big{\rangle}.
   $$  

5. Principio de incertidumbre:  
   $$
   \Delta x\,\Delta p\geq\frac{\hbar}{2}, \, \Delta x=\frac{\Delta}{\sqrt{2}}, \, \Delta p=\frac{\hbar}{\sqrt{2\Delta}} \, \text{para} \, \psi\sim\exp\Bigl{(}-\frac{1}{2}\frac{x^{2}}{\Delta^{2}}\Bigr{)}.
   $$  

6. Estados estacionarios:  
   $$
   \Psi(x,t)=\psi(x)e^{-iEt/\hbar}, \, -\frac{\hbar^{2}}{2m}\frac{d^{2}}{dx^{2}} \psi(x)+V(x)\psi(x)=E\,\psi(x).
   $$  

7. Pozo cuadrado infinito:  
   $$
   V(x)=\left\{\begin{array}{ll}0\,,&~{}\text{para}~{}0<x<a,\\ \infty&~\text{otro caso}\end{array}\right., \, \psi_{n}(x)=\sqrt{\frac{2}{a}}\sin\frac{n\pi x}{a}, \, E_{n}=\frac{\hbar^{2}\pi^{2}n^{2}}{2ma^{2}}.
   $$  

8. Pozo cuadrado finito:  
   $$
   V(x)=\left\{\begin{array}{ll}-V_{0}\,,&~{}\text{para}~|x|<a, \\ 0&~\text{para}~|x|>a\end{array}\right., \, \eta^{2}~{}\equiv~{}\frac{2m(E+V_{0})a^{2}}{\hbar^{2}}, \, \xi^{2}~{}\equiv~{}\frac{2m|E|a^{2}}{\hbar^{2}}, \, z_{0}^{2}~{}\equiv~{}\frac{2mV_{0}a^{2}}{\hbar^{2}}.
   $$  

9. Potencial delta:  
   $$
   V=-\alpha\,\delta(x), \, \text{estado ligado:} \, E=-\frac{m\alpha^{2}}{2\hbar^{2}}.
   $$  

---

#### **Página 4**  
**Fórmulas**:  
1. Oscilador armónico:  
   $$
   \hat{H}=\frac{1}{2m}\hat{p}^{2}+\frac{1}{2}m\omega^{2}\hat{x}^{2}=\hbar\omega\left(\hat{N}+\frac{1}{2}\right), \, \hat{N}=\hat{a}^{\dagger}\hat{a},
   $$  
   $$
   \hat{a}=\sqrt{\frac{m\omega}{2\hbar}}\left(\hat{x}+\frac{i\hat{p}}{m\omega}\right), \, \hat{a}^{\dagger}=\sqrt{\frac{m\omega}{2\hbar}}\left(\hat{x}-\frac{i\hat{p}}{m\omega}\right),
   $$  
   $$
   \hat{x}=\sqrt{\frac{\hbar}{2m\omega}}(\hat{a}+\hat{a}^{\dagger}), \, \hat{p}=i\sqrt{\frac{m\omega\hbar}{2}}(\hat{a}^{\dagger}-\hat{a}),
   $$  
   $$
   [\hat{x},\hat{p}]=i\hbar, \, [\hat{a},\hat{a}^{\dagger}]=1, \, [\hat{N},\hat{a}]=-\hat{a}, \, [\hat{N},\hat{a}^{\dagger}]=\hat{a}^{\dagger}.
   $$  

2. Estados del oscilador armónico:  
   $$
   \hat{a}\phi_{0}\;=\;0, \, \phi_{0}(x)=\left(\frac{m\omega}{\pi\hbar}\right)^{1/4}\exp\left(-\frac{m\omega}{2\hbar}x^{2}\right),
   $$  
   $$
   \phi_{n}=\frac{1}{\sqrt{n!}}(a^{\dagger})^{n}\phi_{0}, \, \hat{H}\,\phi_{n}=E_{n}\,\phi_{n}=\hbar\omega\big{(}n+\tfrac{1}{2}\big{)}\,\phi_{n}.
   $$  

3. Estados de energía positiva:  
   $$
   \psi(x)\;=\;Ae^{ikx}+Be^{-ikx}, \, J\;=\;\frac{\hbar k}{m}\big{(}|A|^{2}-|B|^{2}\big{)}, \, E=\frac{\hbar^{2}k^{2}}{2m}.
   $$  

4. Dispersión en 1D:  
   $$
   \psi(x)\;=\;e^{i\delta}\,\sin(kx+\delta), \, \psi_{s}=A_{s}e^{ikx}, \, A_{s}=e^{i\delta}\sin\delta,
   $$  
   $$
   \Delta t\;=\;2\hbar\,\frac{d\delta}{dE}, \, N_{bound}\;=\;\frac{1}{\pi}\big{(}\,\delta(0)-\delta(\infty)\big{)}.
   $$  

---

#### **Página 5**  
**Fórmulas**:  
1. Momento angular orbital:  
   $$
   \hat{L}_x = \hat{y} \hat{p}_z - \hat{z} \hat{p}_y, \, \hat{L}_y = \hat{z} \hat{p}_x - \hat{x} \hat{p}_z, \, \hat{L}_z = \hat{x} \hat{p}_y - \hat{y} \hat{p}_x,
   $$  
   $$
   [\hat{L}_x, \hat{L}_y] = i \hbar \hat{L}_z, \, [\hat{L}_y, \hat{L}_z] = i \hbar \hat{L}_x, \, [\hat{L}_z, \hat{L}_x] = i \hbar \hat{L}_y,
   $$  
   $$
   \hat{L}^2 = -\hbar^2 \left( \frac{\partial^2}{\partial \theta^2} + \cot \theta \frac{\partial}{\partial \theta} + \frac{1}{\sin^2 \theta} \frac{\partial^2}{\partial \phi^2} \right).
   $$  

2. Armónicos esféricos:  
   $$
   Y_{\ell,m}(\theta, \phi) \equiv N_{\ell,m} P_m^n (\cos \theta) e^{im \phi},
   $$  
   $$
   \hat{L}_z Y_{\ell m} = \hbar m Y_{\ell m}, \, \hat{L}^2 Y_{\ell m} = \hbar^2 \ell (\ell + 1) Y_{\ell m}.
   $$  

3. Normalización:  
   $$
   \int d \Omega \, Y_{\ell m}^* (\theta, \phi) \, Y_{\ell m} (\theta, \phi) = \delta_{\ell', \ell} \delta_{m', m}.
   $$  

---

#### **Página 6**  
**Fórmulas**:  
1. Átomo de hidrógeno:  
   $$
   H = \frac{p^2}{2m} - \frac{Ze^2}{r}, \, E_n = -\frac{Z^2 e^2}{2a_0} \frac{1}{n^2}, \, a_0 = \frac{\hbar^2}{me^2} \approx 0.529 \times 10^{-10} \, \text{m},
   $$  
   $$
   \psi_{n,\ell,m}(\vec{x}) = \frac{u_{n\ell}(r)}{r} Y_{\ell,m}(\theta, \phi).
   $$  

2. Funciones radiales:  
   $$
   u_{1,0}(r) = \frac{2r}{a_0^{3/2}} \exp(-r/a_0), \, u_{2,0}(r) = \frac{2r}{(2a_0)^{3/2}} \left( 1 - \frac{r}{2a_0} \right) \exp(-r/2a_0).
   $$  

---

**Texto de preguntas (Página 6)**:  
1. **Teorema del Virial para potenciales unidimensionales**:  
   (a) Explicar por qué    $\langle [H, \Omega] \rangle = 0$      en un autoestado de energía.  
   (b) Usar     $\Omega = xp$  p   ara relacionar     $\langle T \rangle$ y $\langle x V'(x) \rangle$.  
   (c) Aplicar al oscilador armónico unidimensional.  

--- 

**Nota**: Las ecuaciones se han extraído respetando el formato LaTeX original.