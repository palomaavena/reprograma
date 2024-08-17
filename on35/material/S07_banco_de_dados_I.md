<h1 align="center">
  <img src="assets/reprograma-fundos-claros.png" alt="logo reprograma" width="500">
</h1>

# Lidando com Bancos de Dados

## Turma ON35 | Python | Semana 7 | 2024 | Professora Camila Ribeiro

### Instruções

**Vamos começar a construir nosso conhecimento em bancos de dados!**

1. **Faça o Fork deste repositório!** 
    - Clique no botão "Fork" no canto superior direito da página do repositório.
    - Você terá uma cópia do repositório em sua conta do GitHub.
2. **Clone o repositório na sua máquina:**
    - Abra o seu terminal e digite:
    ```bash
    git clone https://github.com/seu-usuario/lidando-com-bancos-de-dados.git
    ```
    - Substitua "seu-usuario" pelo seu nome de usuário do GitHub.
3. **Entre na pasta do repositório:**
    - Abra o seu terminal e digite:
    ```bash
    cd lidando-com-bancos-de-dados
    ```

## Introdução

Nesta aula, vamos mergulhar no mundo dos bancos de dados relacionais, utilizando o SQLite como ferramenta para criar, manipular e consultar dados. Esta é a primeira de duas aulas que te levarão a dominar os bancos de dados!

## Objetivos da Aula

* Entender o que são bancos de dados e sua importância na análise de dados.
* Aprender os conceitos básicos de bancos de dados relacionais.
* Utilizar o SQLite e a ferramenta online SQLiteOnline.
* Executar comandos SQL básicos para criar, inserir, atualizar e consultar dados.
* Compreender relacionamentos entre tabelas e executar joins.

## Instalação e Configuração

### Ferramentas Necessárias

