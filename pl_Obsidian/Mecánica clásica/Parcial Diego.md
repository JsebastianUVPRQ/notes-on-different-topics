## 1.

Question 1

To register a model using a reference to the Run used to train the model, which SDK commands can you use?

a. from azureml.core import Object

run.register_model( model_name='classification_model',

model_path='outputs/model.pkl',

description='A classification model')

b. from azureml.core import Model

run.register_model( model_name='classification_model',

model_path='outputs/model.pkl',

description='A classification model')

c. from azureml.core import Object

classification_model = Model.register(workspace=your_workspace,

model_name='classification_model',

model_path='model.pkl',

description='A classification model')

d. from azureml.core import Model

classification_model = Model.register(workspace=your_workspace,

model_name='classification_model',

model_path='model.pkl',

description='A classification model')

### 2.

Question 2

Which of the following SDK commands can you use to create a parallel run step?



a. parallelrun_step = ParallelRunStep(

name='batch-score',

parallel_run_config=parallel_run_config,

inputs=[batch_data_set.as_named_input('batch_data')],

output=output_dir,

arguments=[],

allow_reuse=True

b. parallelrun_step = ParallelRunStep(

name='batch-score',

parallel.run.config=parallel_run_config,

inputs=[batch_data_set.as_named_input('batch_data')],

output=output_dir,

arguments=[],

allow_reuse=True

c. parallelrun_step = ParallelRunStep(

name='batch-score',

parallel_run_config=parallel.run.config,

inputs=[batch_data_set.as_named_input('batch_data')],

output=output_dir,

arguments=[],

allow_reuse=True

d. parallelrun.step = ParallelRunStep(

name='batch-score',

parallel_run_config=parallel_run_config,

inputs=[batch_data_set.as_named_input('batch_data')],

output=output_dir,

arguments=[],

allow_reuse=True

### 3.

Question 3

After the run of the pipeline has completed, which code can you use to retrieve the parallel_run_step.txt file from the output of the step?


a. prediction_run = next(pipeline_run.get_children())

prediction_output = prediction_run.get_output_data('inferences')

prediction_output.download(local_path='results')

b. for root, dirs, files in os.walk('results'):

for file in files:

if file.endswith('parallel_run_step.txt'):

result_file = os.path.join(root,file)

c. df = pd.read_csv(result_file, delimiter=":", header=None)

df.columns = ["File", "Prediction"]

print(df)

### 4.

Question 4

You want to define a search space for hyperparameter tuning. The batch_size hyperparameter can have the value 128, 256, or 512 and the learning_rate hyperparameter can have values from a normal distribution with a mean of 10 and a standard deviation of 3.

How can you code this in Python?



from azureml.train.hyperdrive import choice, normal

param_space = {

'--batch_size': choice(128, 256, 512),

'--learning_rate': lognormal(10, 3)

}

from azureml.train.hyperdrive import choice, uniform

param_space = {

'--batch_size': choice(128, 256, 512),

'--learning_rate': uniform(10, 3)

}

from azureml.train.hyperdrive import choice, normal

param_space = {

'--batch_size': choice(128, 256, 512),

'--learning_rate': qnormal(10, 3)

}

from azureml.train.hyperdrive import choice, normal

param_space = {

'--batch_size': choice(128, 256, 512),

'--learning_rate': normal(10, 3)

}

### 5.

Question 5

How does random sampling select values for hyperparameters?



It tries every possible combination of parameters in the search space

From a mix of discrete and continuous values

It tries to select parameter combinations that will result in improved performance from the previous selection

### 6.

Question 6

True or False?

Bayesian sampling can be used only with choice, uniform and quniform parameter expressions, and it can be combined with an early-termination policy.


False

True

### 7.

Question 7

You want to implement a median stopping policy. How can you code this in Python?



a. from azureml.train.hyperdrive import MedianStoppinPolicy

early_termination_policy = MedianStoppingPolicy(slack_amount = 0.2,

evaluation_interval=1,

delay_evaluation=5)

b. from azureml.train.hyperdrive import MedianStoppingPolicy

early_termination_policy = MedianStoppingPolicy(evaluation_interval=1,

delay_evaluation=5)

c. from azureml.train.hyperdrive import MedianStoppingPolicy

early_termination_policy = MedianStoppingPolicy(truncation_percentage=10,

evaluation_interval=1,

delay_evaluation=5)

### Exam Text Extraction

The provided document is an exam in Spanish

---
#### Problem 1
- Fermat's principle states that the trajectory followed by a light ray between two points is the one that corresponds to the minimum time. Use this idea and the variational principle to determine the trajectory of a light ray between two points in the$xx$-plane if it is considered that the medium has a refractive index$n = c/v$, where$c$is the speed of light in vacuum and$v$is the speed of light in the medium given by:
$$
  n(z) = n_0 - \alpha z, \quad n_0, \alpha > 0.
$$
  Sketch the obtained trajectory. Hint:$\int \frac{dx}{\sqrt{\xi^2 - a^2}} = \cosh^{-1}(\xi/a)$.

#### Problem 2
- Consider a spring pendulum, in which a particle of mass$m$moves in the$xy$-plane attached to a spring with elastic constant$k$and natural length$\ell$. The weight acts in the direction$-\mathbf{j}$. The particle is subjected to a viscous force proportional to its velocity, i.e.,$\mathbf{f} = -\mu \mathbf{v}$,$\mu > 0$.

1. Write the Lagrangian of the system using the most appropriate coordinates.
2. Write the components of the generalized force associated with the non-conservative force. (Remember:$Q_j^{NC} = \sum_i \mathbf{f}_i \cdot \frac{\partial \mathbf{q}_i}{\partial q_j}$).
3. Find the equations of motion of the system. Do not solve them.

#### Problem 3
- A particle of mass $m$ moves with velocity $\dot{\mathbf{r}}$ subject to the potential
$$
  V(\mathbf{r}, \dot{\mathbf{r}}) = U(r) + \mathbf{n} \cdot \mathbf{l},
$$
  where $\mathbf{r}$ is the position vector measured from the origin of the reference system, $\mathbf{l}$ is the angular momentum with respect to that origin, $\mathbf{n}$ is a fixed vector in space, and $U(r)$ is a scalar function.

1. Find the force exerted on the particle.
2. Determine all conserved quantities. Explain.  
   Hint: You may find the identity useful:$\nabla (\mathbf{A} \cdot \mathbf{B}) = \mathbf{A} \times (\nabla \times \mathbf{B}) + \mathbf{B} \times (\nabla \times \mathbf{A}) + (\mathbf{A} \cdot \nabla) \mathbf{B} + (\mathbf{B} \cdot \nabla) \mathbf{A}$.

#### Problem 4
- Modifications of the Lagrangian of the form:
$$
  L(q, \dot{q}) \longrightarrow L'(q, \dot{q}) = L(q, \dot{q}) + \frac{d}{dt} M(q, t),
$$
  are called Gauge Transformations.

1. Determine
$$
  \frac{d}{dt} \left( \frac{\partial (L' - L)}{\partial \dot{q}_k} \right) - \frac{\partial (L' - L)}{\partial q_k}
$$
  and explain the implications of this result.
2. Determine the equations of motion obtained from the Lagrangians
3. 1.$L(q, \dot{q}) = \frac{1}{2} m \dot{q}^2 - \frac{1}{2} m \omega^2 q^2$,
4. 2.$L'(q, \dot{q}) = \frac{1}{2} m \dot{q}^2 + q \dot{q} - \frac{1}{2} m \omega^2 q^2$.
   Can it be considered that there exists a Gauge Transformation between these Lagrangians? Explain.

---
---
ESPAÑOL
---

Here is the complete text of the exam in its original Spanish language:

---

### **Examen de Física**

#### **Encabezado**
**Grupo:**  
**Calificación:**

**Durante el desarrollo de la evaluación no está permitido el uso de apuntes y aparatos electrónicos. Toda respuesta debe ir acompañada de un procedimiento o una justificación adecuada según se solicite, de no ser así dicha solución no tendrá ninguna validez. La notación incorrecta o inconsistente también será evaluada. Solamente se calificarán las respuestas y los procedimientos contenidos en la hoja establecida para ello, no se aceptan hojas sueltas que no hayan sido previamente verificadas. No se aceptarán reclamaciones de soluciones escritas a lápiz o que su desarrollo no sea claro. TIEMPO DE LA PRUEBA: 110 min.**

---

### **Problema 1 (3 puntos)**
El principio de Fermat establece que la trayectoria que sigue un rayo de luz entre dos puntos es aquella que corresponde al tiempo mínimo. Use esta idea y el principio variacional para determinar la trayectoria de un rayo de luz entre dos puntos en el plano$xx$si se considera que el medio tiene un índice de refracción$n = c/v$, donde$c$es la rapidez de la luz en el vacío y$v$es la rapidez de la luz en el medio dado por:
$$
n(z) = n_0 - \alpha z, \quad n_0, \alpha > 0.
$$
Bosqueje la trayectoria obtenida. Ayuda:$\int \frac{dx}{\sqrt{\xi^2 - a^2}} = \cosh^{-1}(\xi/a)$.

---

### **Problema 2**
Considere un péndulo de resorte, en el cual una partícula de masa$m$se mueve en el plano$xy$atada a un resorte de constante elástica  $k$y longitud natural$\ell$. El peso actúa en dirección  $-\mathbf{j}$.

La partícula se somete a una fuerza viscosa que es proporcional a la velocidad, es decir$\mathbf{f} = -\mu \mathbf{v}$,$\mu > 0$.

1. **(2 puntos)** Escriba el Lagrangiano del sistema usando las coordenadas más adecuadas para ello.
2. **(2 puntos)** Escriba las componentes de la fuerza generalizada asociada a la fuerza no conservativa. (Recuerde:$Q_j^{NC} = \sum_i \mathbf{f}_i \cdot \frac{\partial \mathbf{q}_i}{\partial q_j}$).
3. **(1 punto)** Encuentre las ecuaciones de movimiento del sistema. No las resuelva.

---

### **Problema 3**
Una partícula de masa $m$ se mueve con velocidad$\dot{\mathbf{r}}$sujeta al potencial
$$
V(\mathbf{r}, \dot{\mathbf{r}}) = U(r) + \mathbf{n} \cdot \mathbf{l},
$$
donde $\mathbf{r}$ es el radio vector medido desde el origen del sistema de referencia, $\mathbf{l}$ es el momento angular con respecto a ese origen, $\mathbf{n}$ es un vector fijo en el espacio y   $U(r)$es una función escalar.

1. **(3 puntos)** Encuentre la fuerza ejercida sobre la partícula.
2. **(2 puntos)** Determine todas las cantidades conservadas. Explique.  
   Ayuda: Podría encontrar útil la identidad:$\nabla (\mathbf{A} \cdot \mathbf{B}) = \mathbf{A} \times (\nabla \times \mathbf{B}) + \mathbf{B} \times (\nabla \times \mathbf{A}) + (\mathbf{A} \cdot \nabla) \mathbf{B} + (\mathbf{B} \cdot \nabla) \mathbf{A}$.

---

### **Problema 4**
A las modificaciones del Lagrangiano que tienen la forma:
$$
L(q, \dot{q}) \longrightarrow L'(q, \dot{q}) = L(q, \dot{q}) + \frac{d}{dt} M(q, t),
$$
se les denomina Transformaciones Gauge.

1. **(2 puntos)** Determine
$$
\frac{d}{dt} \left( \frac{\partial (L' - L)}{\partial \dot{q}_k} \right) - \frac{\partial (L' - L)}{\partial q_k}
$$
y explique qué implicaciones tiene este resultado.
2. **(3 puntos)** Determine las ecuaciones de movimiento que se obtienen a partir de los lagrangianos
   3.$L(q, \dot{q}) = \frac{1}{2} m \dot{q}^2 - \frac{1}{2} m \omega^2 q^2$,
   4.$L'(q, \dot{q}) = \frac{1}{2} m \dot{q}^2 + q \dot{q} - \frac{1}{2} m \omega^2 q^2$.
   ¿Se puede considerar que existe una transformación Gauge entre estos lagrangianos? Explique.

---



---
---
Aquí está tu texto reescrito con notación LaTeX precisa y corregido en los puntos identificados:

---

Dado que la función de potencial depende de la posición y de la velocidad, para obtener la fuerza debemos usar la versión extendida de la fórmula de Euler–Lagrange, en la que la fuerza se obtiene a partir del potencial dependiente de velocidades $V(\mathbf{r},\dot{\mathbf{r}})$ mediante:

$$
\mathbf{F} = -\nabla_{\mathbf{r}} V + \frac{d}{dt}\left(\frac{\partial V}{\partial \dot{\mathbf{r}}}\right).
$$

En nuestro caso, el potencial es:

$$
V(\mathbf{r},\dot{\mathbf{r}}) = U(r) + \mathbf{n} \cdot \mathbf{l},
$$

donde:

$$
\mathbf{l} = \mathbf{r} \times m\dot{\mathbf{r}}.
$$

---

### 1. Cálculo de $\frac{\partial V}{\partial \dot{\mathbf{r}}}$

La parte $U(r)$ no depende de $\dot{\mathbf{r}}$, por lo que su derivada es cero. La segunda parte es:

$$
V_2 = \mathbf{n} \cdot \mathbf{l} = m\, \mathbf{n} \cdot \left(\mathbf{r} \times \dot{\mathbf{r}}\right).
$$

Utilizando la identidad:

$$
\mathbf{n} \cdot \left(\mathbf{r} \times \dot{\mathbf{r}}\right) = \dot{\mathbf{r}} \cdot \left(\mathbf{n} \times \mathbf{r}\right),
$$

podemos escribir:

$$
V_2 = m\, \dot{\mathbf{r}} \cdot \left(\mathbf{n} \times \mathbf{r}\right).
$$

Al derivar con respecto a $\dot{\mathbf{r}}$ (considerando $\mathbf{r}$ y $\mathbf{n}$ fijos) obtenemos:

$$
\frac{\partial V}{\partial \dot{\mathbf{r}}} = m\, \left(\mathbf{n} \times \mathbf{r}\right).
$$

Por lo tanto:

$$
\frac{d}{dt}\left(\frac{\partial V}{\partial \dot{\mathbf{r}}}\right) = m\,\frac{d}{dt}\left(\mathbf{n} \times \mathbf{r}\right).
$$

Dado que $\mathbf{n}$ es constante, se tiene:

$$
\frac{d}{dt}\left(\mathbf{n} \times \mathbf{r}\right) = \mathbf{n} \times \dot{\mathbf{r}},
$$

y en consecuencia:

$$
\frac{d}{dt}\left(\frac{\partial V}{\partial \dot{\mathbf{r}}}\right) = m\, \left(\mathbf{n} \times \dot{\mathbf{r}}\right).
$$

---

### 2. Cálculo de $\nabla_{\mathbf{r}} V$

#### a) Derivada de $U(r)$

Si $r = \|\mathbf{r}\|$, entonces:

$$
\nabla U(r) = U'(r)\,\hat{\mathbf{r}}, \quad \text{con} \quad \hat{\mathbf{r}} = \frac{\mathbf{r}}{r}.
$$

#### b) Derivada de $\mathbf{n} \cdot \mathbf{l}$

Dado que:

$$
\mathbf{l} = \mathbf{r} \times m\dot{\mathbf{r}},
$$

podemos escribir:

$$
V_2 = m\, \mathbf{n} \cdot \left(\mathbf{r} \times \dot{\mathbf{r}}\right).
$$

Al variar $\mathbf{r}$ (manteniendo $\dot{\mathbf{r}}$ fijo) se obtiene:

$$
\delta V_2 = m\, \mathbf{n} \cdot \left(\delta\mathbf{r} \times \dot{\mathbf{r}}\right).
$$

Utilizando la identidad vectorial:

$$
\mathbf{a} \cdot \left(\mathbf{b} \times \mathbf{c}\right) = \mathbf{b} \cdot \left(\mathbf{c} \times \mathbf{a}\right),
$$

podemos escribir:

$$
\delta V_2 = m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right) \cdot \delta\mathbf{r}.
$$

Por definición, el gradiente es el vector que satisface $\delta V_2 = \left(\nabla V_2\right) \cdot \delta \mathbf{r}$, de modo que:

$$
\nabla_{\mathbf{r}} V_2 = m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).
$$

#### c) Resultado total

Por lo tanto, la derivada completa con respecto a $\mathbf{r}$ es:

$$
\nabla_{\mathbf{r}} V = U'(r)\,\hat{\mathbf{r}} + m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).
$$

---

### 3. Cálculo de la fuerza

Sustituyendo en la ecuación de la fuerza:

$$
\mathbf{F} = -\left[U'(r)\,\hat{\mathbf{r}} + m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right)\right] + m\, \left(\mathbf{n} \times \dot{\mathbf{r}}\right).
$$

Recordemos que el producto vectorial es anticomutativo:

$$
\mathbf{n} \times \dot{\mathbf{r}} = -\dot{\mathbf{r}} \times \mathbf{n}.
$$

Por lo tanto:

$$
m\, \left(\mathbf{n} \times \dot{\mathbf{r}}\right) = -m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).
$$

Sustituyendo en la expresión para $\mathbf{F}$:

$$
\mathbf{F} = -U'(r)\,\hat{\mathbf{r}} - m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right) - m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).
$$

Es decir:

$$
\mathbf{F} = -U'(r)\,\hat{\mathbf{r}} - 2m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).
$$

---

### 4. Interpretación y Conclusión

El primer término, $-U'(r)\,\hat{\mathbf{r}}$, es el típico término de fuerza central derivado de un potencial $U(r)$.

El segundo término, $-2m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right)$, es inusual porque depende de la velocidad de la partícula de forma lineal y tiene la forma de una "fuerza magnética" (recordando que en la fuerza de Lorentz la parte magnética es $q\,\dot{\mathbf{r}} \times \mathbf{B}$). Aquí aparece un factor $2m$ y depende de la dirección fija $\mathbf{n}$.

En resumen, la fuerza total ejercida sobre la partícula es:

$$
\boxed{\mathbf{F} = -U'(r)\,\frac{\mathbf{r}}{r} - 2m\, \left(\dot{\mathbf{r}} \times \mathbf{n}\right).}
$$

---

**Correcciones clave realizadas:**  
1. Eliminación de llaves `}` redundantes (e.g., en $\hat{\mathbf{r}}$).  
2. Formato consistente para vectores (todas las magnitudes vectoriales en `\mathbf{}`).  
3. Ajuste de paréntesis con `\left(` y `\right)` para escalado automático.  
4. Espaciado con `\,` en términos como $m\, \mathbf{n} \cdot \ldots$.  

¿Necesitas ajustes adicionales o explicaciones sobre algún paso? 😊