
Passando condição

AND = e
OR = ou
BETWEEN = de um tanto até um tanto

Exemplos:

```sql
SELECT *
FROM coluna
WHERE name = 'Fernando' AND sobrenome = 'Capera';
```
OS 2 tem que ser verdadeiros

```sql
SELECT *
FROM coluna
WHERE name = 'Fernando' OR sobrenome = 'Capera';
```

Um dos 2 tem que ser verdadeiros

```sql
SELECT *
FROM coluna
WHERE idade BETWEEN 0 AND 10;
```
Vai filtrar a idade do valor 0 até o valor 10


IN:

```sql
SELECT *
FROM coluna
WHERE idade IN (10,20,30);
```
Pode filtrar dessa forma também (mesma coisa de OR). Então terá a idade de 10 ou 20 ou 30

Outro exemplo:

```sql
SELECT *
FROM coluna
WHERE pais IN ('German', 'Franch');
```

pais ou german ou franch