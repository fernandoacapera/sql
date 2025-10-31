Union recebe 2 tabelas como entrada e retorna todos os registros das duas tabelas

![[Pasted image 20251022142106.png]]Como já tem o id 1 e 4 no left, o do right é ignorado

Sintaxe:
```sql
SELECT id, val
FROM left_table
UNION
SELECT id,val
FROM right_table;
```

As colunas das tabelas não tem que ter necessariamente o mesmo nome, tem que ter apenas o mesmo tamanho