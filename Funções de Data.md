
STRFTIME

Se meus dados tem ano-mes-dia e eu quero mudar a sequencia ou simplesmente pegar apenas o ano e mês, posso fazer dessa forma:

```sql
SELECT id_colaborador, STRFTIME('%y/%m', datainicio) FROM licencas;
```

No código acima eu peguei o id do colaborador apenas para verificar a data de inicio na empresa por colaborador.

Chamei a função ´STRFTIME´ e passei que queria o ano/mes e uma virgula passando em seguida a coluna da data.![[Pasted image 20251027104616.png]]


Agora se eu tiver uma data de inicio e uma data de fim e ver o intervalo de tempo (em dias) entre eles, eu posso utilizar a função `JULIANDAY`

```sql
SELECT id_colaborador, JULIANDAY(datatermino) - JULIANDAY(datacontratacao) FROM historicoemprego
WHERE datatermino IS NOT NULL;
```


Para extrair a data de um valor de data e hora ou para obter a data atual. Ela retorna a data no formato 'YYYY-MM-DD'.

- **Sintaxe Básica:** `DATE('now', '[modificador]')`
- **Exemplo de Uso:** Para obter a data atual:
- 
```sql
  SELECT DATE('now');
```

Para obter a data 10 dias atrás:
```sql
  SELECT DATE('now', '-10 days');
```



Para extrair a hora de um valor de data e hora ou para obter a hora atual. Ela retorna a hora no formato 'HH:MM:SS'.

- **Sintaxe Básica:** `TIME('now', '[modificador]')`
- - **Exemplo de Uso:** Para obter a hora atual:
```sql
  SELECT TIME('now');
```


Para retornar tanto a data quanto a hora no formato 'YYYY-MM-DD HH:MM:SS'. Pode ser usada para obter o momento atual ou converter/modificar valores de data e hora existentes.

- **Sintaxe Básica:** `DATETIME('now', '[modificador]')`
- **Exemplo de Uso:** Para obter a data e hora atuais:
```sql
  SELECT DATETIME('now');
```

Para obter a data e hora exatas 1 ano no futuro:
```sql
  SELECT DATETIME('now', '+1 year');
```


### Função CURRENT_TIMESTAMP

- **Funcionalidade:** `CURRENT_TIMESTAMP` é uma função de conveniência que retorna a data e hora atuais no formato 'YYYY-MM-DD HH:MM:SS'. É equivalente a usar `DATETIME('now')`.
- **Sintaxe Básica:** `CURRENT_TIMESTAMP`
- **Exemplo de Uso:** Para obter o timestamp atual:
```sql
  SELECT CURRENT_TIMESTAMP;
```

### Considerações Importantes

- Os modificadores, como '-10 days' ou '+1 year', são usados para ajustar a data/hora retornada. Eles podem ser combinados para representar períodos específicos de tempo.
- Essas funções são extremamente úteis para gerar e manipular dados de data e hora, permitindo cálculos temporais, conversões e a extração de componentes específicos.
- O conhecimento preciso de como as datas e horas são armazenadas e manipuladas em seu sistema de banco de dados é crucial para utilizar essas funções efetivamente e evitar erros comuns relacionados a fusos horários e formatos.