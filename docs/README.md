# 📚 Documentação Técnica — Patrimônio 360

Este diretório centraliza toda a documentação de suporte, definições de arquitetura e artefatos de design do sistema Patrimônio 360. O objetivo é garantir a rastreabilidade das decisões técnicas e facilitar o onboarding de novos desenvolvedores.

## 🏗️ Arquitetura do Sistema

O Patrimônio 360 foi desenhado seguindo os princípios de **Clean Architecture** e **Hexagonal Architecture** no backend, garantindo baixo acoplamento entre as regras de negócio e os frameworks externos.

### Componentes de Infraestrutura:
* **API Gateway/Backend:** Java 21 + Spring Boot 3.
* **Frontend:** React (SPA) com Vite.
* **Database:** PostgreSQL (Persistência Relacional + JSONB para flexibilidade).
* **Cache:** Redis (Otimização de consultas de BI e gestão de sessões).
* **Storage:** Amazon S3 (Simulado/Localstack) para armazenamento de Notas Fiscais e Termos de Responsabilidade.

## 📐 Artefatos de Design e Planejamento

Para visualizar o planeamento completo do projeto, utilize os links abaixo:

* **Protótipo de Alta Fidelidade (Figma):** [Link para o Figma]
    * *Foco: Usabilidade em dashboards e gestão de inventário.*
* **Board de Gestão Ágil (Jira):** https://patrimonio360.atlassian.net/jira/software/c/projects/P3/boards/3?atlOrigin=eyJpIjoiMmJjYzk0YTk4ZTE5NDQzNzg1MTU4NzJkZGM1MzAxMGUiLCJwIjoiaiJ9
    * *Estrutura: Épicos, User Stories detalhadas e sub-tasks técnicas.*

## 🔐 Governança e Segurança

A documentação de segurança detalha como o sistema atende aos requisitos de conformidade:

1.  **LGPD:** Mapeamento de dados sensíveis e implementação de auditoria via Spring AOP.
2.  **RBAC (Role-Based Access Control):** Definição da matriz de permissões (ADMIN, RH, LOGÍSTICA, COLABORADOR).
3.  **Criptografia:** Estratégia de encriptação de dados em repouso (AES-256).

## 📊 Estrutura de Diretórios em /docs

* `/architecture`: Diagramas de sequência, diagramas de classe e DER (Diagrama Entidade-Relacionamento).
* `/api-spec`: Definição de contratos (OpenAPI/Swagger) em formato JSON/YAML.
* `/legal`: Modelos dos Termos de Responsabilidade e políticas de privacidade simuladas.
* `/mockups`: Exportações estáticas das principais telas do sistema.

---
> **Nota:** Esta documentação é atualizada continuamente à medida que novos Épicos são implementados no Jira.
