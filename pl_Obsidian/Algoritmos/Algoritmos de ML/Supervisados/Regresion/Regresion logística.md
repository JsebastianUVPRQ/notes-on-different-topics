![[Pasted image 20230826013557.png]]
La Regresión logistica se utiliza en los siguientes casos:

[[Algoritmo - Búsqueda binaria]]: la regresión logística se utiliza para clasificar la observación en dos categorías distintas, como "sí" o "no", "éxito" o "fracaso", "compra" o "no compra", etc.

Datos de entrada no lineales: la regresión logística puede manejar datos de entrada no lineales y se puede utilizar para modelar la relación entre variables predictoras y variables de respuesta no lineales.

Datos con valores atípicos: la regresión logística es robusta a los valores atípicos y no se ve afectada significativamente por los puntos de datos que se desvían de la tendencia general.

Problemas de clasificación multiclase: si bien la regresión logística es una técnica de clasificación binaria, también se puede utilizar para problemas de clasificación multiclase mediante la técnica "uno contra todos".
# matriz de confusión


## Función sigmoide


```Python
import random from math 
import exp import matplotlib.pyplot as plt 

def sigmoid(x): 
	return ( 1 ) / ( 1 + exp( -x ) ) 

def main(): 
	x = [] 
	y = [] 
	
	for _ in range(200): 
		num = random.randint(-10, 10) 
		x.append(num) 
		y.append(sigmoid(num)) 	
	plt.plot(x, y, 'bo') 

if __name__ == "__main__": 
	main()
```
# odds
Los "odds" (en español, "cuotas" o "probabilidades") son una forma de expresar la probabilidad de que ocurra un evento. En particular, los "odds" representan la relación entre la probabilidad de que ocurra un evento y la probabilidad de que no ocurra.

Por ejemplo, si la probabilidad de que un equipo de fútbol gane un partido es del 60%, entonces la probabilidad de que pierda es del 40%. En términos de "odds", la probabilidad de ganar se puede expresar como 3 a 2, lo que significa que por cada 2 veces que pierde el equipo, gana 3 veces. De manera similar, la probabilidad de perder se puede expresar como 2 a 3, lo que significa que por cada 3 veces que gana el equipo, pierde 2 veces.

Los "odds" se utilizan comúnmente en las apuestas y en los juegos de azar, donde se usan para determinar las ganancias potenciales de una apuesta. En la estadística, los "odds" se utilizan en la regresión logística para modelar la relación entre las variables independientes y la variable dependiente binaria.