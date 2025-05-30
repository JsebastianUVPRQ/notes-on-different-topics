#### **What Are First-Order Differential Equations?**
A **first-order differential equation** involves a function and its first derivative. In physics, these equations are used to model systems where the rate of change of a quantity depends on the current state of the system. Mathematically, they take the general form:
$$
\frac{dy}{dx} = f(x, y),
$$
where $y$ is the dependent variable (e.g., position, temperature, or concentration), $x$ is the independent variable (e.g., time or spatial coordinate), and $f(x, y)$ is a function describing the relationship between the variables.

First-order differential equations are particularly useful in physics because many physical processes evolve based on instantaneous conditions. For example:
- The rate of change of velocity depends on forces acting on an object.
- The rate of decay of a radioactive substance depends on the amount of material present.
- The rate of heat transfer depends on the temperature difference.

---

#### **Key Concepts in First-Order Differential Equations**

1. **Types of First-Order Differential Equations:**
   - **Separable Equations**: These can be written as:
     $$
     \frac{dy}{dx} = g(x)h(y),
     $$
     where $g(x)$ depends only on $x$, and $h(y)$ depends only on $y$. Separation of variables is used to solve these equations.
   - **Linear Equations**: These have the form:
     $$
     \frac{dy}{dx} + P(x)y = Q(x),
     $$
     where $P(x)$ and $Q(x)$ are functions of $x$. The integrating factor method is used to solve them.
   - **Exact Equations**: These satisfy the condition:
     $$
     M(x, y)dx + N(x, y)dy = 0,
     $$
     where $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$. Exactness allows for direct integration.
   - **Substitution Methods**: Non-standard equations can sometimes be solved by substituting new variables (e.g., Bernoulli equations).

2. **Initial Conditions:**
   - Solutions to first-order differential equations often involve arbitrary constants. To determine a unique solution, initial conditions (e.g., $y(x_0) = y_0$) are specified.

3. **Physical Interpretation:**
   - The derivative $\frac{dy}{dx}$ represents the rate of change of $y$ with respect to $x$ . In physics, this could mean velocity $dx/dt$ , decay rate $dN/dt$ or heat flow ($dT/dt$)

---

#### **Examples of First-Order Differential Equations in Physics**

1. **Radioactive Decay:**
   - The number of radioactive atoms $N(t)$ decreases over time due to decay. The rate of decay is proportional to the number of atoms present:
     $$
     \frac{dN}{dt} = -\lambda N,
     $$
     where $\lambda$ is the decay constant. This is a separable equation. Solving it gives:
     $$
     N(t) = N_0 e^{-\lambda t},
     $$
     where $N_0$ is the initial number of atoms. This exponential decay law is fundamental in nuclear physics.

2. **Newton's Law of Cooling:**
   - The rate of change of temperature $T(t)$ of an object is proportional to the difference between its temperature and the ambient temperature $T_a$:
     $$
     \frac{dT}{dt} = -k(T - T_a),
     $$
     where $k > 0$ is the cooling constant. This is also a separable equation. Solving it gives:
     $$
     T(t) = T_a + (T_0 - T_a)e^{-kt},
     $$
     where $T_0$ is the initial temperature. This describes how objects cool down over time.

3. **RC Circuits (Electrical Engineering):**
   - In an RC circuit, the charge $Q(t)$ on a capacitor changes over time due to the flow of current. The governing equation is:
     $$
     \frac{dQ}{dt} + \frac{Q}{RC} = \frac{V}{R},
     $$
     where $R$ is resistance, $C$ is capacitance, and $V$ is the applied voltage. This is a linear first-order equation. Solving it gives:
     $$
     Q(t) = CV + (Q_0 - CV)e^{-t/RC},
     $$
     where $Q_0$ is the initial charge. This describes the charging or discharging of a capacitor.

4. **Population Growth (Logistic Model):**
   - The growth of a population $P(t)$ is limited by resources. The logistic equation models this:
     $$
     \frac{dP}{dt} = rP\left(1 - \frac{P}{K}\right),
     $$
     where $r$ is the growth rate and $K$ is the carrying capacity. This is a nonlinear equation. Solving it gives:
     $$
     P(t) = \frac{K}{1 + \left(\frac{K - P_0}{P_0}\right)e^{-rt}},
     $$
     where $P_0$ is the initial population. This describes how populations grow and stabilize.

5. **Fluid Flow (Torricelli's Law):**
   - The height $h(t)$ of water in a tank decreases as water flows out through a hole at the bottom. Torricelli's law states:
     $$
     \frac{dh}{dt} = -k\sqrt{h},
     $$
     where $k$ depends on the size of the hole. This is a separable equation. Solving it gives:
     $$
     h(t) = \left(\sqrt{h_0} - \frac{kt}{2}\right)^2,
     $$
     where $h_0$ is the initial height. This describes the draining of a tank.

---

#### **Solution Techniques**

1. **Separation of Variables:**
   - Rearrange the equation so that all terms involving $y$ are on one side and all terms involving $x$ are on the other:
     $$
     \int \frac{1}{h(y)} dy = \int g(x) dx.
     $$
   - Integrate both sides to find the solution.

2. **Integrating Factor Method (for Linear Equations):**
   - Multiply the equation by an integrating factor $\mu(x) = e^{\int P(x) dx}$ to make the left-hand side a perfect derivative:
     $$
     \mu(x)\frac{dy}{dx} + \mu(x)P(x)y = \mu(x)Q(x).
     $$
   - Solve using standard integration techniques.

3. **Exact Equations:**
   - Check if $M(x, y)dx + N(x, y)dy = 0$ satisfies $\frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$. If so, integrate $M$ with respect to $x$ and $N$ with respect to $y$ to find the solution.

4. **Substitution Methods:**
   - For Bernoulli equations ( $\frac{dy}{dx} + P(x)y = Q(x)y^n$), substitute $v = y^{1-n}$ to reduce it to a linear equation.

---

#### **Applications in Physics**

1. **Mechanics:**
   - Motion under air resistance:
     $$
     m\frac{dv}{dt} = mg - kv,
     $$
     where $v$ is velocity, $g$ is gravity, and $k$ is the drag coefficient.

2. **Thermodynamics:**
   - Heat conduction in materials:
     $$
     \frac{dT}{dx} = -k(T - T_{\text{env}}).
     $$

3. **Electromagnetism:**
   - Charging/discharging of capacitors in circuits.

4. **Biology:**
   - Population dynamics and chemical reactions.

5. **Fluid Dynamics:**
   - Draining tanks and fluid flow through pipes.

---

#### **Conclusion**
First-order differential equations are essential tools in physics for modeling systems where the rate of change of a quantity depends on the current state. They describe phenomena ranging from radioactive decay and cooling to population growth and electrical circuits. By mastering the solution techniques—separation of variables, integrating factors, and substitution methods—you can analyze and predict the behavior of these systems.

**Final Answer:** First-order differential equations in physics model rates of change in systems such as radioactive decay, cooling, population growth, and electrical circuits. Their solutions provide insights into how physical quantities evolve over time, making them crucial for understanding dynamic processes.