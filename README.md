# Sistema de Gerenciamento de Biblioteca

Este é um sistema simples de gerenciamento de biblioteca utilizando o SQLite. O sistema contém as tabelas **Autores**, **Livros** e **Empréstimos** para gerenciar as informações relacionadas a autores de livros, obras disponíveis e os empréstimos realizados.

## Funcionalidades

- Gerenciamento de autores
- Gerenciamento de livros
- Controle de empréstimos de livros

## Estrutura do Banco de Dados

### Tabela: `Autores`
| Campo           | Tipo    | Descrição                            |
|-----------------|---------|--------------------------------------|
| `AutorID`       | INTEGER | Chave primária, autoincremento        |
| `Nome`          | TEXT    | Nome do autor                         |
| `Nacionalidade` | TEXT    | Nacionalidade do autor                |

### Tabela: `Livros`
| Campo           | Tipo    | Descrição                                |
|-----------------|---------|------------------------------------------|
| `LivroID`       | INTEGER | Chave primária, autoincremento            |
| `Titulo`        | TEXT    | Título do livro                           |
| `AutorID`       | INTEGER | Chave estrangeira para `Autores`          |
| `AnoPublicacao` | INTEGER | Ano de publicação                         |
| `Genero`        | TEXT    | Gênero literário                          |

### Tabela: `Emprestimos`
| Campo            | Tipo    | Descrição                                           |
|------------------|---------|-----------------------------------------------------|
| `EmprestimoID`   | INTEGER | Chave primária, autoincremento                       |
| `LivroID`        | INTEGER | Chave estrangeira para `Livros`                      |
| `DataEmprestimo` | TEXT    | Data em que o livro foi emprestado                   |
| `DataDevolucao`  | TEXT    | Data de devolução (pode ser nula)                    |
| `NomeUsuario`    | TEXT    | Nome do usuário que pegou o livro emprestado         |

## Instalação

1. **Clone este repositório:**
    ```bash
    git clone https://github.com/seuusuario/sistema-biblioteca.git
    ```

2. **Instale o Python se ainda não tiver:**
    - [Download do Python](https://www.python.org/downloads/)

3. **Execute o script Python para criar e popular o banco de dados:**
    ```bash
    python nome_do_arquivo.py
    ```

## Dependências

Este projeto não possui dependências externas além do Python e do SQLite, que já está incluído por padrão no Python.

## Como Contribuir

1. Faça um fork do projeto
2. Crie uma branch com sua feature (`git checkout -b minha-feature`)
3. Faça commit das suas mudanças (`git commit -m 'Minha nova feature'`)
4. Faça um push para a branch (`git push origin minha-feature`)
5. Abra um Pull Request

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
