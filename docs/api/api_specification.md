# Especificação da API - EcoTour Fortaleza

## 1. Visão Geral
Esta documentação descreve os endpoints da API RESTful do EcoTour Fortaleza. A API permite o gerenciamento de usuários, pontos turísticos, roteiros e integração com serviços de mapas.

**URL Base:** `https://api.ecotourfortaleza.com/v1`

**Formato de Resposta:** JSON

## 2. Autenticação e Autorização
A API utiliza autenticação via **JWT (JSON Web Token)**. Após o login bem-sucedido, um token deve ser incluído no cabeçalho de todas as requisições que requerem autenticação.

```http
Authorization: Bearer <seu_jwt_token>