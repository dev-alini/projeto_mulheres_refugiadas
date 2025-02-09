# Projeto Social da RecodePro AI 2025
![Static Badge](https://img.shields.io/badge/squad65-red)
![Static Badge](https://img.shields.io/badge/RecodePro2024%2F25-blue)
![Static Badge](https://img.shields.io/badge/mulheres_refugiadas-green)

### squad 065 - integrantes:
- Adenice Lima de Brito Leitao
- Ailton Lucas de Oliveira Silva
- Aline de Jesus Santos(líder)
- Ellen Cristine Maciel da Silva(vice-líder)

### Desafio Escolhido
O desafio escolhido foi criar uma plataforma digital acessível e inclusiva para oferecer qualificação
profissional a mulheres refugiadas venezuelanas no Brasil. A ideia é fornecer cursos gratuitos em
diversas áreas para facilitar a entrada dessas mulheres no mercado de trabalho.

### Problema Identificado
O problema identificado foi a falta de oportunidades e barreiras de acesso ao emprego para mulheres refugiadas, que enfrentam dificuldades como:

* Barreira do idioma (muitas não dominam o português);
* Falta de qualificação profissional (não conseguem validar diplomas ou não possuem experiência formal);
* Desafios econômicos e sociais (dificuldade em acessar cursos pagos ou obter suporte para se reinserir no mercado de trabalho);
* Discriminação no mercado de trabalho (pelo fato de serem refugiadas e mulheres).

A plataforma busca resolver esse problema através de cursos profissionalizantes acessíveis, facilitando o desenvolvimento de
novas habilidades para que essas mulheres possam conquistar independência financeira.

### Público-Alvo
O público-alvo principal são mulheres refugiadas venezuelanas no Brasil, que buscam capacitação para se inserir no mercado de trabalho.
O projeto também pode beneficiar:

Mulheres imigrantes de outros países que enfrentam desafios semelhantes;
Organizações sociais e ONGs que atuam na integração de refugiados;
Empresas interessadas em contratar mão de obra qualificada e apoiar a inclusão social.

## Questionário do Projeto Social:
1. **Considerando o desafio escolhido, qual é o problema a ser resolvido e que será
contemplado com o projeto final?**
<br>R: A dificuldade de integração social e econômica das mulheres refugiadas venezuelanas no
Brasil, incluindo acesso ao trabalho, moradia e proteção contra a violência de gênero.

2. **Qual o público-alvo? A solução poderá ser aplicada a todos, sem restrição de idade
ou grau de escolaridade, por exemplo?**
<br>R: A todas as mulheres venezuelanas, com idades entre 18 a 50 anos.

3. **O problema foi escolhido com base em quais dados oficiais? Como vocês
identificaram que esse realmente é um problema para o público-alvo? Indique as
referências usadas, justificando a sua escolha.**
<br>R: ONU Mulheres e do Comitê Nacional para Refugiados (CONARE), que apontam
desafios específicos enfrentados por mulheres refugiadas. Esses relatórios mostram que
mulheres migrantes e refugiadas enfrentam maior vulnerabilidade no mercado de
trabalho, dificuldades no acesso a serviços básicos e riscos aumentados de exploração e
violência de gênero. Além disso, dados do IBGE e do Ministério da Justiça reforçam o
aumento da imigração venezuelana e os desafios da integração no Brasil.

4. **Como esse problema afeta o público-alvo?**
<br>R: O problema afeta essas mulheres ao limitar suas oportunidades de autonomia
financeira, aumentar sua exposição à exploração e dificultar sua adaptação ao Brasil.

5. **Qual o cronograma das atividades?**
   
   ![image](https://github.com/user-attachments/assets/a164cc82-9bb5-4289-82f0-0e4b22f69c67)

   
6. **Como será feita a distribuição das atividades entre os integrantes do squad para essa
primeira entrega?**

![image](https://github.com/user-attachments/assets/64181473-884f-4f4a-9eec-aad220247204)


7. **Qual a ferramenta de gerenciamento de projeto será usada para o monitoramento
das atividades? Ex: Trello, Asana, Jira, Monday.**
<br>R: Jira

### Modelagem de dados
* Conceitual:

  ![image](https://github.com/user-attachments/assets/7a4de673-9c2a-418c-b811-e64aea682baa)

* Lógico:

    ![image](https://github.com/user-attachments/assets/57fca771-4027-4e4d-a396-69c12fb40a0f)

  *  Script SQL:
 
    CREATE TABLE Usuária 
( 
 Usuaria_ID INT PRIMARY KEY AUTO_INCREMENT,  
 Nome VARCHAR(n) NOT NULL,  
 Email VARCHAR(n) NOT NULL,  
 Senha VARCHAR(n) NOT NULL,  
 Pais_Origem VARCHAR(n) NOT NULL,  
 Data_Nascimento DATE NOT NULL,  
 UNIQUE (Email)
); 

CREATE TABLE Categoria 
( 
 Categoria_ID INT PRIMARY KEY,  
 Nome VARCHAR(n) NOT NULL,  
); 

CREATE TABLE Instrutor 
( 
 Instrutor_ID INT PRIMARY KEY AUTO_INCREMENT,  
 Nome VARCHAR(n) NOT NULL,  
 Especializacao VARCHAR(n),  
); 

CREATE TABLE Curso 
( 
 Curso_ID INT PRIMARY KEY,  
 Nome VARCHAR(n) NOT NULL,  
 Descricao VARCHAR(n),  
 Duracao INT NOT NULL,  
 Categoria_ID INT,  
 Instrutor_ID INT,  
); 

CREATE TABLE Inscricao 
( 
 Inscricao_ID INT PRIMARY KEY AUTO_INCREMENT,  
 Usuaria_ID INT,  
 Curso_ID INT,  
 Data_Inscricao DATE NOT NULL,  
 Status CHAR(n) NOT NULL,  
); 

CREATE TABLE Certificado 
( 
 Certificado_ID INT PRIMARY KEY AUTO_INCREMENT,  
 Inscricao_ID INT,  
 Data_Conclusao DATE NOT NULL,  
 Codigo_Verificacao VARCHAR(n) NOT NULL,  
 UNIQUE (Codigo_Verificacao)
); 

### Link funcional para acessar o site:

https://projeto-mulheres-refugiadas.vercel.app/




