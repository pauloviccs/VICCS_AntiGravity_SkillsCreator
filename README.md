# VICCS AntiGravity Skills Creator

Bem-vindo ao repositório **VICCS AntiGravity Skills Creator**. Este projeto é uma base de conhecimento centralizada e evolutiva projetada para fornecer "Skills" (Habilidades) especializadas para o agente AntiGravity.

## 🎯 Objetivo

O objetivo principal deste repositório é padronizar e expandir as capacidades do agente AntiGravity através de módulos de instruções bem definidos. Cada "Skill" fornece ao agente o contexto, as regras e os fluxos de trabalho necessários para executar tarefas complexas com precisão e consistência.

## 📂 Estrutura do Projeto

A estrutura do repositório é organizada para facilitar a criação, manutenção e consumo das skills:

- **`.agent/skills/`**: O coração do projeto. Contém subdiretórios para cada habilidade específica.
  - Cada pasta de skill (ex: `deploying-vercel`) contém um arquivo `SKILL.md` com as instruções mestras.
  - Pode conter pastas auxiliares como `scripts/`, `examples/` ou `resources/`.
- **`rules/`**: Contém as diretrizes e regras para a criação de novas skills e manutenção do repositório.
  - `AntiGravity_SkillCreator_rules.md`: O guia definitivo para criar novas skills mantendo o padrão do projeto.

## 🛠️ Skills Disponíveis

O repositório conta com uma vasta biblioteca de habilidades, organizadas por domínio:

### 🧠 Core, Arquitetura & Workflow

*Skills fundamentais para planejamento, análise e operação do agente.*

- **`app-builder`**: Orquestrador para construir aplicações completas do zero.
- **`architecture`**: Framework para decisões arquiteturais e análise de trade-offs.
- **`behavioral-modes`**: Modos operacionais do agente (brainstrom, implement, debug, etc.).
- **`brainstorming`**: Protocolo socrático para resolver problemas complexos ou ambíguos.
- **`clean-code`**: Padrões pragmáticos de código limpo e refatoração.
- **`documentation-templates`**: Templates para READMEs, Docs de API e comentários.
- **`parallel-agents`**: Padrões para orquestração de múltiplos agentes.
- **`plan-writing`**: Criação de planos de implementação estruturados.

### 🎨 Frontend & Design

*Criação de interfaces, experiências visuais e identidades.*

- **`brand-identity`**: Gestão de identidade visual e design systems.
- **`building-advanced-visual-websites`**: WebGL, Three.js e efeitos visuais avançados.
- **`building-mobile-apps`**: React Native e Expo para mobile.
- **`frontend-design`**: Princípios de design UI/UX para desenvolvedores.
- **`mobile-design`**: Padrões de design "Mobile-First" e interações por toque.
- **`nextjs-best-practices`**: Arquitetura e padrões para App Router e Server Components.
- **`prototyping-lovable`**: Prototipagem rápida usando Lovable.AI.
- **`react-patterns`**: Hooks, contextos e padrões modernos de React.
- **`tailwind-patterns`**: Arquitetura CSS-first e tokens com Tailwind v4.
- **`ui-ux-pro-max`**: Biblioteca exaustiva de componentes, paletas e heurísticas de UX.
- **`viccs-brand-2025-identity`**: Identidade específica da marca VICCS 2025.

### ⚙️ Backend & Dados

*Lógica de servidor, bancos de dados e APIs.*

- **`api-patterns`**: Design de APIs REST, GraphQL e RPC.
- **`database-design`**: Modelagem de dados, SQL e otimização de schemas.
- **`managing-supabase`**: Gestão completa do ecossistema Supabase.
- **`nestjs-expert`**: Arquitetura modular e injeção de dependência com NestJS.
- **`nodejs-best-practices`**: Segurança, performance e padrões async para Node.js.
- **`prisma-expert`**: Modelagem de schema e queries eficientes com Prisma ORM.
- **`python-patterns`**: Padrões Pythonic e estruturação de projetos Python.
- **`using-bun`**: Utilização do toolkit Bun (runtime, test, bundler).

