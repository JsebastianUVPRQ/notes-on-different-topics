
Two functions $f(x)$ and $g(x)$ are said to be [[orthogonal]] if their inner product vanishes, i.e.,
$$
\begin{equation*}
(f, g)=\int_{a}^{b} f^{*}(x) g(x) d x=0 \tag{1.2.1}
\end{equation*}
$$

A function is said to be [[normalized]] if its norm equals to unity, i.e.,
$$
\begin{equation*}
\|f\|=\sqrt{(f, f)}=1 \tag{1.2.2}
\end{equation*}
$$

Consider now a set of normalized functions $\left\{\phi_{1}(x), \phi_{2}(x), \phi_{3}(x), \ldots\right\}$ which are mutually orthogonal. Such a set is called an [[orthonormal set of functions]], satisfying the orthonormality condition
$$
\left(\phi_{i}, \phi_{j}\right)=\delta_{i j}= \begin{cases}1, & \text { if } i=j  \tag{1.2.3}\\ 0, & \text { otherwise }\end{cases}
$$
where $\delta_{i j}$ is the Kronecker delta symbol itself defined by Eq. (1.2.3).

An orthonormal set of functions $\left\{\phi_{n}(x)\right\}$ is said to form a [[basis for a function space]], or to be [[COMPLETE]], if any function $f(x)$ in that space can be expanded in a series of the form
$$
\begin{equation*}
f(x)=\sum_{n=1}^{\infty} a_{n} \phi_{n}(x) . \tag{1.2.4}
\end{equation*}
$$
(This is not the exact definition of a complete set but it will do for our purposes.) To find the coefficients of the expansion in Eq. (1.2.4), we take the inner product of both sides with $\phi_{m}(x)$ from the left to obtain
$$
\begin{align*}
\left(\phi_{m}, f\right) & =\sum_{n=1}^{\infty}\left(\phi_{m}, a_{n} \phi_{n}\right) \\
& =\sum_{n=1}^{\infty} a_{n}\left(\phi_{m}, \phi_{n}\right)  \tag{1.2.5}\\
& =\sum_{n=1}^{\infty} a_{n} \delta_{m n}=a_{m} .
\end{align*}
$$

In other words, for any $n$,
$$
\begin{equation*}
a_{n}=\left(\phi_{n}, f\right)=\int_{a}^{b} \phi_{n}^{*}(x) f(x) d x . \tag{1.2.6}
\end{equation*}
$$

An example of an orthonormal system of functions on the interval $(-l, l)$ is the infinite set
$$
\begin{equation*}
\phi_{n}(x)=\frac{1}{\sqrt{2 l}} \exp \left[\frac{i n \pi x}{l}\right], \quad n=0, \pm 1, \pm 2, \ldots \tag{1.2.7}
\end{equation*}
$$
with which the expansion of a square-integrable function $f(x)$ on $(-l, l)$ takes the form
$$
\begin{equation*}
f(x)=\sum_{n=-\infty}^{\infty} c_{n} \exp \left[\frac{i n \pi x}{l}\right], \tag{1.2.8a}
\end{equation*}
$$
with
$$
\begin{equation*}
c_{n}=\frac{1}{2 l} \int_{-l}^{+l} f(x) \exp \left[-\frac{i n \pi x}{l}\right], \tag{1.2.8b}
\end{equation*}
$$
which is the familiar complex form of the Fourier series of $f(x)$.

Finally the Dirac delta function $\delta\left(x-x^{\prime}\right)$, defined with $x$ and $x^{\prime}$ in $(a, b)$, can be expanded in terms of a complete set of orthonormal functions $\phi_{n}(x)$ in the form
$$
\delta\left(x-x^{\prime}\right)=\sum_{n} a_{n} \phi_{n}(x)
$$
with
$$
a_{n}=\int_{a}^{b} \phi_{n}^{*}(x) \delta\left(x-x^{\prime}\right) d x=\phi_{n}^{*}\left(x^{\prime}\right) .
$$

