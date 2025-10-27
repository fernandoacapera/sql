Para ver o tamanho de um dado usamos o LENGTH(coluna)

```sql
SELECT nome, LENGHT(cpf) qtd
FROM colaboradores
WHERE qtd = 11
```

No código acima eu pedi para printar o nome e o tamanho que tem os dados da coluna cpf e coloquei o apelido de qtd
Coloquei um where falando que a qtd tem que ser igual 11 (numero de cpf tem 11 digitos)