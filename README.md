# Análise de dados com SQL para Power BI
Entrega do desafio Explore o Poder do NotebookLM para o curso Sem Parar Corpay - Back-end do Zero a Prática da DIO.

O assunto central deste notebook é o uso da linguagem SQL voltada para Analytics e Business Intelligence, integrando o conhecimento técnico de banco de dados com a visão estratégica necessária para a formação de um Power BI Analyst. O matérial explorado no notebook instrui como  transformar fatos brutos em conhecimento para a tomada de decisões, utilizando o SQL como ferramenta primordial para a manipulação e análise de dados. 


## Objetivo 

Adquirir domínio técnico na linguagem SQL orientada à análise de dados e compreender o ciclo de vida do dado através do processo de ETL. A meta é transformar dados brutos de fontes diversas em informações consolidadas, gerando inteligência de negócio e relatórios visuais preliminares no Power BI.

## Resumo do Notebook 

Este notebook apresenta uma visão abrangente sobre os Fundamentos de Análise de Dados utilizando SQL, com foco em sua aplicação para profissionais de Power BI e Business Intelligence. O conteúdo está estruturado desde os conceitos teóricos de BI até os comandos técnicos avançados de manipulação e consulta de bancos de dados.

I. Fundamentos de Business Intelligence (BI) e Análise de Dados
Conceito de BI: É uma área composta por estratégias e tecnologias para análise de dados e gerenciamento de informações, visando transformar dados em conhecimento para suporte à decisão.
Áreas de Atuação: O mercado de dados divide-se em papéis como Engenheiro de Dados (sustentação e extração), Cientista de Dados (modelagem e predição) e Analista de Dados (dashboards e diagnóstico de negócios).

Tipos de Análise:
Descritiva: O que aconteceu?
Diagnóstica: Por que aconteceu?
Preditiva: O que vai acontecer?
Prescritiva: O que fazer?

II. Introdução à Linguagem SQL
Origem: Desenvolvida pela IBM na década de 1970 para bancos de dados relacionais.

Categorias de Comandos:
DDL (Data Definition Language): Define a estrutura (tabelas, índices).
DML (Data Manipulation Language): Manipula os dados (inserir, atualizar, excluir).
DQL (Data Query Language): Recupera informações (comando SELECT).
DCL/TCL: Controle de acesso e de transações.

III. Definição de Estrutura (DDL)
CREATE TABLE: Cria novas tabelas, definindo nomes, tipos de dados e restrições. Permite implementar o autoincremento via IDENTITY ou SEQUENCE.
ALTER TABLE: Modifica a estrutura existente, permitindo adicionar, modificar ou excluir colunas e restrições.
DROP TABLE: Remove permanentemente a tabela e todos os seus dados. A cláusula CASCADE CONSTRAINT pode ser usada para remover restrições de chaves estrangeiras vinculadas.
TRUNCATE: Remove todos os registros de uma tabela, mas mantém sua estrutura intacta.

IV. Manipulação de Dados (DML)
INSERT: Adiciona novos registros. O comando INSERT ALL no Oracle permite inserções múltiplas em uma ou mais tabelas simultaneamente.
UPDATE: Modifica registros existentes com base em condições.
DELETE: Exclui linhas de uma tabela sem apagar sua estrutura.
Aviso Crítico: Se a cláusula WHERE for omitida nos comandos UPDATE ou DELETE, todos os registros da tabela serão afetados.

V. Controle de Transações
COMMIT: Confirma e torna permanentes todas as mudanças pendentes.
ROLLBACK: Desfaz as alterações pendentes desde o último commit.
SAVEPOINT: Cria pontos de salvamento intermediários para retornos parciais via ROLLBACK TO.

VI. Consulta de Dados (DQL - SELECT)
Básico e Ordenação: O comando SELECT extrai dados, podendo usar DISTINCT para valores únicos e AS para apelidar colunas (aliases). 
A cláusula ORDER BY define a ordem (ASC/DESC) e FETCH FIRST limita a quantidade de linhas.
Filtragem (WHERE): Utiliza operadores de comparação (=, <>, >, etc.) e lógicos (AND, OR, NOT). Operadores como BETWEEN, IN, LIKE e IS NULL permitem buscas refinadas.