That is,
$$
\begin{equation*}
\delta\left(x-x^{\prime}\right)=\sum_{n} \phi_{n}^{*}\left(x^{\prime}\right) \phi_{n}(x) . \tag{1.2.9}
\end{equation*}
$$

The expression (1.2.9) is sometimes taken as the statement which implies the completeness of an orthonormal system of functions.

## {1.3 Linear Operators}

An operator can be thought of as a mapping or a transformation which acts on a member of the function space ( i.e., a function) to produce another member of that space (i.e., another function). The operator, typically denoted by a symbol such as $L$, is said to be linear if it satisfies
$$
\begin{equation*}
L(\alpha f+\beta g)=\alpha L f+\beta L g, \tag{1.3.1}
\end{equation*}
$$
where $\alpha$ and $\beta$ are complex numbers, and $f$ and $g$ are members of that function space.

Some trivial examples of linear operators $L$ are
(i) multiplication by a constant scalar, i.e.,
$$
L \phi=a \phi,
$$
(ii) taking the third derivative of a function, i.e.,
$$
L \phi=\frac{d^{3}}{d x^{3}} \phi \quad \text { or } \quad L=\frac{d^{3}}{d x^{3}},
$$
which is a differential operator, or,
(iii) multiplying a function by the kernel, $K\left(x, x^{\prime}\right)$, and integrating over $(a, b)$ with respect to $x^{\prime}$, i.e.,
$$
L \phi(x)=\int_{a}^{b} K\left(x, x^{\prime}\right) \phi\left(x^{\prime}\right) d x^{\prime}
$$
which is an integral operator.
An important concept in the theory of the linear operator is that of the adjoint of the operator which is defined as follows. Given the operator $L$, together with an inner product defined on a vector space, the adjoint $L^{\text {adj }}$ of the operator $L$ is that operator for which
$$
\begin{equation*}
(\psi, L \phi)=\left(L^{\mathrm{adj}} \psi, \phi\right) \tag{1.3.2}
\end{equation*}
$$
is an identity for any two members $\phi$ and $\psi$ of the vector space.
Actually, as we shall see later, in the case of the differential operators, we frequently need to worry to some extent about the boundary conditions associated with the original and the adjoint problems. Indeed, there often arise additional terms on the right-hand side of Eq. (1.3.2) which involve the boundary points, and a prudent choice of the adjoint boundary conditions will need to be made in order to avoid unnecessary difficulties. These issues will be raised in connection with Green's functions for differential equations.

---
En realidad, como veremos más adelante, en el caso de los operadores diferenciales, con frecuencia necesitamos preocuparnos hasta cierto punto por las condiciones de contorno asociadas con los problemas original y adjunto. De hecho, a menudo surgen términos adicionales en el lado derecho de la Ecuación (1.3.2) que involucran los puntos de contorno, y será necesario hacer una elección prudente de las condiciones de contorno adjuntas para evitar dificultades innecesarias. Estos temas se plantearán en relación con las funciones de Green para ecuaciones diferenciales.

As our first example of the adjoint operator, consider the liner vector space of $n$ dimensional complex column vectors $\vec{u}, \vec{v}, \ldots$ with their associated inner product (1.1.10). In this space, $n \times n$ square matrices $A, B, \ldots$ with complex entries are linear operators when multiplied by the $n$-dimensional complex column vectors according to the usual rules of matrix multiplication. Consider now the problem of finding the adjoint $A^{\text {adj }}$ of the matrix $A$. According to the definition (1.3.2) of the adjoint operator, we search for the matrix $A^{\text {adj }}$ satisfying
$$
\begin{equation*}
(\vec{u}, A \vec{v})=\left(A^{\mathrm{adj}} \vec{u}, \vec{v}\right) \tag{1.3.3}
\end{equation*}
$$

