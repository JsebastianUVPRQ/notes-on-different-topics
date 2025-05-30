Módulos de python diseñados especialmente para el manejo de rutas

## Comandos básicos OS

## Comandos básicos Pathlib
## Objetivo

Crear la ruta _“./data/raw/”_ independiente del sistema operativo. Ahora usaremos _pathlib_, otro módulo de Python.

## Implementación

Dentro del notebook de jupyter:

```
import pathlib

pathlib.Path()  # Genera un objeto Unix Path o 

CURRENT_DIR = pathlib.Path().resolve()  # Path local completo
DATA_DIR = CURRENT_DIR.parent.joinpath("data", "raw")  # Directorio objetivo

DATA_DIR.exists()  # Revisa si el directorio existe
DATA_DIR.is_dir()  # Revisa si es un directorio
```

Utiliza el método _“parent”_ para obtener el directorio padre y de ahí concatenar el path de las carpetas _“data”_ y _“raw”_.

Puedes crear una carpeta dentro de un directorio, usando el método _“mkdir”_:

```
DATA_DIR.joinpath("<nombre_carpeta>").mkdir()
```

Para buscar la ruta de un archivo dentro del proyecto, usando regex:

```
list(DATA_DIR.glob("<nombre_archivo>"))
```