```sql
SELECT ('A pessoa colaboradora' || nome || 'de CPF ' || cpf|| 'possui o seguinte endereço' || endereco)
```

Para deixar todos com letra maiuscula:
```sql
SELECT UPPER('A pessoa colaboradora' || nome || 'de CPF ' || cpf|| 'possui o seguinte endereço' || endereco)
```

Para deixar todos com letra minuscula
```sql
SELECT LOWER('A pessoa colaboradora' || nome || 'de CPF ' || cpf|| 'possui o seguinte endereço' || endereco)
```

Para remover espaços (ou outro conjunto especificado de caracteres)

Sintaxe: TRIM(string, caractere_para_trimar)

Exemplo de Uso: Para remover espaços do início e do fim da coluna `nome`:
```sql
  SELECT TRIM(nome) FROM tabela;
```

Para retornar a posição de uma substring dentro de uma string.

**Sintaxe Básica:** `INSTR(string, substring)`

**Exemplo de Uso:** Para encontrar a posição da substring 'abc' dentro da coluna `descricao`:

```sql
  SELECT INSTR(descricao, 'abc') FROM tabela;
```
Isso retornará um número indicando a posição inicial de 'abc' em `descricao`, ou 0 se 'abc' não for encontrado.


Para substituir todas as ocorrências de uma substring específica por outra substring dentro de uma string.

- **Sintaxe Básica:** `REPLACE(string, substring_a_substituir, substring_para_substituir)`
- 
- **Exemplo de Uso:** Para substituir 'hello' por 'hi' na coluna `saudacao`:
```sql
  SELECT REPLACE(saudacao, 'hello', 'hi') FROM tabela;
```


Para extrair uma parte de uma string com base em um ponto de início e um comprimento especificados.

- **Sintaxe Básica:** `SUBSTR(string, inicio[, comprimento])`

- **Exemplo de Uso:** Para extrair os primeiros 5 caracteres da coluna `comentario`:

```sql
  SELECT SUBSTR(comentario, 1, 5) FROM tabela;
```

Se `comprimento` não for especificado, `SUBSTR` retornará todos os caracteres a partir da posição `inicio` até o final da string.

### Considerações Importantes

- Ao trabalhar com `TRIM`, se nenhum caractere específico for fornecido para remoção, ele removerá espaços por padrão.
- A função `INSTR` é particularmente útil para localizar substrings e pode ser usada em operações mais complexas, como extrações condicionais ou verificação de presença de padrões.
- `REPLACE` é uma ferramenta poderosa para limpeza e formatação de dados, sendo capaz de alterar padrões específicos em uma grande quantidade de texto.
- `SUBSTR` é amplamente utilizada para cortar e analisar partes de strings, especialmente quando combinada com outras funções como `INSTR`.


<hr>