Agrupamento:
GROUP BY: Agrupa registros para aplicar funções de agregação como SUM, AVG, COUNT, MIN e MAX.
HAVING: Filtra os resultados após o agrupamento, permitindo condições sobre funções agregadas (diferente do WHERE, que filtra antes).
Junções (JOINs): Combinam dados de múltiplas tabelas.
INNER JOIN: Apenas registros com correspondência em ambas as tabelas.
LEFT/RIGHT JOIN: Todos os registros de um lado e os correspondentes do outro (preenchendo nulos onde não há match).
FULL JOIN: Retorna todos os registros de ambas as tabelas.

Subqueries: Consultas aninhadas que fornecem valores para a query principal. 
Recomenda-se o uso do operador IN quando a subquery retorna múltiplos valores para evitar erro.

VII. Tipos de Dados e Integridade
Tipos Comuns: VARCHAR2 (texto variável), NUMBER (numérico), DATE (data/hora), CLOB/BLOB (grandes objetos de texto ou binários).
Restrições (Constraints): PRIMARY KEY (identificador único), FOREIGN KEY (relacionamento), NOT NULL (obrigatoriedade), UNIQUE (unicidade) e CHECK (validação de valores).


## Glossário

O seguinte glossário reúne os principais conceitos técnicos e teóricos abordados nos documentos em anexo sobre Business Intelligence e Linguagem SQL.

Fundamentos de Business Intelligence (BI) e Dados Business Intelligence (BI): Conjunto de estratégias e tecnologias utilizadas pelas empresas para análise de dados e gerenciamento de informações, visando transformar dados em conhecimento para suporte à decisão.

Dados: Fatos brutos que, isoladamente, não possuem valor ou significado contextual.
Informação: Representação de um cenário resultante do processamento de dados.

Conhecimento: Compreensão e aplicação da informação dentro de um contexto específico.

ETL (Extract, Transform, Load): Processo de extração de dados de fontes diversas, sua transformação (limpeza e estruturação) e carregamento em um destino (como um Data Warehouse) para análise.

Tipos de Análise:

Descritiva: Focada em entender o que aconteceu no passado.
Diagnóstica: Busca as causas e efeitos de determinados comportamentos (por que aconteceu?).
Preditiva: Utiliza modelos e probabilidades para tentar prever cenários futuros.
Prescritiva: Sugere ações para resolver problemas ou otimizar resultados.

Linguagem SQL e Categorias

SQL (Structured Query Language): Linguagem padrão desenvolvida pela IBM na década de 1970 para manipulação e consulta de dados em bancos de dados relacionais.
DDL (Data Definition Language): Comandos que definem e modificam a estrutura do banco de dados, como CREATE, ALTER e DROP.
DML (Data Manipulation Language): Comandos utilizados para manipular os dados dentro das tabelas, incluindo INSERT, UPDATE e DELETE.
DQL (Data Query Language): Comandos focados na recuperação de informações, sendo o principal o SELECT.
TCL (Transaction Control Language): Comandos para controle de transações, garantindo a integridade dos dados (ex: COMMIT, ROLLBACK).

Estrutura e Integridade de Dados

Tabela: Estrutura tabular composta por colunas (campos) e linhas (registros) onde os dados são armazenados.
Chave Primária (Primary Key): Coluna ou conjunto de colunas que identifica de forma única cada linha de uma tabela.
Chave Estrangeira (Foreign Key): Coluna que estabelece um relacionamento entre duas tabelas, garantindo que o valor corresponda a uma chave primária em outra tabela.
Constraint (Restrição): Mecanismos que garantem a integridade e qualidade dos dados, como NOT NULL (não aceita nulos), UNIQUE (valor único) e CHECK (valida condições).
Índice: Estrutura criada para melhorar a velocidade de busca e recuperação de dados em uma tabela.

