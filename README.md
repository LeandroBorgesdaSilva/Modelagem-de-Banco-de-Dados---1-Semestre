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
    IdVendedor INTEGER PRIMARY KEY,
    RG INT,
    Genero VARCHAR(9),
    PrimeiroNome VARCHAR(60),
    NomeMeio VARCHAR(60),
    UltimoNome VARCHAR(60),
    DataNascimento DATE,
    Idade INT
);



<h2>Inserindo dados de 20 vendedores</h2>


   INSERT INTO Vendedor VALUES (null,123456789, 'Masculino', 'João', 'Silva', 'Santos', '1990-05-15', 32);
   INSERT INTO Vendedor VALUES (null,987654321, 'Feminino', 'Maria', 'Ferreira', 'Oliveira', '1985-10-20', 37);
   INSERT INTO Vendedor VALUES (null,234567890, 'Masculino', 'Pedro', 'Henrique', 'Almeida', '1995-12-03', 27);
   INSERT INTO Vendedor VALUES  (null,456789012, 'Feminino', 'Ana', 'Carolina', 'Pereira', '1992-08-28', 31);
   INSERT INTO Vendedor VALUES (null,789012345, 'Masculino', 'Lucas', 'Santos', 'Silveira', '1988-04-10', 34);
   INSERT INTO Vendedor VALUES (null,567890123, 'Feminino', 'Julia', 'Mendes', 'Rodrigues', '1998-07-22', 25);
   INSERT INTO Vendedor VALUES (null,321098765, 'Masculino', 'Marcos', 'Antônio', 'Rocha', '1980-11-05', 43);
   INSERT INTO Vendedor VALUES (null,890123456, 'Feminino', 'Carla', 'Xavier', 'Sousa', '1991-03-17', 30);
   INSERT INTO Vendedor VALUES (null,678901234, 'Masculino', 'Gustavo', 'Oliveira', 'Lima', '1993-09-09', 28);
   INSERT INTO Vendedor VALUES (null,901234567, 'Feminino', 'Beatriz', 'Fernandes', 'Costa', '1987-06-12', 36);
   INSERT INTO Vendedor VALUES (null,345678901, 'Masculino', 'Felipe', 'Gomes', 'Albuquerque', '1997-01-30', 26);
   INSERT INTO Vendedor VALUES (null,112233445, 'Feminino', 'Larissa', 'Santana', 'Pereira', '1983-02-25', 39);
   INSERT INTO Vendedor VALUES (null,998877665, 'Masculino', 'Rafael', 'Silveira', 'Costa', '1994-04-18', 29);
   INSERT INTO Vendedor VALUES (null,556677889, 'Feminino', 'Amanda', 'Martins', 'Cunha', '1999-09-05', 24);
   INSERT INTO Vendedor VALUES  (null,334455667, 'Masculino', 'Henrique', 'Ferreira', 'Oliveira', '1986-12-07', 36);
   INSERT INTO Vendedor VALUES  (null,778899001, 'Feminino', 'Camila', 'Ribeiro', 'Alves', '1996-08-14', 27);
   INSERT INTO Vendedor VALUES  (null,990011223, 'Masculino', 'Thiago', 'Rodrigues', 'Gonçalves', '1990-07-01', 33);
   INSERT INTO Vendedor VALUES  (null,667788990, 'Feminino', 'Bianca', 'Lima', 'Souza', '1993-05-19', 28);
   INSERT INTO Vendedor VALUES  (null,112233445, 'Masculino', 'Diego', 'Sousa', 'Pereira', '1984-11-29', 38);
   INSERT INTO Vendedor VALUES  (null,445566778, 'Feminino', 'Fernanda', 'Cruz', 'Mendes', '1997-04-03', 26);

<h2>Criação da tabela email do vendedor</h2>


CREATE TABLE email_vendedor (
    id_emailvendedor INTEGER PRIMARY KEY,
    email VARCHAR(60),
    id_vendedor INT,
    FOREIGN KEY (id_vendedor) REFERENCES Vendedor(IdVendedor)
);

