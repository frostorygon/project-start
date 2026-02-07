# project-start 🚀 (WIP)

Opinionated full-stack starter template for rapid project deployment.

## Stack
- **Frontend:** TanStack Router + React + Shadcn/UI + Tailwind v4
- **Backend:** Convex (real-time DB + serverless functions)
- **Auth:** WorkOS
- **Deploy:** Cloudflare Pages + GitHub Actions

## Structure
```
apps/web/            ← TanStack Router app
convex/              ← Shared backend (all apps use same API)
packages/shared/     ← Types, Zod validators
.github/workflows/   ← CI/CD
docs/                ← Project planning docs (templates)
```

## Workflow (How to start a new project)
1. **Discovery** — Talk to AI, dump moodboard/references, clarify scope
2. **Docs** — AI generates `DATA_SCHEMA.md`, `API_ENDPOINTS.md`, `SITEMAP_UI_LOGIC.md`
3. **Design** — Use Stitch to generate UI screens from docs + moodboard
4. **Build** — Clone this template, copy docs in, start coding

## Docs (Templates)
- `docs/ARCHITECTURE.md` — Stack & system overview
- `docs/API_ENDPOINTS.md` — Convex queries, mutations, actions
- `docs/DATA_SCHEMA.md` — Table definitions
- `docs/SITEMAP_UI_LOGIC.md` — Routes, screens, components
- `docs/IMPLEMENTATION_CHECKLIST.md` — Phase-based build checklist

## Status
🚧 **WIP** — Skeleton only. Scaffolding coming soon.
