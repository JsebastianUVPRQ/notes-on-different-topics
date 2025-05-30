- **A: Atomicity** -> Separar las funciones desarrolladas en la BD como pequeñas tareas y ejecutarlas como un todo. Si alguna tarea falla se hace un rollback(Se deshacen los cambios)

- **C: Consistency** -> Todo lo que se desarrolló en base al objeto relacional. Los datos tienen congruencia.

- **I: Isolation (aislado)** -> Varias tareas ejecutándose al mismo tiempo dentro de la BD. Guarda datos en la **Bitácora** para evitar pérdidas inesperadas de información.

- **D: Durability** -> Puedes tener seguridad que la información no se perderá por un fallo catastrófico. PostgreSQL guarda la información en una Bitácora.
	![[Apunte_durability_PostgreSQL.png]]