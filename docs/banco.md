# 1 :

create table denunciante(
cpf int PRIMARY key,
nome varchar(255) not null,
data_de_nascimento varchar(255) not null,
sexo varchar(255),
email varchar(255) not null,
telefone int UNIQUE,
senha varchar(255) UNIQUE
);

create table endereco(
cpf int primary key,
rua varchar(255),
numero varchar(255),
bairro varchar(255),
cep int(8),
estado varchar(255),
cidade varchar(255),
foreign key(cpf) REFERENCES denunciante(cpf)
on update cascade on delete cascade
);

create table denuncia(
protocolo int PRIMARY KEY AUTO_INCREMENT,
denuncia varchar(255),
cpf int ,
foreign key(cpf) REFERENCES denunciante(cpf)
on update cascade on delete cascade
);

create table agente_publico(
cpf int PRIMARY key,
nome varchar(255),
cargo varchar(255),
email varchar(255),
telefone int UNIQUE,
senha varchar(255) UNIQUE
);

create table analise(
despacho varchar(255),
data varchar(255),
cpf int PRIMARY KEY,
protocolo int(10),
foreign key(cpf) REFERENCES agente_publico(cpf)
on update cascade on delete cascade,
FOREIGN key(protocolo) REFERENCES denuncia(protocolo)
on update cascade on delete cascade
);

create table endereco_agente_publico(
cpf int primary key,
rua varchar(255),
numero varchar(255),
bairro varchar(255),
cep int(8),
estado varchar(255),
cidade varchar(255),
FOREIGN KEY(cpf) REFERENCES agente_publico(cpf)
on update cascade on delete cascade
);
