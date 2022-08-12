# Documento de Arquitetura 

## 1 - Introdução 

### 1.1 - Finalidade 

Este documento tem como finalidade fornecer uma visão geral da arquitetura que será utilizada no desenvolvimento do projeto Seleção CTEDS como parte do curso de Metodologias Ágeis.

### 1.2 - Escopo

O Seleção CTEDS é uma plataforma para o auxilío de seleção de candidatos à novas turmas do curso Capacitação Tecnológica em Engenharia e Desenvolvimento. 

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

Será utilizado neste projeto o padrão de arquitetura MVC (Model, View and Controller). A camada Model fica responsável por gerenciar, controlar os dados e regras de négocio da aplicação. Esta, está ligada diretamente ao banco de dados.
A camada View é responsável pela apresentação das informações aos usuários, o frontend da aplicação. Já a camada de Controller é responsável pela intermediação das requisições vindas da View para o Model.

### 2.1 - .NET  
O .NET é uma plataforma de desenvolvedor gratuita, multiplataforma de código aberto para criação de aplicativos web, mobile, desktop, games, ioT, cloud e microserviços. O .NET é criado em um runtime de alto desempenho que é usado em produção por muitas aplicações de alta escala.

### 2.2 React

React é uma biblioteca Javascript open source para criar interfaces de usuário. 

### 2.3 Bootstrap

Bootstrap é um conjunto de ferramentas e componentes frontend, que facilicitam a padronização e estilização de interfaces de usuário.

## 2.4 PostgreSQL

O PostgreSQL é um poderoso sistema de banco de dados relacional de código aberto com mais de 30 anos de desenvolvimento ativo, confiável, de alto desempenho e vários recursos.

## 3 - Requisitos e Restrições Arquiteturais

### 3.1 Ferramentas de desenvolvimento

O projeto será desenvolvido utilizando a IDE Visual Studio 2022 versão Community para a criação do backend e Visual Studio Code para implementação do frontend.

### 3.2 Infraestrutura

Iaas na AZURE com as seguintes configurações:

* Máquina virtual com 4 vcores
* 16 GB de memória ram
* Sistema operacional Debian 11
* Nginx para servidor web
* Banco de dados PostgreSQL

### 3.3 Restrições

A aplicação apesar de ser responsiva devido ao uso da biblioteca Bootstrap, poderá apresentar limitações de uso em dispositivos móveis como tablets e smartphones pois será priorizado o uso de teclado e mouse nas provas práticas.

## 4 - Visão de Casos de Uso

 ### Casos de uso:

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
* ...

    

## 5 - Visão Lógica

A aplicação consiste em um frontend rodando React e Bootstrap como interface do usuário e uma API construída com ASP.Net e ORM Entity Framework para mapeamento das tabelas do banco de dados PostgreSQL.

### 5.1 Visão Geral
!["Visão Geral"](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/visao-geral.jpg)

O Usuário interage com a aplicação em uma página Web responsiva e apesar de ser possível o uso em dispositivos móveis como smartphones e tablets, será recomendado o uso em notebooks e desktops, pois o uso de teclado e mouse se tornam necessários para a realização dos testes práticos dos candidatos.

As requisições e respostas realizadas pelo frontend, são feitas através do protocolo HTTP para uma API Restful implementando todos os verbos do protocolo de forma correta.
No backend, uma aplicação escrita em C# utilizando o framework .NET com ASP.NET e para facilitar a escrita das querys, é feito o uso do ORM Entity Framework 6.0.
O banco de dados utilizado será o PostgreSQL por ser open source e ter uma licença mais abrangente.

## 6 - Visão de implementação

## Referências

NET | Free. Cross-platform. Open Source - Disponível em https://dotnet.microsoft.com/en-us/ - Acessado em 07/08/2022

React - Disponível em https://pt-br.reactjs.org/ - Acessado em 08/08/2022
