<h1>🎦Cenário</h1>

O cliente procura um sistema de vendas de carros eficiente, onde ao chegar à nossa concessionária, será prontamente recebido por um vendedor dedicado. Para adquirir um veículo, é imprescindível que o cliente se cadastre em nosso sistema, fornecendo informações como nome, nome do meio, sobrenome, gênero, RG, e-mail, telefone, data de nascimento e idade, quando o atendimento acabar deverá ficar salvo no sistema qual vendedor realizou o atendimento para aquele cliente e caso o cliente compre um carro, esse deverá ficar salvo em seu registro.

O vendedor, por sua vez, deve conter em seu cadastro dados como nome, nome do meio, sobrenome, gênero, RG, e-mail, telefone, data de nascimento e idade, garantindo um atendimento personalizado e eficaz.

Os carros disponíveis em nossa loja terão informações detalhadas, incluindo marca, ano, cor e modelo para que o cliente possa fazer uma escolha consciente e alinhada com suas preferências.

No que diz respeito à manutenção dos veículos, a equipe de manutenção desempenha um papel fundamental. Cada serviço realizado terá registrado a data do serviço, o valor correspondente, o carro envolvido e a equipe responsável por essa manutenção.

Essa equipe de manutenção será composta por duas pessoas, organizadas em diferentes horários de trabalho, cada funcionário estará alocada em pelo menos 2 times. Teremos um líder designado para cada equipe, cujas informações de contato, juntamente com o horário de trabalho da equipe, serão registradas para assegurar um acompanhamento eficaz das atividades de manutenção.

Cada membro da equipe de manutenção, incluindo funcionários individuais, terá suas informações como telefone, nome, nome do meio, sobrenome, e-mail, gênero, RG, data de nascimento e idade devidamente registradas, garantindo assim um trabalho coordenado e eficiente para manter os veículos em excelentes condições.

<h1>Modelagem Conceitual</h1>

https://drive.google.com/file/d/17A_i0HOLAqzjhDvkU28m7RQSX_4iNIrj/view?usp=sharing

<h1>Modelagem Lógica</h1>

https://drive.google.com/file/d/1hjME-4vkaoV-pGO1cwEY_tU2drBq_Sx_/view?usp=sharing

<h1>Dados</h1>

<h2>Criação da tabela Vendedor</h2>

CREATE TABLE Vendedor (
    IdVendedor INT AUTO_INCREMENT PRIMARY KEY,
    RG INT,
    Genero VARCHAR(9),
    PrimeiroNome VARCHAR(60),
    NomeMeio VARCHAR(60),
    UltimoNome VARCHAR(60),
    DataNascimento DATE,
    Idade INT
);

<h2>Inserindo dados de 20 vendedores</h2>

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

<h2>Criação da tabela email do vendedor</h2>

CREATE TABLE email_vendedor (
    id_emailvendedor INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(60),
    id_vendedor INT,
    FOREIGN KEY (id_vendedor) REFERENCES Vendedor(IdVendedor)
);

<h2>Inserindo email dos vendedores</h2>

INSERT INTO email_vendedor (email, id_vendedor)
VALUES
    ('joao@gmail.com', 1),
    ('joaosilva@gmail.com', 1),
    ('maria@gmail.com', 2),
    ('pedro@gmail.com', 3),
    ('ana@gmail.com', 4),
    ('lucas@gmail.com', 5),
    ('julia@gmail.com', 6),
    ('marcos@gmail.com', 7),
    ('carla@gmail.com', 8),
    ('gustavo@gmail.com', 9),
    ('beatriz@gmail.com', 10),
    ('felipe@gmail.com', 11),
    ('larissa@gmail.com', 12),
    ('rafael@gmail.com', 13),
    ('rafaelsilveira@gmail.com', 13),
    ('amanda@gmail.com', 14),
    ('henrique@gmail.com', 15),
    ('camila@gmail.com', 16),
    ('thiago@gmail.com', 17),
    ('bianca@gmail.com', 18),
    ('diego@gmail.com', 19),
    ('fernanda@gmail.com', 20),
    ('fernandaCruz@gmail.com', 20),

