# Preparación de los datos
## LINK-Taller Explore clustering with Azure Machine Learning Designer [step-by-step clustering tutorial](https://microsoftlearning.github.io/AI-900-AIFundamentals/instructions/02b-create-classification-model.html)
El diseñador de Azure Machine Learning tiene varios componentes creados previamente que se pueden usar para preparar los datos para el entrenamiento. Estos componentes permiten limpiar datos, normalizar características, combinar tablas, etc. ![Captura de pantalla de los componentes del diseñador que se pueden usar para preparar los datos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/prepare-data-example.png)

# Entrenamiento de un modelo

Para entrenar un modelo de clasificación, necesita un conjunto de datos que incluya _características_ históricas, características de la entidad para la que quiere realizar una predicción y valores de _etiqueta_ conocidos. La etiqueta es el indicador de clase que quiere para entrenar un modelo para predecir.

Es habitual entrenar el modelo con un subconjunto de los datos, a la vez que se retienen algunos con los que probar el modelo entrenado. Esto le permite comparar las etiquetas que predice el modelo con las etiquetas conocidas reales del conjunto de datos original.

Usará el componente **Puntuar modelo** del _diseñador_ para generar el valor de etiqueta de clase predicho. Una vez que conecte todos los componentes, querrá ejecutar un experimento, que usará el recurso de datos del lienzo para entrenar y puntuar un modelo.

![Captura de pantalla de los componentes del diseñador que se pueden conectar para entrenar un modelo de clasificación.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/classification-train-model-example.png)

## Evaluación del rendimiento

Después de entrenar un modelo, es importante evaluar su rendimiento. Hay muchas métricas de rendimiento y metodologías para evaluar el rendimiento de las predicciones de un modelo. Para revisar las métricas de evaluación en la página del trabajo completado, haga clic con el botón derecho en el componente **Evaluar modelo**.

![Captura de pantalla de hacer un clic con el botón derecho en el modelo de evaluación en los trabajos completados para ver los resultados de la evaluación.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/evaluate-model-example.png)

#### Matriz de confusión

La matriz de confusión es una herramienta que se usa para evaluar la calidad de las predicciones de un modelo de clasificación. Compara las etiquetas predichas con las etiquetas reales.

En un modelo de clasificación binaria en el que se predice uno de dos valores posibles, la matriz de confusión es una cuadrícula de 2x2 en la que se muestran los recuentos de los valores previstos y reales de las clases **1** y **0**. Clasifica los resultados del modelo en cuatro tipos de resultados. Con nuestro ejemplo de diabetes, estos resultados pueden ser similares a los siguientes:

- _Verdadero positivo_: el modelo predice que el paciente tiene diabetes y el paciente realmente la tiene.
- _Falso positivo_: el modelo predice que el paciente tiene diabetes, pero el paciente realmente no la tiene.
- _Falso negativo_: el modelo predice que el paciente no tiene diabetes, pero el paciente realmente la tiene.
- _Verdadero negativo_: el modelo predice que el paciente no tiene diabetes y el paciente realmente no la tiene.

![Captura de pantalla de los términos de una matriz de confusión que muestran verdaderos y falsos positivos, así como verdaderos y falsos negativos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/confusion-matrix-terms.png)

Supongamos que tiene datos para 100 pacientes. Crea un modelo que predice que un paciente tiene diabetes el 15 % del tiempo, por lo que _predice_ que 15 personas tienen diabetes y _predice_ que 85 personas no tienen. En realidad, supongamos que 25 personas _realmente_ la tienen y 75 personas _realmente_ no la tienen. Esta información se puede presentar en una matriz de confusión como la siguiente:

![Captura de pantalla de una matriz de confusión en la que se muestran los recuentos de valores reales y previstos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/confusion-matrix.png)

En un modelo de clasificación de varias clases (donde hay más de dos clases posibles), se usa el mismo enfoque para mostrar en formato de tabla cada combinación posible de recuentos de valores reales y previstos; por tanto, un modelo con tres clases posibles daría como resultado una matriz de 3x3 con una línea diagonal de celdas en las que las etiquetas previstas y reales coincidan.

Entre las métricas que se pueden derivar de la matriz de confusión, se encuentran las siguientes:

- **Exactitud**: el número de predicciones correctas (verdaderos positivos y verdaderos negativos) dividido por el número total de predicciones.
- **Precisión**: el número de casos clasificados como positivos que lo son realmente (el número de verdaderos positivos dividido por el de verdaderos positivos más los falsos positivos).
- **Coincidencia**: la fracción de casos positivos identificados correctamente (el número de verdaderos positivos dividido por el de verdaderos positivos más los falsos negativos).
- **Puntuación F1**: métrica general que básicamente combina la precisión y la coincidencia.

De estas métricas, la _exactitud_ puede ser la más intuitiva. Sin embargo, debe tener cuidado al usar la precisión como medida del funcionamiento correcto de un modelo. Con el modelo que predice que el 15 % de los pacientes tienen diabetes cuando en realidad el 25 % de los pacientes la tienen podemos calcular las métricas siguientes:

La _exactitud_ del modelo es la siguiente: (10+70)/ 100 = 80 %.

