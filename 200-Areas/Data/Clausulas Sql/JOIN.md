[[Clausulas de definición de tablas]] | [[USING]]

## TIPO DE UNIONES
La cláusula `JOIN` se utiliza para combinar filas de dos o más tablas en función de una condición de unión. Puedes usar diferentes tipos de `JOIN` según el tipo de combinación que necesites.
La cláusula `ON` se utiliza junto con `JOIN` para especificar la condición de unión entre las tablas. Define cómo se relacionan las filas de una tabla con las filas de otra tabla en la combinación.

![[Pasted image 20240513161222.png]]

Query example.
```sql
SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.column_name = table2.column_name;
---
SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.column_name = table2.column_name;
```

---

## UNIONES EXTERNAS
### INNER JOIN

**Combinación externa**
La cláusula `INNER JOIN` en SQL se utiliza para combinar filas de dos o más tablas en base a una condición de unión. Cuando se usa `INNER JOIN`, solo se devuelven las filas que tienen una coincidencia en las tablas que se están uniendo según la condición especificada.

![[Pasted image 20240513155821.png]]

```sql
--CLAUSULA ON: Inner join de la tabla countries y economies union por el campo code
SELECT c.code AS country_code, c.name, e.year, e.inflation_rate
FROM countries AS c
INNER JOIN economies AS e
ON c.code = e.code_economies;

--CLAUSULA USING(): Inner join de la tabla presidents y prime_ministers unidas por el campo country
SELECT p1.country, p1.continent, prime_minister, president
FROM prime_ministers AS p1
INNER JOIN presidents AS p2
USING(country);
```

Tips 1: Cuando los nombre de campos no se repiten en las tablas no es requerido en el SELECT especificar el alias de la tabla donde pertenece el campo.


#### UNIONES MULTIPLES CON INNER JOIN
```sql
SELECT name, p.year, fertility_rate, e.year, unemployment_rate
FROM countries AS c             --Primera tabla izquierda
INNER JOIN populations AS p     --Segunda tabla derecha
ON c.code = p.country_code
INNER JOIN economies AS e       --Tercera tabla derecha
ON c.code = e.code
AND e.year = p.year;
```

---

### LEFT JOIN

**Combinación externa**
Esta clausula realiza uniones de tablas uniendo la totalidad de la tabla de la izquierda y solo las coincidencias de la tabla de la derecha. 

![[Pasted image 20240513161808.png]]


---

### RIGHT JOIN

**Combinación externa**
Esta clausula realiza uniones de tablas con la totalidad de los datos de la tabla derecha y solo las coincidencias de la tabla izquierda.

![[Pasted image 20240513161737.png]]

---

### FULL JOIN

**Combinación externa**
Esta clausula combina la unión izquierda y una unión derecha para formar una unión completa.
Nota: La clausula `FULL OUTER JOIN` también se puede usar para devolver el mismo resultado.

![[Pasted image 20240514151056.png]]

Ejemplo de consulta.
```sql
SELECT 
	name AS country, 
	code, 
	region, 
	basic_unit
FROM countries
FULL JOIN currencies
USING (code)
WHERE region = 'North America'
OR name IS NULL
ORDER BY region;
```

#### Encadenado FULL JOIN

```sql
SELECT
    c1.name AS country,
    region,
    l.name AS language,
    basic_unit,
    frac_unit
FROM countries as c1
FULL JOIN languages as l   --Primera unión full
USING(code)
FULL JOIN currencies AS c2 --Segunda unión full
USING(code)
WHERE region LIKE 'M%esia';
```

## UNIONES INTERNAS
### CROSS JOIN

**Unión interna**
Esta clausula crea todas las combinaciones posibles de dos tablas.

Diagrama de la clausula `CROSS JOIN`.
![[Pasted image 20240514155855.png]]

Sintaxis de la clausula
```sql
SELECT id1, id2
FROM table1
CROSS JOIN table2;
```

Nota: La sintaxis utilizada en una consulta con esta clausula es mínima y no especifica `ON` o `USING` con `CROSS JOIN`.