Criação das tabelas e inserção de exemplos : 
CREATE TABLE Professores (
    id_professor INT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    departamento VARCHAR(50)
);

-- Tabela Cursos
CREATE TABLE Cursos (
    id_curso INT PRIMARY KEY,
    nome VARCHAR(100),
    descricao TEXT,
);

-- Tabela Alunos
CREATE TABLE Alunos (
    id_aluno INT PRIMARY KEY,
    nome VARCHAR(100),
    email VARCHAR(100),
    curso_id INT, -- chave estrangeira referenciando a tabela Cursos
    FOREIGN KEY (curso_id) REFERENCES Cursos(id_curso)
);

![image](https://github.com/gumarson/SQL-Querys/assets/155173740/15e37fdf-a56f-437e-8c69-20a51c7a65fb)



store procedure - inserir cursos
CREATE PROCEDURE InserirCurso(
    @nome VARCHAR(100),
    @descricao TEXT,
    @duracao INT
)
AS
BEGIN
    INSERT INTO Cursos (nome, descricao, duracao)
    VALUES (@nome, @descricao, @duracao);
END;


stored proccedures - selecioonar cursos 
CREATE PROCEDURE SelecionarCursos
AS
BEGIN
    SELECT * FROM Cursos;
END;





funcao do email do aluno ---

CREATE FUNCTION GerarEmailAluno(
    @nome VARCHAR(100),
    @sobrenome VARCHAR(100)
)
RETURNS VARCHAR(100)
AS
BEGIN
    DECLARE @email VARCHAR(100);
    DECLARE @contador INT;

    SET @contador = 1;
    SET @email = LOWER(CONCAT(@nome, '.', @sobrenome, '@dominio.com'));

    -- Verifica se o e-mail já existe na tabela Alunos
    WHILE EXISTS (SELECT 1 FROM Alunos WHERE email = @email)
    BEGIN
        SET @contador = @contador + 1;
        SET @email = LOWER(CONCAT(@nome, '.', @sobrenome, @contador, '@dominio.com'));
    END;

    RETURN @email;
END;


