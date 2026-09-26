# Build-environment facts (Orchestrator)

Observed facts about the development environment used for this build, recorded so downstream
agents can judge feasibility and testability. These are not product decisions.

| ID | Fact | Evidence | Date |
|---|---|---|---|
| ENV-001 | Node.js v22.22.2, npm 10.9.7, pnpm available | `node --version`, `npm --version` | 2026-09-26 |
| ENV-002 | PostgreSQL 16.13 server runs locally (port 5432) | `pg_lsclusters`, `select version()` | 2026-09-26 |
| ENV-003 | npm registry reachable | `npm view` succeeded | 2026-09-26 |
| ENV-004 | Chromium + Playwright preinstalled (`/opt/pw-browsers`) for E2E testing | environment documentation | 2026-09-26 |
| ENV-005 | OSV API (`POST https://api.osv.dev/v1/query`) reachable and returns advisories (queried `pkg:npm/lodash@4.17.20` → GHSA-29mw-wpgm-hmr9) | curl | 2026-09-26 |
| ENV-006 | ENISA EUVD API (`https://euvdservices.enisa.europa.eu/api/lastvulnerabilities`) reachable, HTTP 200 | curl | 2026-09-26 |
| ENV-007 | Stripe API host reachable (HTTP 401 without key — expected). No Stripe account/keys are available in this session. | curl | 2026-09-26 |
| ENV-008 | No SMTP provider credentials available in this session | — | 2026-09-26 |
| ENV-009 | Docker CLI present; daemon not verified | `docker info` | 2026-09-26 |
| ENV-010 | Repository started empty (no existing code) | `git status` | 2026-09-26 |
| ENV-011 | CISA KEV JSON feed reachable; catalogVersion 2026.09.25, 1,726 entries (imported from Strategy S3-C1) | Agent 3 check | 2026-09-26 |
| ENV-012 | OSV per-ecosystem bulk exports (`osv-vulnerabilities.storage.googleapis.com/<eco>/all.zip`) reachable for npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems, Packagist; npm export ≈217 MB compressed (S3-C2) | Agent 3 check | 2026-09-26 |
| ENV-013 | `npm sbom` produces CycloneDX 1.5 and SPDX 2.3 JSON with a purl on every component (S3-C3) | Agent 3 check | 2026-09-26 |
| ENV-014 | OSV `POST /v1/querybatch` returns real advisories for SBOM purls (S3-C4) | Agent 3 check | 2026-09-26 |
| ENV-015 | GOV.UK bank-holidays JSON reachable (S3-C6) | Agent 3 check | 2026-09-26 |