<h2>Criação da tabela telefone do vendedor</h2>

CREATE TABLE telefone_vendedor (
    id_telefonedovendedor INT AUTO_INCREMENT PRIMARY KEY,
    telefone VARCHAR(60),
    id_vendedor INT,
    FOREIGN KEY (id_vendedor) REFERENCES Vendedor(IdVendedor)
);

<h2>Inserindo o telefone dos vendedores</h2>

  ('(11) 1234-5678', 1),
  ('(11) 1239-2345', 1),
  ('(21) 9876-5432', 2),
  ('(31) 4567-8901', 3),
  ('(41) 5555-1234', 4),
  ('(51) 7777-4321', 5),
  ('(62) 9999-8765', 6),
  ('(62) 9999-8806', 6),
  ('(71) 3333-4444', 7),
  ('(85) 2222-1111', 8),
  ('(92) 8888-9999', 9),
  ('(13) 7777-8888', 10),
  ('(81) 4444-5555', 11),
  ('(47) 2222-3333', 12),
  ('(17) 9999-7777', 13),
  ('(84) 3333-2222', 14),
  ('(27) 8888-1111', 15),
  ('(65) 7777-9999', 16),
  ('(98) 4444-5555', 17),
  ('(54) 3333-6666', 18),
  ('(31) 2222-8888', 19),
  ('(92) 7777-1111', 20),
  ('(92) 7777-2323', 20),
 
    
<h2>Criação da tabela cliente</h2>

CREATE TABLE cliente (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    RG INT,
    Genero VARCHAR(9),
    PrimeiroNome VARCHAR(60),
    NomeMeio VARCHAR(60),
    UltimoNome VARCHAR(60),
    DataNascimento DATE,
    Idade INT,
    id_vendedor INT,
    FOREIGN KEY (id_vendedor) REFERENCES Vendedor(IdVendedor)
);


<h2>Inserindo dados de 20 clientes</h2>

INSERT INTO cliente (RG, Genero, PrimeiroNome, NomeMeio, UltimoNome, DataNascimento, Idade, id_vendedor)
VALUES
    (123456789, 'Masculino', 'Carlos', 'Alberto', 'Silva', '1988-03-10', 33, 1),
    (987654321, 'Feminino', 'Patrícia', 'Fernandes', 'Oliveira', '1995-09-21', 28, 2),
    (234567890, 'Masculino', 'Ricardo', 'Henrique', 'Almeida', '1980-12-05', 43, 3),
    (456789012, 'Feminino', 'Laura', 'Carolina', 'Pereira', '1992-06-15', 29, 4),
    (789012345, 'Masculino', 'Fernando', 'Santos', 'Lima', '1987-07-28', 36, 5),
    (567890123, 'Feminino', 'Aline', 'Mendes', 'Rodrigues', '1998-01-03', 25, 6),
    (321098765, 'Masculino', 'Gabriel', 'Antônio', 'Rocha', '1983-11-18', 38, 7),
    (890123456, 'Feminino', 'Juliana', 'Xavier', 'Sousa', '1990-04-30', 31, 8),
    (678901234, 'Masculino', 'Mateus', 'Oliveira', 'Lima', '1993-02-08', 28, 9),
    (901234567, 'Feminino', 'Cristina', 'Fernandes', 'Costa', '1985-08-22', 36, 10),
    (345678901, 'Masculino', 'Diego', 'Gomes', 'Albuquerque', '1996-07-14', 25, 11),
    (112233445, 'Feminino', 'Valentina', 'Santana', 'Pereira', '1989-05-27', 32, 12),
    (998877665, 'Masculino', 'Raul', 'Silveira', 'Costa', '1994-10-09', 29, 13),
    (556677889, 'Feminino', 'Elisa', 'Martins', 'Cunha', '1999-12-01', 22, 14),
    (334455667, 'Masculino', 'Vinicius', 'Ferreira', 'Oliveira', '1986-02-13', 35, 15),
    (778899001, 'Feminino', 'Isabela', 'Ribeiro', 'Alves', '1997-04-17', 24, 16),
    (990011223, 'Masculino', 'Lucas', 'Rodrigues', 'Gonçalves', '1991-06-25', 30, 17),
    (667788990, 'Feminino', 'Caroline', 'Lima', 'Souza', '1994-11-08', 29, 18),
    (112233445, 'Masculino', 'Enzo', 'Sousa', 'Pereira', '1984-08-03', 37, 19),
    (445566778, 'Feminino', 'Mariana', 'Cruz', 'Mendes', '1997-10-12', 26, 20),



