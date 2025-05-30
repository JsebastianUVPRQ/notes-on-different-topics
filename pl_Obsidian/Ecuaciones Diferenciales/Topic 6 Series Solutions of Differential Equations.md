
Differential equations are fundamental in physics, as they describe the behavior of physical systems. Many physical phenomena, such as oscillations, wave propagation, and quantum mechanics, are modeled using differential equations. However, not all differential equations can be solved using elementary functions. In such cases, **series solutions** provide a powerful tool to approximate solutions. This explanation focuses on two key methods: **power series solutions near ordinary points** and the **Frobenius method for regular singular points**.

---

### 1. Power Series Solutions Near Ordinary Points

#### What is an Ordinary Point?
Consider a second-order linear differential equation of the form:
$$
P(x) y''(x) + Q(x) y'(x) + R(x) y(x) = 0,
$$
where $P(x)$, $Q(x)$, and $R(x)$ are polynomials. A point $x = x_0$ is called an **ordinary point** if:
$$
P(x_0) \neq 0.
$$
At an ordinary point, the coefficients of the differential equation are well-behaved, and the solution can be expressed as a **power series**.

#### Power Series Solution
Near an ordinary point $x_0$, the solution $y(x)$ can be written as a Taylor series:
$$
y(x) = \sum_{n=0}^\infty a_n (x - x_0)^n,
$$
where $a_n$ are coefficients to be determined. Substituting this series into the differential equation and equating coefficients of like powers of $(x - x_0)$ yields a **recurrence relation** for the coefficients $a_n$.

#### Steps to Find the Solution:
1. Assume a power series solution $y(x) = \sum_{n=0}^\infty a_n (x - x_0)^n$.
2. Compute $y'(x)$ and $y''(x)$ by differentiating the series term by term.
3. Substitute $y(x)$, $y'(x)$, and $y''(x)$ into the differential equation.
4. Collect terms with the same power of $(x - x_0)$ and set the coefficients to zero.
5. Solve the resulting recurrence relation to find the coefficients $a_n$.

#### Example: Simple Harmonic Oscillator
The differential equation for a simple harmonic oscillator is:
$$
y''(x) + \omega^2 y(x) = 0.
$$
Assuming a power series solution $y(x) = \sum_{n=0}^\infty a_n x^n$, we substitute into the equation and find the recurrence relation:
$$
a_{n+2} = -\frac{\omega^2}{(n+2)(n+1)} a_n.
$$
This yields the familiar solutions $y(x) = A \cos(\omega x) + B \sin(\omega x)$.

---

### 2. Frobenius Method for Regular Singular Points

#### What is a Regular Singular Point?
A point $x = x_0$ is called a **regular singular point** if:
1. $P(x_0) = 0$, but
2. $(x - x_0) \frac{Q(x)}{P(x)}$ and $(x - x_0)^2 \frac{R(x)}{P(x)}$ are analytic (i.e., have convergent power series expansions) at $x = x_0$.

At a regular singular point, the power series method fails, but the **Frobenius method** can be used to find solutions.

#### Frobenius Method
The Frobenius method assumes a solution of the form:
$$
y(x) = (x - x_0)^r \sum_{n=0}^\infty a_n (x - x_0)^n,
$$
where $r$ is a constant called the **indicial exponent**. The goal is to determine $r$ and the coefficients $a_n$.

#### Steps to Find the Solution:
1. Assume a Frobenius series solution $y(x) = (x - x_0)^r \sum_{n=0}^\infty a_n (x - x_0)^n$.
2. Compute $y'(x)$ and $y''(x)$ by differentiating the series term by term.
3. Substitute $y(x)$, $y'(x)$, and $y''(x)$ into the differential equation.
4. Equate the coefficient of the lowest power of $(x - x_0)$ to zero to obtain the **indicial equation**, which determines $r$.
5. Solve the indicial equation for $r$. If the roots differ by an integer, additional care is needed to find a second linearly independent solution.
6. Use the recurrence relation to find the coefficients $a_n$.

#### Example: Bessel's Equation
Bessel's equation arises in problems with cylindrical symmetry, such as heat conduction in a cylinder:
$$
x^2 y''(x) + x y'(x) + (x^2 - \nu^2) y(x) = 0.
$$
Here, $x = 0$ is a regular singular point. Using the Frobenius method, we assume:
$$
y(x) = x^r \sum_{n=0}^\infty a_n x^n.
$$
Substituting into Bessel's equation yields the indicial equation:
$$
r^2 - \nu^2 = 0,
$$
with roots $r = \pm \nu$. The recurrence relation for the coefficients $a_n$ leads to the Bessel functions $J_\nu(x)$ and $J_{-\nu}(x)$.

---

### Applications in Physics
1. **Quantum Mechanics**: The Schrödinger equation for potentials like the harmonic oscillator or the hydrogen atom often requires series solutions.
2. **Electrodynamics**: Solutions to Maxwell's equations in cylindrical or spherical coordinates involve Bessel and Legendre functions, which are derived using the Frobenius method.
3. **Fluid Dynamics**: The Navier-Stokes equations in certain geometries lead to differential equations with singular points, solvable using the Frobenius method.

---

### Summary
- **Power series solutions** are used near ordinary points, where the solution is analytic and can be expressed as a Taylor series.
- The **Frobenius method** extends this approach to regular singular points, where the solution may involve a fractional power $(x - x_0)^r$.
- Both methods are essential for solving differential equations that arise in physics, particularly in problems with symmetry or singular behavior.