# Lumini Estética - Supabase Backend (`@vitoria-rodrigues/lumini-supabase`)

> [!NOTE]
> **Project Creator**: Vitória Rodrigues Ferreira
> **Tech Stack**: Supabase, PostgreSQL, Deno, TypeScript

This workspace houses the PostgreSQL database architecture, Row-Level Security (RLS) migrations, and Deno Edge Functions powering **Lumini Estética**.

---

## 1. Directory Structure

- **`migrations/`**: SQL files defining PostgreSQL tables, constraints, and RLS policies.
- **`functions/`**: TypeScript Deno Edge Functions handling server-side workflows and Stripe webhooks.
- **`config.toml`**: Supabase CLI configuration for local development and remote project linking.

---

## 2. Building and Running

Managed via the Supabase CLI and automated deployment defined in [../.github/workflows/deploy-supabase.yaml](../.github/workflows/deploy-supabase.yaml):

| Command | Description |
| :--- | :--- |
| `pnpm --filter "@vitoria-rodrigues/lumini-supabase" types:generate` | Generates `types.ts` from the local Supabase PostgreSQL schema. |
