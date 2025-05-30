## Notación de objetos JavaScript (JSON)

JSON es un formato omnipresente en el que se usa un esquema de documento jerárquico para definir entidades de datos (objetos) que tienen varios atributos. Cada atributo puede ser un objeto (o una colección de objetos ), lo que hace de JSON un formato flexible adecuado tanto para datos estructurados como semiestructurados.

En el ejemplo siguiente se muestra un documento JSON que contiene una colección de clientes. Cada cliente tiene tres atributos (_firstName_, _lastName_ y _contact_) y el atributo _contact_ contiene una colección de objetos que representan uno o varios métodos de contacto (correo electrónico o teléfono). Tenga en cuenta que los objetos se incluyen entre llaves (**{..}**) y las colecciones se incluyen entre corchetes (**[..]**). Los atributos se representan mediante pares _nombre_**:**_valor_ y se separan por comas (**,**).

## Lenguaje de marcado extensible (XML)

XML es un formato de datos legible popular en la década de 1990 y 2000. En gran medida lo ha reemplazado el formato JSON, menos detallado, pero todavía hay algunos sistemas que usan XML para representar datos. XML usa _etiquetas_ entre corchetes angulares (**../**) para definir _elementos_ y _atributos_, como se muestra en este ejemplo

## Objeto binario grande (BLOB)

En última instancia, todos los archivos se almacenan como datos binarios (1 y 0), pero en los formatos legibles que se describen anteriormente, los bytes de datos binarios se asignan a caracteres imprimibles (normalmente a través de un esquema de codificación de caracteres como ASCII o Unicode). Aun así, algunos formatos de archivo, especialmente para los datos no estructurados, almacenan los datos como datos binarios sin formato que las aplicaciones deben interpretar y representar. Los tipos comunes de datos almacenados como datos binarios incluyen imágenes, vídeo, audio y documentos específicos de aplicaciones.

Cuando trabajan con datos de este tipo, los profesionales de datos suelen hacer referencia a estos archivos de datos como _BLOB_ (objetos binarios grandes).

## Formatos de archivo optimizados

Aunque los formatos legibles para datos estructurados y semiestructurados pueden ser útiles, normalmente no están optimizados para el procesamiento o el espacio de almacenamiento. Con el paso del tiempo, se han desarrollado algunos formatos de archivo especializados que permiten la compresión, la indexación y un almacenamiento y procesamiento eficientes.

Entre los formatos de archivo optimizados más habituales que puede ver se incluyen _Avro_, _ORC_ y _Parquet_:

- _Avro_ es un formato basado en filas creado por Apache. Cada registro contiene un encabezado que describe la estructura de los datos en ese registro. Este encabezado se almacena como JSON. Los datos, por su parte, se almacenan como información binaria. Una aplicación usa la información del encabezado para analizar los datos binarios y extraer los campos que contienen. Avro es un formato adecuado para comprimir datos y reducir los requisitos de almacenamiento y ancho de banda de red.
    
- _ORC_ (formato de columnas de filas optimizadas) organiza los datos en columnas en lugar de en filas. Lo desarrolló HortonWorks para optimizar las operaciones de lectura y escritura en Apache Hive (Hive es un sistema de almacenamiento de datos que admite resúmenes de datos rápidos y consultas en grandes conjuntos de datos). Un archivo ORC contiene _franjas_ de datos. Cada franja contiene los datos de una columna o de un conjunto de columnas. Una franja contiene un índice de las filas de dicha franja, los datos de cada fila y un pie de página que contiene información estadística (count, sum, max, min, etc.) de cada columna.
    
- _Parquet_ es otro formato de datos en columnas creado por Cloudera y Twitter. Un archivo Parquet contiene grupos de filas. Los datos de cada columna se almacenan juntos en el mismo grupo de filas. Cada grupo de filas contiene uno o varios fragmentos de datos. Un archivo Parquet incluye metadatos que describen el conjunto de filas que hay en cada fragmento. Una aplicación puede usar estos metadatos para localizar rápidamente el fragmento correcto para un conjunto determinado de filas y, a continuación, para recuperar los datos de las columnas especificadas relativos a esas filas. Parquet destaca por almacenar y procesar tipos de datos anidados de forma eficaz. Admite esquemas de compresión y codificación muy eficaces.