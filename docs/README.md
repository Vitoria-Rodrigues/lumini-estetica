# Lumini Estética - Docs Workspace (`@vitoria-rodrigues/lumini-docs`)

> [!NOTE]
> **Project Creator**: Vitória Rodrigues Ferreira
> **Tech Stack**: Docusaurus 3.10, MDX v3, React 19, Tailwind CSS 4, Mermaid

This workspace contains the unified documentation portal for the **Lumini Estética** management system, structured according to the Diátaxis documentation framework.

---

## 1. Documentation Taxonomy

- **`tutorials/`**: Learning-oriented step-by-step onboarding guides.
- **`how-to-guides/`**: Task-oriented operational recipes.
- **`reference/`**: Technical schemas, specifications, and architectural catalogs.
- **`explanation/`**: Architectural rationale and domain background.

---

## 2. Building and Running

Execute from the monorepo root using pnpm and Turborepo:

| Command | Description |
| :--- | :--- |
| `pnpm docs:dev` | Starts the Docusaurus development server on port `3002`. |
| `pnpm docs:build` | Runs `tsx scripts/docs-build.ts` to produce static documentation assets. |
| `pnpm docs:typecheck` | Runs TypeScript validation (`tsc -b`). |
| `pnpm docs:lint` | Runs ESLint and MDX v3 checks across documentation sources. |
| `pnpm docs:down` | Frees port `3002` if a local server process remains active. |
| `pnpm --filter "@vitoria-rodrigues/lumini-docs" generate:changelog` | Regenerates changelog artifacts. |
| `pnpm --filter "@vitoria-rodrigues/lumini-docs" generate:roadmap` | Regenerates roadmap artifacts. |
