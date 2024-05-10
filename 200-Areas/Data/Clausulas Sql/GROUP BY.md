[[Clausulas de definición de tablas]]

La cláusula `GROUP BY` en SQL se utiliza principalmente en consultas que involucran funciones de agregación como `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`, etc. Esta cláusula agrupa filas que tienen los mismos valores en una o más columnas especificadas y permite aplicar funciones de agregación sobre cada grupo de filas.

Por ejemplo, supongamos que tienes una tabla de ventas con las siguientes columnas: `id_venta`, `id_producto`, `cantidad`, `precio_unitario`. Si deseas obtener la cantidad total vendida por producto, agrupando por `id_producto`, usarías la cláusula `GROUP BY` de la siguiente manera:

```sql
SELECT id_producto, SUM(cantidad) AS cantidad_total
FROM ventas
GROUP BY id_producto;
```