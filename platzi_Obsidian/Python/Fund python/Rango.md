Los rangos representan una secuencia de enteros y al igual que nuestra notación de rebanadas, podemos definirnos como un comienzo con un fin y con los pasos que nosotros vamos a utilizar para generar esta secuencia. 
Ahora los rangos, al igual que los **Strings** y las **to Push**, son inmutables
Es decir, una vez que nosotros generamos un rango, ya no podemos modificarlo.
Pero esto nos da una gran ventaja, que son muy, muy deficientes en cuanto memoria porque
porque sabemos desde el principio cuánta memoria vamos a necesitar para almacenar este rango.
Y normalmente nosotros utilizamos estos rangos dentro de los foros Dotx.

```Python 
#sintaxis:------------
nombre_rango = range(<comienzo(incluyente)>,<fin(excluyente)>,<longitud_paso>)
type(nombre_rango)
	<class 'range'>

#Ejemplo1----------------
my_range = range(1,5)
	for i in my_range 
	print(i)
1
2
...
#Dirección en memoria-------
id(my_range)
```
### modificadores del print()
![[Pasted image 20230804014318.png]]