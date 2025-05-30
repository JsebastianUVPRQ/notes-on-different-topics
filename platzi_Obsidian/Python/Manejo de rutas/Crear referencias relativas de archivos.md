## Objetivo

Necesitamos encontrar una forma de evitar que nuestro proyecto se rompa cuando movamos de lugar un archivo dentro del proyecto, para esto usaremos Referencias Relativas.

## Implementación

**Usando PyProjRoot:**

``` Python
import pyprojroot

pyprojroot.here()  # Esto es un Posix Path (pathlib)
pyprojroot.here().joinpath("data", "raw") 
```

- El path en pyprojroot se construye desde la raíz, no desde el path del archivo que lo ejecuta.
- Puedes mover el archivo a cualquier parte de la carpeta del proyecto, pero los paths no se romperán.

**Usando PyHere:**

``` Python
import pyhere

pyhere.here()  # También regresa un Posix Path
```

- El directorio que regresa es el directorio padre del directorio actual.

## Comparación

Estas dos líneas de código regresan el mismo resultado:

```Python
pyprojroot.here("data").joinpath("raw")
pyhere.here().resolve() / "data" / "raw"
```

- Estas dos librerías sirven para crear shortcuts. Para esto, se puede usar la siguiente función:

```Python
def make_dir_function(dir_name):
    def dir_function(*args):
        return pyprojroot.here()joinpath(dir_name, *args)
    return dir_function


data_dir = make_dir_function("data")
data_dir("raw", "pathlib")  # Devuelve el path personalizado
```