# Lumini Estetica Monorepo Agents Context

This document serves as the sovereign root context router (Layer 1) for AI agents operating in the `Vitoria-Rodrigues/Lumini-Estetica` monorepo, created by Vitória Rodrigues Ferreira.

## Navigation

- [README.md](./README.md): Primary developer documentation, functional/non-functional requirements, and workspace index.
- [.agents/plugins.json](./.agents/plugins.json): Antigravity plugin registry importing domain plugins from `@vitoria-rodrigues/agent-mesh`.
- [app/AGENTS.md](./app/AGENTS.md): Frontend clinic management workspace (`@vitoria-rodrigues/lumini-app`).
- [docs/AGENTS.md](./docs/AGENTS.md): Docusaurus technical documentation portal (`@vitoria-rodrigues/lumini-docs`).
- [supabase/AGENTS.md](./supabase/AGENTS.md): PostgreSQL schemas, migrations, and Deno Edge Functions (`@vitoria-rodrigues/lumini-supabase`).

## Architecture

`Lumini-Estetica` is a Turborepo + pnpm monorepo (`catalogMode: strict`) partitioned into three sovereign workspaces:

- **`app/` (`@vitoria-rodrigues/lumini-app`)**: React 19, TypeScript 6, Vite 8, TanStack Query, Zod, Stripe, and Supabase client application.
- **`docs/` (`@vitoria-rodrigues/lumini-docs`)**: Docusaurus 3.10 MDX v3 portal structured under the Diátaxis framework.
- **`supabase/` (`@vitoria-rodrigues/lumini-supabase`)**: PostgreSQL database migrations, Row-Level Security (RLS) policies, and Deno Edge Functions.

## Scoped Guardrails

- MUST maintain a strict senior, objective, and technical tone across all communications, documentation, and code.
- MUST conduct conversational chat responses in Brazilian Portuguese (pt-BR) while keeping all code, configuration files, commit messages, `AGENTS.md`, and `README.md` files in English (en-US). End-user clinical portal documentation inside `docs/docs/` follows its configured Docusaurus locale.
- MUST NOT use emojis anywhere in code, markdown headers, body text, commit messages, or chat responses (Zero-Emoji Invariant).
- MUST align all implementations strictly with the business rules, RBAC profiles (Admin, Attendant, Specialist), FR01-FR09, and NFR01-NFR04 documented in [README.md](./README.md).
- MUST use `pnpm` exclusively and consume all shared dependencies via `catalog:` entries in [pnpm-workspace.yaml](./pnpm-workspace.yaml).
- MUST consume `@vitoria-rodrigues/agent-mesh` solely via `catalog:plugins-stack` and `.agents/plugins.json` without duplicating local skills or rules inside `.agents/`.
- MUST maintain `app/.env.example` synchronized with `app/.env` keys using `<YOUR_VARIABLE_NAME>` placeholders and zero plaintext secrets.
- MUST use Conventional Commits v1.0.0 (`<type>(<scope>): <description>`) and sign commits with SSH (`git commit -S -m "..."`) when `user.signingkey` is configured.
- MUST use relative paths for all Markdown links inside repository files.

## Required Skills

When operating in this monorepo, agents MUST activate the relevant `@vitoria-rodrigues/agent-mesh` skill:

- **`router-architect`**: Active when authoring or auditing any `AGENTS.md` context router.
- **`readme-architect`**: Active when creating or updating any `README.md` documentation.
- **`monorepo-architect`**: Active when auditing `pnpm-workspace.yaml` catalogs, `turbo.json`, `tsconfig*.json`, or `package.json` manifests.
- **`docusaurus-architect`, `docusaurus-mdx-architect`, `docusaurus-auditor`**: Active when authoring or validating documentation inside `docs/`.
- **`github-flow-operator`**: Active when managing branches, commits, pull requests, or CI/CD workflows.