<h2>Inserindo email dos vendedores</h2>


  INSERT INTO email_vendedor VALUES   (null,'joao@gmail.com', 1);
  INSERT INTO email_vendedor VALUES  (null,'joaosilva@gmail.com', 1);
  INSERT INTO email_vendedor VALUES  (null,'maria@gmail.com', 2);
  INSERT INTO email_vendedor VALUES  (null,'pedro@gmail.com', 3);
  INSERT INTO email_vendedor VALUES  (null,'ana@gmail.com', 4);
  INSERT INTO email_vendedor VALUES  (null,'lucas@gmail.com', 5);
  INSERT INTO email_vendedor VALUES  (null,'julia@gmail.com', 6);
  INSERT INTO email_vendedor VALUES  (null,'marcos@gmail.com', 7);
  INSERT INTO email_vendedor VALUES  (null,'carla@gmail.com', 8);
  INSERT INTO email_vendedor VALUES  (null,'gustavo@gmail.com', 9);
  INSERT INTO email_vendedor VALUES   (null,'beatriz@gmail.com', 10);
  INSERT INTO email_vendedor VALUES  (null,'felipe@gmail.com', 11);
  INSERT INTO email_vendedor VALUES  (null,'larissa@gmail.com', 12);
  INSERT INTO email_vendedor VALUES  (null,'rafael@gmail.com', 13);
  INSERT INTO email_vendedor VALUES  (null,'rafaelsilveira@gmail.com', 13);
  INSERT INTO email_vendedor VALUES   (null,'amanda@gmail.com', 14);
  INSERT INTO email_vendedor VALUES  (null,'henrique@gmail.com', 15);
  INSERT INTO email_vendedor VALUES   (null,'camila@gmail.com', 16);
  INSERT INTO email_vendedor VALUES  (null,'thiago@gmail.com', 17);
  INSERT INTO email_vendedor VALUES  (null,'bianca@gmail.com', 18);
  INSERT INTO email_vendedor VALUES  (null,'diego@gmail.com', 19);
  INSERT INTO email_vendedor VALUES  (null,'fernanda@gmail.com', 20);
  INSERT INTO email_vendedor VALUES  (null,'fernandaCruz@gmail.com', 20);

<h2>Criação da tabela telefone do vendedor</h2>

CREATE TABLE telefone_vendedor (
    id_telefonedovendedor INTEGER PRIMARY KEY,
    telefone VARCHAR(60),
    id_vendedor INT,
    FOREIGN KEY (id_vendedor) REFERENCES Vendedor(IdVendedor)
);

<h2>Inserindo o telefone dos vendedores</h2>



INSERT INTO telefone_vendedor VALUES (null,'(11) 1234-5678', 1);
INSERT INTO telefone_vendedor VALUES  (null,'(11) 1239-2345', 1);
INSERT INTO telefone_vendedor VALUES  (null,'(21) 9876-5432', 2);
INSERT INTO telefone_vendedor VALUES  (null,'(31) 4567-8901', 3);
INSERT INTO telefone_vendedor VALUES  (null,'(41) 5555-1234', 4);
INSERT INTO telefone_vendedor VALUES  (null,'(51) 7777-4321', 5);
INSERT INTO telefone_vendedor VALUES  (null,'(62) 9999-8765', 6);
INSERT INTO telefone_vendedor VALUES  (null,'(62) 9999-8806', 6);
INSERT INTO telefone_vendedor VALUES  (null,'(71) 3333-4444', 7);
INSERT INTO telefone_vendedor VALUES  (null,'(85) 2222-1111', 8);
INSERT INTO telefone_vendedor VALUES  (null,'(92) 8888-9999', 9);
INSERT INTO telefone_vendedor VALUES  (null,'(13) 7777-8888', 10);
INSERT INTO telefone_vendedor VALUES  (null,'(81) 4444-5555', 11);
INSERT INTO telefone_vendedor VALUES  (null,'(47) 2222-3333', 12);
INSERT INTO telefone_vendedor VALUES  (null,'(17) 9999-7777', 13);
INSERT INTO telefone_vendedor VALUES  (null,'(84) 3333-2222', 14);
INSERT INTO telefone_vendedor VALUES  (null,'(27) 8888-1111', 15);
INSERT INTO telefone_vendedor VALUES  (null,'(65) 7777-9999', 16);
INSERT INTO telefone_vendedor VALUES  (null,'(98) 4444-5555', 17);
INSERT INTO telefone_vendedor VALUES  (null,'(54) 3333-6666', 18);
INSERT INTO telefone_vendedor VALUES  (null,'(31) 2222-8888', 19);
INSERT INTO telefone_vendedor VALUES  (null,'(92) 7777-1111', 20);
INSERT INTO telefone_vendedor VALUES  (null,'(92) 7777-2323', 20);
 
    
<h2>Criação da tabela cliente</h2>

