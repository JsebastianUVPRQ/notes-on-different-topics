## Definición
En [[Azure Machine Learning Studio]], hay varias maneras de crear modelos de aprendizaje automático de regresión. Una de ellas consiste en usar una interfaz visual denominada __diseñador__, que puede usar para entrenar, probar e implementar modelos de aprendizaje automático. La interfaz de arrastrar y colocar usa entradas y salidas claramente definidas que se pueden compartir, reutilizar y controlar la versión.

Cada proyecto de _diseñador_, conocido como [[Pipeline]], tiene un __panel izquierdo para la navegación__ y un lienzo en el lado derecho.
Para usar el _diseñador_, identifique los bloques de creación o los componentes necesarios para el modelo, colóquelos y conéctelos en el lienzo y ejecute un trabajo de aprendizaje automático.
![[Pasted image 20230809232018.png]]
## Pipelines

Las [[Pipeline]] permiten organizar, administrar y reutilizar flujos de trabajo de aprendizaje automático complejos entre proyectos y usuarios. Una canalización se inicia con el conjunto de datos desde el que quiere entrenar el modelo. Cada vez que se ejecuta una canalización, la configuración de esta y sus resultados se almacenan en el área de trabajo como un trabajo de canalización.
![[Pasted image 20230809232124.png]]
## Componentes

Un [[Azure ML E/DP-100/Optimize model training/Components]] de Azure Machine Learning encapsula un paso en una canalización de aprendizaje automático. Puede considerar un componente como una función de programación y como un bloque de creación para las canalizaciones de Azure Machine Learning. En un proyecto de canalización, puede acceder a los componentes y recursos de datos desde la pestaña **Biblioteca de recursos** del panel izquierdo.
![[Pasted image 20230809232145.png]]
## Conjuntos de datos

Puede crear recursos de datos en la página **Datos** a partir de archivos locales, un almacén de datos, archivos web y Open Datasets. Estos recursos de datos aparecerán junto con los conjuntos de datos de ejemplo estándar en la _biblioteca de recursos_ del **diseñador**.
![[Pasted image 20230809232558.png]]

## Trabajos de Azure Machine Learning

Un trabajo de Azure Machine Learning (ML) ejecuta una tarea en un destino de proceso especificado. Los trabajos permiten el seguimiento sistemático de los flujos de trabajo y la experimentación de aprendizaje automático. Una vez creado un trabajo, Azure ML mantiene un registro de ejecución del mismo. Todos los registros de ejecución de los trabajos se pueden ver en Azure ML Studio.

En el proyecto del diseñador, puede acceder al estado de un trabajo de canalización mediante la pestaña **Trabajos enviados** del panel izquierdo.
![[Pasted image 20230809232754.png]]

Puede encontrar todos los trabajos que ha ejecutado en un área de trabajo en la página **Trabajos**.
![[Pasted image 20230809232835.png]]