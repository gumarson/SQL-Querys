# Desafio de Normalização de Tabela

## Descrição
Este desafio envolve a normalização de uma tabela. A seguir, temos um exemplo para ser normalizado:

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/06b2c48e-b8bb-48a9-b696-9c9e77d70691)

## Requisitos
- Observe a tabela não normalizada de uma locadora de veículos e aplique a 3ª Forma Normal.
- Crie o modelo lógico de banco de dados relacional.
- Escreva o script que cria as tabelas.
- Crie uma view que seleciona todas as locações e seus respectivos veículos e clientes.

## Resolução do Desafio

### Primeira Normalização
A tabela proposta já está na 1ª Forma Normal, onde todos os atributos contêm apenas valores atômicos.

### Segunda Normalização
A 2ª Forma Normal exige que a tabela esteja na 1NF e que todos os atributos não chave sejam totalmente dependentes da chave primária.

#### Identificação das Dependências
- **Veículo, Cor, Placa e Diária** dependem apenas do veículo.
- **Cliente, CPF e Nascimento** dependem apenas do cliente.
- **Dias e Total** dependem da locação.

#### Divisão das Tabelas

**Tabela Cliente**
- id_cliente
- nome
- cpf
- data_nascimento

**Tabela Veículo**
- id_veiculo
- modelo
- cor
- placa
- diária

**Tabela Locação**
- id_locacao
- id_cliente
- id_veiculo
- dias
- total

Essas são as tabelas e seus atributos separados, porém sem os exemplos inputados.

### Terceira Normalização + Scripts
A 3ª Forma Normal exige que a tabela esteja na 2NF e que todos os atributos não chave sejam independentes entre si, ou seja, não deve haver dependências transitivas.

Nossas tabelas já estão na 3NF, pois todos os atributos não chave são dependentes apenas da chave primária das respectivas tabelas.

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/1c86a624-3be5-4196-856a-63e8225a037b)

## Inserção dos Dados

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/bc77ce3c-4b60-4e04-8500-f28e68c382cf)

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/17e87214-35e8-421e-a492-04048979746e)



![image](https://github.com/gumarson/SQL-Querys/assets/155173740/6ae2407c-730d-4ce5-8b4a-22aba6bac55b)



![image](https://github.com/gumarson/SQL-Querys/assets/155173740/8013323a-ea93-4da3-a0f4-e91d70a57f9a)

## Criação das Views

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/40676cd0-95b7-4295-865b-0e39eab94eb4)




![image](https://github.com/gumarson/SQL-Querys/assets/155173740/a85fc71d-16f9-4ea7-9b66-81f7fec52903)




