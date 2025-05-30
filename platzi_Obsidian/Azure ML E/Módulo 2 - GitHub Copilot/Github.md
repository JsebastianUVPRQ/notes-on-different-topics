### lista paso a paso para publicar en GitHub una carpeta que contiene un proyecto de ciencia de datos, incluyendo notebooks, archivos `.txt` e imágenes:

1. **Crea una cuenta en GitHub:** Si aún no tienes una cuenta en GitHub, crea una en [https://github.com](https://github.com/).
    
2. **Crea un nuevo repositorio:**
    
    - Inicia sesión en tu cuenta de GitHub.
    - Haz clic en el ícono "+" en la esquina superior derecha y selecciona "Nuevo repositorio".
    - Asigna un nombre al repositorio y, opcionalmente, proporciona una descripción.
    - Puedes configurar la visibilidad del repositorio como público o privado.
3. **Prepara la carpeta de tu proyecto:**
    
    - Organiza todos los archivos de tu proyecto (notebooks, archivos `.txt`, imágenes, etc.) en una carpeta en tu computadora.
4. **Inicializa un repositorio local:**
    
    - Abre una terminal en la carpeta de tu proyecto.
    - Ejecuta el siguiente comando para inicializar un repositorio Git local:
  
	```git
	git init
	```
5. **Agrega y confirma los archivos:**
    
    - Utiliza los siguientes comandos para agregar todos los archivos de tu proyecto al área de preparación y realizar el primer commit:
        ```git 
        git add . git commit -m "Primer commit"
        ```

1. **Conecta tu repositorio local al repositorio remoto en GitHub:**
    
    - Copia la URL del repositorio remoto que creaste en GitHub.
2. **Agrega el repositorio remoto:**
    
    - Ejecuta el siguiente comando en tu terminal, reemplazando `<URL_del_repositorio>` con la URL que copiaste:
        ```csharp 
        git remote add origin <URL_del_repositorio>
        ```
3. **Sube tus archivos al repositorio remoto:**
    
    - Ejecuta el siguiente comando para subir tus archivos al repositorio remoto en GitHub:
        ```perl
        git push -u origin master
        ```
    - Proporciona tus credenciales de GitHub si se te solicitan.

1. **Verifica en GitHub:**
    
    - Actualiza la página del repositorio en GitHub y verás tus archivos cargados.
10. **Opcional: Archivos `.gitignore`:**
    
    - Crea un archivo llamado `.gitignore` en la raíz de tu proyecto y lista los nombres de los archivos o carpetas que deseas excluir del seguimiento de Git (por ejemplo, archivos de datos grandes o archivos temporales). Puedes encontrar plantillas de `.gitignore` para diferentes lenguajes y entornos en [https://github.com/github/gitignore](https://github.com/github/gitignore).

¡Listo! Ahora tu proyecto de ciencia de datos está publicado en GitHub y accesible para otras personas. Puedes compartir el enlace del repositorio para mostrar tus resultados y colaborar con otros en tu proyecto.

