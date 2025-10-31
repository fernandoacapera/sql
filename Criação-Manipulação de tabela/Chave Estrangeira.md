Chave estrangeira é a coluna que se relaciona em mais de uma tabela, por exemplo:

 ***CHAVE ESTRANGEIRA SEMPRE LIGADA A UMA CHAVE PRIMARIA***

Tenho a tabela categoria que tem ID_Categoria

Também tenho a tabela produto que dentro da tabela tem a coluna categoria

Quando for criar uma tabela, deve colocar que ela é uma chave estrangeira dessa forma

```sql
FOREIGN KEY (coluna_da_minha_coluna) REFERENCES tabela_que_vai_ser_relacionada (coluna_da_tabela_relacionada)
```

Por exemplo: 
```sql
CREATE TABLE tabelaprodutos(
	ID_Produto INT PRIMARY KEY,
	nome_produto VARCHAR (250),
  	descriao TEXT,
  	categoria INT,
  	preco_de_compra DECIMAL (10, 2),
  	unidade VARCHAR (50),
  	fornecedor INT,
  	data_de_inclusao DATE,
  	FOREIGN KEY (categoria) REFERENCES tabelacategorias (id_categoria),
  	FOREIGN KEY (fornecedor) REFERENCES tabelafornecedores (id)
);
```

