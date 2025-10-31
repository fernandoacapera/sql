![[Pasted image 20251022171849.png]]

Vai retornar os valores que não estão na tabela da direita

Sintaxe:

```SQL
SELECT country, president
FROM presidents
WHERE continent LIKE '%America'
AND country NOT IN
(SELECT country
FROM states
WHERE indep_year < 1800);
```

Retorna os paises da américa que conqusitaram a idependencia depois de 1800