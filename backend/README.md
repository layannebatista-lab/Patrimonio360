# ⚙️ Patrimônio 360 — Backend Engine

Esta é a API core do sistema, construída sobre a stack Java/Spring, focada em alta disponibilidade, segurança rigorosa e conformidade com a LGPD.

## 🏗️ Arquitetura Técnica
O projeto utiliza uma arquitetura **Hexagonal (Ports and Adapters)** simplificada, garantindo que as regras de negócio sejam independentes de frameworks externos.

* **Spring Boot 3.x:** Framework base.
* **Spring Security + JWT:** Autenticação stateless e RBAC.
* **Spring Data JPA:** Abstração de persistência.
* **Spring AOP:** Implementação de Auditoria Imutável (Log de eventos de sistema).
* **PostgreSQL:** Banco de dados relacional com suporte a JSONB para atributos dinâmicos.
* **Redis:** Cache de segundo nível para agregação de BI.
* **JasperReports:** Motor de geração de documentos legais (PDF).

## 🔐 Segurança e LGPD
* **Criptografia:** Dados sensíveis (CPF) são criptografados em repouso usando AES-256.
* **Auditoria:** Utilização de `@Aspect` para capturar alterações de estado em entidades críticas e persistir no log de auditoria de forma assíncrona.
* **Sanitização:** Implementação de Serializers customizados para omitir campos financeiros baseados na Authority do usuário (RBAC).

## 🚀 Como Rodar
1. Certifique-se de ter o **JDK 21** e **Maven** instalados.
2. Configure as variáveis de ambiente no `application-dev.yml` ou via Docker.
3. Execute o comando:
   ```bash
   mvn spring-boot:run -Dspring-boot.run.profiles=dev
