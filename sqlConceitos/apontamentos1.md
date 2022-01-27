## CONCEITOS HISTÓRICOS

<img src="https://user-images.githubusercontent.com/52088444/151182053-232f341d-6ad4-4632-8d3d-00bc3efc7cec.png" width="90%"></img> 

## SOBRE SQL

**SQL significa Structure Query Language, literalmente a linguagem padrão para realizar queries.**

- Vantagens de utilizar o padrão ANSI:
        - Aprendizado
        - Portabilidade
        - Longevidade
        - Comunicação
        - Liberdade de Escolha

- Desvatagens
        - Falta de Criatividade( feito apenas para dados estruturados, não podem ser utilizados em redes sociais que é o noSql)
        - Falta de estruturação(não possui ifs e elses, é uma linguagem simples, foi criado linguagens externas para estruturar e isso faz fugir do padrão ANSI)

**o padrão ANSI nunca deixa de usar as regras, ou seja nunca deixa de funcionar, o que o ANSI faz é incrementar novas regras**

## CONJUNTOS DE COMANDOS

- DDL - Data Definition Language(Linguagem de definição de Dados).É a parte da linguagem SQL que permite a manipulação das estruturas do banco de dados. Por exemplo, criar um banco de dados, criar uma tabela, criar um índice, apagar uma tabela, alterar o índice, alterar a política de crescimento de uma tabela ou de um índice. Quem acessa esses comandos é quem constrói 

- DML - Data Manipulation Language (Linguagem de Manipulação de Dados). O seu objetivo é dar manutenção aos dados do BD, INCLUIR DADOS, ALTERAR DADOS. Os comandos não mudam a estrutura dos dados. E atraves de les que fazemos consultas para fazer relatórios.

- DCL - Data Control Language(Linguagem de Controle de Dados). Administra o ambiente, acesso do usuario, o que cada usuario pode acessar, como armazenar tal tabela no disco, controle de logs,  qual vai ser a política de crescimento daquela tabela ao longo do tempo, na medida em que dados forem sendo incluídas nas tabelas.

## Definição de banco de Dados(SQL SERVER)

Um servdor/ Instancia do SQL Server pode possuir diversos Bancos de dados, BD é a unidade de agregação mais importante do SQL Server
Eu posso separar o BD por tema assunto, um BD pode se comunicar entre si, desde que estejam no mesmos ervidor

- ESQUEMA(SCHEMA)
- Esquema padrão =DBO (aquele esquema default, todo mundo esta relacionado ao dbo
<img src="https://user-images.githubusercontent.com/52088444/151411850-d2b170e0-c5e3-48ab-b6db-e5db8e9a31f8.png" width="45%"></img> 

**Dentro do Esquema eu posso ter

- TABELAS(TABLE)
- VISÕES(VIEWS)
- RESTRIÇÕES(CONTRAINTS)
- PROGRAMAÇÕES

A tabela é o componente mais importante do BD;
   - Numeros de linhas= capacidade do banco
   - Numero de colunas = Fixo , todos os valores que estão numa coluna tem o mesmo tipo. Ex.: texto, numero, data...., As colunas tem o mesmo tipo e nome, e são dadas para gravar o tipo de informação que estou guardando
   - Linhas são chamadas de registros 
   - Colunas são chamadas de campo
   - Constraints são regras de validação de dados , uma restrição por exemplo e se o campo pode receber vazio, ou não vazio(not null) 
   - Chave primaria(Primary key) não pode ter linhas com valores nas PKS repetidos , ou seja isso é uma constraint também.
   - Foreign key(chave estrangeira) - não podemos incluir valores no campo que não exista em outro campo de outra tabela, relacionamento entre tabelas, é através dela que existe o relacionamento, isso também é uma constraint
   - Visões(views) estrutura logica baseada em um comando de consulta sql. Ex: visao=Passa a valer como uma tabela, ou seja se  eu quiser sempre ver um dado ano quantde de compra, eu gero uma tabela lógica e não física, que é o caso da view.
   - Programações, cada BD é implementado de uma forma(psql),  exemplo: 
        IF(select)>0 then<br>
        SET DATA=SELECT Y FROM TABELA;<br>
        INSERT X INTO Y;<br>
        END IF<br>
   
**As tabelas podem se agrupadas em esquemas (Schema).**


## Conhecendo o SQL Server Management Studio
Dentro de cada tabela nós temos os dados da tabela
<img src="https://user-images.githubusercontent.com/52088444/151412306-4f31aa7d-4a16-4f14-b24b-7d161df05364.png" width="45%"></img> 

- Colunas ou "campo"
- chaves (primarys keys)
- Restrições (constraints)
- Gatilhos (regras que eu vão disparar quando alguma coisa acontecer. Exemplo quando eu fizer uma ação dispara tal coisa)
- índices(são estruturas que eu ligo ao campo para fazer consultas mais rapidas)
- estatísticas



**Em 2019 melhorias pontuais nos módulos SQL**
## Versões SQL
<img src="https://user-images.githubusercontent.com/52088444/151203730-fde8c51e-7886-43c6-bc76-7b60f9805a9e.png" width="90%"></img> 


<img src="https://user-images.githubusercontent.com/52088444/151415105-04eea1a2-02c6-4447-88ba-8662d9780be4.png" width="45%"></img> 

- O ARQUIVO QUE TEM O BD , a base de dados - é o mdf
- ldf arquivo de transações
- Quando eu crio um arquivo no sql server são criados automaticamente os dois arquivos com o mesmo nome e as duas extensões mdf e ldf


**Exemplo de criação de BD**

<img src="https://user-images.githubusercontent.com/52088444/151417031-2d1ebb8c-b4e2-42f0-b699-0465195effe5.png" width="45%"></img> 

Esse arquivo foi criado fora do local padrão do sql server, e nele foi informado o nome do arquivos, local onde será armazenado, tamanho
inicial do arquivo, tamanho máximo e de quanto ele vai crescer, e a mesma coisa foi feito com o  arquivo de log(ldf)
        
<img src="https://user-images.githubusercontent.com/52088444/151417530-234c07bf-9fdc-45cb-aaae-7436134f0e4e.png" width="90%"></img> 

**Se fossemos criar da maneira padrão o BD**
CREATE DATABASE SUCOS_VENDAS_01;

**Fiz o curso da alura com o SQL Develpment  e com a interface SQL Server Managment Studio**




