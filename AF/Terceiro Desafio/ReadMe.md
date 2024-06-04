# Terceiro Desafio

## Etapa 1: Localização do Google
Transforme a seguinte configuração do Google para o formato JSON:

[localização_google_sp.json](https://github.com/user-attachments/files/15541022/localizacao_google_sp.json)

---

## Etapa 2: Normalização de Dados

![Planilha de Funcionários](https://github.com/gumarson/SQL-Querys/assets/155173740/10925942-c255-4763-affb-174fd2c9dea5)

### Primeira Normalização (1NF)
Para atingir a 1NF, devemos eliminar os valores múltiplos em uma única célula. Cada valor atômico deve estar em uma célula separada, ou seja, uma tabela para funcionários e outra para e-mails.

**Tabela Funcionario:**
- `id_funcionario`
- `nome`
- `endereço`
- `cargo`
- `jornada`
- `salário`

**Tabela Email:**
- `id_email`
- `id_funcionario`
- `email`

### Segunda Normalização (2NF)
Para atingir a 2NF, todos os atributos não chave devem depender da chave primária. Já atingimos essa forma com as tabelas acima, pois cada tabela tem uma chave primária única e todos os atributos dependem dessa chave.

### Terceira Normalização (3NF)
A 3ª Forma Normal não ocorre porque para existir dependências transitivas na tabela, isso já não ocorre nas tabelas atuais, logo, não é necessário.

---

## Modelo Relacional e Arquivo no Formato JSON

![Modelo Relacional](https://github.com/gumarson/SQL-Querys/assets/155173740/4b50dc27-4484-4074-bb8a-b732c1bd7311)

[funcionario.json](https://github.com/user-attachments/files/15541070/funcionario.json)

---

## Relacionamento no Firestore

Acesse o exemplo de relacionamento no Firestore através do link abaixo:

[Console Firebase](https://console.firebase.google.com/u/0/project/first-project-aaa82/firestore/databases/-default-/data/~2FAnimais~2FGarfield?hl=pt)

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/80346f81-9606-4e37-9abc-13676484cd78)








