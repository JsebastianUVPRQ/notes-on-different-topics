La funcionalidad de aprendizaje automático automatizado de Azure Machine Learning admite modelos de Machine Learning _supervisados_, es decir, modelos para los que los datos de entrenamiento incluyen valores de etiqueta conocidos. Puede usar el aprendizaje automático automatizado a fin de entrenar modelos para:

- **Clasificación** (predicción de categorías o _clases_)
- **Regresión** (predicción de valores numéricos)
- **Previsión de series temporales** (predicción de valores numéricos en un momento futuro en el tiempo)

En el aprendizaje automático automatizado puede seleccionar varios tipos de tareas:
![[Pasted image 20230808194754.png]]

En el aprendizaje automático automatizado puede seleccionar configuraciones para la métrica principal, el tipo de modelo que se usa para el entrenamiento, los criterios de salida y los límites de simultaneidad.
![[Pasted image 20230808194815.png]]

Lo importante es que AutoML dividirá los datos en un conjunto de entrenamiento y un conjunto de validación. Puede configurar los detalles en la configuración antes de ejecutar el trabajo.