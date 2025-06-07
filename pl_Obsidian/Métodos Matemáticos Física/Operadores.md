  
# Linear and Hermitian Properties of the Operator $\hat{D}$

## (a) Linearity of $\hat{D}$

To show that $\hat{D} = \frac{d^2}{dx^2} + \omega^2$ is linear, we verify additivity and homogeneity for any $|u\rangle, |v\rangle \in L^2(\mathbb{R})$ and $\alpha \in \mathbb{R}$:

### Additivity
$$
\hat{D}(|u\rangle + |v\rangle) = \left(\frac{d^2}{dx^2} + \omega^2\right)(u + v) = \frac{d^2u}{dx^2} + \frac{d^2v}{dx^2} + \omega^2u + \omega^2v = \hat{D}|u\rangle + \hat{D}|v\rangle
$$
### Homogeneity
$$
\hat{D}(\alpha|u\rangle) = \left(\frac{d^2}{dx^2} + \omega^2\right)(\alpha u) = \alpha \frac{d^2u}{dx^2} + \alpha \omega^2u = \alpha \hat{D}|u\rangle
$$

**Conclusion:** $\hat{D}$ is linear.

---

## (b) Hermiticity of $\hat{D}$

An operator is Hermitian if   $\langle u | \hat{D} v \rangle = \langle \hat{D} u | v \rangle$    for all     $|u\rangle, |v\rangle \in L^2(\mathbb{R})$.

### Key Equality to Verify
$$
\int_{-\infty}^\infty u \left(\frac{d^2v}{dx^2} + \omega^2 v\right) dx = \int_{-\infty}^\infty \left(\frac{d^2u}{dx^2} + \omega^2 u\right) v \, dx
$$

### Simplification
The $\omega^2$ terms cancel out, reducing the problem to showing:
$$
\int_{-\infty}^\infty u \frac{d^2v}{dx^2} dx = \int_{-\infty}^\infty \frac{d^2u}{dx^2} v \, dx
$$

### Integration by Parts (Twice)
1. **First Integration:**
   $$
   \int u \frac{d^2v}{dx^2} dx = \left. u \frac{dv}{dx} \right|_{-\infty}^\infty - \int \frac{du}{dx} \frac{dv}{dx} dx
   $$
   - Boundary term vanishes because $u, \frac{dv}{dx} \to 0$ at $\pm \infty$ for $L^2$ functions.

2. **Second Integration:**
   $$
   -\int \frac{du}{dx} \frac{dv}{dx} dx = -\left. \frac{du}{dx} v \right|_{-\infty}^\infty + \int \frac{d^2u}{dx^2} v \, dx
   $$
   - Boundary term vanishes for the same reason.

### Final Result
$$
\int u \frac{d^2v}{dx^2} dx = \int \frac{d^2u}{dx^2} v \, dx
$$

**Conclusion:** $\hat{D}$ is Hermitian.

---

### Key Properties
- **Linearity:** Follows directly from the linearity of differentiation and scalar multiplication.
- **Hermiticity:** Relies on integration by parts and decay conditions of $L^2$ functions.

Cuando la superficie está definida de manera general (no necesariamente alineada con los ejes), el **vector diferencial de área** $d\vec{A}$ depende de cómo se parametrice la superficie. Para una superficie descrita por una función $f(\mathbf{r}) = 0$ o parametrizada en términos de dos variables, su expresión general se obtiene mediante el cálculo de vectores tangentes y su producto cruz.

---


