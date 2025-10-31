
UNION ALL pega duas tabelas e retorna todos os registros das duas incluindo repetições

![[Pasted image 20251022162342.png]]Sintaxe:
```sql
SELECT id, val
FROM left_table
UNION ALL
SELECT id,val
FROM right_table;
```