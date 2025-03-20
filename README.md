# Comandos_SQL
Comandos mais utilizados no SQL 


Aqui estão alguns dos comandos mais usados no **MySQL**, organizados por categoria:

---

### 📌 **Comandos Básicos**
```sql
SHOW DATABASES; -- Lista todos os bancos de dados
USE nome_do_banco; -- Seleciona um banco de dados para usar
SHOW TABLES; -- Lista todas as tabelas do banco de dados selecionado
DESC nome_da_tabela; -- Exibe a estrutura de uma tabela
SHOW COLUMNS FROM nome_da_tabela; -- Exibe as colunas de uma tabela
SHOW CREATE TABLE nome_da_tabela; -- Exibe o comando SQL usado para criar uma tabela
```

---

### 📌 **Gerenciamento de Bancos de Dados**
```sql
CREATE DATABASE nome_do_banco; -- Cria um novo banco de dados
DROP DATABASE nome_do_banco; -- Exclui um banco de dados
ALTER DATABASE nome_do_banco CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci; -- Altera o charset do banco
```

---

### 📌 **Gerenciamento de Tabelas**
```sql
CREATE TABLE nome_da_tabela (
    id INT AUTO_INCREMENT PRIMARY KEY,
    nome VARCHAR(100) NOT NULL,
    idade INT,
    email VARCHAR(255) UNIQUE
); -- Cria uma tabela

DROP TABLE nome_da_tabela; -- Exclui uma tabela

ALTER TABLE nome_da_tabela ADD COLUMN telefone VARCHAR(15); -- Adiciona uma nova coluna

ALTER TABLE nome_da_tabela MODIFY COLUMN idade SMALLINT; -- Modifica o tipo de uma coluna

ALTER TABLE nome_da_tabela DROP COLUMN telefone; -- Remove uma coluna

RENAME TABLE nome_antigo TO nome_novo; -- Renomeia uma tabela
```

---

### 📌 **Comandos CRUD (Create, Read, Update, Delete)**
#### 🔹 **Inserir dados (CREATE)**
```sql
INSERT INTO nome_da_tabela (nome, idade, email) 
VALUES ('João', 25, 'joao@email.com');
```
#### 🔹 **Consultar dados (READ)**
```sql
SELECT * FROM nome_da_tabela; -- Seleciona todos os registros

SELECT nome, idade FROM nome_da_tabela WHERE idade > 20; -- Filtra registros

SELECT COUNT(*) FROM nome_da_tabela; -- Conta o número de registros
```
#### 🔹 **Atualizar dados (UPDATE)**
```sql
UPDATE nome_da_tabela SET idade = 26 WHERE nome = 'João';
```
#### 🔹 **Excluir dados (DELETE)**
```sql
DELETE FROM nome_da_tabela WHERE nome = 'João';
DELETE FROM nome_da_tabela; -- CUIDADO! Remove todos os registros!
```

---

### 📌 **Comandos Avançados**
```sql
CREATE INDEX idx_nome ON nome_da_tabela (nome); -- Cria um índice para melhorar a busca

DROP INDEX idx_nome ON nome_da_tabela; -- Remove um índice

CREATE VIEW minha_view AS 
SELECT nome, idade FROM nome_da_tabela WHERE idade > 18; -- Cria uma view

DROP VIEW minha_view; -- Remove uma view

GRANT ALL PRIVILEGES ON nome_do_banco.* TO 'usuario'@'localhost' IDENTIFIED BY 'senha'; -- Concede permissões

FLUSH PRIVILEGES; -- Atualiza as permissões
```

Quer algo mais específico?
