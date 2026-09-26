# Market & Competitive Validation — v2

| Field | Value |
|---|---|
| Artifact | `project/research/market-validation-v2.md` |
| Supersedes | `project/research/market-validation-v1.md` (frozen; judged FAIL by Judge 2, `project/judges/judge-02-market-validation-v1.md`, findings J2-001 … J2-008) |
| Owner | Agent 2 — Market & Competitive Validation |
| Research date | 2026-09-26. Every price, status and capability is "as seen on 2026-09-26" unless a source date is given. |
| Status | DRAFT v2 — resubmitted for independent judging |
| Input (approved) | `project/research/opportunity-research-v2.md` (Agent 1, APPROVED); open finding **J1-013** forwarded to Agent 2 (resolved in §2.0) |
| Candidates | **O1** EU CRA vulnerability-handling / Art. 14 reporting-clock and evidence workspace for SBOM-capable software-product SMEs · **O2** Great Britain holiday-record and holiday-pay assurance for variable-hours employers · **O4** EU Pay Transparency compliance for SME / lower-mid-market employers in a transposed jurisdiction (conditional) · O3 Awaab's Law (watchlist check only) |
| Out of scope | Choosing the winner, product strategy, pricing, requirements, building anything. No numerical market scores are given. |

**What changed from v1 (summary; details in §11 Revision log).** O2's direct competitor paiyroll was re-read in full: it publishes a 104-week lookback, 104-week historic import, pay-item selection, XLSX calculation reports described as "a complete audit trail", integrations with Xero, Sage 50, BrightPay and Moneysoft, bureau payroll tiers (£50/£75/£100 per month), a free Holiday Pay Compliance Check, and vendor-selected customer stories. KeyPay's behaviour is restated accurately (a rate floor and a missing-data notification, not a gap). O1's competitor overlap is restated function by function, using only published prices and claims. One explicit under-service standard (§1.4) is now applied to both candidates. Quotations were re-checked verbatim; ESTIMATE and PREDICTION labels are removed; the dropped Agent 1 questions are answered or carried forward.

### Evidence labels (charter set only) and grades

| Label | Meaning here |
|---|---|
| **VERIFIED [n]** | Stated by the cited source. The source was **Read** in this session (fetched page, or PDF/XHTML/HTML extracted locally), or at least **two independent snippets** agree. Snippet-only claims are always marked "(snippet)". |
| **SUPPORTED INFERENCE** | My reasoning (including arithmetic) from verified facts; the reasoning is stated. |
| **ASSUMPTION** | Taken as true without evidence; must be tested. |
| **HYPOTHESIS** | Testable proposition about customers, demand or behaviour. |
| **UNKNOWN** | Not established. Statements about **future events** (e.g., a law being adopted) are labelled UNKNOWN (future event), with any stated plan cited as VERIFIED. |