Now, from the definition of the inner product (1.1.10), we must have
$$
\vec{u}^{* \mathrm{~T}}\left(A^{\mathrm{adj}}\right)^{* \mathrm{~T}} \vec{v}=\vec{u}^{* \mathrm{~T}} A \vec{v},
$$
i.e.,
$$
\begin{equation*}
\left(A^{\mathrm{adj}}\right)^{* \mathrm{~T}}=A \quad \text { or } \quad A^{\mathrm{adj}}=A^{* \mathrm{~T}} . \tag{1.3.4}
\end{equation*}
$$

That is, the adjoint $A^{\text {adj }}$ of a matrix $A$ is equal to the complex conjugate of its transpose, which is also known as its Hermitian transpose,
$$
\begin{equation*}
A^{\mathrm{adj}}=A^{* \mathrm{~T}} \equiv A^{\mathrm{H}} . \tag{1.3.5}
\end{equation*}
$$

As a second example, consider the problem of finding the adjoint of the linear integral operator
$$
\begin{equation*}
L=\int_{a}^{b} d x^{\prime} K\left(x, x^{\prime}\right) \tag{1.3.6}
\end{equation*}
$$
on our function space. By definition, the adjoint $L^{\text {adj }}$ of $L$ is the operator which satisfies Eq. (1.3.2). Upon expressing the left-hand side of Eq. (1.3.2) explicitly with the operator $L$ given by Eq. (1.3.6), we find
$$
\begin{equation*}
(\psi, L \phi)=\int_{a}^{b} d x \psi^{*}(x) L \phi(x)=\int_{a}^{b} d x^{\prime}\left[\int_{a}^{b} d x K\left(x, x^{\prime}\right) \psi^{*}(x)\right] \phi\left(x^{\prime}\right) \tag{1.3.7}
\end{equation*}
$$

Requiring Eq. (1.3.7) to be equal to
$$
\left(L^{\mathrm{adj}} \psi, \phi\right)=\int_{a}^{b} d x\left(L^{\mathrm{adj}} \psi(x)\right)^{*} \phi(x)
$$
necessitates defining
$$
L^{\mathrm{adj}} \psi(x)=\int_{a}^{b} d \xi K^{*}(\xi, x) \psi(\xi)
$$

Hence the adjoint of integral operator (1.3.6) is found to be
$$
\begin{equation*}
L^{\mathrm{adj}}=\int_{a}^{b} d x^{\prime} K^{*}\left(x^{\prime}, x\right) \tag{1.3.8}
\end{equation*}
$$

**Note that**, aside from the complex conjugation of the kernel $K\left(x, x^{\prime}\right)$, the integration in Eq. (1.3.6) is carried out with respect to the second argument of $K\left(x, x^{\prime}\right)$ while that in Eq. (1.3.8) is carried out with respect to the first argument of $K^{*}\left(x^{\prime}, x\right)$. Also, be careful to note which of the variables throughout the above is the dummy variable of integration.

Before we end this section, let us define what is meant by a self-adjoint operator. An operator $L$ is said to be self-adjoint (or Hermitian) if it is equal to its own adjoint $L^{\text {adj }}$. Hermitian operators have very nice properties which will be discussed in Section 1.6. Not the least of these is that their eigenvalues are real. (Eigenvalue problems are discussed in the next section.)

Examples of self-adjoint operators are Hermitian matrices, i.e., matrices which satisfies
$$
A=A^{\mathrm{H}}
$$
and linear integral operators of the type (1.3.6) whose kernel satisfy
$$
K\left(x, x^{\prime}\right)=K^{*}\left(x^{\prime}, x\right)
$$
each on their respective linear spaces and with their respective inner products.

## 1.4 Eigenvalues and Eigenfunctions

Given a linear operator $L$ on a linear vector space, we can set up the following eigenvalue problem
$$
\begin{equation*}
L \phi_{n}=\lambda_{n} \phi_{n} \quad(n=1,2,3, \ldots) \tag{1.4.1}
\end{equation*}
$$

