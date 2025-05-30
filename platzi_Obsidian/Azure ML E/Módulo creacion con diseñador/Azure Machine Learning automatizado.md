Azure Machine Learning incluye capacidad de aprendizaje automático automatizado que prueba diversas técnicas de procesamiento previo y algoritmos de entrenamiento de modelos en paralelo. Utiliza la potencia del procesamiento en la nube para encontrar el mejor modelo de Machine Learning supervisado para los datos. 
El aprendizaje automático automatizado permite entrenar modelos sin amplio conocimiento de programación o ciencia de datos. Para aquellos con conocimientos en estas áreas, ahorra tiempo y recursos al automatizar la selección de algoritmos y la optimización de hiperparámetros.
![[Pasted image 20230808012235.png]]
En Azure Machine Learning, las operaciones que se ejecutan se denominan _trabajos_. Puede configurar varias opciones para el trabajo antes de iniciar una ejecución de aprendizaje automático automatizado. La configuración de ejecución proporciona la información necesaria para especificar el script de entrenamiento, el destino de proceso y el entorno de Azure ML en la configuración de ejecución y ejecutar un trabajo de entrenamiento.

![[Pasted image 20230808012359.png]]

# Proceso Azure AutoML
Puede pensar en los pasos de un proceso de aprendizaje automático como:

1. **Preparar datos**: identifique las características y la etiqueta de un conjunto de datos. Procese previamente o limpie y transforme los datos según sea necesario.
2. **Entrenar el modelo**: divida los datos en dos grupos, un conjunto de entrenamiento y uno de validación. Entrene un modelo de Machine Learning con el conjunto de datos de entrenamiento. Pruebe el modelo de Machine Learning en cuanto al rendimiento con el conjunto de datos de validación.
3. **Evaluar el rendimiento**: compare la proximidad de las predicciones del modelo con las etiquetas conocidas.
4. **Implementar un servicio predictivo**: después de entrenar un modelo de Machine Learning, puede implementar el modelo como una aplicación en un servidor o dispositivo para que otros usuarios puedan usarlo.

Estos son los mismos pasos del proceso de aprendizaje automático automatizado con Azure Machine Learning.