CREATE TABLE cliente (
    id_cliente INTEGER PRIMARY KEY,
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


   INSERT INTO cliente VALUES (null,123456789, 'Masculino', 'Carlos', 'Alberto', 'Silva', '1988-03-10', 33, 1);
   INSERT INTO cliente VALUES  (null,987654321, 'Feminino', 'Patrícia', 'Fernandes', 'Oliveira', '1995-09-21', 28, 2);
   INSERT INTO cliente VALUES  (null,234567890, 'Masculino', 'Ricardo', 'Henrique', 'Almeida', '1980-12-05', 43, 3);
   INSERT INTO cliente VALUES (null,456789012, 'Feminino', 'Laura', 'Carolina', 'Pereira', '1992-06-15', 29, 4);
   INSERT INTO cliente VALUES (null,789012345, 'Masculino', 'Fernando', 'Santos', 'Lima', '1987-07-28', 36, 5);
   INSERT INTO cliente VALUES (null,567890123, 'Feminino', 'Aline', 'Mendes', 'Rodrigues', '1998-01-03', 25, 6);
   INSERT INTO cliente VALUES (null,321098765, 'Masculino', 'Gabriel', 'Antônio', 'Rocha', '1983-11-18', 38, 7);
   INSERT INTO cliente VALUES (null,890123456, 'Feminino', 'Juliana', 'Xavier', 'Sousa', '1990-04-30', 31, 8);
   INSERT INTO cliente VALUES (null,678901234, 'Masculino', 'Mateus', 'Oliveira', 'Lima', '1993-02-08', 28, 9);
   INSERT INTO cliente VALUES (null,901234567, 'Feminino', 'Cristina', 'Fernandes', 'Costa', '1985-08-22', 36, 10);
   INSERT INTO cliente VALUES (null,345678901, 'Masculino', 'Diego', 'Gomes', 'Albuquerque', '1996-07-14', 25, 11);
   INSERT INTO cliente VALUES (null,112233445, 'Feminino', 'Valentina', 'Santana', 'Pereira', '1989-05-27', 32, 12);
   INSERT INTO cliente VALUES  (null,998877665, 'Masculino', 'Raul', 'Silveira', 'Costa', '1994-10-09', 29, 13);
   INSERT INTO cliente VALUES (null,556677889, 'Feminino', 'Elisa', 'Martins', 'Cunha', '1999-12-01', 22, 14);
   INSERT INTO cliente VALUES (null,334455667, 'Masculino', 'Vinicius', 'Ferreira', 'Oliveira', '1986-02-13', 35, 15);
   INSERT INTO cliente VALUES (null,778899001, 'Feminino', 'Isabela', 'Ribeiro', 'Alves', '1997-04-17', 24, 16);
   INSERT INTO cliente VALUES (null,990011223, 'Masculino', 'Lucas', 'Rodrigues', 'Gonçalves', '1991-06-25', 30, 17);
   INSERT INTO cliente VALUES (null,667788990, 'Feminino', 'Caroline', 'Lima', 'Souza', '1994-11-08', 29, 18);
   INSERT INTO cliente VALUES (null,112233445, 'Masculino', 'Enzo', 'Sousa', 'Pereira', '1984-08-03', 37, 19);
   INSERT INTO cliente VALUES (null,445566778, 'Feminino', 'Mariana', 'Cruz', 'Mendes', '1997-10-12', 26, 20);



<h2>Criação da tabela email do cliente</h2>

CREATE TABLE email_cliente (
    id_emailcliente INTEGER PRIMARY KEY,
    email VARCHAR(60),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);

<h2>Inserindo email dos clientes</h2>


   INSERT INTO email_cliente VALUES (null,'carlos@gmail.com', 1);
   INSERT INTO email_cliente VALUES (null,'carlos_silva@gmail.com', 1);
   INSERT INTO email_cliente VALUES (null,'patricia@gmail.com', 2);
   INSERT INTO email_cliente VALUES (null,'ricardo@gmail.com', 3);
   INSERT INTO email_cliente VALUES (null,'ricardo_almeida@gmail.com', 3);
   INSERT INTO email_cliente VALUES (null,'laura@gmail.com', 4);
   INSERT INTO email_cliente VALUES (null,'fernando@gmail.com', 5);
   INSERT INTO email_cliente VALUES (null,'aline@gmail.com', 6);
   INSERT INTO email_cliente VALUES  (null,'aline_rodrigues@gmail.com', 6);
   INSERT INTO email_cliente VALUES  (null,'gabriel@gmail.com', 7);
   INSERT INTO email_cliente VALUES (null,'juliana@gmail.com', 8);
   INSERT INTO email_cliente VALUES (null,'juliana_sousa@gmail.com', 8);
   INSERT INTO email_cliente VALUES  (null,'mateus@gmail.com', 9);
   INSERT INTO email_cliente VALUES  (null,'cristina@gmail.com', 10);
   INSERT INTO email_cliente VALUES  (null,'cristina_costa@gmail.com', 10);
   INSERT INTO email_cliente VALUES  (null,'diego@gmail.com', 11);
   INSERT INTO email_cliente VALUES  (null,'valentina@gmail.com', 12);
   INSERT INTO email_cliente VALUES (null,'raul@gmail.com', 13);
   INSERT INTO email_cliente VALUES  (null,'raul_costa@gmail.com', 13);
   INSERT INTO email_cliente VALUES  (null,'elisa@gmail.com', 14);
   INSERT INTO email_cliente VALUES  (null,'vinicius@gmail.com', 15);
   INSERT INTO email_cliente VALUES  (null,'isabela@gmail.com', 16);
   INSERT INTO email_cliente VALUES  (null,'isabela_alves@gmail.com', 16);
   INSERT INTO email_cliente VALUES  (null,'lucas@gmail.com', 17);
   INSERT INTO email_cliente VALUES (null,'caroline@gmail.com', 18);
   INSERT INTO email_cliente VALUES (null,'enzo@gmail.com', 19);
   INSERT INTO email_cliente VALUES  (null,'mariana@gmail.com', 20);
   INSERT INTO email_cliente VALUES  (null,'mariana_mendes@gmail.com', 20);

    
<h2>Criação da tabela telefone do cliente</h2>

CREATE TABLE telefone_cliente (
    id_telefonecliente INTEGER PRIMARY KEY,
    telefone VARCHAR(60),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);

<h2>Inserindo o telefone dos clientess</h2>


   INSERT INTO telefone_cliente VALUES (null,'(11) 1234-5678', 1);
   INSERT INTO telefone_cliente VALUES (null,'(21) 9876-5432', 1);
   INSERT INTO telefone_cliente VALUES (null,'(31) 4567-8901', 2);
   INSERT INTO telefone_cliente VALUES (null,'(41) 5555-1234', 3);
   INSERT INTO telefone_cliente VALUES (null,'(51) 7777-4321', 3);
   INSERT INTO telefone_cliente VALUES (null,'(62) 9999-8765', 4);
   INSERT INTO telefone_cliente VALUES (null,'(71) 3333-4444', 5);
   INSERT INTO telefone_cliente VALUES (null,'(85) 2222-1111', 6);
   INSERT INTO telefone_cliente VALUES (null,'(92) 8888-9999', 6);
   INSERT INTO telefone_cliente VALUES  (null,'(13) 7777-8888', 7);
   INSERT INTO telefone_cliente VALUES (null,'(81) 4444-5555', 8);
   INSERT INTO telefone_cliente VALUES (null,'(47) 2222-3333', 9);
   INSERT INTO telefone_cliente VALUES (null,'(17) 9999-7777', 9);
   INSERT INTO telefone_cliente VALUES (null,'(84) 3333-2222', 10);
   INSERT INTO telefone_cliente VALUES (null,'(27) 8888-1111', 11);
   INSERT INTO telefone_cliente VALUES (null,'(65) 7777-9999', 12);
   INSERT INTO telefone_cliente VALUES (null,'(98) 4444-5555', 12);
   INSERT INTO telefone_cliente VALUES (null,'(54) 3333-6666', 13);
   INSERT INTO telefone_cliente VALUES  (null,'(31) 2222-8888', 14);
   INSERT INTO telefone_cliente VALUES  (null,'(92) 7777-1111', 14);
   INSERT INTO telefone_cliente VALUES (null,'(11) 8888-0000', 15);
   INSERT INTO telefone_cliente VALUES (null,'(11) 2188-4678', 15);
   INSERT INTO telefone_cliente VALUES  (null,'(11) 8348-2784', 16);
   INSERT INTO telefone_cliente VALUES (null,'(11) 7573-3590', 17);
   INSERT INTO telefone_cliente VALUES (null,'(11) 2029-2168', 18);
   INSERT INTO telefone_cliente VALUES (null,'(11) 0988-7965', 19);
   INSERT INTO telefone_cliente VALUES (null,'(11) 0769-7764', 20);



<h2>Criação da tabela carro</h2>


  CREATE TABLE carro (
    id_carro  INTEGER PRIMARY KEY,
    marca VARCHAR(20),
    cor VARCHAR(20),
    ano DATE,
    modelo VARCHAR(30),
    id_cliente INT,
    FOREIGN KEY (id_cliente) REFERENCES cliente(id_cliente)
);


<h2>Inserindo informações de 20 carros</h2>


   INSERT INTO carro VALUES  (null,'Toyota', 'Preto', '2019-01-01', 'Corolla', 1);
   INSERT INTO carro VALUES  (null,'Honda', 'Prata', '2020-05-15', 'Civic', 2);
   INSERT INTO carro VALUES (null,'Volkswagen', 'Azul', '2018-10-20', 'Golf', 3);
   INSERT INTO carro VALUES (null,'Ford', 'Vermelho', '2017-07-07', 'Focus', 4);
   INSERT INTO carro VALUES  (null,'Chevrolet', 'Branco', '2021-12-30', 'Onix', 5);
   INSERT INTO carro VALUES  (null,'Hyundai', 'Cinza', '2019-03-25', 'HB20', 6);
   INSERT INTO carro VALUES (null,'Renault', 'Azul Escuro', '2016-09-12', 'Sandero', 7);
   INSERT INTO carro VALUES (null,'Fiat', 'Verde', '2020-11-05', 'Uno', 8);
   INSERT INTO carro VALUES (null,'BMW', 'Prata', '2018-04-18', '320i', 9);
   INSERT INTO carro VALUES (null,'Mercedes-Benz', 'Preto', '2017-06-22', 'CLA 250', 10);
   INSERT INTO carro VALUES (null,'Audi', 'Vermelho', '2019-08-08', 'A4', 11);
   INSERT INTO carro VALUES (null,'Kia', 'Branco', '2020-02-14', 'Sportage', 12);
   INSERT INTO carro VALUES (null,'Nissan', 'Cinza', '2016-11-30', 'Versa', 13);
   INSERT INTO carro VALUES (null,'Jeep', 'Azul Marinho', '2017-10-03', 'Renegade', 14);
   INSERT INTO carro VALUES (null,'Peugeot', 'Bordô', '2018-07-19', '208', 15);
   INSERT INTO carro VALUES (null,'Land Rover', 'Prata', '2021-04-26', 'Evoque', 16);
   INSERT INTO carro VALUES (null,'Volvo', 'Preto', '2019-09-10', 'XC40', 17);
   INSERT INTO carro VALUES (null,'Mitsubishi', 'Vermelho', '2017-12-05', 'Lancer', 18);
   INSERT INTO carro VALUES (null,'Subaru', 'Azul', '2018-06-28', 'Impreza', 19);
   INSERT INTO carro VALUES  (null,'Ferrari', 'Vermelho', '2020-03-12', '488 GTB', 20);


<h2>Criação da tabela serviço de manutenção</h2>

CREATE TABLE servico_de_manutencao (
    id_servicodemanutencao INTEGER PRIMARY KEY,
    data_de_servico DATE,
    valor_de_servico DOUBLE,
    id_manutencao INT,
    id_carro INT,
    FOREIGN KEY (id_manutencao) REFERENCES manutencao(id_manutencao),
    FOREIGN KEY (id_carro) REFERENCES carro(id_carro)
);


<h2>Inserindo informações de registros de manutenção que ocorreram</h2>



INSERT INTO servico_de_manutencao VALUES (null,'2023-01-10', 250.00, 1, 1);
INSERT INTO servico_de_manutencao VALUES (null,'2023-02-22', 180.50, 2, 2);
INSERT INTO servico_de_manutencao VALUES (null,'2023-03-15', 300.00, 3, 3);
INSERT INTO servico_de_manutencao VALUES (null,'2023-04-05', 150.75, 4, 4);
INSERT INTO servico_de_manutencao VALUES (null,'2023-05-18', 400.25, 5, 5);
INSERT INTO servico_de_manutencao VALUES (null,'2023-06-20', 275.80, 6, 6);
INSERT INTO servico_de_manutencao VALUES (null,'2023-07-03', 350.00, 7, 7);
INSERT INTO servico_de_manutencao VALUES (null,'2023-08-12', 210.30, 8, 8);
INSERT INTO servico_de_manutencao VALUES (null,'2023-09-28', 180.00, 9, 9);
INSERT INTO servico_de_manutencao VALUES(null,'2023-10-14', 420.50, 10, 10);
INSERT INTO servico_de_manutencao VALUES (null,'2023-11-30', 320.00, 11, 11);
INSERT INTO servico_de_manutencao VALUES (null,'2023-12-25', 290.75, 12, 12);
INSERT INTO servico_de_manutencao VALUES (null,'2024-01-05', 180.50, 13, 13);
INSERT INTO servico_de_manutencao VALUES (null,'2024-02-17', 390.20, 14, 14);
INSERT INTO servico_de_manutencao VALUES (null,'2024-03-08', 260.00, 15, 15);
INSERT INTO servico_de_manutencao VALUES (null,'2024-04-21', 180.90, 16, 16);
INSERT INTO servico_de_manutencao VALUES (null,'2024-05-14', 300.00, 17, 17);
INSERT INTO servico_de_manutencao VALUES (null,'2024-06-30', 350.60, 18, 18);
INSERT INTO servico_de_manutencao VALUES (null,'2024-07-18', 180.75, 19, 19);
INSERT INTO servico_de_manutencao VALUES (null,'2024-08-22', 400.25, 20, 20);

<h2>Criação da tabela equipe de manutenção</h2>

CREATE TABLE equipe_de_manutencao (
    id_manutencao INTEGER PRIMARY KEY,
    horario_de_trabalho TIME,
    lider_da_equipe VARCHAR(60)
);


<h2>Inserindo informações das equipes de manutenção</h2>


  INSERT INTO equipe_de_manutencao VALUES  (null,'08:00:00', 'João Silva');
  INSERT INTO equipe_de_manutencao VALUES (null,'09:30:00', 'Maria Oliveira');
  INSERT INTO equipe_de_manutencao VALUES (null,'10:45:00', 'Pedro Santos');
  INSERT INTO equipe_de_manutencao VALUES (null,'12:15:00', 'Ana Costa');
  INSERT INTO equipe_de_manutencao VALUES  (null,'14:00:00', 'Marcos Rodrigues');
  INSERT INTO equipe_de_manutencao VALUES  (null,'15:30:00', 'Carla Almeida');
  INSERT INTO equipe_de_manutencao VALUES  (null,'16:45:00', 'Rafaela Pereira');
  INSERT INTO equipe_de_manutencao VALUES  (null,'08:30:00', 'Fernando Gomes');
  INSERT INTO equipe_de_manutencao VALUES (null,'10:00:00', 'Aline Souza');
  INSERT INTO equipe_de_manutencao VALUES  (null,'11:20:00', 'Gabriel Ferreira');
  INSERT INTO equipe_de_manutencao VALUES  (null,'13:00:00', 'Juliana Martins');
  INSERT INTO equipe_de_manutencao VALUES  (null,'14:45:00', 'Ricardo Vieira');
  INSERT INTO equipe_de_manutencao VALUES  (null,'09:15:00', 'Luiza Carvalho');
  INSERT INTO equipe_de_manutencao VALUES  (null,'10:45:00', 'Gustavo Oliveira');
  INSERT INTO equipe_de_manutencao VALUES  (null,'12:00:00', 'Patrícia Silva');
  INSERT INTO equipe_de_manutencao VALUES   (null,'13:30:00', 'Daniel Santos');
  INSERT INTO equipe_de_manutencao VALUES   (null,'15:00:00', 'Mariana Costa');
  INSERT INTO equipe_de_manutencao VALUES   (null,'16:20:00', 'Renato Rodrigues');
  INSERT INTO equipe_de_manutencao VALUES  (null,'08:45:00', 'Lúcia Almeida');
  INSERT INTO equipe_de_manutencao VALUES  (null,'10:10:00', 'Felipe Pereira');


<h2>Criação da tabela telefone da equipe de manutenção</h2>

CREATE TABLE telefone_equipe_de_manutencao (
    id_telefoneequipedemanutencao INTEGER PRIMARY KEY,
    telefone VARCHAR(60),
    id_manutencao INT,
    FOREIGN KEY (id_manutencao) REFERENCES equipe_de_manutencao(id_manutencao)
);

<h2>Inserindo informações dos telefones das equipes de manutenção</h2>


   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(16) 6345-2357', 1);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(12) 7845-2357', 2);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(13) 3467-1235', 3);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(12) 2365-2167', 4);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(15) 2354-2354', 5);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(11) 2365-0098', 6);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(13) 2179-2178', 7);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(13) 0876-5678', 8);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(16) 8678-1235', 9);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(17) 4645-4567', 10);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(15) 8879-3412', 11);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(11) 9007-3122', 12);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(12) 1245-1231', 13);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(11) 2345-5345', 14);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(13) 4334-5555', 15);
   INSERT INTO telefone_equipe_de_manutencao VALUES (null,'(16) 7566-8787', 16);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(11) 9067-5675', 17);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(16) 3432-8656', 18);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(11) 3241-5433', 19);
   INSERT INTO telefone_equipe_de_manutencao VALUES  (null,'(66) 1235-4564', 20);