Obviously the trivial solution $\phi(x)=0$ always satisfies this equation, but it also turns out that for some particular values of $\lambda$ (called the eigenvalues and denoted by $\lambda_{n}$ ), nontrivial solutions to Eq. (1.4.1) also exist. Note that for the case of the differential operators on bounded domains, we must also specify an appropriate homogeneous boundary condition (such that $\phi=0$ satisfies those boundary conditions) for the eigenfunctions $\phi_{n}(x)$. We have affixed the subscript $n$ to the eigenvalues and eigenfunctions under the assumption that the eigenvalues are discrete and that they can be counted (i.e., with $n=1,2,3, \ldots$ ). This is not always the case. The conditions which guarantee the existence of a discrete (and complete) set of eigenfunctions are beyond the scope of this introductory chapter and will not be discussed.

So, for the moment, let us tacitly assume that the eigenvalues $\lambda_{n}$ of Eq. (1.4.1) are discrete and that their eigenfunctions $\phi_{n}$ form a basis (i.e., a complete set) for their space.

Similarly the adjoint $L^{\text {adj }}$ of the operator $L$ would posses a set of eigenvalues and eigenfunctions satisfying
$$
\begin{equation*}
L^{\text {adj }} \psi_{m}=\mu_{m} \psi_{m} \quad(m=1,2,3, \ldots) \tag{1.4.2}
\end{equation*}
$$

It can be shown that the eigenvalues $\mu_{m}$ of the adjoint problem are equal to complex conjugates of the eigenvalues $\lambda_{n}$ of the original problem. (We will prove this only for matrices but it remains true for general operators.) That is, if $\lambda_{n}$ is an eigenvalue of $L, \lambda_{n}^{*}$ is an eigenvalue of $L^{\text {adj. }}$. This prompts us to rewrite Eq. (1.4.2) as
$$
\begin{equation*}
L^{\mathrm{adj}} \psi_{m}=\lambda_{m}^{*} \psi_{m}, \quad(m=1,2,3, \ldots) \tag{1.4.3}
\end{equation*}
$$

It is then a trivial matter to show that the eigenfunctions of the adjoint and original operators are all orthogonal, except those corresponding to the same index $(n=m)$. To do this, take the inner product of Eq. (1.4.1) with $\psi_{m}$ from the left, and the inner product of Eq. (1.4.3) with $\phi_{n}$ from the right, to find
$$
\begin{equation*}
\left(\psi_{m}, L \phi_{n}\right)=\left(\psi_{m}, \lambda_{n} \phi_{n}\right)=\lambda_{n}\left(\psi_{m}, \phi_{n}\right) \tag{1.4.4}
\end{equation*}
$$
and
$$
\begin{equation*}
\left(L^{\mathrm{adj}} \psi_{m}, \phi_{n}\right)=\left(\lambda_{m}^{*} \psi_{m}, \phi_{n}\right)=\lambda_{m}\left(\psi_{m}, \phi_{n}\right) \tag{1.4.5}
\end{equation*}
$$

Subtract the latter two equations and note that their left-hand sides are equal because of the definition of the adjoint, to get
$$
\begin{equation*}
0=\left(\lambda_{n}-\lambda_{m}\right)\left(\psi_{m}, \phi_{n}\right) \tag{1.4.6}
\end{equation*}
$$

This implies
$$
\begin{equation*}
\left(\psi_{m}, \phi_{n}\right)=0 \quad \text { if } \quad \lambda_{n} \neq \lambda_{m} \tag{1.4.7}
\end{equation*}
$$
which proves the desired result. Also, since each $\phi_{n}$ and $\psi_{m}$ is determined to within a multiplicative constant (e.g., if $\phi_{n}$ satisfies Eq. (1.4.1) so does $\alpha \phi_{n}$ ), the normalization for the latter can be chosen such that
$$
\left(\psi_{m}, \phi_{n}\right)=\delta_{m n}= \begin{cases}1, & \text { for } n=m  \tag{1.4.8}\\ 0, & \text { otherwise }\end{cases}
$$

