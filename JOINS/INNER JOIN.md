Procura registros em amabas as tabelas que correspondem um determinado campo

![[Pasted image 20251021090444.png]]
Exemplo:

![[Pasted image 20251021090459.png]]

Para fazer essa junção:

```sql
SELECT p2.country, p2.continent, prime_minister, president
FROM presidents as p1
INNER JOIN prime_ministers AS p2
ON p1.country = p2.country
```

FROM eu pego meu banco de dados presidents e e no inner join eu pego o banco de dados prime_ministers e coloco um alias nos 2 (p1, p2)

SELECT eu coloco o country e continent e coloco o alias p2 para mostrar que é a coluna do banco de dados prime_minister e para o que é do banco de dados presidents, eu passo direto os valores (prime_minister, president), pois já está selecionado no FROM

no ON eu falo que p1.country - p2.country para filtrar apenas os valores em comum que contem nas 2 tabelas.

Da para ver quais são pela imagem acima também.

Resultando nessa visualização:

![[Pasted image 20251021091026.png]]

<hr>
Se verificar, usamos `ON p1.country = p2.country`, mas podemos usar ´`USING(country)` para unir 2 nomes de colunas idênticos
