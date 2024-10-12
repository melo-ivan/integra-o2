# Biblioteca SQLite

Este projeto é um sistema de gerenciamento de uma biblioteca simples utilizando SQLite. Ele contém tabelas para Autores, Livros e Empréstimos, permitindo a inserção e consulta de dados de empréstimos de livros e seus respectivos autores.

## Estrutura do Banco de Dados

O banco de dados contém três tabelas:

- **Autores**: armazena informações sobre os autores dos livros.
- **Livros**: armazena detalhes sobre os livros, como título, autor e ano de publicação.
- **Empréstimos**: registra os empréstimos de livros, com a data de empréstimo, devolução e nome do usuário.

### Tabelas

#### 1. Autores

| Coluna         | Tipo      | Descrição                           |
|----------------|-----------|-------------------------------------|
| AutorID        | INTEGER   | ID único do autor (chave primária). |
| Nome           | TEXT      | Nome do autor.                      |
| Nacionalidade  | TEXT      | Nacionalidade do autor.             |

#### 2. Livros

| Coluna         | Tipo      | Descrição                           |
|----------------|-----------|-------------------------------------|
| LivroID        | INTEGER   | ID único do livro (chave primária). |
| Titulo         | TEXT      | Título do livro.                    |
| AutorID        | INTEGER   | ID do autor (chave estrangeira).    |
| AnoPublicacao  | INTEGER   | Ano de publicação do livro.         |
| Genero         | TEXT      | Gênero literário do livro.          |

#### 3. Empréstimos

| Coluna         | Tipo      | Descrição                           |
|----------------|-----------|-------------------------------------|
| EmprestimoID   | INTEGER   | ID único do empréstimo (chave primária). |
| LivroID        | INTEGER   | ID do livro emprestado (chave estrangeira). |
| DataEmprestimo | TEXT      | Data do empréstimo.                 |
| DataDevolucao  | TEXT      | Data da devolução (pode ser nulo).  |
| NomeUsuario    | TEXT      | Nome do usuário que fez o empréstimo. |

## Como executar o projeto

### Requisitos

- Python 3.x
- SQLite

### Executando o Projeto

1. Clone este repositório:

   ```bash
   git clone https://github.com/seu-usuario/biblioteca-sqlite.git
   cd biblioteca-sqlite
