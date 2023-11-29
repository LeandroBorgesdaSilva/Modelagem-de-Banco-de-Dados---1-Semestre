<h1>🎦Cenário</h1>

O cliente procura um sistema de vendas de carros eficiente, onde ao chegar à nossa concessionária, será prontamente recebido por um vendedor dedicado. Para adquirir um veículo, é imprescindível que o cliente se cadastre em nosso sistema, fornecendo informações como nome, nome do meio, sobrenome, gênero, RG, e-mail, telefone, data de nascimento e idade, quando o atendimento acabar deverá ficar salvo no sistema qual vendedor realizou o atendimento para aquele cliente e caso o cliente compre um carro, esse deverá ficar salvo em seu registro.

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

INSERT INTO carro (marca, cor, ano, modelo, id_cliente, id_servicodemanutencao)
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




    

<h1>CRUD </h1>

<h1>Relatórios</h1>
