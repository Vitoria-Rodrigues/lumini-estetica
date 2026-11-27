# Lumini Estética - App Workspace (`@vitoria-rodrigues/lumini-app`)

> [!NOTE]
> **Project Creator**: Vitória Rodrigues Ferreira
> **Tech Stack**: React 19, TypeScript 6, Vite 8, TanStack Query, Zod, Supabase, Stripe

This workspace contains the frontend clinic management application for Lumini Estética, delivering the centralized operational interface defined in the root [README.md](../README.md).

---

## 1. Key Modules

- **Authentication & RBAC**: Login and route protection across `Admin`, `Attendant`, and `Specialist` roles.
- **Client & Employee Management**: CRUD workflows enforcing data protection for sensitive records (such as CPF).
- **Procedures Catalog**: Classification of procedures into `Facial` and `Corporal` domains.
- **Scheduling & Agenda**: Consultation lifecycle tracking (`scheduled`, `performed`, `canceled`) with logical deletion/archiving to preserve referential integrity.
- **Financial Module**: Transaction tracking and Stripe payment integration.

---

## 2. Configuration

Copy [.env.example](./.env.example) to `.env` before running locally:

| Variable | Required | Description |
| :--- | :--- | :--- |
| `VITE_SUPABASE_URL` | Yes | Public Supabase project URL. |
| `VITE_SUPABASE_ANON_KEY` | Yes | Public Supabase anonymous API key. |
| `VITE_STRIPE_PUBLIC_KEY` | Yes | Stripe publishable API key. |

---

## 3. Building and Running

Execute from the monorepo root or inside `app/`:

| Command | Description |
| :--- | :--- |
| `pnpm app:dev` | Starts the Vite development server with HMR. |
| `pnpm app:build` | Compiles TypeScript (`tsc -b`) and bundles production assets. |
| `pnpm app:typecheck` | Runs strict TypeScript validation (`tsc -b`). |
| `pnpm app:lint` | Runs ESLint across application source files. |
| `pnpm --filter "@vitoria-rodrigues/lumini-app" preview` | Previews the production build locally. |
