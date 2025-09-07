# Documento de Requisitos - EcoTour Fortaleza

## 1. Introdução
Este documento descreve os requisitos funcionais e não funcionais do sistema EcoTour Fortaleza, uma aplicação multiplataforma voltada para o turismo sustentável.

## 2. Objetivo do Sistema
Promover um turismo mais consciente e sustentável em Fortaleza, conectando turistas a experiências locais autênticas, opções de transporte verde e roteiros personalizados que reduzam o impacto ambiental.

## 3. Público-Alvo
- Turistas nacionais e internacionais visitando Fortaleza.
- Guias turísticos locais.
- Estabelecimentos comerciais parceiros (restaurantes, aluguel de bikes, pousadas).

## 4. Requisitos Funcionais (RF)

| ID    | Descrição | Prioridade |
| :---- | :--- | :--- |
| **RF01** | **Cadastro e Gerenciamento de Usuários**: O sistema deve permitir que usuários se cadastrem e façam login utilizando email e senha ou autenticação social (Google). | Alta |
| **RF02** | **Perfil de Usuário**: O usuário deve poder editar seu perfil, incluindo preferências de turismo (ex: "baixo custo", "gastronomia", "cultural"). | Alta |
| **RF03** | **Busca e Filtros**: O sistema deve permitir buscar pontos turísticos por categoria (praia, cultura, gastronomia) e filtrar por proximidade, avaliação ou preço. | Alta |
| **RF04** | **Sugestão de Roteiros Personalizados**: O sistema deve gerar roteiros completos baseados nas preferências do usuário e na localização atual. | Alta |
| **RF05** | **Integração com Mapas**: O sistema deve exibir mapas interativos e traçar rotas entre pontos, integrando-se com Google Maps API ou similar. | Alta |
| **RF06** | **Listagem de Transportes Sustentáveis**: Deve listar opções de transporte verde (ex: bicicletárias, pontos de carona solidária) com localização e preços. | Média |
| **RF07** | **Sistema de Avaliações e Comentários**: Usuários podem avaliar e comentar sobre pontos turísticos e estabelecimentos. | Média |
| **RF08** | **Modo Offline Básico**: O usuário deve poder baixar mapas e informações básicas de roteiros para uso offline. | Baixa |

## 5. Requisitos Não-Funcionais (RNF)

| ID    | Descrição | Categoria |
| :---- | :--- | :--- |
| **RNF01** | **Usabilidade**: A interface deve ser intuitiva e responsiva, seguindo princípios de UX/UI. | Usabilidade |
| **RNF02** | **Performance**: O tempo de resposta do sistema deve ser inferior a 3 segundos para todas as requisições. | Performance |
| **RNF03** | **Confiabilidade**: O sistema deve estar disponível 99% do tempo (uptime). | Confiabilidade |
| **RNF04** | **Segurança**: Dados dos usuários devem ser criptografados e o sistema deve estar em conformidade com a LGPD. | Segurança |
| **RNF05** | **Compatibilidade**: O aplicativo deve funcionar nas versões recentes do Android e iOS. | Compatibilidade |
| **RNF06** | **Escalabilidade**: A arquitetura deve permitir escalar horizontalmente para suportar aumento de usuários. | Escalabilidade |

## 6. Regras de Negócio

| ID    | Descrição |
| :---- | :--- |
| **RN01** | Um usuário deve estar logado para favoritar locais, salvar roteiros e fazer comentários. |
| **RN02** | Os roteiros sugeridos devem priorizar meios de transporte sustentáveis (como caminhada ou bike) quando possível. |
| **RN03** | Estabelecimentos parceiros (como restaurantes ou aluguel de bikes) devem ser previamente validados pela equipe do EcoTour ou por uma entidade parceira (ex: SETUR). |
| **RN04** | A avaliação de um local será calculada como a média aritmética das notas dadas pelos usuários. |

## 7. Histórias de Usuário

- **Como** um turista,
  **quero** poder informar minhas preferências (ex: "gastronomia", "baixo custo"),
  **para que** eu receba sugestões de roteiros personalizados.

- **Como** um usuário,
  **quero** visualizar no mapa as rotas até um ponto turístico,
  **para que** eu possa escolher o meio de transporte mais conveniente e sustentável.

- **Como** um usuário logado,
  **quero** poder avaliar e comentar sobre um lugar que visitei,
  **para que** outros turistas possam ter mais informações.

## 8. Casos de Uso (Resumido)

- **Cadastrar Usuário**
- **Buscar Pontos Turísticos**
- **Criar/Salvar Roteiro Personalizado**
- **Avaliar Local**
- **Visualizar Rota no Mapa**