Comandos e Operações SQL

SELECT: Comando fundamental para extrair informações específicas. Pode usar DISTINCT para valores únicos e AS para criar apelidos (aliases) de colunas.
JOIN: Operação que combina dados de duas ou mais tabelas baseada em uma coluna comum.
INNER JOIN: Retorna registros que possuem correspondência em ambas as tabelas.
LEFT/RIGHT JOIN: Retorna todos os registros de um lado e os correspondentes do outro, preenchendo com nulo onde não há match.
WHERE: Cláusula de filtragem aplicada antes de qualquer agrupamento de dados.
GROUP BY: Agrupa registros com valores idênticos para aplicar funções de agregação como SUM (soma), AVG (média), COUNT (contagem), MIN e MAX.
HAVING: Cláusula de filtragem aplicada após o agrupamento do GROUP BY.
Subquery (Subconsulta): Uma consulta aninhada dentro de outra instrução SQL para fornecer valores dinâmicos.
COMMIT: Confirma as alterações pendentes, tornando-as permanentes no banco.
ROLLBACK: Desfaz as alterações pendentes desde o último commit efetivado.

## Perguntas Estratégicas 

1. Fundamentos de BI e Análise

Pergunta: Explique a diferença entre os quatro tipos de análise em Business Intelligence (Descritiva, Diagnóstica, Preditiva e Prescritiva) e dê um exemplo de pergunta de negócio para cada uma.
Pergunta: Como os conceitos de Dados, Informação e Conhecimento se conectam no fluxo de tomada de decisão de uma empresa?

2. Estrutura e Definição de Dados (DDL)

Pergunta: Quais são as regras básicas de nomeação de tabelas e colunas no SQL e por que os comandos DDL (como CREATE e DROP) devem ser usados com cautela em produção?

Pergunta: Compare as duas formas de implementar o autoincremento no Oracle: utilizando SEQUENCE versus a cláusula IDENTITY. Quais as vantagens de cada uma?
Pergunta: Explique o funcionamento da cláusula CASCADE CONSTRAINT ao executar um DROP TABLE. O que acontece com as chaves estrangeiras de outras tabelas?

3. Manipulação de Dados e Riscos (DML)

Pergunta: Qual é o perigo de omitir a cláusula WHERE nos comandos UPDATE e DELETE? Como o SQL trata os registros nesses casos?
Pergunta: Explique a diferença fundamental entre os comandos DELETE, TRUNCATE e DROP. Qual 
deles mantém a estrutura da tabela intacta mas remove todos os dados?

4. Consultas, Filtragem e Agregação (DQL)

Pergunta: Explique a ordem de precedência dos operadores lógicos (AND, OR, NOT) e como o uso de parênteses pode alterar o resultado de um filtro no WHERE.
Pergunta: Diferencie o uso das cláusulas WHERE e HAVING. Em qual momento do processamento da query cada uma delas atua sobre os dados?
Pergunta: Como funcionam as funções de agregação (SUM, AVG, COUNT, MIN, MAX) em conjunto com a cláusula GROUP BY?

5. Relacionamentos e Subqueries

Pergunta: Compare os tipos de JOIN (INNER, LEFT, RIGHT e FULL). O que acontece com os registros que não possuem correspondência na tabela da direita em um LEFT JOIN?
Pergunta: Ao trabalhar com Subqueries, quando devo preferir o operador IN em vez do operador de igualdade (=)? O que causa o erro 'Subquery returns more than one row'?

6. Integridade e Controle de Transações (TCL)

Pergunta: Descreva o papel das Constraints (PRIMARY KEY, FOREIGN KEY, NOT NULL, CHECK, UNIQUE) na manutenção da qualidade e integridade de um banco de dados.
Pergunta: O que caracteriza uma transação pendente e como os comandos COMMIT e ROLLBACK garantem que o banco de dados não fique em um estado inconsistente?
Pergunta: Como os SAVEPOINTS podem ser utilizados para realizar retornos parciais em uma transação sem anular todo o trabalho feito?
