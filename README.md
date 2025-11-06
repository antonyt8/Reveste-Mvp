<div align="center">
   <img width="300" alt="Reveste Logo" src="/reveste-logo.png" />
</div>

# Reveste — Conectar Solidariedade e Esperança (MVP)

> Aplicativo MVP para gerenciamento de doações, cadastro de doadores e um fluxo simples de doação com gamificação.

Este repositório contém o front-end do projeto implementado com React + Vite + TypeScript. É uma prova de conceito (MVP) pensada para prototipagem e testes rápidos.

## Tecnologias

- React 19
- Vite
- TypeScript
- react-hook-form + zod (validação de formulários)
- framer-motion (animações)

## Estrutura do projeto (resumo)

- `App.tsx` — provê contexto da aplicação, navegação baseada em enum `Screen` e persistência simples via `localStorage`.
- `components/` — telas e componentes organizados por domínio (auth, donor, admin, common).
- `public/` — assets públicos (manifest, service worker, logo, etc.).
- `netlify.toml` — configuração para deploy no Netlify (inclui redirect SPA).

## Funcionalidades implementadas (MVP)

- Fluxo de autenticação (Splash, Login, SignUp, Forgot Password).
- Tela `Meus Dados` com edição via `react-hook-form` + `zod` e upload de avatar (compressão/resizing no cliente).
- Fluxo de doação em múltiplos passos com confirmação e tela de sucesso.
- Sistema simples de pontos e cupons para gamificação (acumula pontos por doação, resgata cupons).
- PWA fallback básico: `public/manifest.webmanifest` + `public/sw.js`.

## Rodando localmente

Pré-requisitos: Node.js (recomendo >= 18)

1. Instale dependências:

```bash
npm install
```

2. Rodar em desenvolvimento:

```bash
npm run dev
```

3. Criar build de produção:

```bash
npm run build
```

4. Pré-visualizar o build:

```bash
npm run preview
```

## Deploy no Netlify

O repositório já inclui `netlify.toml` com o comando de build e redirect configurados. Você pode usar duas abordagens:

- Conectar o repositório ao Netlify (recomendado):
   - Em Netlify: New site → Import from Git → escolha o repo.
   - Build command: `npm run build`
   - Publish directory: `dist`

- Netlify CLI (rápido, sem Git):

```bash
npm run build
npx netlify-cli login
npx netlify-cli deploy --dir=dist --prod
```

Consulte `DEPLOY.md` no repositório para passos detalhados.

## Variáveis de ambiente

Atualmente o MVP não necessita de variáveis obrigatórias. Se você integrar serviços externos (ex.: armazenamento, APIs), adicione as chaves no painel do Netlify (Site → Site settings → Build & deploy → Environment) ou no seu provedor CI.

## Contribuições

1. Fork e clone o repositório
2. Crie uma branch: `git checkout -b feat/minha-feature`
3. Commit suas mudanças e abra um Pull Request descrevendo a alteração

## Sugestões de próximos passos

- Migrar persistência para backend (usuários, doações, imagens via presigned uploads).
- Adicionar linting (ESLint/Prettier) e testes (Vitest + Testing Library).
- Melhorar a experiência PWA e cache strategies com um Service Worker mais robusto.

## Licença

Escolha uma licença (ex.: MIT) e adicione aqui ou remova se o projeto for privado.

---

Se quiser, eu posso também:

- Adicionar o badge do Netlify no topo do README (preciso do `BADGE_ID`/site name),
- Criar um workflow GitHub Actions que faz `npm run build` e deploy automático (precisa de `NETLIFY_AUTH_TOKEN` como segredo),
- Adicionar scripts úteis (lint/test/format) ao `package.json`.

<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/drive/1m-VKEYXdsKDQlrs2qxzBydxlvfEts75W

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`

## Deploy

See `DEPLOY.md` for step-by-step instructions to publish this site to Netlify (UI and CLI). You can also add a Netlify deploy badge once your site is created — replace <YOUR_NETLIFY_BADGE_ID> and <YOUR_NETLIFY_SITE> with the values Netlify provides:

```markdown
[![Netlify Status](https://api.netlify.com/api/v1/badges/<YOUR_NETLIFY_BADGE_ID>/deploy-status)](https://app.netlify.com/sites/<YOUR_NETLIFY_SITE>/deploys)
```

The `DEPLOY.md` file includes UI and CLI options and tips for single-page apps and caching.
# Reveste-Mvp
