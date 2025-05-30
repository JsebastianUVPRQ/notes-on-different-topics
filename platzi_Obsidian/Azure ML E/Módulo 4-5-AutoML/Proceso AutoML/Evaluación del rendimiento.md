Después de completar el trabajo, se revisa el modelo de mejor rendimiento utilizando criterios de salida para detener el proceso. Sin embargo, el "mejor" modelo obtenido puede no ser el mejor posible, sino simplemente el mejor dentro del tiempo permitido. La evaluación del mejor modelo se basa en la métrica de evaluación, en este caso, el error cuadrático medio normalizado (NRMSE).

La métrica se calcula mediante validación cruzada, que divide los datos en partes de entrenamiento y prueba. Los valores previstos se comparan con los valores reales para calcular los errores o residuos. El error se mide mediante la raíz del error cuadrático medio (RMSE), que se normaliza para comparar modelos con diferentes escalas utilizando el NRMSE.

El histograma de valores residuales muestra la frecuencia de los errores. Los errores pequeños son preferibles y se esperan valores residuales alrededor de cero, indicando una buena predicción del modelo. Sin embargo, valores residuales extremos indican errores en los extremos de la escala que el modelo no puede explicar.
![[Pasted image 20230808212352.png]]

El gráfico **Valores previstos frente a los reales** debe mostrar una tendencia diagonal en la que el valor previsto se correlacione estrechamente con el valor verdadero. La línea de puntos muestra cómo debe realizarse un modelo perfecto. Cuanto más se acerque la línea del valor previsto promedio del modelo a la línea de puntos, mejor será su rendimiento. Un histograma debajo del gráfico de líneas muestra la distribución de los valores verdaderos.
![[Pasted image 20230808212417.png]]

## Implementación de servicio predictivo

En Azure Machine Learning, puede implementar un servicio como una instancia de Azure Container Instances (ACI) o en un clúster de Azure Kubernetes Service (AKS). En escenarios de producción, se recomienda una implementación de AKS, para lo cual debe crear un destino de proceso de _clúster de inferencia_. En este ejercicio usará un servicio ACI, que es un destino de implementación adecuado para las pruebas y no requiere la creación de un clúster de inferencia