### 🚀 DevOps & Infraestrutura

*Deploy, CI/CD e gerenciamento de servidores.*

- **`automating-github-actions`**: Pipelines de CI/CD e automação de workflows.
- **`bash-linux`**: Automação e scripts via terminal Linux/Bash.
- **`deploying-vercel`**: Deploy serverless e edge functions na Vercel.
- **`deployment-procedures`**: Estratégias de deploy seguro e rollbacks.
- **`docker-expert`**: Otimização avançada de Dockerfiles e segurança de containers.
- **`hosting-vite`**: Build e hospedagem de SPAs com Vite.
- **`powershell-windows`**: Automação e administração via PowerShell.
- **`server-management`**: Monitoramento e gestão de servidores Linux.
- **`using-docker`**: Fundamentos de containerização e Docker Compose.

### 🕹️ Game Dev & Modding

*Desenvolvimento de jogos e modificações.*

- **`game-development`**: Orquestrador para desenvolvimento de jogos multipataforma.
- **`modding-fivem-qbcore`**: Servidores de GTA V RP com QBCore e Lua.
- **`modding-hytale`**: Modding para Hytale (Java 25, Visual Scripting, V2 World Gen).
- **`using-noesis-gui`**: Interfaces XAML para engines de jogos.

### ✅ Qualidade (QA) & Testes

*Garantia de qualidade e correção de bugs.*

- **`code-review-checklist`**: Diretrizes para revisão de código e segurança.
- **`lint-and-validate`**: Configuração de linters e ferramentas de análise estática.
- **`systematic-debugging`**: Metodologia científica para resolução de bugs complexos.
- **`tdd-workflow`**: Ciclo Red-Green-Refactor e desenvolvimento guiado por testes.
- **`testing-apps`**: Configuração de runners como Vitest e Jest.
- **`testing-patterns`**: Estratégias de mocking, stubs e testes de integração.
- **`webapp-testing`**: Testes E2E e automação com Playwright/Cypress.

### 🔒 Segurança & Otimização

*Proteção, performance e visibilidade.*

- **`geo-fundamentals`**: Otimização para "Generative Engines" (AI Search).
- **`performance-profiling`**: Análise de gargalos e otimização de runtime.
- **`red-team-tactics`**: Simulação de ataques e análise de vulnerabilidades.
- **`seo-fundamentals`**: Otimização para motores de busca e Core Web Vitals.
- **`vulnerability-scanner`**: Identificação e mitigação de CVEs e riscos de segurança.

### 🧩 Especializadas & Integração

*Habilidades de domínio específico.*

- **`i18n-localization`**: Internacionalização e suporte a múltiplos idiomas.
- **`integrating-ai`**: Implementação de LLMs e agentes via SDKs de IA.
- **`mcp-builder`**: Criação de servidores MCP (Model Context Protocol).
- **`typescript-expert`**: Tipagem avançada e configuração de TSConfig.

## 🚀 Como Criar uma Nova Skill

Para adicionar uma nova habilidade ao arsenal do AntiGravity:

1. Consulte o arquivo `rules/AntiGravity_SkillCreator_rules.md` para entender os padrões obrigatórios.
2. Crie uma nova pasta em `.agent/skills/` com o nome da skill (formato `verbo-substantivo`, ex: `debugging-react`).
3. Crie o arquivo `SKILL.md` seguindo o template oficial, definindo triggers, workflows e instruções.
4. (Opcional) Adicione exemplos ou scripts auxiliares.

## ✨ Filosofia

Este projeto segue a filosofia **"Vibe Coding"**:

- **Eficiência**: Instruções diretas e práticas.
- **Qualidade**: Padrões elevados de código e design.
- **Evolução**: Aprendizado contínuo e adaptação a novas tecnologias.

---
*Gerado por AntiGravity Agent*
