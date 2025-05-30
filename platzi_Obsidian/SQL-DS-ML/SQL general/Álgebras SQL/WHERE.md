La cláusula _WHERE_ es la instrucción que nos permite filtrar el resultado de una sentencia **FROM**. Habitualmente no deseamos obtener toda la información existente en la tabla, sino que queremos obtener solo la información que nos resulte útil en ese momento. La cláusula **WHERE** filtra los datos antes de ser devueltos por la consulta. su [[Tipos de operadores álgebra relacional]] es **selección.**
 
Cuando en la Cláusula WHERE queremos incluir un tipo texto, debemos incluir el valor entre comillas simples. En nuestro ejemplo, se desea consultar un coche en concreto, para esto se agregó una cláusula **WHERE**. Esta cláusula especifica una o varias condiciones que deben cumplirse para que la sentencia **SELECT** devuelva los datos. En este caso la consulta devolverá solo los datos del coche con matrícula para que la consulta devuelva solo los datos del coche con matrícula `MF-234-ZD` o bien la matrícula `FK-938-ZL` . Se puede utilizar la cláusula **WHERE** solamente, o en combinación con tantas condiciones como queramos.

`WHERE` es usado para filtrar registros. `WHERE` es cuando para extraer solamente las condiciones que cumplen con esa condición.

```sql 
SELECT * FROM tabla_diaria WHERE id=1; 
SELECT * FROM tabla_diaria WHERE cantidad>10; 
SELECT * FROM tabla_diaria WHERE cantidad<100;
```

## complementos 
Este puede ser combinado con `AND` ,`OR` y `NOT`.

`AND` y `OR` son usados para filtrar registros de más de una condición.

- `AND` muestra un registro si todas las condiciones separadas por `AND` son `TRUE`.
- `OR` muestra un registro si alguna de las condiciones separadas por `OR` son `TRUE`.

```sql
SELECT * FROM tabla_diaria WHERE cantidad > 10 	AND cantidad < 100; 
SELECT * FROM tabla_diaria WHERE cantidad BETWEEN 10 AND cantidad < 100;
```

`BETWEEN` puede ser usado para **definir límites.**

La separación por paréntesis es muy importante.

`SELECT *  FROM users WHERE name = "Israel" 	AND ( 	lastname = "Vázquez" 	OR 	lastname = "López" ); SELECT *  FROM users WHERE name = "Israel" 	AND  	lastname = "Vázquez" 	OR 	lastname = "López";`

En el primero va a devolver todos los que son Israel Vázquez o Israel López, en el segundo devolverá a todos los que se llaman Israel Vázquez o se apellida López(sólo apellido).

`NOT` valida que un dato no sea `TRUE`.

`SELECT column1, column2, ... FROM table_name WHERE NOT condition;`

**Para especificar patrones en una columna** usamos `LIKE`. Podemos mostrar diferentes cosas que buscamos.

`SELECT * FROM users WHERE name LIKE "Is%"; SELECT * FROM users WHERE name LIKE "Is_ael"; SELECT * FROM users WHERE name NOT LIKE "Is_ael";`

- En el primero, colocamos un `%` para representar que se va a buscar lo que tenga `is%` pero que no importa los carácteres después de `%`.
- En el segundo le estamos diciendo con `_` que puede haber lo que sea en medio de `Is` y `ael`.
- Y en el último le decimos que ponga todas las filas que no sean igual a lo que arriba estabamos buscando.

Igual podemos decir que nos traiga registros que estén vacíos o que no lo estén.

`SELECT *  FROM users WHERE name IS NULL; SELECT * FROM users WHERE name IS NOT NULL;`

Y para seleccionar filas con datos específicos, usamos IN.

`SELECT * FROM users WHERE name IN ('Israel','Laura','Luis');`

### Having
La cláusula HAVING es una implemetacion que el sistema gestor de bases de datos SQL crea para complementar el condicionante WHERE, ya que el condicionante WHERE no permite utilizar funciones de agregación como SUM, MAX, MIN o AVG, es decir, con un condicionante WHERE no podemos crear consultas válidas que sean capaz de devolvernos los datos de los clientes que compraron más de 1000 productos durante un año, por ejemplo.