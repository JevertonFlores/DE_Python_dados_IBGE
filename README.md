# ETL_Python_dados_IBGE
Este repositório exemplifica um simples processo de ETL em ambiente local, utilizando conceitos de modelagem dimensional.

<h3>Objetivo:</h3>
Este projeto tem como objetivo a criação de um Data Warehouse em ambiente local, onde estarão disponíveis dados públicos sobre os Batalhões de Polícia Militar do estado do Rio de Janeiro e registros de boletins de ocorrências.

<h3>Ferramentas e liguagens utilizadas:</h3>

- SQLite para criação dos bancos de dados;
- Jupyter para criação dos scripts;
- Python para coleta, manipulação e carga de dados;
- SQL para criação das tabelas no banco de dados.

<h3>Origens dos dados:</h3>

Parte dos dados está disponível no <a href="https://www.ibge.gov.br/explica/codigos-dos-municipios.php#RJ">site do IBGE</a> e a outra parte está armazenada no diretório 
<a href="https://github.com/JevertonFlores/ETL_Python_dados_IBGE/tree/main/datasets">datasets</a> dentro deste repositório.

<h3>Processo e estrutura:</h3>

Via linguagem Python, serão coletados dados contidos em arquivos .csv e também diretamente no site do IBGE, posteriormente estes dados serão armazenados em uma área de Stage, passarão por alguns tratamento e, por fim, serão disponibilizados em tabelas modeladas em um DW no banco SQLite.
- Para a criação das tabelas Dimensão foram utilizados os conceitos de SCD Tipo 1.
- Para a tabela fato, além do script de criação da tabela e carga dos dados, também foi programado a carga incremental dos dados e atualização retroativa dos registros.

**Acesse os scripts:**

<a href="https://github.com/JevertonFlores/ETL_Python_dados_IBGE/tree/main/00.%20Cria%C3%A7%C3%A3o%20da%20estrutura%20de%20banco%20de%20dados">- Criação da estrutura de banco de dados;</a>

<a href="https://github.com/JevertonFlores/ETL_Python_dados_IBGE/tree/main/01.%20Coleta%20de%20Dados">- Coleta de Dados;</a>

<a href="https://github.com/JevertonFlores/ETL_Python_dados_IBGE/tree/main/02.%20Dimens%C3%B5es">- Desenvolvimento das tabelas de Dimensão;</a>

<a href="https://github.com/JevertonFlores/ETL_Python_dados_IBGE/tree/main/03.%20Fato">- Desenvolvimento da tabela Fato;</a>





<h3>Modelo lógico do Data Warehouse:</h3>
<img width="298" alt="image" src="https://user-images.githubusercontent.com/36814309/221437834-0d237be5-cb63-4f96-ae5c-d35258dd8313.png">
