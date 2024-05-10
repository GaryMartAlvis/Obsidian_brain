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

