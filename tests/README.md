# 🧪 Estratégia de Qualidade e Automação — Patrimônio 360

Este diretório contém os planos de teste, massa de dados e scripts de automação que garantem a estabilidade e a segurança do sistema Patrimônio 360. A estratégia é baseada na Pirâmide de Testes, focando em cobertura de código e fluxos críticos de negócio.

## 🚀 Pilares da Automação

### 1. Testes de API (Integration & Contract)
* **Ferramenta:** RestAssured (Java)
* **Foco:** Validar regras de negócio, segurança dos endpoints (RBAC), integridade dos JSONs e contratos da API.
* **Localização:** `/backend/src/test`

### 2. Testes de Interface E2E (End-to-End)
* **Ferramenta:** Cypress (JavaScript)
* **Foco:** Simular a jornada completa do usuário (ex: fluxo de envio de ativo até a assinatura do termo).
* **Cenários Críticos:** Login, atribuição de ativos, filtros de dashboard e geração de PDF.
* **Localização:** `/frontend/cypress`

## 📋 Cobertura de Cenários Críticos

O plano de testes prioriza os seguintes cenários de alto risco:

* **Segurança (Auth):** Tentativa de acesso a recursos administrativos por perfis sem permissão (403 Forbidden).
* **Conformidade (LGPD):** Verificação se os logs de auditoria foram gerados corretamente após alteração de dados sensíveis.
* **Logística:** Validação do fluxo de status do ativo (Disponível -> Enviado -> Recebido).
* **Persistência:** Garantir que dados complexos (JSONB) estão sendo salvos e recuperados sem perda de integridade.

## 🛠️ Como Executar os Testes

### Testes de Backend (API)
Navegue até a pasta `/backend` e execute:
```bash
mvn test
