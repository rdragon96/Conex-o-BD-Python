# Sistema CRUD de Produtos com Python e MySQL

Este projeto é um sistema simples de cadastro de produtos desenvolvido em Python utilizando MySQL como banco de dados.  
O objetivo do projeto é praticar operações CRUD (Create, Read, Update e Delete) utilizando a biblioteca PyMySQL.

---

# Funcionalidades

O sistema permite:

- Cadastrar novos produtos
- Listar todos os produtos cadastrados
- Buscar produtos pelo código
- Atualizar informações dos produtos
- Remover produtos do banco de dados
- Conectar o Python ao MySQL

---

# Tecnologias Utilizadas

- Python 3
- MySQL
- Biblioteca PyMySQL

---

# Estrutura do Projeto

```bash
projeto/
│
├── main.py
├── README.md
```

---

# Instalação


## 1. Instale a biblioteca necessária

```bash
pip install pymysql
```

---

# Configuração do Banco de Dados

Abra o MySQL e execute os comandos abaixo:

```sql
CREATE DATABASE loja;

USE loja;

CREATE TABLE produtos (
    codigo INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(100),
    preco DECIMAL(10,2),
    categoria VARCHAR(100)
);
```

---

# Configuração da Conexão

No arquivo Python, configure os dados do seu banco:

```python
conexao = pymysql.connect(
    host='localhost',
    user='root',
    password='',
    database='loja',
    cursorclass=pymysql.cursors.DictCursor
)
```

Caso necessário, altere:

- host
- user
- password
- database

de acordo com sua configuração local.

---

# Explicação das Funções

## criar_conexao()

Responsável por criar a conexão com o banco de dados MySQL.

---

## inserir_produto(nome, preco, categoria)

Insere um novo produto na tabela.

### Exemplo:

```python
inserir_produto('Notebook', 3500.00, 'Eletrônicos')
```

---

## listar_produtos()

Lista todos os produtos cadastrados.

### Exemplo:

```python
listar_produtos()
```

---

## listar_produtos_codigo(id)

Busca um produto específico pelo código.

### Exemplo:

```python
listar_produtos_codigo(1)
```

---

## update_produto(nome, categoria, preco, codigo)

Atualiza os dados de um produto.

### Exemplo:

```python
update_produto('Mouse Gamer', 'Periféricos', 150.00, 1)
```

---

## deletar_produto(id)

Remove um produto do banco de dados.

### Exemplo:

```python
deletar_produto(1)
```

---

# Exemplo de Saída

```bash
Conexão criada com sucesso
Dados inseridos com sucesso.
```

---

# Conceitos Praticados

Neste projeto foram praticados conceitos como:

- CRUD em banco de dados
- Integração Python + MySQL
- Funções em Python
- Tratamento de erros com try/except
- Manipulação de queries SQL
- Uso de cursores
- Commit em banco de dados

---


# Autor

Desenvolvido por Rafael Santos.

- Graduando em Engenharia de Software
- Formado em Análise e Desenvolvimento de Sistemas
- Estudante de Data Science e Banco de Dados

---
```