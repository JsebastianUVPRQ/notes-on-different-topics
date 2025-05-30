- Puedes asignar alias con **“AS”** (Muy potente):
	SELECT field AS abreviacionOalias

- **COUNT()** Cuenta el número de elementos que existen en todas las tuplas de la base de datos

- **SUM()** Toma la columna que le digas y suma sus valores de forma consecutiva

- **AVE()** (De AVErage) Saca el valor promerdio de toda la columna

Al igual que otros lenguajes puedes hacer **“IF”** con un montón de posibilidades.
![[Pasted image 20231019005124.png]]

## SELECT junto a FROM
Con `SELECT` se especifica que columnas queremos obtener de una tabla determinada y con `FROM` se indica de donde se va a obtener la información que se va proyectar con `SELECT`. `FROM` va después de `SELECT`

```sql 
SELECT * FROM base_de_datos.tabla
```

En la sentencia anterior el manejador de base de datos (**DBMS**) va al esquema y proyecta lo solicitado.
  
**Las sentencias SQL no son sensibles a minúsculas o mayúsculas pero se recomienda escribir las palabras claves en MAÝUSCULAS y el resto en minúsculas**
*****`[[JOIN]] es un complemento de `FROM`.**


También se puede obtener la información de una base de datos remota, es decir que el esquema de donde que queremos obtener información se encuentra en otro **DBMS**.

  
## dblink
Para obtener información de una tabla que se encuentra remotamente se utiliza la función
`dblink`, dicha función recibe dos parámetros:
1. configuración de conexión al DBMS remoto
2. consulta SQL

  
Ejemplo de dblink

```SQL 
SELECT * FROM dblink(' 	dbname=somedb 	port=5432 host=someserver 	user=someuser 	password=somepwd', 	'SELECT gid, area, parimeter, 			state, country, 			tract, blockgroup, 			block, the_geom 	FROM massgis.cens2000blocks') 	AS blockgroups
```