<h2>Criação da tabela Funcionário de manutenção - Equipe de manutenção</h2>

CREATE TABLE Funcionario_de_manutencao_Equipe_de_manutencao (
    id_funcionariomanutencao INT,
    id_manutencao INT,
    FOREIGN KEY (id_funcionariomanutencao) REFERENCES funcionario_manutencao(id_funcionario),
    FOREIGN KEY (id_manutencao) REFERENCES equipe_de_manutencao(id_manutencao)
);

<h2>Inserindo informações na tabela Funcionario_de_manutencao_Equipe_de_manutencao </h2>


INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(1,1);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(1,2);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(2,1);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(2,2);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(3,3);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(3,4);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(4,3);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(4,4);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(5,5);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(5,6);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(6,5);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(6,6);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(7,7);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(7,8);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(8,8);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(8,9);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(9,8);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(9,9);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(10,10);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(10,11);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(11,10);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(11,11);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(12,12);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(12,13);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(13,12); 
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(13,13);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(14,14);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(14,15);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(15,14);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(15,15);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(16,16);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(16,17);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(17,16);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(17,17);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(18,18);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(18,19);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(19,19);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(19,20);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(20,29);
INSERT INTO Funcionario_de_manutencao_Equipe_de_manutencao VALUES(20,20);


