# Documento de Arquitetura 

## 1 - Introdução 

### 1.1 - Finalidade 

Este documento tem como finalidade fornecer uma visão geral da arquitetura que será utilizada no desenvolvimento do projeto Seleção CTEDS, como parte do curso de Metodologias Ágeis.

### 1.2 - Escopo

O Seleção CTEDS é uma plataforma para o auxilío de seleção de candidatos à novas turmas do curso Capacitação Tecnológica em Engenharia e Desenvolvimento de Software, além de reunir ferramentas de apoio ao ensino (chats de texto e videoconferência) em um único lugar.

O projeto contará com ferramenta open source integrada para realização das aulas ao vivo por videoconferência em substituição ao Zoom, ferramenta para aplicação de testes de código e provas de seleção com correção automática e ferramenta de chat de texto para comunicação dos alunos e professores, em substituição ao Discord.



### 1.3 - Definições, acrônimos e abreviações

Sigle/Termo/Acrônimo | Definição
-------------------- | ----------
API                  | Application Programming Interface
IAAS                 | Infrastructure as a Service
MVC                  | Model View Controlle
ORM                  | Object-Realational Mapping
SPA                  | Single Page Application
VM                   | Virtual Machine

## 2 - Representação Arquitetural

O projeto utilizará a arquitetura MVC (Model, View e Controller) para o desenvolvimento da aplicação base (frontend e backend). Serão utilizados ainda, soluções de terceiros, preferencialmente Open Source para a comunicação dos usuários e aplicação de testes/provas.


### 2.1 - .NET  
O .NET é uma plataforma de desenvolvedor gratuita, multiplataforma de código aberto para criação de aplicativos web, mobile, desktop, games, ioT, cloud e microserviços. O .NET é criado em um runtime de alto desempenho que é usado em produção por muitas aplicações de alta escala.

### 2.2 React

React é uma biblioteca Javascript open source para criar interfaces de usuário. 

### 2.3 Bootstrap

Bootstrap é um conjunto de ferramentas e componentes frontend, que facilicitam a padronização e estilização de interfaces de usuário.

## 2.4 PostgreSQL

O PostgreSQL é um poderoso sistema de banco de dados relacional de código aberto com mais de 30 anos de desenvolvimento ativo, confiável, de alto desempenho e vários recursos.

## 2.5 Revolt
O Revolt é uma alternativa Open Source ao Discord, utilizado para criação de canais de audio e texto.

## 2.6 OpenRank
O OpenRank é uma plataforma de code challenge Open Source para a criação de desafios de código e provas. 

## 2.7 Jitsi
Jitsi é uma plataforma Open Source para videoconferência com criptografia de ponta a ponta e com possibilidade de criar instância própria em máquina virtual.

## 3 - Requisitos e Restrições Arquiteturais

### 3.1 Ferramentas de desenvolvimento

O projeto será desenvolvido utilizando a IDE Visual Studio 2022 versão Community para a criação do backend e Visual Studio Code para implementação do frontend.

### 3.2 Infraestrutura

#### 3.2.1 Infraestrutura para a aplicação Seleção CTEDS

Iaas na AZURE com as seguintes configurações:

* Máquina virtual com 2 vcores
* 8 GB de memória ram
* Sistema operacional Debian 11
* Nginx para servidor web
* Banco de dados PostgreSQL

#### 3.2.2 Infraestrutura para os serviços de audio, vídeo e code challenge

Iaas na AZURE com as seguintes configurações:

* Máquina virtual com 4 vcores
* 16 GB de memória ram
* Sistema operacional Debian 11
* 1 TB de armazenamento

### 3.3 Restrições

A aplicação apesar de ser responsiva devido ao uso da biblioteca Bootstrap, poderá apresentar limitações de uso em dispositivos móveis como tablets e smartphones pois será priorizado o uso de teclado e mouse nas provas práticas.

## 4 - Visão de Casos de Uso

 ### 4.1 Casos de uso:

* Registrar interesse (oferta do curso)
* Aviso/notificação abertura de oferecimento do curso 
* Preencher formulário com os dados do usuário
* Triagem dos candidatos
* Puxar dados do candidato API Linkedin
* Enviar email com resposta da triagem
* Formulário para receber documentação (aprovados)
* Página com IDE para aplicação da prova
* Enviar por email resultado
* Acessar página com conteúdo do curso
* Hub com links para acessar as plataformas de chat e vídeo
* Acessar Revolt para chats de texto 
* Acessar Jitsi para aulas ao vivo

### 4.2 Diagrama casos de uso

![Diagrama Casos de Uso](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/fluxograma.png)
    

## 5 - Visão Lógica

A aplicação consiste em um frontend SPA rodando React e Bootstrap como interface do usuário e uma API construída com ASP.Net e ORM Entity Framework para mapeamento das tabelas do banco de dados PostgreSQL.

### 5.1 Visão Geral
![Visão Geral](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/visao-geral.jpg)

O Usuário interage com a aplicação em uma página Web responsiva e apesar de ser possível o uso em dispositivos móveis como smartphones e tablets, será recomendado o uso em notebooks e desktops, pois o uso de teclado e mouse se tornam necessários para a realização dos testes práticos dos candidatos.

As requisições e respostas realizadas pelo frontend, são feitas através do protocolo HTTP para uma API Restful implementando todos os verbos do protocolo de forma correta.
No backend, uma aplicação escrita em C# utilizando o framework .NET com ASP.NET e para facilitar a escrita das querys, é feito o uso do ORM Entity Framework 6.0.
O banco de dados utilizado será o PostgreSQL por ser open source e ter uma licença mais abrangente.



## Referências

Bootstrap - Disponível em https://getbootstrap.com/ - Acessado em 09/08/2022

Jitsi - Disponível em https://jitsi.github.io/ - Acessado em 12/08/2022

NET | Free. Cross-platform. Open Source - Disponível em https://dotnet.microsoft.com/en-us/ - Acessado em 07/08/2022

OpenRank - Disponível em https://github.com/MrPeker/OpenRank - Acessado em 12/08/2022

PostgreSQL - Disponível em https://www.postgresql.org/ - Acessado em 09/08/2022

React - Disponível em https://pt-br.reactjs.org/ - Acessado em 08/08/2022

Revolt - Disponível em https://github.com/revoltchat - Acessado em 12/08/2022


