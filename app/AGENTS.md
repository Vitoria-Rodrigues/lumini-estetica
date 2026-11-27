<context-hierarchy>
  <parent src="../AGENTS.md" type="global-rules" />
  <system-instruction>
    AGENT: You are operating in the app bounded context (@vitoria-rodrigues/lumini-app) of Lumini-Estetica. If you have not read "../AGENTS.md" in this session, stop now and read it using your file-reading tools before proceeding.
  </system-instruction>
</context-hierarchy>

# App Workspace Context (`@vitoria-rodrigues/lumini-app`)

This document serves as the bounded context router (Layer 2) for the `app/` workspace of **Lumini Estética**, created by Vitória Rodrigues Ferreira.

## Navigation

- [README.md](./README.md): App workspace documentation, scripts, and environment setup.
- [package.json](./package.json): Workspace manifest (`@vitoria-rodrigues/lumini-app`) consuming `catalog:web-stack` and `catalog:shared-stack`.
- [.env.example](./.env.example): Authoritative environment configuration template for Supabase and Stripe client keys.

## Architecture

- **Framework & Bundler**: React 19, TypeScript 6 (`tsc -b && vite build`), and Vite 8 (`@vitejs/plugin-react-swc`).
- **State & Validation**: TanStack Query (`@tanstack/react-query`), React Router DOM, and Zod payload validation schemas.
- **Integrations**: Supabase JS client (`@supabase/supabase-js`) for PostgreSQL/Auth/RBAC and Stripe (`@stripe/react-stripe-js`, `@stripe/stripe-js`) for checkout workflows.

## Scoped Guardrails

- MUST align all components, hooks, schemas, and state logic with the business rules and RBAC matrix in [../README.md](../README.md).
- MUST enforce Role-Based Access Control across UI routes and API calls for `Admin`, `Attendant`, and `Specialist` roles.
- MUST NEVER implement hard-deletes for `Client` or `Procedure` records with linked consultations; always apply logical deletion/archiving (NFR04).
- MUST keep [.env.example](./.env.example) synchronized with `.env` keys without ever committing plaintext credentials.
- MUST verify `pnpm app:typecheck`, `pnpm app:lint`, and `pnpm app:build` pass after code changes.

## Required Skills

- **`monorepo-architect`**: Active when modifying `package.json` or TypeScript project references.
- **`browser-auditor`**: Active when testing live application flows and UI state in a browser.
- **`readme-architect`**: Active when updating [README.md](./README.md).
