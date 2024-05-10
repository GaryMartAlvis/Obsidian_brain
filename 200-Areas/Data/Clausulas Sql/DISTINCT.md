[[Clausulas de selección]]

La cláusula `DISTINCT` se utiliza dentro de la cláusula `SELECT` para eliminar filas duplicadas en el resultado. Esto significa que solo se mostrarán valores únicos en la columna o columnas especificadas.

```sql
SELECT DISTINCT column1, column2, ...
FROM table_name;
```