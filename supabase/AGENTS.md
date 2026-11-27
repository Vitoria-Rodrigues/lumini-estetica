<context-hierarchy>
  <parent src="../AGENTS.md" type="global-rules" />
  <system-instruction>
    AGENT: You are operating in the supabase bounded context (@vitoria-rodrigues/lumini-supabase) of Lumini-Estetica. If you have not read "../AGENTS.md" in this session, stop now and read it using your file-reading tools before proceeding.
  </system-instruction>
</context-hierarchy>

# Supabase Workspace Context (`@vitoria-rodrigues/lumini-supabase`)

This document serves as the bounded context router (Layer 2) for the `supabase/` backend workspace of **Lumini Estética**, created by Vitória Rodrigues Ferreira.

## Navigation

- [README.md](./README.md): Database migrations, Deno Edge Functions, and Supabase CLI commands.
- [package.json](./package.json): Workspace manifest (`@vitoria-rodrigues/lumini-supabase`) with `types:generate` script.

## Architecture

- **`migrations/`**: PostgreSQL schema definitions, foreign key constraints, and Row-Level Security (RLS) policies enforcing Admin, Attendant, and Specialist RBAC.
- **`functions/`**: TypeScript Deno Edge Functions handling server-side business logic and Stripe payment lifecycle webhooks.
- **`config.toml`**: Local Supabase CLI runtime configuration.

## Scoped Guardrails

- MUST align all database schemas, RLS policies, and Edge Functions with the business rules and data protection constraints in [../README.md](../README.md).
- MUST protect sensitive client fields (such as CPF) and enforce logical deletion/archiving for `Client` and `Procedure` records with consultation history (NFR01, NFR04).
- MUST regenerate TypeScript database types via `pnpm --filter @vitoria-rodrigues/lumini-supabase types:generate` whenever migrations change.

## Required Skills

- **`router-architect`**: Active when auditing bounded context alignment.
- **`readme-architect`**: Active when updating [README.md](./README.md).
- **`github-flow-operator`**: Active when maintaining [.github/workflows/deploy-supabase.yaml](../.github/workflows/deploy-supabase.yaml).
