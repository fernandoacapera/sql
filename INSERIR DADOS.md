Para inserir valor você colocar INSERT INTO e na frente a tabela e dentro de parenteses você coloca as colunas, ficando dessa forma:

```sql
INSERT INTO tabelaclientes(
  id_cliente,
  nome_cliente,
  informacoes_de_contato,
  endereco_cliente
 )
```

Depois disso, você coloca os valores que vão receber passando abaixo o VALUES
```sql
 VALUES (
   '1',
   'Fernando',
   'fernandocapera2019@gmail.com',
   'rua flores - casa 1'
 );
```

Dessa forma, ele segue na sequencia, id_cliente recebe 1, nome_cliente recebe fernando e assim por diante.

Para colocar mais valores ao mesmo tempo, coloca virgula depois que fechar o parenteses no VALUES, abrir um novo parenteses e ir fazendo quantas vezes for necessário
```sql
 VALUES (
   '1',
   'Fernando',
   'fernandocapera2019@gmail.com',
   'rua flores - casa 1'
 ),
 (
   '2',
    'João Santos', 
    'joao@email.com', 
    'rua zé'
    );
```

<hr>

Inserir dados de outra tabela:
Quero pegar da tabelapedidos os pedidos que sejam maior ou igual a 400 e passar para uma nova tabela chamada tabela_gold

```sql
INSERT INTO tabelapedidosgold(
  ID_pedidos_gold,
  Data_do_pedido_gold,
  Status_gold,
  total_de_pedido_gold,
  cliente_gold,
  data_do_envio_estimada_gold
 )
 SELECT 
 id,
 data_do_pedido,
 status,
 total_do_pedido,
 cliente,
 data_de_envio_estimada
 FROM tabelapedidos
 WHERE total_do_pedido >= 400;
 ```