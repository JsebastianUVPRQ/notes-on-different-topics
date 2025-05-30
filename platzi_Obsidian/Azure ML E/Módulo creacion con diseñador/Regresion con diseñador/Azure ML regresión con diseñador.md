Se creará un modelo de regresión en el [[diseñador Azure ML]] con los pasos principales tratados en Auto ML
Puede pensar en los pasos para entrenar y evaluar un modelo de aprendizaje automático de regresión como los siguientes:

1. **Preparar datos**: identifique las características y la etiqueta de un conjunto de datos. Procese previamente o limpie y transforme los datos según sea necesario.
2. **Entrenar el modelo**: divida los datos en dos grupos, un conjunto de entrenamiento y uno de validación. Entrene un modelo de Machine Learning con el conjunto de datos de entrenamiento. Pruebe el modelo de Machine Learning en cuanto al rendimiento con el conjunto de datos de validación.
3. **Evaluar el rendimiento**: compare la proximidad de las predicciones del modelo con las etiquetas conocidas.
4. **Implementar un servicio predictivo**: después de entrenar un modelo de Machine Learning, debe convertir la canalización de entrenamiento en una canalización de inferencia en tiempo real. A continuación, puede implementar el modelo como una aplicación en un servidor o dispositivo para que otros usuarios puedan usarlo.

Sigamos estos cuatro pasos a medida que aparecen en el diseñador de Azure.

## LINK-Taller Explore regression with Azure Machine Learning Designer: [Step-by-step tutorial](https://microsoftlearning.github.io/AI-900-AIFundamentals/instructions/02a-create-regression-model.html)
## Preparación de los datos

El diseñador de Azure Machine Learning tiene varios componentes integrados que se pueden usar para preparar los datos para el entrenamiento. Estos componentes permiten limpiar datos, normalizar características, combinar tablas, etc. ![Captura de pantalla de los componentes del diseñador que se pueden usar para preparar los datos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/prepare-data-example.png)

## Entrenamiento de un modelo

Para entrenar un modelo de regresión, necesita un conjunto de datos que incluya _características_ históricas, características de la entidad para la que quiere realizar una predicción y valores de _etiqueta_ conocidos. La etiqueta es la cantidad que quiere para entrenar un modelo que va a predecir.

Es habitual entrenar el modelo con un subconjunto de los datos, a la vez que se retienen algunos con los que probar el modelo entrenado. Esto le permite comparar las etiquetas que predice el modelo con las etiquetas conocidas reales del conjunto de datos original.

Usará el componente **Puntuar modelo** del _diseñador_ para generar el valor de etiqueta de clase predicho. Una vez que conecte todos los componentes, querrá ejecutar un experimento, que usará el recurso de datos en el lienzo para entrenar y puntuar un modelo.

![Captura de pantalla de los componentes del diseñador que se pueden conectar para entrenar un modelo de regresión.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/train-model-example.png)

## Evaluación del rendimiento

Después de entrenar un modelo, es importante evaluar su rendimiento. Hay muchas métricas de rendimiento y metodologías para evaluar el rendimiento de las predicciones de un modelo. Para revisar las métricas de evaluación en la página del trabajo completado, haga clic con el botón derecho en el componente **Evaluar modelo**.

![Captura de pantalla de hacer un clic con el botón derecho en el modelo de evaluación en trabajos completados para ver los resultados de la evaluación.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/evaluate-model-example.png)

- **Error medio absoluto (EAM)**: la diferencia media entre los valores pronosticados y los reales. Este valor se basa en las mismas unidades que la etiqueta, en este caso, dólares. Cuanto menor sea este valor, mejor será la predicción del modelo.
- **Raíz del error cuadrático medio (RECM)**: raíz cuadrada de la diferencia cuadrática media entre valores predichos y verdaderos. El resultado es una métrica basada en la misma unidad que la etiqueta (dólares). En comparación con el valor EAM (anterior), una diferencia mayor indica una mayor desviación en los errores individuales (por ejemplo, algunos errores son muy pequeños, mientras que otros son grandes).
- **Error cuadrático relativo (ESR)**: una métrica relativa entre 0 y 1 en función del cuadrado de las diferencias entre los valores pronosticados y los reales. Cuanto más cercano a 0 sea el valor de esta métrica, mejor funciona el modelo. Como esta métrica es relativa, se puede usar para comparar modelos en los que las etiquetas se encuentran en unidades distintas.
- **Error absoluto relativo (EAR)**: una métrica relativa entre 0 y 1 en función de las diferencias absolutas entre los valores pronosticados y los reales. Cuanto más cercano a 0 sea el valor de esta métrica, mejor funciona el modelo. Al igual que ESR, esta métrica se puede usar para comparar modelos en los que las etiquetas se encuentran en unidades distintas.
- **Coeficiente de determinación (R2)**: esta métrica se suele denominar _R cuadrado_ y resume la cantidad de la varianza entre los valores reales y los previstos que se explica en el modelo. Cuanto más cercano a 1 sea esta valor, mejor funciona el modelo.

## Implementación de un servicio predictivo
[Comprensión de los pasos para la regresión - Training | Microsoft Learn](https://learn.microsoft.com/es-es/training/modules/create-regression-model-azure-machine-learning-designer/5-regression-steps)

Tiene la capacidad de implementar un servicio que se puede usar en tiempo real. Para automatizar el modelo en un servicio que realice predicciones conti
nuas, debe crear e implementar una canalización de inferencia.

#### Canalización de inferencia

Para implementar la canalización, antes debe convertir la canalización de entrenamiento en una canalización de inferencia en tiempo real. Este proceso quita los componentes de entrenamiento y agrega entradas y salidas de servicios web para administrar las solicitudes.

La canalización de inferencia realiza las mismas transformaciones de datos que la primera canalización para los datos _nuevos_. Después, usa el modelo entrenado para _deducir_ o predecir valores de etiqueta en función de sus características. Este modelo formará la base de un servicio predictivo que puede publicar para que lo usen las aplicaciones.

Para crear una canalización de inferencia, seleccione el menú situado encima de un trabajo completado. ![Captura de pantalla de las opciones de la canalización de inferencia en el panel de trabajos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/inference-pipeline-example.png)

#### Implementación

Después de crear la canalización de inferencia, puede implementarla como un punto de conexión. En la página Puntos de conexión, puede ver los detalles de implementación, probar el servicio de canalización con datos de ejemplo y buscar credenciales para conectar el servicio de canalización a una aplicación cliente.

El punto de conexión tardará un tiempo en implementarse. El estado de implementación de la pestaña **Detalles** indicará _Correcto_ cuando la implementación se realice correctamente.

![Captura de pantalla de la página Puntos de conexión de un modelo implementado correctamente.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/endpoints-example-1.png)
En la pestaña **Prueba**, puede probar el servicio implementado con datos de ejemplo en formato JSON. La pestaña Prueba es una herramienta que puede usar para comprobar rápidamente si el modelo se comporta según lo previsto. Normalmente, resulta útil probar el servicio antes de conectarlo a una aplicación.

![Captura de pantalla de la pestaña Prueba en la página Puntos de conexión.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/endpoints-example-3.png)

Puede encontrar las credenciales para el servicio en la pestaña **Consumir**. Estas credenciales se usan para conectar el modelo de Machine Learning entrenado como un servicio a una aplicación cliente.

![Captura de pantalla en la que se muestra dónde encontrar la clave y el punto de conexión en la pestaña Consumo.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-regression-model-azure-machine-learning-designer/media/endpoints-example-2.png)

