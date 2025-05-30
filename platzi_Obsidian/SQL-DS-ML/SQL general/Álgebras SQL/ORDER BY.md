La cláusula _ORDER BY_ es la instrucción que nos permite especificar el orden en el que serán devueltos los datos. Podemos especificar el orden de forma ascendente o descendente a través de las palabras clave **ASC** y **DESC**. 
El orden depende del tipo de datos que estén definidos en la columna, de forma que un campo numérico será ordenado como tal, y un alfanumérico se ordenará de la A a la Z, aunque su contenido sea numérico. El valor predeterminado es ASC si no se especifica al hacer la consulta.

Ejemplos:

``` SQL 
SELECT
    matricula,
    marca,
    modelo,
    color,
    numero_kilometros,
	    Num_plazas
FROM
    coches
ORDER BY
    marca ASC,
    modelo DESC;
```
Este ejemplo, selecciona todos los campos matricula, marca, modelo, color, numero_kilometros y num_plazas de la tabla coches, ordenándolos por los campos marca y modelo, marca en forma ascendente y modelo en forma descendente.
### strings
La ordenacion se realiza de forma alfabética

### querys complejas
**INDICES:** excelentes para búsquedas y ordenamientos, cuando estamos haciendo queries complejos, cuando estamos tratando de extraer información constantemente, haciendo joins complicados a través de esos campos y nos sirve tener un índice que guarde el orden de ese campo en particular para hacer extracciones muy rápidas.

**CUIDAR PARA ALTA TRANSACCIONALIDAD:** la contrapartida de esto es que cuando tienes un índice, la parte de escritura, cuando llegas a hacer un Update de esa columna en particular en la que pusiste un índice, entonces cada escritura tardará un poco más que la anterior porque básicamente agrega un nuevo elemento, revisa todos elementos anteriores y posteriores y vuelve a ordenarlos en el índice y si agregamos otro elemento vuelve a revisar todos y a ordenarlos.

No debemos poner índices por poner sino ser muy cuidadosos de aquellas columnas que hacemos JOIN muy seguido o que tienen muchísimos datos y siempre estamos ordenando por esa columna. Es válido ponerlo pero siempre teniendo en cuenta que cuando tenemos que ingerir muchos datos o hacer muchos INSERT no es bueno tener índices en esas tablas (o tener la menor cantidad de índices posible). Es importante tener en mente cuántas lecturas Vs cuántas escrituras haces en una tabla o en un campo particular para decidir si conviene poner un índice. Si vas a hacer muchas escrituras por segundo no es conveniente poner índices o tratar de mantenerlo al mínimo. En cambio, si realmente escribes muy poco en esa tabla pero haces búsquedas constantes y muchos Joins sobre esa tabla entonces vale la pena usar el índice sobre ese campo en particular donde haces el Join o donde haces el ordenamiento porque es un gran complemento para nuestra cláusula ORDER BY.