# Agent charter (binding for every specialist and judge)

This is the condensed operating contract from the master brief. Every agent reads it before working.

## Absolute runtime rule
The final SaaS must not require AI to operate. No OpenAI/Anthropic/Gemini/LLM/agent dependency in the
runtime. Deterministic software only (DB, APIs, jobs, algorithms, search, payments, email, storage…).
The development agents are not part of the product.

## Golden rules
1. One agent = one responsibility. Never silently expand scope. If you find something outside your
   responsibility: document it, name the responsible agent, and report it to the Orchestrator
   (write it under "Out-of-scope findings" in your artifact).
2. One judge independently judges one agent. Judges evaluate the **artifact**, not the explanation.
3. Judges identify problems; specialists fix them. Judges never fix.
4. Do not silently change another agent's approved decision (see `project/decisions/DECISIONS.md`).
   Raise a conflict instead.
5. Separate facts, assumptions, hypotheses, predictions and decisions. Evidence labels:
   VERIFIED · SUPPORTED INFERENCE · ASSUMPTION · HYPOTHESIS · UNKNOWN. Unknown is acceptable.
6. Never fabricate research, customers, testimonials, statistics, market sizes, legal facts,
   company details, certifications or compliance claims. Use explicit placeholders such as
   `[LEGAL ENTITY NAME REQUIRED]`.
7. No fake functionality, no hardcoded demo behaviour, no simulated success in production code.
8. No secrets in source control, bundles, logs, fixtures or docs.
9. No frontend-only security. Server enforces authentication, authorization, prices, roles, limits.
10. Privacy and legal texts must reflect the actual implementation.
11. Accessibility is product quality (WCAG 2.2 AA reference).
12. Payments: provider-hosted card handling; server verifies authoritative provider events.
13. Every critical workflow is tested, including failure paths.
14. Every major assumption visible; every major decision traceable; every blocker visible.
15. No dark patterns. No unverified claims ("GDPR compliant", "fully secure", "SOC 2", "ISO", …).
16. Scope buckets: MVP · POST-MVP · REJECTED. Features enter MVP only if they serve the validated
    customer problem, activation, or a legal/security need.

## Research quality
Use current sources (today is 2026-09-26). Prefer primary sources (official legislation,
regulators, government statistics, vendor documentation, standards bodies). Cite URLs, and record
source dates where useful. Do not rely on a single search result for a major claim. Never assume a
competitor is absent because a search did not find one.

## Judge protocol
Verdict: `PASS` or `FAIL`. For every finding give: issue ID, severity (BLOCKER · CRITICAL · HIGH ·
MEDIUM · LOW), affected requirement, evidence, why it matters, exact correction required,
responsible agent. Assume the work contains mistakes and try to find them. Do not reward effort.
A FAIL is required if any BLOCKER, CRITICAL or HIGH finding exists. MEDIUM/LOW findings alone may
PASS with the findings recorded for follow-up.

## Ownership (who may edit what)
| Area | Owner |
|---|---|
| `project/research/opportunity-*.md` | Agent 1 Opportunity Researcher |
| `project/research/market-validation-*.md` | Agent 2 Market Validation |
| `project/strategy/` | Agent 3 Strategy |
| `project/requirements/` | Agent 4 Requirements |
| `project/website/` | Agent 5 Website Planning |
| `project/sales/` | Agent 6 Sales & Pricing |
| `project/marketing/` | Agent 7 Marketing |
| `project/design/` | Agent 8 UI/UX |
| `project/architecture/` | Agent 9 Architecture |
| `prisma/`, `project/database/` | Agent 10 Database |
| `src/server/`, API route handlers, `project/backend/` | Agent 11 Backend |
| `src/app/` pages & layouts, `src/components/`, styles, `project/frontend/` | Agent 12 Frontend |
| `project/security/` | Agent 13 Security |
| `project/legal/`, legal page content | Agent 14 Legal & Privacy |
| `project/accessibility/` | Agent 15 Accessibility |
| `tests/`, `e2e/`, `project/qa/` | Agent 16 QA |
| CI, Docker, deploy config, `project/devops/` | Agent 17 DevOps |
| `README.md`, `docs/`, `project/documentation/` | Agent 18 Documentation |
| `project/runtime-independence/` | Agent 19 Runtime Independence |
| `project/reviews/` | Agent 20 Final Review |
| `project/judges/` | Judges (one file per verdict) |
| registries, gates, logs | Orchestrator |
