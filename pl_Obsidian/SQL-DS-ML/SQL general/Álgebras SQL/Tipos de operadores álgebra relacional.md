### Operadores unarios.
- Requieren una relación o tabla para funcionar. 
- Proyección (π): Equivale al comando Select. Saca un número de columnas o atributos sin necesidad de hacer una unión con una segunda tabla. π<Nombre, Apellido, Email>(Tabla_Alumno) ⠀ 
- Selección (σ): Equivale al comando [[WHERE]]. Consiste en el filtrado de de tuplas. σ<Suscripción=Expert>(Tabla_Alumno). ⠀

### Operadores binarios.
- Requieren más de una tabla para operar. 
- Producto cartesiano (x): Toma todos los elementos de una tabla y los combina con los elementos de la segunda tabla. Docentes_Quinto_A x Alumnos_Quinto_A ⠀ 
- Unión (∪): Obtiene los elementos que existen en una de las tablas o en la otra de las tablas. Alumnos_Quinto_A  U  Alumnos_Quinto_B ⠀ 
- Diferencia (-): Obtiene los elementos que existe en una de las tablas pero que no corresponde a la otra tabla. Alumnos_planExpertPlus - Alumnos_planFree