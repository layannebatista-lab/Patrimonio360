# 🏢 Patrimônio 360 — Gestão de Ativos Distribuídos

## 📌 Visão Geral

O **Patrimônio 360** é um sistema corporativo para **gestão completa do ciclo de vida de ativos de TI**, desenvolvido para empresas que operam em modelo **híbrido e remoto**, com colaboradores distribuídos em diferentes estados do Brasil.

O projeto foi idealizado para resolver desafios reais de **logística, controle patrimonial, segurança da informação e conformidade com a LGPD**, garantindo rastreabilidade total desde a compra do equipamento até sua devolução.

---

## 🎯 Objetivos do Sistema

* Centralizar o controle de ativos corporativos
* Garantir segurança e controle de acesso por perfil
* Atender requisitos de auditoria e LGPD
* Formalizar processos logísticos com validade jurídica
* Disponibilizar indicadores estratégicos para tomada de decisão

---

## 🧠 Visão de Produto

O Patrimônio 360 foi construído com **mentalidade enterprise**, priorizando:

* Segurança by design
* Arquitetura escalável
* Governança de dados
* Experiência do usuário
* Testabilidade e qualidade

---

## 🧩 Arquitetura Geral

**Frontend:** React

**Backend:** Java + Spring Boot

**Autenticação:** JWT + RBAC

**Banco de Dados:** PostgreSQL

**Cache:** Redis

**Relatórios:** JasperReports

**Testes Automatizados:**

* API: RestAssured
* E2E: Cypress

📐 Diagramas detalhados disponíveis em:

```
/docs/architecture
```

---

## 🔐 Segurança e Controle de Acesso

O sistema implementa **controle rigoroso de acesso**, baseado em papéis e regras de visualização:

### Perfis

* **ADMIN**: Controle total do sistema
* **RH**: Gestão de colaboradores e visualização de ativos associados
* **LOGÍSTICA**: Gestão de envios, recebimentos e devoluções
* **COLABORADOR**: Visualização apenas de seus próprios dados e ativos

### Destaques Técnicos

* Autenticação stateless com JWT
* RBAC com validação por contexto (ownership)
* Bloqueio automático por tentativas inválidas
* Mensagens de erro opacas (anti-enumeração)

---

## 🧾 Auditoria e LGPD

Todos os dados sensíveis são protegidos por um **sistema de auditoria imutável**, garantindo rastreabilidade jurídica.

### Logs de Auditoria

Cada operação relevante registra:

* Quem executou a ação
* O que foi alterado
* Quando ocorreu
* IP e User-Agent
* Estado anterior e posterior do dado (JSONB)

📌 Implementado via **Spring AOP** com persistência assíncrona.

---

## 👥 Gestão de Colaboradores

* Cadastro e edição de colaboradores
* Integração com ViaCEP
* Criptografia de dados sensíveis (CPF)
* Visualização de ativos por colaborador
* Histórico completo de movimentações

---

## 📦 Gestão de Ativos

* Cadastro de ativos com especificações dinâmicas (JSONB)
* Controle de status:

  * Disponível
  * Enviado
  * Recebido
  * Em Manutenção
  * Devolvido
* Upload de documentos (NF, fotos)
* Consulta conforme perfil de acesso

---

## 🚚 Logística e Termos Legais

* Envio e recebimento de ativos
* Registro obrigatório de código de rastreio
* Assinatura digital de termos de responsabilidade
* Geração de PDFs com validade jurídica
* Histórico logístico completo

---

## 🔔 Sistema de Notificações

Sistema orientado a eventos para comunicação automática:

* Envio de e-mails e notificações
* Alertas de segurança
* Notificações de envio, recebimento e devolução
* Histórico de notificações

---

## 📊 BI e Relatórios

* Dashboards gerenciais
* Indicadores de custo e depreciação
* Métricas operacionais e logísticas
* Exportação de relatórios executivos

---

## 🧪 Qualidade e Testes

O projeto foi desenvolvido com **forte cultura de qualidade**:

### Testes Automatizados

* **API:** RestAssured
* **E2E:** Cypress

### Cobertura de Cenários

* Segurança
* Permissões por perfil
* Fluxos críticos de negócio
* LGPD e auditoria

---

## 🗂 Estrutura do Repositório

```
/patrimonio-360
 ├── backend
 ├── frontend
 ├── docs
 │   ├── architecture
 │   └── mockups
 └── tests
     ├── api
     └── e2e
```

---

## 🧑‍💼 Papéis Simulados no Projeto

Este projeto simula um ambiente real de time multidisciplinar:

* Product Owner
* Analista de Sistemas
* UX Designer
* Desenvolvedor Backend
* Desenvolvedor Frontend
* QA Automação (API e E2E)



📌 **Este projeto foi desenvolvido com foco em aprendizado avançado, qualidade técnica e aderência a cenários reais de mercado.**
