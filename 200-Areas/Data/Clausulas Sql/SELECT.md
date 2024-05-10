[[Clausulas de selección]]

Comando para seleccionar columnas de una tabla.
Parámetros

_*_   : El asterisco corresponde a la selección de todas las columnas dentro de una tabla.
```sql
SELECT *
...;
```

AS: Palabra reservada para renombrar una columna
```sql
SELECT fiel_name AS name
...;
```

DISTINCT(): Envuelve la el nombre de la columna para que el resultado que se retorna sean únicos
```sql
SELECT DISTINCT(field_name)
...;
```

COUNT(): Cuenta registros se puede combinar con diferentes parámetros tales como.
```sql
SELECT COUNT(*) --Cuenta todos los registros de la tabla
...;
SELECT COUNT(field_name) --Cuenta todos los registros del campo
...;
```

---
