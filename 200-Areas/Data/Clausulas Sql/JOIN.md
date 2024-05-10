[[Clausulas de definición de tablas]] | [[USING]]
La cláusula `JOIN` se utiliza para combinar filas de dos o más tablas en función de una condición de unión. Puedes usar diferentes tipos de `JOIN` según el tipo de combinación que necesites.
La cláusula `ON` se utiliza junto con `JOIN` para especificar la condición de unión entre las tablas. Define cómo se relacionan las filas de una tabla con las filas de otra tabla en la combinación.

```sql
SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.column_name = table2.column_name;
---
SELECT column1, column2, ...
FROM table1
JOIN table2 ON table1.column_name = table2.column_name;
```

### INNER JOIN
```sql
--CLAUSULA ON: Inner join de la tabla countries y economies union por el campo code
SELECT c.code AS country_code, c.name, e.year, e.inflation_rate
FROM countries AS c
INNER JOIN economies AS e
ON c.code = e.code;

--CLAUSULA USING(): Inner join de la tabla presidents y prime_ministers unidas por el campo country
SELECT p1.country, p1.continent, prime_minister, president
FROM prime_ministers AS p1
INNER JOIN presidents AS p2
USING(country);
```

