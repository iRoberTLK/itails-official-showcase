# 🐾 iTails Official - Arquitetura e Engenharia de Sistema

> **Nota:** Este é um repositório de portfólio (Showcase). O código-fonte dos aplicativos e da API do **iTails Official** é mantido em repositórios privados para proteção de propriedade intelectual.

## 📌 Visão Geral
O **iTails Official** é um ecossistema completo (Marketplace e Agendador de Serviços) focado no nicho pet, conectando tutores a profissionais e pet shops. A plataforma lida com transações financeiras, gestão de agendas, controle de parceiros e programas de fidelização.

## 🏗️ Arquitetura do Ecossistema
A plataforma foi desenhada utilizando uma arquitetura baseada em microsserviços lógicos, dividida em três frentes principais:

*   **App Cliente (React Native / Expo):** Interface voltada para os tutores pesquisarem e agendarem serviços.
*   **App Parceiro (React Native / Expo):** Painel do profissional para controle de agenda, ganhos e programa de fidelidade.
*   **Back-Office & Core API (PHP / Laravel):** Motor de regras de negócio, painel administrativo em **Blade** e exposição de rotas API RESTful.

## ⚙️ Desafios Técnicos & Soluções Aplicadas

### 1. Motor Financeiro e Split de Pagamentos
Implementação de integrações complexas com gateways de pagamento (Stone / Pagar.me) lidando com:
*   Autenticação de APIs via manipulação de certificados de segurança.
*   Lógica robusta de **Split de Pagamento**, gerenciando a retenção de comissões da plataforma e os repasses diretos aos parceiros.
*   Gestão de estornos e cálculo automatizado de multas de cancelamento.

### 2. DevOps e Deploy Mobile (EAS)
*   Gestão completa do ciclo de vida dos aplicativos móveis utilizando o **Expo Application Services (EAS)** para builds na nuvem.
*   Configuração de esteiras para geração de pacotes `.aab` e publicação direta no Google Play Console para testes internos e produção.

### 3. Lógica de Negócios e Fidelização
*   Desenvolvimento de regras dinâmicas de comissionamento, incluindo a inteligência do programa de fidelidade para parceiros (cálculo de descontos na taxa de retenção baseados em métricas de indicação de novos clientes).

## 💻 Stack Tecnológico
*   **Back-end:** PHP, Laravel, Blade
*   **Front-end Mobile:** React Native, TypeScript, TSX, Expo (PWA e Android)
*   **Infraestrutura & Ambiente:** Docker, Laragon (gestão de certificados SSL locais), Azure DevOps (CI/CD)
