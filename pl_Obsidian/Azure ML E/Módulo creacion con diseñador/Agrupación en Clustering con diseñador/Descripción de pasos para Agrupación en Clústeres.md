Puede pensar en los pasos para entrenar y evaluar un modelo de Machine Learning de agrupación en clústeres como los siguientes:

1. **Preparar los datos**: identifique las características de un conjunto de datos. Procese previamente o limpie y transforme los datos según sea necesario.
2. **Entrenar el modelo**: divida los datos en dos grupos, un conjunto de entrenamiento y uno de validación. Entrene un modelo de Machine Learning con el conjunto de datos de entrenamiento. Pruebe el modelo de Machine Learning en cuanto al rendimiento con el conjunto de datos de validación.
3. **Evaluar el rendimiento**: estas métricas pueden ayudar a los científicos de datos a evaluar lo bien que el modelo separa los clústeres.
4. **Implementar un servicio predictivo**: después de entrenar un modelo de Machine Learning, debe convertir la canalización de entrenamiento en una canalización de inferencia en tiempo real. A continuación, puede implementar el modelo como una aplicación en un servidor o un dispositivo para que otros usuarios puedan usarlo.

Vamos a seguir estos cuatro pasos a medida que aparecen en el diseñador de Azure.
## LINK-Taller Explore Agrupación en Clustering with Azure Machine Learning Designer: [step-by-step tutorial](https://microsoftlearning.github.io/AI-900-AIFundamentals/instructions/02c-create-clustering-model.html)

## Preparación de los datos

Para entrenar un modelo de agrupación en clústeres, necesita un conjunto de datos que incluya varias observaciones de los elementos que quiere agrupar, incluidas las características numéricas que se pueden usar para determinar las similitudes entre los casos individuales que ayudarán a separarlos en clústeres.

El diseñador de Azure Machine Learning tiene varios componentes creados previamente que se pueden usar para preparar los datos para el entrenamiento. Estos componentes permiten limpiar datos, normalizar características, combinar tablas, etc. ![Captura de pantalla de los componentes del diseñador que se pueden usar para preparar los datos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/prepare-data-example.png)

## Entrenamiento de un modelo

Para entrenar un modelo de agrupación en clústeres, debe aplicar un algoritmo de agrupación en clústeres a los datos, usando solamente las características que ha seleccionado para la agrupación en clústeres. Entrenará el modelo con un subconjunto de los datos y usará el resto para probar el modelo entrenado.

El algoritmo de la **agrupación en clústeres [[k-means clustering]]** agrupa los elementos en el número de clústeres, o centroides, que especifique, un valor que se conoce como _**K**_.


Usará el componente _Assign Data to Clusters_ (Asignar datos a los clústeres) del **diseñador** para agrupar los datos en clústeres. Una vez que conecte todos los componentes, querrá ejecutar un experimento, que usará el recurso de datos del lienzo para entrenar un modelo.

![Captura de pantalla de los componentes del diseñador que se pueden conectar para entrenar un modelo de clasificación.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/train-model-example.png)

## Evaluación del rendimiento

Después de entrenar un modelo, es importante evaluar su rendimiento. Hay muchas métricas de rendimiento y metodologías para evaluar el rendimiento de las predicciones de un modelo. Para revisar las métricas de evaluación en la página del trabajo completado, haga clic con el botón derecho en el componente **Evaluar modelo**.

![Captura de pantalla de hacer un clic con el botón derecho en el modelo de evaluación en los trabajos completados para ver los resultados de la evaluación.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/evaluate-model-example.png)

Cuando se haya completado la ejecución del experimento, seleccione **Detalles del trabajo**. Haga clic con el botón derecho en el módulo **Evaluar modelo** y seleccione **Vista previa de los datos** y, a continuación, **Resultados de la evaluación**. Estas métricas pueden ayudar a los científicos de datos a evaluar el grado de separación de los clústeres. Incluyen una fila de métricas para cada clúster y una fila de resumen para una evaluación combinada. Las métricas de cada fila son las siguientes:

