En Python, todos los datos son objetos, desde las funciones hasta las estructuras
de datos, pasando por los literales. En este capítulo se estudiará
en profundidad qué son los objetos y cómo se crean, usan y modifican.
Asimismo, se verán todas sus características principales.
En los capítulos anteriores se hablaba de las asignaciones y de las variables
como en el siguiente ejemplo:

>>> mi_variable = int(42)

Dijimos que mi_variable es solo el nombre que se le otorga a la referencia
que se hace sobre el literal 42 y es una forma de guardar los datos
en memoria y poder usarlos más adelante de forma simple. No obstante, el
literal 42 realmente se encaja dentro del tipo int, que es un tipo de objeto
y técnicamente es una instancia de la clase número entero cuyo valor interno
es 42.
>>> type(mi_variable)
<class 'int'>

Para definirlo de una forma sencilla, una clase es el molde que se utiliza
para crear objetos de un tipo específico. Puede haber tantas clases como
sean necesarias. Una vez que se crea un objeto específico de una clase (en
el ejemplo anterior, el objeto que tiene el valor 42), el objeto se considera
una instancia de la clase (en el ejemplo anterior, instancia de la clase int).
El uso de clases permite tener múltiples instancias distintas de la misma
clase. Estas se comportan de la forma que se ha definido en la clase, e incluso
posibilitan generar clases más específicas de la clase original (denominada
padre), lo que se conoce como herencia.
Las instancias o las clases pueden guardar información, lo que se denomina
atributos. Por otro lado, cada clase puede definir herramientas para operar
tanto con sus propios datos como con otros objetos. A estas se les denomina
métodos y pueden ser de distintos tipos, como se verá en los siguientes
apartados.