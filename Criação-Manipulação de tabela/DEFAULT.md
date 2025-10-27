Em algumas tabelas quando criamos, passamos o NOT NULL, dizendo que é um dado que deve ser preenchido obrigatoriamente, mas alguns não tem.

Nesses que não contem, podemos passar o DEFAULT, para que ao inves de ficar null quando o dado não for preenchido, nós colocarmos um valor padrão

```sql
  CREATE TABLE cliente(
  	id TEXT NOT NULL,
    nome VARCHAR(255),
    telefone VARCHAR(20),
    email VARCHAR(100) DEFAULT 'Sem email',
    endereco VARCHAR (255),
    PRIMARY KEY (id)
  );
```

Passei o default no email, está dizendo que caso a pessoa não coloque um valor em email, ao inves do null, ele vai colocar "sem email"