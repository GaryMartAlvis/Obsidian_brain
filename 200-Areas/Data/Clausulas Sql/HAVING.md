[[Clausulas de definición de tablas]]

Filtra registros agrupados por la [[GROUP BY]]. Esta cláusula es utilizada para filtrar resultados de agrupaciones.

```sql
SELECT 
	release_year,
	COUNT(title) AS title_count
FROM films
GROUP BY release_year
HAVING COUNT(title) > 10;
```