<h2>Criação da tabela Funcionário de manutenção</h2>

CREATE TABLE Funcionario_de_manutencao (
    id_funcionariomanutencao INTEGER PRIMARY KEY,
    RG INT,
    Genero VARCHAR(9),
    primeiro_nome VARCHAR(60),
    nome_do_meio VARCHAR(60),
    nome_final VARCHAR(60),
    data_de_nascimento DATE,
    idade INT
);

<h2>Inserindo informações na tabela Funcionario_de_manutencao</h2>


   INSERT INTO Funcionario_de_manutencao VALUES (null,123456, 'Masculino', 'João', 'Silva', 'Junior', '1980-05-15', 42);
   INSERT INTO Funcionario_de_manutencao VALUES (null,234567, 'Feminino', 'Maria', 'Oliveira', 'Pereira', '1985-08-20', 37);
   INSERT INTO Funcionario_de_manutencao VALUES (null,345678, 'Masculino', 'Pedro', 'Santos', 'Silveira', '1990-11-10', 32);
   INSERT INTO Funcionario_de_manutencao VALUES (null,456789, 'Feminino', 'Ana', 'Costa', 'Martins', '1988-03-25', 34);
   INSERT INTO Funcionario_de_manutencao VALUES (null,567890, 'Masculino', 'Marcos', 'Rodrigues', 'Almeida', '1992-07-07', 29);
   INSERT INTO Funcionario_de_manutencao VALUES (null,678901, 'Feminino', 'Carla', 'Almeida', 'Pereira', '1987-09-12', 35);
   INSERT INTO Funcionario_de_manutencao VALUES (null,789012, 'Masculino', 'Rafael', 'Pereira', 'Gomes', '1995-01-30', 27);
   INSERT INTO Funcionario_de_manutencao VALUES (null,890123, 'Feminino', 'Fernanda', 'Gomes', 'Souza', '1993-04-18', 29);
   INSERT INTO Funcionario_de_manutencao VALUES (null,901234, 'Masculino', 'Lucas', 'Silva', 'Ferreira', '1991-12-05', 30);
   INSERT INTO Funcionario_de_manutencao VALUES (null,123401, 'Feminino', 'Aline', 'Souza', 'Rocha', '1989-06-22', 33);
   INSERT INTO Funcionario_de_manutencao VALUES (null,234012, 'Masculino', 'Gabriel', 'Ferreira', 'Machado', '1986-10-09', 36);
   INSERT INTO Funcionario_de_manutencao VALUES (null,340123, 'Feminino', 'Juliana', 'Martins', 'Santos', '1994-02-14', 28);
   INSERT INTO Funcionario_de_manutencao VALUES (null,401234, 'Masculino', 'Mateus', 'Almeida', 'Oliveira', '1984-11-30', 37);
   INSERT INTO Funcionario_de_manutencao VALUES (null,512345, 'Feminino', 'Rafaela', 'Oliveira', 'Rodrigues', '1990-09-08', 31);
   INSERT INTO Funcionario_de_manutencao VALUES (null,612340, 'Masculino', 'Diego', 'Rodrigues', 'Costa', '1997-07-03', 24);
   INSERT INTO Funcionario_de_manutencao VALUES (null,723401, 'Feminino', 'Luana', 'Costa', 'Santos', '1987-04-20', 34);
   INSERT INTO Funcionario_de_manutencao VALUES  (null,834012, 'Masculino', 'Miguel', 'Santos', 'Gonçalves', '1993-03-17', 28);
   INSERT INTO Funcionario_de_manutencao VALUES (null,945678, 'Feminino', 'Larissa', 'Gonçalves', 'Alves', '1995-12-12', 26);
   INSERT INTO Funcionario_de_manutencao VALUES  (null,156789, 'Masculino', 'Bruno', 'Alves', 'Ribeiro', '1988-08-28', 33);
   INSERT INTO Funcionario_de_manutencao VALUES (null,267890, 'Feminino', 'Isabela', 'Ribeiro', 'Mendes', '1991-05-01', 30);


