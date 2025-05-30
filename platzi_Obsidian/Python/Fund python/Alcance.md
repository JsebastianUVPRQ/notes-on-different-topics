Cuando ejecutamos una funcion, python entra en un "contexto de ejecución" al cual le son asignadas **ciertas variables** de las que existen en el total del código. 
se refiere al ámbito o contexto en el que una variable o función es válida y puede ser accedida. En otras palabras, el alcance determina en qué partes del programa una variable o función puede ser utilizada y cuál es su tiempo de vida.

En Python, existen dos tipos principales de alcance:

1. **Alcance global (Global scope)**: Las variables y funciones declaradas fuera de cualquier función o bloque de código tienen alcance global. Esto significa que pueden ser accedidas desde cualquier lugar del programa, tanto dentro como fuera de funciones o bloques anidados. Las variables y funciones con alcance global persisten durante toda la ejecución del programa.	
   ``` python
x = 10 # Variable global def my_function(): print(x) # Acceso a la variable global dentro de la función my_function() # Imprime 10, ya que la variable x es global
```
2. **Alcance local (Local scope)**: Las variables y [[funciones]] declaradas dentro de una función o bloque de código tienen alcance local. Esto significa que solo pueden ser accedidas dentro de la función o bloque donde fueron declaradas. Las variables y funciones con alcance local solo existen mientras se está ejecutando esa función o bloque, y luego desaparecen.

``` python
def my_function(): y = 5 # Variable local print(y) # Acceso a la variable local dentro de la función my_function() # Imprime 5, ya que la variable y es local print(y) # Generará un error, ya que la variable y no es accesible fuera de la función
```

![[Pasted image 20230731232153.png]]