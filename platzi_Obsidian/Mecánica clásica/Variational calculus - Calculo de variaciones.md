Presentamos el cálculo variacional y el enfoque variacional a la dinámica, que se basa en el **Principio de Mínima Acción**. En esta sección, desarrollaremos el cálculo variacional y derivaremos la ecuación de **Euler-Lagrange** a partir de un principio variacional, en lugar de hacerlo desde la segunda ley de Newton. Las restricciones holonómicas se incluirán mediante la técnica de los multiplicadores de Lagrange, lo cual es una alternativa a definir un conjunto de coordenadas generalizadas no restringidas que hayan eliminado cualquier grado de libertad sujeto a restricciones. Algunas restricciones no-holonómicas también pueden abordarse mediante dinámica variacional. Aunque pueda parecer que tanto esta sección como la anterior son nuevas formulaciones de la mecánica, uno debe darse cuenta de que la mecánica lagrangiana introducida en el capítulo anterior se deriva directamente de la segunda ley de Newton. El uso de restricciones, variables generalizadas, el lagrangiano y la derivación de la ecuación de Euler-Lagrange deben considerarse como "tecnología", no como nueva física. Esta sección, por otro lado, proporciona un nuevo principio sobre el cual basar la mecánica, una alternativa a la segunda ley de Newton. Otra diferencia entre la última sección y esta es que, en la última sección, continuamos con la tendencia mecánica newtoniana de derivar las ecuaciones de movimiento a partir de un "principio diferencial" — es decir, las ecuaciones de movimiento solo se preocupan por lo que ocurre localmente. Como dice Goldstein, el Principio de Mínima Acción es diferente porque es un "principio integral", determinando las ecuaciones de movimiento a partir de un requisito sobre todo el movimiento del sistema entre un par de tiempos inicial y final.

La nomenclatura e historia sin duda se están volviendo muy confusas. La línea de razonamiento presentada en la sección anterior se debe a Lagrange y, por lo tanto, se conoce como **mecánica lagrangiana**. Pero Lagrange también fue responsable de la aplicación del cálculo variacional a la mecánica, y por eso el material derivado en esta sección a veces también se denomina **dinámica lagrangiana**. Pero, de hecho, el Principio de Mínima Acción fue formulado por Hamilton, no por Lagrange. La confusión continuará cuando empecemos con la dinámica hamiltoniana en la siguiente sección. Nos referiremos al uso del cálculo de variaciones en la mecánica como **dinámica variacional** o **mecánica variacional** para distinguirla de la mecánica lagrangiana estudiada en la sección anterior. Seguimos el Capítulo 2 de Hand y Finch, aunque con algunas diferencias pedagógicas en cómo se derivan ciertos resultados. Consulte también los Capítulos 6 y 7 de Thornton.

### 2.2.1 El Cálculo Variacional y la Ecuación de Euler
Comenzamos estudiando el cálculo variacional como una herramienta puramente matemática. Un nombre mejor podría ser "cálculo funcional" porque consideraremos el concepto de diferenciación con respecto a funciones en lugar de números o conjuntos de números. Derivaremos la ecuación de Euler, un resultado importante del cálculo variacional que aplicaremos a la mecánica.

#### Funcionales y Variaciones

- **Función** = regla que asigna un conjunto de números de entrada a un conjunto de números de salida.
- **Funcional** = regla que asigna una función o conjunto de funciones a un conjunto de números de salida.

Ejemplo no genérico:
$$
I[y] \equiv \int_{x_0}^{x_1} dx F\left(y, \frac{dy}{dx}, x\right) \tag{2.21}
$$
donde $x$ es la variable de integración, $y$ es una función de $x$, y $F$ es una función simple que acepta tres argumentos. Por ejemplo, $F = y^2 + \left(\frac{dy}{dx}\right)^3 + x^4$. El funcional $I[y]$ es solo un ejemplo específico de un funcional. No todos los funcionales están basados en una integración. Además, la elección de los argumentos de la función $F - y$, $\frac{dy}{dx}$, y $x$ es especial.

