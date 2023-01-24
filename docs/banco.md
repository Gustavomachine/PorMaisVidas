# 1 :
create table contato_emergencial(
    nome varchar(255)not null,
    telefone int UNIQUE, 
    PRIMARY key (nome,telefone)
);

create table endereco(
    id_endereco int(10) AUTO_INCREMENT PRIMARY KEY, 
    rua varchar(255), 
    numero int(10), 
    bairro varchar(255), 
    cep int(8)
);

create table analise(
    despacho varchar(255),
    data date,
    cpf int,
    id_analise int(10) AUTO_INCREMENT PRIMARY KEY
    
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
    id_endereco int UNIQUE,
    protocolo_denuncia int UNIQUE,
    foreign key(nome) REFERENCES contato_emergencial(nome)
    on update cascade on delete cascade,  
    foreign key(id_endereco) REFERENCES endereco(id_endereco)
    on update cascade on delete cascade,
    foreign key(protocolo_denuncia) REFERENCES denuncia(protocolo)
    on update cascade on delete cascade
);

create table endereco_agente_publico(
    id_endereco_agente int(10) AUTO_INCREMENT PRIMARY KEY,
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
    id_endereco_agente int(255),
    telefone int UNIQUE,
    FOREIGN KEY(id_endereco_agente) REFERENCES endereco_agente_publico(id_endereco_agente)
    on update cascade on delete cascade
);

# 2 :
create table contato_emergencial( 
    nome varchar(255)not null, 
    telefone int UNIQUE,  
    PRIMARY key (nome,telefone) 
foreign key(nome) REFERENCES denunciante(nome), 
on update cascade on delete cascade 
 
); 
 
create table endereco( 
    id_endereco int(10) AUTO_INCREMENT PRIMARY KEY,  
    rua varchar(255),  
    numero int(10),  
    bairro varchar(255),  
    cep int(8) 
foreign key( id_endereco) REFERENCES denunciante(id_endereco) 
    on update cascade on delete cascade, 
 
); 
 
create table analise( 
    despacho varchar(255), 
    data date, 
    cpf int, 
    id_analise int(10) AUTO_INCREMENT PRIMARY KEY 
    foreing Key (id_analise) references análise (id_analise) 
    on update cascade on delete cascade 
     
); 
create table denuncia( 
    protocolo int(10) AUTO_INCREMENT PRIMARY KEY, 
    corpo varchar(255), 
    data date, 
    hora time, 
    cpf int, 
    id_analise int UNIQUE, 
foreign key(protocolo_denuncia) REFERENCES denuncia(protocolo) 
    on update cascade on delete cascade 

); 
 
create table denunciante( 
    cpf int PRIMARY key,  
    nome varchar(255) not null,  
    data_de_nascimento date not null,  
    sexo varchar(255),  
    email varchar(255) not null,  
    telefone int UNIQUE,  
    id_endereco int UNIQUE, 
    protocolo_denuncia int UNIQUE, 
     
); 
 
create table endereco_agente_publico( 
    id_endereco_agente int(10) AUTO_INCREMENT PRIMARY KEY, 
    rua varchar(255),  
    numero int(10),  
    bairro varchar(255),  
    cep int(8) 
    foreing Key(id_endereco_agente)references agente publico(id_endereco_agente) 
); 
 
create table agente_publico( 
    cpf int PRIMARY key, 
    nome varchar(255), 
    cargo varchar(255), 
    email varchar(255), 
    id_endereco_agente int(255), 
    telefone int UNIQUE, 
 
    on update cascade on delete cascade 
);

