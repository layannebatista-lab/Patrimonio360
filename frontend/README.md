# 💻 Patrimônio 360 — Frontend Dashboard

Interface administrativa de alta performance desenvolvida para a gestão centralizada de ativos de TI. O projeto foca em uma experiência de usuário (UX) fluida, com tabelas densas, dashboards analíticos e fluxos de governança.

## 🛠️ Stack Tecnológica

* **React 18+:** Utilização de Concurrent Mode e Hooks customizados para separação de lógica e visual.
* **Tailwind CSS:** Sistema de estilização utilitária para garantir responsividade e design system consistente.
* **TanStack Query (React Query) v5:** Gerenciamento de estado assíncrono, cache inteligente e sincronização de dados com o servidor.
* **TanStack Table v8:** Engine para grids complexos, suportando filtros por facetas, ordenação multi-coluna e virtualização de linhas.
* **React Hook Form + Zod:** Validação rigorosa de formulários e inferência de tipos em schemas dinâmicos.
* **Recharts:** Visualização de dados para os indicadores de BI e saúde patrimonial.
* **Lucide React:** Conjunto de ícones leves e consistentes.

## 📐 Arquitetura do Cliente

O projeto segue uma estrutura modular baseada em responsabilidades:

* **`/src/components`**: Componentes de interface (Atoms, Molecules, Organisms) seguindo o padrão de design system.
* **`/src/hooks`**: Hooks customizados encapsulando a lógica de negócio e as chamadas ao TanStack Query.
* **`/src/services`**: Configuração da instância Axios com interceptors para injeção automática de Token JWT e tratamento global de erros (401, 403).
* **`/src/pages`**: Views principais organizadas pelos Épicos do sistema (Dashboard, Inventário, Colaboradores).
* **`/src/utils`**: Funções auxiliares para formatação de moeda (BRL), datas e manipulação de arquivos (PDF/Blob).

## 🔐 Segurança e Performance

* **RBAC (Role-Based Access Control):** Proteção de rotas e componentes baseada no perfil do usuário (Admin, RH, Logística).
* **State Hydration:** Persistência seletiva de filtros e preferências do usuário para melhorar a retenção de contexto.
* **Virtualização:** Implementação de `react-window` para tabelas com grande volume de dados, mantendo 60fps na rolagem.
* **Sanitização:** Proteção nativa contra XSS e validação de payloads antes do envio para a API.

## 🚀 Guia de Execução

1.  **Instalação das dependências:**
    ```bash
    npm install
    ```

2.  **Configuração das variáveis de ambiente:**
    Crie um arquivo `.env` na raiz seguindo o modelo `.env.example`:
    ```env
    VITE_API_URL=http://localhost:8080/api/v1
    ```

3.  **Iniciar servidor de desenvolvimento:**
    ```bash
    npm run dev
    ```

## 🧪 Suíte de Qualidade

Execução de testes de ponta a ponta (E2E) com **Cypress**:
```bash
npm run cy:open
