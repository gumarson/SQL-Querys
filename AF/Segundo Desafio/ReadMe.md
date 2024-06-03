<h3>Descrição</h3>
<p>Esse próximo desafio engloba a parte de normalização de uma tabela, onde teremo o exemplo a seguir para normalização:</p>
![image](https://github.com/gumarson/SQL-Querys/assets/155173740/06b2c48e-b8bb-48a9-b696-9c9e77d70691)

<h3>Requisitos</h3>
<p>
- Observe a tabela não normalizada de uma locadora de veículos e aplique a 3ª Forma normal;
- Faça o modelo lógico de banco de  dados relacional;
- Escreva o script que cria as tabelas;
- Crie uma view que seleciona todas as locações e seus respectivos veículos e clientes.
</p>

<h3>Resolução do desafio proposto:</h3>

<h3>Primeira noramlização</h3>
a tabela proposta já está na 1° normalização onde todos os atributos contém apenas os valores atômicos

<h3>Segunda normalização</h3>
A Segunda Forma Normal exige que a tabela esteja na 1NF e que todos os atributos não chave sejam totalmente dependentes da chave primária.

Identificação das Dependências:
Veículo, Cor, Placa e Diária dependem apenas do veículo.
Cliente, CPF e Nascimento dependem apenas do cliente.
Dias e Total dependem da locação.
Divisão das Tabelas:

Tabela Cliente
id_cliente
nome
cpf
data_nascimento

Tabela Veículo
id_veiculo
modelo
cor
placa
diária

Tabela Locação
id_locacao
id_cliente
id_veiculo
dias
total

Essas são as tabelas e seus atributos separados porém sem os exemplos inputados

<h3>Terceira normalização + scripts</h3>
A Terceira Forma Normal exige que a tabela esteja na 2NF e que todos os atributos não chave sejam independentes entre si, ou seja, não deve haver dependências transitivas.

Nossas tabelas já estão na 3NF, pois todos os atributos não chave são dependentes apenas da chave primária das respectivas tabelas.


![image](https://github.com/gumarson/SQL-Querys/assets/155173740/1c86a624-3be5-4196-856a-63e8225a037b)


<h3>Inserção dos dados</h3>

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/bc77ce3c-4b60-4e04-8500-f28e68c382cf)

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/17e87214-35e8-421e-a492-04048979746e)


![image](https://github.com/gumarson/SQL-Querys/assets/155173740/6ae2407c-730d-4ce5-8b4a-22aba6bac55b)


![image](https://github.com/gumarson/SQL-Querys/assets/155173740/8013323a-ea93-4da3-a0f4-e91d70a57f9a)




<h3>Criação das views</h3>
![image](https://github.com/gumarson/SQL-Querys/assets/155173740/40676cd0-95b7-4295-865b-0e39eab94eb4)



![image](https://github.com/gumarson/SQL-Querys/assets/155173740/a85fc71d-16f9-4ea7-9b66-81f7fec52903)







