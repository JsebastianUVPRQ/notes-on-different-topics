## segundo valor más alto de colegiatura 
```sql
#PRIMERA FORMA
SELECT distinct colegiatura
FROM platzi.alumnos AS a1
WHERE 2 = (
	SELECT COUNT (DISTINCT colegiatura)
	FROM platzi.alumnos a2
	WHERE a1.colegiatura <= a2.colegiatura
);
#SEGUNDA FORMA
SELECT DISTINCT colegiatura
FROM platzi.alumnos
ORDER BY colegiatura DESC
LIMIT 1 OFFSET 1;
```

## Extraer la mitad de una tabla
```sql
SELECT * 
    FROM platzi.alumnos
    OFFSET ( SELECT COUNT(*)/2 FROM platzi.alumnos );
```

## Seleccionar    de un array
```sql
Select *
FROM (
	SELECT ROW_NUMBER() OVER() AS row_id, *
	FROM platzi.alumnos
) AS alumnos_with_row_num
WHERE row_id IN (1,5,10,12,15,20);
```
## Sacar año de una columna de fecha
```sql
SELECT EXTRACT (YEAR FROM fecha_incorporacion) AS anio_incorp
FROM platzi.alumnos
```

## Usar año como sub-query
```sql
SELECT *
FROM platzi.alumnos
WHERE (EXTRACT (YEAR FROM fecha_incorporacion)) = 2018;


SELECT *
FROM platzi.alumnos
WHERE (DATE_PART('YEAR', FECHA_INCORPORACION)) = 2019;
```

## Selectores de rango

```sql
SELECT *
FROM platzi.alumnos
WHERE tutor_id BETWEEN 1 AND 10;

SELECT int4range(1, 20) @>3;

--valor más alto 
SELECT UPPER(int8range(15,25));

--interseccion
SELECT int4range(10,20)*int4range(15,25);
```

## Matrícula más reciente
```sql

SELECT FECHA_INCORPORACION
FROM platzi.alumnos
ORDER BY fecha_incorporacion DESC
LIMIT 1; 

SELECT carrera_id, MAX(fecha_incorporacion)
FROM platzi.alumnos
GROUP BY carrera_id
ORDER BY carrera_id
```

## Tutor correspondiente a un alumno
```sql
SELECT  CONCAT(a.nombre, ' ', a.apellido,) AS alumno
		CONCAT(t.nombre, ' ', t.apellido) AS tutor
FROM platzi.alumnos AS a
	INNER JOIN platzi.alumnos AS t ON a.tutor_id = t.id;

--Lo que hace este query es asumir que el tutor con el tutor_id X de cada alumno es otro alumno con el mismo id, por eso te muestra los nombres y apellidos de profesores cuando en la table esta información no está, solo tenemos los nombres y apellidos de alumnos.

```

## Contar estudiantes 
```sql
SELECT carrera_id, COUNT(*) AS cuenta
FROM platzi.alumnos
GROUP BY carrera_id
ORDER BY cuenta DESC;
```

## nombre y apellido de la localización con más ventas

```sql
--Hace una semana tuve un test de SQL para una empresa donde me presentaban 3 tablas parecidas a las descritas en clase, y me pedían que **hiciera una query** (que si traducimos a los datos de este schema DB) trayendo una lista de los alumnos (customers) con su respectivo tutor_id (company) de la carrera (location) que tuviera más alumnos (customers). DE acuerdo a este test que por cierto no pude resolver en el tiempo indicado hago un query para esta DB equivalente
SELECT CONCAT(a.nombre, ' ', a.apellido), a.tutor_id FROM platzi.alumnos AS a JOIN platzi.carreras AS c ON c.id = a.carrera_id WHERE c.id = ( SELECT c.id FROM platzi.carreras AS c INNER JOIN platzi.alumnos AS a ON a.carrera_id = c.id GROUP BY c.id ORDER BY COUNT(*) DESC LIMIT 1);
```

## Profundizar en JOIN's
[Tutorial de youtube][https://www.youtube.com/watch?v=9yeOJ0ZMUYw]

