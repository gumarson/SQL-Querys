Aqui está as tabelas da atividade relacionadas á Usina de projetos, onde foi designado ao meu grupo para realizar o MER e DER em conjunto com as tabelas e scripts sql sobre a cantina de uma faculdade

Aqui está representado a tabela de funcionários e seu script:

CREATE TABLE funcionarios (
    id INT PRIMARY KEY AUTO_INCREMENT,
    nome VARCHAR(255),
    cpf VARCHAR(14),
    salario DECIMAL(10, 2),
    data_de_nascimento DATE,
    telefone VARCHAR(15),
    cep VARCHAR(9)
);

INSERT INTO funcionarios (nome, cpf, salario, data_de_nascimento, telefone, cep) VALUES
('João da Silva', '12345678910', 3500.00, '1990-05-15', '(11) 987654321', '01234-567'),
('Maria Oliveira', '98765432100', 4200.00, '1985-08-20', '(11) 912345678', '04567-890'),
('Pedro Santos', '23456789021', 2800.00, '1982-11-10', '(11) 923456789', '07890-123'),
('Ana Pereira', '87654321001', 4000.00, '1978-03-25', '(11) 934567890', '09876-543'),
('Carlos Souza', '34567890132', 3200.00, '1995-07-08', '(11) 945678901', '05678-901'),
('Fernanda Lima', '76543210902', 3700.00, '1989-09-30', '(11) 956789012', '08901-234'),
('Luiz Oliveira', '45678901243', 4500.00, '1983-12-17', '(11) 967890123', '01234-678'),
('Vanessa Silva', '65432109803', 3000.00, '1992-04-05', '(11) 978901234', '04567-234'),
('Rafaela Santos', '56789012354', 3800.00, '1975-06-29', '(11) 989012345', '07890-567'),
('Thiago Pereira', '43210987604', 4100.00, '1987-10-12', '(11) 991234567', '09876-012');


![image](https://github.com/gumarson/SQL-Querys/assets/155173740/d82bc1c9-0a97-463f-bf23-8e55bf5d25e3)

E aqui está representado a tabela de produtos e seu script:

CREATE TABLE produtos (
    id INT PRIMARY KEY IDENTITY(1,1),
    nome VARCHAR(255),
    tipo VARCHAR(50),
    estoque INT,
    marca VARCHAR(100)
);

INSERT INTO produtos (nome, tipo, estoque, marca) VALUES
('Salgado de Frango', 'Salgado', 50, 'Cantina da Facens'),
('Suco de Laranja 300ml', 'Suco', 30, 'Del Valle'),
('Misto Quente', 'Sanduíche', 100, 'Cantina da Facens'),
('Pão de Queijo', 'Salgado', 40, 'Cantina da Facens'),
('Café', 'Bebida Quente', 80, 'Cantina da Facens'),
('Salgado de Presunto e Queijo', 'Salgado', 60, 'Cantina da Facens'),
('Bolo de Chocolate', 'Bolo', 70, 'Cantina da Facens'),
('Refrigerante Lata 350ml', 'Refrigerante', 90, 'Coca-Cola'),
('Salgado de Carne', 'Salgado', 35, 'Cantina da Facens'),
('Coxinha', 'Salgado', 120, 'Cantina da Facens');


![image](https://github.com/gumarson/SQL-Querys/assets/155173740/96f7e2ab-e338-426a-a2ec-68b5c3005d23)



Os participantes do grupo são

- Gustavo M.
- Caio H.
- Felipe S.
