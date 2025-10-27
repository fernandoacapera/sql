
Caso eu tenha uma coluna que os dados sejam string e eu quero mudar o tipo

Por exemplo:

Tenho uma coluna string que está em formato (YYYY-MM-DD), e quero mudar para o tipo de data e selecionar todos os eventos após '2023-01-01'.

```sql
SELECT *
FROM eventos
WHERE CAST(data_string AS DATE) > 2023-01-01
```

OBS: não converte definitivamente, toda vez que você for usar para alguma filtragem ou algo relacionado, você tem que passar o cast com as tipo