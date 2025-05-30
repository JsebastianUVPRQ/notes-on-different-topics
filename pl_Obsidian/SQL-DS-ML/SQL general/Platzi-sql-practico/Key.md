En el contexto de [[SQL-DML]] (Structured Query Language), las "llaves" se refieren a los campos o columnas de una tabla de base de datos que se utilizan para identificar de manera única cada fila o registro en esa tabla. Las llaves desempeñan un papel fundamental en la organización y gestión de los datos en una base de datos relacional, y se dividen en varios tipos clave según su función:

|Tipo de Clave|Descripción|
|---|---|
|**Clave Primaria**|- Se utiliza para identificar de manera única cada fila en una tabla.|
||- Debe ser única y no puede contener valores nulos.|
||- Garantiza la integridad de los datos y se utiliza para establecer relaciones entre tablas.|
|**Clave Externa**|- Se relaciona con la clave primaria de otra tabla, estableciendo relaciones entre tablas.|
||- Asegura la integridad referencial y mantiene la consistencia en la base de datos.|
|**Clave Candidata**|- Puede ser utilizada como clave primaria.|
||- En una tabla, puede haber varias claves candidatas, pero solo una se elige como clave primaria.|
|**Clave Alternativa**|- Son claves candidatas que no se seleccionaron como clave primaria.|
||- Aunque no son clave principal, pueden identificar registros de manera única.|
|**Clave Superclave**|- Conjunto de una o más columnas que identifican de manera única una fila.|
||- Incluye tanto las claves primarias como las candidatas.|
|**Clave Compuesta**|- Clave primaria que consta de dos o más columnas utilizadas en conjunto para identificar registros.|
||- Se usa cuando una sola columna no puede garantizar la unicidad.|


1. **Clave Primaria (Primary Key):** La clave primaria es una columna o un conjunto de columnas que se elige para identificar de forma única cada fila en una tabla. Debe ser única para cada fila y no puede contener valores nulos. La clave primaria garantiza la integridad de los datos y se utiliza frecuentemente para establecer relaciones entre tablas en una base de datos relacional.
    
2. **Clave Externa (Foreign Key):** La clave externa es una columna o conjunto de columnas en una tabla que se relaciona con la clave primaria de otra tabla. Se utiliza para establecer relaciones entre tablas, lo que permite que una tabla haga referencia a datos en otra. Las claves externas aseguran la integridad referencial y permiten mantener consistencia en la base de datos.
    
3. **Clave Candidata (Candidate Key):** Una clave candidata es una columna o conjunto de columnas que podría usarse como clave primaria. En una tabla, puede haber varias claves candidatas, pero solo una se elige como clave primaria.
    
4. **Clave Alternativa (Alternate Key):** Las claves alternativas son las claves candidatas que no se seleccionaron como clave primaria. Aunque no se usan como clave principal, pueden ser útiles para identificar registros de manera única.
    
5. **Clave Superclave (Super Key):** Una superclave es un conjunto de una o más columnas que permite identificar de manera única una fila en una tabla. Una clave primaria es un tipo de superclave, pero no todas las superclaves son clave primaria.
    
6. **Clave Compuesta (Composite Key):** Una clave compuesta es una clave primaria que consta de dos o más columnas que juntas se utilizan para identificar de manera única una fila. Esta clave se utiliza cuando una sola columna no puede garantizar la unicidad.