Now, if the set of eigenfunctions $\phi_{n}(n=1,2, \ldots)$ forms a complete set, any arbitrary function $f(x)$ in the space may be expanded as
$$
\begin{equation*}
f(x)=\sum_{n} a_{n} \phi_{n}(x) \tag{1.4.9}
\end{equation*}
$$
and to find the coefficients $a_{n}$, we simply take the inner product of both sides with $\psi_{k}$ to get
$$
\begin{aligned}
\left(\psi_{k}, f\right)=\sum_{n}\left(\psi_{k}, a_{n} \phi_{n}\right) & =\sum_{n} a_{n}\left(\psi_{k}, \phi_{n}\right) \\
& =\sum_{n} a_{n} \delta_{k n}=a_{k},
\end{aligned}
$$
i.e.,
$$
\begin{equation*}
a_{n}=\left(\psi_{n}, f\right), \quad(n=1,2,3, \ldots) \tag{1.4.10}
\end{equation*}
$$

Note the difference between Eqs. (1.4.9) and (1.4.10) and the corresponding formulas (1.2.4) and (1.2.6) for an orthonormal system of functions. In the present case, neither $\left\{\phi_{n}\right\}$ nor $\left\{\psi_{n}\right\}$ form an orthonormal system, but they are orthogonal to one another.

Proof that the eigenvalues of the adjoint matrix are complex conjugates of the eigenvalues of the original matrix.

Above, we claimed without justification that the eigenvalues of the adjoint of an operator are complex conjugates of those of the original operator. Here we show this for the matrix case. The eigenvalues of a matrix $A$ are given by
$$
\begin{equation*}
\operatorname{det}(A-\lambda I)=0 \tag{1.4.11}
\end{equation*}
$$

The latter is the characteristic equation whose $n$ solutions for $\lambda$ are the desired eigenvalues. On the other hand, the eigenvalues of $A^{\text {adj }}$ are determined by setting
$$
\begin{equation*}
\operatorname{det}\left(A^{\mathrm{adj}}-\mu I\right)=0 \tag{1.4.12}
\end{equation*}
$$

Since the determinant of a matrix is equal to that of its transpose, we easily conclude that the eigenvalues of $A^{\text {adj }}$ are the complex conjugates of $\lambda_{n}$.

## 1.5 The Fredholm Alternative}

The Fredholm Alternative, which may be also called the Fredholm solvability condition, is concerned with the existence of the solution $y(x)$ of the inhomogeneous problem
$$
\begin{equation*}
L y(x)=f(x) \tag{1.5.1}
\end{equation*}
$$
where $L$ is a given linear operator and $f(x)$ a known forcing term. As usual, if $L$ is a differential operator, additional boundary or initial conditions must also be specified.

The Fredholm Alternative states that the unknown function $y(x)$ can be determined uniquely if the corresponding homogeneous problem
$$
\begin{equation*}
L \phi_{H}(x)=0 \tag{1.5.2}
\end{equation*}
$$
with homogeneous boundary conditions, has no nontrivial solutions. On the other hand, if the homogeneous problem (1.5.2) does possess a nontrivial solution, then the inhomogeneous problem (1.5.1) has either no solution or infinitely many solutions.

What determines the latter is the homogeneous solution $\psi_{H}$ to the adjoint problem
$$
\begin{equation*}
L^{\mathrm{adj}} \psi_{H}=0 \tag{1.5.3}
\end{equation*}
$$

Taking the inner product of Eq. (1.5.1) with $\psi_{H}$ from the left,
$$
\left(\psi_{H}, L y\right)=\left(\psi_{H}, f\right)
$$

Then, by the definition of the adjoint operator (excluding the case wherein $L$ is a differential operator, to be discussed in Section 1.7.), we have
$$
\left(L^{\text {adj }} \psi_{H}, y\right)=\left(\psi_{H}, f\right)
$$

The left-hand side of the equation above is zero by the definition of $\psi_{H}$, Eq. (1.5.3).
Thus the criteria for the solvability of the inhomogeneous problem Eq. (1.5.1) is given by
$$
\left(\psi_{H}, f\right)=0 .
$$

