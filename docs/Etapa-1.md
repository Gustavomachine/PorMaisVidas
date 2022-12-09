# Especificações sobre o projeto de auxilio a mulher

## 1. OBJETIVO PRINCIPAL

O sistema tem como proposta uma solução viavel para vitimas de violência que por medo de seus agressores (medo de se exporem), assim a essência do trabalho é proporcionar uma maneira simples, rapida e eficaz das vitimas denunciarem.

## 2. Requisitos funcionais
1.Registrar o usuario. 
Essencial
O sistema deve conter um metodo de cadastrar as informções do denunciante.

2. Registrar o agente publico.

o sistema devera conter um metodo de cadastrar as informações do agente publico.

3. Visualizar denuncia
Essencial
O site deverá conter uma pagina onde será possível visualizar a denuncia.

4. Registrar a denuncia da vitima
Essencial
O site deve ter um campo para que a vitima informe o ocorrido.

5. Fazer alterações cadastrais do denunciante
Essencial
O sistema devera conter uma funcionalidade de alteração cadastral caso ocorra alguma alterção dos dados.

6. Bloquear o sistema até todo o formulario esteja completo
Desejável
O sistema não avançará para a denuncia os outros dados até que a vitima informe todos os dados necessários.

7.Página de login.
o sistema deverá conter a funcionalidade de login, logo identificando se será agente publico ou denunciante.

### Usuario final:
Agente Publico;
resposavel por manusear as denuncias e gerir o atendimento, 
logo tem direito a visualizar as informações como (tipo de violencia, 
local, Gravidade da agressão, data do ocorrido, )
Denunciante;
O usuario principal vai abordar sua situação no site onde ocorre todo o processo da denuncia, especificando todo o ocorrido como (tipo de violencia, 
local, Gravidade da agressão, data do ocorrido, )
2- A pagina inicial:
deverá conter o login do usuario e o login do admin, logo com o cadastro das devidas pessoas e usuarios.
3- Na página da denuncia:
conterá, identificação da denuncia, a denuncia, parecer, data e hora.

## 3. Requisitos não funcionais

###Segurança

acessos não autorizados ao sistema não serão permitidos . Portanto, é assegurada a integridade do sistema quanto a ataques intencionais ou acidentes.

###Confiabilidade

Garantir maior probabilidade de uma operação livre de falhas no maior tempo possivel.

###Usabilidade

Facilitar a utilização dos usuários ao lidarem com a ferramenta

###Requisitos de Compatibilidade

Aqui são especificadas quais as compatibilidades necessárias para a execução do sistema. Logo, podem fazer parte dessa solicitação a compatibilidade com navegadores, em quais versões do sistema operacional o sistema é capaz de rodar etc.

###Legalidade

Nos requisitos legais correspondem às necessidades de implementação de padrões exigidos por lei, como normas específicas, adoção de processos para garantir a segurança da informação (como os exigidos pela LGPD — Lei Geral de Proteção de Dados), entre outros.

###Requisitos éticos

Garantem à pessoa utilizadora do sistema que seus dados não serão compartilhados para outras pessoas e que informações sensível, não serão visíveis a olho nu. 


## 4. Criação das tabelas no Banco de Dados pelo Mysql.

Criaçao das tabelas com base na modelagem do banco de Dados.

1. Tabela Denunciante (contendo: Cpf como chave primaria, Nome, data de nascimento, sexo, email, endereço, telefone e contato emergencial).

2. Tabela Denuncia (contendo: Protocolo como chave primaria, corpo, data e hora).

3. Tabela Agente_Publico (contendo: Cpf como chave primaria, nome, cargo, email, endereço, telefone).

4. Tabela Analise (contendo: id_Protocolo como chave estrangueira referenciando a tabela denuncia, despacho, data).

5. Tabela Endereço (contendo: Cpf_Denunciante como chave  estrangueira onde referencia a tabela denunciante, rua, numero, bairro e cep).

6. Tabela Contato Emergencial (contenco:Cpf_Denunciante como chave  estrangueira onde referencia a tabela denunciante e contato).

7. Tabela Endereço agente_publico (contenco: Cpf_agente_publico como chave estrangueira onde referencia a tabela agente publico, rua, numero, bairro e cep).
