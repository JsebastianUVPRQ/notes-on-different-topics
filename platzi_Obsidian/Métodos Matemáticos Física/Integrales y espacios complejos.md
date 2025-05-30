1.1 Function Spaces

Consider the set of all complex valued functions of the real variable $x$, denoted by $f(x), g(x), \ldots$ and defined on the interval $(a, b)$. We shall restrict ourselves to those functions which are square-integrable. Define the inner product of any two of the latter functions by
$$
(f, g) \equiv \int_a^b f^*(x) g(x) d x
$$
in which $f^*(x)$ is the complex conjugate of $f(x)$. The following properties of the inner product follow from the definition (1.1.1).
$$
\begin{array}{rlc}
(f, g)^* & = & (g, f) \\
(f, g+h) & = & (f, g)+(f, h) \\
(f, \alpha g) & = & \alpha(f, g) \\
(\alpha f, g) & = & \alpha^*(f, g)
\end{array}
$$

While the inner product of any two functions is in general a complex number, the inner
product of a function with itself is a real number and is non-negative. This prompts us to
define the norm of a function by

$$
\|f\| \equiv \sqrt{(f, f)}=\left[\int_a^b f^*(x) f(x) d x\right]^{\frac{1}{2}}
$$

## Schwarz inequality

A very important inequality satisfied by the inner product (1.1.1) is the so-called __Schwarz inequality__ which says
$$
|(f, g)| \leq\|f\| \cdot\|g\|
$$

To prove the latter, start with the trivial inequality $\|(f+\alpha g)\|^2 \geq 0$, which holds for any $f(x)$ and $g(x)$ and for any complex number $\alpha$. With a little algebra, the left-hand side of this inequality may be expanded to yield
$$
(f, f)+\alpha^*(g, f)+\alpha(f, g)+\alpha \alpha^*(g, g) \geq 0
$$

The latter inequality is true for any $\alpha$, and is thus true for the value of $\alpha$ which minimizes the left-hand side. This value can be found by writing $\alpha$ as $a+i b$ and minimizing the left-hand side 
of Eq. (1.1.6) with respect to the real variables $a$ and $b$. 
A quicker way would be to treat $\alpha$ and $\alpha^*$ as independent variables and requiring 
$\partial / \partial \alpha$ and $\partial / \partial \alpha^*$ of the left hand side of Eq. (1.1.6) to vanish.
This immediately yields $\alpha=-(g, f) /(g, g)$ as the value of $\alpha$ at which the minimum occurs. Evaluating the left-hand side of Eq. (1.1.6) at this minimum then yields