If these criteria are satisfied, there will be an infinity of solutions to Eq. (1.5.1), otherwise Eq. (1.5.1) will have no solution.

To understand the above claims, let us suppose that $L$ and $L^{\text {adj }}$ possess complete sets of eigenfunctions satisfying
$$
\begin{align*}
& L \phi_{n}=\lambda_{n} \phi_{n} \quad(n=0,1,2, \ldots),  \tag{1.5.4a}\\
& L^{\mathrm{adj}} \psi_{n}=\lambda_{n}^{*} \psi_{n} \quad(n=0,1,2, \ldots) \tag{1.5.4b}
\end{align*}
$$
with
$$
\begin{equation*}
\left(\psi_{m}, \phi_{n}\right)=\delta_{m n} \tag{1.5.5}
\end{equation*}
$$

The existence of a nontrivial homogeneous solution $\phi_{H}(x)$ to Eq. (1.5.2), as well as $\psi_{H}(x)$ to Eq. (1.5.3), is the same as having one of the eigenvalues $\lambda_{n}$ in Eqs. (1.5.4a), (1.5.4b) to be zero. If this is the case, i.e., if zero is an eigenvalue of Eq. (1.5.4a) and hence Eq. (1.5.4b), we shall choose the subscript $n=0$ to signify that eigenvalue ( $\lambda_{0}=0$ ), and in that case
$\phi_{0}$ and $\psi_{0}$ are the same as $\phi_{H}$ and $\psi_{H}$. The two circumstances in the Fredholm Alternative correspond to cases where zero is an eigenvalue of Eqs. (1.5.4a), (1.5.4b) and where it is not.

Let us proceed formally with the problem of solving the inhomogeneous problem Eq. (1.5.1). Since the set of eigenfunctions $\phi_{n}$ of Eq. (1.5.4a) is assumed to be complete, both the known function $f(x)$ and the unknown function $y(x)$ in Eq. (1.5.1) can presumably be expanded in terms of $\phi_{n}(x)$ :
$$
\begin{align*}
& f(x)=\sum_{n=0}^{\infty} \alpha_{n} \phi_{n}(x),  \tag{1.5.6}\\
& y(x)=\sum_{n=0}^{\infty} \beta_{n} \phi_{n}(x) \tag{1.5.7}
\end{align*}
$$
where the $\alpha_{n}$ are known (since $f(x)$ is known), i.e., according to Eq. (1.4.10)
$$
\begin{equation*}
\alpha_{n}=\left(\psi_{n}, f\right), \tag{1.5.8}
\end{equation*}
$$
while the $\beta_{n}$ are unknown. Thus, if all the $\beta_{n}$ can be determined, then the solution $y(x)$ to Eq. (1.5.1) is regarded as having been found.

To try to determine the $\beta_{n}$, substitute both Eqs. (1.5.6) and (1.5.7) into Eq. (1.5.1) to find
$$
\begin{equation*}
\sum_{n=0}^{\infty} \lambda_{n} \beta_{n} \phi_{n}=\sum_{k=0}^{\infty} \alpha_{k} \phi_{k} \tag{1.5.9}
\end{equation*}
$$
where different summation indices have been used on the two sides to remind the reader that the latter are dummy indices of summation. Next, take the inner product of both sides with $\psi_{m}$ (with an index which must be different from the two above) to get
$$
\sum_{n=0}^{\infty} \lambda_{n} \beta_{n}\left(\psi_{m}, \phi_{n}\right)=\sum_{k=0}^{\infty} \alpha_{k}\left(\psi_{m}, \phi_{k}\right)
$$
or
$$
\sum_{n=0}^{\infty} \lambda_{n} \beta_{n} \delta_{m n}=\sum_{k=0}^{\infty} \alpha_{k} \delta_{m k}
$$
i.e.,
$$
\begin{equation*}
\lambda_{m} \beta_{m}=\alpha_{m} \tag{1.5.10}
\end{equation*}
$$

