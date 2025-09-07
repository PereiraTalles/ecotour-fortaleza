# Modelo de Banco de Dados - EcoTour Fortaleza

## 1. Visão Geral
Este documento descreve o modelo de dados do sistema EcoTour Fortaleza, incluindo as entidades, seus atributos, relacionamentos e o diagrama Entidade-Relacionamento (ER).

## 2. Diagrama Entidade-Relacionamento (ER)
O diagrama abaixo ilustra as principais entidades e seus relacionamentos:

```mermaid
erDiagram
    USUARIOS {
        int id PK
        varchar nome
        varchar email
        varchar senha_hash
        json preferencias
        datetime data_criacao
    }

    PONTOS_TURISTICOS {
        int id PK
        varchar nome
        text descricao
        varchar categoria
        decimal latitude
        decimal longitude
        varchar endereco
        boolean validado
    }

    ROTEIROS {
        int id PK
        int usuario_id FK
        varchar titulo
        text descricao
        datetime data_criacao
    }

    TRANSPORTES {
        int id PK
        varchar tipo
        varchar descricao
        decimal latitude
        decimal longitude
        decimal preco_medio
    }

    AVALIACOES {
        int id PK
        int usuario_id FK
        int ponto_id FK
        int nota
        text comentario
        datetime data_avaliacao
    }

    USUARIOS ||--o{ ROTEIROS : cria
    USUARIOS ||--o{ AVALIACOES : faz
    PONTOS_TURISTICOS ||--o{ AVALIACOES : recebe
    ROTEIROS }o--o{ PONTOS_TURISTICOS : contém
    ROTEIROS }o--o{ TRANSPORTES : utiliza