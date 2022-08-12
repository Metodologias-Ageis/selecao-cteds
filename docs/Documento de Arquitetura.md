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
MVC                  | Model View Controlle
ORM                  | Object-Realational Mapping
SPA                  | Single Page Application
VM                   | Virtual Machine

## 2 - Representação Arquitetural

Será utilizado neste projeto o padrão de arquitetura MVC (Model, View and Controller). A camada Model fica responsável por gerenciar, controlar os dados e regras de négocio da aplicação. Está está ligada diretamente ao banco de dados.
A camada View é responsável pela apresentação das informações aos usuários, o frontend da aplicação. Já a camada de Controller é responsável pela intermediação das requisições vindas da View para o Model.

### 2.1 - .NET  
O .NET é uma plataforma de desenvolvedor gratuita, multiplataforma de código aberto para criação de aplicativos web, mobile, desktop, games, ioT, cloud e microserviços. O .NET é criado em um runtime de alto desempenho que é usado em produção por muitas aplicações de alta escala.

### 2.2 React

React é uma biblioteca Javascript open source para criar interfaces de usuário. 

### 2.3 Bootstrap

Bootstrap é um conjunto de ferramentas e componentes frontend, que facilicitam a padronização e estilização de interfaces de usuário.

## ...

## 3 - Requisitos e Restrições Arquiteturais

## 4 - Visão de Casos de Uso

    Casos de uso:
    * Interesse (oferta do curso)
    * Autenticação
    *

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
