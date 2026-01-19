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

Atualmente, o repositório conta com uma vasta gama de habilidades para diversas áreas do desenvolvimento:

### Desenvolvimento Web & App

- **`building-advanced-visual-websites`**: Criação de sites de alto desempenho com WebGL, Three.js e shaders.
- **`building-mobile-apps`**: Desenvolvimento mobile com React Native e Expo.
- **`prototyping-lovable`**: Prototipagem rápida e "Frontend First" com Lovable.AI.
- **`viccs-brand-2025-identity`**: Diretrizes de marca e design tokens da identidade VICCS 2025.
- **`brand-identity`**: Gestão de identidade visual e design systems genéricos.

### DevOps & Infraestrutura

- **`deploying-vercel`**: Deploy e configuração de projetos na Vercel.
- **`automating-github-actions`**: Automação de pipelines CI/CD com GitHub Actions.
- **`using-docker`**: Containerização de aplicações e Docker Compose.
- **`hosting-vite`**: Configuração e build de projetos Vite.
- **`using-bun`**: Gerenciamento de projetos com Bun (runtime, package manager).
- **`managing-supabase`**: Gestão de backend Supabase (Auth, DB, Edge Functions).

### Modding & Games

- **`modding-hytale`**: Criação de mods para Hytale (Java, ECS).
- **`modding-fivem-qbcore`**: Scripting Lua e gestão de servidores FiveM (QBCore).
- **`using-noesis-gui`**: Criação de interfaces de usuário (UI) com NoesisGUI e XAML para jogos (ex: Hytale).

### Qualidade & IA

- **`testing-apps`**: Testes unitários e E2E com Vitest e Playwright.
- **`integrating-ai`**: Integração de IA com Vercel AI SDK e Ollama.

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