<h2>Criação da tabela Telefone do funcionário de manutenção</h2>

CREATE TABLE Telefone_funcionario_manutencao (
    ID_Telefonefuncionariomanutencao INTEGER PRIMARY KEY,
    Telefone VARCHAR(60),
    ID_Funcionariomanutencao INT,
    FOREIGN KEY (ID_Funcionariomanutencao) REFERENCES Funcionario_de_manutencao(id_funcionariomanutencao)
);

<h2>Inserindo informações na tabela Telefone do funcionário de manutenção</h2>



 INSERT INTO Telefone_funcionario_manutencao VALUES  (null,'(11) 7534-1237', 1);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(24) 3456-1674', 2);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(16) 5667-2345', 3);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(13) 3456-6789', 4);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(13) 2367-5679', 5);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(12) 6789-0098', 6);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(16) 5675-6783', 7);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(11) 7545-6455', 8);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(12) 6474-6465', 9);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(13) 6745-6789', 10);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(24) 4567-1234', 11);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(12) 4567-3456', 12);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(16) 4567-1235', 13);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(24) 4745-2346', 14);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(11) 4574-1234', 15);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(13) 3453-1234', 16);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(16) 3456-12356', 17);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(12) 3456-4567', 18);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(24) 2134-6789', 19);
 INSERT INTO Telefone_funcionario_manutencao VALUES (null,'(11) 1200-4567', 20);

