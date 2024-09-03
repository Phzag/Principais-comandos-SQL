# Principais-comandos-SQL

# Banco de Dados Venda

## Descrição

Este repositório contém scripts SQL para gerenciar um banco de dados simples chamado `venda`. O banco de dados mantém registros de vendas para diversos cursos, incluindo o nome do curso, nome do aluno, estado do aluno e o valor da venda.

## Começando

Para usar esses scripts SQL, você precisa ter um servidor de banco de dados MySQL em funcionamento. Você pode executar os scripts usando um cliente MySQL ou através da interface de linha de comando do MySQL.

### Pré-requisitos

- Servidor MySQL (versão 5.7 ou superior recomendado)
- Cliente MySQL ou MySQL Workbench

### Uso

1. **Criar o Banco de Dados e a Tabela:**

    Execute o seguinte script para criar o banco de dados e a tabela `venda`:

   
    CREATE DATABASE venda;
    USE venda;

    CREATE TABLE venda (
        ID_venda INT,
        Curso VARCHAR(100),
        Aluno VARCHAR(100),
        Estado VARCHAR(100),
        Valor DECIMAL(10, 2)
    );
    ```

2. **Inserir Dados:**

    Popule a tabela com dados de exemplo:

   
    INSERT INTO venda (ID_venda, curso, aluno, estado, valor)
    VALUES 
    (1, 'excel', 'João', 'SP', 100),
    (2, 'vba', 'Lucas', 'RJ', 50),
    (3, 'excel', 'Alice', 'SP', 100),
    (4, 'Excel', 'Pedro', 'PE', 100),
    (5, 'VBA', 'Amanda', 'BA', 50),
    (6, 'Power BI', 'Rita', 'RS', 80),
    (7, 'Excel', 'Julia', 'RJ', 100),
    (8, 'Power BI', 'Caio', 'SP', 80),
    (9, 'Power BI', 'Lara', 'MG', 80),
    (10, 'Excel', 'Rogério', 'AC', 100);
    ```

3. **Executar Consultas:**

    Execute consultas para visualizar, atualizar ou excluir dados conforme necessário:

   
    -- Selecionar todos os dados
    SELECT * FROM venda;

    -- Selecionar colunas específicas
    SELECT Aluno, curso, valor FROM venda;

    -- Ordenar por Aluno
    SELECT * FROM venda ORDER BY Aluno;

    -- Filtrar por estado
    SELECT * FROM venda WHERE estado = 'RJ';

    -- Atualizar valor
    UPDATE venda SET valor = 150 WHERE curso = 'vba';

    -- Excluir um registro específico
    DELETE FROM venda WHERE ID_venda = 10;

    -- Limpar todos os dados
    TRUNCATE TABLE venda;
    ```

## Licença

Este projeto está licenciado sob a Licença MIT - veja o arquivo [LICENSE](LICENSE) para mais detalhes.
