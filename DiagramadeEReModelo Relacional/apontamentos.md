# Modelagem de banco de dados relacional: Entidades, relacionamentos e atributos

**O que é um banco de dados?**
é uma coleção de dados relacionados.

- Representa o aspecto de algo do mundo real.
- Coleção logicamente coerente de dados
- projetado para uma finalidade específica


**O banco de dados NoSQL é aquele onde é armazenado uma grande quantidade de 
informações, além de estruturas complexas, que atendem as necessidades das redes sociais.**

** O que é um SGBD?**

Sistema de gernciamento de Banco de de dados. Sistema computacional que permite que usuários
mantenham um banco de dados. Permite definir, construir, manipular, compartilhar o banco de dados.
Permite compartilhamento, armazenar os dados em algum meio, especificar tipos, estruturas e reastrições 
dos dados armazenados(Metadados). Manipulação, funções de consulta, recuperar dados, atualizar dados, refletir 
as mudanças do mundo real.

**SGBD**
Abstração de Dados -> suprimir ao usuario detalher da organização e armazenamento de dados. 
O modelo de dados permite esta abstração.

**Modelos de alto nivel**
modelo de entidade e relacionamento(entidade, atributos e relacionamentos)
**Modelos de relacionamento(relacional)**
Linguagem em NoSQL
**Modelo de baixo Nível(físico)**
Acesso a estrutura de armazenamento e índices.

**Esquema de Banco de dados:**
refere-se a descrição do banco de dados. Normalmente não muda. O que muda é o conteudo do BD.


## Etapas

<img src="https://user-images.githubusercontent.com/52088444/151546838-8507132b-5531-4a98-bbb7-e76d0a5086b3.png" width="90%"></img> 


## Modelo Entidade e Relacionamento(MER)

- 1° PASSO- entrevista com o cliente para entender o que ele precisa
- 2° ENTIDADE MODELO E RELACIONAMENTO

<img src="https://user-images.githubusercontent.com/52088444/151548132-f40fa911-5837-4979-85dc-7abbb1385bfc.png" width="90%"></img> 


**Dados ER**

- Entidade - representa uma coisa ou objeto do mundo real com uma existencia independete, a entidade possui uma existencia física ou conceitual, cada entidade possui atributos. Eles descrevem a Entidade.

<img src="https://user-images.githubusercontent.com/52088444/151548457-16c4348c-ab12-4a4a-8a79-51283d04e871.png" width="90%"></img> 

- Atributos Simples ou compostos, vai depender de como o usuario precisa
Ex: compostos: endereço;  simples: cidade, logradouro

## relacionamento
<img src="https://user-images.githubusercontent.com/52088444/151550819-a4d9f200-9f82-4749-b07c-91c2a434b486.png" width="90%"></img> 

# Entidade

<img src="https://user-images.githubusercontent.com/52088444/151553240-5473af32-9186-4cf7-afb2-bfbfac42aa0e.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151553455-a39c117c-175f-442b-8738-de8f4e729e60.png" width="45%"></img> 

**Como se representa, graficamente, os relacionamentos de entidades dependentes?**
Com um losango duplo

## representação de componentes

<img src="https://user-images.githubusercontent.com/52088444/151554676-e7c311fa-facb-4f99-a4cc-7ccfe96af912.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151554945-caf4bf05-b613-47fd-a699-c63a22238eac.png" width="45%"></img> 

<img src="https://user-images.githubusercontent.com/52088444/151555037-69aeb318-672b-41b5-bd2d-992bf4895fb2.png" width="90%"></img> 


**generalização ou especialização**
<img src="https://user-images.githubusercontent.com/52088444/151555742-b3efc162-1292-4f00-9fbc-ef7ee3706c61.png" width="45%"></img> 

**convenção mais usada, mais existem outras**

# Estudo de Caso

- Queremos coletar os dados pessoais de nossos **clientes**(entidade forte) como pessoa física ou jurídica. No caso de física, coletaremos o CPF e o RG, e no caso da jurídica, o CNPJ e IE. Mas também queremos coletar o nome, endereço, telefone e e-mail;
- Nossa livraria vende **livros**(entidade fraca /livro pertence a editora) com informações associadas, como título, categoria, ISBN (International Standard Book Number), ano de publicação, valor, editoria e autor ou autores;
- Os livros são fornecidos por **editoras**(entidade forte) que precisam ter o telefone, nome de contato, e-mail e no máximo dois telefones;
- Não podemos ter o mesmo livro de várias editoras, pois é exclusivo desta;
- O cliente pode comprar um ou mais livros por um **pedido de compra**(entidade fraca - depende de cliente e estoque/pedido de contra é feito pelo o cliente, o pedido contem um livro). Mas sempre que faz uma compra, precisamos verificar a disponibilidade no **estoque**(entidade fraca/ livro precisa existir no estoque para se fazer um pedido) para terminar a operação.

<img src="https://user-images.githubusercontent.com/52088444/151565109-7f37c249-3eb6-4108-974a-f3bb91a5ca7e.png" width="90%"></img> 