Source grades in §9: **P** primary/official (legislation, regulator, government, a product's own documentation of its own features), **S** reputable secondary (law firm, professional body, trade press, independent directory), **V** vendor marketing page. A V page can verify a *published price* or *what a vendor claims*; it never verifies a legal fact or a market-level fact. Customer stories on a vendor's own site are graded V and described as "vendor-selected". "[A1 n]" means source *n* of Agent 1's approved v2, not re-read by me.

**Quotation rule.** Text inside quotation marks is verbatim from the cited source, with omissions shown as "…". Everything else is paraphrase.

No customer, statistic, price or quote in this artifact is invented. No customer interviews, surveys or pricing tests were possible in this session.

---

## 1. Scope & method

### 1.1 Scope
For each of O1, O2 and O4: (1) competitor matrix, (2) alternatives and substitutes, (3) pricing evidence, (4) market and demand evidence, (5) complaints and feature gaps, (6) differentiation opportunities, (7) switching costs, saturation and acquisition, (8) risks and weaknesses, (9) open validation questions, (10) assumptions. Also the candidate-specific questions in the assignment, a cross-candidate evidence comparison (§6), an evidence-quality summary (§7), open unknowns (§8), sources (§9), out-of-scope findings (§10) and the revision log (§11). O3 was checked only for decisive new evidence (§5).

### 1.2 Method
- **Search angles for every candidate:** vendor category queries; "alternatives to X"; vendor pricing pages (read directly); directories and review sites (Cyber Vendor Guide, Capterra, G2, effy.ai list); product-idea boards and forums (Xero Product Ideas, Sage Community Hub, QuickBooks Community, Hacker News); GitHub repository and issue search (GitHub API, 2026-09-26); regulator and government pages; Italian-language queries for O4.
- **Primary documents read locally:** CRA OJ text (Arts. 14–16 and 33) via `publications.europa.eu/resource/celex/32024R2847`; ENISA *CRA SRP Glossary v1.3* (HTML table parsed); ENISA SRP FAQ (HTML); ENISA *SME CRA Survey Report* (PDF); ENISA *SBOM Adoption State of Play 2026* (PDF); EUVD public API/FAQ documentation; DBT *Make Work Pay: Holiday Pay Compliance and Enforcement* consultation (PDF); GOV.UK FWA delivery plan (HTML and content API); ISTAT census report (PDF).
- **Verbatim re-reads for v2 (curl + local text extraction):** paiyroll holiday-pay companion, bureau pricing, customer stories, free compliance checker, free template and payroll-audit pages; KeyPay 52-week averaging; Staffology average-holiday-pay settings; Xero Product Ideas thread (all comments with authors and dates); Sage 50 KB article; CVD Portal home and pricing; ConformOps home, pricing and "AI info"; CRA Evidence platform; Kunnus home; SPDX CVE terms of use; SaM Solutions CRA article.
- Competitors were found by searching for them. Lists are **not exhaustive**; a failed search is never treated as proof of absence.

### 1.3 Limitations
- **No primary customer research.** All demand statements about segments are HYPOTHESES until tested.
- Pages not reachable: AccountingWEB "Any Answers" (403), Crowell & Moring (403), BrightPay support hub (403), IT Security Guru (403), Altalex (login), AlternativeTo (403), Trustpilot (403), ENISA glossary URL `…/cra-srp-glossary` (403; `…/cra-srp-glossary2` worked), Personio pricing and product pages (HTTP 429 rate limit), nvd.nist.gov (JavaScript-only; read via ScanCode's reproduction).
- **Reddit** threads did not surface through the search tool. Absence of Reddit evidence is not evidence of absence.
- Vendor pages are self-descriptions. No CRA vendor publishes customer counts; paiyroll publishes vendor-selected stories only.
- National-language coverage: Italian sampled for O4; German, Spanish and French not sampled.

### 1.4 One standard for "evidence the target segment is underserved" (applies to O1, O2, O4)
To remove the J1-013 asymmetry, every candidate is assessed on the same three questions, and the §6 rating is built from them:
1. **Incumbent and free-tool gaps** — are gaps in the tools customers already use documented by primary sources (product documentation, regulator statements, user forums)?
2. **Published SME-priced direct competitors** — does any offer with a *published* SME price *claim* to cover the core job functions listed for that candidate? Unpriced offers are listed separately and are not counted as "SME-priced".
3. **Traction** — is there evidence that customers pay for those offers? Vendor-selected stories count as weak evidence; independent reviews or published counts count as stronger evidence.

Under-service is **not** treated as "contradicted" by V-grade claims alone, because a V page shows only what a vendor claims.

---

## 2. O1 — EU CRA vulnerability-handling, Art. 14 reporting-clock and evidence workspace

### 2.0 Resolution of forwarded finding J1-013

**(a) Segment wording — "already produce" vs "can export" SBOMs.**

| Evidence | What it shows | Label |
|---|---|---|
| ENISA SME CRA survey (n=194; fieldwork Feb–Mar 2026). Q3.3 "technical practices or standards … you currently implement": SBOM 67 (34.54%); "None" 21 (10.82%); no answer 20 (10.31%). Roles (multi-select): software developer 80 (41.24%), service provider/integrator 53 (27.32%), product manufacturer 39 (20.10%), importer/distributor 33 (17.01%) [8] | Whole-sample SME figure over all 194 responses, including non-answers. I found **no role-by-practice cross-tabulation** in the report text. | VERIFIED [8]; cross-tab UNKNOWN |
| ENISA *SBOM Adoption State of Play 2026* (n=334, end-2025; >65% large firms; micro+small 16%): "10 % of the respondents do not generate SBOMs at all"; manual processes ~11% overall, 16% in micro; formats CycloneDX 44%, SPDX 29%, no standard 11%, proprietary 17%; micro 23% and small 25% "mature" vs medium 4% and large 6% [9] | Large-firm-heavy. For micro respondents the second-most common engagement was "providing SBOM tools, solutions and/or integration services", so the micro subsample includes SBOM vendors and is not representative of CRA-affected SMEs. | VERIFIED [9]; caveat SUPPORTED INFERENCE |
| Linux Foundation Research 2026: "The share of respondents producing Software Bill of Materials (SBOMs) for all products held at 32%" [10] | Open-source-ecosystem sample, not SME-specific; sample size not stated in the blog. | VERIFIED [10] (S) |
| GitHub exports an SPDX 2.3 SBOM from the dependency graph via UI or REST API [13] | Exporting is available without extra tooling for package-managed code on GitHub; completeness is not assured (62% of ENISA SBOM respondents rate completeness "quite a lot or extremely difficult") [9]. | VERIFIED [13][9] |

**Conclusion.** About one third of *surveyed organisations* report producing or implementing SBOMs (34.54% of all SME respondents [8]; 32% "for all products" [10]). The share among **CRA-relevant software-product SMEs** is **UNKNOWN**; both figures are whole-sample proxies (SUPPORTED INFERENCE on the proxy; population share UNKNOWN). "Can export" is larger (any package-managed product can emit an SBOM with free tooling [13]), but its size is **UNKNOWN** because the share of package-managed vs firmware/embedded products is unmeasured (Agent 1's A-19 remains UNKNOWN).

**Recommended single segment definition (for Agent 3 to adopt or reject):** *"EU-market software-product SMEs — software developers, and connected-device makers whose application layer is package-managed — whose build tooling can export CycloneDX or SPDX SBOMs."* Track two sub-segments in validation:
- **S1 — already producing SBOMs** (proxy: about one third of surveyed SMEs, all roles; true share UNKNOWN).
- **S2 — can export but not yet producing** (size UNKNOWN). The MVP can serve S2 only after an SBOM-generation step is added (e.g., GitHub export or an SBOM GitHub Action [13]). This is onboarding friction, not a solved problem.

**(b) Criterion (c) "evidence the segment is underserved", with the §1.4 standard.** The O1 core job has six functions: **F1** SBOM-based component-to-advisory matching; **F2** actively-exploited trigger (KEV or equivalent flag); **F3** Art. 14 clocks from the awareness time; **F4** SRP-aligned notification drafts; **F5** Art. 14(8) user notification or machine-readable advisories (e.g., CSAF); **F6** evidence retention / audit trail. §2.1a maps each vendor's *published* claims to F1–F6.
1. *Gaps in incumbent and free tools* (documented): Dependency-Track covers F1 and F2 but no Art. 14 clock or SRP draft was found in its release notes [39]; the SRP has no API [3]; SME demand for compliance tools is high (68.04%) [8]. Moderate evidence.
2. *Published SME-priced direct competitors*: **CVD Portal** Reporting (€99/month billed annually) claims F2–F6, but its "Automated SBOM ↔ CVE supply chain alerts" appear only in the quote-only Enterprise tier, so F1 at €99 is limited to an SBOM registry plus NVD/EUVD feeds [24]. **ConformOps** Continuous (€79/month per product) claims F1, F3 and F6 [22]. **Article 14 Ready** (free compiler; €79 dry run) claims F3 and F4 without persistence by design [23]. No published SME-priced offer found claims all six functions. **CRA Evidence** and **Kunnus** claim most functions but publish no price [25][26].
3. *Traction*: no O1 vendor publishes customer counts, named customer stories or independent reviews (Kunnus: 0 Capterra reviews) [26]. UNKNOWN.

**Result (SUPPORTED INFERENCE).** Evidence of under-service is **Weak–Moderate**: tool gaps and stated SME demand are documented, and 2–3 SME-priced offers claim overlapping Art. 14 functions, none publishing all six; traction is UNKNOWN. v1's wording ("contradicted"; "several paid SME-priced tools claim to [combine all functions]") overstated the overlap and is withdrawn. The same standard applied to O2 is in §3.0(b). The ranking decision belongs to Agent 3. Agent 1's switch condition ("if SBOM-capable software SMEs will not pay more than free tooling plus the €79–€99 one-off offers, O2 should lead") remains untested because no pricing interviews were possible.

**(c) Competitor asymmetry.** ConformOps' €79/month per product and €249/month portfolio plan, and CVD Portal's €99/month Reporting tier, are recorded as direct competitors and price anchors (§2.1, §2.3). paiyroll receives the same treatment for O2 (§3.1).

### 2.1 Competitor matrix (direct)

All prices are as published on 2026-09-26. "Traction" lists only what is published.

| # | Name / URL | Target (as claimed) | Capabilities relevant to O1's job | Published pricing | Hosting / region | Published traction | Grade |
|---|---|---|---|---|---|---|---|
| 1 | **CVD Portal** — cvdportal.com | EU manufacturers, importers, distributors | Free Art. 13 disclosure intake; "Actively exploited vulnerability flagging" (listed in all tiers); Reporting tier adds "Article 14 notification workflow (24h / 72h / 14d)", "SRP-ready submission package", SBOM registry (SPDX / CycloneDX), CVSS, remediation decisions, "CSAF 2.0 advisory export", NVD / EUVD feeds, "Compliance audit trail"; "Automated SBOM ↔ CVE supply chain alerts" and "AI-assisted vulnerability triage" in Enterprise only; "ENISA provides no submission API at this stage. CVD Portal produces an SRP-ready package for one-step manual submission" | Free €0; **Reporting €99/month, billed annually €1,188**; Compliance €299/month (€3,588/yr; 3 products then €99/month each); Enterprise on quote [24] | Homepage: "EU hosted" [24]; Hetzner infrastructure in Germany, operator Porta Regulus B.V. (NL), founded 2026 per [21] | None published | V (read) [24]; S [21] |
| 2 | **ConformOps** — conformops.eu | Small software teams | Reads manifests, lockfiles, CI, SBOMs and security docs from a read-only GitHub App or ZIP; OSV matching by package URL across npm, NuGet, PyPI, Maven, Go, crates.io and others; Continuous tier: "Daily dependency and OSV monitoring" and "Article 14 reporting, history, deltas, refreshed artifacts"; Art. 14 case records that run "the 24-hour early warning, 72-hour notification, and final-report clocks against a recorded awareness time"; "ConformOps never files on your behalf"; optional AI: "OpenAI is the only AI provider. Processing is off by default at workspace and product level" | Free (2 preview products); **€99 per product one-off** (Art. 14 reporting "not included"); **€79/month per product** or €790/year; **€249/month for five products** [22] | Not stated; operator based in Italy per [21] | None published | V (read) [22]; S [21] |
| 3 | **Article 14 Ready** — article14ready.com | Product-security teams preparing Art. 14 reports | Browser-local stage-aware field compiler ("Incident entries stay in this browser"); deadline calculation from awareness time; Markdown/JSON export; aligned to "ENISA's SRP Glossary v1.1, dated 5 September 2026"; not the official SRP and does not submit | Field compiler free per [21] (site wording "one-time purchase" is ambiguous); **"24h Dry Run" €79 excl. VAT** one-off [23] | Operator PEAK Consulting Services GmbH, Mannheim (DE) [21] | None published | V (read) [23]; S [21] |
| 4 | **CRA Evidence** — craevidence.com | Manufacturers, importers, distributors | CycloneDX / SPDX ingest, HBOM, VEX; feeds: "The CVE List (cvelistV5) is refreshed hourly; OSV.dev, CISA KEV, EPSS, and ENISA EUVD are refreshed daily"; 24h/72h/final deadlines with reminders; "Structured payloads for ENISA Single Reporting Platform"; "CSAF advisories Full advisory lifecycle: import, validate, publish"; submission history "Full audit trail" | **Custom** (all plans); 14-day free trial [25] | Not disclosed | None published | V (read) [25] |
| 5 | **Kunnus** — kunnus.tech (Think Ahead Technologies GmbH) | Startups, SMEs, enterprises | Continuous matching of components "against NVD and OSV"; coordinated disclosure, security advisories and reporting to the CSIRT and ENISA via the SRP; SBOM generation; EU DoC | Not published; startup tier text: "Reduced licensing for early stages" [26] | "Built in Germany, hosted exclusively with European providers" [26] | Capterra: 0 reviews [26] | V (read) [26] |
| 6 | **sbomify** — sbomify.com (open-source core) | OSS maintainers (free); mid-size teams | SBOM/CBOM hub; OSV scanning (weekly free, daily paid); Dependency-Track integration; CRA scope screening and CRA Compliance Wizard; no Art. 14 workflow in the plan table | Community $0; **Business $159/month billed annually** (5 products, 200 components); Enterprise custom [27] | Not stated; self-hostable | GitHub repo 60 stars [27] | V (read) [27] |
| 7 | **Regulus** — goregulus.com | Manufacturers, IoT, embedded | Applicability, classification, Annex II/VII templates, vulnerability workflow | Basic **€2,500/yr**; Pro **€15,000/yr**; Enterprise custom; early access [28] | Not disclosed | None | V (read) [28] |
| 8 | **Zealience Z-CMS** — zealience.com | Radio/IoT makers (EN 18031, RED DA, CRA) | CRA gap analysis, vulnerability-handling policy, risk assessment; free CRA templates on GitHub | **€4,000/yr per licence** (1–4), graduated to €1,000/yr (76–100) [29] | Frankfurt (DE) [29] | Templates repo 36 stars [42] | V (read) [29] |
| 9 | **Vulert** — vulert.com | Small dev teams | Manifest/SBOM upload; hourly monitoring; PDF/audit reports; SBOM-export add-on; no Art. 14 workflow found | Pro **$15/month per app** ($13 annual); Growth $25/month; SBOM Export add-on $13/month; 30-day trial [30] | Not stated | None | V (read) [30] |
| 10 | **Aikido Security** — aikido.dev | Developer teams | SCA/SAST/secrets; SBOM and VEX export; CRA content; no Art. 14 workflow found | Developer **$0**; Basic $300/month; Pro $600/month [31] | Not stated | None on pricing page | V (read) [31] |
| 11 | **SBOM Observer** (Bitfront AB, SE) | Software teams | SBOM management; policies mapped to CRA/DORA/NIS2; VEX | Not shown [32] | Not stated | ~10 customer logos [32] | V (read) |
| 12 | **ReARM** (Reliza) | Release governance | SBOM/xBOM per release, findings roll-up, VDR; open-source CE | Pro price not shown [33] | Self-host or managed | None | V (read) |
| 13 | Enterprise / firmware SBOM platforms: **ONEKEY**, **Cybeats**, **Interlynk**, **Anchore**, **Finite State**, **Black Duck**, **Keysight** | Device makers / enterprise | SBOM generation incl. binaries, VEX, vulnerability management | Quote-only [21][36][37] | Various | None published | S [21]; V (snippet) [36][37] |
| 14 | Test/certification/consulting: **pi3g**, **Bureau Veritas**, **DEKRA**, **SGS**, **TÜV SÜD**, **BearingPoint** | Manufacturers needing assessment | Gap assessment, testing, conformity advice | Quote-only [21] | EU labs | None | S [21] |
| 15 | Adjacent: runtime-security vendors repositioned as CRA tools (EdgeLabs list: Sysdig, Aqua/Trivy — Trivy free, Falco, etc.) [38]; **Distr** (software-distribution platform, Pro $80/month; CRA content only) [34]; AI-centric **UnitOne** (Team $99/month, snippet) [35] and **cra-agent** (GitHub, "Autonomous agentic AI for CRA", 452 stars) [42] | Various | Adjacent evidence capture or scanning | As stated | Various | Stars only [42] | V [34][38]; V (snippet) [35]; P [42] |

**Traction (all rows).** No CRA vendor publishes a customer count, named customer story or independent review volume. A dominant SME-focused leader is UNKNOWN.

### 2.1a Function coverage of the O1 core job (published claims only)

✓ = claimed on the vendor's own page at the price shown; ◐ = partial or tier-limited; — = not found on the pages read (not proof of absence).

| Offer (published price) | F1 SBOM→advisory matching | F2 exploited trigger | F3 Art. 14 clocks | F4 SRP-aligned drafts | F5 user notification / CSAF | F6 evidence / audit trail | Source |
|---|---|---|---|---|---|---|---|
| CVD Portal Reporting (€99/month, annual) | ◐ SBOM registry + NVD/EUVD feeds; automated SBOM↔CVE alerts Enterprise-only | ✓ | ✓ | ✓ | ✓ (CSAF 2.0 export) | ✓ | [24] |
| ConformOps Continuous (€79/month per product) | ✓ (OSV by package URL) | — | ✓ | — | — | ✓ (case records, history) | [22] |
| Article 14 Ready (free; €79 dry run) | — | — | ✓ | ✓ (glossary v1.1) | — | — (browser-local by design) | [23] |
| sbomify Business ($159/month) | ✓ (OSV) | — | — | — | — | ◐ (SBOM archive) | [27] |
| Dependency-Track (free, Apache-2.0) | ✓ | ✓ (CISA + ENISA EU KEV) | — | — | ◐ (VEX export, not user notices) | ◐ (project history) | [39] |
| *Unpriced:* CRA Evidence | ✓ | ✓ (CISA KEV) | ✓ | ✓ ("Structured payloads…") | ✓ (CSAF) | ✓ | [25] |
| *Unpriced:* Kunnus | ✓ (NVD, OSV) | — | ✓ | ◐ (SRP reporting described) | ◐ (advisories) | ✓ (claimed) | [26] |

SUPPORTED INFERENCE: among offers with a published SME price, **CVD Portal** is the closest overlap with the O1 MVP (five of six functions, F1 limited). ConformOps and Article 14 Ready overlap partially. Two unpriced vendors claim near-complete coverage.

### 2.2 Alternatives and substitutes

| Substitute | Cost | What it covers | Where it breaks (for the O1 job) | Label |
|---|---|---|---|---|
| **OWASP Dependency-Track** (Apache-2.0; 4,238 GitHub stars, 817 forks, 1,041 open issues on 2026-09-26) | Free; self-hosting effort | SBOM ingest and matching; VEX; v5.1.0 (31 Aug 2026) "mirrors the CISA and ENISA EU KEV catalogs out of the box", and KEV status can drive policies and notifications | No Art. 14 clock or SRP packaging found in the release notes; CPE false positives with per-project suppression (issue #5992, open) | VERIFIED [39][40] |
| **ENISA SRP web form + Glossary** | Free (mandatory channel) | Guides every field; later stages "By default copied from previous step, or updated" | No API at initial release; English only; no SBOM matching or evidence retention | VERIFIED [2][3] |
| **GitHub dependency-graph SBOM export** | Free | SPDX 2.3 export via UI/REST; SBOM GitHub Actions | Export only; no triage, clocks or evidence | VERIFIED [13] |
| **Open-source scanners**: Trivy (free) [38]; `crawatch.dev` (free CLI + GitHub Action failing builds on CISA KEV; created 18 Sep 2026); `cra-evidence` (AGPL-3.0; Art. 14 clock and SRP field schema; 0 stars); `CycloneDX.CRA.Validator`; `DX.Comply` (Delphi CycloneDX SBOMs, 56 stars) [42][43] | Free | Fragments of the job | Very low adoption; single maintainers | VERIFIED [38][42][43] |
| **Article 14 Ready free compiler** | Free / €79 dry run | Stage-aware drafting | No SBOM link, no persistence by design | VERIFIED [23] |
| **Templates and guidance**: ENISA helpdesk; Zealience free templates; ORC WG FAQ and learning hub; OpenChain CRA-Compliance framework (18 stars); CVD Portal's "37 fillable CRA templates" (offline packages; price not checked) | Free or low cost | Process templates | Manual | VERIFIED [5][24][42][44] |
| **Spreadsheets + consultants / test labs** | Consultants quote-only [21]; Regulus's calculator assumes €85/h engineering cost (vendor claim) [28] | Anything | Cost; episodic | VERIFIED [21]; [28] is V |
| **Grant-funded services**: SECURE first open call, "up to € 30.000" per SME, €5m call budget, first call closed [12] | Subsidy | CRA compliance activities | Whether SaaS subscriptions are eligible costs is UNKNOWN | VERIFIED [12]; co-financing rate (50%) snippet [12] |

SUPPORTED INFERENCE: no **free** option found combines F1–F6. Among **priced** options, only unpriced vendors claim all six (§2.1a).

### 2.3 Pricing evidence (all published; date seen 2026-09-26)

| Offer | Price | Unit / scope | Source |
|---|---|---|---|
| ConformOps Free / Full Assessment | €0 / €99 once | 2 preview products / per product (Art. 14 reporting not included) | [22] V |
| ConformOps Continuous | €79/month or €790/year | per product | [22] V |
| ConformOps Portfolio | €249/month or €2,490/year | 5 products | [22] V |
| CVD Portal Free / Reporting / Compliance | €0 / €99 per month (billed annually €1,188) / €299 per month (€3,588) | 1 / 3 / 5 members; Compliance: 3 products then €99/month each | [24] V |
| Article 14 Ready "24h Dry Run" | €79 excl. VAT, one-off | 45-minute tabletop exercise | [23] V |
| sbomify Business | $159/month billed annually | 5 products, 200 components | [27] V |
| Regulus Basic / Pro | €2,500 / €15,000 per year | early access | [28] V |
| Zealience Z-CMS | €4,000/yr per licence (1–4) down to €1,000 (76–100) | per product/family | [29] V |
| Vulert Pro / Growth | $15 / $25 per month per app ($13 / $22 annual) | 1 app | [30] V |
| Aikido Developer / Basic / Pro | $0 / $300 / $600 per month | 2 / 10 / 10 users | [31] V |
| CRA Evidence, Kunnus, SBOM Observer, ReARM Pro, ONEKEY, Cybeats, Interlynk, labs | not published | — | [21][25][26][32][33][36] |
| Conformity-assessment engagements | €10,000–30,000 per product family (vendor claim, snippet) | — | [28] V (snippet) |

A Vulert blog snippet quoted $20/$45/$125 plans; the pricing page read on 2026-09-26 shows $15/$25 per app and is used.

### 2.4 Market / demand evidence

| # | Signal | Evidence | Quality |
|---|---|---|---|
| D1 | Legal trigger live | Art. 14(1): a manufacturer "shall notify any actively exploited vulnerability … via the single reporting platform"; ENISA, 11 Sep 2026: "From today, 11 September 2026, manufacturers are required to report actively exploited vulnerabilities" [1][5] | Primary, strong (obligation); not evidence of willingness to pay |
| D2 | SMEs ask for tools — and for money | ENISA SME survey: "Technical tools that help assess compliance" 132/194 (68.04%); vulnerability-handling templates 56%; financial support 142 (73.20%) is "the joint highest figure for any single item in the support needs section alongside support in terms of templates and checklists for required technical documentation"; "Practical templates are the most requested form of support" [8] | Primary, moderate. Cost pressure is real, but a tool-like need (templates) ties for first place, so the WTP signal is mixed, not purely negative |
| D3 | Regulator prefers free, simple support | ENISA: guidance "needs to be easy to use, without requiring companies to rely on additional tools, external support or consultants, and it should be freely accessible" [8] | Primary, strong as a *risk* signal |
| D4 | Low readiness | 36% of micro-companies have no incident-response plan [8]; LF 2026: 66% unfamiliar with the CRA; 41% of manufacturers expect full compliance by Dec 2027 [10] | Primary / secondary; strong for pain, weak for purchase |
| D5 | Tool investment | ENISA SBOM 2026: 43% say the CRA "significantly accelerated" SBOM-tooling investment; 34% invested in tools for vulnerability handling via SBOM [9] | Primary, moderate; large-firm-heavy sample |
| D6 | Developer community | Ask HN "Is anyone else preparing for the EU Cyber Resilience Act?" (~2 Sep 2026): 7 points, 6 comments, mostly vendor replies [41]. GitHub: 114–115 repositories mention "cyber resilience act"; top non-AI community projects have 18–56 stars [42] | Primary, **weak** |
| D7 | Supply-side entry | ≥15 vendors with CRA-specific offers (§2.1), several launched in 2026 [21][24] | Secondary, moderate for *expected* demand; not proof of paid demand |
| D8 | Events | Black Duck webinar "Are you ready: CRA reporting" (snippet) [37]; a Toradex CRA event in Munich mentioned on HN [41]; webinars are the most preferred SME information channel (57%) [8] | Weak–moderate |
| D9 | Enforcement actions | None found (reporting began 11 Sep 2026) | UNKNOWN |
| D10 | Job postings for CRA/product-security roles | Search found none; job boards not searched directly | UNKNOWN |

### 2.5 Customer complaints and feature gaps in existing solutions
- **False positives and per-project suppression** in Dependency-Track: "Currently, Dependency-Track allows marking vulnerabilities as FALSE_POSITIVE only at the project level and for a specific component version" (issue #5992, opened 2 Apr 2026, open) [40]; related CPE-matching false-positive issues #3178, #3268, #3063 (snippet) [40]. VERIFIED (read #5992).
- **SBOM completeness is hard:** 62% rate it "quite a lot or extremely difficult"; 30% cite poor vendor-supplied SBOMs [9]. VERIFIED.
- **Ecosystems without SBOM tooling** (C/C++, embedded, Delphi): the community builds its own generators (e.g., DX.Comply) [42]; Agent 1 documented C/C++ limitations [A1 38]. SUPPORTED INFERENCE.
- **The SRP cannot be automated at launch:** "no Application Programming Interface (API) will be provided at the initial release of the SRP, so notifications must be submitted through the platform interface"; "At launch, the platform will be available in English only" [3]. VERIFIED.
- **No independent reviews** exist for the new CRA tools (Kunnus 0 Capterra reviews) [26]. VERIFIED.
- **Market misinformation:** an IT-services firm's article (27 Feb 2026) states: "SMEs and micro-enterprises cannot be financially sanctioned for failing to meet Article 14 notification deadlines" [92]. The corrigendum only exempts micro and small enterprises from fines for the 24-hour early-warning deadline [A1 3]; other guides say the same (snippets) [92]. This is buyer confusion, not a feature gap. VERIFIED (statement read).

### 2.6 Differentiation opportunities (AI-free, small team)

Could credibly be better (all HYPOTHESES):
1. **All six functions at an SME price.** No published SME-priced offer found claims F1–F6 together (§2.1a). The nearest, CVD Portal Reporting, limits automated SBOM↔CVE alerts to Enterprise [24].
2. **Versioned SRP-glossary schema.** The glossary moved from v1.1 (5 Sep 2026) to v1.3 (25 Sep 2026) in three weeks [2][23]. Stage-by-stage Required/Optional validation with the glossary version recorded is buildable. CVD Portal, CRA Evidence and Article 14 Ready already claim SRP-aligned output, so this is parity plus maintenance discipline, not a moat.
3. **Package-URL-first matching with triage decisions reused across products and versions,** addressing the Dependency-Track #5992 complaint [40]. ConformOps already matches by package URL [22].
4. **Deterministic, AI-free positioning.** ConformOps offers optional OpenAI-based proposals (off by default) [22]; CVD Portal Enterprise lists AI-assisted triage [24]. Whether buyers value "no AI" is UNKNOWN.

Could not credibly be better: binary/firmware SBOM generation; conformity assessment and testing; price (€79–€99/month anchors and free Dependency-Track / Article 14 Ready exist); submission (no SRP API) [3]; breadth (CVD Portal, Kunnus and CRA Evidence already combine Art. 13, Art. 14 and Annex I documentation) [24][25][26].

### 2.7 Switching costs, saturation, acquisition
- **Switching (SUPPORTED INFERENCE):** low for greenfield SMEs (reporting began 11 Sep 2026); moderate for Dependency-Track users (self-hosted history, suppressions).
- **Saturation:** offers with a published SME price that claim an Art. 14 clock: CVD Portal, ConformOps, Article 14 Ready. CRA Evidence and Kunnus claim Art. 14 workflows without published prices. sbomify, Vulert and Aikido are adjacent (monitoring/SBOM without Art. 14 workflows). Saturation of *paying customers* is UNKNOWN.
- **Channels:** SME preferred channels — webinars 57%, EU-level websites 56%, national cybersecurity authority 55%, industry association/cluster 46%; "50 % of respondents are not members of any industry association" [8]. Among CRA-aware respondents, 48% learned of the CRA through developer spaces vs 25% through official EU channels [10]. Small entrants distribute via GitHub Actions (crawatch.dev) [42]. VERIFIED.
- **Acquisition difficulty (SUPPORTED INFERENCE):** high — technical buyers, free alternatives, trust needs for a security-adjacent tool, dense vendor content for "Article 14".

### 2.8 O1-specific questions

**Q1. Do the target SMEs already produce SBOMs (CycloneDX/SPDX), and with what tools?**
- About one third of surveyed organisations: 34.54% of all SME respondents (all roles) [8]; 32% "for all products" in the LF 2026 sample [10]. VERIFIED as whole-sample figures; the share among CRA-relevant software-product SMEs is UNKNOWN (§2.0).
- Formats: CycloneDX 44%, SPDX 29%, no standard format 11%, proprietary 17% [9]. VERIFIED (large-firm-heavy sample).
- Tooling: "33 % of overall SBOM generation relying on open-source tools"; large and medium firms also use commercial tools; manual processes ~11% overall and 16% in micro; 39% generate at build time [9]. VERIFIED.
- Named tools: GitHub dependency-graph export (SPDX 2.3) and SBOM Actions such as the Anchore SBOM Action [13]; Trivy (free) [38]; Aikido (SBOM + VEX export) [31]; Kunnus and CRA Evidence generate SBOMs [25][26]. Tool market shares among SMEs are UNKNOWN.
- BSI TR-03183-2 (cited by ENISA) expects CycloneDX ≥1.6 or SPDX ≥3.0.1 in JSON/XML [9]; an MVP parsing only older versions may fall short of that expectation (SUPPORTED INFERENCE).

**Q2. Vulnerability data sources and licence terms**

| Source | Licence / terms found | Commercial use | Label |
|---|---|---|---|
| OSV.dev sources | GitHub Advisory DB CC-BY 4.0; PyPI CC-BY 4.0; Go CC-BY 4.0; Rust CC0 1.0; Drupal MIT; Global Security Database CC0; OSS-Fuzz CC-BY 4.0; Rocky BSD; AlmaLinux MIT; Haskell CC0; RConsortium Apache 2.0; OpenSSF Malicious Packages Apache 2.0; PSF CC-BY 4.0; Bitnami Apache 2.0; **Ubuntu CC-BY-SA 4.0**; opam CC0; Erlang EEF CNA CC-BY 4.0; converted Debian, Alpine, NVD CVEs for OSS (no licence stated for converted data) [14] | Yes with attribution; Ubuntu adds share-alike | VERIFIED [14] |
| GitHub Advisory Database | "This project is licensed under the terms of the CC-BY 4.0 open source license." The README also points to GitHub's additional-product terms, which I did not read [15] | Yes with attribution | VERIFIED [15] |
| NVD API | Services "are asked to display the following notice prominently within the application: 'This product uses the NVD API but is not endorsed or certified by the NVD.'"; no implied endorsement; modified content may not be attributed to NVD; rate limits; API key above public limits; provided "as is" [16] | Yes, with notice and rate-limit compliance | VERIFIED [16] (ScanCode's copy; nvd.nist.gov is JavaScript-only) |
| CVE List (MITRE) | "MITRE hereby grants you a perpetual, worldwide, non-exclusive, no-charge, royalty-free, irrevocable copyright license to reproduce, prepare derivative works of, publicly display, publicly perform, sublicense, and distribute Common Vulnerabilities and Exposures (CVE®). Any copy you make for such purposes is authorized provided that you reproduce MITRE's copyright designation and this license in any such copy." [20] | Yes with notice | VERIFIED [20] (read in v2; SPDX reproduction) |
| CISA KEV | "licensed under the CC0 license" [19] | Yes | VERIFIED [19] |
| **ENISA EUVD** | API: all endpoints `GET` and "require no authentication"; search limited to 100 records per request; daily EUVD↔CVE mapping CSV and consolidated KEV JSON (CISA KEV + ENISA EU KEV) [17]. **No licence or terms** in the EUVD docs, the docs repository or the web app; the app links to the ENISA Legal Notice: "Reproduction of ENISA material published on this website is authorized, provided the source is acknowledged, unless it is stated otherwise" [18]. EUVD also aggregates third-party data [17] | Whether the legal notice covers EUVD data, and the terms of third-party content in EUVD, are **UNKNOWN** | Docs VERIFIED [17][18]; terms UNKNOWN |
| EPSS (FIRST) | Used by CRA Evidence [25]; terms not checked | — | UNKNOWN |

**Q3. What must Art. 14 notifications contain, and through which channel?**

*Legal minimum (Regulation (EU) 2024/2847, OJ text) [1]:*

| Stage | Actively exploited vulnerability (Art. 14(2)) | Severe incident (Art. 14(4)) |
|---|---|---|
| Early warning | Within 24h of awareness; indicate, where applicable, Member States where the product has been made available | Within 24h; at least whether suspected of being caused by unlawful or malicious acts; Member States |
| Notification | Within 72h; general information about the product, the general nature of the exploit and of the vulnerability, corrective or mitigating measures taken and those users can take; how sensitive the manufacturer considers the information | Within 72h; nature of the incident, initial assessment, measures taken and user measures; sensitivity |
| Final report | No later than 14 days after a corrective or mitigating measure is available: description incl. severity and impact; where available, information on any malicious actor; details of the security update or other corrective measure | Within one month after the incident notification: detailed description incl. severity and impact; type of threat or root cause; applied and ongoing mitigation |
| Other | CSIRT may request an intermediate report (14(6)); inform impacted users "where appropriate in a structured, machine-readable format that is easily automatically processable" (14(8)); the Commission "may, by means of implementing acts, specify further the format and procedures of the notifications" (14(10)) | same |

*Channel:* notifications go through the ENISA Single Reporting Platform, using the electronic notification end-point of the CSIRT designated as coordinator in the Member State of the manufacturer's main establishment (fallback rules for non-EU manufacturers in Art. 14(7)), simultaneously accessible to ENISA [1]. Platform facts from the ENISA FAQ [3]: ARs "must have an EU Login account with multi-factor authentication (MFA) enabled"; "There can be only one Primary AR per manufacturer and up to 20 Secondary ARs"; no API at initial release; English only at launch. ENISA published T&Cs v1.0 (10 Sep 2026), an AR user manual, submission guidance (9 Sep 2026) and a factsheet (v1.0, Jul 2026) [4]. VERIFIED.

*Platform fields (ENISA CRA SRP Glossary, "Version 1.3. Last update: 25 September 2026") [2]:* 18 common fields, 13 vulnerability-specific (v19–v30 incl. v26a) and 9 incident-specific (i31–i39).
- **Required at early warning:** notification type; title; summary; manufacturer name (system-generated); Member States where the product is available (concerned CSIRT); product name; product version or range; date/time of awareness (UTC); for incidents, whether suspected of unlawful or malicious acts (Yes/No/Unknown).
- **Required at 72h:** for vulnerabilities, general information and date/time of occurrence; for incidents, general information, occurrence date/time and initial assessment.
- **Required at final report:** corrective or mitigating measures taken; measures users can take; for vulnerabilities, date the measure became available, details of the update, full description of severity and of impact, and malicious-actor information "if such information available"; for incidents, applied and ongoing mitigation, detailed severity and impact, and threat type or root cause.
- **Optional examples:** product type (Default / Important / Critical), class, category, end-of-support indicator, component name, CVE ID, EUVD ID, attack vector, "Particular Exceptional Circumstances" and delay reasons.

SUPPORTED INFERENCE: the platform requires more fields at the early warning than the Regulation's minimum text lists (e.g., title, summary, product version). A tool can prepare, validate and time-stamp these fields deterministically and export them for manual entry, while stating that the SRP is the only submission channel. Because the glossary changed twice in September 2026, the schema must be versioned.

**Q4 (Agent 1 Q6). When, and what, will the Commission's simplified technical-documentation form for micro and small enterprises be?**
- Law: Art. 33(5): micro and small enterprises "may provide all elements of the technical documentation specified in Annex VII by using a simplified format. For that purpose, the Commission shall, by means of implementing acts, specify the simplified technical documentation form"; notified bodies "shall accept that form" [1]. No deadline is set in that paragraph. VERIFIED.
- Commission MSMEs page (updated 31 Jul 2026): the Commission "may also establish" such a form; no date or draft is given [11]. VERIFIED. (The page's "may" is weaker than the Regulation's "shall".)
- A secondary blog says that as of July 2026 the form was not available to download (snippet) [93].
- **Status: UNKNOWN (future event)** — no draft or date found. SUPPORTED INFERENCE on relevance: when adopted, the form would be free and would commoditise template-only technical-documentation offers; O1's core job (vulnerability handling and Art. 14) is less exposed, but any documentation module would be.

### 2.9 Major risks and obvious weaknesses (O1)
1. **Commoditisation by free and public tools:** Dependency-Track now tracks EU KEV [39]; the SRP form guides drafting [2]; ENISA favours "freely accessible" support [8]; an ENISA API "may be considered in a future phase" [3]; a free simplified documentation form is required by law but undated [1][11]. Facts VERIFIED; the commoditisation effect is UNKNOWN (future event).
2. **Contested SME price band:** CVD Portal (€99/month) and ConformOps (€79/month per product) [22][24]. VERIFIED.
3. **Episodic trigger (HYPOTHESIS):** Art. 14 fires only on *actively exploited* vulnerabilities or *severe* incidents; for many small products this may be rare, which weakens monthly retention unless continuous monitoring and evidence carry the value. Frequency per SME UNKNOWN.
4. **Mixed WTP signal:** financial support ties for the highest support item (73.2%) with templates for technical documentation [8].
5. **Schema churn and regulatory change:** glossary v1.1→v1.3 in three weeks [2][23]; possible implementing act on format (Art. 14(10)) [1].
6. **Liability** for missed or mismatched vulnerabilities; the product must not imply compliance (Agent 1 OOS-01).
7. **Data-licence gating:** EUVD terms UNKNOWN; NVD notice; CC-BY attribution; Ubuntu CC-BY-SA share-alike [14][16][17][18].
8. **Segment size UNKNOWN** (S1/S2 in §2.0); micro/small 24-hour fine relief lowers urgency [A1 3].
9. **Positioning pressure from AI-centric offers** ("Autonomous agentic AI for CRA", 452 stars) [42]; AI-free status is a constraint, not proven buyer value.

### 2.10 Validation questions still open (O1)
(No customer interviews were possible in this session.)

| # | Question | Evidence that would answer it |
|---|---|---|
| V1-1 | Share of target SMEs in S1 vs S2 vs firmware-only | Screener survey in developer communities; ENISA/LF microdata if obtainable; landing-page segmentation question |
| V1-2 | How often do SME products face an actively exploited vulnerability or severe incident? | Interviews with 10–15 S1 SMEs; KEV hit-rate analysis on public SBOMs of SME products |
| V1-3 | Will S1 SMEs pay above €79–€99/month for all six functions, vs Dependency-Track + Article 14 Ready or CVD Portal Reporting? | Van Westendorp or Gabor-Granger test; fake-door trial at €49/€99/€149 |
| V1-4 | Which function is most valued (F1–F6, support-period management)? | Card sorting; feature-interest clicks |
| V1-5 | Traction of CVD Portal, ConformOps, Kunnus, CRA Evidence | Direct enquiries; public customer lists (none found) |
| V1-6 | Are EUVD data reusable commercially? | Written confirmation from ENISA |
| V1-7 | Trust prerequisites (EU hosting, security page, references) | Interviews; A/B test of the security page |
| V1-8 | Do SECURE-type grants pay for SaaS subscriptions? | SECURE Annex 2 eligible costs; helpdesk |
| V1-9 | When will the Art. 33(5) simplified documentation form be adopted? | Commission comitology register; CRA expert-group minutes |

### 2.11 Assumptions requiring testing (O1)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O1-01 | About one third of surveyed SMEs (all roles) report implementing SBOMs; the share among CRA-relevant software-product SMEs is unknown | UNKNOWN (whole-sample proxy [8][10]) | V1-1 |
| MV-O1-02 | S2 SMEs will add an SBOM-generation step to use the product | HYPOTHESIS | Onboarding test |
| MV-O1-03 | SMEs will pay a recurring fee above the €79–€99/month anchors for all six functions | HYPOTHESIS (mixed signal [8]) | V1-3 |
| MV-O1-04 | Actively exploited vulnerabilities affect SME products often enough to sustain monthly value | HYPOTHESIS | V1-2 |
| MV-O1-05 | No dominant SME-focused CRA vendor exists | UNKNOWN (no traction published by anyone) | V1-5 |
| MV-O1-06 | EUVD data may be used in a commercial product | UNKNOWN | V1-6 |
| MV-O1-07 | Buyers value an AI-free, deterministic tool | ASSUMPTION | Interviews / positioning test |
| MV-O1-08 | ENISA will not ship a free submission API or drafting tool within 12 months that removes the drafting value | UNKNOWN (future event; [3] says an API "may be considered") | Monitor ENISA SRP releases |

---

## 3. O2 — Great Britain holiday-record and holiday-pay assurance for variable-hours employers

### 3.0 Context and the §1.4 standard

**(a) Context re-checked (DBT consultation read locally) [45].**
- "Since April 2026, employers have been required to keep holiday pay records for six years (regulation 16B of the Working Time Regulations 1998) that are adequate to show whether they have complied with the requirements. It is up to the employer how they keep those records." VERIFIED.
- Proposed FWA penalty: 200% of arrears, maximum £20,000 per worker, minimum £100; consultation closed 22 Sep 2026; FWA powers "apply only to England & Wales and Scotland. Employment law is devolved in Northern Ireland". VERIFIED.
- **J1-015 confirmed:** "Holiday pay claims will not be enforceable by the FWA if they occurred before Royal Assent … Royal Assent was 18 December 2025 so claims from before this date cannot be enforced by the FWA". VERIFIED.
- Self-audit incentive (proposal): "A penalty would not ordinarily be issued where an employer has correctly repaid all holiday pay arrears that are owing to the workers before the start of an FWA investigation." VERIFIED.
- FWA delivery plan 2026–27 (GOV.UK, first published 10 Aug 2026, updated 21 Aug 2026): "Holiday pay enforcement is expected to begin in 2027"; "Ready to communicate new enforcement approach, guidance and tools to support holiday pay compliance and processes in place to begin enforcement during 2027" [46]. VERIFIED.

**(b) Under-service evidence with the §1.4 standard.** The O2 core job has seven functions: **G1** 52-week holiday-pay rate with excluded weeks and a lookback of up to 104 weeks; **G2** selection of the pay items that count ("normal remuneration"); **G3** 12.07% irregular-hours accrual / rolled-up holiday pay; **G4** a calculation audit trail (inputs, method, outputs); **G5** works with the payroll products that do not automate the rate (Xero, Sage 50, BrightPay, Moneysoft); **G6** a guarantee of six-year retention and immutability of the records; **G7** a multi-client view for bureaus.
1. *Incumbent gaps* (documented by primary sources): Xero does not automate the rate and it is not on its roadmap [51]; Moneysoft cannot calculate the rate [50]; Sage 50's report must not be used when weeks need excluding [54]; BrightPay and QuickBooks are unresolved (§3.1b). Strong evidence for the Xero, Moneysoft and Sage 50 user bases.
2. *Published SME-priced direct competitor*: **paiyroll**'s holiday-pay companion (15p per payslip, £30/month minimum) claims **G1–G5** for exactly those products (§3.1a). G6 (a six-year retention/immutability guarantee) and G7 (a multi-client view in the companion) were **not found** on the pages read; paiyroll's full bureau *payroll* pack includes "Holiday pay /schemes" for unlimited client companies [90]. Payroll-native automation also exists in Staffology and KeyPay/Employment Hero [53][56].
3. *Traction*: paiyroll publishes vendor-selected customer stories (six named organisations, one of which "resolved holiday pay calculations") and testimonials including one titled "Recommend Paiyroll for Bureaus" [89]. No independent count was obtained (Trustpilot returned 403). Weak evidence of a paying market for the add-on specifically.

**Result (SUPPORTED INFERENCE).** Evidence of under-service is **Weak–Moderate**, the same rating as O1: incumbent gaps are strongly documented, but a published SME-priced add-on claims to cover five of seven functions for exactly the gap products, and its uptake is shown only by vendor-selected stories. v1's statements that paiyroll lacked an audit trail and 104-week lookback, and that it published no traction, were wrong and are withdrawn.

### 3.1 Competitor matrix (direct)

**3.1a Direct calculation / assurance offers**

| Name / URL | Target | Capabilities relevant (quoted where verbatim) | Published pricing | Region | Published traction | Grade |
|---|---|---|---|---|---|---|
| **paiyroll** holiday-pay companion — paiyroll.com (© 2026 Innovatie Limited) | Employers and payroll bureaus keeping their existing payroll | "Records every payment made by date to be able to perform the required weekly calculations looking back 104 weeks to find 52 paid weeks"; "The software can import 104 weeks of historical pay data"; "The software allows you to specify only the Pay Items that need to be included in the holiday pay calculation"; 12.07% rolled-up holiday pay for irregular-hour workers; "Holiday pay XLSX reports ( data table and accrual ) are available at any point to show the data and calculations. You can be assured you have a complete audit trail."; "Generates records and reports for each holiday booking on each pay run"; import from 18 listed payroll formats including Xero, Sage 50 CSV, Sage FPS, Brightpay, Moneysoft Payroll Manager, Quickbooks, Staffology, Keypay / Employment Hero, Iris Earnie, Iris Star; results are entered into the existing payroll by copy/paste or file download; branded booking app "for any company or bureau"; vendor claim: "we are one of the only providers to automatically support the new 52-week holiday pay law" | **15p per payslip**, "Minimum £30 pcm", optional "£90 one-off setup/training/configuration fee", monthly, no annual contract, ex VAT [49] | UK | Customer-stories page: six named organisations (e.g., The President Estate Farming Partnership — "resolved holiday pay calculations"; Ignite Nursing; Personnel Link); testimonials incl. "Recommend Paiyroll for Bureaus" (vendor-selected) [89] | V (read) [49][89] |
| **paiyroll** bureau payroll pack — paiyroll.com/payroll-bureau-pricing | Payroll bureaus (full payroll) | Full payroll incl. "Holiday pay /schemes" in all three tiers; "you can have an unlimited number of companies and an unlimited number of administrators"; FAQ: "For Northern Ireland, the 12-week reference period can be specified." | **Bureau 25: £50 pcm** (25 clients, <10 employees each); **Bureau 75: £75 pcm** (75 clients, <20 employees each; the page's feature table lists 50 companies for this tier — internal inconsistency); **Bureau: £100 pcm** (100 clients included, additional clients £1, <50 employees each) [90] | UK | See above | V (read) [90] |
| **paiyroll** free services | Employers, bureaus | "Holiday Pay Compliance Check … FREE service!" ("Audit holiday pay process", "Advice on calculating holiday pay"); free Excel holiday-pay template based on BEIS guidance; "Payroll Audit" service that imports historical payroll files to "import, replay and verify" payroll (price on request) [90][91] | Free / on request | UK | — | V (read) [90][91] |
| **Staffology Payroll** (IRIS) — in-payroll | Employers and bureaus | Average Holiday Pay schemes: setting "Weeks for average calculations", described as "Defaults to 52 weeks."; option "Use only paid weeks"; statutory-pay exclusion options ("Only one exclusion option can be selected at a time"); pay items via NI'able pay or a pay-code set; optional floor: "Use Hourly Rate (where average rate is lower than normal hourly rate)" (page updated 24 June 2026). Whether the lookback extends beyond 52 weeks to reach 52 paid weeks is not stated | Not captured (pricing URL redirects to IRIS) | UK | Not published | P (own docs, read) [53] |
| **KeyPay / Employment Hero UK** — in-payroll | SMEs; site navigation lists Bureau, Accountant, Bookkeeper business types | "the system will automatically calculate the average amount of holiday pay based on the historic data held"; "a calculations are held against the employee so the user can see how the holiday amount was calculated"; floor: "If the average hourly rate calculates to be less than the employees' current hourly rate then the system will default the holiday hours to be paid at the current pay rate"; "If any data is missing to make 52 weeks, then KeyPay will notify you"; configurable pay categories | Not on page | UK | Two named testimonials on page (vendor-selected) | P (own docs, read) [56] |
| **IRIS Earnie Holiday Pay Module** | IRIS Earnie users | Configurable holiday-pay calculation incl. 52-week averaging (updated 16 Feb 2026) | Licensing/price not stated | UK | — | P (read) [57] |
| **Healthbox HR** | SMEs | HR + payroll; a Xero user is "in the process of switching payroll from Xero to Healthbox HR to comply with the law" [51] | Custom pricing (snippet) [63] | UK | — | V (snippet) |
| Leave/rota tools: **StaffLeave** (claims six-year storage and audit trails for FWA audits), **Employment Hero HR**, **BrightHR**, **Breathe**, **Timetastic**, **RotaCloud**, **Planday**, **Fourth**, **Shiftbase**, **LeaveWizard** | SMEs | Leave tracking and 12.07% hours accrual; pay-rate calculation not claimed on the pages read | Various | UK | — | V (read [58][59]; snippets [62]) |
| Advisory services: accountancy/payroll consultancies (e.g., Azets), employment lawyers | Employers | Reviews and remediation | Not published | UK | — | S/V (snippet) [65] |

**3.1b Coverage of 52-week averaging and irregular-hours accrual in common UK payroll products**

| Product | 12.07% accrual | 52-week holiday-pay *rate* | Evidence and date | Label |
|---|---|---|---|---|
| **Sage 50 Payroll** | Calculated-entitlement schemes; one user reports they use the prior 12 weeks (snippet) | 52-week average report, but "you must only use this when there are no weeks to exclude in the 52-week period"; if there are unpaid or SSP-only periods "the report does not add further periods to the calculation. In this case you must manually calculate the relevant hourly rate for holiday pay" (KB last modified 4 Sep 2024) | [54] | VERIFIED as of KB date; 2026 status UNKNOWN |
| **Sage Payroll (cloud)** | UNKNOWN | No evidence of automatic calculation (>2-year-old thread) | [54] | UNKNOWN |
| **Xero Payroll UK** | Not checked | Not automated. Idea created 1 Jun 2022, 93 votes, status "Accepted"; Xero admin, 27 Nov 2025: "for the time being this is not a feature we have planned in our roadmap"; workaround: "running the Payroll Activity Summary or Gross to Net report over a 52 week period" | [51] | VERIFIED |
| **QuickBooks Payroll UK** | UNKNOWN | Conflicting staff statements in a community thread (Feb 2022: not available; Nov 2022: available for several schedules); standard vs Advanced unclear | [55] | UNKNOWN (sources conflict) |
| **BrightPay** | Yes: "applying 12.07% to hours worked (excluding hours marked as overtime hours)" (2025-26 docs) | Conflicting: a BrightPay doc snippet says BrightPay will not calculate holiday pay amounts (not found in the 2024-25 or 2025-26 page text); Xero users write "I have had to look at other software such as BrightPay / BrightHR as they offer this as a part of their software!" (18 Nov 2025) and "I keep hearing that systems like BrightPay and BrightHR can handle this automatically" (9 Apr 2025) | [51][52] | Accrual VERIFIED; rate UNKNOWN (sources conflict) |
| **Staffology (IRIS)** | Not checked | Automatic average-holiday-pay schemes (see §3.1a) | [53] | VERIFIED (own docs) |
| **IRIS Earnie** | Not checked | Holiday Pay Module; degree of automation UNKNOWN | [57] | Partly VERIFIED |
| **Moneysoft Payroll Manager** | Yes: automatic 12.07% of hours worked; rolled-up holiday pay automatic | No: "Payroll Manager is not able to calculate the holiday pay rate automatically, instead the rate must be calculated by the user" | [50] | VERIFIED |
| **KeyPay / Employment Hero** | Not checked | Yes, automatic, with rate floor, missing-data notification and stored calculation breakdown | [56] | VERIFIED (own docs) |

SUPPORTED INFERENCE: the rate calculation is automated in some payroll products (Staffology, KeyPay/Employment Hero) and manual or conditional in several widely used SME products (Xero, Moneysoft, Sage 50 when weeks must be excluded). paiyroll markets an add-on for exactly those products. How many employers use the gap products for variable-hours staff is UNKNOWN.

**3.1c Who is the buyer — employer or bureau?**
- Liability and the criminal offence sit with the **employer** [45]. VERIFIED.
- **Bureau signals:** paiyroll addresses both routes ("Whether you are a bureau or an employer" [91]; a booking app that "can be branded for any company or bureau" [49]) and publishes bureau payroll tiers with holiday-pay schemes [90]; a vendor-selected testimonial is titled "Recommend Paiyroll for Bureaus" [89]; KeyPay's site lists Bureau, Accountant and Bookkeeper as business types [56]; a Xero commenter writes as an adviser: "This lack of functionality is stopping our client using Xero payroll , so going elsewhere !!" (25 Apr 2023) [51]. VERIFIED (V and forum sources).
- **Employer signals:** most Xero commenters describe calculating for their own employees, e.g., "we’re currently having to calculate it manually" (10 Apr 2025) and "I am in the process of switching payroll from Xero to Healthbox HR to comply with the law, which is a major inconvenience." (2 May 2026) [51]. VERIFIED.
- Share of SMEs using bureaus or accountants for payroll, and the number of UK payroll bureaus: only low-quality aggregator snippets [66]. UNKNOWN.
- **Conclusion: HYPOTHESIS** — two buyer routes. Employers carry liability and write about the pain; bureaus and accountants are targeted by at least two vendors and have their own price anchor (§3.3). Which route converts better is untested.

### 3.2 Alternatives and substitutes

| Substitute | Cost | Where it breaks | Label |
|---|---|---|---|
| **Spreadsheet or paper records** — the ATT says records may be kept in any format the employer thinks reasonable, including dedicated software, a spreadsheet or paper (paraphrase) [60] | Staff time | Excluded weeks, the 104-week lookback and normal-remuneration components are error-prone; six-year retention; data spanning tax years | VERIFIED [60]; failure modes SUPPORTED INFERENCE |
| **Free templates and checks**: paiyroll's free Excel holiday-pay template (52-week reference period, BEIS guidance) and free "Holiday Pay Compliance Check" [90][91] | Free | Manual data entry per worker and per holiday; paiyroll itself says the template "still takes a long time to enter all the data" [91] | VERIFIED (V) |
| **Payroll reports + Excel** (Xero, Sage 50, BrightPay workarounds) [51][52][54] | Included in payroll | Manual rate entry each period; no recorded method | VERIFIED |
| **GOV.UK holiday-entitlement calculator** | Free | Entitlement and accrual only, not pay [47] | VERIFIED |
| **GOV.UK worked examples**: Insolvency Service guidance on calculating average weekly pay over 52 weeks for holiday-pay claims (6 Apr 2021) [48] | Free | For workers claiming from insolvent employers; not an employer tool | VERIFIED |
| **Tools the government is considering**: DBT lists "a more detailed calculator or self-assessment tool to help employers and workers work out holiday entitlement and holiday pay", worked examples, a chatbot and webinars among "the types of support we are considering" [45]; FWA plans "guidance and tools to support holiday pay compliance" [46] | The consultation does not state a price; that a GOV.UK/FWA tool would be free is SUPPORTED INFERENCE | Not yet available; scope UNKNOWN | VERIFIED (intention); delivery UNKNOWN (future event) |
| **Acas** free advice [45]; worker-side calculators (payslipchecker.uk, timetally.uk, uktax.tools, youtemp) [64] | Free | Guidance or single calculations; no records | VERIFIED [45]; snippets [64] |
| **Leave/rota tools** with 12.07% accrual [58][62] | Per user | Accrue hours; no pay rate | SUPPORTED INFERENCE |
| **Accountants, bureaus, HR consultancies, lawyers** [65]; paiyroll's "Payroll Audit" replay service [91] | Fees not published | Episodic reviews | UNKNOWN (fees) |
| **Switching payroll** to a product that automates averaging (Staffology, KeyPay/Employment Hero, Healthbox; paiyroll's own full payroll) [51][53][56][90] | Migration cost; bureau payroll from £50 pcm for 25 clients [90] | Disruptive; historic data import needed (paiyroll and Staffology both offer historic import) | SUPPORTED INFERENCE |

### 3.3 Pricing evidence (date seen 2026-09-26)

| Offer | Price | Source |
|---|---|---|
| paiyroll holiday-pay companion | 15p per payslip; minimum £30/month; optional £90 one-off setup; ex VAT | [49] V |
| Illustration: employer with 50 weekly-paid variable-hours workers | ≈ 217 payslips/month × £0.15 ≈ £32.50/month, i.e., close to the £30 minimum (SUPPORTED INFERENCE: arithmetic on [49]) | [49] |
| paiyroll bureau **payroll** tiers (full payroll including "Holiday pay /schemes") | £50 pcm (25 clients), £75 pcm (75 clients), £100 pcm (100 clients, +£1 per additional client) | [90] V |
| Illustration: per-client cost in the bureau tiers | ≈ £1–£2 per client per month for payroll including holiday-pay schemes (SUPPORTED INFERENCE: £50/25, £75/75, £100/100) | [90] |
| paiyroll Holiday Pay Compliance Check; holiday-pay template | Free | [90][91] V |
| paiyroll Pro plan (FAQ, daily pay) | base 15p; 1st payslip in a month £1.35; extra payslips +15p | [90] V |
| Staffology, KeyPay/Employment Hero, BrightPay, Sage, Xero, Moneysoft, IRIS licences | Not captured in this session | UNKNOWN |
| Outsourced payroll | "£4–£25 per employee" per month quoted by aggregators (snippet, low quality) | [66] |
| Healthbox HR, StaffLeave PlusPack, Azets reviews, paiyroll Payroll Audit | Not published / on request | [58][63][65][91] |

### 3.4 Market / demand evidence

| # | Signal | Evidence | Quality |
|---|---|---|---|
| D1 | Records duty in force; criminal offence | reg. 16B since April 2026 [45]; CIPP (30 Mar 2026) [61]; ATT (16 Jun 2026) [60] | Primary, strong (obligation) |
| D2 | Government acknowledges calculation difficulty | "We know calculating holiday pay entitlement can be complex and can lead to accidental non-compliance and underpayment." [45] | Primary, strong (qualitative) |
| D3 | Enforcement coming | "Holiday pay enforcement is expected to begin in 2027" [46]; proposed 200% penalty, £20,000 cap per worker [45] | Primary; timing is a stated plan |
| D4 | Non-compliance proxies | Resolution Foundation: 2.2m jobs with no annual leave in 2025; TUC: ~1.1m workers without holiday pay in 2023 (~£2bn); DBT: these estimates "do not provide a direct, robust measure of the level of holiday pay non-compliance" [45] | Primary citing secondary; measures leave denial, not calculation error |
| D5 | Dispute volume | ~8,000 ET claims on "Working Time (annual leave)" and 13,000 "Wages Act" claims in 2024/25 (Acas data) [45] | Primary, moderate |
| D6 | User demand in an incumbent forum | Xero idea: 93 votes since 2022; comments to May 2026, e.g., "This is a legal requirement, not a nice-to-have wish." (2 May 2026); "Every single payroll user in the UK requires this by law, and we’re currently having to calculate it manually." (10 Apr 2025); "It would also be good if there's the option to select which pay elements to include / exclude from the 52 week average calculation." (20 Apr 2026); several threaten to switch ("We may need to move to other accounting software …", 18 Mar 2025) [51] | Primary (user forum), **strong** for the Xero user base |
| D7 | Vendor documentation admits gaps | Moneysoft (manual rate) [50]; Sage 50 (manual when weeks excluded) [54] | Primary product docs, strong |
| D8 | A paying market for an add-on | paiyroll publishes prices and vendor-selected stories [49][89] | V, weak |
| D9 | Content volume since April 2026 | Law firms, ATT, CIPP, HR vendors on six-year records and FWA readiness [58]–[61][65] | Secondary, moderate (supply-side) |
| D10 | Self-audit incentive | No penalty "ordinarily" if arrears repaid before an investigation (proposal) [45] | Primary, moderate |
| D11 | Prevalence of miscalculation among SMEs | No survey found; CIPP 2024 ">30%" is snippet-only [A1 45] | UNKNOWN |
| D12 | Forums (Reddit, AccountingWEB) | Not reachable | UNKNOWN |

### 3.5 Customer complaints and documented limitations

*Complaints (user sources):*
- **Xero** users: "I would have thought that something that has been a legal requirement since 2020, should have the highest priority" (18 Mar 2025); "I too am starting to look elsewhere for better software." (30 Apr 2025); "Xero doesn't even produce reports with the necessary figures to perform the calculations" (18 Nov 2025); "I am in the process of switching payroll from Xero to Healthbox HR to comply with the law, which is a major inconvenience." (2 May 2026) [51]. VERIFIED.
- **Sage 50** users report that calculated entitlement based on prior weeks gives wrong results for irregular hours and use report-merging workarounds (snippet) [54].

*Limitations stated in vendor documentation (not complaints):*
- Moneysoft: no automatic rate; no automatic accrual during statutory leave [50]. VERIFIED.
- Sage 50: the 52-week report does not extend the period when unpaid or SSP-only weeks occur [54]. VERIFIED.
- BrightPay: 52-week reports cover one tax year at a time and must be combined manually (snippet) [52].
- Staffology: the documentation does not state whether the lookback extends beyond 52 weeks to reach 52 paid weeks [53]. UNKNOWN (not a complaint).
- KeyPay: the rate floor and missing-data notification are safeguards, not gaps [56]; whether its lookback extends beyond 52 weeks is not stated. UNKNOWN.

### 3.6 Differentiation opportunities (restated after J2-001)

paiyroll's pages already describe G1–G5 for the gap products: a 104-week lookback and historic import, pay-item selection, 12.07% rolled-up pay, XLSX reports described as "a complete audit trail", per-booking records per pay run, and imports from Xero, Sage 50, BrightPay and Moneysoft [49]. Calculation, the 104-week lookback and a calculation audit trail are therefore **not** differentiators.

What remains, as HYPOTHESES only (not described on the paiyroll pages read):
1. **Six-year retention and immutability guarantees** — a tamper-evident per-worker ledger with retention stated for six years (reg. 16B) [45]. paiyroll describes an audit trail but not a retention period or immutability (not found; not proof of absence).
2. **An FWA-oriented evidence-pack format** — method, reference weeks, pay items, inputs and outputs per worker per booking, in a format designed around an FWA request. Its value depends on FWA guidance that does not yet exist [46].
3. **A multi-client bureau view for the add-on** — paiyroll's bureau offer is a full-payroll pack; a companion-only multi-client view was not described [49][90].
4. **An arrears self-check limited to post-18-Dec-2025 periods** — aligned with the proposed "repay before investigation" incentive [45]. paiyroll offers a free compliance check and a payroll-audit replay service, so this is partly covered [90][91].

Not better: in-payroll automation (Staffology, KeyPay) [53][56]; write-back into payroll (fails Agent 1's MVP filter; paiyroll also relies on copy/paste or file download) [49]; price (15p/payslip; bureau payroll from about £1–£2 per client per month) [49][90]; a government calculator if built [45]; legal interpretation (Agent 1 OOS-04).

### 3.7 Switching costs, saturation, acquisition
- **Switching (SUPPORTED INFERENCE):** an add-on avoids replacing payroll but needs a per-period export/upload routine (paiyroll requires weekly pay uploads and holiday bookings via app or spreadsheet [49]). Changing payroll provider is the high-cost alternative; one Xero user reports doing it [51].
- **Saturation:** leave tracking is saturated. The calculation add-on niche has one dedicated, published competitor (paiyroll) with bureau pricing and free lead-in services, plus payroll-native automation in Staffology and KeyPay [49][53][56][90]. Uptake beyond vendor-selected stories is UNKNOWN.
- **Channels:** bureaus and accountants are targeted by paiyroll and KeyPay [56][90]; payroll-software user forums are where the pain is visible [51]. No primary data on channel size or conversion. UNKNOWN.
- **Acquisition difficulty (SUPPORTED INFERENCE):** moderate. The pain is concentrated in identifiable user bases (Xero, Sage 50, Moneysoft), but an incumbent add-on with free lead-in services already targets them, and the market is GB-only.

### 3.8 Major risks and obvious weaknesses (O2)
1. **Direct incumbent add-on** covering G1–G5 at 15p/payslip with free lead-in services [49][90][91]. VERIFIED (V).
2. **Government tool:** DBT lists a holiday-pay calculator among the support it is considering [45]. VERIFIED (intention).
3. **Incumbents closing the gap** (Staffology, KeyPay; Xero could change its roadmap) [51][53][56].
4. **Regime still a proposal**; penalties, claim period and the 2027 start await the government response [45][46].
5. **Smaller near-term exposure** than "six years": FWA cannot enforce pre-18 Dec 2025 underpayments [45].
6. **Calculation liability** (normal remuneration, 52/104-week rules, EU vs domestic leave).
7. **GB-only market**; NI equivalence of the records duty UNKNOWN (A-18). paiyroll's FAQ says a 12-week reference period can be specified for Northern Ireland [90], which suggests (SUPPORTED INFERENCE, vendor-sourced) that NI calculation rules differ.
8. **Low price anchors** (15p/payslip; bureau payroll ~£1–£2 per client per month) [49][90].
9. **Data protection**: pay and possibly health-related absence data (Agent 1 OOS-02).

### 3.9 Validation questions still open (O2)
(No interviews possible in this session.)

| # | Question | Evidence that would answer it |
|---|---|---|
| V2-1 | Employer or bureau: who buys, and do bureaus buy a calculation add-on or switch clients to payroll that includes it (e.g., paiyroll's bureau pack)? | 10 bureau + 10 employer interviews; ICPA/CIPP membership data; bureau directory count |
| V2-2 | How many employers with variable-hours staff use Xero, Sage 50, BrightPay or Moneysoft? | Payroll-software market-share data; screener survey |
| V2-3 | Does BrightPay (2026-27) calculate the 52-week rate? Does QuickBooks standard payroll? | Trial accounts; vendor support |
| V2-4 | Will buyers pay for six-year retention/immutability and an FWA-oriented pack beyond paiyroll's calculation + XLSX audit trail? | Pricing test vs 15p/payslip and vs bureau pack per-client cost |
| V2-5 | paiyroll's add-on uptake (not full-payroll customers) | Direct enquiry; integration marketplace reviews; Trustpilot count (403 in this session) |
| V2-6 | Will DBT/FWA ship a holiday-pay calculator, when, and at what price (presumably free)? | Government response to the consultation |
| V2-7 | Prevalence of miscalculation | CIPP 2024 survey; bureau audit data |

### 3.10 Assumptions requiring testing (O2)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O2-01 | A material share of GB variable-hours employers use payroll products that do not automate the 52-week rate | HYPOTHESIS (per-product gaps VERIFIED [50][51][54]; user counts UNKNOWN) | V2-2 |
| MV-O2-02 | Bureaus are the efficient channel | HYPOTHESIS (targeted by two vendors [56][90]; conversion UNKNOWN) | V2-1 |
| MV-O2-03 | Buyers value six-year retention/immutability and an FWA-oriented pack beyond an existing audit trail | HYPOTHESIS | V2-4 |
| MV-O2-04 | The government will not release a holiday-pay calculator that covers the MVP's core within 12 months | UNKNOWN (future event; DBT considering one [45]) | V2-6 |
| MV-O2-05 | FWA enforcement starts in 2027 | VERIFIED as stated plan [46]; actual start UNKNOWN (future event) | Monitor |
| MV-O2-06 | Payroll exports contain enough data (hours, pay elements, dates) to compute rates deterministically | ASSUMPTION (paiyroll claims it reads each supplier's file format [49]) | Collect sample exports from 3–5 products |

---

## 4. O4 — EU Pay Transparency compliance for SME / lower-mid-market employers (conditional)

### 4.0 Status of Italy and other states

**Italy — Legislative Decree No. 96 of 7 May 2026** (Gazzetta Ufficiale n. 125, 1 Jun 2026; in force 7 Jun 2026). VERIFIED [69][70][71] (three secondary sources read; Italian snippets agree [72]).
- Arts. 5–7 obligations apply from 7 Jun 2026; the pay-progression criteria obligation does not apply below 50 employees [69][70]. VERIFIED.
- Reporting: **250+** annually, first by **7 Jun 2027**; **150–249** every three years, first by **7 Jun 2027**; **100–149** every three years, first by **7 Jun 2031**; no reporting below 100 [69][70][71]. VERIFIED.
- Indicators: mean and median gender pay gap, variable-pay gaps, share receiving variable pay, quartile distribution, gaps by category of workers doing the same work or work of equal value; data confirmed after consulting worker representatives [71]. VERIFIED (S).
- Recipient: a monitoring body set up at the Ministry of Labour [70][71]; composition (ISTAT, INPS, INAPP, CNEL, unions) within 180 days (snippet) [72].
- **Reporting format: not yet defined as far as found.** Technical data specifications are to be set by ministerial decree within 90 days of entry into force (about 5 Sep 2026), after the data-protection authority's opinion [70]. Ius Laboris (23 Sep 2026): the Minister "is expected to adopt ministerial decrees in September setting out further details regarding the reporting obligations under Article 9(4)" [68]. No evidence of adoption by 26 Sep 2026. **UNKNOWN.**
- Job classification: national collective bargaining agreements (NCBAs) are the primary framework for equal work and work of equal value; internal systems may "only integrate — and not replace" them [69]. VERIFIED (S).
- Existing routine: Italy's biennial report on male and female staff (art. 46 D.Lgs. 198/2006) is mandatory above 50 employees and filed online; the 2024–25 edition was due 15 May 2026 after an extension (several snippets agree) [73]. Relationship to the new reports UNKNOWN.
- Segment size: ISTAT counts **22,861** enterprises with 50–249 persons employed ("le medie (50-249 addetti) … 2,2% (22.861 unità in valori assoluti)"), for firms with at least 3 persons employed, excluding agriculture and public administration, reference year 2021 [74]. VERIFIED (read in v2). The 100–249 subset is UNKNOWN. SUPPORTED INFERENCE: only the 150–249 band faces a first report in 2027, so the near-term Italian SME reporting segment is a fraction of that figure.

**Other member states (answer to "which will transpose by early 2027")**

| State | Status (source date) | Early-2027 outlook | Label |
|---|---|---|---|
| Malta, Lithuania, Slovakia | Fully transposed by 7 Jun 2026 (Lewis Silkin, 25 Jun 2026) [75] | In force | VERIFIED (S) |
| **Greece** | Law 5316/2026, Government Gazette 6 Jul 2026; most obligations from **1 Nov 2026**; reporting 250+ and 150–249 first by 7 Jun 2027, 100–149 by 7 Jun 2031; Ombudsman as monitoring body with a digital platform; fines €300–€50,000 per violation; SME technical assistance [76] | In force from 1 Nov 2026 | VERIFIED (Lewis Silkin read + Jackson Lewis and Zepos snippets) |
| Poland; Belgium; Estonia | Partial (PL recruitment rules; BE public sector only; EE recruitment and pay secrecy) [75][77] | Further PL legislation in parliament [77] | VERIFIED (S) |
| Netherlands | Draft; plenary debate second week of January 2027; the 1 Jan 2027 target "now appears uncertain" [68] | UNKNOWN (future event) | Status VERIFIED |
| Germany | "(unconfirmed) rumours" of cabinet approval in October 2026 [68]; another consultancy lists January 2027 [77] | UNKNOWN (future event; sources differ) | Status VERIFIED |
| Romania | Draft; likely enacted before end-2026 per one consultancy [77] | UNKNOWN (future event; single source) | — |
| Hungary | Law "planned for adoption in October 2026" [68] | UNKNOWN (future event) | Plan VERIFIED |
| Cyprus | Draft to Council of Ministers Sep 2026; first reports for 150+ by 7 Jun 2027 [68] | UNKNOWN (future event) | Plan VERIFIED |
| Czechia | Draft sent to the Chamber after 4 Sep 2026 [68]; phased 2027–2031 [77] | UNKNOWN (future event) | Status VERIFIED |
| France | Draft amended 10 Sep 2026; aim for a final vote before the April/May 2027 elections [68] | UNKNOWN (future event) | Status VERIFIED |
| Spain | Draft Royal Decree published 3 Aug 2026 [68] | UNKNOWN | Status VERIFIED |
| Portugal; Bulgaria | Partial draft (5 Aug 2026); bill to parliament (11 Sep 2026) [68] | UNKNOWN | Status VERIFIED |
| Ireland | Pay Transparency Bill not given priority drafting status (16 Sep 2026) [68] | UNKNOWN (unlikely by early 2027 on this evidence — SUPPORTED INFERENCE) | Status VERIFIED |
| Sweden | Government (26 Mar 2026) will not submit a bill; seeks EU-level postponement and renegotiation [78] | UNKNOWN | Status VERIFIED |

Agent 1's approved v2 describes Ius Laboris as treating "only Italy" as transposed. The Ius Laboris text I read lists only recent *changes* (its map is not machine-readable); Lewis Silkin and others record Malta, Lithuania, Slovakia and, from 6 Jul 2026, Greece as transposed. See OOS-MV-01.

### 4.1 Competitor matrix (direct)

| Name / URL | Target | Capabilities relevant | Published pricing | Hosting / region | Traction | Grade |
|---|---|---|---|---|---|---|
| **Axios Analytics** — axiosanalytics.com | Mid-market; all EU member states | CSV/Excel import with data-quality scoring; EG-Check job evaluation; the seven Art. 9 metrics and the 5% Art. 10 trigger; remediation simulator; sign-offs (paraphrase) | <100 employees: one-off report **€4,000**; **100–149: €3,000/yr; 150–249: €4,500/yr**; 250–499 €7,000/yr; 500–999 €10,000; 1,000–1,999 €16,000; onboarding €1,500 one-off; 12-month auto-renew [80] | EU hosting in Frankfurt [80] | None published | V (read) [80] |
| **Evenpay** — evenpay.io | Mid-size and enterprise | Job evaluation, pay-gap reporting, salary bands, joint pay assessments, justification archive | **Evenpay Core €4,900/yr** (band-dependent; bands include 100–249); SSO +€189/month [81] | Not stated | None | V (read) [81] |
| **Zucchetti HR PayGap** — zucchetti.it | Italian HR/payroll customers (also via partners such as Veridian; errepi for associations and professionals) | Equal-value clusters; automatic gender-pay-gap calculation; 5% flags; reports; answers to employee requests; simulations; HR/payroll integration | Not published [84] | Italy | Not published | V (read) [84]; partners snippet [85] |
| **TeamSystem**, **Inaz** (Italy) | Italian employers | Published D.Lgs. 96/2026 guidance; product scope not verified | Not published | Italy | — | V (snippet) [85] |
| **Figures** — figures.hr | Mid-market / enterprise | Benchmarking, salary bands, pay-gap analysis, an EU-directive compliance report, employee information letters | Quote by headcount [82]; starting figures reported as €2,500/yr (snippet) and €4,000 (page metadata per [83]) — sources conflict | EU | — | V (read, no price) [82] |
| **Personio** | SMEs (HR suite) | Publishes directive guidance and gender-pay-gap reporting features (snippets) [94]; Italian coverage and product details UNKNOWN (pages rate-limited, HTTP 429) | Quote-based (not published on pages found) | EU | — | V (snippet) [94] |
| **Ravio**, **PayAnalytics (beqom)**, **Sysarb**, **Trusaic**, **Syndio**, **HiBob**, **Lattice** | Mid-market to enterprise | Pay-equity analytics | Ravio £5,000/yr for a 500-person company; Lattice $13/seat/month + $6 add-on, $4,000 minimum; PayAnalytics per employee analysed, 1-year minimum; Sysarb onboarding fee + annual; others quote-only [83] | Various | — | V [83] |
| **TracefyHR**, **employsome**, **Jet HR** (IT), **Fluida** (IT) | SMEs (content) | Directive guides; products and prices not verified | UNKNOWN | — | — | V (snippet) [95] |

SUPPORTED INFERENCE: for the 100–249 band, an EU-wide, EU-hosted tool publishes €3,000–€4,500/year [80], and the leading Italian payroll vendor sells a dedicated pay-gap module [84].

### 4.2 Alternatives and substitutes
- **Commission/EIGE gender-neutral job-evaluation toolkit** (April 2026): step-by-step guidance; Tool 4 for organisations of 10–49 and up to 250 employees with fewer than 15 distinct roles, using pair comparison; voluntary and free [79]. VERIFIED (S).
- **Payroll/HRIS reports + Excel** (consulenti del lavoro and in-house payroll) — staff time; breaks on equal-value categorisation and worker-representative sign-off. SUPPORTED INFERENCE.
- **Italy's biennial staff-report routine** and portal [73] — may absorb part of the new reporting (UNKNOWN).
- **Law firms and consultancies** (e.g., Ius Laboris's own pay-gap offer) — quote-only [68].
- **GitHub prototypes**: 12 repositories, all 0 stars, several AI-based; a free "quick scan" (FairWave, 17 Sep 2026) [87]. Weak.

### 4.3 Pricing evidence (date seen 2026-09-26)

| Offer | Price | Source |
|---|---|---|
| Axios Analytics 100–149 / 150–249 | €3,000 / €4,500 per year + €1,500 onboarding | [80] V |
| Axios Analytics <100 | €4,000 one-off report | [80] V |
| Evenpay Core | €4,900/year (band-dependent) | [81] V |
| Ravio | £5,000/year for a 500-person company | [83] V (third-party list) |
| Lattice | $13/seat/month + $6 add-on, $4,000 minimum | [83] V |
| Figures | Quote; €2,500 or €4,000 starting figures reported (sources conflict) | [82][83] |
| Zucchetti, TeamSystem, Inaz, Personio, PayAnalytics, Sysarb, Trusaic, Syndio | Not published | [83][84][85][94] |

Pricing transparency: effy.ai's list of 15 pay-equity tools (23 Sep 2026) says "Two of fifteen publish a figure" [83]. That list is US- and enterprise-heavy and omits Axios and Evenpay, which publish SME-band prices [80][81]. SUPPORTED INFERENCE, limited to that list: opaque pricing is common among enterprise pay-equity tools; it is not a market-wide gap in the SME band.

### 4.4 Market / demand evidence

| # | Signal | Evidence | Quality |
|---|---|---|---|
| D1 | Law in force in Italy and Greece | D.Lgs. 96/2026 [69]; Law 5316/2026 [76] | Secondary, strong (consistent) |
| D2 | First SME-band deadline | 150–249: first report 7 Jun 2027 (IT, GR); 100–149: 2031 [69][76] | Strong, but narrows the near-term segment |
| D3 | Readiness surveys | Aon 2026 Pulse: 19% ready for reporting; Mercer 2026: 9% of Europe-based employers have a full transparency strategy; Littler 2025: 24% "very prepared"; 42% cite inconsistent job or role data (all snippet) [86] | Secondary, snippet-only, enterprise-weighted |
| D4 | Italian professional-channel activity | Many consulenti del lavoro, Confindustria and payroll-software publishers issued D.Lgs. 96/2026 guides in June–September 2026 (snippets) [72][85] | Secondary, moderate (supply-side) |
| D5 | Italy-specific SME demand survey | None found | UNKNOWN |
| D6 | Community/OSS | 12 GitHub repositories, 0 stars [87] | Weak |
| D7 | Political volatility | Sweden seeks renegotiation [78]; the Commission refused a delay [A1 16] | Moderate |

### 4.5 Customer complaints and feature gaps
- No user reviews or complaints about SME pay-transparency tools were found. UNKNOWN.
- NCBA-based categorisation is central in Italy [69]; whether generic EU tools handle NCBA levels is UNKNOWN (HYPOTHESIS that they do not).
- (v1 listed effy.ai's "only 2 of 15 publish a figure" as a complaint; it is moved to §4.3 and limited to that list — J2-006(c).)

### 4.6 Differentiation opportunities
Could be better (HYPOTHESES): Italian-language, NCBA-level categories; Art. 7 request workflow with the two-month deadline; a multi-client mode for consulenti del lavoro; output in the ministerial format once it is defined.
Could not be better: Zucchetti's payroll data access in Italy [84]; Axios's published €3,000–€4,500 SME pricing and all-EU coverage [80]; the statistical and legal depth of enterprise tools; the free EIGE methodology [79].

### 4.7 Switching costs, saturation, acquisition
- Switching: HR data already sits in Italian payroll suites; an external tool needs exports (SUPPORTED INFERENCE).
- Saturation: crowded at mid-market/enterprise; SME-priced EU-wide tools exist [80][81].
- Channels: consulenti del lavoro and payroll-software resellers (Zucchetti's partner model is visible [85]); employer associations (Confindustria) [72]. Size and access UNKNOWN.
- Acquisition difficulty (SUPPORTED INFERENCE): high for a new, non-Italian entrant (language and professional-channel barriers).

### 4.8 Major risks and obvious weaknesses (O4)
1. **Italian reporting format not yet defined** (ministerial decree pending as far as found) [68][70].
2. **Narrow near-term segment:** the 100–149 band not until 2031 [69].
3. **Strong local incumbent** (Zucchetti) and SME-priced EU tools [80][84].
4. **Sensitive personal data**; the data-protection authority is involved, especially for employers below 50 [70][72].
5. **Political volatility** (Sweden; renegotiation pressure) [78].
6. **Methodological liability:** "work of equal value" judgments; worker-representative sign-off [69][71].

### 4.9 Validation questions still open (O4)
(No interviews possible in this session.)

| # | Question | Evidence that would answer it |
|---|---|---|
| V4-1 | Has Italy's ministerial decree on reporting modalities been adopted, and what format does it set? | Gazzetta Ufficiale / lavoro.gov.it monitoring |
| V4-2 | Number of Italian employers with 150–249 and 100–149 employees | ISTAT I.Stat extraction by size class |
| V4-3 | How will Italian 150–249 employers report: payroll-vendor module, consulente del lavoro, or a new tool? | Interviews with 10 consulenti del lavoro |
| V4-4 | Does Zucchetti HR PayGap cover NCBA categories and the final ministerial format, and at what price? | Demo and price enquiry |
| V4-5 | Greece as an alternative (obligations from 1 Nov 2026; Ombudsman platform): size and language feasibility | Hellenic Statistical Authority size-class data |
| **V4-6 (Agent 1 Q3)** | Will SMEs, worker representatives and equality bodies accept a deterministic job-evaluation method? Evidence so far: the EIGE toolkit offers voluntary, published methods including pair comparison for small organisations [79]; Axios uses the EG-Check method [80]; in Italy, NCBAs are the primary framework and internal systems may "only integrate — and not replace" them [69]; data are confirmed after consulting worker representatives [71]. Acceptance itself is **UNKNOWN**. | Interviews with 3–5 worker representatives or union officials and the Consigliera di parità; review of any guidance from the monitoring body; test whether an EIGE-method output is accepted in a mock joint pay assessment |
| **V4-7 (Agent 1 Q4)** | How far does Personio cover Arts. 5–10 in Italy, and at what price? Evidence so far: Personio publishes directive guidance and gender-pay-gap reporting features (snippets) [94]; Italian coverage, Art. 7 and Art. 10 support, and price are **UNKNOWN** (product and pricing pages returned HTTP 429). | Personio demo for an Italian 150–249 employer; price quote; check whether Personio runs Italian payroll or integrates with Italian payroll providers |

### 4.10 Assumptions requiring testing (O4)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O4-01 | Italian 150–249 employers need a tool beyond their payroll vendor's module | HYPOTHESIS | V4-3, V4-4 |
| MV-O4-02 | The Italian ministerial format will be published before 2027 reporting preparation begins | UNKNOWN (future event) | V4-1 |
| MV-O4-03 | A non-Italian small team can serve Italian employers credibly (language, NCBA, channel) | ASSUMPTION | V4-3 |
| MV-O4-04 | SMEs will pay above Axios's €3,000–€4,500/yr anchors | HYPOTHESIS (no evidence) | Pricing test |
| MV-O4-05 | Netherlands, Germany or France transpose by early 2027 | UNKNOWN (future event; NL uncertain; DE rumoured; FR before May 2027) [68][77] | Monitor |
| MV-O4-06 | A deterministic job-evaluation method is acceptable to worker representatives and equality bodies | HYPOTHESIS | V4-6 |

---

## 5. O3 — Awaab's Law (watchlist check)
No decisive new evidence. As far as the sources found show, Awaab's Law does not yet apply to the private rented sector, and the extension has no confirmed start date; commentators point to 2027 at the earliest (snippets, several) [88]. Phase 2 remains 30 Nov 2026. Agent 1's watchlist status and revival conditions are unaffected.

---

## 6. Cross-candidate comparison (restated after corrections; evidence strength only — no scores, no winner)

Each cell describes the **strength and direction of the evidence found**, not the attractiveness of the candidate. The "underserved" row uses the §1.4 standard for all three.

| Dimension | O1 CRA (SBOM-capable software SMEs) | O2 GB holiday-pay assurance | O4 Pay Transparency (Italy first) |
|---|---|---|---|
| Legal obligation in force | Strong — Art. 14 applies since 11 Sep 2026; SRP live [1][5] | Strong — records duty since Apr 2026 [45] | Strong in IT (7 Jun 2026) and GR (1 Nov 2026) [69][76]; absent in DE/FR/ES/NL |
| First hard deadline for the segment | Now (per event); Annex I from Dec 2027 | Records now; enforcement planned for 2027 [46] | 7 Jun 2027 for 150–249; 2031 for 100–149 [69] |
| Primary pain evidence | Moderate — ENISA surveys (readiness gaps, tool and template requests) [8][9] | Moderate–strong — DBT statement; vendor docs admitting manual steps; Xero idea (93 votes, switching threats) [45][50][51][54] | Weak — secondary, enterprise-weighted readiness surveys (snippets) [86] |
| Incumbent / free-tool gaps documented | Moderate — Dependency-Track lacks Art. 14 clock/SRP drafts; no SRP API [3][39] | Strong for Xero, Moneysoft, Sage 50 [50][51][54] | Weak — no complaint data found |
| Published SME-priced direct competitor covering the core job | Yes, partly — CVD Portal Reporting (€99/month) claims five of six functions (automated SBOM↔CVE alerts Enterprise-only); ConformOps (€79/month/product) three of six; Article 14 Ready two of six; two unpriced vendors claim more [22]–[26] | Yes, largely — paiyroll (15p/payslip, £30 minimum) claims five of seven functions for exactly the gap products; retention guarantee and companion multi-client view not found [49][90] | Yes — Axios (€3,000–€4,500/yr for 100–249, all EU); Zucchetti module (unpriced) [80][84] |
| Competitor traction published | None | Vendor-selected stories and testimonials (paiyroll) [89]; none independent | None |
| **Evidence the segment is underserved (§1.4)** | **Weak–Moderate** — gaps and SME tool demand documented; 2–3 SME-priced offers claim overlapping Art. 14 functions, none all six; traction UNKNOWN | **Weak–Moderate** — incumbent gaps strongly documented; a published SME-priced add-on claims G1–G5 for those products; uptake shown only by vendor-selected stories | **Weak** — SME-band tool at published prices; strong local incumbent; no complaint data |
| Free / public substitutes | Strong — Dependency-Track with EU KEV, SRP form, GitHub export; simplified documentation form required by law but undated [1][2][13][39] | Moderate now (free template and compliance check, GOV.UK entitlement calculator), possibly strong later (DBT considering a holiday-pay calculator) [45][47][90][91] | Moderate — EIGE toolkit (free method) [79] |
| Published price anchors | €79–€99/month (SME); $159/month; €2,500–€15,000/yr [22]–[29] | 15p/payslip, £30/month minimum; bureau payroll £50–£100 pcm (~£1–£2 per client) [49][90] | €3,000–€4,900/yr [80][81] |
| Willingness-to-pay signals | Mixed — financial support ties for top support request with templates (73.2%) [8]; no traction | Low but present — priced add-on with vendor-selected customers [49][89] | UNKNOWN |
| Buyer clarity | Moderate — product/security lead at a software SME (SUPPORTED INFERENCE) | Weak–moderate — employer liability; bureau route targeted by two vendors and one adviser comment; unresolved | Weak — HR vs consulente del lavoro vs payroll vendor |
| Channel evidence | Moderate — ENISA channel survey; developer communities [8][10] | Weak–moderate — vendor bureau targeting; user forums [51][56][90] | Weak — professional-channel content only |
| Segment size evidence | Weak — about a third of surveyed SMEs (all roles) report SBOMs; software-SME share UNKNOWN | Weak — ~1.23m UK zero-hours workers [A1 46]; employers by payroll product UNKNOWN | Weak — 22,861 IT firms at 50–249 (2021); 100–249 split UNKNOWN [74] |
| Gating unknowns | EUVD terms; glossary churn | Government calculator; final penalty regime | Italian reporting format |
| Legal-risk exposure of the product | Material (missed matches; compliance implication) | Material (calculation errors) | Material (equal-value categorisation; sensitive data) |

---

## 7. Evidence-quality summary

**Strongest evidence per candidate**
- **O1:** primary legal text and ENISA's own platform documentation define exactly what must be reported, how and when [1][2][3]; two ENISA surveys give primary adoption data [8][9]; vendor pricing pages and function claims were read verbatim [22][24].
- **O2:** the government's consultation (read verbatim) states the complexity, the penalty proposal, the Royal Assent limit and the self-audit incentive [45]; vendor documentation admits manual steps (Moneysoft, Sage 50) [50][54]; a Xero idea with 93 votes and dated user comments [51]; the direct competitor's capabilities, prices and bureau tiers were read verbatim [49][89][90][91].
- **O4:** the Italian decree's thresholds and dates (three secondary sources agree) [69][70][71]; a published SME-band price list [80]; ISTAT's size-class count (read) [74].

**Weakest evidence per candidate**
- **O1:** paying demand (no traction for any vendor; the HN thread is tiny); the software-SME SBOM share; how often actively exploited vulnerabilities occur in SME products; EUVD licensing.
- **O2:** add-on uptake beyond vendor-selected stories; buyer identity and bureau channel size; miscalculation prevalence; BrightPay/QuickBooks conflicts; forums unreachable.
- **O4:** the Italian reporting format; Italian SME demand; the 100–249 split; readiness surveys are snippet-only and enterprise-weighted; Personio coverage.

**Source mix.** §9 lists 94 numbered source entries (entry 67 unused), many grouping several URLs. Primary sources include the CRA OJ text, the ENISA glossary/FAQ/surveys, EUVD docs, the DBT consultation, GOV.UK pages, ISTAT, and products' documentation of their own features. Every price was read on the vendor's own page except those marked snippet and the Ravio, Lattice and PayAnalytics figures, which come from a third-party vendor list [83]. Snippet-only items: SECURE co-financing rate [12]; the BrightPay "will not calculate" statement [52]; Italian status items [72][73]; readiness surveys [86]; Awaab's Law PRS status [88]; the simplified-form blog [93]; Personio [94]; Italian SME HR tools [95]; several vendor capability claims [35]–[37], [62]–[66], [85].

**Items to re-read before external use:** [52], [72], [73], [86], [93], [94], and any Italian ministerial-decree status after 26 Sep 2026. The Italian and Greek transposition facts rest on law-firm summaries; the primary texts (Gazzetta Ufficiale / Normattiva; Greek FEK) should be read before any requirement is built on national details.

---

## 8. Consolidated open unknowns (for the Orchestrator's assumption registry)

| ID | Unknown | Candidate |
|---|---|---|
| MV-U01 | SBOM production share among CRA-relevant software-product SMEs (only whole-sample proxies exist) | O1 |
| MV-U02 | EUVD commercial-reuse terms | O1 |
| MV-U03 | Paying traction of any SME CRA tool | O1 |
| MV-U04 | Employer vs bureau buyer; number of UK payroll bureaus | O2 |
| MV-U05 | BrightPay and QuickBooks 52-week-rate automation in 2026-27 | O2 |
| MV-U06 | Whether DBT/FWA will publish a holiday-pay calculator, and when | O2 |
| MV-U07 | Italian ministerial decree on reporting format (adopted or not) | O4 |
| MV-U08 | Italian employer counts at 100–149 and 150–249 | O4 |
| MV-U09 | paiyroll add-on uptake (independent evidence) | O2 |
| MV-U10 | Adoption date and content of the CRA Art. 33(5) simplified documentation form | O1 |
| MV-U11 | Personio's Italian coverage and price | O4 |

---

## 9. Sources (accessed 2026-09-26 unless stated)

Grade: P / S / V. Access: **Read** = fetched and read (or extracted locally); **Snippet** = search-result summary only.

**CRA — law, regulator, surveys (O1)**
1. Regulation (EU) 2024/2847, OJ text (Arts. 14–16, 33(5)) — https://publications.europa.eu/resource/celex/32024R2847 — P, Read (local XHTML extraction)
2. ENISA, *CRA SRP Glossary*, "Version 1.3. Last update: 25 September 2026" — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/cra-srp-glossary2 — P, Read (HTML table parsed)
3. ENISA, SRP Frequently Asked Questions (EU Login/MFA; Primary and Secondary ARs; FAQ 15 API; FAQ 24 language) — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/frequently-asked-questions — P, Read (re-read verbatim in v2)
4. ENISA, Single Reporting Platform page — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp — P, Read
5. ENISA news, "The CRA Single Reporting Platform is launched", 11 Sep 2026 — https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched — P, Read
6. Help Net Security, 14 Sep 2026 — https://www.helpnetsecurity.com/2026/09/14/enisa-cra-single-reporting-platform/ — S, Read (supporting; [3] is now the cited source for AR facts)
7. sbomify, "The CRA Single Reporting Platform Opens Tomorrow…", 10 Sep 2026 — https://sbomify.com/2026/09/10/cra-single-reporting-platform-enisa-srp/ — V, Read (not relied on)
8. ENISA, *SME CRA Survey Report*, 24 Jun 2026 (CC BY 4.0) — https://www.enisa.europa.eu/sites/default/files/2026-06/SME%20CRA%20survey%20report.pdf — P, Read (local PDF)
9. ENISA, *SBOM Adoption State of Play – 2026*, June 2026 (CC BY 4.0) — https://www.enisa.europa.eu/sites/default/files/2026-06/SBOM%20Adoption%20State%20of%20Play%202026.pdf — P, Read (local PDF)
10. Linux Foundation, "The CRA Readiness Reality…", 19 Jun 2026 — https://www.linuxfoundation.org/blog/the-cra-readiness-reality-what-changed-and-what-didnt-between-2025-and-2026 — S, Read
11. European Commission, "CRA – MSMEs", last update 31 Jul 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-msmes — P, Read (cited in §2.8 Q4)
12. SECURE first open call — https://www.secure4sme.eu/cascade-funding/first-open-call — P, Read; co-financing rate — https://www.digitalsme.eu/fundings/open-call-for-smes-to-strengthen-cyber-resilience/ — S, Snippet
13. GitHub Docs, "Exporting a software bill of materials for your repository" — https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/exporting-a-software-bill-of-materials-for-your-repository — P, Read

**Vulnerability-data licences (O1)**
14. OSV, "Data sources" — https://google.github.io/osv.dev/data/ — P, Read
15. GitHub Advisory Database repository — https://github.com/github/advisory-database — P, Read
16. NIST NVD API Terms of Use, ScanCode LicenseDB reproduction (generated 21 Sep 2026) — https://scancode-licensedb.aboutcode.org/nist-nvd-api-tou.html — S, Read
17. ENISA EUVD public documentation — https://raw.githubusercontent.com/enisaeu/euvd-docs-public/main/apidoc.md and …/faq.md — P, Read
18. ENISA, Legal Notice — https://www.enisa.europa.eu/about-enisa/legal-notice/legal-notice — P, Read
19. CISA, KEV data repository (CC0) — https://github.com/cisagov/kev-data — P, Read
20. CVE Terms of Use (SPDX "cve-tou") — https://spdx.org/licenses/cve-tou.html — S, **Read** (upgraded in v2)

**CRA competitors and substitutes (O1)**
21. Cyber Vendor Guide, "CRA Compliance Companies (2026)", updated Aug 2026 — https://www.cybervendorguide.com/guides/cra-compliance — S, Read
22. ConformOps — https://conformops.eu ; https://conformops.eu/pricing ; https://conformops.eu/ai-info — V, Read (verbatim in v2)
23. Article 14 Ready — https://article14ready.com — V, Read
24. CVD Portal — https://cvdportal.com ; https://cvdportal.com/pricing — V, Read (verbatim in v2)
25. CRA Evidence — https://craevidence.com/platform ; https://craevidence.com/pricing — V, Read (verbatim in v2)
26. Kunnus — https://kunnus.tech/en — V, Read (verbatim in v2); Capterra — https://www.capterra.com/p/10036889/Kunnus/ — S, Read
27. sbomify pricing — https://sbomify.com/pricing/ — V, Read; repository metadata https://github.com/sbomify/sbomify — P, Read
28. Regulus — https://goregulus.com/ — V, Read; cost-calculator claims — https://goregulus.com/resources/cra-cost-calculator/ — V, Snippet
29. Zealience Z-CMS pricing — https://zealience.com/pricing/ — V, Read
30. Vulert pricing — https://vulert.com/pricing — V, Read
31. Aikido Security pricing — https://www.aikido.dev/pricing — V, Read
32. SBOM Observer — https://sbom.observer/ — V, Read
33. ReARM — https://rearmhq.com/ — V, Read
34. Distr pricing — https://distr.sh/pricing/ — V, Read (adjacent, §2.1 row 15)
35. UnitOne — https://unitone.ai/faq — V, Snippet
36. Interlynk (AWS Marketplace) — https://aws.amazon.com/marketplace/pp/prodview-n6mc7symiq2rm ; Cybeats — https://www.cybeats.com/product/sbom-studio — V, Snippet
37. Black Duck, "Are you ready: CRA reporting" — https://www.blackduck.com/resources/webinars/are-you-ready-cra-reporting.html — V, Snippet
38. EdgeLabs, "10 Best CRA Compliance Tools", 3 Aug 2026 — https://edgelabs.ai/blog/cra-compliance-tools — V, Read (cited in §2.1 row 15, §2.2, §2.8)
39. Dependency-Track 5.1.0, 31 Aug 2026 — https://dependencytrack.org/news/dependency-track-5-1/ — P, Read; repository metadata (Apache-2.0; 4,238 stars) — P, Read
40. Dependency-Track issue #5992 — https://github.com/DependencyTrack/dependency-track/issues/5992 — P, Read; issues #3178, #3268, #3063 — Snippet
41. Hacker News, Ask HN — https://news.ycombinator.com/item?id=49520688 — P (forum), Read
42. GitHub repository search "cyber resilience act" by stars — GitHub API, 2026-09-26 — P, Read
43. robertolocatelli81-dev/cra-evidence — https://github.com/robertolocatelli81-dev/cra-evidence — P, Read
44. Open Regulatory Compliance WG, CRA page — https://orcwg.org/cra/ — S, Read

**Holiday records and pay (O2)**
45. DBT, *Make Work Pay: Holiday Pay Compliance and Enforcement*, 30 Jun 2026, closed 22 Sep 2026 — https://assets.publishing.service.gov.uk/media/6a3e79add52550a19950f617/make-work-pay-holiday-pay-compliance-and-enforcement.pdf — P, Read (local PDF)
46. GOV.UK, *Fair Work Agency delivery plan 2026 to 2027*, first published 10 Aug 2026, updated 21 Aug 2026 — https://www.gov.uk/government/publications/fair-work-agency-delivery-plan-for-2026-to-2027/fair-work-agency-delivery-plan-2026-to-2027 — P, Read (dates from the GOV.UK content API); PAYadvice.UK summary — https://payadvice.uk/2026/08/12/fair-work-agency-delivery-plan/ — S, Read
47. GOV.UK, "Calculate holiday entitlement" — https://www.gov.uk/calculate-your-holiday-entitlement — P, Read
48. GOV.UK, "Holiday pay: calculate your average weekly pay if it varied", 6 Apr 2021 — https://www.gov.uk/government/publications/holiday-pay-calculate-your-average-weekly-pay-if-it-varied/holiday-pay-calculate-your-average-weekly-pay-if-it-varied — P, Read (cited in §3.2)
49. paiyroll, "Automated holiday pay for existing payroll software" (holiday pay companion) — https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ — V, Read (verbatim in v2)
50. Moneysoft, "Holiday Pay for irregular hours and part-year workers" — https://moneysoft.co.uk/support/holiday-pay-for-irregular-hours-and-part-year-workers/ — P, Read
51. Xero Product Ideas, "UK Payroll: Reporting – Run a report to calculate holiday pay based on a 52 week average" — https://productideas.xero.com/forums/967118-payroll-expenses/suggestions/45241594-uk-payroll-reporting-run-a-report-to-calculate — P (vendor forum), Read (all comments with authors and dates, v2)
52. BrightPay docs, "Annual Leave Entitlement Methods" (2025-26) — https://www.brightpay.co.uk/docs/25-26/annual-leave/annual-leave-entitlement-methods-in-brightpay/ — P, Read; "will not calculate holiday pay amounts" statement — https://www.brightpay.co.uk/docs/24-25/annual-leave/holiday-entitlements-useful-information/ — Snippet (not found in page text)
53. Staffology help: "Set up Average Holiday Pay schemes" (last updated 24 June 2026) — https://help.staffology.co.uk/payroll/leave-and-absence/holidays/average-holiday/configuring-average-hol.htm — P, Read (verbatim in v2); guide and "coming soon" pages — P, Read
54. Sage KB, "How do I calculate holiday pay rate for employees working variable hours?" (created 8 Mar 2023, last modified 4 Sep 2024) — https://gb-kb.sage.com/portal/app/portlets/results/viewsolution.jsp?solutionid=230308162057663 — P, Read (verbatim in v2); Sage Community Hub threads 254095, 209263 (Read), 219636 (Snippet)
55. QuickBooks Community thread 619909 — https://quickbooks.intuit.com/learn-support/en-uk/other-questions/holiday-pay-and-holiday-entitlement/00/619909 — P (vendor forum), Read
56. KeyPay (Employment Hero), "52 week averaging for holiday pay" — https://www.keypay.co.uk/features/52-week-averaging — P, Read (verbatim in v2)
57. IRIS Help Hub, Earnie Holiday Pay Module (updated 16 Feb 2026) — https://help-iris.co.uk/payroll/earnie/modules/hol/holiday-landing.htm — P, Read
58. StaffLeave — https://www.staffleave.com/blog/uk-holiday-pay-rules-2026 — V, Read
59. Employment Hero, six-year records rule (updated 18 Jun 2026) — https://employmenthero.com/uk/blog/six-year-records-rule-holiday-pay-compliance/ — V, Read
60. ATT, "Holiday pay – new record keeping requirements", 16 Jun 2026 — https://www.att.org.uk/employers/welcome-employer-focus/holiday-pay-new-record-keeping-requirements — S, Read
61. CIPP, "Employers must keep annual leave and pay records from 6 April", 30 Mar 2026 — https://www.cipp.org.uk/resources/news/annual-leave-and-pay-records-from-6-april.html — S, Read
62. RotaCloud, Planday, Fourth help pages — V, Snippet
63. Healthbox HR — https://healthboxhr.com/pricing — V, Snippet
64. Worker-side calculators (payslipchecker.uk, timetally.uk, uktax.tools, youtemp.co.uk) — V, Snippet
65. Azets — https://www.azets.com/en-uk/resources/new-holiday-pay-and-leave-record-keeping-requirements-from-6-april-2026 — S/V, Snippet
66. Payroll-outsourcing statistics aggregators — V, Snippet (low quality; not relied on)
67. (unused)

**Pay transparency (O4)**
68. Ius Laboris tracker, 23.09.26 — https://iuslaboris.com/insights/eu-pay-transparency-directive-which-countries-have-transposed/ — S, Read
69. Littler, Italy final decree guide — https://www.littler.com/news-analysis/asap/italy-implements-eu-pay-transparency-directive-guide-final-decree — S, Read
70. Edotto, 3 Jun 2026 — https://www.edotto.com/articolo/parita-retributiva-e-trasparenza-salariale-tutte-le-novita-del-decreto-definitivo — S, Read
71. EC News, 4 Jun 2026 — https://www.ecnews.it/lavoro/rapporto-di-lavoro/gestione-del-rapporto/gender-pay-gap-reporting-e-tutele-gli-adempimenti-previsti-dal-d-lgs-n-96-2026/ — S, Read
72. Italian status snippets (Altalex, IPSOA, Ministero del Lavoro, Garante opinion 26 Mar 2026) — S/P, Snippet
73. Rapporto biennale (lavoro.gov.it; MySolution; pmi.it) — P/S, Snippet
74. ISTAT, *Censimento permanente delle imprese 2023: primi risultati*, 14 Nov 2023 — https://www.istat.it/it/files/2023/11/REPORTCensimprese.pdf — P, **Read** (upgraded in v2; local PDF)
75. Lewis Silkin, "Pay Transparency Directive FAQs", 25 Jun 2026 — https://www.lewissilkin.com/insights/2026/06/25/pay-transparency-directive-faqs — S, Read
76. Lewis Silkin, "Greece transposes…", 13 Jul 2026 — https://www.lewissilkin.com/insights/2026/07/13/greece-transposes-the-eu-pay-transparency-directive-what-employers-need-to-know — S, Read; Jackson Lewis, Zepos — S, Snippet
77. People Performance Reward, 2 Sep 2026 — https://www.people-performance-reward.co.uk/post/eu-pay-transparency-directive-update-september-2026 — S/V, Read
78. Pinsent Masons, Sweden, 20 Apr 2026 — https://www.pinsentmasons.com/out-law/news/sweden-not-implement-eu-pay-transparency-directive — S, Read
79. Baker McKenzie, EU toolkit, 7 Apr 2026 — https://www.bakermckenzie.com/en/insight/publications/2026/04/european-union-toolkit-launched-to-support-pay-transparency-compliance — S, Read
80. Axios Analytics pricing — https://axiosanalytics.com/pricing — V, Read
81. Evenpay pricing — https://evenpay.io/pricing/ — V, Read
82. Figures pricing — https://figures.hr/pricing — V, Read (no figures); starting-price snippet — Snippet
83. effy.ai, "Pay Equity Software: 15 Tools and 2 Published Prices", 23 Sep 2026 — https://www.effy.ai/blog/pay-equity-software — V, Read
84. Zucchetti HR PayGap — https://www.zucchetti.it/it/cms/soluzioni/software-hr-zucchetti/hr-core-platform/software-trasparenza-retributiva/software-trasparenza-retributiva.html — V, Read
85. TeamSystem, Inaz, Veridian, errepi pages — V, Snippet
86. Readiness surveys (Aon 2026 Pulse; Mercer 2026; Littler 2025) via secondary summaries — S, Snippet
87. GitHub repository searches "pay transparency" EU directive; "holiday pay" uk — GitHub API, 2026-09-26 — P, Read

**Awaab's Law (O3)**
88. Awaab's Law PRS status: https://www.russell-cooke.co.uk/news-and-insights/news/awaab-s-law-extending-safety-standards-to-the-private-rented-sector ; https://www.nrla.org.uk/news/how-to-prepare-for-awaabs-law-as-a-private-landlord — S, Snippet

**Added in v2**
89. paiyroll, "Customer Success Stories" — https://paiyroll.com/customers/ — V, Read (vendor-selected stories and testimonials)
90. paiyroll, bureau pricing (tiers, FAQ incl. Northern Ireland reference period, free "Holiday Pay Compliance Check") — https://paiyroll.com/payroll-bureau-pricing/ — V, Read
91. paiyroll, free holiday pay compliance checker, free holiday pay template, payroll audit — https://paiyroll.com/free-holiday-pay-compliance-checker/ ; https://paiyroll.com/free-holiday-pay-template/ ; https://paiyroll.com/payroll-audit/ — V, Read
92. SaM Solutions, "Three CRA Scenarios: What the Cyber Resilience Act Means for Your Business", 27 Feb 2026 — https://sam-solutions.com/blog/what-the-cyber-resilience-act-means-for-your-business/ — V/S, Read; contrasting guides (e.g., https://cra-facts.com/penalties ; https://konvu.com/blog/cra-readiness-checklist) — Snippet
93. Regara, "How to write CRA technical documentation as an SME: the simplified form" — https://www.regara.eu/blog/cra-technical-documentation-sme — V, Snippet
94. Personio directive pages — https://www.personio.com/blog/eu-pay-transparency-directive/ ; https://www.personio.com/whats-new-q1-26/ — V, Snippet (HTTP 429 on direct fetch)
95. Italian SME HR tools with directive content: https://www.jethr.com/risorse/legge-trasparenza-salariale-cosa-cambia-da-giugno-202/ ; https://www.fluida.io/blog/trasparenza-salariale-busta-paga-2026 ; TracefyHR, employsome guides — V, Snippet

**Agent 1 sources referenced, not re-read:** [A1 3] CRA corrigendum; [A1 16] Commission refusal to delay; [A1 38] Interlynk C/C++ SBOM report; [A1 45] CIPP 2024 survey (snippet); [A1 46] ONS EMP17.

---

## 10. Out-of-scope findings (reported to the Orchestrator)

| ID | Finding | Responsible agent |
|---|---|---|
| OOS-MV-01 | The approved v2 (O4 status) says Ius Laboris treats only Italy as transposed. Sources read here record Malta, Lithuania and Slovakia (by 7 Jun 2026) and Greece (Law 5316/2026, 6 Jul 2026; obligations from 1 Nov 2026) as transposed, and Sweden as paused. v2 has not been edited. | Orchestrator; Agent 1 (if reopened); Agent 3 |
| OOS-MV-02 | ENISA's SRP glossary moved from v1.1 (5 Sep 2026) to v1.3 (25 Sep 2026) in three weeks. Any O1 field schema must be versioned, and the UI must show the glossary version used. | Agent 9 Architecture; Agent 4 Requirements |
| OOS-MV-03 | EUVD has no licence or terms of use in its docs or app; ENISA's general legal notice may or may not apply, and EUVD contains third-party data. Get written confirmation from ENISA before commercial use. Ubuntu (via OSV) is CC-BY-SA 4.0; GHSA/PyPI/Go are CC-BY 4.0; the NVD API requires a specific non-endorsement notice; CVE requires MITRE's copyright designation and licence. | Agent 14 Legal & Privacy; Agent 9 |
| OOS-MV-04 | DBT lists a holiday-pay calculator or self-assessment tool among the support it is considering, and the FWA plans "guidance and tools". This is a strategic commoditisation risk for O2. | Agent 3 Strategy |
| OOS-MV-05 | FWA exposure is limited to underpayments after 18 Dec 2025, and the "no penalty if repaid before investigation" rule is only a proposal. Marketing must not claim six years of exposure or promise penalty avoidance. | Agent 7 Marketing; Agent 14 |
| OOS-MV-06 | The CRA market contains misinformation that SMEs cannot be fined for Art. 14 deadlines [92]. Only micro and small enterprises are exempt, and only from fines for the 24-hour early-warning deadline. Copy must state this precisely. | Agent 7; Agent 14 |
| OOS-MV-07 | Competitors in all three candidates market AI features (ConformOps optional OpenAI proposals, CVD Portal Enterprise AI triage, cra-agent, UnitOne, AI pay-transparency prototypes). "AI-free" is a positioning choice; no evidence yet that buyers value it. | Agent 3; Agent 7; Agent 19 Runtime Independence |
| OOS-MV-08 | An Art. 14(7) "which CSIRT is your coordinator" helper (main establishment; non-EU fallback rules) would border on legal advice. | Agent 14; Agent 4 |
| OOS-MV-09 | Research tooling notes: the ENISA glossary is readable at `…/cra-srp-glossary2`; the EUVD docs are Markdown files at `raw.githubusercontent.com/enisaeu/euvd-docs-public/main/`; the NVD terms are readable via ScanCode LicenseDB; GOV.UK publication dates are available from `https://www.gov.uk/api/content/<path>`; UserVoice (Xero Ideas) comments can be parsed with authors and dates from the raw HTML. | All research agents; Orchestrator |
| OOS-MV-10 | O4 in Italy processes pay data by sex; the Garante's involvement and rules for employers below 50 to prevent re-identification will shape data design (DPIA). | Agent 13 Security; Agent 14; Agent 10 Database |
| OOS-MV-11 | paiyroll's FAQ states a 12-week reference period can be specified for Northern Ireland [90]. If O2 is chosen, NI must be excluded or handled with separate rules; the NI records-duty question (A-18) is still open. | Agent 3; Agent 14 |

---

## 11. Revision log (Judge 2 findings on v1 → changes in v2)

| Finding | Severity | Accepted? | What changed in v2 (sections) |
|---|---|---|---|
| **J2-001** | HIGH | Accepted | paiyroll's companion, bureau, customer and free-service pages were re-read verbatim [49][89][90][91]. §3.1a paiyroll row rewritten: 104-week lookback and historic import, pay-item selection, "complete audit trail" via XLSX reports, per-booking records per pay run, and integrations including Xero, Sage 50, BrightPay and Moneysoft, all quoted. §3.6 rewritten: calculation, 104-week lookback and calculation audit trail are stated as already offered; only a retention/immutability guarantee, an FWA-oriented pack, a companion multi-client view and a post-18-Dec-2025 arrears self-check remain, all as HYPOTHESES; "the one thing not described by paiyroll's page" deleted. KeyPay restated in §3.1a/§3.1b with the rate floor, the missing-data notification and the stored calculation breakdown, and removed from complaints (§3.5). New §1.4 defines one under-service standard; §2.0(b) and §3.0(b) apply it to O1 (F1–F6) and O2 (G1–G7); both are rated "Weak–Moderate" in §6. The v1 sentence "By contrast, O2 has documented incumbent gaps" was replaced. |
| **J2-002** | MEDIUM | Accepted | New §2.1a maps each O1 vendor's *published* claims to F1–F6 from verbatim re-reads of CVD Portal, ConformOps, CRA Evidence and Kunnus. §2.0(b), §2.2 closing note, §2.7 and §6 now name only CVD Portal, ConformOps and Article 14 Ready as SME-priced offers with Art. 14 clocks, put CRA Evidence and Kunnus in an "unpriced" group, and record that CVD Portal's automated SBOM↔CVE alerts are Enterprise-only. "Weak / contradicted" replaced by "Weak–Moderate … traction UNKNOWN". |
| **J2-003** | MEDIUM | Accepted | §3.3 adds paiyroll's bureau payroll tiers (£50/£75/£100 pcm, holiday-pay schemes in all tiers; stated as full-payroll tiers) and a per-client illustration. §3.1a traction column adds the customer-stories page and the "Recommend Paiyroll for Bureaus" testimonial (V, vendor-selected). §3.2 adds the free Holiday Pay Compliance Check, the free template and the Payroll Audit service. §3.1c rewrites buyer identity with the adviser comment ("stopping our client using Xero payroll"), KeyPay's bureau/accountant targeting and paiyroll's bureau offer; the conclusion stays HYPOTHESIS. V2-1, V2-4 and V2-5 revised. |
| **J2-004** | LOW | Accepted | §2.4 D2, §2.9 item 4 and §6 now say financial support is the "joint highest" item (142, 73.2%), tied with templates for technical documentation, quoting ENISA's key findings and "Practical templates are the most requested form of support". |
| **J2-005** | LOW | Accepted | All Xero quotes re-extracted with authors and dates and quoted verbatim (e.g., "I am in the process of switching payroll from Xero to Healthbox HR to comply with the law, which is a major inconvenience."; "I too am starting to look elsewhere for better software."; "I would have thought that something that has been a legal requirement since 2020, should have the highest priority"). The Healthbox row says "is switching". Staffology quote corrected to "Only one exclusion option can be selected at a time". A quotation rule is stated in the header; unverified vendor phrases were paraphrased without quotation marks (e.g., ATT, Italian monitoring body, Axios features). |
| **J2-006** | LOW | Accepted | (a) ESTIMATE and PREDICTION removed; arithmetic labelled SUPPORTED INFERENCE; future events labelled UNKNOWN (future event). (b) AR limits now cited to the ENISA FAQ [3], quoted verbatim. (c) effy.ai moved from complaints to §4.3 and limited to its list. (d) "Free" for the DBT tool labelled SUPPORTED INFERENCE (§3.2). (e) CRA misinformation now cited to SaM Solutions (27 Feb 2026) [92], read verbatim. (f) "EU/Hetzner": CVD Portal homepage "EU hosted" [24]; Hetzner and operator from [21]. (g) FWA plan dates corrected to first published 10 Aug 2026, updated 21 Aug 2026 [46]. (h) [11] cited in §2.8 Q4; [34] and [38] cited in §2.1 row 15, §2.2 and §2.8; [48] cited in §3.2. (i) ISTAT upgraded to Read with the verbatim figure and scope [74]; CVE ToU also upgraded to Read [20]. |
| **J2-007** | LOW | Accepted | MV-O1-01 reworded to "about one third of surveyed SMEs (all roles) report implementing SBOMs; the share among CRA-relevant software-product SMEs is unknown" and labelled UNKNOWN with a whole-sample proxy; §2.0 conclusion and §6 aligned; MV-U01 reworded. |
| **J2-008** | LOW | Accepted | O1 Q6 answered in §2.8 Q4 from [11] and the CRA Art. 33(5) text (the Regulation says "shall", the Commission page says "may"; no date; status UNKNOWN; free-provision risk noted in §2.9) with V1-9 and MV-U10 added. O4 Q3 and Q4 added as V4-6 and V4-7 with current evidence, plus MV-O4-06 and MV-U11. |

**Disagreements with Judge 2:** none. One nuance: the judge counted paiyroll's integrations as 19; the page read on 2026-09-26 lists 18 named payroll formats, and v2 uses that count.