Thus, for any $m=0,1,2, \ldots$, we can solve Eq. (1.5.10) for the unknowns $\beta_{m}$ to get
$$
\begin{equation*}
\beta_{n}=\alpha_{n} / \lambda_{n} \quad(n=0,1,2, \ldots) \tag{1.5.11}
\end{equation*}
$$
provided that $\lambda_{n}$ is not equal to zero. Obviously the only possible difficulty occurs if one of the eigenvalues (which we take to be $\lambda_{0}$ ) is equal to zero. In that case, equation (1.5.10) with $m=0$ reads
$$
\begin{equation*}
\lambda_{0} \beta_{0}=\alpha_{0} \quad\left(\lambda_{0}=0\right) \tag{1.5.12}
\end{equation*}
$$

Now if $\alpha_{0} \neq 0$, then we cannot solve for $\beta_{0}$ and thus the problem $L y=f$ has no solution. On the other hand if $\alpha_{0}=0$, i.e., if
$$
\begin{equation*}
\left(\psi_{0}, f\right)=\left(\psi_{H}, f\right)=0 \tag{1.5.13}
\end{equation*}
$$
implying that $f$ is orthogonal to the homogeneous solution to the adjoint problem, then Eq. (1.5.12) is satisfied by any choice of $\beta_{0}$. All the other $\beta_{n}(n=1,2, \ldots)$ are uniquely determined but there are infinitely many solutions $y(x)$ to Eq. (1.5.1) corresponding to the infinitely many values possible for $\beta_{0}$. The reader must make certain that he or she understands the equivalence of the above with the original statement of the Fredholm Alternative.

## {1.6 Self-adjoint Operators}

Operators which are self-adjoint or Hermitian form a very useful class of operators. They possess a number of special properties, some of which are described in this section.

The first important property of self-adjoint operators is that their eigenvalues are real. To prove this, begin with
$$
\begin{align*}
L \phi_{n} & =\lambda_{n} \phi_{n},  \tag{1.6.1}\\
L \phi_{m} & =\lambda_{m} \phi_{m},
\end{align*}
$$
and take the inner product of both sides of the former with $\phi_{m}$ from the left, and the latter with $\phi_{n}$ from the right, to obtain
$$
\begin{align*}
\left(\phi_{m}, L \phi_{n}\right) & =\lambda_{n}\left(\phi_{m}, \phi_{n}\right)  \tag{1.6.2}\\
\left(L \phi_{m}, \phi_{n}\right) & =\lambda_{m}^{*}\left(\phi_{m}, \phi_{n}\right)
\end{align*}
$$

For a self-adjoint operator $L=L^{\text {adj }}$, the two left-hand sides of Eq. (1.6.2) are equal and hence, upon subtraction of the latter from the former, we find
$$
\begin{equation*}
0=\left(\lambda_{n}-\lambda_{m}^{*}\right)\left(\phi_{m}, \phi_{n}\right) \tag{1.6.3}
\end{equation*}
$$

Now, if $m=n$, the inner product $\left(\phi_{n}, \phi_{n}\right)=\left\|\phi_{n}\right\|^{2}$ is nonzero and Eq. (1.6.3) implies
$$
\begin{equation*}
\lambda_{n}=\lambda_{n}^{*} \tag{1.6.4}
\end{equation*}
$$
proving that all the eigenvalues are real. Thus Eq. (1.6.3) can be rewritten as
$$
\begin{equation*}
0=\left(\lambda_{n}-\lambda_{m}\right)\left(\phi_{m}, \phi_{n}\right) \tag{1.6.5}
\end{equation*}
$$
indicating that if $\lambda_{n} \neq \lambda_{m}$, then the eigenfunctions $\phi_{m}$ and $\phi_{n}$ are orthogonal. Thus, upon normalizing each $\phi_{n}$, we verify a second important property of self-adjoint operators that (upon normalization) the eigenfunctions of a self-adjoint operator form an orthonormal set.

