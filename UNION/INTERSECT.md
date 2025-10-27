Retorna os registros comuns entre as 2 tabelas

![[Pasted image 20251022163848.png]]
Sintaxe:
```sql
SELECT id, val
FROM left_table
INTERSECT
SELECT id,val
FROM right_table;
```