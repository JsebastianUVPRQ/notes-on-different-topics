## Definición 
Los entornos virtuales son una forma de crear un sistema operativo virtual dentro de otro sistema operativo. Esto permite a un usuario tener varios sistemas operativos diferentes en un mismo equipo físico, lo que puede ser muy útil en situaciones en las que es necesario utilizar diferentes aplicaciones o tecnologías que requieren entornos diferentes:
	* Permiten utilizar varios sistemas operativos en un mismo equipo físico.
	* Permiten instalar y utilizar diferentes aplicaciones y tecnologías de manera segura, sin tener que hacer cambios permanentes en el sistema operativo principal.
	* Pueden ser fácilmente movidos o copiados, lo que significa que pueden ser utilizados en diferentes equipos o compartidos con otros usuarios.
	* También pueden ser fácilmente respaldados y restaurados en caso de que se produzca un problema, lo que puede ayudar a prevenir la pérdida de datos o el tiempo de inactividad.  
- - -
## Instalación 
Para crear un entorno virtual usar el comando -> python3 -m venv envname 
	**Verificar donde esta python y pip**	->which python3   which pip3
		**Si estas en _linux_ o _wsl_ debes instalar** -> sudo apt install -y python3-venv
	**Poner cada proyecto en su propio ambiente, entrar en cada carpeta** -> python3 -m venv envname
	**Activar ambiente** -> source env/bin/activate
	Una __librería__ se puede instalar en un Venv con el comando -> pip3 install <libreria>==<version>  
	**Verificar las instalaciones** -> pip3 freeze
### Requirementstxt 
	
