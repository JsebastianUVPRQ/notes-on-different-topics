## **K-fold Cross Validation - (Validación Cruzada de k pliegues)**

La validación cruzada de k pliegues es una técnica comúnmente utilizada en el aprendizaje automático para evaluar y seleccionar modelos de manera robusta. Consiste en dividir el conjunto de datos en k pliegues o partes de tamaño aproximadamente igual.

El proceso de k-fold cross validation se puede resumir en los siguientes pasos:

1. Se divide el conjunto de datos en k pliegues o partes de tamaño similar.
2. Se selecciona uno de los pliegues como conjunto de validación y los restantes k-1 pliegues se utilizan como conjunto de entrenamiento.
3. Se entrena el modelo utilizando los datos del conjunto de entrenamiento y se evalúa su rendimiento utilizando el conjunto de validación.
4. Se repiten los pasos 2k y 3k veces, de manera que cada pliegue se haya utilizado una vez como conjunto de validación.
5. Se calcula el promedio de las métricas de rendimiento obtenidas en cada iteración, lo que proporciona una estimación más confiable del rendimiento del modelo.
6. Se repite el proceso con diferentes divisiones de pliegues, y se obtiene un promedio de las métricas de rendimiento para obtener una evaluación más robusta del modelo.

La validación cruzada de k pliegues es útil cuando se dispone de un conjunto de datos limitado y se busca obtener una estimación más precisa del rendimiento del modelo. Permite evaluar el modelo en datos no vistos y reducir el sesgo en la estimación del rendimiento al utilizar diferentes combinaciones de conjuntos de entrenamiento y validación.

- - - 
## **Validación cruzada leave-one-out (LOOCV)**:
es un enfoque de validación cruzada que se utiliza para evaluar modelos cuando se dispone de un conjunto de datos relativamente pequeño. En LOOCV, se utiliza cada punto de datos individualmente como conjunto de validación, mientras que el resto de los datos se utilizan para entrenar el modelo.

El proceso de validación cruzada leave-one-out se puede resumir en los siguientes pasos:

1. Se selecciona un punto de datos como conjunto de validación.
2. El modelo se entrena utilizando los datos restantes, es decir, todos los puntos excepto el punto de validación seleccionado.
3. Se evalúa el modelo utilizando el punto de validación y se registra la métrica de rendimiento correspondiente.
4. Se repiten los pasos 1-3 para cada punto de datos en el conjunto de datos, es decir, se realiza un ciclo completo de entrenamiento y evaluación para cada punto de datos individual.
5. Se calcula el promedio de las métricas de rendimiento obtenidas para obtener una estimación general del rendimiento del modelo.

El término "leave-one-out" se refiere al hecho de que en cada iteración, se deja fuera un único punto de datos como conjunto de validación. Dado que este enfoque utiliza todos los puntos de datos disponibles, es especialmente útil cuando el tamaño del conjunto de datos es pequeño y se desea aprovechar al máximo la información disponible.
Una ventaja clave de LOOCV es que **proporciona una estimación no sesgada del rendimiento del modelo**, ya que utiliza todos los puntos de datos en el conjunto de datos para evaluar el modelo en cada iteración. 
**Sin embargo, LOOCV puede ser computacionalmente costoso** cuando se tienen grandes conjuntos de datos, ya que requiere entrenar y evaluar el modelo tantas veces como puntos de datos haya.