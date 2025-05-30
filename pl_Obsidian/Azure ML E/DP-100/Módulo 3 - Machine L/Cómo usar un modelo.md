Entrenar un modelo es el proceso de mejorar el funcionamiento de dicho modelo. El entrenamiento requiere que usemos el modelo, la función objetivo y el optimizador en un bucle específico. Esto puede tardar unos minutos o días en completarse. Solemos entrenar el modelo solo una vez. Una vez entrenado, podemos usarlo tantas veces como queramos sin realizar más cambios.

Por ejemplo, en nuestro escenario de la tienda para perros de rescate de avalanchas, queremos entrenar un modelo mediante un conjunto de datos públicos, que cambiará el modelo para que pueda predecir la talla de las botas de un perro en función de la talla de su arnés. Una vez entrenado, usaremos el modelo en nuestra tienda en línea para asegurarnos de que los clientes van a comprar las botas que se adaptarán mejor a sus perros.

## Datos para usar, datos para entrenar

Recuerde que un conjunto de datos es una recopilación de información sobre objetos o cosas. Por ejemplo, un conjunto de datos puede contener información sobre perros:

|Identificador del perro|Talla de las botas|Talla del arnés|Color del perro|Raza|
|---|---|---|---|---|
|0|27|12|Brown|San Bernard|
|1|26|11|Negro|Labrador|
|2|25|10|Blanco|Labrador|
|3|29|14|Negro|Pastor alemán negro|

Cuando usamos nuestro modelo, solo necesitamos las columnas de datos que el modelo acepta como entrada. **Estas columnas se denominan características.** En nuestro escenario, si el modelo acepta la talla del arnés y calcula la talla de las botas, entonces **nuestra característica es la talla del arnés.**

Durante el entrenamiento, la función objetivo normalmente necesita saber tanto la salida del modelo como cuál era la respuesta correcta. **Estas se denominan etiquetas.** En nuestro escenario, si el modelo predice la talla de las botas, **nuestra etiqueta será la talla de las botas.**

En conjunto, esto significa que para usar un modelo solo necesitamos las características, mientras que durante el entrenamiento normalmente necesitamos tanto las características como las etiquetas. Durante el entrenamiento en nuestro escenario, necesitamos tanto la característica de la talla del arnés como la etiqueta de la talla de las botas. Cuando usamos el modelo en nuestro sitio web, solo necesitamos saber la característica de la talla del arnés. A continuación, nuestro modelo calculará la talla de las botas que debemos usar. 
En este módulo se han tratado algunas nuevas jergas importantes. A continuación, se resumirá lo que se ha aprendido:

- El objetivo del aprendizaje automático es detectar patrones en los datos y usarlos para realizar estimaciones.
    
- El aprendizaje automático se diferencia del desarrollo de software normal en que usamos código específico, en lugar de nuestra propia intuición, para mejorar el funcionamiento del software.
    
- El proceso de aprendizaje usa, de forma conceptual, cuatro componentes:
    
    - **Datos** sobre el tema que nos ocupa.
    - Un **modelo**, que realiza estimaciones.
    - Un **objetivo** que el modelo está intentando lograr.
    - Un **optimizador**, que es el código adicional que cambia el modelo en función de su rendimiento.
- Los datos pueden entenderse como características y etiquetas. Las características se corresponden con las posibles entradas del modelo, mientras que las etiquetas se corresponden con las salidas del modelo o las salidas del modelo que queremos.
    
- Pandas y Plotly son herramientas eficaces para explorar los conjuntos de datos en Python.
    
- Una vez que tenemos un modelo entrenado, podemos guardarlo en el disco para su uso posterior.