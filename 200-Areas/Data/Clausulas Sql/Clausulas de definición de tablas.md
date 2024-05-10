[[SQL]] | [[FROM]], [[JOIN]], [[WHERE]], [[GROUP BY]], [[HAVING]] 

Las cláusulas de definición de tablas permiten especificar las fuentes de datos, combinar tablas, aplicar filtros y realizar operaciones de agrupación en tus consultas.

```sql
FROM table_name 
--Se utiliza para especificar las tablas de las cuales se seleccionarán los datos. 
JOIN ON 
--Se utiliza para combinar filas de dos o más tablas en función de una condición de unión. 
INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN 
--Son variantes de la cláusula `JOIN` que especifican diferentes tipos de combinaciones de tablas.
WHERE
--Se utiliza para filtrar filas antes de que se apliquen las funciones de agregación o se seleccionen las columnas.
GROUP BY
--Se utiliza para agrupar filas basadas en los valores de una o más columnas.
HAVING
--Se utiliza para filtrar grupos de filas después de que se han aplicado las funciones de agregación y la cláusula `GROUP BY`.
```