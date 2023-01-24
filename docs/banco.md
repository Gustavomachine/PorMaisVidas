# 1 :

create table denunciante(
cpf int PRIMARY key, 
nome varchar(255) not null, 
data_de_nascimento date not null, 
sexo varchar(255), 
email varchar(255) not null, 
<<<<<<< HEAD
telefone int UNIQUE
=======
telefone int UNIQUE,
>>>>>>> 356e3b515b20d8b4ed585420af255594fed7ab07
);

create table contato_emergencial(
nome_CE varchar(255)not null,
cpf int,
telefone int UNIQUE, 
PRIMARY key (cpf,telefone),
foreign key(cpf) REFERENCES denunciante(cpf)
<<<<<<< HEAD
on update cascade on delete cascade
=======
on update cascade on delete cascade, 
>>>>>>> 356e3b515b20d8b4ed585420af255594fed7ab07
);

create table endereco(
cpf int primary key,
rua varchar(255), 
numero int(10), 
bairro varchar(255), 
cep int(8),
foreign key(cpf) REFERENCES denunciante(cpf)
on update cascade on delete cascade
);

create table denuncia(
protocolo int(10) PRIMARY KEY,
corpo varchar(255),
data date,
hora time,  
<<<<<<< HEAD
cpf int ,
=======
cpf int primary key,
id_analise int(10) AUTO_INCREMENT,
>>>>>>> 356e3b515b20d8b4ed585420af255594fed7ab07
foreign key(cpf) REFERENCES denunciante(cpf)
on update cascade on delete cascade
);

create table agente_publico(
cpf int PRIMARY key,
nome varchar(255),
cargo varchar(255),
email varchar(255),
telefone int UNIQUE
);

create table analise(
despacho varchar(255),
data date,
<<<<<<< HEAD
cpf int PRIMARY KEY,
protocolo int(10), 
foreign key(cpf) REFERENCES agente_publico(cpf)
on update cascade on delete cascade,
FOREIGN key(protocolo) REFERENCES denuncia(protocolo)
on update cascade on delete cascade
=======
cpf int,
id_analise int(10),
primary key, (cpf, id_analise),
foreign key(id_analise) REFERENCES denuncia(id_analise)
on update cascade on delete cascade,
foreign key(cpf) REFERENCES agente_publico(cpf)
on update cascade on delete cascade  
>>>>>>> 356e3b515b20d8b4ed585420af255594fed7ab07
);


create table endereco_agente_publico(
cpf int primary key,
rua varchar(255), 
numero int(10), 
bairro varchar(255), 
<<<<<<< HEAD
cep int(8),
=======
cep int(8)
>>>>>>> 356e3b515b20d8b4ed585420af255594fed7ab07
FOREIGN KEY(cpf) REFERENCES agente_publico(cpf)
on update cascade on delete cascade
);
