La sintaxis general de un [[comando]] Linux es la siguiente:  

- **Nombre del comando** _opcion(es)_  _parametro(s)_
	- **Nombredelcomando** es la regla que deseas ejecutar 
	- **opcion** o **flag** modifica el funcionamiento de un comando. Para ejecutarla, utiliza guiones **(-**) o guiones dobles **(—**).
	- **Parameter** o **argument** especifica cualquier información necesaria para el  [comando]. 
---
## **sudo (comando**)
- También puedes añadir una opción, por ejemplo:
	- **-k** o **-reset-timestamp** invalida el archivo timestamp.
	- **-g** o **-group=group** ejecuta comandos como un nombre o ID de grupo especificado.
	- **-h** o **-host=host** ejecuta comandos en el host.    
- - -
## **comando pwd**
-Utiliza el comando **pwd** para encontrar la ruta de tu directorio de trabajo actual. Simplemente introduciendo **pwd** te devolverá la ruta actual completa, una ruta de todos los directorios que comienza con una barra oblicua (**/**). Por ejemplo, **/inicio/nombredeusuario**.
El comando **pwd** utiliza la siguiente sintaxis: **pwd** *Opcion*
	-Tiene dos opciones aceptables:
	- **-L** o **-logical** imprime el contenido de las variables de entorno, incluidos los enlaces simbólicos.
	- **-P** o **-physical** imprime la ruta real del directorio actual.
- --
## Comando touch

El [comando touch](https://www.hostinger.co/tutoriales/usar-comando-touch-linux-ejemplos) permite crear un archivo vacío o generar y modificar una marca de tiempo en la línea de comandos de Linux.
	Por ejemplo, introduce el siguiente comando para crear un archivo HTML llamado **Web** en el directorio **Documentos**:
	 **touch /inicio/nombredeusuario/Documentos/Web.txt**  
-- -
### Comando head

El comando **head** permite ver las diez primeras líneas de un texto. Añadiendo una opción se puede cambiar el número de líneas mostradas. El comando **head** también se utiliza para dar salida a datos canalizados a la CLI. Esta es la sintaxis general:
	**head [opción] [archivo]**
Por ejemplo, si quieres ver las diez primeras líneas de **nota.txt**, situado en el directorio actual:
	**head nota.txt**
A continuación te indicamos algunas opciones que puedes añadir:
	* **-n** o **-lines** imprime el primer número personalizado de líneas. Por ejemplo, introduce **head -n 5 nombredearchivo.txt** para mostrar las cinco primeras líneas de **nombredearchivo.txt**.
	*  **-c** o **-bytes** imprime el primer número personalizado de bytes de cada archivo.
	* **-q** o **-quiet** no imprimirán cabeceras que especifiquen el nombre del archivo.

- - - 

Standard output-Standard error
	![[diagrama_redirect.bmp]]