<h2>Criação da tabela email do cliente</h2>

CREATE TABLE email_cliente (
    id_emailcliente INT AUTO_INCREMENT PRIMARY KEY,
    email VARCHAR(60),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);

<h2>Inserindo email dos clientes</h2>

INSERT INTO email_cliente (email, id_cliente)
VALUES
    ('carlos@gmail.com', 1),
    ('carlos_silva@gmail.com', 1),
    ('patricia@gmail.com', 2),
    ('ricardo@gmail.com', 3),
    ('ricardo_almeida@gmail.com', 3),
    ('laura@gmail.com', 4),
    ('fernando@gmail.com', 5),
    ('aline@gmail.com', 6),
    ('aline_rodrigues@gmail.com', 6),
    ('gabriel@gmail.com', 7),
    ('juliana@gmail.com', 8),
    ('juliana_sousa@gmail.com', 8),
    ('mateus@gmail.com', 9),
    ('cristina@gmail.com', 10),
    ('cristina_costa@gmail.com', 10),
    ('diego@gmail.com', 11),
    ('valentina@gmail.com', 12),
    ('raul@gmail.com', 13),
    ('raul_costa@gmail.com', 13),
    ('elisa@gmail.com', 14),
    ('vinicius@gmail.com', 15),
    ('isabela@gmail.com', 16),
    ('isabela_alves@gmail.com', 16),
    ('lucas@gmail.com', 17),
    ('caroline@gmail.com', 18),
    ('enzo@gmail.com', 19),
    ('mariana@gmail.com', 20),
    ('mariana_mendes@gmail.com', 20),

    
<h2>Criação da tabela telefone do cliente</h2>

CREATE TABLE telefone_cliente (
    id_telefonecliente INT AUTO_INCREMENT PRIMARY KEY,
    telefone VARCHAR(60),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);

<h2>Inserindo o telefone dos clientess</h2>

INSERT INTO telefone_cliente (telefone, id_cliente)
VALUES
    ('(11) 1234-5678', 1),
    ('(21) 9876-5432', 1),
    ('(31) 4567-8901', 2),
    ('(41) 5555-1234', 3),
    ('(51) 7777-4321', 3),
    ('(62) 9999-8765', 4),
    ('(71) 3333-4444', 5),
    ('(85) 2222-1111', 6),
    ('(92) 8888-9999', 6),
    ('(13) 7777-8888', 7),
    ('(81) 4444-5555', 8),
    ('(47) 2222-3333', 9),
    ('(17) 9999-7777', 9),
    ('(84) 3333-2222', 10),
    ('(27) 8888-1111', 11),
    ('(65) 7777-9999', 12),
    ('(98) 4444-5555', 12),
    ('(54) 3333-6666', 13),
    ('(31) 2222-8888', 14),
    ('(92) 7777-1111', 14),
    ('(11) 8888-0000', 15);
    ('(11) 2188-4678', 15);
    ('(11) 8348-2784', 16);
    ('(11) 7573-3590', 17);
    ('(11) 2029-2168', 18);
    ('(11) 0988-7965', 19);
    ('(11) 0769-7764', 20);



<h2>Criação da tabela carro</h2>

