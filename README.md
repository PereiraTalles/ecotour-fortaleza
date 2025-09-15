# EcoTour Fortaleza

## 🌱 1. Sobre o Projeto

O **EcoTour Fortaleza** é um aplicativo multiplataforma que funciona como um guia digital sustentável para turistas na cidade de Fortaleza. Nosso objetivo é promover um turismo mais consciente, integrando cultura local, gastronomia autêntica e opções de mobilidade de baixo impacto ambiental, alinhando-se com o **ODS 11: Cidades e Comunidades Sustentáveis**.

## 🎯 2. Problema e Solução

### Problema:
Turistas em Fortaleza frequentemente não têm acesso a informações que os ajudem a fazer escolhas turísticas sustentáveis, resultando em:
- Maior uso de transporte poluente.
- Pouco apoio à economia e cultura locais.
- Dificuldade em descobrir rotas e experiências autênticas e ecológicas.

### Solução:
Um aplicativo que oferece:
- 📍 Roteiros personalizados com pontos turísticos culturais e naturais.
- 🍽️ Sugestões de gastronomia local e sustentável.
- 🚲 Integração com opções de transporte verde (bikes, rotas a pé, caronas).
- 🗺️ Rotas otimizadas para menor consumo de combustível (via integração com APIs de mapa).
- 💚 Um diferencial que une tecnologia, sustentabilidade e experiência do usuário.

## 👥 3. Equipe e Divisão de Tarefas

| Integrante | Matrícula | Função Principal |
| :--- | :--- | :--- |
| Talles de Lima Pereira | 2326201 | Gerente de Projeto & Arquiteto de Software |
| João Eduardo Lúcio Araújo | 291356 | Analista de Requisitos |
| Milene de Souza Júnior | 2326165 | Designer UX/UI & Documentadora |
| Herison Daniel Wanderley | 2315221 | Especialista em Dados & APIs |

## 🏗️ 4. Visão Geral da Arquitetura

O sistema será desenvolvido utilizando uma arquitetura baseada em microssserviços, com as seguintes camadas:

- **Frontend:** Aplicação móvel desenvolvida em **React Native** e versão web em **React**.
- **Backend:** API RESTful construída com **Node.js** e **Express**.
- **Banco de Dados:** **PostgreSQL** para persistência de dados.
- **Integração com APIs Externas:** Google Maps API/Places API para geolocalização e rotas.


### Link do Figma:

https://www.figma.com/design/jvcID6f9Ls8jKJ3cisPKGO/EcoTour-Fortaleza---Prot%C3%B3tipos?node-id=15-10183&m=dev&t=nFmJZ7UaovwJZLHo-1

### Diagrama de Arquitetura Simplificado:

```mermaid
graph TD
    A[Usuário Mobile] --> B[React Native]
    C[Usuário Web] --> D[React]
    B --> E[Backend - Node.js/Express]
    D --> E
    E --> F[Banco de Dados PostgreSQL]
    E --> G[Google Maps API]