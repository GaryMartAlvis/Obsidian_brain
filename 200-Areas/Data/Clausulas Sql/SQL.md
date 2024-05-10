[[Data]]
[[Clausulas de selección]], [[Clausulas de definición de tablas]], [[Clausulas de ordenamiento y limitación]]
Structure Query Language - Lenguaje de consulta estructurado

### Orden de ejecución de las consultas SQL

```sql
FROM 
--Step1: La primera parte de una consulta SQL suele ser la cláusula `FROM`, que especifica las tablas de las que se extraerán los datos.

WHERE
--Step2: Filtra registros individuales, Después de la cláusula `FROM`, se aplica la cláusula `WHERE`, que filtra las filas de las tablas especificadas en la cláusula `FROM` según las condiciones proporcionadas.

GROUP BY
--Step3: Si se está utilizando la cláusula `GROUP BY`, los datos se agrupan en conjuntos según los valores de las columnas especificadas en esta cláusula.

HAVING
--Step4: Filtra registros agrupados, La cláusula `HAVING` se usa para filtrar grupos de datos creados por la cláusula `GROUP BY` basándose en condiciones específicas. Esta cláusula se aplica después de la agrupación de datos.

SELECT
--Step5: La cláusula `SELECT` se utiliza para seleccionar las columnas que se mostrarán en los resultados de la consulta. Aquí es donde se aplican las funciones de agregación si se están utilizando (`SUM()`, `COUNT()`, `AVG()`).

ORDER BY
--Step6: La cláusula `ORDER BY` se usa para ordenar los resultados de la consulta según una o más columnas especificadas. Esta cláusula se aplica después de que se han seleccionado y agrupado los datos.

LIMIT/OFFSET
--Step7: Si se desea limitar el número de filas devueltas por la consulta o se desea implementar paginación, se usa la cláusula `LIMIT` junto con `OFFSET`.
```