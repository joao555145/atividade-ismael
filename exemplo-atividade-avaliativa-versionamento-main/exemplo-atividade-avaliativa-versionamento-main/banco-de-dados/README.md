Banco de Dados

📝 Descrição do Projeto/Atividade

Criação de um banco de dados relacional para um sistema de biblioteca escolar, incluindo a modelagem das tabelas de alunos, livros e empréstimos. O projeto foi desenvolvido para armazenar e organizar informações de forma segura, permitindo consultas e relacionamentos entre os dados.

🧠 Reflexão de Aprendizado

1. O que aprendi?

Aprendi os conceitos de modelagem relacional, criação de tabelas e relacionamentos utilizando chaves primárias (PK) e chaves estrangeiras (FK). Também aprendi a utilizar comandos SQL como CREATE, INSERT, SELECT, UPDATE e DELETE, além de realizar consultas mais avançadas utilizando JOINs para relacionar informações de diferentes tabelas. Com isso, compreendi a importância da integridade e da organização dos dados em um sistema.

2. Para que serve (Por que aprendi)?

Aprender Banco de Dados é essencial porque praticamente todo sistema precisa armazenar informações de forma organizada e segura. Um banco de dados bem projetado permite consultas rápidas, evita a duplicação de informações e facilita a manutenção do sistema. Essa competência é muito valorizada no mercado, pois empresas dependem de dados para gerenciar clientes, produtos, vendas e diversos outros processos.

🛠️ Tecnologias e Ferramentas Utilizadas

- MySQL
- brModelo
- DBeaver
- Linguagem SQL

💻 Demonstração e Como Rodar

Código/Script SQL Relevante Comentado

-- Consulta os empréstimos juntamente com os dados do aluno e do livro

SELECT
    alunos.nome AS nome_aluno,
    livros.titulo AS titulo_livro,
    emprestimos.data_emprestimo

FROM emprestimos

INNER JOIN alunos
ON emprestimos.id_aluno = alunos.id

INNER JOIN livros
ON emprestimos.id_livro = livros.id

WHERE emprestimos.status = 'pendente'

ORDER BY emprestimos.data_emprestimo ASC;

Explicação:

- "INNER JOIN": relaciona as tabelas através das chaves.
- "WHERE": filtra apenas os empréstimos pendentes.
- "ORDER BY": organiza os resultados pela data do empréstimo.

Instruções para Executar

1. Execute o arquivo "schema.sql" no MySQL para criar as tabelas.

2. Execute o arquivo "seed.sql" para inserir os dados de teste.

3. Utilize as consultas SQL disponíveis para verificar os resultados e testar os relacionamentos entre as tabelas.

4. O projeto pode ser executado e visualizado utilizando o DBeaver ou outro cliente SQL compatível.
