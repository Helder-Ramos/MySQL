
# 📘 Resumo de Comandos MySQL

## 🔹 Criar e selecionar banco de dados

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `CREATE DATABASE nome_do_banco;` | `CREATE DATABASE ong_animais;` | Cria um novo banco de dados |
| `USE nome_do_banco;` | `USE ong_animais;` | Seleciona o banco a ser usado |

## 🔹 Criar tabela

```sql
CREATE TABLE nome_da_tabela (
  campo1 TIPO,
  campo2 TIPO,
  campo3 TIPO
);
```

## 🔹 Inserir dados

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `INSERT INTO tabela (campo1, campo2) VALUES (v1, v2);` | `INSERT INTO doadores (nome, email) VALUES ('Ana', 'ana@gmail.com');` | Inserção de dados em campos específicos |

## 🔹 Consultar dados

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `SELECT * FROM tabela;` | `SELECT * FROM doadores;` | Retorna todos os registros |
| `SELECT * FROM tabela WHERE condicao;` | `SELECT * FROM doadores WHERE nome = 'Ana';` | Consulta com filtro |

## 🔹 Atualizar dados

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `UPDATE tabela SET campo = valor WHERE condicao;` | `UPDATE doadores SET email = 'novo@email.com' WHERE nome = 'Ana';` | Atualiza registros existentes |

## 🔹 Excluir dados

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `DELETE FROM tabela WHERE condicao;` | `DELETE FROM doadores WHERE nome = 'Ana';` | Exclui registros com base em condição |

## 🔹 Alterar estrutura da tabela

| Comando | Exemplo | Observação |
|--------|---------|------------|
| `ALTER TABLE tabela ADD COLUMN campo TIPO AFTER outro_campo;` | `ALTER TABLE doadores ADD COLUMN cidade VARCHAR(50) AFTER email;` | Adiciona nova coluna |
| `ALTER TABLE tabela ADD COLUMN campo TIPO FIRST;` | `ALTER TABLE doadores ADD COLUMN id INT FIRST;` | Adiciona coluna no início |
| `ALTER TABLE tabela DROP COLUMN campo;` | `ALTER TABLE doadores DROP COLUMN cidade;` | Remove uma coluna |
| `ALTER TABLE tabela CHANGE COLUMN antigo novo NOVO_TIPO;` | `ALTER TABLE doadores CHANGE COLUMN telefone celular VARCHAR(20);` | Renomeia e/ou altera tipo da coluna |
| `ALTER TABLE tabela MODIFY COLUMN campo NOVO_TIPO;` | `ALTER TABLE doadores MODIFY COLUMN email VARCHAR(150);` | Altera tipo da coluna |
| `ALTER TABLE tabela RENAME TO novo_nome;` | `ALTER TABLE doadores RENAME TO cadastro_doadores;` | Renomeia a tabela |

## 🔹 Exemplo completo de criação de tabela

```sql
CREATE TABLE doadores (
  id_doador INT AUTO_INCREMENT PRIMARY KEY,
  nome VARCHAR(100),
  email VARCHAR(100),
  telefone VARCHAR(20)
);
```

---

✅ **Dica:** Para estudar e documentar seus projetos no GitHub, o formato `.md` (Markdown) é ideal para deixar seu conteúdo bem organizado e visual.

