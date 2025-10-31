Uma semijunção selecionada registros da primeira tabela em que uma condição é atendida na segunda tabela

```sql
SELECT president, country, continent
FROM presidents
WHERE country IN 
(SELECT country
FROM states
WHERE indep_year < 1800);
```

Retorna os presidentes, paises e continente onde o pais teve a independência antes de 1800 

DENTRO DO () está praticamente assim: 
WHERE country IN ('Estados Unidos', 'França', 'Brasil', ...)
O select dentro do () é para mostrar essa lista dentro do where e ele filtrar