<h2>Criação da tabela email do funcionário da manutenção</h2>

CREATE TABLE Email_funcionario_manutencao (
    ID_Emailfuncionariomanutencao INTEGER PRIMARY KEY,
    Email VARCHAR(60),
    ID_Funcionariomanutencao INT,
    FOREIGN KEY (ID_Funcionariomanutencao) REFERENCES Funcionario_de_manutencao(id_funcionariomanutencao)
);

<h2>Inserindo informações na tabela email do funcionário da manutenção</h2>



 INSERT INTO Email_funcionario_manutencao VALUES(null,'joaosilvajunior@gmail.com', 1);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'mariaoliveirapereira@gmail.com',2);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'pedrosantossilveira@gmail.com',3);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'pedrosantos@gmail.com',3);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'anacostamartins@gmail.com',4);
 INSERT INTO Email_funcionario_manutencao VALUES(null,'marcosrodriguesalmeida@gmail.com',5);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'carlaalmeidapereira@gmail.com',6);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'carlaalmeida@gmail.com',6);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'rafaelpereiragomes@gmail.com',7);
 INSERT INTO Email_funcionario_manutencao VALUES(null,'fernandagomessouza@gmail.com',8);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'lucassilvaferreira@gmail.com',9);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'alinesouzarocha@gmail.com',10);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'alinesouza@gmail.com',10);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'gabrielferreiramachado@gmail.com',11);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'gabrielferreira@gmail.com',11);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'julianamartinssantos@gmail.com',12);
 INSERT INTO Email_funcionario_manutencao VALUES(null,'mateusalmeidaoliveira@gmail.com',13);
 INSERT INTO Email_funcionario_manutencao VALUES(null,'rafaelaoliveirarodrigues@gmail.com',14);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'diegorodriguescosta@gmail.com',15);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'luanacostasantos@gmail.com',16);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'miguelsantosgoncalves@gmail.com',17);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'larissagoncalvesalves@gmail.com',18);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'larissagancalves@gmail.com',18);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'brunoalvesribeiro@gmail.com',19);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'isabelaribeiromendes@gmail.com',20);
 INSERT INTO Email_funcionario_manutencao VALUES (null,'isabelaribeiro@gmail.com',20);