* **SQLiteOnline:** Ferramenta online para praticar SQL. Acesse: [https://sqliteonline.com/](https://sqliteonline.com/)

### Como Acessar o SQLiteOnline

1. Acesse o site do SQLiteOnline.
2. Clique em "Start" para iniciar a ferramenta.
3. Você verá uma interface com um editor SQL à esquerda e os resultados das consultas à direita.

## Conceitos Básicos de Banco de Dados

### O que é um Banco de Dados?

Um banco de dados é um sistema organizado para armazenar e gerenciar informações de forma eficiente.  Pense nele como um grande armário, dividido em gavetas (tabelas) que guardam informações sobre um tema específico.  Cada gaveta é organizada em colunas (campos) e linhas (registros).

**Exemplo:**

Imagine um banco de dados para uma biblioteca. 

* **Tabela:** Livros
* **Colunas:** Título, Autor, Ano, Gênero, Editora
* **Linhas:** Cada linha representa um livro específico, com informações sobre seu título, autor, ano de publicação, gênero e editora.

### Terminologia Básica

* **Tabela**: Estrutura que organiza os dados em linhas e colunas.
* **Linha (Registro)**: Um único conjunto de dados em uma tabela.
* **Coluna (Campo)**: Um único tipo de dado armazenado em uma tabela.
* **Chave Primária**: Identificador único para cada registro em uma tabela.
* **Chave Estrangeira**: Coluna que cria um vínculo entre duas tabelas.

## Introdução ao SQLite

### O que é o SQLite?

SQLite é um sistema de gerenciamento de banco de dados relacional, leve e incorporável. Ele é amplamente utilizado em aplicações web, dispositivos móveis e projetos de pequena escala.

### Vantagens do SQLite

* **Simplicidade e facilidade de uso:**  É fácil de configurar e usar, ideal para iniciantes.
* **Sem servidor:** Funciona diretamente no seu aplicativo, sem necessidade de um servidor dedicado.
* **Portabilidade e desempenho:** Pode ser usado em diversos sistemas operacionais e oferece bom desempenho.

## Tipos de Dados

No SQLite, assim como em outros bancos de dados, os **tipos de dados** determinam o formato e as características de cada informação que você armazena.

**Tipos de Dados Comuns no SQLite:**

* **TEXT:** Armazena strings de texto (ex: nomes, endereços, descrições).
* **INTEGER:** Armazena números inteiros (ex: id, ano).
* **REAL:** Armazena números de ponto flutuante (ex: preços, medidas).
* **BLOB:** Armazena dados binários (ex: imagens, arquivos).
* **NUMERIC:** Armazena números decimais com alta precisão.
* **BOOLEAN:** Armazena valores lógicos (TRUE ou FALSE).

## Comandos SQL por Categoria

### DDL (Data Definition Language)

**Função:** Define a estrutura do banco de dados, criando, alterando e excluindo objetos como tabelas, colunas, índices e outros elementos.

**Comandos:**

* **CREATE:**  Cria novos objetos.
    * **CREATE TABLE:** Criar uma nova tabela:
    ```sql
    CREATE TABLE tabela (
        coluna1 TIPO_DE_DADO,
        coluna2 TIPO_DE_DADO,
        ...
    );
    ```
    * **EXEMPLO:** Criar uma nova tabela chamada "Livros":
    ```sql
    CREATE TABLE Livros (
       Título TEXT,
       Autor TEXT,
       Ano INTEGER,
       Gênero TEXT
    );
    ```
* **DROP:**  Exclui objetos existentes.
    * **DROP TABLE:** Excluir uma tabela:
    ```sql
    DROP TABLE tabela;
    ```
    * **EXEMPLO:** Excluir a tabela "Livros":
    ```sql
    DROP TABLE Livros;
    ```
* **ALTER:** Altera a estrutura de objetos existentes.
    * **ALTER TABLE:** Adicionar uma nova coluna à tabela:
    ```sql
    ALTER TABLE tabela
    ADD COLUMN nova_coluna TIPO_DE_DADO;
    ```
    * **EXEMPLO:** Adicionar uma nova coluna chamada "Editora" à tabela "Livros":
    ```sql
    ALTER TABLE Livros
    ADD COLUMN Editora TEXT;
    ```
* **TRUNCATE:**  Exclui todos os dados de uma tabela, mas mantém a estrutura.
    * **TRUNCATE TABLE:** Excluir todos os dados de uma tabela:
    ```sql
    TRUNCATE TABLE tabela;
    ```
    * **EXEMPLO:** Excluir todos os dados da tabela "Livros", mas manter a estrutura da tabela:
    ```sql
    TRUNCATE TABLE Livros;
    ```
* **RENAME:** Renomeia objetos (tabelas, colunas, etc.).
    * **RENAME TABLE:** Renomear uma tabela:
    ```sql
    RENAME TABLE tabela TO nova_tabela;
    ```
    * **EXEMPLO:** Renomear a tabela "Livros" para "Obras":
    ```sql
    RENAME TABLE Livros TO Obras;
    ```

### DQL (Data Query Language)

**Função:** Permite consultar e recuperar dados do banco de dados.

**Comandos:**

* **SELECT:** Seleciona dados de uma ou mais tabelas.
    * **SELECT:** Selecionar todos os dados de uma tabela:
    ```sql
    SELECT * FROM tabela;
    ```
    * **EXEMPLO:** Selecionar todos os livros da tabela "Livros":
    ```sql
    SELECT * FROM Livros;
    ```
    * Selecionar colunas específicas de uma tabela:
    ```sql
    SELECT coluna1, coluna2 FROM tabela;
    ```
    * **EXEMPLO:** Selecionar os títulos e autores dos livros publicados após 2000:
    ```sql
    SELECT Título, Autor FROM Livros WHERE Ano > 2000;
    ```

### DML (Data Manipulation Language)

**Função:** Manipula os dados dentro das tabelas, inserindo, atualizando e excluindo registros. 

**Comandos:**

* **INSERT:** Insere novas linhas em uma tabela.
    * **INSERT INTO:** Inserir um novo registro em uma tabela:
    ```sql
    INSERT INTO tabela (coluna1, coluna2, ...)
    VALUES (valor1, valor2, ...);
    ```
    * **EXEMPLO:** Inserir um novo livro na tabela "Livros":
    ```sql
    INSERT INTO Livros (Título, Autor, Ano, Gênero) 
    VALUES ('O Senhor dos Anéis', 'J. R. R. Tolkien', 1954, 'Fantasia');
    ```
* **UPDATE:**  Altera dados em linhas existentes.
    * **UPDATE:** Atualizar dados em uma tabela:
    ```sql
    UPDATE tabela
    SET coluna1 = valor1, coluna2 = valor2, ...
    WHERE condição;
    ```
    * **EXEMPLO:** Atualizar o gênero do livro "O Senhor dos Anéis" para "Fantasia épica":
    ```sql
    UPDATE Livros 
    SET Gênero = 'Fantasia épica' 
    WHERE Título = 'O Senhor dos Anéis';
    ```
* **DELETE:**  Exclui linhas de uma tabela.
    * **DELETE FROM:** Excluir registros de uma tabela:
    ```sql
    DELETE FROM tabela
    WHERE condição;
    ```
    * **EXEMPLO:** Excluir o livro "O Senhor dos Anéis" da tabela "Livros":
    ```sql
    DELETE FROM Livros WHERE Título = 'O Senhor dos Anéis';
    ```
* **LOCK:**  Bloqueia linhas para evitar alterações simultâneas.
    ```sql
    BEGIN TRANSACTION;
    SELECT * FROM tabela WHERE condição FOR UPDATE;
    -- Faça a atualização da linha
    UPDATE tabela SET coluna = valor WHERE condição;
    COMMIT;
    ```
    * **EXEMPLO:** Bloqueia a linha com o título "O Senhor dos Anéis" para edição exclusiva:
    ```sql
    BEGIN TRANSACTION;
    SELECT * FROM Livros WHERE Título = 'O Senhor dos Anéis' FOR UPDATE;
    -- Faça a atualização da linha
    UPDATE Livros SET Gênero = 'Fantasia épica' WHERE Título = 'O Senhor dos Anéis';
    COMMIT;
    ```
* **CALL:** Chama uma função ou procedimento armazenado.
    ```sql
    CALL nome_do_procedimento(argumento1, argumento2, ...);
    ```
    * **EXEMPLO:** Supondo que exista um procedimento armazenado chamado "get_livros_por_genero":
    ```sql
    CALL get_livros_por_genero('Fantasia');
    ```
* **EXPLAIN PLAN:** Mostra o plano de execução de uma consulta, ajudando a otimizar a performance.
    ```sql
    EXPLAIN QUERY PLAN SELECT * FROM tabela WHERE condição;
    ```
    * **EXEMPLO:** Mostra o plano de execução da consulta "SELECT * FROM Livros WHERE Ano > 2000":
    ```sql
    EXPLAIN QUERY PLAN SELECT * FROM Livros WHERE Ano > 2000;
    ```

### DCL (Data Control Language)

**Função:** Controla o acesso aos dados do banco de dados, definindo permissões e privilégios para usuários e grupos.

**Comandos:**

* **GRANT:** Concede permissões a usuários.
    ```sql
    GRANT permissão ON tabela TO usuário;
    ```
    * **EXEMPLO:** Conceder permissão de leitura e escrita na tabela "Livros" ao usuário "Alice":
    ```sql
    GRANT SELECT, INSERT, UPDATE, DELETE ON Livros TO Alice;
    ```
* **REVOKE:**  Revoca permissões de usuários.
    ```sql
    REVOKE permissão ON tabela FROM usuário;
    ```
    * **EXEMPLO:** Retirar a permissão de escrita na tabela "Livros" do usuário "Alice":
    ```sql
    REVOKE INSERT, UPDATE, DELETE ON Livros FROM Alice;
    ```

### TCL (Transaction Control Language)

**Função:** Controla as transações no banco de dados, garantindo que todas as operações de uma transação sejam concluídas com sucesso ou que nenhuma seja aplicada caso ocorra um erro.

**Comandos:**

* **COMMIT:** Confirma as alterações de uma transação.
    ```sql
    COMMIT;
    ```
* **ROLLBACK:**  Reverte as alterações de uma transação.
    ```sql
    ROLLBACK;
    ```
* **SAVEPOINT:**  Cria um ponto de salvamento dentro de uma transação, permitindo reverter as alterações até esse ponto.
    ```sql
    SAVEPOINT nome_do_ponto_de_salvamento;
    ```
    * **EXEMPLO:** Cria um ponto de salvamento:
    ```sql
    SAVEPOINT my_savepoint;
    ```

<br>


## Links Úteis

* **Documentação do SQLite:** [https://www.sqlite.org/docs.html](https://www.sqlite.org/docs.html)
* **Tutorial de SQL W3Schools:** [https://www.w3schools.com/sql/](https://www.w3schools.com/sql/)
* **SQLite Tutorial:** [https://www.sqlitetutorial.net/](https://www.sqlitetutorial.net/)
* **Game SQL:** [https://sql-island.informatik.uni-kl.de/](https://sql-island.informatik.uni-kl.de/)
* **SQL Murder Mystery:** [https://mystery.knightlab.com/](https://mystery.knightlab.com/)
* **SQLZoo:** [https://sqlzoo.net/wiki/SQL_Tutorial](https://sqlzoo.net/wiki/SQL_Tutorial)

<br>

---

# Glossário SQL - Tradução e Funcionalidade

<br>

| Palavra SQL | Tradução | Função | Exemplo | Tradução do Exemplo |
| --- | --- | --- | --- | --- |
| SELECT | Selecionar | Seleciona dados de uma tabela. | SELECT * FROM livros; | Selecione todos os dados da tabela "livros". |
| FROM | De | Especifica a tabela de onde os dados serão selecionados. | SELECT * FROM livros; | Selecione os dados da tabela "livros". |
| WHERE | Onde | Filtra os registros com base em uma condição. | SELECT * FROM livros WHERE genero = 'Ficção'; | Selecione os livros onde o gênero seja "Ficção". |
| AND | E | Combina múltiplas condições com "E" lógico. | SELECT * FROM livros WHERE genero = 'Ficção' AND ano_publicacao > 2000; | Selecione os livros onde o gênero seja "Ficção" e o ano de publicação seja maior que 2000. |
| OR | Ou | Combina múltiplas condições com "OU" lógico. | SELECT * FROM livros WHERE genero = 'Ficção' OR genero = 'Romance'; | Selecione os livros onde o gênero seja "Ficção" ou "Romance". |
| LIKE | Semelhante a | Faz comparações de padrões usando caracteres curinga (%, _). | SELECT * FROM livros WHERE titulo LIKE '%Harry Potter%'; | Selecione os livros cujo título contenha a palavra "Harry Potter". |
| NOT | Não | Nega uma condição. | SELECT * FROM livros WHERE ano_publicacao NOT BETWEEN 2000 AND 2010; | Selecione os livros que não foram publicados entre 2000 e 2010. |
| IN | Dentro de | Verifica se um valor está dentro de uma lista. | SELECT * FROM livros WHERE genero IN ('Ficção', 'Fantasia'); | Selecione os livros cujo gênero seja "Ficção" ou "Fantasia". |
| BETWEEN | Entre | Filtra valores dentro de um intervalo. | SELECT * FROM livros WHERE ano_publicacao BETWEEN 1990 AND 2000; | Selecione os livros publicados entre 1990 e 2000. |
| ORDER BY | Ordenar por | Ordena os resultados em ordem crescente ou decrescente. | SELECT * FROM livros ORDER BY ano_publicacao DESC; | Selecione os livros ordenados pelo ano de publicação em ordem decrescente. |
| ASC | Ascendente | Ordena em ordem crescente (padrão). | SELECT * FROM livros ORDER BY titulo ASC; | Selecione os livros ordenados pelo título em ordem crescente. |
| DESC | Decrescente | Ordena em ordem decrescente. | SELECT * FROM livros ORDER BY ano_publicacao DESC; | Selecione os livros ordenados pelo ano de publicação em ordem decrescente. |
| LIMIT | Limitar | Limita o número de registros retornados. | SELECT * FROM livros LIMIT 5; | Selecione os 5 primeiros livros da tabela. |
| GROUP BY | Agrupar por | Agrupa linhas com valores iguais em uma coluna. | SELECT genero, COUNT(*) AS num_livros FROM livros GROUP BY genero; | Agrupe os livros por gênero e conte o número de livros em cada gênero. |
| COUNT(*) | Contar | Conta o número de registros em um grupo. | SELECT COUNT(*) FROM livros; | Conte o número total de livros na tabela. |
| SUM() | Somar | Soma os valores de uma coluna. | SELECT SUM(preco) FROM livros; | Some o preço de todos os livros da tabela. |
| AVG() | Média | Calcula a média dos valores de uma coluna. | SELECT AVG(preco) FROM livros; | Calcule a média do preço dos livros na tabela. |
| MIN() | Mínimo | Encontra o valor mínimo de uma coluna. | SELECT MIN(ano_publicacao) FROM livros; | Encontre o ano de publicação mais antigo dos livros. |
| MAX() | Máximo | Encontra o valor máximo de uma coluna. | SELECT MAX(ano_publicacao) FROM livros; | Encontre o ano de publicação mais recente dos livros. |
| DISTINCT | Distintos | Retorna apenas valores únicos de uma coluna. | SELECT DISTINCT genero FROM livros; | Selecione apenas os gêneros distintos (sem repetições) da tabela. |
| AS | Como | Renomeia uma coluna no resultado da consulta. | SELECT id AS livro_id, titulo AS nome_livro FROM livros; | Renomeie as colunas "id" para "livro_id" e "titulo" para "nome_livro". |
| CREATE TABLE | Criar Tabela | Cria uma nova tabela no banco de dados. | CREATE TABLE livros (id INTEGER PRIMARY KEY, titulo TEXT, ...); | Crie uma nova tabela chamada "livros" com as colunas especificadas. |
| INTEGER | Inteiro | Define uma coluna do tipo inteiro. | id INTEGER PRIMARY KEY, | Defina a coluna "id" como um número inteiro. |
| TEXT | Texto | Define uma coluna do tipo texto. | titulo TEXT, | Defina a coluna "titulo" como texto. |
| REAL | Real | Define uma coluna do tipo número de ponto flutuante. | preco REAL | Defina a coluna "preco" como um número real. |
| PRIMARY KEY | Chave Primária | Define uma coluna como chave primária, garantindo unicidade de registros. | id INTEGER PRIMARY KEY, | Defina a coluna "id" como a chave primária, garantindo que cada livro tenha um ID único. |
| FOREIGN KEY | Chave Estrangeira | Cria um relacionamento com outra tabela. | FOREIGN KEY (livro_id) REFERENCES livros(id) | Defina "livro_id" como chave estrangeira, referenciando a tabela "livros". |
| REFERENCES | Referencia | Especifica a tabela e a coluna referenciada pela chave estrangeira. | FOREIGN KEY (livro_id) REFERENCES livros(id) | Faça com que a chave estrangeira "livro_id" se refira à coluna "id" da tabela "livros". |
| INSERT INTO | Inserir em | Insere novos dados em uma tabela. | INSERT INTO livros (titulo, genero, ...) VALUES ('Dom Quixote', 'Ficção', ...); | Insira um novo livro com os dados "Dom Quixote", "Ficção", etc. na tabela "livros". |
| VALUES | Valores | Especifica os valores para cada coluna dos novos registros. | INSERT INTO livros (titulo, genero, ...) VALUES ('Dom Quixote', 'Ficção', ...); | Especifique os valores para "titulo", "genero", etc. |
| UPDATE | Atualizar | Altera dados em registros existentes. | UPDATE livros SET preco = 30.00 WHERE id = 1; | Atualize o preço do livro com ID 1 para 30.00. |
| SET | Definir | Define novos valores para as colunas a serem atualizadas. | UPDATE livros SET preco = 30.00 WHERE id = 1; | Defina o novo preço do livro como 30.00. |
| DELETE | Excluir | Remove registros de uma tabela. | DELETE FROM livros WHERE id = 1; | Exclua o livro com ID 1 da tabela. |
| TRUNCATE TABLE | Truncar Tabela | Remove todos os dados de uma tabela, mantendo a estrutura. | TRUNCATE TABLE livros; | Exclua todos os dados da tabela "livros", mas mantenha a estrutura da tabela. |
| ALTER TABLE | Alterar Tabela | Modifica a estrutura de uma tabela. | ALTER TABLE livros ADD COLUMN idioma TEXT; | Adicione uma nova coluna chamada "idioma" do tipo texto à tabela "livros". |
| RENAME TABLE | Renomear Tabela | Renomeia uma tabela. | RENAME TABLE livros TO obras_literarias; | Renomeie a tabela "livros" para "obras_literarias". |
| BEGIN TRANSACTION | Iniciar Transação | Inicia um bloco de comandos como uma única transação. | BEGIN TRANSACTION; | Inicie uma transação. |
| COMMIT | Confirmar | Confirma as alterações de uma transação. | COMMIT; | Confirme as alterações da transação atual. |
| ROLLBACK | Reverter | Reverte as alterações de uma transação. | ROLLBACK; | Reverte as alterações da transação atual. |
| SAVEPOINT | Ponto de Salvamento | Cria um ponto de salvamento dentro de uma transação. | SAVEPOINT meu_ponto; | Crie um ponto de salvamento chamado "meu_ponto" dentro da transação atual. |
| GRANT | Conceder | Concede permissões de acesso a usuários. | GRANT SELECT, INSERT ON livros TO usuario_admin; | Conceda ao usuário "usuario_admin" permissões de seleção e inserção na tabela "livros". |
| REVOKE | Revogar | Revoca permissões de acesso de usuários. | REVOKE INSERT ON livros FROM usuario_admin; | Revogue a permissão de inserção na tabela "livros" do usuário "usuario_admin". |
| JOIN | Juntar | Combina dados de duas ou mais tabelas. | SELECT * FROM livros JOIN autores ON livros.autor_id = autores.id; | Junte a tabela "livros" com a tabela "autores" usando a coluna "autor_id" como chave. |
| ON | Em | Especifica a condição de relacionamento para juntar tabelas. | SELECT * FROM livros JOIN autores ON livros.autor_id = autores.id; | Junte as tabelas usando a condição "livros.autor_id = http://autores.id/". |
| EXISTS | Existe | Verifica se uma subconsulta retorna algum resultado. | SELECT * FROM livros WHERE EXISTS (SELECT 1 FROM autores WHERE id = livros.autor_id); | Selecione os livros que existem na tabela "autores". |
| UNION | União | Combina resultados de duas consultas, removendo duplicatas. | SELECT titulo FROM livros WHERE genero = 'Ficção' UNION SELECT titulo FROM livros WHERE genero = 'Romance'; | Combine os títulos de livros de ficção com os títulos de livros de romance, removendo duplicatas. |
| UNION ALL | União Tudo | Combina resultados de duas consultas, incluindo duplicatas. | SELECT titulo FROM livros WHERE genero = 'Ficção' UNION ALL SELECT titulo FROM livros WHERE genero = 'Romance'; | Combine os títulos de livros de ficção com os títulos de livros de romance, incluindo duplicatas. |
| INTERSECT | Interseção | Retorna apenas as linhas que aparecem em ambos os conjuntos de resultados. | SELECT titulo FROM livros WHERE ano_publicacao > 2000 INTERSECT SELECT titulo FROM livros WHERE genero = 'Ficção'; | Selecione os títulos de livros publicados após 2000 que também sejam do gênero "Ficção". |
| EXCEPT | Exceto | Retorna apenas as linhas que aparecem no primeiro conjunto de resultados, mas não no segundo. | SELECT titulo FROM livros WHERE genero = 'Ficção' EXCEPT SELECT titulo FROM livros WHERE ano_publicacao > 2000; | Selecione os títulos de livros de ficção que não foram publicados após 2000. |

> **Lembre-se: essa tabela é apenas uma introdução ao SQL. Existem muitos outros comandos, funções e conceitos que você pode explorar para dominar essa linguagem poderosa!** 😉

<br>

🔸 Para testar as consultas, você pode usar o código SQL abaixo para criar a tabela `livros` e inserir alguns dados de exemplo:

```sql
-- Cria a tabela 'livros'
CREATE TABLE livros (
    id INTEGER PRIMARY KEY,
    titulo TEXT,
    genero TEXT,
    autor TEXT,
    ano_publicacao INTEGER,
    preco REAL
);

-- Insere alguns livros de exemplo
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('Dom Quixote', 'Ficção', 'Miguel de Cervantes', 1605, 29.90);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('Orgulho e Preconceito', 'Romance', 'Jane Austen', 1813, 25.50);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('1984', 'Ficção', 'George Orwell', 1949, 35.75);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('O Senhor dos Anéis: A Sociedade do Anel', 'Fantasia', 'J. R. R. Tolkien', 1954, 39.90);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('Harry Potter e a Pedra Filosofal', 'Fantasia', 'J. K. Rowling', 1997, 20.90);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('O Hobbit', 'Fantasia', 'J. R. R. Tolkien', 1937, 28.50);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('A Menina que Roubava Livros', 'Ficção Histórica', 'Markus Zusak', 2005, 32.90);
INSERT INTO livros (titulo, genero, autor, ano_publicacao, preco) VALUES ('O Código Da Vinci', 'Mistério', 'Dan Brown', 2003, 34.90);

-- Confirma a criação da tabela e os dados
SELECT * FROM livros;

```

> Agora você tem uma tabela `livros` com alguns dados de exemplo para testar as consultas SQL! 💜




<br>

<p align="center">
Desenvolvido com :purple_heart:  
</p>
