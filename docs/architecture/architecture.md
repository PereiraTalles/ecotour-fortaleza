# Arquitetura do Sistema - EcoTour Fortaleza

## 1. Visão Geral
Este documento descreve a arquitetura do sistema EcoTour Fortaleza, uma aplicação multiplataforma desenvolvida para promover turismo sustentável. A arquitetura foi projetada para ser escalável, segura e de fácil manutenção.

## 2. Objetivos Arquiteturais
- **Escalabilidade:** Suportar crescimento de usuários e dados.
- **Manutenibilidade:** Facilitar atualizações e correções.
- **Desempenho:** Garantir tempo de resposta rápido.
- **Segurança:** Proteger dados dos usuários e conformidade com LGPD.
- **Portabilidade:** Funcionar em diferentes dispositivos e plataformas.

## 3. Padrão Arquitetural
Foi escolhida a **Arquitetura em Microssserviços** para permitir escalabilidade independente e desenvolvimento paralelo de equipes. O frontend comunica-se com o backend através de APIs RESTful.

## 4. Diagrama de Arquitetura

```mermaid
flowchart TD
    A[Usuário Mobile<br>React Native] --> B[API Gateway<br>Node.js]
    C[Usuário Web<br>React] --> B
    B --> D[Serviço de Autenticação]
    B --> E[Serviço de Pontos Turísticos]
    B --> F[Serviço de Roteiros]
    B --> G[Serviço de Mapas]
    D --> H[(Banco de Dados<br>Usuários)]
    E --> I[(Banco de Dados<br>Pontos Turísticos)]
    F --> J[(Banco de Dados<br>Roteiros)]
    G --> K[API Google Maps]