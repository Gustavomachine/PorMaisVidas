# 1 :
create table contato_emergencial(
nome_CE varchar(255)not null,
cpf int,
telefone int UNIQUE, 
PRIMARY key (cpf,telefone)
);

create table endereco(
cpf int primary key,
rua varchar(255), 
numero int(10), 
bairro varchar(255), 
cep int(8)
);

create table analise(
despacho varchar(255),
data date,
cpf int,
id_analise int(10)AUTO_INCREMENT PRIMARY KEY
   
);
create table denuncia(
protocolo int(10) AUTO_INCREMENT PRIMARY KEY,
corpo varchar(255),
data date,
hora time,
cpf int,
id_analise int UNIQUE,
foreign key(id_analise) REFERENCES analise(id_analise)
on update cascade on delete cascade

);

create table denunciante(
cpf int PRIMARY key, 
nome varchar(255) not null, 
data_de_nascimento date not null, 
sexo varchar(255), 
email varchar(255) not null, 
telefone int UNIQUE,
foreign key(cpf) REFERENCES contato_emergencial(cpf)
on update cascade on delete cascade,  
foreign key(cpf) REFERENCES endereco(cpf)
on update cascade on delete cascade
);

create table endereco_agente_publico(
cpf int primary key,
rua varchar(255), 
numero int(10), 
bairro varchar(255), 
cep int(8)
);

create table agente_publico(
cpf int PRIMARY key,
nome varchar(255),
cargo varchar(255),
email varchar(255),
telefone int UNIQUE,
FOREIGN KEY(cpf) REFERENCES endereco_agente_publico(cpf)
on update cascade on delete cascade
);

