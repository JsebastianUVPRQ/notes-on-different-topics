Al llegar un archivo, lo primero que deberíamos hacer es intentar responder: 
• ¿Cuántos registros hay? – ¿Son pocos? – ¿Son muchos y no tenemos Capacidad (CPU+RAM) suficiente para procesarlo? 
– ¿Están todas las filas completas ó tenemos campos con valores nulos? – En caso que haya demasiados nulos: ¿Queda el resto de información inútil?
• ¿Qué datos son discretos y cuáles continuos? 
• Muchas veces sirve distinguir el tipo de datos: texto, int, double, float 
• Si es un problema de tipo supervisado:
	– ¿Cuál es la columna de “salida”? ¿binaria, multiclase? 
	– ¿Esta balanceado el conjunto salida? • ¿Cuales parecen ser features importantes? ¿Cuales podemos descartar? 
• ¿Siguen alguna distribución? 
• ¿Hay correlación entre features (características)?
• En [[NLP - Procesamiento de lenguaje natural]] es frecuente que existan categorías repetidas ó mal tipeadas, ó con mayusculas/minúsculas, singular y plural, por ejemplo “Abogado” y “Abogadas”, “avogado” pertenecerían todos a un mismo conjunto. 
• ¿Estamos ante un problema dependiente del del tiempo? Es decir un problema de [[Algoritmos/Time Series/Series temporales]].
Si fuera un problema de [[Vision por computadora]]: ¿Tenemos suficientes muestras de cada clase y variedad, para poder hacer generalizar un modelo de Machine Learning?
• Cuales son los Outliers¹⁹? (unos pocos datos aislados que difieren drásticamente del resto y “contaminan” ó desvían las distribuciones) 
	– Podemos eliminarlos? es importante conservarlos? 
	– son errores de carga o son reales?
¿Tenemos posible sesgo de datos? (por ejemplo perjudicar a clases minoritarias²⁰ por no incluirlas y que el modelo de ML discrimine en sus predicciones) [[Clasificación con datos desbalanceados | Aprende Machine Learning](https://www.aprendemachinelearning.com/clasificacion-con-datos-desbalanceados/)]

**También puede ocurrir que nos pasen múltiples fuentes de datos, por ejemplo un csv, un excel y el acceso a una base de datos. Entonces tendremos que hacer un paso previo de unificación de datos.**
## Qué sacamos del EDA? 
El EDA será entonces una primer aproximación a los datos, ATENCION, si estamos mas o menos bien preparados y suponiendo una muestra de datos “suficiente”, puede que en “unas horas” tengamos ya varias conclusiones como por ejemplo: 
• Esto que quiere hacer el cliente CON ESTOS DATOS es una locura imposible! 
• No tenemos datos suficientes ó son de muy mala calidad, pedir más al cliente. 
• Un modelo de tipo Arbol²¹ es lo más recomendado usar – (reemplazar Arbol, por el tipo de modelo que hayamos descubierto como mejor opción!) 
• No hace falta usar Machine Learning para resolver lo que pide el cliente. (ESTO ES MUY **IMPORTANTE!**)
Repito: el EDA debe tomar horas, ó puede que un día, pero la idea es poder sacar algunas conclusiones rápidas para contestar al cliente si podemos seguir o no con su propuesta. Luego del EDA, suponiendo que seguimos adelante podemos tomarnos más tiempo y analizar en mayor detalle los datos y avanzar a nuevas etapas para aplicar modelos de Machine Learning²².