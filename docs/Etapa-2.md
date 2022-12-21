########################################################## Análise de Projeto #######################################################

### Criação das tabelas no Banco de Dados pelo Mysql:

Criaçao das tabelas com base na modelagem do banco de Dados.

1. Tabela Denunciante (contendo: Cpf como chave primaria, Nome, data de nascimento, sexo, email, endereço, telefone e contato emergencial).

2. Tabela Denuncia (contendo: Protocolo como chave primaria, corpo, data e hora).

3. Tabela Agente_Publico (contendo: Cpf como chave primaria, nome, cargo, email, endereço, telefone).

4. Tabela Analise (contendo: id_Protocolo como chave estrangueira referenciando a tabela denuncia, despacho, data).

5. Tabela Endereço (contendo: Cpf_Denunciante como chave  estrangueira onde referencia a tabela denunciante, rua, numero, bairro e cep).

6. Tabela Contato Emergencial (contenco:Cpf_Denunciante como chave  estrangueira onde referencia a tabela denunciante e contato).

7. Tabela Endereço agente_publico (contenco: Cpf_agente_publico como chave estrangueira onde referencia a tabela agente publico, rua, numero, bairro e cep).