La _precisión_ del modelo es la siguiente: 10/(10+5) = 67 %.

La _coincidencia_ del modelo es 10/(10+15) = 40 %

#### Selección de un umbral

Un modelo de clasificación predice la probabilidad de cada clase posible. En otras palabras, el modelo calcula una probabilidad para cada etiqueta predicha. En el caso de un modelo de clasificación binaria, la probabilidad de una predicción es un valor comprendido entre 0 y 1. De manera predeterminada, una probabilidad de predicción _igual o superior_ a 0,5 da como resultado una predicción de clase de 1, mientras que una predicción _por debajo_ de este umbral significa que hay una mayor probabilidad de una predicción _negativa_ (recuerde que las probabilidades de todas las clases suman 1), por lo que la clase pronosticada sería 0.

El diseñador tiene un _control deslizante para el umbral_ que resulta útil para revisar cómo cambiaría el rendimiento del modelo en función del umbral establecido. ![Captura de pantalla del control deslizante para el umbral en los resultados del módulo Evaluar.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/threshold-example.png)

#### Curva ROC y métrica AUC

Otro término para la _coincidencia_ es la **tasa de verdaderos positivos**, que tiene una métrica correspondiente denominada **tasa de falsos positivos**, que mide el número de casos negativos que se han identificado incorrectamente como positivos en comparación con el número de casos negativos reales. Trazar estas métricas entre sí para cada valor del umbral posible entre 0 y 1 da como resultado una curva, conocida como **curva ROC** (ROC significa _característica operativa del receptor_, pero la mayoría de los científicos de datos simplemente la llaman curva ROC). En un modelo ideal, la curva ascendería por el lado izquierdo y discurriría por la parte superior, para cubrir todo el área del gráfico. Cuanto mayor sea el _área bajo la curva_ de la métrica **AUC** (que puede ser cualquier valor comprendido entre 0 y 1), mejor será el rendimiento del modelo. Puede revisar la curva ROC en **Resultados de la evaluación**.

![Captura de pantalla de la curva ROC encontrada mediante la vista previa de los resultados del módulo Evaluar.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/roc-curve-example.png)

# Implementación de un servicio predictivo

Tiene la capacidad de implementar un servicio que se puede usar en tiempo real. Para automatizar el modelo en un servicio que realice predicciones continuas, debe crear e implementar una canalización de inferencia.

#### Canalización de inferencia

Para implementar la canalización, antes debe convertir la canalización de entrenamiento en una canalización de inferencia en tiempo real. Este proceso quita los componentes de entrenamiento y agrega entradas y salidas de servicios web para administrar las solicitudes.

La canalización de inferencia realiza las mismas transformaciones de datos que la primera canalización para los datos _nuevos_. Después, usa el modelo entrenado para _deducir_ o predecir valores de etiqueta en función de sus características. Este modelo formará la base de un servicio predictivo que puede publicar para que lo usen las aplicaciones.

Para crear una canalización de inferencia, seleccione el menú situado encima de un trabajo completado. ![Captura de pantalla de las opciones de la canalización de inferencia en el panel de trabajos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/inference-pipeline-example.png)

#### Implementación

Después de crear la canalización de inferencia, puede implementarla como un punto de conexión. En la página Puntos de conexión, puede ver los detalles de implementación, probar el servicio de canalización con datos de ejemplo y buscar credenciales para conectar el servicio de canalización a una aplicación cliente.

El punto de conexión tardará un tiempo en implementarse. El estado de implementación de la pestaña **Detalles** indicará _Correcto_ cuando la implementación se realice correctamente.

![Captura de pantalla de la página Puntos de conexión de un modelo implementado correctamente.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/endpoints-example-1.png)

En la pestaña **Prueba**, puede probar el servicio implementado con datos de ejemplo en formato JSON. La pestaña Prueba es una herramienta que puede usar para comprobar rápidamente si el modelo se comporta según lo previsto. Normalmente, resulta útil probar el servicio antes de conectarlo a una aplicación.

![Captura de pantalla de la pestaña Prueba en la página Puntos de conexión.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/diabetes-endpoints-example-3.png)

Puede encontrar las credenciales para el servicio en la pestaña **Consumir**. Estas credenciales se usan para conectar el modelo de Machine Learning entrenado como un servicio a una aplicación cliente.

![Captura de pantalla en la que se muestra dónde encontrar la clave y el punto de conexión en la pestaña Consumir.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-classification-model-azure-machine-learning-designer/media/endpoints-example-2.png)

- **Accuracy**: The ratio of correct predictions (true positives + true negatives) to the total number of predictions. In other words, what proportion of diabetes predictions did the model get right? 
    
- **Precision**: The fraction of positive cases correctly identified (the number of true positives divided by the number of true positives plus false positives). In other words, out of all the patients that the model predicted as having diabetes, how many are actually diabetic? 
    
- **Recall**: The fraction of the cases classified as positive that are actually positive (the number of true positives divided by the number of true positives plus false negatives). In other words, out of all the patients who actually have diabetes, how many did the model identify? 
    
- **F1 Score**: An overall metric that essentially combines precision and recall. 
    
- _We'll return to_ _**AUC**_ _later_.