The Fredholm Alternative can also be restated for a self-adjoint operator $L$ in the following form: The inhomogeneous problem $L y=f$ (with $L$ self-adjoint) is solvable for $y$, if $f$ is orthogonal to all eigenfunctions $\phi_{0}$ of $L$ with eigenvalue zero (if indeed any exist). If zero is not an eigenvalue of $L$, the solution is unique. Otherwise, there is no solution if $\left(\phi_{0}, f\right) \neq 0$, and an infinite number of solutions if $\left(\phi_{0}, f\right)=0$.

Diagonalization of Self-adjoint Operators: Any linear operator can be expanded in some sense in terms of any orthonormal basis set. To elaborate on this, suppose that the orthonormal system $\left\{e_{i}(x)\right\}_{i}$, with $\left(e_{i}, e_{j}\right)=\delta_{i j}$ forms a complete set. Any function $f(x)$ can be expanded as
$$
\begin{equation*}
f(x)=\sum_{j=1}^{\infty} \alpha_{j} e_{j}(x), \quad \alpha_{j}=\left(e_{j}, f\right) \tag{1.6.6}
\end{equation*}
$$

Thus the function $f(x)$ can be thought of as an infinite dimensional vector with components $\alpha_{j}$. Now consider the action of an arbitrary linear operator $L$ on the function $f(x)$. Obviously
$$
\begin{equation*}
L f(x)=\sum_{j=1}^{\infty} \alpha_{j} L e_{j}(x) \tag{1.6.7}
\end{equation*}
$$

But $L$ acting on $e_{j}(x)$ is itself a function of $x$ which can be expanded in the orthonormal basis $\left\{e_{i}(x)\right\}_{i}$. Thus we write
$$
\begin{equation*}
L e_{j}(x)=\sum_{i=1}^{\infty} l_{i j} e_{i}(x) \tag{1.6.8}
\end{equation*}
$$
wherein the coefficients $l_{i j}$ of the expansion are found to be $l_{i j}=\left(e_{i}, L e_{j}\right)$. Substitution of Eq. (1.6.8) into Eq. (1.6.7) then shows
$$
\begin{equation*}
L f(x)=\sum_{i=1}^{\infty}\left(\sum_{j=1}^{\infty} l_{i j} \alpha_{j}\right) e_{i}(x) \tag{1.6.9}
\end{equation*}
$$

We discover that just as we can think of $f(x)$ as the infinite dimensional vector with components $\alpha_{j}$, we can consider $L$ to be equivalent to an infinite dimensional matrix with components $l_{i j}$, and we can regard Eq. (1.6.9) as a regular multiplication of the matrix $L$ (components $l_{i j}$ ) with the vector $f$ (components $\alpha_{j}$ ). However, this equivalence of the operator $L$ with the matrix whose components are $l_{i j}$, i.e., $L \Leftrightarrow l_{i j}$, depends on the choice of the orthonormal set.

For a self-adjoint operator $L=L^{\text {adj }}$, the most natural choice of the basis set is the set of eigenfunctions of $L$. Denoting these by $\left\{\phi_{i}(x)\right\}_{i}$, the components of the equivalent matrix for $L$ take the form
$$
\begin{equation*}
l_{i j}=\left(\phi_{i}, L \phi_{j}\right)=\left(\phi_{i}, \lambda_{j} \phi_{j}\right)=\lambda_{j}\left(\phi_{i}, \phi_{j}\right)=\lambda_{j} \delta_{i j} \tag{1.6.10}
\end{equation*}
$$

## 1.7 Green's Functions for Differential Equations}

In this section, we describe the conceptual basis of the theory of Green's functions. We do this by first outlining the abstract themes involved and then by presenting a simple example. More complicated examples will appear in later chapters.

Prior to discussing Green's functions, recall some of the elementary properties of the socalled Dirac delta function $\delta\left(x-x^{\prime}\right)$. In particular, remember that if $x^{\prime}$ is inside the domain