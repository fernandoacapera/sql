Para modificar os dados da tabela usamos o update

Por exemplo, tenho uma tabela de pedidos e quero mudar o status de processando para enviar:

```sql
UPDATE tabelapedidos SET status = 'Enviado' WHERE status = 'Processando';
```