CREATE TABLE carro (
  CREATE TABLE carro (
    id_carro INT AUTO_INCREMENT PRIMARY KEY,
    marca VARCHAR(20),
    cor VARCHAR(20),
    ano DATE,
    modelo VARCHAR(30),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);


<h2>Inserindo informações de 20 carros</h2>

INSERT INTO carro (marca, cor, ano, modelo, id_cliente)
VALUES
    ('Toyota', 'Preto', '2019-01-01', 'Corolla', 1),
    ('Honda', 'Prata', '2020-05-15', 'Civic', 2),
    ('Volkswagen', 'Azul', '2018-10-20', 'Golf', 3),
    ('Ford', 'Vermelho', '2017-07-07', 'Focus', 4),
    ('Chevrolet', 'Branco', '2021-12-30', 'Onix', 5),
    ('Hyundai', 'Cinza', '2019-03-25', 'HB20', 6),
    ('Renault', 'Azul Escuro', '2016-09-12', 'Sandero', 7),
    ('Fiat', 'Verde', '2020-11-05', 'Uno', 8),
    ('BMW', 'Prata', '2018-04-18', '320i', 9),
    ('Mercedes-Benz', 'Preto', '2017-06-22', 'CLA 250', 10),
    ('Audi', 'Vermelho', '2019-08-08', 'A4', 11),
    ('Kia', 'Branco', '2020-02-14', 'Sportage', 12),
    ('Nissan', 'Cinza', '2016-11-30', 'Versa', 13),
    ('Jeep', 'Azul Marinho', '2017-10-03', 'Renegade', 14),
    ('Peugeot', 'Bordô', '2018-07-19', '208', 15),
    ('Land Rover', 'Prata', '2021-04-26', 'Evoque', 16),
    ('Volvo', 'Preto', '2019-09-10', 'XC40', 17),
    ('Mitsubishi', 'Vermelho', '2017-12-05', 'Lancer', 18),
    ('Subaru', 'Azul', '2018-06-28', 'Impreza', 19),
    ('Ferrari', 'Vermelho', '2020-03-12', '488 GTB', 20);


<h2>Criação da tabela serviço de manutenção</h2>

CREATE TABLE servico_de_manutencao (
    id_servicodemanutencao INT AUTO_INCREMENT PRIMARY KEY,
    data_de_servico DATE,
    valor_de_servico DOUBLE,
    id_manutencao INT,
    id_carro INT,
    FOREIGN KEY (id_manutencao) REFERENCES manutencao(id_manutencao),
    FOREIGN KEY (id_carro) REFERENCES carro(id_carro)
);


<h2>Inserindo informações de registros de manutenção que ocorreram</h2>

INSERT INTO servico_de_manutencao (data_de_servico, valor_de_servico, id_manutencao, id_carro)
VALUES

 ('2023-01-10', 250.00, 1, 1),
 ('2023-02-22', 180.50, 2, 2),
 ('2023-03-15', 300.00, 3, 3),
 ('2023-04-05', 150.75, 4, 4),
 ('2023-05-18', 400.25, 5, 5),
 ('2023-06-20', 275.80, 6, 6),
 ('2023-07-03', 350.00, 7, 7),
 ('2023-08-12', 210.30, 8, 8),
 ('2023-09-28', 180.00, 9, 9),
 ('2023-10-14', 420.50, 10, 10),
 ('2023-11-30', 320.00, 11, 11),
 ('2023-12-25', 290.75, 12, 12),
 ('2024-01-05', 180.50, 13, 13),
 ('2024-02-17', 390.20, 14, 14),
 ('2024-03-08', 260.00, 15, 15),
 ('2024-04-21', 180.90, 16, 16),
 ('2024-05-14', 300.00, 17, 17),
 ('2024-06-30', 350.60, 18, 18),
 ('2024-07-18', 180.75, 19, 19),
 ('2024-08-22', 400.25, 20, 20);

<h2>Criação da tabela equipe de manutenção</h2>

CREATE TABLE equipe_de_manutencao (
    id_manutencao INT AUTO_INCREMENT PRIMARY KEY,
    horario_de_trabalho TIME,
    lider_da_equipe VARCHAR(60)
);


<h2>Inserindo informações das equipes de manutenção</h2>

INSERT INTO equipe_de_manutencao (horario_de_trabalho, lider_da_equipe)
VALUES
    ('08:00:00', 'João Silva'),
    ('09:30:00', 'Maria Oliveira'),
    ('10:45:00', 'Pedro Santos'),
    ('12:15:00', 'Ana Costa'),
    ('14:00:00', 'Marcos Rodrigues'),
    ('15:30:00', 'Carla Almeida'),
    ('16:45:00', 'Rafaela Pereira'),
    ('08:30:00', 'Fernando Gomes'),
    ('10:00:00', 'Aline Souza'),
    ('11:20:00', 'Gabriel Ferreira'),
    ('13:00:00', 'Juliana Martins'),
    ('14:45:00', 'Ricardo Vieira'),
    ('09:15:00', 'Luiza Carvalho'),
    ('10:45:00', 'Gustavo Oliveira'),
    ('12:00:00', 'Patrícia Silva'),
    ('13:30:00', 'Daniel Santos'),
    ('15:00:00', 'Mariana Costa'),
    ('16:20:00', 'Renato Rodrigues'),
    ('08:45:00', 'Lúcia Almeida'),
    ('10:10:00', 'Felipe Pereira');


<h2>Criação da tabela telefone da equipe de manutenção</h2>

CREATE TABLE telefone_equipe_de_manutencao (
    id_telefoneequipedemanutencao INT AUTO_INCREMENT PRIMARY KEY,
    telefone VARCHAR(60),
    id_manutencao INT,
    FOREIGN KEY (id_manutencao) REFERENCES equipe_de_manutencao(id_manutencao)
);

<h2>Inserindo informações dos telefones das equipes de manutenção</h2>

INSERT INTO telefone_equipe_de_manutencao (telefone, id_manutencao)
VALUES
    ('(16) 6345-2357', 1),
    ('(12) 7845-2357', 2),
    ('(13) 3467-1235', 3),
    ('(12) 2365-2167', 4),
    ('(15) 2354-2354', 5),
    ('(11) 2365-0098', 6),
    ('(13) 2179-2178', 7),
    ('(13) 0876-5678', 8),
    ('(16) 8678-1235', 9),
    ('(17) 4645-4567', 10),
    ('(15) 8879-3412', 11),
    ('(11) 9007-3122', 12),
    ('(12) 1245-1231', 13),
    ('(11) 2345-5345', 14),
    ('(13) 4334-5555', 15),
    ('(16) 7566-8787', 16),
    ('(11) 9067-5675', 17),
    ('(16) 3432-8656', 18),
    ('(11) 3241-5433', 19),
    ('(66) 1235-4564', 20);


<h2>Criação da tabela Funcionário de manutenção - Equipe de manutenção</h2>

CREATE TABLE Funcionario_de_manutencao_Equipe_de_manutencao (
    id_funcionariomanutencao INT,
    id_manutencao INT,
    FOREIGN KEY (id_funcionariomanutencao) REFERENCES funcionario_manutencao(id_funcionario),
    FOREIGN KEY (id_manutencao) REFERENCES equipe_de_manutencao(id_manutencao)
);

<h2>Inserindo informações na tabela Funcionario_de_manutencao_Equipe_de_manutencao </h2>

INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao (id_funcionariomanutencao, id_manutencao)
VALUES
(1,1)
(1,2)
(2,1)
(2,2)
(3,3)
(3,4)
(4,3)
(4,4)
(5,5)
(5,6)
(6,5)
(6,6)
(7,7)
(7,8)
(8,8)
(8,9)
(9,8)
(9,9)
(10,10)
(10,11)
(11,10)
(11,11)
(12,12)
(12,13)
(13,12)    
(13,13)
(14,14)
(14,15)
(15,14)
(15,15)
(16,16)
(16,17)
(17,16)
(17,17)
(18,18)
(18,19)
(19,19)
(19,20)
(20,29)
(20,20)


<h2>Criação da tabela Funcionário de manutenção</h2>

CREATE TABLE Funcionario_de_manutencao (
    id_funcionariomanutencao INT AUTO_INCREMENT PRIMARY KEY,
    RG INT,
    Genero VARCHAR(9),
    primeiro_nome VARCHAR(60),
    nome_do_meio VARCHAR(60),
    nome_final VARCHAR(60),
    data_de_nascimento DATE,
    idade INT
);

<h2>Inserindo informações na tabela Funcionario_de_manutencao</h2>

INSERT INTO Funcionario_de_manutencao (RG, Genero, primeiro_nome, nome_do_meio, nome_final, data_de_nascimento, idade)
VALUES
    (123456, 'Masculino', 'João', 'Silva', 'Junior', '1980-05-15', 42),
    (234567, 'Feminino', 'Maria', 'Oliveira', 'Pereira', '1985-08-20', 37),
    (345678, 'Masculino', 'Pedro', 'Santos', 'Silveira', '1990-11-10', 32),
    (456789, 'Feminino', 'Ana', 'Costa', 'Martins', '1988-03-25', 34),
    (567890, 'Masculino', 'Marcos', 'Rodrigues', 'Almeida', '1992-07-07', 29),
    (678901, 'Feminino', 'Carla', 'Almeida', 'Pereira', '1987-09-12', 35),
    (789012, 'Masculino', 'Rafael', 'Pereira', 'Gomes', '1995-01-30', 27),
    (890123, 'Feminino', 'Fernanda', 'Gomes', 'Souza', '1993-04-18', 29),
    (901234, 'Masculino', 'Lucas', 'Silva', 'Ferreira', '1991-12-05', 30),
    (123401, 'Feminino', 'Aline', 'Souza', 'Rocha', '1989-06-22', 33),
    (234012, 'Masculino', 'Gabriel', 'Ferreira', 'Machado', '1986-10-09', 36),
    (340123, 'Feminino', 'Juliana', 'Martins', 'Santos', '1994-02-14', 28),
    (401234, 'Masculino', 'Mateus', 'Almeida', 'Oliveira', '1984-11-30', 37),
    (512345, 'Feminino', 'Rafaela', 'Oliveira', 'Rodrigues', '1990-09-08', 31),
    (612340, 'Masculino', 'Diego', 'Rodrigues', 'Costa', '1997-07-03', 24),
    (723401, 'Feminino', 'Luana', 'Costa', 'Santos', '1987-04-20', 34),
    (834012, 'Masculino', 'Miguel', 'Santos', 'Gonçalves', '1993-03-17', 28),
    (945678, 'Feminino', 'Larissa', 'Gonçalves', 'Alves', '1995-12-12', 26),
    (156789, 'Masculino', 'Bruno', 'Alves', 'Ribeiro', '1988-08-28', 33),
    (267890, 'Feminino', 'Isabela', 'Ribeiro', 'Mendes', '1991-05-01', 30);


<h2>Criação da tabela Telefone do funcionário de manutenção</h2>

CREATE TABLE Telefone_funcionario_manutencao (
    ID_Telefonefuncionariomanutencao INT AUTO_INCREMENT PRIMARY KEY,
    Telefone VARCHAR(60),
    ID_Funcionariomanutencao INT,
    FOREIGN KEY (ID_Funcionariomanutencao) REFERENCES Funcionario_de_manutencao(id_funcionariomanutencao)
);

<h2>Inserindo informações na tabela Telefone do funcionário de manutenção</h2>

  ('(11) 7534-1237', 1),
  ('(24) 3456-1674', 2),
  ('(16) 5667-2345', 3),
  ('(13) 3456-6789', 4),
  ('(13) 2367-5679', 5),
  ('(12) 6789-0098', 6),
  ('(16) 5675-6783', 7),
  ('(11) 7545-6455', 8),
  ('(12) 6474-6465', 9),
  ('(13) 6745-6789', 10),
  ('(24) 4567-1234', 11),
  ('(12) 4567-3456', 12),
  ('(16) 4567-1235', 13),
  ('(24) 4745-2346', 14),
  ('(11) 4574-1234', 15),
  ('(13) 3453-1234', 16),
  ('(16) 3456-12356', 17),
  ('(12) 3456-4567', 18),
  ('(24) 2134-6789', 19),
  ('(11) 1200-4567', 20),


















<h1>CRUD </h1>

<h1>Relatórios</h1>
