[[Clausulas de definición de tablas]]

La cláusula WHERE  filtra registros individuales.
`WHERE` es una cláusula en SQL que se utiliza para filtrar filas de una tabla o vista. Cuando ejecutas una consulta SQL que incluye la cláusula `WHERE`, estás especificando un conjunto de condiciones que deben cumplir las filas para ser incluidas en el resultado de la consulta.

Entre las clausulas que se pueden utilizar como parámetros están:
# NULL
--- start-multi-column: ID_lvaf
```column-settings
Number of Columns: 2
Largest Column: standard
```

### IS NULL
Esta condición se refiere a registros vacios
```sql
...
WHERE field_name IS NULL;
```

--- column-break ---
### IS NOT NULL
Esta condición se refiere a registros con datos (Excluye registros vacios)
```sql
...
WHERE field_name IS NOT NULL;
```



--- end-multi-column


