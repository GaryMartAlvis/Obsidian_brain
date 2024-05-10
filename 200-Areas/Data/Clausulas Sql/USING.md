[[JOIN]]

La cláusula USING se utiliza seguida la cláusula JOIN del nombre de la columna compartida entre paréntesis.

```sql
--Inner join de la tabla presidents y prime_ministers unidas por el campo country
SELECT p1.country, p1.continent, prime_minister, president
FROM prime_ministers AS p1
INNER JOIN presidents AS p2
USING(country);
```