<h1>CRUD </h1>

<h2>Prints da inserção de alguns dados</h2>

![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/6dcfb599-be7e-4595-80c2-d7764007fd3c)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/1d760036-6ca9-436a-aefd-3648097e4400)


<h2>Prints da leitura desses dados</h2>

![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/cb37b61c-e7b2-4449-8572-c33f94541b12)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/106e61c8-3a74-410d-894e-4ab179cfa9cc)

<h2>Prints da Deleção de alguns desses dados</h2>

![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/db07bd5f-6d3c-41c7-8ad8-7dc4d7f6bce0)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/14f4e25c-cecf-4ce5-ae1c-9437dd3e8c8b)

<h2>Prints das alterações de alguns desses dados</h2>

![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/77023d31-d8fb-4d43-93aa-139a20aeb6a8)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/e72d20fd-94ce-4262-bb4f-97e8e4c8bb67)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/07f12ffa-de80-4585-8896-45d3e928fbe5)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/b6ba9547-bdf1-4d4f-a1e4-4a3a83d6b1b6)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/7936f833-eae3-4650-be11-d7bc0779079a)


<h1>Relatórios</h1>

<h2>Prints de alguns dos relatórios</h2>

![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/f48cac0d-6c8f-4402-a152-afbe9dfcba17)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/fd8a1c04-4131-4f84-95b4-b20c1717532d)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/2b3c1eb3-5d65-4112-8cc0-ce79189c1116)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/49af9b1f-c486-4557-88b0-ac802fb5da70)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/b64f3e5b-7fc7-4269-a7ab-d62890e8e6a8)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/826929ca-0e39-49ba-9807-0b16ffefe122)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/1f1ee063-0a54-4ff0-acc5-c226f21b94bf)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/e95ad1f3-3bcb-47de-b17b-5dcb8045b20f)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/06944941-38bd-4c66-add9-e65a92559f5d)
![image](https://github.com/LeandroBorgesdaSilva/Modelagem-de-Banco-de-Dados---1-Semestre/assets/104734317/feeafd62-9c29-4fd5-84e5-70c42a461aa9)











