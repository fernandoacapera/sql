Para criar tabelas, é usado a sintaxe:

```sql
CREATE TABLE nome_da_tabela (
	id INT PRIMARY KEY,
	nome VARCHAR(250),
	etc)
```

Para criar um Schema (Esquema)
```sql
CREATE SCHEMA vendas;
```

Criar um banco de dados:

```sql
CREATE DATABASE biblioteca;
```

Estrutura:

```yaml
BancoDeDados: loja_online
 ├── Schema: vendas
 │     ├── Tabela: pedidos
 │     └── Tabela: clientes
 └── Schema: estoque
       ├── Tabela: produtos
       └── Tabela: fornecedores
       
```

<hr>

Para alterar algo na tabela, podemos usar o ALTER TABLE, por exemplo, quero adicionar mais uma coluna na tabela.

```sql
ALTER TABLE tabela_clientes ADD endereco_cliente VARCHAR(250);
```
Explicando sintaxe:

ALTER TABLE tabela_clientes= tabela que vai ser alterada

ADD = como vou adicionar uma nova coluna, coloquei ADD (adicionar)

endereco_cliente = nome da coluna nova

VARCHAR (250) = tipo da coluna

Para apagar uma coluna:
```sql
ALTER TABLE nome_da_tabela
DROP COLUMN nome_da_coluna;
```

<hr>

Para apagar uma tabela:

```sql
DROP TABLE tabelaclientes;
```
