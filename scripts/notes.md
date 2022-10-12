Repaso Sql

Sql es un lenguaje de programacion para bases de datos.Su traducción literal seria lenguaje estructurado de consultas (Structured query leanguage)


Sql es un lenguaje insensible a mayusculas y minusculas."select" == SELECT.

En sql las tablas tienen columnas que tendran informacion de cierto "tipo"

>Como buena practica los nombres de las tablas deben ser en "" PLURAL"

LLave primaria:con valor unico y no nulo

csv : es un formato de archivo muy popular en los negocios .A partir de xls se pueden exportar datos en csv y tambien importar."valores"separados por coma.

SELECT <colum>
FROM<table>;
````

La sentencia "WHERE" es para filtrar información

``sql
SELECT <column>
FROM <table>;
WHERE <column><condition>;
`````

##Ejemplo usando **AND**

``sql
SELECT name,country,area
FROM cities
WHERE area < 1100
AND country = 'Japan';
``

## Ejemplo usando **OR**

``sql
SELECT name,country,area
FROM cities
WHERE area < 1100
OR country = 'Japan';
``

## Ejemplo ordenando los resultados en forma
ascendente

``sql
SELECT name,country,area
FROM cities
ORDER BY area

##Ejemplo con WHERE,OR Y ORDER

``sql
SELECT name,country,area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area;
``
## Ejemplo descendente

``sql
SELECT name,country,area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area DESC;

##

## Ejemplo pais distinti a japon

``sql
SELECT name,country,area
FROM cities
WHERE area < 1100
OR country != 'Japan'
ORDER BY area DESC;

> Nota : distinto puede ser <> o !=

## Campos o columna alculados con AS (como) ordenar en forma descendentes

```sql
SELECT name,population/area AS density
FROM cities
ORDER BY density DESC;
``
##Ordenar los resultados en forma ascendentes

```sql
SELECT name,population/area AS density
FROM cities
ORDER BY density ASC;

## Contando elementos con su COUNT

``sql
SELECT COUNT(name)
From cities
WHERE country = 'India';
``

## Limitar los resultados con **Limit**

``sql
SELECT name,population/area AS density
FROM cities
ORDER BY density DESC
LIMIT 2;
``






