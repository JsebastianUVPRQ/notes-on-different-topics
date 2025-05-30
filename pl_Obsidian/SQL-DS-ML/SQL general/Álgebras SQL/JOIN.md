En SQL, la cláusula `JOIN` se utiliza para combinar filas de dos o más tablas basándose en una relación entre las columnas de esas tablas. Equivalente a producto cartesiano.
Esta operación permite recuperar datos de múltiples tablas y relacionarlos en función de un campo común, lo que facilita la consulta y recuperación de información de una manera más completa y significativa. La cláusula `JOIN` es fundamental en SQL para trabajar con bases de datos relacionales.

La sintaxis básica de la cláusula `JOIN` es la siguiente:

```sql

SELECT columnas 
FROM tabla1 
JOIN tabla2 ON tabla1.columna = tabla2.columna;
```

Donde:

- `columnas`: Las columnas que deseas seleccionar de las tablas.
- `tabla1` y `tabla2`: Las tablas que deseas combinar.
- `ON`: Especifica la condición o la columna en la que se basa la combinación.
- `columna`: La columna que se utiliza para relacionar las tablas.


Tener en cuenta que full join no sirve en todos los BDSM

![[Pasted image 20231019011550.png]]
1. **INNER JOIN:** Retorna solo las filas que tienen un valor coincidente en ambas tablas. Si no hay coincidencias, esas filas no se incluyen en el resultado.
    
2. **LEFT JOIN (o LEFT OUTER JOIN):** Retorna todas las filas de la tabla izquierda (primera tabla en la cláusula) y las filas de la tabla derecha que tienen valores coincidentes. Si no hay coincidencias en la tabla derecha, se llenan con valores nulos.
    
3. **RIGHT JOIN (o RIGHT OUTER JOIN):** Es similar al LEFT JOIN, pero devuelve todas las filas de la tabla derecha y las coincidencias de la tabla izquierda.
    
4. **FULL JOIN (o FULL OUTER JOIN):** Retorna todas las filas de ambas tablas, llenando con valores nulos donde no haya coincidencias.
    
5. **SELF JOIN:** Se utiliza para combinar una tabla consigo misma. Puede ser útil en situaciones en las que se necesita comparar registros dentro de la misma tabla.
    
6. **CROSS JOIN:** Genera un producto cartesiano entre las tablas, es decir, combina todas las filas de la primera tabla con todas las filas de la segunda tabla. No se basa en una condición de coincidencia.