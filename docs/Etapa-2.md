########################################################## Análise de Projeto #######################################################

![Criação da modelagem de banco de dados](..\images\ModelagemdeBancodeDados.png)

<<<<<<< HEAD
![Criação do Diagrama de Casos de uso; login e registro](..\images\Diagrama_de_Casos_de_uso;login_e_registro.jpg)

![Criação do Diagrama de Casos de uso; telas principais](..\images\Diagrama_de_Casos_de_uso;telas_principais.jpg)
=======
>>>>>>> 56fd0f1a38c13bb0b539c23f84b34981d5ca168d

### Criação das tabelas no Banco de Dados pelo Mysql

Criaçao das tabelas com base na modelagem do banco de Dados.

1. Tabela Denunciante (contendo: Cpf como chave primaria (PK) e (FK) como chave estrangueira referenciando as tabelas id_endereco e denuncia, Nome, data de nascimento, sexo, email, endereço, telefone e contato emergencial).

2. Tabela Denuncia (contendo: Protocolo como chave primaria (PK) e  cpf (FK) como chave estrangueira referenciando a tabela denuncia, corpo, data e hora).

3. Tabela Agente_Publico (contendo: Cpf como chave primaria, nome, cargo, email, id_endereço_agente, telefone).

4. Tabela Analise (contendo: protocolo como chave primaria (PK) e (FK) como chave estrangueira referenciando a tabela denuncia, e cpf (FK) como chave estrangueira referenciando a tabela agente_publico, despacho, data).

5. Tabela Endereço (contendo: id_endereco como chave estrangueira onde referencia a tabela denunciante, rua, numero, bairro e cep).

6. Tabela Contato Emergencial (contendo : nome e telefone como chave composta)

7. Tabela Endereço_agente_publico (contenco: id_endereco_agente como chave primaria(PK ) e (FK) como chave estrangueira onde referencia a tabela agente_publico, rua, numero, bairro e cep).






