
You can increase the flexibility of script-based experiments by using arguments to set variables in the script.

## Working with script arguments

To use parameters in a script, you must use a library such as argparse to read the arguments passed to the script and assign them to variables. For example, the following script reads an argument named --reg-rate, which is used to set the regularization rate hyperparameter for the logistic regression algorithm used to train a model.
```python
from azureml.core import Run

import argparse

import pandas as pd

import numpy as np

import joblib

import os

from sklearn.model_selection import train_test_split

from sklearn.linear_model import LogisticRegression

  

# Get the experiment run context

run = Run.get_context()

  

# Set regularization hyperparameter

parser = argparse.ArgumentParser()

parser.add_argument('--reg-rate', type=float, dest='reg_rate', default=0.01)

args = parser.parse_args()

reg = args.reg_rate

  

# Prepare the dataset

diabetes = pd.read_csv('data.csv')

X, y = data[['Feature1','Feature2','Feature3']].values, data['Label'].values

X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.30)

  

# Train a logistic regression model

model = LogisticRegression(C=1/reg, solver="liblinear").fit(X_train, y_train)

  

# calculate accuracy

y_hat = model.predict(X_test)

acc = np.average(y_hat == y_test)

run.log('Accuracy', np.float(acc))

  

# Save the trained model

os.makedirs('outputs', exist_ok=True)

joblib.dump(value=model, filename='outputs/model.pkl')

  

run.complete()
```

## Passing arguments to an experiment script

To pass parameter values to a script being run in an experiment, you need to provide an **arguments** value containing a list of comma-separated arguments and their values to the **ScriptRunConfig**, like this:

```python
# Create a script config

script_config = ScriptRunConfig(source_directory='training_folder',

                                script='training.py',

                                arguments = ['--reg-rate', 0.1],

                                environment=sklearn_env)
```

Para resolver el problema, podemos usar trigonometría aplicando la relación entre los ángulos de depresión y las distancias desde la cima de la colina hasta los puntos A y B.

  

Llamemos:

- \( $h$ \): altura de la colina (lo que queremos encontrar)

- \( $d_A$ \): distancia horizontal al punto A

- \( $d_B$ \): distancia horizontal al punto B

  

Dado:

- Los ángulos de depresión son 30.2° para el punto A y 22.5° para el punto B.

- La distancia horizontal entre A y B es 75 m.

  

Usamos la tangente para expresar \( h \) en términos de \( $d_A$ \) y \( d_B \):

  

1. Para el punto A:

   $$ \tan(30.2^\circ) = \frac{h}{d_A} $$

  

   Por lo tanto:

   $$ h = d_A \cdot \tan(30.2^\circ) $$

  

2. Para el punto B:

   $$ \tan(22.5^\circ) = \frac{h}{d_B} $$

  

   Por lo tanto:

   $$ h = d_B \cdot \tan(22.5^\circ) $$

  

Dado que \( d_B = d_A + 75 \), podemos igualar las expresiones de \( h \):

  

$$ d_A \cdot \tan(30.2^\circ) = (d_A + 75) \cdot \tan(22.5^\circ) $$

  

Despejamos \( d_A \):

  

$$ d_A (\tan(30.2^\circ) - \tan(22.5^\circ)) = 75 \cdot \tan(22.5^\circ) $$

  

Por lo tanto:

  

$$ d_A = \frac{75 \cdot \tan(22.5^\circ)}{\tan(30.2^\circ) - \tan(22.5^\circ)} $$

  

Una vez calculado \( d_A \), sustituimos en la ecuación para \( h \):

  

$$ h = d_A \cdot \tan(30.2^\circ) $$

  

Vamos a resolver estos cálculos para obtener el valor de \( h \).

  

La altura de la colina es aproximadamente:
$$ h \approx 107.75 \, \text{m} $$