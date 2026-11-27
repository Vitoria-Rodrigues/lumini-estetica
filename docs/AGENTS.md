<context-hierarchy>
  <parent src="../AGENTS.md" type="global-rules" />
  <system-instruction>
    AGENT: You are operating in the docs bounded context (@vitoria-rodrigues/lumini-docs) of Lumini-Estetica. If you have not read "../AGENTS.md" in this session, stop now and read it using your file-reading tools before proceeding.
  </system-instruction>
</context-hierarchy>

# Docs Workspace Context (`@vitoria-rodrigues/lumini-docs`)

This document serves as the bounded context router (Layer 2) for the `docs/` documentation portal of **Lumini Estética**, created by Vitória Rodrigues Ferreira.

## Navigation

- [README.md](./README.md): Docusaurus workspace overview, Diátaxis quadrant guide, and build commands.
- [package.json](./package.json): Workspace manifest (`@vitoria-rodrigues/lumini-docs`) consuming `catalog:docs-stack`.

## Architecture

- **Documentation Engine**: Docusaurus 3.10 with `@docusaurus/faster`, Tailwind CSS 4, GSAP, Mermaid, and MDX v3.
- **Taxonomy**: Organized according to the Diátaxis framework (`tutorials/`, `how-to-guides/`, `reference/`, `explanation/`).
- **Tooling**: Custom changelog and roadmap generators (`tooling/generate-changelog.ts`, `tooling/generate-roadmap.ts`) and build orchestration (`scripts/docs-build.ts`).

## Scoped Guardrails

- MUST align all documented requirements, roles, and architectures with [../README.md](../README.md).
- MUST strictly enforce MDX v3 compatibility (trailing slashes on self-closing JSX tags, `{/* ... */}` comments, explicit code fence language identifiers).
- MUST NOT create `AGENTS.md` or boilerplate `README.md` files inside Diátaxis content quadrant subdirectories (3-Layer Ceiling).
- MUST verify `pnpm docs:typecheck`, `pnpm docs:lint`, and `pnpm docs:build` pass after documentation edits.

## Required Skills

- **`docusaurus-architect`**: Active when designing or organizing Diátaxis hierarchies and `_category_.json` metadata.
- **`docusaurus-mdx-architect`**: Active when authoring or refactoring `.mdx` documents.
- **`docusaurus-auditor`**: Active when auditing internal links, MDX syntax, or Docusaurus builds.
- **`readme-architect`**: Active when updating [README.md](./README.md).
