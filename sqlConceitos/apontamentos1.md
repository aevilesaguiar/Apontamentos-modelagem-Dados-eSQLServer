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


**APAGANDO BANCO DE DADOS**
DROP DATABASE[SUCOS_VENDAS_04]

**Tipos de dados**
<img src="https://user-images.githubusercontent.com/52088444/151423678-f7123bdb-ac1e-491a-8e66-eb7866fb4e62.png" width="30%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151423773-75a01cfa-e501-4417-9a56-b773289185ba.png" width="60%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151424034-2571df0a-96cf-48d8-ac2c-7edf0fa479a4.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151424193-bfc14aa1-72c3-4bdb-a948-db02da667682.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151424434-f09f7caa-df7d-401d-88c2-bbf36a2ead14.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151424587-5ff9c4d9-fbee-4cb4-9086-a3871f4341e6.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151425595-865b4477-a215-44e6-9751-a5b00822d1b5.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151425727-b806305e-e7b4-4f29-a13f-c7b3a97028be.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151425852-0f92f2cd-9325-4964-b285-82fdc0fcec70.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151425951-b2349dfe-19d2-4335-86b8-f5474370aaa6.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151426099-d038d507-ddc6-4726-931e-7d06811951e3.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151426231-31e1a8ec-85e8-4a52-9027-b6da44928c75.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151426322-56f00d63-155e-4405-9a84-72a8ea37dd65.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151426929-505b2793-6f98-46f9-a80a-2655c39a790e.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151427265-325b4315-8e18-4389-a01d-1a41f9cab5f8.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151427353-7c6bfc75-b09a-4109-a334-e9683ac1eac5.png" width="45%"></img> 

**Fiz o curso da alura com o SQL Develpment  e com a interface SQL Server Managment Studio**




