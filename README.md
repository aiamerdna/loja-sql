Maaag Shop — Banco de Dados de uma Loja de Roupas

-- Sobre o projeto --

O Maaag Shop é um projeto de banco de dados relacional desenvolvido em SQL, com o objetivo de simular o gerenciamento de uma loja de roupas. O sistema foi elaborado para organizar e administrar informações relacionadas a clientes, pedidos, produtos, categorias, fornecedores e pagamentos.
O projeto foi desenvolvido como parte dos estudos de Análise e Desenvolvimento de Sistemas, com foco na prática de conceitos de banco de dados, modelagem relacional e programação SQL.

-- Estrutura do banco de dados --

O banco de dados db_maaag_shop é composto por 9 tabelas:
1. cliente: armazena os dados dos consumidores.
2. pedido: registra os pedidos realizados pelos clientes.
3. pagamento: armazena as informações dos pagamentos.
4. pedido_pagamento: estabelece o relacionamento entre pedidos e pagamentos.
5. fornecedor: registra os dados dos fornecedores.
6. categoria: organiza os produtos por categorias.
7. produto: armazena as informações das mercadorias, incluindo preço e quantidade em estoque.
8. fornecedor_produto: estabelece o relacionamento entre fornecedores e produtos.
9. item_pedido: relaciona os produtos aos pedidos, registrando preços e quantidades.

-- Funcionalidades e conceitos SQL aplicados --

Durante o desenvolvimento, foram utilizados diversos recursos da linguagem SQL:

1. Manipulação e consulta de dados

- Criação de banco de dados e tabelas (CREATE DATABASE e CREATE TABLE).
- Inserção de registros (INSERT INTO).
- Consultas utilizando SELECT, WHERE, ORDER BY e DISTINCT.
- Filtragem de resultados com IN, BETWEEN e operadores lógicos.

2. Funções de agregação e agrupamento

- Utilização de COUNT, SUM, AVG, MAX e MIN.
- Agrupamento de registros com GROUP BY.
- Filtragem de agrupamentos com HAVING.

3. Relacionamentos e JOINs

- Utilização de chaves primárias e estrangeiras.
- Relacionamentos entre diferentes tabelas.
- Consultas com INNER JOIN e LEFT JOIN.
- Relacionamentos muitos para muitos por meio de tabelas associativas.

4. Triggers
Foram desenvolvidas triggers para automatizar operações e garantir a integridade dos dados:

- validar_estoque: impede a inclusão de produtos em pedidos quando não existe estoque suficiente.
- baixa_estoque: atualiza automaticamente a quantidade de produtos em estoque após sua inclusão em um pedido.
- validar_produto: impede o cadastro de produtos com preços inválidos ou quantidades negativas.
- atualizar_pedido: atualiza o estado de um pedido para "Pago" quando o valor acumulado dos pagamentos atinge ou ultrapassa o valor total da compra.

5. Functions
Foram implementadas funções personalizadas para facilitar cálculos e consultas:

- fn_preco_desconto: calcula o preço de um produto após a aplicação de um percentual de desconto.
- fn_total_pedido: calcula o valor total de um pedido com base nos produtos e nas respectivas quantidades.

6. Procedures
Foram desenvolvidas procedures para executar operações específicas:

- pprodutos_por_cor_tamanho: consulta os produtos de acordo com a cor e o tamanho informados.
- ptotal_gasto_cliente: calcula o total gasto por um cliente, desconsiderando pedidos cancelados, e retorna o resultado por meio de um parâmetro de saída.

-- Tecnologias utilizadas -- 

MySQL: sistema de gerenciamento de banco de dados relacional.
SQL: linguagem utilizada para criação, manipulação, consulta e automação dos dados.

-- Objetivos de aprendizagem --

Este projeto teve como finalidade aprofundar conhecimentos em bancos de dados relacionais, especialmente nos seguintes conceitos:

1. Modelagem e estruturação de bancos de dados.
2. Normalização e relacionamentos entre tabelas.
3. Integridade referencial com chaves primárias e estrangeiras.
4. Consultas envolvendo múltiplas tabelas.
5. Funções de agregação e subconsultas.
6. Automação e validação de dados com triggers.
7. Desenvolvimento de funções e procedures armazenadas.

-- Autor -- 

Projeto desenvolvido como atividade acadêmica durante o curso de Análise e Desenvolvimento de Sistemas (ADS) na UDF.

