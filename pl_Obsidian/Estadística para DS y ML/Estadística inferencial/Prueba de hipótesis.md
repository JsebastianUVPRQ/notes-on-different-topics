## Definición
La **prueba de hipótesis** es un proceso estadístico utilizado para evaluar la validez de una afirmación o hipótesis sobre una población o conjunto de datos. Se utiliza para tomar decisiones basadas en evidencia empírica y proporciona un marco formal para realizar inferencias y sacar conclusiones sobre una población más amplia a partir de una muestra.
El proceso de prueba de hipótesis generalmente sigue los siguientes pasos:
	
1. **Formulación de hipótesis**: Se establecen **dos** hipótesis: la **hipótesis nula (H0)** y la **hipótesis alternativa (H1)**. La hipótesis nula establece que no hay diferencia o efecto real en la población, mientras que la hipótesis alternativa plantea la existencia de una diferencia o efecto específico.
    
2. **Selección del nivel de significancia**: Se determina el nivel de significancia, generalmente denotado como α (alfa), que representa el grado de confianza necesario para rechazar la hipótesis nula. El nivel de significancia es una medida de cuán improbable debe ser el resultado observado bajo la hipótesis nula para rechazarla.
    
3. **Recopilación y análisis de datos**: Se obtiene una muestra representativa de la población y se realizan cálculos y análisis estadísticos adecuados para evaluar la evidencia empírica.
    
4. **Cálculo del estadístico de prueba**: Se calcula un estadístico de prueba basado en los datos de la muestra y se compara con una distribución de probabilidad conocida bajo la hipótesis nula.
    
5. **Toma de decisión**: Se compara el valor del estadístico de prueba con un valor crítico o se utiliza un enfoque basado en el [[p-valor]] para determinar si se rechaza o no la hipótesis nula. Si el valor del estadístico de prueba es menor que el valor crítico o el p-valor es menor que el nivel de significancia, se rechaza la hipótesis nula a favor de la hipótesis alternativa. En caso contrario, no se rechaza la hipótesis nula.
    
6. **Interpretación de resultados**: Se interpretan los resultados en el contexto del problema o la pregunta de investigación. Si se rechaza la hipótesis nula, se concluye que hay evidencia suficiente para respaldar la hipótesis alternativa. Si no se rechaza la hipótesis nula, no se encuentran pruebas suficientes para afirmar la hipótesis alternativa.

## Resumen visual de la definición
![[Statistical_test_HipoProve.png]]
## Tipos de pruebas de hipótesis
Los distintos tipos de pruebas de hipótesis se utilizan en diferentes situaciones y contextos estadísticos para evaluar afirmaciones sobre parámetros poblacionales o características de una muestra. A continuación, se presenta una breve explicación de los tipos comunes de pruebas de hipótesis y algunos ejemplos de los **algoritmos** para los que estas pruebas son necesarias:
- Prueba de hipótesis **para la media**: Se utiliza para evaluar afirmaciones sobre el valor medio de una variable en una población o muestra. Ejemplo de algoritmo: Prueba t de Student.
- Prueba de hipótesis **para la proporción**: Se utiliza para evaluar afirmaciones sobre la proporción de una característica o evento en una población o muestra. Ejemplo de algoritmo: Prueba de proporciones.
- Prueba de hipótesis **para la diferencia de medias**: Se utiliza para comparar las medias de dos grupos o poblaciones y evaluar si hay una diferencia significativa entre ellos. Ejemplo de algoritmo: Prueba t de Student para muestras independientes.
- Prueba de hipótesis **para la diferencia de proporciones**: Se utiliza para comparar las proporciones de dos grupos o poblaciones y evaluar si hay una diferencia significativa entre ellas. Ejemplo de algoritmo: Prueba de diferencia de proporciones.
- Prueba de hipótesis **para la varianza**: Se utiliza para evaluar afirmaciones sobre la varianza de una población o muestra. Ejemplo de algoritmo: Prueba F.

- - - 
## Tipos de errores

Estos dos tipos de error están relacionados con el concepto de 
**"bias-variance trade-off"** (compromiso entre sesgo y varianza). 
Un modelo con **alto sesgo y baja varianza tiende a ser demasiado simplificado y no captura adecuadamente la complejidad de los datos**. Por otro lado, un modelo con bajo sesgo y alta varianza puede adaptarse demasiado a los datos de entrenamiento y tener dificultades para generalizar.

El objetivo en el aprendizaje automático es encontrar un equilibrio entre sesgo y varianza, lo que se conoce como [[minimización del error de generalización]]. Esto implica seleccionar un modelo que sea lo suficientemente complejo como para capturar los patrones relevantes en los datos, pero no tan complejo como para ajustarse excesivamente a los datos de entrenamiento. Estrategias como la validación cruzada, el ajuste de hiperparámetros y la selección de modelos adecuados se utilizan para abordar estos errores y lograr un mejor rendimiento y generalización en los algoritmos de machine learning.