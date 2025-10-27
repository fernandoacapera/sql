O Case tem a mesma ideia do que o if/else de Python

```sql
SELECT id_colaborador, cargo, salario,
CASE
WHEN salario < 3000 THEN 'Baixo'
WHEN salario BEETWEEN 3000 AND 6000 THEN 'Médio'
ELSE 'Alto'
END AS categoria_salario
FROM historicoemprego;
```

Case fica no select também.

Caso queira criar uma condição, coloco o CASE e depois veio com WHEN que seria o "se" e depois o THEN que seria "entao".

No exemplo acima seria

Se o salario for menor que 3000, então é baixo
Se o salário for entre 3000 e 6000 então é médio
se não for nenhuma das opções acima(ELSE) retorne 'Alto'

Após dar todas as condições, coloque um END e um apelido