- **Distancia media a otro centro**: esto indica la proximidad media de cada punto del clúster a los centroides de todos los demás clústeres.
- **Distancia media al centro del clúster**: esto indica la proximidad media de cada punto del clúster al centroide del clúster.
- **Número de puntos**: número de puntos asignados al clúster.
- **Distancia máxima al centro del clúster**: máximo de las distancias entre cada punto y el centroide del clúster de ese punto. Si este número es alto, el clúster puede estar ampliamente disperso. Esta estadística, combinada con la **Distancia media al centro de clústeres**, le ayuda a determinar la _distribución_ del clúster.

## Implementación de un servicio predictivo

Tiene la capacidad de implementar un servicio que se puede usar en tiempo real. Para automatizar el modelo en un servicio que realice predicciones continuas, debe crear e implementar una canalización de inferencia.

#### Canalización de inferencia

Para implementar la canalización, antes debe convertir la canalización de entrenamiento en una canalización de inferencia en tiempo real. Este proceso quita los componentes de entrenamiento y agrega entradas y salidas de servicios web para administrar las solicitudes.

La canalización de inferencia realiza las mismas transformaciones de datos que la primera canalización para los datos _nuevos_. Después, se usa el modelo entrenado para realizar _deducciones_ o predicciones en función de sus características. Este modelo formará la base de un servicio predictivo que puede publicar para que lo usen las aplicaciones.

Para crear una canalización de inferencia, seleccione el menú situado encima de un trabajo completado. ![Captura de pantalla de las opciones de la canalización de inferencia en el panel de trabajos.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/inference-pipeline-example.png)

#### Implementación

Después de crear la canalización de inferencia, puede implementarla como un punto de conexión. En la página Puntos de conexión, puede ver los detalles de implementación, probar el servicio de canalización con datos de ejemplo y buscar credenciales para conectar el servicio de canalización a una aplicación cliente.

El punto de conexión tardará un tiempo en implementarse. El estado de implementación de la pestaña **Detalles** indicará _Correcto_ cuando la implementación se realice correctamente.

![Captura de pantalla de la página Puntos de conexión de un modelo implementado correctamente.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/endpoints-example-1.png)

En la pestaña **Prueba**, puede probar el servicio implementado con datos de ejemplo en formato JSON. La pestaña Prueba es una herramienta que puede usar para comprobar rápidamente si el modelo se comporta según lo previsto. Normalmente, resulta útil probar el servicio antes de conectarlo a una aplicación.

![Captura de pantalla de la pestaña Prueba en la página Puntos de conexión.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/endpoints-example-3.png)

Puede encontrar las credenciales para el servicio en la pestaña **Consumir**. Estas credenciales se usan para conectar el modelo de Machine Learning entrenado como un servicio a una aplicación cliente.

![Captura de pantalla en la que se muestra dónde encontrar la clave y el punto de conexión en la pestaña Consumir.](https://learn.microsoft.com/es-es/training/wwl-data-ai/create-clustering-model-azure-machine-learning-designer/media/endpoints-example-2.png)

## Comprobación de conocimientos
1. Está usando una canalización del diseñador de Azure Machine Learning para entrenar y probar un modelo de agrupación en clústeres K-means. Quiere que el modelo asigne elementos a uno de los tres clústeres. ¿Qué propiedad de la configuración del módulo de agrupación en clústeres K-means debe establecer para lograrlo?

a. Establecer el número de centroides en 3

CORRECTO. Para crear clústeres K, debe establecer el número de centroides en K.

b. Establecer la inicialización del número aleatorio en 3   INCORRECTO

c. Establecer las iteraciones en 3      INCORRECTO

2. Usa el diseñador de Azure Machine Learning para crear una canalización de entrenamiento para un modelo de agrupación en clústeres. Ahora quiere usar el modelo en una canalización de inferencia. ¿Qué módulo debe usar para deducir las predicciones de clúster del modelo?


a. Puntuación de modelo  --- INCORRECTO

b. Asignación de datos a clústeres

CORRECTO. Use el módulo de asignación de datos a clústeres para generar predicciones de clústeres a partir de un modelo de agrupación en clústeres entrenado.

c. Entrenamiento del modelo de agrupación en clústeres      --- INCORRECTO