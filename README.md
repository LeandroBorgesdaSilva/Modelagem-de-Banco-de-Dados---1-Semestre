<h1>🎦Cenário</h1>

O cliente procura um sistema de vendas de carros eficiente, onde ao chegar à nossa concessionária, será prontamente recebido por um vendedor dedicado. Para adquirir um veículo, é imprescindível que o cliente se cadastre em nosso sistema, fornecendo informações como nome, nome do meio, sobrenome, gênero, RG, e-mail, telefone, data de nascimento e idade.

O vendedor, por sua vez, deve conter em seu cadastro dados como nome, nome do meio, sobrenome, gênero, RG, e-mail, telefone, data de nascimento e idade, garantindo um atendimento personalizado e eficaz.

Os carros disponíveis em nossa loja terão informações detalhadas, incluindo marca, ano, cor e modelo para que o cliente possa fazer uma escolha consciente e alinhada com suas preferências.

No que diz respeito à manutenção dos veículos, a equipe de manutenção desempenha um papel fundamental. Cada serviço realizado terá registrado a data do serviço, o valor correspondente, o carro envolvido e a equipe responsável por essa manutenção.

Essa equipe de manutenção será composta por seis pessoas, organizadas em diferentes horários de trabalho, cada funcionário estará alocada em pelo menos 2 times. Teremos um líder designado para cada equipe, cujas informações de contato, juntamente com o horário de trabalho da equipe, serão registradas para assegurar um acompanhamento eficaz das atividades de manutenção.

Cada membro da equipe de manutenção, incluindo funcionários individuais, terá suas informações como telefone, nome, nome do meio, sobrenome, e-mail, gênero, RG, data de nascimento e idade devidamente registradas, garantindo assim um trabalho coordenado e eficiente para manter os veículos em excelentes condições.

<h1>Modelagem Conceitual</h1>

https://drive.google.com/file/d/17A_i0HOLAqzjhDvkU28m7RQSX_4iNIrj/view?usp=sharing

<h1>Modelagem Lógica</h1>

https://drive.google.com/file/d/1hjME-4vkaoV-pGO1cwEY_tU2drBq_Sx_/view?usp=sharing

<h1>Dados</h1>

*Criação da tabela Vendedor*

CREATE TABLE Vendedor (
    RG INT,
    Genero VARCHAR(9),
    PrimeiroNome VARCHAR(60),
    NomeMeio VARCHAR(60),
    UltimoNome VARCHAR(60),
    DataNascimento DATE,
    Idade INT
);

*Inserindo dados de 20 vendedores*

INSERT INTO Vendedor (RG, Genero, PrimeiroNome, NomeMeio, UltimoNome, DataNascimento, Idade)
VALUES
    (123456789, 'Masculino', 'João', 'Silva', 'Santos', '1990-05-15', 32),
    (987654321, 'Feminino', 'Maria', 'Ferreira', 'Oliveira', '1985-10-20', 37),
    (234567890, 'Masculino', 'Pedro', 'Henrique', 'Almeida', '1995-12-03', 27),
    (456789012, 'Feminino', 'Ana', 'Carolina', 'Pereira', '1992-08-28', 31),
    (789012345, 'Masculino', 'Lucas', 'Santos', 'Silveira', '1988-04-10', 34),
    (567890123, 'Feminino', 'Julia', 'Mendes', 'Rodrigues', '1998-07-22', 25),
    (321098765, 'Masculino', 'Marcos', 'Antônio', 'Rocha', '1980-11-05', 43),
    (890123456, 'Feminino', 'Carla', 'Xavier', 'Sousa', '1991-03-17', 30),
    (678901234, 'Masculino', 'Gustavo', 'Oliveira', 'Lima', '1993-09-09', 28),
    (901234567, 'Feminino', 'Beatriz', 'Fernandes', 'Costa', '1987-06-12', 36),
    (345678901, 'Masculino', 'Felipe', 'Gomes', 'Albuquerque', '1997-01-30', 26),
    (112233445, 'Feminino', 'Larissa', 'Santana', 'Pereira', '1983-02-25', 39),
    (998877665, 'Masculino', 'Rafael', 'Silveira', 'Costa', '1994-04-18', 29),
    (556677889, 'Feminino', 'Amanda', 'Martins', 'Cunha', '1999-09-05', 24),
    (334455667, 'Masculino', 'Henrique', 'Ferreira', 'Oliveira', '1986-12-07', 36),
    (778899001, 'Feminino', 'Camila', 'Ribeiro', 'Alves', '1996-08-14', 27),
    (990011223, 'Masculino', 'Thiago', 'Rodrigues', 'Gonçalves', '1990-07-01', 33),
    (667788990, 'Feminino', 'Bianca', 'Lima', 'Souza', '1993-05-19', 28),
    (112233445, 'Masculino', 'Diego', 'Sousa', 'Pereira', '1984-11-29', 38),
    (445566778, 'Feminino', 'Fernanda', 'Cruz', 'Mendes', '1997-04-03', 26),

<h1>CRUD </h1>

<h1>Relatórios</h1>
