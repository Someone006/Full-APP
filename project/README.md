# Project workspace

This directory is the shared project memory for the development process that built this SaaS.
It is **development-time material only**. Nothing in `project/` is loaded, imported, or required by
the running application. The application must operate if this directory is deleted.

## Process

Research → Validate → Define → Plan → Design → Architect → Build → Secure → Test → Review → Deploy

Every stage follows: single responsibility → artifact → independent judge → revision if necessary →
approval → next stage.

## Layout

| Directory | Owner (single responsibility) |
|---|---|
| `research/` | Agent 1 — SaaS Opportunity Researcher; Agent 2 — Market & Competitive Validation (separate files) |
| `strategy/` | Agent 3 — SaaS Strategy |
| `requirements/` | Agent 4 — Requirements |
| `website/` | Agent 5 — Website Planning |
| `sales/` | Agent 6 — Sales & Pricing |
| `marketing/` | Agent 7 — Marketing |
| `design/` | Agent 8 — UI/UX |
| `architecture/` | Agent 9 — Software Architecture |
| `database/` | Agent 10 — Database (design notes; schema lives in `prisma/`) |
| `backend/` | Agent 11 — Backend (notes; code lives in `src/server/`) |
| `frontend/` | Agent 12 — Frontend (notes; code lives in `src/app/`, `src/components/`) |
| `security/` | Agent 13 — Security |
| `legal/` | Agent 14 — Legal & Privacy |
| `accessibility/` | Agent 15 — Accessibility |
| `qa/` | Agent 16 — QA & Testing |
| `devops/` | Agent 17 — DevOps & Reliability |
| `documentation/` | Agent 18 — Documentation (notes; user-facing docs live in `docs/`) |
| `runtime-independence/` | Agent 19 — Runtime Independence |
| `reviews/` | Agent 20 — Final Review |
| `judges/` | One independent judge per agent; verdicts are append-only |
| `decisions/` | Orchestrator — decision registry |
| `assumptions/` | Orchestrator — assumption registry |
| `risks/` | Orchestrator — risk register |
| `conflicts/` | Orchestrator — conflict reports |
| `changes/` | Orchestrator — change requests |
| `release/` | Orchestrator — gate log, release checklist, final report |

## Registries

- [Decision registry](decisions/DECISIONS.md)
- [Assumption registry](assumptions/ASSUMPTIONS.md)
- [Risk register](risks/RISKS.md)
- [Business & jurisdiction configuration](decisions/BUSINESS_CONFIG.md)
- [Gate log](release/GATES.md)
- [Orchestrator log](release/ORCHESTRATOR_LOG.md)
