## Definición y sintaxis
Las listas son
```Python 
my_list = [<element_1>,<element_2>, ... , <element_n>]
```
## mutabilidad
- **lista.extend(iterable)** #extiende la lista con valores dentro de un iterable como un range()
- **lista.insert(i, ‘valor’)** #Agrega un valor en la posición i y recorre todos los demás. No borra nada.
- **lista.pop(i)** #Elimina valor en la posición i de la lista.
- l**ista.remove(‘valor’)** #Elimina el primer elemento con ese valor.
- **lista.clear()** #Borra elementos en la lista.
- **lista.index(‘valor’)** #Retorna posición del primer elemento con el valor.
- **lista.index(‘valor’, start, end)** #Retorna posición del elemento con el valor dentro de los elementos desde posición start hasta posición end)
- lista.count(‘valor’) #Cuenta cuántas veces esta ese valor en la lista.
- lista.sort() #Ordena los elementos de mayor a menor.
- lista.sort(reverse = True) #Ordena los elementos de menor a mayor.
- lista.reverse() #Invierte los elementos
- lista.copy() #Genera una copia de la lista. También útil para clonar listas.

## Clonación
Casi siempre es mejor clonar una lista en lugar de mutarla.
Para la clonacion se pueden utilizar las rebanadas (slices) o la función list:
```Python 
lista_org = [1, 2, 3]
lista_cop = list(lista_org)

id(lista_org) != id(lista_cop) --> True

```

## Comprehensions
Es una forma concisa de aplicar operaciones a los valores de una secuencia. También se pueden aplicar condiciones para filtrar.
```Python
my_list = [range(100)] #Números del 0 al 99
double = [i*2 for i in my_list]  #Pares del 0 al 198

pares = [i in my_list if i % 2 == 0]
```