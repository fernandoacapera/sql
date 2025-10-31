
Fazer o agrupamento

Sintaxe:
```sql
SELECT language, COUNT(title) AS count_title FROM films GROUP BY 
language;
```
Caso for usar Group BY com Order By, o group by vem antes

 ```sql
SELECT release_year, country, MAX(budget) AS max_budget

FROM films

GROUP BY release_year, country

ORDER BY release_year, country;
 ```
