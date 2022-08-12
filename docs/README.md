# D5 - Grupo 8

# Projeto e Acompanhamento de Progresso

[Quadro do Projeto](https://github.com/users/ferdinandocastilho/projects/2/views/1)

# Solução CTEDS

#1. Visão Geral

Seleção CTEDS é uma plataforma unificada a ser agregada na infraestrutura da USP para recrutamento, acompanhamento e realização de avaliações do curso CTEDS 

# Competências # 

O Time é composto por 4 pessoas, cada um com as seguintes atribuições:

- **Fernando Castilho** - _Team Manager_ - Responsável pela atribuição de tarefas e gerenciamento da qualidade dos trabalhos dos demais integrantes.
- **Maikeu Locatelli** - _Backend Developer_ - Responsável por todo desenvolvimento da api responsável pelo recrutamento, assim como o gerenciamento do banco de dados e outras funções acessórias aos mesmos.
- **Gabriela Provedel Dalla Bernardi** - _Frontend Developer_ - Responsável pelo desenvolvimento da página resposável pelo recrutamento e tudo relativo diretamente a esta página.
- **Renato Nascimento** - _Coordenador de Infraestrutura_ - Responsável pela implantação e manutenção da infraestrutura em que a aplicação é executada, como máquinas virtuais.

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

## 5 - Visão Lógica

## 6 - Visão de implementação

## Referências

NET | Free. Cross-platform. Open Source - Disponível em https://dotnet.microsoft.com/en-us/ - Acessado em 07/08/2022

React - Disponível em https://pt-br.reactjs.org/ - Acessado em 08/08/2022

# Protótipo de baixa fidelidade

O protótipo de baixa fidelidade tem um viés de desenvolver estratégias e sintetizar ideias do grupo, para definir a interação do usuário com o projeto e a base da futura visualização da aplicação.

## Fluxo de usuário

![Fluxograma](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/fluxograma.png)

## Telas

![Tela1](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/mockup1.png)

![Tela2](https://github.com/ferdinandocastilho/selecao-cteds/blob/main/assets/mockup2.png)