- "Variación" en la función $y$: el equivalente funcional del diferencial en una variable $dy$: pequeños cambios en la función $y$ en cada punto $x$, manteniendo los valores de los extremos $y(x_0)$ y $y(x_1)$ fijos, y denotados por $\delta y$. También habrá una variación en $\frac{dy}{dx}$, denotada por $\delta \frac{dy}{dx}$, aunque está completamente especificada por la variación $\delta y$ porque $\delta \frac{dy}{dx} = \frac{d}{dx}\delta y$. (Esta afirmación no contradice el argumento en nuestra discusión de la mecánica lagrangiana de que una coordenada generalizada y su velocidad asociada – aquí representadas más abstractamente por $y$ y $\frac{dy}{dx}$ – son independientes.) Para visualizar la variación $\delta y$, piense en una cuerda flexible y estirable que se mantiene fija en sus extremos.

- "Variación" en el funcional $I$: El cambio en $I$ debido a las variaciones $\delta y$ y $\delta \frac{dy}{dx}$ se encuentra de manera familiar desde el cálculo elemental:
$$
\begin{aligned}
\delta I~ &\equiv  I~[y~ + \delta y~] - I[y] \\
&= \int_{x_0}^{x_1} dx F\left(y + \delta y, \frac{dy}{dx} + \delta \frac{dy}{dx}, x\right) - \int_{x_0}^{x_1} dx F\left(y, \frac{dy}{dx}, x\right)
\end{aligned}
$$
$\delta I$ es la "variación". Podemos evaluarlo aún más utilizando la regla de la cadena:
$$
F\left(y + \delta y, \frac{dy}{dx} + \delta \frac{dy}{dx}, x\right) - F\left(y, \frac{dy}{dx}, x\right) = \frac{\partial F}{\partial y} \delta y + \frac{\partial F}{\partial \frac{dy}{dx}} \delta \frac{dy}{dx} + \mathcal{O}(\delta^2)
$$
donde $\mathcal{O}(\delta^2)$ denota los términos de orden superior que se ignoran en esta expansión lineal. Entonces tenemos
$$
\delta I = \int_{x_0}^{x_1} dx \left[ \frac{\partial F}{\partial y} \delta y + \frac{\partial F}{\partial \frac{dy}{dx}} \delta \frac{dy}{dx} \right]
$$
$$
= \int_{x_0}^{x_1} dx \left[ \frac{\partial F}{\partial y} \delta y + \frac{\partial F}{\partial \frac{dy}{dx}} \frac{d}{dx} \delta y \right]
$$
$$
= \int_{x_0}^{x_1} dx \left[ \frac{\partial F}{\partial y} \delta y - \frac{d}{dx} \left( \frac{\partial F}{\partial \frac{dy}{dx}} \right) \delta y \right] + \left[ \frac{\partial F}{\partial \frac{dy}{dx}} \delta y \right]_{x_0}^{x_1}
$$
donde en el penúltimo paso integramos por partes. El "término superficial" desapareció debido a las condiciones de contorno en $\delta y$.

---

<sup>9</sup>Es cierto que, para una trayectoria candidata dada $y(x)$, la función $\frac{dy}{dx}$ está completamente especificada. Sin embargo, en este momento —es decir, antes de escribir y resolver la ecuación de Euler— no sabemos qué camino candidato $y(x)$ es el correcto. Hay toda una familia de caminos candidatos que pasan por un valor dado de $y$ en un valor dado de $x$, pero cuyas primeras y derivadas de orden superior difieren todas, y permitimos que cualquiera de ellos sea un camino candidato. Uno podría seguir preocupándose de que, si $y$ y $\frac{dy}{dx}$ en un valor dado de $x$ son conocidos, entonces toda la trayectoria $y(x)$ estaría especificada. Esto simplemente no es cierto porque uno tiene infinita libertad en las derivadas de orden superior de $y(x)$ en este momento. Otra forma de expresarlo es: si $y$ y $\frac{dy}{dx}$ en un valor dado de $x$ son conocidos, ¿es posible predecir $y$ para valores cercanos de $x$? No, porque la expansión de Taylor que conecta $y$ en dos valores de $x$ es una serie de potencias infinita con un número infinito de derivadas por especificar. Así, hasta que se encuentre una trayectoria física $y(x)$ mediante la ecuación de Euler, $y$ y $\frac{dy}{dx}$ son variables independientes; pero, para un camino candidato particular, no lo son.