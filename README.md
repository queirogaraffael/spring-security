# API de Autenticação

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=for-the-badge&logo=openjdk&logoColor=white)  
![Spring](https://img.shields.io/badge/spring-%236DB33F.svg?style=for-the-badge&logo=spring&logoColor=white)  
![H2](https://img.shields.io/badge/H2-%230092CC.svg?style=for-the-badge&logo=h2&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens)  

Este projeto é uma API construída utilizando **Java, Java Spring, H2 como banco de dados e Spring Security com JWT para controle de autenticação.**  

A API foi desenvolvida com base no repositório de [Fernanda Kipper](https://github.com/Fernanda-Kipper/auth-api) para fins de estudo, com o objetivo de demonstrar como configurar autenticação e autorização em uma aplicação Spring utilizando Spring Security.

## Índice  

- [Instalação](#instalação)  
- [Configuração](#configuração)  
- [Uso](#uso)  
- [Endpoints da API](#endpoints-da-api)  
- [Autenticação](#autenticação)  
- [Banco de Dados](#banco-de-dados)  
- [Contribuindo](#contribuindo)  

## Instalação  

1. Clone o repositório:  

```bash
git clone git@github.com:queirogaraffael/spring-security.git
```

2. Instale as dependências com Maven.  

## Uso  

1. Inicie a aplicação com Maven.  
2. A API estará acessível em http://localhost:8080.  

## Endpoints da API  

A API fornece os seguintes endpoints:  

```markdown
GET /product - Retorna uma lista de todos os produtos. (Usuários autenticados)

POST /product - Cadastra um novo produto (Requer acesso ADMIN).

POST /auth/login - Faz login no aplicativo.

POST /auth/register - Registra um novo usuário no aplicativo.
```

## Autenticação  

A API utiliza Spring Security para controle de autenticação. Os seguintes papéis (roles) estão disponíveis:  

```
USER -> Papel padrão para usuários autenticados.
ADMIN -> Papel de administrador para gerenciar parceiros (cadastrar novos parceiros).
```
Para acessar endpoints protegidos como ADMIN, forneça as credenciais apropriadas no cabeçalho da requisição.  

## Banco de Dados  

O projeto utiliza o banco de dados em memória H2.
