# Market & Competitive Validation — v1

| Field | Value |
|---|---|
| Artifact | `project/research/market-validation-v1.md` |
| Owner | Agent 2 — Market & Competitive Validation |
| Research date | 2026-09-26. Every price, status and capability is "as seen on 2026-09-26" unless a source date is given. |
| Status | DRAFT v1 — submitted for independent judging |
| Input (approved) | `project/research/opportunity-research-v2.md` (Agent 1, APPROVED); open finding **J1-013** from `project/judges/judge-01-opportunity-research-v2.md`, forwarded to Agent 2 (resolved in §2.0) |
| Candidates | **O1** EU CRA vulnerability-handling / Art. 14 reporting-clock and evidence workspace for SBOM-capable software-product SMEs · **O2** Great Britain holiday-record and holiday-pay assurance for variable-hours employers · **O4** EU Pay Transparency compliance for SME / lower-mid-market employers in a transposed jurisdiction (conditional) · O3 Awaab's Law (watchlist check only) |
| Out of scope for this artifact | Choosing the winner, product strategy, pricing, requirements, building anything. No numerical market scores are given. |

### Evidence labels and grades

| Label | Meaning here |
|---|---|
| **VERIFIED [n]** | Stated by the cited source. The source was **Read** in this session (fetched page, or PDF/XHTML/xlsx extracted locally), or at least **two independent snippets** agree. Snippet-only claims are always marked "(snippet)". |
| **SUPPORTED INFERENCE** | My reasoning from verified facts; the reasoning is stated. |
| **ASSUMPTION** | Taken as true without evidence; must be tested. |
| **HYPOTHESIS** | Testable proposition about customers, demand or behaviour. |
| **PREDICTION** | Statement about a future event. |
| **UNKNOWN** | Not established in this session. |
| **ESTIMATE** | An illustrative number I computed; not a source figure. |

Source grades in §9: **P** primary/official (legislation, regulator, government, the product's own documentation for its own features), **S** reputable secondary (law firm, professional body, trade press, independent directory), **V** vendor marketing page (shows only what a vendor *claims* or *publishes*; a V page can verify a *published price*, never a legal fact or a market fact). "[A1 n]" means source *n* of Agent 1's approved v2, not re-read by me.

No customer, statistic, price or quote in this artifact is invented. No customer interviews, surveys or pricing tests were possible in this session.

---

## 1. Scope & method

### 1.1 Scope
For each of O1, O2 and O4: (1) competitor matrix, (2) alternatives and substitutes, (3) pricing evidence, (4) market and demand evidence, (5) complaints and feature gaps, (6) differentiation opportunities, (7) switching costs, saturation and acquisition, (8) risks and weaknesses, (9) open validation questions, (10) assumptions. Plus the candidate-specific questions in the assignment, a cross-candidate evidence comparison (§6), an evidence-quality summary (§7), sources (§9) and out-of-scope findings (§10). O3 was checked only for decisive new evidence (§5).

### 1.2 Method
- **Search angles used for every candidate:** vendor category queries; "alternatives to X"; vendor pricing pages (read directly); directories and review sites (Cyber Vendor Guide, Capterra, G2, AlternativeTo, effy.ai buyer list); product-idea boards and community forums (Xero Product Ideas, Sage Community Hub, QuickBooks Community, Hacker News); GitHub repository and issue search (via GitHub API, 2026-09-26); regulator and government pages; national-language queries (Italian for O4).
- **Primary documents read locally:** CRA OJ text (Art. 14–16) via `publications.europa.eu/resource/celex/32024R2847`; ENISA *CRA SRP Glossary v1.3* (HTML table parsed); ENISA *SME CRA Survey Report* (PDF); ENISA *SBOM Adoption State of Play 2026* (PDF); EUVD public API/FAQ documentation (Markdown files served to the EUVD web app); DBT *Make Work Pay: Holiday Pay Compliance and Enforcement* consultation (PDF).
- **Vendor pages:** every price in §2.3, §3.3, §4.3 was read on the vendor's own pricing page unless marked "(snippet)".
- **Duplicated checks:** where a status claim came from one secondary source, I looked for a second (e.g., Greece's transposition; Sweden's postponement; SRP onboarding details).

### 1.3 Limitations
- **No primary customer research** (interviews, landing-page or pricing tests). All demand statements about segments are HYPOTHESES until tested.
- Most web pages were read through a summarising fetch tool. Load-bearing legal/regulatory texts (CRA Art. 14, SRP glossary, ENISA surveys, DBT consultation) were extracted and read verbatim locally.
- **Unreadable (HTTP 403/redirect):** AccountingWEB "Any Answers", Crowell & Moring CRA alert, BrightPay support hub (brightsg), IT Security Guru, Altalex (login), AlternativeTo, ENISA glossary URL `…/cra-srp-glossary` (the `…/cra-srp-glossary2` URL worked), nvd.nist.gov (JavaScript-only; read via ScanCode's reproduction).
- **Reddit** threads did not surface through the search tool (including `site:reddit.com` queries); absence of Reddit evidence is **not** evidence of absence.
- Vendor pages are self-descriptions; none of the CRA or holiday-pay vendors publishes customer counts.
- National-language coverage: Italian sampled for O4; German, Spanish, French not sampled.

---

## 2. O1 — EU CRA vulnerability-handling, Art. 14 reporting-clock and evidence workspace

### 2.0 Resolution of forwarded finding J1-013 (segment definition, criterion (c), competitor asymmetry)

**(a) Segment wording — "already produce" vs "can export" SBOMs.** The two describe different populations:

| Evidence | What it shows | Label |
|---|---|---|
| ENISA SME CRA survey (n=194 SMEs; fieldwork Feb–Mar 2026): SBOM used by 67 respondents (34.54%); "None" 21 (10.82%); no answer 20 (10.31%). Roles (multi-select): software developer 80 (41.24%), service provider/integrator 53 (27.32%), product manufacturer 39 (20.10%), importer/distributor 33 (17.01%) [8] | Whole-sample SME figure. I found **no role-by-practice cross-tabulation** in the report text, so the SBOM share of software-developer SMEs specifically is not published. | VERIFIED [8]; cross-tab UNKNOWN |
| ENISA *SBOM Adoption State of Play 2026* (n=334, end-2025; >65% large, micro+small only 16%): "10 % of the respondents do not generate SBOMs at all"; manual SBOM processes ~11% overall, 16% in micro; formats CycloneDX 44%, SPDX 29%, 11% no standard format, 17% proprietary; micro 23% and small 25% report "mature" adoption vs medium 4% and large 6% [9] | Skewed to large firms; the micro/small subsample is small, and for micro respondents the second-most common engagement was "providing SBOM tools, solutions and/or integration services" — i.e., the micro sample includes SBOM vendors. The micro/small maturity figure is therefore **not** representative of CRA-affected SMEs. | VERIFIED [9]; representativeness caveat is SUPPORTED INFERENCE |
| Linux Foundation Research CRA readiness 2026: "The share of respondents producing Software Bill of Materials (SBOMs) for all products held at 32%" [10] | Open-source-ecosystem sample, not SME-specific; sample size not stated in the blog. | VERIFIED [10] (S) |
| GitHub exports an SPDX 2.3 SBOM from the dependency graph via UI or REST API [13] | For package-managed code hosted on GitHub, *exporting* an SBOM is available without extra tooling; completeness is not assured (ENISA: 62% rate completeness "quite a lot or extremely difficult") [9]. | VERIFIED [13][9] |

**Conclusion (SUPPORTED INFERENCE).** "Already produce SBOMs" is roughly a third of surveyed organisations in two independent surveys (34.5% [8]; 32% "for all products" [10]) — and those are the more mature firms. "Can export" is larger (any package-managed product can emit one with free tooling [13]) but its size is **UNKNOWN**, because the share of CRA-relevant SME products that are package-managed rather than firmware/embedded is unmeasured (A-19 in Agent 1's v2 remains UNKNOWN).

**Recommended single segment definition (for Agent 3 to adopt or reject; I do not set strategy):** *"EU-market software-product SMEs — software developers, and connected-device makers whose application layer is package-managed — whose build tooling can export CycloneDX or SPDX SBOMs."* Two sub-segments should be tracked separately in validation:
- **S1 — already producing SBOMs** (about one third of surveyed firms; evidence moderate).
- **S2 — can export but do not yet produce** (size UNKNOWN). The MVP can serve S2 only after the customer adds an SBOM-generation step (e.g., GitHub export [13], or an SBOM GitHub Action [13]); this is onboarding friction, not a solved problem.

**(b) Criterion (c) "evidence the segment is underserved".** The 34.5% SBOM and ">70% want templates" figures [8] are whole-sample and cannot show that S1 is underserved. Applying the **same standard used for O2** (where one dedicated add-on counted against O2), the competitive record for O1's MVP job is at least as dense (§2.1):
- **CVD Portal** "Reporting" tier, **€99/month billed annually (€1,188)**: Art. 14 24h/72h/14d workflow, "SRP-ready submission package", SBOM registry, CVSS scoring, remediation-decision tracking, CSAF 2.0 export, NVD and EUVD feeds [24].
- **ConformOps**, **€79/month per product** continuous monitoring (daily dependency monitoring, reads CycloneDX, Art. 14 early-warning and 72-hour workflows); **€249/month for five products**; €99 one-off assessment; free preview for 2 products [22].
- **sbomify** Business **$159/month billed annually** (5 products, daily re-scans, CRA Compliance Wizard) [27]; **Article 14 Ready** free field compiler plus €79 dry run [23]; **CRA Evidence** and **Kunnus** with Art. 14 workflows (price on request; free trial) [25][26]; **OWASP Dependency-Track** free, now mirroring CISA and ENISA EU KEV catalogues [39].

**Result.** On the artifact's own framing, criterion (c) cannot be scored in O1's favour: the evidence shows **contested, SME-priced direct overlap**, not under-service (SUPPORTED INFERENCE). By contrast, O2 has *documented* incumbent gaps in widely used SME payroll products (§3.1). This changes the evidence under one of the three edges Agent 1 gave O1; the ranking decision itself belongs to Agent 3, and Agent 1's switch condition ("if SBOM-capable software SMEs will not pay more than free tooling plus the €79–€99 one-off offers, O2 should lead") is untested because no pricing interviews were possible.

**(c) Competitor asymmetry.** ConformOps' €79/month/product monitoring and €249/month portfolio plan, and CVD Portal's €99/month Reporting tier, are now recorded as direct competitors and price anchors in §2.1 and §2.3.

### 2.1 Competitor matrix (direct)

All prices are as published on 2026-09-26 unless stated. "Traction" lists only what is published.

| # | Name / URL | Target segment (as claimed) | Capabilities relevant to O1's job | Published pricing | Hosting / region (if stated) | Published traction | Grade |
|---|---|---|---|---|---|---|---|
| 1 | **CVD Portal** — cvdportal.com | EU manufacturers, importers, distributors | Art. 13 disclosure intake (free); Art. 14 24h/72h/14d workflow; "SRP-ready submission package"; SBOM registry; CVSS 3.1/4.0; remediation decisions; CSAF 2.0 advisory export; NVD + EUVD feeds; "final submission remains a manual human action"; automated SBOM-to-CVE alerts listed only in Enterprise | Free €0 (intake); **Reporting €99/mo billed annually €1,188**; Compliance €299/mo (€3,588/yr; 3 products then €99/mo each); Enterprise on quote [24] | "EU/Hetzner" [24]; operator Porta Regulus B.V. (NL), founded 2026 [21] | None published | V (read) [24]; S [21] |
| 2 | **ConformOps** — conformops.eu | Small software teams | GitHub App / ZIP static repository analysis; reads CycloneDX; daily dependency monitoring; Art. 14 early-warning and 72-hour workflows; evidence traceability to files/commits; release deltas | Free preview (2 products); **€99 per product one-off**; **€79/mo per product** ("€790/year equivalent"); **€249/mo for five products** [22] | Not stated on site; operator based in Italy per [21] | None published | V (read) [22]; S [21] |
| 3 | **Article 14 Ready** — article14ready.com | Product-security teams preparing Art. 14 reports | Browser-local stage-aware field compiler ("Incident entries stay in this browser"); deadline calculation from awareness time; Markdown/JSON export; aligned to "ENISA's SRP Glossary v1.1, dated 5 September 2026"; explicitly "not the official SRP" and does not submit | Field compiler free per [21] (site wording "one-time purchase" is ambiguous); **"24h Dry Run" €79 excl. VAT** one-off [23] | Operator PEAK Consulting Services GmbH, Mannheim (DE) [21] | None published | V (read) [23]; S [21] |
| 4 | **CRA Evidence** — craevidence.com | Manufacturers, importers, distributors | CycloneDX 1.6 / SPDX 2.2+ ingest; HBOM; VEX authoring; feeds: CVE List (hourly), OSV, CISA KEV, EPSS, ENISA EUVD (daily); 24h/72h/14d/30d reporting with "structured payloads for ENISA Single Reporting Platform"; support-period tracking | **Custom** for all plans; 14-day free trial [25] | Not disclosed | None published | V (read) [25] |
| 5 | **Kunnus** — kunnus.tech (Think Ahead Technologies GmbH) | Startups, SMEs, enterprises; 9 industries incl. software/SaaS | Product inventory & classification; SBOM generation (CycloneDX/SPDX); vulnerability tracking; ENISA reporting workflow; supplier portal; EU DoC | Not published; "Reduced licensing for early stages" [26] | "Built in Germany, hosted exclusively with European providers" [26] | Capterra: 0 reviews [26] | V (read) [26] |
| 6 | **sbomify** — sbomify.com (open-source core) | OSS maintainers (free); mid-size teams | SBOM/CBOM hub; OSV scanning (weekly free, daily paid); Dependency-Track integration; CRA scope screening and 5-step CRA Compliance Wizard; blog on SRP | Community $0 (1 product, 5 components); **Business $159/mo billed annually** (5 products, 200 components); Enterprise custom [27] | Not stated; self-hostable | GitHub repo 60 stars; licence "Other" [27] | V (read) [27] |
| 7 | **Regulus** — goregulus.com | Manufacturers, IoT and embedded teams | Applicability, classification, Annex II/VII templates, requirement matrices, vulnerability workflow "from detection to coordinated disclosure" | Basic **€2,500/yr**; Pro **€15,000/yr**; Enterprise custom; "early access" [28] | Not disclosed | None | V (read) [28] |
| 8 | **Zealience Z-CMS** — zealience.com | Radio/IoT makers (EN 18031, RED DA, CRA) | CRA gap analysis, vulnerability-handling policy, risk assessment; free CRA templates on GitHub | **€4,000/yr per licence** (1–4), graduated to €1,000/yr (76–100) [29] | Frankfurt (DE) [29] | Templates repo 36 stars [42] | V (read) [29] |
| 9 | **Vulert** — vulert.com | Small dev teams | Manifest/SBOM upload; hourly vulnerability monitoring; PDF/audit reports; SBOM export add-on; no Art. 14 workflow found | Pro **$15/mo per app** ($13 annual); Growth $25/mo; SBOM Export add-on $13/mo; 30-day trial [30] | Not stated | None | V (read) [30] |
| 10 | **Aikido Security** — aikido.dev | Developer teams | SCA/SAST/secrets; SBOM and VEX export; CRA content; no Art. 14 workflow found | Developer **$0** (2 users, 10 repos); Basic $300/mo; Pro $600/mo [31] | Not stated | None on pricing page | V (read) [31] |
| 11 | **SBOM Observer** (Bitfront AB, SE) — sbom.observer | Software teams | SBOM management; policies mapped to CRA/DORA/NIS2; VEX; on-prem option | Not shown in content read [32] | Not stated | ~10 customer logos [32] | V (read) |
| 12 | **ReARM** (Reliza) — rearmhq.com | Release governance | SBOM/xBOM per release, findings roll-up, VDR; CE open source | Pro price not shown [33] | Self-host or managed | None | V (read) |
| 13 | Enterprise / firmware SBOM platforms: **ONEKEY** (firmware analysis; "Platform subscription + advisory"), **Cybeats SBOM Studio**, **Interlynk** (priced by active developers, AWS Marketplace), **Anchore**, **Finite State**, **Black Duck** (flags EUVD exploitability; "Are you ready: CRA reporting" webinar), **Keysight SBOM Manager** | Device makers / enterprise | SBOM generation incl. binaries, VEX, vulnerability management | Quote-only [21][36][37] | Various | None published | S [21]; V (snippet) [36][37] |
| 14 | Test/certification/consulting: **pi3g** (DE, embedded Linux), **Bureau Veritas**, **DEKRA**, **SGS**, **TÜV SÜD**, **BearingPoint** | Manufacturers needing assessment | Gap assessment, testing, conformity advice | Quote-only [21] | EU labs | None | S [21] |
| 15 | Adjacent, AI-centric: **UnitOne** (AI-agent gateway capturing "Article 14-style" evidence; Team $99/mo), **cra-agent** (GitHub, "autonomous agentic AI for CRA", 452 stars, created 10 Aug 2026) | AI-agent users / developers | Evidence capture; AI triage/auto-fix | $0 / $99/mo (snippet) [35]; OSS [42] | Customer cloud [35] | Stars only [42] | V (snippet) [35]; P [42] |

**Traction (all rows).** No CRA vendor in this list publishes a customer count or named SME case study. Kunnus has 0 Capterra reviews [26]. A dominant SME-focused leader is **UNKNOWN**; I found no evidence that one exists (and absence is not proof).

### 2.2 Alternatives and substitutes

| Substitute | Cost | What it covers | Where it breaks (for the O1 job) | Label |
|---|---|---|---|---|
| **OWASP Dependency-Track** (Apache-2.0; 4,238 GitHub stars, 817 forks, 1,041 open issues on 2026-09-26) | Free; self-hosting effort | SBOM ingest, component analysis against NVD/OSV/GHSA, VEX; **v5.1.0 (31 Aug 2026) "mirrors the CISA and ENISA EU KEV catalogs out of the box"**, and KEV status can drive policies and notifications; release notes explicitly reference the CRA reporting clock | No Art. 14 clock or SRP-field packaging found in the release notes; false positives from CPE matching, with suppression only per project and version (issue #5992, opened 2 Apr 2026, open) | VERIFIED [39][40] |
| **ENISA SRP web form + Glossary** | Free (mandatory channel) | The form itself guides the 39+ fields; later stages "by default copied from previous step" | No API at initial release; English only; no SBOM matching or evidence retention | VERIFIED [2][3] |
| **GitHub dependency-graph SBOM export** | Free | SPDX 2.3 export via UI/REST; SBOM GitHub Actions (e.g., Anchore SBOM Action) | Export only; no triage, clocks or evidence; completeness depends on manifests | VERIFIED [13] |
| **Small OSS CRA tools**: `crawatch.dev` (free CLI + GitHub Action failing builds when a dependency is on CISA KEV; created 18 Sep 2026), `cra-evidence` (AGPL-3.0; Art. 14 clock and SRP field schema; 0 stars; README says it was written by an AI agent), `CycloneDX.CRA.Validator` (BSI TR-03183-2 validation), `DX.Comply` (Delphi CycloneDX SBOMs, 56 stars) | Free | Fragments of the job | Very low adoption; single maintainers | VERIFIED [42][43] |
| **Article 14 Ready free compiler** | Free / €79 dry run | Stage-aware field drafting in the browser | No SBOM link, no persistence by design | VERIFIED [23] |
| **Templates and guidance**: ENISA helpdesk and guidance; Zealience free CRA templates; ORC WG FAQ and learning hub; OpenChain CRA-Compliance framework (18 stars) | Free | Process templates | Manual; no automation | VERIFIED [5][42][44] |
| **Spreadsheets + consultants / test labs** | Consultants quote-only [21]. Regulus's calculator assumes €85/h engineering cost (vendor claim) [28] | Anything | Cost; episodic; no continuous monitoring | VERIFIED [21]; [28] is V |
| **Grant-funded services**: SECURE project first open call, "up to € 30.000" per SME, €5m call budget (closed); 50% co-financing (snippet) | Subsidy | Funds CRA compliance activities | Whether SaaS subscriptions are eligible costs is UNKNOWN (Annex 2 not read) | VERIFIED [12]; co-financing rate snippet [12] |

SUPPORTED INFERENCE: none of the **free** options found combines SBOM matching, actively-exploited triggers, Art. 14 clocks from the awareness timestamp, SRP-glossary-aligned drafts, Art. 14(8) user notification and evidence retention. Several **paid SME-priced** tools claim to (rows 1–5 of §2.1).

### 2.3 Pricing evidence (all published; date seen 2026-09-26)

| Offer | Price | Unit / scope | Source |
|---|---|---|---|
| ConformOps Free | €0 | up to 2 preview products | [22] V |
| ConformOps Full Assessment | €99 | once, per product | [22] V |
| ConformOps Continuous | €79/month ("€790/year equivalent") | per product | [22] V |
| ConformOps Portfolio | €249/month | 5 active products | [22] V |
| CVD Portal Free | €0 | intake portal, 1 member | [24] V |
| CVD Portal Reporting | €99/month, billed annually €1,188 | up to 3 members; Art. 14 workflow, SBOM registry, NVD+EUVD | [24] V |
| CVD Portal Compliance | €299/month, billed annually €3,588 | 5 members; 3 products then €99/month each | [24] V |
| Article 14 Ready "24h Dry Run" | €79 excl. VAT, one-off | 45-minute tabletop exercise | [23] V |
| sbomify Business | $159/month billed annually | 5 products, 200 components | [27] V |
| Regulus Basic / Pro | €2,500 / €15,000 per year | early access | [28] V |
| Zealience Z-CMS | €4,000/yr per licence (1–4), down to €1,000 (76–100) | per product/product family | [29] V |
| Vulert Pro / Growth | $15 / $25 per month per app ($13 / $22 annual) | 1 app, unlimited users | [30] V |
| Aikido Developer / Basic / Pro | $0 / $300 / $600 per month | 2 / 10 / 10 users | [31] V |
| CRA Evidence, Kunnus, SBOM Observer, ReARM Pro, ONEKEY, Cybeats, Interlynk, labs | not published | — | [21][25][26][32][33][36] |
| Conformity-assessment engagements | "EUR 10,000 to 30,000 per product family" (vendor claim, snippet) | — | [28] V (snippet) |

Note: a Vulert blog snippet quoted $20/$45/$125 plans; the pricing page read on 2026-09-26 shows $15/$25 per app. The pricing page is used.

### 2.4 Market / demand evidence

| # | Signal | Excerpt / figure | Quality |
|---|---|---|---|
| D1 | Legal trigger live | Art. 14(1): manufacturers "shall notify any actively exploited vulnerability … via the single reporting platform"; SRP launched 11 Sep 2026: "From today, 11 September 2026, manufacturers are required to report actively exploited vulnerabilities" [1][5] | Primary, strong (obligation); not evidence of willingness to pay |
| D2 | SMEs ask for tools | ENISA SME survey: "Technical tools that help assess compliance" 132/194 (68.04%); vulnerability-handling templates 56%; financial support 142 (73.20%), the highest single item [8] | Primary, moderate (stated preferences; the financial-support signal cuts against paid tools) |
| D3 | Regulator prefers free, simple support | ENISA's recommendation: guidance "needs to be easy to use, without requiring companies to rely on additional tools, external support or consultants, and it should be freely accessible" [8] | Primary, strong as a *risk* signal (public free provision) |
| D4 | Low readiness | 36% of micro-companies have no incident-response plan; SRP guidance needed [8]. LF 2026: 66% unfamiliar with the CRA; 41% of manufacturers expect full compliance by Dec 2027 [10] | Primary (ENISA) / secondary (LF), strong for pain, weak for purchase |
| D5 | Tool investment | ENISA SBOM 2026: 43% say the CRA "significantly accelerated" SBOM-tooling investment; 34% invested in tools dedicated to vulnerability handling via SBOM [9] | Primary, moderate; sample >65% large firms |
| D6 | Developer community | Ask HN "Is anyone else preparing for the EU Cyber Resilience Act?" (posted by a one-person German firmware GmbH, ~2 Sep 2026): 7 points, 6 comments, mostly vendor replies [41]. GitHub: 114 repositories mention "cyber resilience act"; top non-AI community projects have 18–56 stars [42] | Primary, **weak** |
| D7 | Supply-side entry | ≥15 vendors with CRA-specific offers (§2.1), several founded or launched in 2026 [21][24] | Secondary, moderate for *expected* demand; not proof of paid demand |
| D8 | Events | Black Duck webinar "Are you ready: CRA reporting" (snippet) [37]; Toradex "Torizon CRA Event in Munich" (HN comment) [41]; webinars are the most preferred SME information channel (57%) [8] | Mixed, weak–moderate |
| D9 | Enforcement actions | None found (reporting began 11 Sep 2026) | UNKNOWN |
| D10 | Job postings for CRA/product-security roles | Search found none | UNKNOWN (not searched on job boards directly) |

### 2.5 Customer complaints and feature gaps in existing solutions
- **False positives and per-project suppression** in Dependency-Track: "Currently, Dependency-Track allows marking vulnerabilities as FALSE_POSITIVE only at the project level and for a specific component version" (issue #5992, 2 Apr 2026, open) [40]; related CPE-matching false-positive issues #3178, #3268, #3063 (snippet) [40]. VERIFIED (read #5992).
- **SBOM completeness is hard**: 62% rate it "quite a lot or extremely difficult"; 30% cite poor vendor-supplied SBOMs [9]. VERIFIED.
- **Ecosystems without SBOM tooling** (C/C++, embedded, Delphi): community builds its own generators (e.g., DX.Comply for Delphi) [42]; Agent 1 [A1 38] documented C/C++ limitations. SUPPORTED INFERENCE.
- **The SRP cannot be automated at launch**: "no Application Programming Interface (API) will be provided at the initial release of the SRP, so notifications must be submitted through the platform interface"; "At launch, the platform will be available in English only" [3]. VERIFIED.
- **No independent reviews** exist for the new CRA tools (Kunnus 0 Capterra reviews [26]); buyers cannot compare quality. VERIFIED / SUPPORTED INFERENCE.
- **Market misinformation**: search snippets on 2026-09-26 stated that SMEs "cannot be financially sanctioned for failing to meet Article 14 notification deadlines". The corrigendum only exempts micro and small enterprises from fines for the **24-hour** early-warning deadline [A1 3]. This is a buyer-confusion gap, not a feature gap. VERIFIED (snippet seen; legal scope per Agent 1's OJ read).

### 2.6 Differentiation opportunities (for an AI-free, small-team product)

Where it **could credibly be better** (all HYPOTHESES to test):
1. **Exact SRP-glossary alignment with version tracking.** Glossary v1.3 (25 Sep 2026) distinguishes Required / Optional / "copied from previous step" per stage and per notification type [2]; the glossary moved from v1.1 (5 Sep) to v1.3 in three weeks [2][23]. A deterministic, versioned field schema with stage validation is buildable; most competitors describe Art. 14 support only generically.
2. **Package-URL-first matching and reusable triage decisions** across products and versions (answering the Dependency-Track #5992 complaint) using CC-BY / CC0 feeds (§2.8 Q2).
3. **Art. 14(8) user notification** "in a structured, machine-readable format" [1], e.g., CSAF drafts. CVD Portal already exports CSAF [24], so this is parity, not a moat.
4. **Transparent, EU-hosted, AI-free positioning** against AI-centric offers (UnitOne, cra-agent) [35][42]. Whether buyers value "no AI" is UNKNOWN.

Where it **could not credibly be better**:
- Binary/firmware SBOM generation (ONEKEY-class tools).
- Conformity assessment, testing, notified-body evidence.
- Price floor: €79–€99/month SME anchors and free Dependency-Track/Article 14 Ready already exist.
- Submission: no tool can submit to the SRP (no API) [3].
- Breadth: CVD Portal, Kunnus and CRA Evidence already combine Art. 13 intake, Art. 14 workflows and Annex I documentation [24][25][26].

### 2.7 Switching costs, saturation, acquisition
- **Switching costs (SUPPORTED INFERENCE):** low for greenfield SMEs (reporting began 11 Sep 2026; a third or fewer produce SBOMs). Moderate for Dependency-Track users (self-hosted history, suppressions).
- **Saturation:** the SME-priced Art. 14 niche has at least five offers (§2.1 rows 1–6) within months of the obligation starting; none publishes traction. Saturation of *paying customers* is UNKNOWN.
- **Channel evidence:** SME preferred channels — webinars 57%, EU-level websites 56%, national cybersecurity authority 55%, industry association/cluster 46%; "50 % of respondents are not members of any industry association" [8]. Among CRA-aware respondents, 48% learned of the CRA through developer spaces vs 25% through official EU channels [10]. GitHub Actions/marketplaces are used by small entrants (crawatch.dev) [42]. VERIFIED.
- **Acquisition difficulty (SUPPORTED INFERENCE):** high. Technical buyers, free alternatives, trust requirements for a security-adjacent tool, and dense vendor content already competing for "Article 14" searches.

### 2.8 O1-specific questions

**Q1. Do the target SMEs already produce SBOMs (CycloneDX/SPDX), and with what tools?**
- About one third produce SBOMs: 34.54% of SME respondents [8]; 32% "for all products" in the LF 2026 sample [10]. VERIFIED (whole-sample figures, not role-specific).
- Formats in use: CycloneDX 44%, SPDX 29%, no standard format 11%, proprietary 17% [9]. VERIFIED (large-firm-heavy sample).
- Tooling: "33 % of overall SBOM generation relying on open-source tools"; large and medium firms also use commercial tools; manual processes ~11% overall and 16% in micro-enterprises; 39% generate at build time [9]. VERIFIED.
- Named tools: GitHub dependency-graph export (SPDX 2.3) and SBOM Actions such as the Anchore SBOM Action [13]; Aikido (SBOM + VEX export) [31]; Kunnus and CRA Evidence generate SBOMs [25][26]. **Tool market shares among SMEs are UNKNOWN**; no survey found names them.
- BSI TR-03183-2 (cited by ENISA) expects CycloneDX ≥1.6 or SPDX ≥3.0.1 in JSON/XML [9]. An MVP that parses only older versions may face expectations set by that guideline (SUPPORTED INFERENCE).

**Q2. Vulnerability data sources a commercial product can use, and licence terms**

| Source | Licence / terms found | Commercial use | Label |
|---|---|---|---|
| OSV.dev aggregated sources | Per source: GitHub Advisory DB CC-BY 4.0; PyPI CC-BY 4.0; Go CC-BY 4.0; Rust CC0 1.0; Drupal MIT; Global Security Database CC0; OSS-Fuzz CC-BY 4.0; Rocky BSD; AlmaLinux MIT; Haskell CC0; RConsortium Apache 2.0; OpenSSF Malicious Packages Apache 2.0; PSF CC-BY 4.0; Bitnami Apache 2.0; **Ubuntu CC-BY-SA 4.0**; opam CC0; Erlang EEF CNA CC-BY 4.0. Converted sources: Debian, Alpine, NVD CVEs for OSS [14] | Yes with attribution; CC-BY-SA (Ubuntu) adds share-alike on derived data | VERIFIED [14] |
| GitHub Advisory Database | "licensed under the terms of the CC-BY 4.0 open source license" [15] | Yes with attribution | VERIFIED [15] |
| NVD API | Terms of Use: services "are asked to display the following notice prominently within the application: 'This product uses the NVD API but is not endorsed or certified by the NVD.'"; the NVD name may identify the source but not imply endorsement; modified content may not be attributed to NVD; rate limits; API key above public limits; "as is" [16] | Yes, with notice and rate-limit compliance | VERIFIED [16] (read via ScanCode's copy of the terms; nvd.nist.gov itself is JavaScript-only) |
| CVE List (MITRE / CVE Program) | Terms of use grant "a perpetual, worldwide, non-exclusive, no-charge, royalty-free, irrevocable copyright license to reproduce, prepare derivative works of … and distribute" CVE, provided MITRE's copyright designation and licence are reproduced [20] | Yes with notice | Snippet only [20] — re-read before architecture |
| CISA KEV | "licensed under the CC0 license" [19] | Yes | VERIFIED [19] |
| **ENISA EUVD** | EUVD API documentation: all endpoints `GET`, "require no authentication"; search limited to 100 records per request; daily full EUVD↔CVE mapping CSV and consolidated KEV JSON (CISA KEV + ENISA EU KEV) [17]. **No licence or terms of use** appear in the EUVD docs or web app; the app links to the ENISA Legal Notice, which says "Reproduction of ENISA material published on this website is authorized, provided the source is acknowledged, unless it is stated otherwise" [18]. EUVD also aggregates third-party data (CVE Program, vendor advisories, CISA KEV) [17] | Whether ENISA's legal notice covers euvd.enisa.europa.eu data, and the terms of third-party content inside EUVD, are **UNKNOWN** | Docs VERIFIED [17][18]; terms UNKNOWN (still gates A-03 in Agent 1's v2) |
| EPSS (FIRST) | Used by CRA Evidence [25]; terms not checked | — | UNKNOWN |

**Q3. What must Art. 14 notifications contain, and through which channel?** (so that a tool could prepare content without claiming to submit it)

*Legal minimum (Regulation (EU) 2024/2847, OJ text read) [1]:*

| Stage | Actively exploited vulnerability (Art. 14(2)) | Severe incident (Art. 14(4)) |
|---|---|---|
| Early warning | Within 24h of awareness; indicate, where applicable, Member States where the product has been made available | Within 24h; at least whether suspected of being caused by unlawful or malicious acts; Member States |
| Notification | Within 72h; general information about the product, the general nature of the exploit and the vulnerability, corrective or mitigating measures taken and those users can take; how sensitive the manufacturer considers the information | Within 72h; nature of the incident, initial assessment, measures taken and user measures; sensitivity |
| Final report | No later than 14 days after a corrective or mitigating measure is available: description incl. severity and impact; where available, information on any malicious actor; details of the security update or other corrective measure | Within one month after the incident notification: detailed description incl. severity and impact; type of threat or root cause; applied and ongoing mitigation |
| Other | CSIRT may request an intermediate report (14(6)); inform impacted users "where appropriate in a structured, machine-readable format" (14(8)); Commission **may** specify format and procedures by implementing acts (14(10)) | same |

*Channel [1][3][4][6][7]:* notifications are submitted via the ENISA Single Reporting Platform using the electronic notification end-point of the CSIRT designated as coordinator of the Member State of the manufacturer's main establishment (rules for non-EU manufacturers in Art. 14(7)), simultaneously accessible to ENISA [1]. On the platform: web interface only, no API at initial release; English only at launch [3]; registration via EU Login with multi-factor authentication; one Primary Assigned Representative per manufacturer and up to 20 Secondary ARs [6][7] (two independent secondary sources, both read). ENISA published T&Cs v1.0 (10 Sep 2026), an AR user manual, submission guidance (9 Sep 2026) and a factsheet (v1.0, Jul 2026) [4].

*Platform fields (ENISA CRA SRP Glossary v1.3, "Last update: 25 September 2026") [2]:* 18 common fields, 13 vulnerability-specific fields (v19–v30 incl. v26a) and 9 incident-specific fields (i31–i39).
- **Required at early warning:** notification type; title; summary; manufacturer name (system-generated); Member States where the product is available (concerned CSIRT); product name; product version or range; date/time of awareness (UTC); for incidents, "suspected of unlawful or malicious acts" (Yes/No/Unknown).
- **Required at 72h:** vulnerability "general information" and occurrence date/time; incident general information, occurrence date/time and initial assessment.
- **Required at final report:** corrective or mitigating measures taken; measures users can take; for vulnerabilities, date the measure became available, details of the update, full description of severity and of impact, and malicious-actor information "if such information available"; for incidents, applied and ongoing mitigation, detailed severity and impact, and threat type or root cause.
- **Optional examples:** product type (Default / Important / Critical), class, category, end-of-support indicator, component name, CVE ID, EUVD ID, attack vector, "Particular Exceptional Circumstances" and delay reasons.

SUPPORTED INFERENCE: the platform requires more fields at the early-warning stage than the Regulation's minimum text lists (e.g., title, summary, product version). A tool can deterministically prepare, validate and time-stamp these fields and export them for manual entry. It must state that the SRP is the only submission channel. Because the glossary changed twice in September 2026, the field schema must be versioned.

### 2.9 Major risks and obvious weaknesses (O1)
1. **Commoditisation by free and public tools:** Dependency-Track now tracks EU KEV [39]; the SRP form guides drafting [2]; ENISA favours "freely accessible" support [8]; an ENISA API "may be considered in a future phase" [3]. VERIFIED facts; the commoditisation effect is a PREDICTION.
2. **Contested SME price band:** €79–€99/month overlaps exist (CVD Portal, ConformOps) [22][24]. VERIFIED.
3. **Episodic trigger (HYPOTHESIS):** Art. 14 fires only on *actively exploited* vulnerabilities or *severe* incidents. For many small software products this may be rare, which weakens monthly retention for a "clock" product unless continuous monitoring and evidence carry the value. The frequency per SME is UNKNOWN.
4. **Low willingness to pay:** financial support is the most requested item (73.2%) [8].
5. **Schema churn and regulatory change:** glossary v1.1→v1.3 in three weeks [2][23]; possible implementing act on format (Art. 14(10)) [1].
6. **Liability** for missed or mismatched vulnerabilities; must not imply compliance (Agent 1 OOS-01).
7. **Data-licence gating:** EUVD terms UNKNOWN; NVD notice; CC-BY attribution; Ubuntu CC-BY-SA share-alike [14][16][17][18].
8. **Segment size UNKNOWN** (S2 in §2.0); micro/small 24-hour fine relief lowers urgency [A1 3].
9. **Positioning pressure from AI-centric offers** ("autonomous agentic AI for CRA", 452 stars) [42]; AI-free status is a constraint, not proof of a buyer benefit.

### 2.10 Validation questions still open (O1) and the evidence that would answer them
(No customer interviews were possible in this session.)

| # | Question | Evidence that would answer it |
|---|---|---|
| V1-1 | What share of target SMEs are S1 (already producing) vs S2 (can export) vs firmware-only? | Short screener survey via developer communities; ENISA/LF microdata if obtainable; landing-page segmentation question |
| V1-2 | How often do SME products face an *actively exploited* vulnerability or severe incident? | Interviews with 10–15 S1 SMEs; KEV hit-rate analysis on public SBOMs of SME products (deterministic desk study) |
| V1-3 | Will S1 SMEs pay above €79–€99/month for SRP-aligned drafts + evidence, versus Dependency-Track + Article 14 Ready? | Van Westendorp or Gabor-Granger pricing test; fake-door "start trial" test at €49/€99/€149 |
| V1-4 | Which job is most valued: continuous monitoring, triage evidence, Art. 14 drafts, Art. 14(8) user notifications, support-period management? | Card-sorting in interviews; feature-interest clicks on the landing page |
| V1-5 | Traction of CVD Portal, ConformOps, Kunnus, CRA Evidence | Direct enquiries, LinkedIn follower growth, public customer lists (none found) |
| V1-6 | Are EUVD data reusable commercially? | Written confirmation from ENISA (euvd contact / legal) |
| V1-7 | Trust prerequisites (EU hosting, security page, references) | Interviews; A/B test of the security page |
| V1-8 | Do SECURE-type grants pay for SaaS subscriptions? | Read SECURE Annex 2 eligible costs; ask the helpdesk |

### 2.11 Assumptions requiring testing (O1)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O1-01 | S1 SMEs (already producing SBOMs) are about a third of CRA-relevant software SMEs | SUPPORTED INFERENCE from [8][10]; role-specific share UNKNOWN | V1-1 |
| MV-O1-02 | S2 SMEs will add an SBOM-generation step to use the product | HYPOTHESIS | Onboarding test |
| MV-O1-03 | SMEs will pay a recurring fee for Art. 14 readiness plus monitoring above existing €79–€99 anchors | HYPOTHESIS (evidence against: [8] financial-support signal) | V1-3 |
| MV-O1-04 | Actively exploited vulnerabilities affect SME products often enough to sustain monthly value | HYPOTHESIS | V1-2 |
| MV-O1-05 | No dominant SME-focused CRA vendor exists | UNKNOWN (no traction published by anyone) | V1-5 |
| MV-O1-06 | EUVD data may be used in a commercial product | UNKNOWN | V1-6 |
| MV-O1-07 | Buyers value an AI-free, deterministic tool | ASSUMPTION | Interviews / positioning test |
| MV-O1-08 | ENISA will not ship a free submission API or drafting tool within 12 months that removes the drafting value | PREDICTION (uncertain; [3] says API "may be considered") | Monitor ENISA SRP releases |

---

## 3. O2 — Great Britain holiday-record and holiday-pay assurance for variable-hours employers

### 3.0 Context re-checked in this session
- DBT consultation (read locally) [45]: "Since April 2026, employers have been required to keep holiday pay records for six years (regulation 16B of the Working Time Regulations 1998) that are adequate to show whether they have complied … It is up to the employer how they keep those records." Proposed FWA penalty: 200% of arrears, maximum £20,000 per worker, minimum £100. Consultation closed 22 Sep 2026. FWA powers extend to England & Wales and Scotland; "Employment law is devolved in Northern Ireland". VERIFIED [45].
- **J1-015 confirmed:** "Holiday pay claims will not be enforceable by the FWA if they occurred before Royal Assent … Royal Assent was 18 December 2025 so claims from before this date cannot be enforced by the FWA" [45]. Near-term exposure is therefore periods from 18 Dec 2025 onward, not six years back. VERIFIED.
- **Self-audit incentive:** "A penalty would not ordinarily be issued where an employer has correctly repaid all holiday pay arrears that are owing to the workers before the start of an FWA investigation" [45]. VERIFIED (proposal).
- FWA delivery plan 2026–27 (GOV.UK, published 21 Aug 2026): "holiday pay enforcement is expected to begin in 2027"; "Ready to communicate new enforcement approach, guidance and tools to support holiday pay compliance" [46]. VERIFIED.

### 3.1 Competitor matrix (direct) and payroll-product coverage

**Direct calculation / assurance offers**

| Name / URL | Target | Capabilities relevant | Published pricing | Region | Published traction | Grade |
|---|---|---|---|---|---|---|
| **paiyroll** holiday-pay companion — paiyroll.com (© 2026 Innovatie Limited) | Employers and payroll bureaus keeping their existing payroll | 52-week averaging for variable pay (overtime, commission); 12.07% rolled-up holiday pay; zero/variable/fixed hours; integrations with 19+ payroll systems incl. BrightPay, Sage 50, Xero, QuickBooks, Staffology, IRIS Star, KeyPay/Employment Hero, FPS XML | **15p per payslip**, "Minimum £30 pcm", optional £90 setup; monthly, no annual contract [49] | UK (implied) | None published | V (read) [49] |
| **Staffology Payroll** (IRIS) | Employers and bureaus | "Average Holiday Pay" schemes calculate a rate automatically; lookback "Defaults to 52 weeks"; configurable pay codes; one statutory-pay exclusion option at a time (page updated 24 Jun 2026) | Not captured (pricing URL redirects to IRIS) | UK | Not published | P (product docs, read) [53] |
| **KeyPay / Employment Hero UK** | SMEs | "will automatically calculate the average amount of holiday pay based on the historic data held"; 52 weeks; falls back to the current hourly rate if data are insufficient | Not on page | UK | Not published | P (product docs, read) [56] |
| **IRIS Earnie Holiday Pay Module** | IRIS Earnie users | Configurable holiday-pay calculation incl. 52-week averaging considerations (updated 16 Feb 2026) | Licensing/price not stated | UK | — | P (read) [57] |
| **Healthbox HR** | SMEs | HR + payroll platform; named by a Xero user as the product they switched to "to comply" | Custom pricing (snippet) | UK | — | V (snippet) [63]; [51] |
| **StaffLeave**, **Employment Hero** (HR), **BrightHR**, **Breathe**, **Timetastic**, **RotaCloud**, **Planday**, **Fourth**, **Shiftbase**, **LeaveWizard** | SMEs, shift-based sectors | Leave tracking and 12.07% hours accrual; StaffLeave claims "Securely store data for six years … with easy audit trails for FWA audits" | Various, mostly per-user | UK | — | V (read [58][59]; snippets [62]) |
| **Advisory services**: accountancy/payroll consultancies (e.g., Azets offers reviews of current systems and FWA preparation), employment lawyers | Employers | Reviews, remediation | Not published | UK | — | S/V (snippet) [65] |

**Coverage of 52-week averaging and irregular-hours accrual in common UK payroll products (answer to the O2 question)**

| Product | 12.07% irregular-hours accrual | 52-week average holiday-pay *rate* | Evidence and date | Label |
|---|---|---|---|---|
| **Sage 50 Payroll** | Calculated-entitlement schemes; one user reports they are based on 12 weeks (snippet) | 52-week average *report*; "You must only use this when there are no weeks to exclude"; otherwise "manually calculate" (KB last modified 4 Sep 2024); community reply describes manual division (>1 year old) | [54] | VERIFIED as of the KB date; 2026 status UNKNOWN |
| **Sage Payroll (cloud)** | UNKNOWN | No evidence of automatic calculation; a >2-year-old thread discusses which payments are included | [54] | UNKNOWN |
| **Xero Payroll UK** | Not checked | Not automated. Idea "Run a report to calculate holiday pay based on a 52 week average" (created 1 Jun 2022, 93 votes). Xero admin, 27 Nov 2025: "for the time being this is not a feature we have planned in our roadmap"; workaround: run Payroll Activity Summary or Gross-to-Net over 52 weeks | [51] | VERIFIED |
| **QuickBooks Payroll UK** | UNKNOWN | Conflicting: staff said "this feature is not yet available" (Feb 2022), then that the 52-week average is available for weekly, 2-weekly, 4-weekly and monthly schedules (Nov 2022); a snippet says standard payroll has no holiday-pay tracking | [55] | UNKNOWN (conflicting) |
| **BrightPay** | Yes: accrual method "applying 12.07% to hours worked (excluding hours marked as overtime hours)" (2025-26 docs) | Conflicting: a BrightPay doc snippet says "BrightPay will not calculate holiday pay amounts … the calculation for number of hours x hourly rate will have to be calculated manually outside of BrightPay", and that 52-week reports must be combined across two tax years in Excel; a Xero user (18 Nov 2025) says "Other software like BrightPay offer this feature" | [52][51] | Accrual VERIFIED; rate UNKNOWN (conflicting) |
| **Staffology (IRIS)** | Not checked | Automatic average-holiday-pay schemes (docs updated 24 Jun 2026) | [53] | VERIFIED (vendor docs) |
| **IRIS Earnie** | Not checked | Holiday Pay Module; degree of automation UNKNOWN | [57] | Partly VERIFIED |
| **Moneysoft Payroll Manager** | Yes: "will automatically calculate 12.07% of their 'Hours worked'"; rolled-up holiday pay automatic | No: "Payroll Manager is not able to calculate the holiday pay rate automatically, instead the rate must be calculated by the user" (Pay Count report provided as aid) | [50] | VERIFIED |
| **KeyPay / Employment Hero** | Not checked | Yes, automatic over 52 weeks (no 104-week extension stated) | [56] | VERIFIED (vendor docs) |

SUPPORTED INFERENCE: the rate calculation is **automated in some products (Staffology, KeyPay/Employment Hero)** and **manual or conditional in several widely used SME products (Xero, Moneysoft, Sage 50 when weeks must be excluded)**, with BrightPay and QuickBooks unresolved. This is documented under-service for the calculation job in part of the market. It is not evidence about how many employers use the affected products for variable-hours staff (UNKNOWN).

**Who is the buyer — employer or bureau?**
- The legal duty and the criminal offence sit with the **employer** [45]. VERIFIED.
- paiyroll sells to both employers and bureaus, priced per payslip [49]. VERIFIED (V).
- Xero Ideas commenters write as employers or in-house payroll administrators ("I am switching payroll to Healthbox HR to comply") [51]. SUPPORTED INFERENCE.
- Share of SMEs using bureaus or accountants for payroll: only low-quality aggregator snippets ("61% of UK businesses outsourced payroll in 2024"; "38% of accounting firms offer outsourced payroll"), no primary source [66]. **UNKNOWN.** No count of UK payroll bureaus was found. **UNKNOWN.**
- Conclusion: **HYPOTHESIS** — two buyer routes. Employers carry liability and pain; bureaus and accountants control tool choice for outsourced payrolls and run several payroll products at once. Evidence for either route is weak.

### 3.2 Alternatives and substitutes

| Substitute | Cost | Where it breaks | Label |
|---|---|---|---|
| **Spreadsheet or paper records** — ATT (16 Jun 2026): records "can be kept in any format the employer thinks reasonable. This could be dedicated software, a spreadsheet or a paper-based system" [60] | Staff time | Excluded weeks, the 104-week lookback and normal-remuneration components are error-prone; six-year retention; data spans two tax years (BrightPay snippet) [52] | VERIFIED [60]; failure modes SUPPORTED INFERENCE |
| **Payroll reports + Excel** (Xero, Sage 50, BrightPay workarounds) [51][52][54] | Included in payroll | Manual rate entry each period; no audit trail of the method | VERIFIED |
| **GOV.UK holiday-entitlement calculator** | Free | Entitlement and accrual only, **not pay** [47] | VERIFIED |
| **Announced or considered government tools**: DBT is "considering … a more detailed calculator or self-assessment tool to help employers and workers work out holiday entitlement and holiday pay", worked examples, a chatbot, webinars [45]; FWA plans "guidance and tools to support holiday pay compliance" [46] | Free | Not yet available; scope UNKNOWN | VERIFIED (intention); delivery PREDICTION |
| **Acas** free advice [45]; worker-side calculators (payslipchecker.uk, timetally.uk, uktax.tools, youtemp) [64] | Free | Guidance or single calculations; no records | VERIFIED [45]; snippets [64] |
| **Leave/rota tools** with 12.07% accrual [58][62] | Per user | Accrue hours; do not compute the pay rate | SUPPORTED INFERENCE |
| **Accountants, payroll bureaus, HR consultancies, lawyers** [65] | Fees not published | Episodic reviews; cost | UNKNOWN (fees) |
| **Switching payroll** to a product that automates averaging (Staffology, KeyPay/Employment Hero, Healthbox) [51][53][56] | Migration cost | Disruptive; historic data import needed (Staffology offers "import historic average earnings") | SUPPORTED INFERENCE |

### 3.3 Pricing evidence (date seen 2026-09-26)

| Offer | Price | Source |
|---|---|---|
| paiyroll holiday-pay add-on | 15p per payslip; minimum £30/month; optional £90 one-off setup | [49] V |
| ESTIMATE: employer with 50 weekly-paid variable-hours workers | ≈ 217 payslips/month × £0.15 ≈ £32.50/month, i.e., close to the £30 minimum | arithmetic on [49] |
| Staffology, KeyPay/Employment Hero, BrightPay, Sage, Xero, Moneysoft, IRIS payroll licences | Not captured in this session | UNKNOWN |
| Outsourced payroll | "£4–£25 per employee" per month quoted by aggregator pages (snippet, low quality) | [66] |
| Healthbox HR, StaffLeave PlusPack, Azets reviews | Not published / custom | [58][63][65] |

### 3.4 Market / demand evidence

| # | Signal | Excerpt / figure | Quality |
|---|---|---|---|
| D1 | Records duty in force; criminal offence | reg. 16B, since April 2026 [45]; also CIPP (30 Mar 2026) [61], ATT (16 Jun 2026) [60] | Primary, strong (obligation) |
| D2 | Government acknowledges calculation difficulty | "We know calculating holiday pay entitlement can be complex and can lead to accidental non-compliance and underpayment" [45] | Primary, strong (qualitative) |
| D3 | Enforcement coming | FWA holiday-pay enforcement "expected to begin in 2027" [46]; proposed 200% penalty, £20,000 cap per worker [45] | Primary, strong on timing (proposal status) |
| D4 | Non-compliance proxies | Resolution Foundation: 2.2m jobs with no annual leave in 2025; TUC: ~1.1m workers without holiday pay in 2023 (~£2bn); DBT notes these "do not provide a direct, robust measure" [45] | Primary citing secondary; measures leave denial, not calculation error |
| D5 | Dispute volume | ~8,000 ET claims on "Working Time (annual leave)" and 13,000 "Wages Act" claims in 2024/25 (Acas data) [45] | Primary, moderate |
| D6 | User demand in incumbent forums | Xero idea: 93 votes since 2022, comments through May 2026 ("This is a legal requirement, not a nice-to-have wish") [51] | Primary (user forum), **strong** for the Xero user base |
| D7 | Vendor documentation admits gaps | Moneysoft (manual rate) [50]; Sage 50 (manual when weeks excluded) [54] | Primary product docs, strong |
| D8 | Content volume after April 2026 | Law firms, ATT, CIPP, HR vendors publishing on six-year records and FWA readiness [58]–[61][65] | Secondary, moderate (supply-side) |
| D9 | Self-audit incentive | No penalty "ordinarily" if arrears repaid before an FWA investigation (proposal) [45] | Primary, moderate (proposal) |
| D10 | Prevalence of miscalculation among SMEs | No survey found; CIPP 2024 ">30%" still snippet-only [A1 45] | UNKNOWN |
| D11 | Forums (Reddit, AccountingWEB) | Not reachable (AccountingWEB 403; Reddit not surfaced) | UNKNOWN |

### 3.5 Customer complaints and feature gaps
- **Xero:** "Something that has been a legal requirement since 2020 should have the highest priority" (18 Mar 2025); "I'm starting to look elsewhere for better software" (30 Apr 2025); "I am switching payroll to Healthbox HR to comply" (2 May 2026) [51]. VERIFIED.
- **Sage 50:** users report calculated entitlement based on 12 prior weeks gives wrong results for irregular hours; workaround merges two reports (snippet) [54]. The report does not add further weeks when unpaid or SSP-only weeks occur [54]. VERIFIED (KB) / snippet (user).
- **Moneysoft:** no automatic rate; no automatic accrual during statutory leave [50]. VERIFIED.
- **KeyPay/Employment Hero:** lookback fixed at 52 weeks; falls back to the current hourly rate when history is short [56]. Whether this matches the 104-week guidance cited by Sage [54] is a compliance question (UNKNOWN).
- **Staffology:** "Only one statutory pay exclusion option can be active simultaneously" [53]. VERIFIED.
- **BrightPay:** 52-week reports cover one tax year at a time and must be combined manually (snippet) [52].

### 3.6 Differentiation opportunities
Could credibly be better (HYPOTHESES):
1. **Payroll-agnostic calculation + evidence layer** for bureaus and employers running Xero, Sage 50, BrightPay or Moneysoft: import payroll exports, compute the rate with excluded weeks and a lookback of up to 104 weeks, and document the components used — the record the ATT and CIPP say employers must keep [60][61].
2. **Six-year, immutable per-worker ledger** and an "FWA-ready" evidence pack (method, reference weeks, inputs, outputs) — the one thing not described by paiyroll's page [49].
3. **Arrears self-check** aligned with the proposed "repay before investigation" incentive [45], limited to periods after 18 Dec 2025.
4. **Multi-client bureau view** across several payroll products (bureaus often run more than one). HYPOTHESIS (no bureau evidence found).

Could not credibly be better:
- In-run automation inside payroll (Staffology, KeyPay already do it) [53][56]; write-back into payroll fails Agent 1's MVP filter.
- Price: paiyroll sets a low anchor (≈£30/month for small employers) [49].
- A free government calculator, if DBT builds one [45].
- Legal interpretation (normal remuneration, EU vs domestic leave) cannot be productised without legal review (Agent 1 OOS-04).

### 3.7 Switching costs, saturation, acquisition
- **Switching (SUPPORTED INFERENCE):** an add-on avoids replacing payroll (low switching cost), but needs a per-period export/import routine (recurring friction). The alternative, changing payroll provider, is high-cost; one Xero user has done it [51].
- **Saturation:** leave tracking is saturated; the dedicated calculation add-on niche has at least one competitor (paiyroll) and incumbents are closing the gap (Staffology's scheme docs, 2026) [49][53]. paiyroll's customer uptake is UNKNOWN (J1-014).
- **Channels:** payroll bureaus and accountants (ICPA, CIPP, AccountingWEB communities) and payroll-software app marketplaces are *plausible*; no primary evidence of their effectiveness or size was found (UNKNOWN). The FWA's 2027 guidance launch and webinars [45][46] are a PREDICTION of a demand moment.
- **Acquisition difficulty (SUPPORTED INFERENCE):** moderate. Pain is concentrated in identifiable user bases (Xero, Sage 50, Moneysoft), but GB-only and price-anchored low.

### 3.8 Major risks and obvious weaknesses (O2)
1. **Free public tool:** DBT is explicitly considering "a more detailed calculator or self-assessment tool" for holiday pay [45]. VERIFIED (intention).
2. **Incumbents closing the gap** (Staffology, KeyPay; Xero could change its roadmap) [51][53][56].
3. **Regime still a proposal**; penalties, claim period and 2027 start await the government response [45][46].
4. **Smaller near-term exposure** than "six years": FWA cannot enforce pre-18 Dec 2025 underpayments [45].
5. **Calculation liability** for the vendor (normal remuneration, 52/104-week rules, EU vs domestic leave).
6. **GB-only market**; Northern Ireland equivalence UNKNOWN (A-18 unchanged).
7. **Low WTP anchor** (15p/payslip, £30 minimum) [49].
8. **Data protection**: pay and possibly health-related absence data (Agent 1 OOS-02).

### 3.9 Validation questions still open (O2)
(No interviews possible in this session.)

| # | Question | Evidence that would answer it |
|---|---|---|
| V2-1 | Employer or bureau: who buys, and how many bureaus serve variable-hours SMEs? | 10 bureau + 10 employer interviews; ICPA/CIPP membership data; bureau directory count |
| V2-2 | How many employers with variable-hours staff use Xero, Sage 50, BrightPay or Moneysoft (the gap products)? | Payroll-software market-share data; screener survey |
| V2-3 | Does BrightPay (2026-27) calculate the 52-week rate? Does QuickBooks standard payroll? | Trial accounts; vendor support confirmation |
| V2-4 | Value of the evidence pack vs calculation alone; WTP vs paiyroll's 15p/payslip | Pricing test with bureaus (per payslip vs per client per month) |
| V2-5 | paiyroll's uptake | Direct enquiry; integration marketplace reviews |
| V2-6 | Will DBT/FWA ship a free holiday-*pay* calculator, and when? | Government response to the consultation (closed 22 Sep 2026) |
| V2-7 | Prevalence of miscalculation | Obtain the CIPP 2024 survey; bureau audit data |

### 3.10 Assumptions requiring testing (O2)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O2-01 | A material share of GB variable-hours employers use payroll products that do not automate the 52-week rate | HYPOTHESIS (gaps VERIFIED per product [50][51][54]; user counts UNKNOWN) | V2-2 |
| MV-O2-02 | Bureaus are the efficient channel | HYPOTHESIS | V2-1 |
| MV-O2-03 | Employers value a six-year evidence pack beyond calculation | HYPOTHESIS | V2-4 |
| MV-O2-04 | The government will not release a free holiday-pay calculator that covers the MVP's core within 12 months | PREDICTION (uncertain; DBT considering one [45]) | V2-6 |
| MV-O2-05 | FWA enforcement starts in 2027 as planned | VERIFIED as stated intention [46]; commencement PREDICTION | Monitor |
| MV-O2-06 | Payroll exports contain enough data (hours, pay elements, dates) to compute rates deterministically | ASSUMPTION | Collect sample exports from 3–5 products |

---

## 4. O4 — EU Pay Transparency compliance for SME / lower-mid-market employers (conditional)

### 4.0 Status of Italy and other states (answers to the O4 questions)

**Italy — Legislative Decree No. 96 of 7 May 2026** (Gazzetta Ufficiale n. 125, 1 Jun 2026; in force 7 Jun 2026). VERIFIED [69][70][71] (three secondary sources read; Italian snippets agree [72]).
- Articles 5–7 (pre-employment pay information, salary-history ban, pay criteria, information requests) apply from 7 Jun 2026; the pay-progression criteria obligation does not apply below 50 employees [69][70]. VERIFIED.
- Reporting: **250+ employees** annually, first by **7 Jun 2027**; **150–249** every three years, first by **7 Jun 2027**; **100–149** every three years, first by **7 Jun 2031**; no reporting below 100 [69][70][71]. VERIFIED.
- Indicators: mean and median gender pay gap, variable-pay gaps, share receiving variable pay, quartile distribution, gaps by category of workers doing the same work or work of equal value; confirmation after consulting worker representatives [71]. VERIFIED (S).
- Recipient: "un organismo istituito presso il Ministero del Lavoro" (a monitoring body at the Ministry of Labour) [70][71]; composition (ISTAT, INPS, INAPP, CNEL, unions) within 180 days (snippet) [72]. VERIFIED / snippet.
- **Reporting format: not yet defined, as far as found.** Technical data specifications are to be set by ministerial decree within 90 days of entry into force, after an opinion of the data-protection authority [70]. On 23 Sep 2026 Ius Laboris reported that the Minister "is expected to adopt ministerial decrees in September setting out further details regarding the reporting obligations under Article 9(4)" [68]. I found no evidence of adoption by 26 Sep 2026. **UNKNOWN** whether adopted; the format is therefore **not yet defined** in any source found.
- Job classification: national collective bargaining agreements (NCBAs) are the primary framework for "same work" and "work of equal value"; internal systems may "only integrate — and not replace" them [69]. VERIFIED (S).
- Existing substitute channel: Italy's **"Rapporto biennale"** on male and female staff (art. 46 D.Lgs. 198/2006) is already mandatory for employers with more than 50 employees, filed online on the Ministry's portal; the 2024–25 edition was due 15 May 2026 after an extension (several snippets agree) [73]. Its relationship to the new reports is UNKNOWN.
- Segment size: ISTAT counted 22,861 enterprises with 50–249 persons employed (snippet, Nov 2023 census report) [74]. The 100–249 subset is UNKNOWN. SUPPORTED INFERENCE: only the 150–249 band faces a first report in 2027; the 100–149 band not until 2031, so the near-term Italian SME reporting segment is a fraction of an already small number.

**Other member states (status, and which will transpose by early 2027)**

| State | Status (source date) | Early-2027 outlook | Label |
|---|---|---|---|
| Malta, Lithuania, Slovakia | Fully transposed by 7 Jun 2026 (Lewis Silkin, 25 Jun 2026) [75] | In force | VERIFIED (S, read; also Agent 1's Morgan Lewis source) |
| **Greece** | **Law 5316/2026**, Government Gazette 6 Jul 2026; most obligations from **1 Nov 2026**; reporting 250+ and 150–249 first by 7 Jun 2027, 100–149 by 7 Jun 2031; Ombudsman as monitoring body with a digital platform; fines €300–€50,000 per violation; SME technical assistance [76] | In force from 1 Nov 2026 | VERIFIED (Lewis Silkin read + Jackson Lewis and Zepos snippets) |
| Poland; Belgium; Estonia | Partial (PL recruitment rules; BE public sector only; EE recruitment and pay secrecy) [75][77] | Further PL legislation in parliament [77] | VERIFIED (S) |
| Netherlands | Draft; plenary debate second week of January 2027; the 1 Jan 2027 target "now appears uncertain" [68] | PREDICTION: early-to-mid 2027 | VERIFIED status |
| Germany | "(unconfirmed) rumours" of cabinet approval in October 2026 [68]; another consultancy lists January 2027 [77] | PREDICTION: law in 2027; date conflicting | Conflicting |
| Romania | Draft; "likely enacted before year-end 2026" (single consultancy source) [77] | PREDICTION | Single source |
| Hungary | Law "planned for adoption in October 2026" [68] | PREDICTION | VERIFIED as plan |
| Cyprus | Draft to Council of Ministers Sep 2026; first reports for 150+ by 7 Jun 2027 [68] | PREDICTION | VERIFIED as plan |
| Czechia | Draft sent to the Chamber after 4 Sep 2026 [68]; phased 2027–2031 [77] | PREDICTION | VERIFIED status |
| France | Draft amended 10 Sep 2026; aim for a final vote before the April/May 2027 elections [68] | PREDICTION | VERIFIED status |
| Spain | Draft Royal Decree published 3 Aug 2026 [68] | Timing UNKNOWN | VERIFIED status |
| Portugal; Bulgaria | Partial draft (5 Aug 2026); bill to parliament (11 Sep 2026) [68] | UNKNOWN | VERIFIED status |
| Ireland | Pay Transparency Bill not given priority drafting status (16 Sep 2026 programme) [68] | Unlikely by early 2027 (PREDICTION) | VERIFIED status |
| Sweden | Government (26 Mar 2026) will not submit a bill and seeks EU-level postponement and renegotiation [78] | Not before renegotiation (PREDICTION) | VERIFIED (S) |

Note for the Orchestrator: Agent 1's approved v2 describes Ius Laboris as treating "only Italy" as transposed. The Ius Laboris page text I read lists only *changes over the last month* (the country map is not machine-readable), while Lewis Silkin and others record Malta, Lithuania, Slovakia and, from 6 Jul 2026, Greece as transposed. See OOS-MV-01.

### 4.1 Competitor matrix (direct)

| Name / URL | Target | Capabilities relevant | Published pricing | Hosting / region | Traction | Grade |
|---|---|---|---|---|---|---|
| **Axios Analytics** — axiosanalytics.com | Mid-market; all EU member states | CSV/Excel import with data-quality scoring; EG-Check job evaluation; "Seven mandatory Article 9 metrics and 5% Article 10 trigger analysis"; remediation simulator; sign-offs | <100 employees: one-off report **€4,000**; **100–149: €3,000/yr; 150–249: €4,500/yr**; 250–499 €7,000/yr; 500–999 €10,000; 1,000–1,999 €16,000; onboarding €1,500 one-off; 12-month auto-renew [80] | "EU hosting in Frankfurt" [80] | None published | V (read) [80] |
| **Evenpay** — evenpay.io | Mid-size and enterprise | Job evaluation, pay-gap reporting, salary bands, joint pay assessments, justification archive | **Evenpay Core €4,900/yr** (band-dependent; bands include 100–249); SSO +€189/mo [81] | Not stated | None | V (read) [81] |
| **Zucchetti HR PayGap** — zucchetti.it | Italian HR/payroll customers (resold via partners such as Veridian, errepi for associations and professionals) | Equal-value clusters; automatic gender-pay-gap calculation; 5% flags; reports; answers to employee requests; simulations; integrates with HR/payroll | Not published [84] | Italy | Not published | V (read) [84]; resellers snippet [85] |
| **TeamSystem**, **Inaz** (Italy) | Italian employers | Published D.Lgs. 96/2026 guidance; product scope not verified | Not published | Italy | — | V (snippet) [85] |
| **Figures** — figures.hr | Mid-market / enterprise | Benchmarking, salary bands, pay-gap analysis, "Compliance report aligned with the EU Directive", employee information letters | Quote-based by headcount [82]; "starts at EUR 2,500/yr" (snippet) vs "starting from €4,000" (page metadata per [83]) — conflicting | EU | — | V (read, no price) [82] |
| **Ravio** | Tech sector | Benchmarking + equity | £5,000/yr for a 500-person company [83] | — | — | V [83] |
| **PayAnalytics (beqom)**, **Sysarb**, **Trusaic**, **Syndio**, **Personio** (pay-gap reporting features), **HiBob**, **Lattice** ($13/seat/month + $6 compensation add-on, $4,000 minimum) | Mid-market to enterprise | Pay-equity analytics; Personio publishes directive guidance and features | Mostly quote-based; PayAnalytics priced per employee analysed, 1-year minimum; Sysarb onboarding fee + annual [83] | Various | — | V [83] |
| **TracefyHR**, **employsome** | SMEs (content) | Directive guides; product/pricing not verified | UNKNOWN | — | — | V (snippet) |

SUPPORTED INFERENCE: for the 100–249 band an **EU-wide, EU-hosted tool already publishes €3,000–€4,500/year** [80], and the dominant Italian payroll vendor (Zucchetti) sells a dedicated pay-gap module [84]. The "most tools are built for enterprise" claim (Agent 1 [A1 19], from Axios's own buyer guide) is weaker now that Axios itself publishes SME-band pricing.

### 4.2 Alternatives and substitutes
- **Commission/EIGE gender-neutral job-evaluation toolkit** (April 2026): step-by-step guidance; "Tool 4" for organisations of 10–49 and up to 250 employees with fewer than 15 distinct roles, using pair comparison; voluntary and free [79]. VERIFIED (S).
- **Payroll/HRIS reports + Excel** (Italian consulenti del lavoro and in-house payroll) — cost is staff time; breaks on equal-value categorisation and worker-representative sign-off. SUPPORTED INFERENCE.
- **Italy's existing biennial staff report** process and portal [73] — a familiar compliance routine that may absorb part of the new reporting (relationship UNKNOWN).
- **Law firms and consultancies** (Ius Laboris "Pay GAP IQ", Deloitte, Aon, Mercer) — quote-only [68].
- **Free OSS/prototypes on GitHub**: 12 repositories, all 0 stars, several AI-based (e.g., "RAG-powered assistant"), plus a free "quick scan" (FairWave, 17 Sep 2026) [87]. Weak.

### 4.3 Pricing evidence (date seen 2026-09-26)

| Offer | Price | Source |
|---|---|---|
| Axios Analytics 100–149 / 150–249 | €3,000 / €4,500 per year + €1,500 onboarding | [80] V |
| Axios Analytics <100 | €4,000 one-off report | [80] V |
| Evenpay Core | €4,900/year (band-dependent) | [81] V |
| Ravio | £5,000/year for a 500-person company | [83] V (third-party list) |
| Lattice | $13/seat/month + $6 add-on, $4,000 minimum | [83] V |
| Figures | quote; €2,500 or €4,000 starting figures reported (conflicting) | [82][83] |
| Zucchetti, TeamSystem, Inaz, PayAnalytics, Sysarb, Trusaic, Syndio | not published | [83][84][85] |

### 4.4 Market / demand evidence

| # | Signal | Excerpt / figure | Quality |
|---|---|---|---|
| D1 | Law in force in Italy and Greece | D.Lgs. 96/2026 [69]; Law 5316/2026 [76] | Primary-derived, strong |
| D2 | First SME-band deadline | 150–249: first report 7 Jun 2027 (IT, GR); 100–149: 2031 [69][76] | Strong, but narrows the near-term segment |
| D3 | Readiness surveys | Aon 2026 Pulse: 19% ready for reporting; Mercer 2026: 9% of Europe-based employers have a full transparency strategy; Littler 2025: 24% "very prepared"; 42% cite inconsistent job or role data (all snippet) [86] | Secondary, snippet-only, enterprise-weighted |
| D4 | Italian professional-channel activity | Many consulenti del lavoro, Confindustria and payroll-software publishers issued D.Lgs. 96/2026 guides in June–September 2026 (snippets) [72][85] | Secondary, moderate (supply-side) |
| D5 | Italy-specific SME demand survey | None found | UNKNOWN |
| D6 | Community/OSS | 12 GitHub repos, 0 stars [87] | Weak |
| D7 | Political volatility | Sweden seeks renegotiation [78]; Commission refused delay [A1 16] | Moderate |

### 4.5 Customer complaints and feature gaps
- "Almost no vendor publishes a price" — only 2 of 15 pay-equity tools published figures (vendor-authored list, 23 Sep 2026) [83]. VERIFIED (V).
- NCBA-based categorisation is central in Italy [69]; whether generic EU tools handle NCBA levels is UNKNOWN (HYPOTHESIS that they do not).
- No user reviews of SME pay-transparency tools were found. UNKNOWN.

### 4.6 Differentiation opportunities
Could be better (HYPOTHESES): Italian-language, NCBA-level categories; Art. 7 request workflow with the two-month deadline; multi-client mode for consulenti del lavoro; output in the ministerial format once defined.
Could not be better: Zucchetti's payroll data access in Italy [84]; Axios's published €3,000–€4,500 SME pricing and all-EU coverage [80]; statistical and legal depth of enterprise tools; the free EIGE methodology [79].

### 4.7 Switching costs, saturation, acquisition
- Switching: HR data already sits in Italian payroll suites; an external tool needs exports (SUPPORTED INFERENCE).
- Saturation: crowded at mid-market/enterprise; SME-priced EU-wide tools exist [80][81].
- Channels: consulenti del lavoro and payroll-software resellers (partner model visible for Zucchetti [85]); employer associations (Confindustria) [72]. Size and access UNKNOWN.
- Acquisition difficulty (SUPPORTED INFERENCE): high for a new, non-Italian-native entrant; language and professional-channel barriers.

### 4.8 Major risks and obvious weaknesses (O4)
1. **Italian reporting format not yet defined** (ministerial decree pending as far as found) [68][70].
2. **Narrow near-term segment**: 100–149 band not until 2031 [69].
3. **Strong local incumbent** (Zucchetti) and SME-priced EU tools [80][84].
4. **Sensitive personal data** and data-protection-authority involvement, especially for <50 employers [70][72].
5. **Political volatility** (Sweden; possible renegotiation pressure) [78].
6. **Methodological liability**: "work of equal value" judgments; worker-representative sign-off [69][71].

### 4.9 Validation questions still open (O4)
(No interviews possible in this session.)

| # | Question | Evidence |
|---|---|---|
| V4-1 | Has Italy's ministerial decree on reporting modalities been adopted, and what format does it set? | Gazzetta Ufficiale / lavoro.gov.it monitoring |
| V4-2 | Number of Italian employers with 150–249 and 100–149 employees | ISTAT I.Stat extraction by size class |
| V4-3 | How do Italian 150–249 employers plan to report: payroll vendor module, consulente del lavoro, or a new tool? | Interviews with 10 consulenti del lavoro |
| V4-4 | Does Zucchetti HR PayGap cover NCBA-based categories and the final ministerial format, and at what price? | Demo/price enquiry |
| V4-5 | Greece as an alternative (obligations from 1 Nov 2026; Ombudsman platform) — size and language feasibility | Hellenic Statistical Authority size-class data |

### 4.10 Assumptions requiring testing (O4)

| ID | Statement | Label | Test |
|---|---|---|---|
| MV-O4-01 | Italian 150–249 employers need a tool beyond their payroll vendor's module | HYPOTHESIS | V4-3, V4-4 |
| MV-O4-02 | The Italian ministerial format will be published before 2027 reporting preparation begins | PREDICTION | V4-1 |
| MV-O4-03 | A non-Italian small team can serve Italian employers credibly (language, NCBA, channel) | ASSUMPTION | V4-3 |
| MV-O4-04 | SMEs will pay above Axios's €3,000–€4,500/yr anchors | HYPOTHESIS (no evidence) | Pricing test |
| MV-O4-05 | Netherlands, Germany or France transpose by early 2027 | PREDICTION (NL uncertain; DE rumoured; FR before May 2027) [68][77] | Monitor |

---

## 5. O3 — Awaab's Law (watchlist check)
No decisive new evidence. As of the sources found, Awaab's Law does not yet apply to the private rented sector; the extension has no confirmed start date, and commentators point to 2027 at the earliest (snippets, several) [88]. Phase 2 remains 30 Nov 2026. Agent 1's watchlist status and revival conditions are unaffected.

---

## 6. Cross-candidate comparison (evidence only; no scores, no winner)

Each cell describes the **strength of the evidence found** on that dimension, not the attractiveness of the candidate.

| Dimension | O1 CRA (SBOM-capable software SMEs) | O2 GB holiday-pay assurance | O4 Pay Transparency (Italy first) |
|---|---|---|---|
| Legal obligation in force | Strong — Art. 14 applies since 11 Sep 2026; SRP live [1][5] | Strong — records duty since Apr 2026 [45] | Strong in IT (7 Jun 2026) and GR (1 Nov 2026) [69][76]; absent in DE/FR/ES/NL |
| First hard deadline for the segment | Now (per event); Annex I from Dec 2027 | Records now; enforcement expected 2027 [46] | 7 Jun 2027 for 150–249; 2031 for 100–149 [69] |
| Primary pain evidence | Moderate — ENISA surveys (readiness gaps, tool requests) [8][9] | Moderate–strong — DBT statement; vendor docs admitting manual steps; Xero idea (93 votes) [45][50][51][54] | Weak — secondary, enterprise-weighted readiness surveys (snippets) [86] |
| Evidence the target segment is underserved | **Weak / contradicted** — ≥5 SME-priced overlapping offers (§2.0) | Moderate — documented gaps in Xero, Moneysoft, Sage 50; one dedicated add-on; some incumbents automated [49]–[56] | Weak — SME-band tool at €3,000–€4,500/yr; Zucchetti module [80][84] |
| Direct SME-priced competitors found | Many (CVD Portal, ConformOps, sbomify, Article 14 Ready, Kunnus, CRA Evidence) | Few (paiyroll; payroll-native features) | Several (Axios, Evenpay, Zucchetti, Figures) |
| Free / public substitutes | Strong — Dependency-Track with EU KEV, SRP form, GitHub export [2][13][39] | Moderate now, possibly strong later — GOV.UK entitlement calculator; DBT considering a pay calculator [45][47] | Moderate — EIGE toolkit (free method) [79] |
| Published price anchors | €79–€99/month (SME); $159/month; €2,500–€15,000/yr [22]–[29] | 15p/payslip, £30/month minimum [49] | €3,000–€4,900/yr [80][81] |
| Willingness-to-pay signals | Negative/mixed — financial support top request (73%) [8] | Low but present — priced add-on exists; uptake UNKNOWN [49] | UNKNOWN |
| Buyer clarity | Moderate — product/security lead at a software SME (SUPPORTED INFERENCE) | Weak — employer vs bureau unresolved | Weak — HR vs consulente del lavoro vs payroll vendor |
| Channel evidence | Moderate — ENISA channel survey; developer communities [8][10] | Weak — no bureau data found | Weak — professional-channel content only |
| Segment size evidence | Weak — ~1/3 produce SBOMs (whole-sample); package-managed share UNKNOWN | Weak — ~1.23m UK zero-hours workers [A1 46]; employer counts by payroll product UNKNOWN | Weak — 22,861 IT firms at 50–249 (snippet); 100–249 split UNKNOWN |
| Competitor traction published | None | None | None |
| Gating unknowns | EUVD terms; glossary churn | Government calculator; penalty regime final | Italian reporting format |
| Legal-risk exposure of the product | Material (missed matches; compliance implication) | Material (calculation errors) | Material (equal-value categorisation; sensitive data) |

---

## 7. Evidence-quality summary

**Strongest evidence per candidate**
- **O1:** primary legal text and ENISA's own platform documentation define exactly what must be reported, how and when [1][2][3]; two ENISA surveys give primary adoption data [8][9]; vendor pricing pages give hard anchors [22][24].
- **O2:** the government's own consultation (read verbatim) states the complexity, the penalty proposal, the Royal Assent limit and the self-audit incentive [45]; vendor documentation directly admits manual steps (Moneysoft, Sage 50) [50][54]; a public Xero idea with 93 votes and a "not on the roadmap" response [51].
- **O4:** the Italian decree's thresholds and dates (three secondary sources agree) [69][70][71]; a published SME-band price list [80].

**Weakest evidence per candidate**
- **O1:** role-specific SBOM production share; paying demand (no traction for any vendor; the HN thread is tiny); frequency of actively exploited vulnerabilities in SME products; EUVD licensing.
- **O2:** buyer identity and bureau channel size; miscalculation prevalence; BrightPay/QuickBooks capability conflicts; forums unreachable.
- **O4:** the Italian reporting format (not yet defined as far as found); Italian SME demand (no survey); segment size by the 100–249 split; readiness surveys are snippet-only and enterprise-weighted.

**Source mix (this artifact's §9 list):** 87 numbered source entries (entry 67 unused), many grouping several URLs. Primary sources (P) include the CRA OJ text, the ENISA glossary/FAQ/surveys, EUVD docs, the DBT consultation, GOV.UK pages, and product documentation for own features. Every price was read on the vendor's own page except those marked snippet and the Ravio, Lattice and PayAnalytics figures, which come from a third-party vendor list [83]. Snippet-only items are marked in §9 and include the CVE terms of use [20], the SECURE co-financing rate [12], several Italian status items [72]–[74], the readiness surveys [86], the Awaab's Law PRS status [88], and several vendor capability claims [35]–[37], [62]–[66], [85].

**Items that should be re-read before external use:** [20] (CVE ToU), [52] (BrightPay "will not calculate" statement), [72]–[74], [86], and any Italian ministerial-decree status after 26 Sep 2026.

---

## 8. Consolidated open unknowns (for the Orchestrator's assumption registry)

| ID | Unknown | Candidate |
|---|---|---|
| MV-U01 | Role-specific (software-developer SME) SBOM production share | O1 |
| MV-U02 | EUVD commercial-reuse terms | O1 |
| MV-U03 | Paying traction of any SME CRA tool | O1 |
| MV-U04 | Employer vs bureau buyer; number of UK payroll bureaus | O2 |
| MV-U05 | BrightPay and QuickBooks 52-week-rate automation in 2026-27 | O2 |
| MV-U06 | Whether DBT/FWA will publish a free holiday-pay calculator | O2 |
| MV-U07 | Italian ministerial decree on reporting format (adopted or not) | O4 |
| MV-U08 | Italian employer counts at 100–149 and 150–249 | O4 |

---

## 9. Sources (accessed 2026-09-26 unless stated)

Grade: P / S / V (see header). Access: **Read** = fetched and read (or extracted locally); **Snippet** = search-result summary only.

**CRA — law, regulator, surveys (O1)**
1. Regulation (EU) 2024/2847, OJ text (Arts. 14–16) — https://publications.europa.eu/resource/celex/32024R2847 — P, Read (local XHTML extraction)
2. ENISA, *CRA SRP Glossary*, Version 1.3, "Last update: 25 September 2026" — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/cra-srp-glossary2 — P, Read (HTML table parsed; the `…/cra-srp-glossary` URL returned 403)
3. ENISA, SRP Frequently Asked Questions (FAQ 15 API; FAQ 24 language; FAQ 19 EUVD) — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/frequently-asked-questions — P, Read
4. ENISA, Single Reporting Platform (SRP) page (factsheet v1.0 Jul 2026; T&Cs v1.0 10 Sep 2026; AR guidance 9–10 Sep 2026) — https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp — P, Read
5. ENISA news, "The CRA Single Reporting Platform is launched", 11 Sep 2026 — https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched — P, Read
6. Help Net Security, "ENISA launched the CRA Single Reporting Platform…", 14 Sep 2026 — https://www.helpnetsecurity.com/2026/09/14/enisa-cra-single-reporting-platform/ — S, Read
7. sbomify, "The CRA Single Reporting Platform Opens Tomorrow: What ENISA Actually Requires", 10 Sep 2026 — https://sbomify.com/2026/09/10/cra-single-reporting-platform-enisa-srp/ — V, Read
8. ENISA, *SME CRA Survey Report*, 24 Jun 2026 (CC BY 4.0) — https://www.enisa.europa.eu/sites/default/files/2026-06/SME%20CRA%20survey%20report.pdf — P, Read (local PDF)
9. ENISA, *SBOM Adoption State of Play – 2026*, June 2026 (CC BY 4.0) — https://www.enisa.europa.eu/sites/default/files/2026-06/SBOM%20Adoption%20State%20of%20Play%202026.pdf — P, Read (local PDF)
10. Linux Foundation, "The CRA Readiness Reality: What Changed (and What Didn't) Between 2025 and 2026", 19 Jun 2026 — https://www.linuxfoundation.org/blog/the-cra-readiness-reality-what-changed-and-what-didnt-between-2025-and-2026 — S, Read
11. European Commission, "CRA – MSMEs", last update 31 Jul 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-msmes — P, Read
12. SECURE (secure4sme) First Open Call — https://www.secure4sme.eu/cascade-funding/first-open-call — P (EU-funded project), Read; 50% co-financing and Jan–Mar 2026 dates from https://www.digitalsme.eu/fundings/open-call-for-smes-to-strengthen-cyber-resilience/ — S, Snippet
13. GitHub Docs, "Exporting a software bill of materials for your repository" — https://docs.github.com/en/code-security/supply-chain-security/understanding-your-software-supply-chain/exporting-a-software-bill-of-materials-for-your-repository — P (own-feature docs), Read

**Vulnerability-data licences (O1)**
14. OSV, "Data sources" — https://google.github.io/osv.dev/data/ — P, Read
15. GitHub Advisory Database repository (licence statement) — https://github.com/github/advisory-database — P, Read
16. NIST NVD API Terms of Use, as reproduced by ScanCode LicenseDB (generated 21 Sep 2026) — https://scancode-licensedb.aboutcode.org/nist-nvd-api-tou.html ; original https://nvd.nist.gov/developers/terms-of-use (JavaScript-only, not readable) — S (reproduction), Read
17. ENISA EUVD public documentation (API and FAQ), served to euvd.enisa.europa.eu from https://raw.githubusercontent.com/enisaeu/euvd-docs-public/main/apidoc.md and …/faq.md — P, Read
18. ENISA, Legal Notice — https://www.enisa.europa.eu/about-enisa/legal-notice/legal-notice — P, Read
19. CISA, KEV data repository (CC0) — https://github.com/cisagov/kev-data — P, Read
20. CVE Terms of Use (SPDX "cve-tou") — https://spdx.org/licenses/cve-tou.html — S, Snippet

**CRA competitors and substitutes (O1)**
21. Cyber Vendor Guide, "CRA Compliance Companies (2026)", updated Aug 2026 — https://www.cybervendorguide.com/guides/cra-compliance — S, Read
22. ConformOps — https://conformops.eu — V, Read
23. Article 14 Ready — https://article14ready.com — V, Read
24. CVD Portal — https://cvdportal.com and https://cvdportal.com/pricing — V, Read
25. CRA Evidence — https://craevidence.com/platform and https://craevidence.com/pricing — V, Read
26. Kunnus — https://kunnus.tech/en — V, Read; Capterra listing — https://www.capterra.com/p/10036889/Kunnus/ — S, Read
27. sbomify pricing — https://sbomify.com/pricing/ — V, Read; repository metadata https://github.com/sbomify/sbomify — P, Read (GitHub API)
28. Regulus — https://goregulus.com/ — V, Read; cost-calculator claims https://goregulus.com/resources/cra-cost-calculator/ — V, Snippet
29. Zealience Z-CMS pricing — https://zealience.com/pricing/ — V, Read
30. Vulert pricing — https://vulert.com/pricing — V, Read
31. Aikido Security pricing — https://www.aikido.dev/pricing — V, Read
32. SBOM Observer — https://sbom.observer/ — V, Read
33. ReARM — https://rearmhq.com/ — V, Read
34. Distr pricing — https://distr.sh/pricing/ — V, Read
35. UnitOne — https://unitone.ai/faq ; https://unitone.ai/blog/cra-article-14-security-evidence-checklist — V, Snippet
36. Interlynk (AWS Marketplace) — https://aws.amazon.com/marketplace/pp/prodview-n6mc7symiq2rm ; Cybeats — https://www.cybeats.com/product/sbom-studio — V, Snippet
37. Black Duck, "Are you ready: CRA reporting" — https://www.blackduck.com/resources/webinars/are-you-ready-cra-reporting.html — V, Snippet
38. EdgeLabs, "10 Best CRA Compliance Tools", 3 Aug 2026 — https://edgelabs.ai/blog/cra-compliance-tools — V, Read
39. Dependency-Track 5.1.0 release news, 31 Aug 2026 — https://dependencytrack.org/news/dependency-track-5-1/ — P, Read; repository metadata (Apache-2.0; 4,238 stars) https://github.com/DependencyTrack/dependency-track — P, Read (GitHub API)
40. Dependency-Track issue #5992 (opened 2 Apr 2026) — https://github.com/DependencyTrack/dependency-track/issues/5992 — P, Read; issues #3178, #3268, #3063 — Snippet
41. Hacker News, "Ask HN: Is anyone else preparing for the EU Cyber Resilience Act?" — https://news.ycombinator.com/item?id=49520688 — P (forum), Read
42. GitHub repository search "cyber resilience act" sorted by stars (114 results; cra-agent, DX.Comply, awesome-cra-compliance, zealience/Cyber-Resilience-Act, OpenChain-Project/CRA-Compliance, crawatch.dev, CycloneDX.CRA.Validator) — GitHub API, 2026-09-26 — P, Read
43. robertolocatelli81-dev/cra-evidence — https://github.com/robertolocatelli81-dev/cra-evidence — P, Read
44. Open Regulatory Compliance WG, CRA page — https://orcwg.org/cra/ — S, Read

**Holiday records and pay (O2)**
45. DBT, *Make Work Pay: Holiday Pay Compliance and Enforcement*, 30 Jun 2026, closed 22 Sep 2026 — https://assets.publishing.service.gov.uk/media/6a3e79add52550a19950f617/make-work-pay-holiday-pay-compliance-and-enforcement.pdf — P, Read (local PDF)
46. GOV.UK, *Fair Work Agency delivery plan 2026 to 2027*, 21 Aug 2026 — https://www.gov.uk/government/publications/fair-work-agency-delivery-plan-for-2026-to-2027/fair-work-agency-delivery-plan-2026-to-2027 — P, Read; PAYadvice.UK summary, 12 Aug 2026 — https://payadvice.uk/2026/08/12/fair-work-agency-delivery-plan/ — S, Read
47. GOV.UK, "Calculate holiday entitlement" — https://www.gov.uk/calculate-your-holiday-entitlement — P, Read
48. GOV.UK, "Holiday pay: calculate your average weekly pay if it varied", 6 Apr 2021 — https://www.gov.uk/government/publications/holiday-pay-calculate-your-average-weekly-pay-if-it-varied/holiday-pay-calculate-your-average-weekly-pay-if-it-varied — P, Read
49. paiyroll, "Automated holiday pay for existing payroll software" — https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ — V, Read
50. Moneysoft, "Holiday Pay for irregular hours and part-year workers" — https://moneysoft.co.uk/support/holiday-pay-for-irregular-hours-and-part-year-workers/ — P (own-product docs), Read
51. Xero Product Ideas, "UK Payroll: Reporting – Run a report to calculate holiday pay based on a 52 week average" — https://productideas.xero.com/forums/967118-payroll-expenses/suggestions/45241594-uk-payroll-reporting-run-a-report-to-calculate — P (vendor forum), Read
52. BrightPay docs, "Annual Leave Entitlement Methods" (2025-26) — https://www.brightpay.co.uk/docs/25-26/annual-leave/annual-leave-entitlement-methods-in-brightpay/ — P, Read; "will not calculate holiday pay amounts" statement — https://www.brightpay.co.uk/docs/24-25/annual-leave/holiday-entitlements-useful-information/ and https://payrollsupport.uk.brightsg.com/hc/en-gb/articles/39828589872401 — Snippet (support hub 403; statement not found in the 2025-26 page text)
53. Staffology help: "Set up Average Holiday Pay schemes" (updated 24 Jun 2026) — https://help.staffology.co.uk/payroll/leave-and-absence/holidays/average-holiday/configuring-average-hol.htm ; "Guide to average holiday pay" (1 May 2026) — https://help.staffology.co.uk/payroll/leave-and-absence/holidays/average-holiday/information-average-holiday-pay.htm ; "Coming soon" (23 Sep 2026) — https://help.staffology.co.uk/payroll/produpdates/coming-soon.htm — P, Read
54. Sage KB, "How do I calculate holiday pay rate for employees working variable hours?" (last modified 4 Sep 2024) — https://gb-kb.sage.com/portal/app/portlets/results/viewsolution.jsp?solutionid=230308162057663 — P, Read; Sage Community Hub threads 254095 (Read), 209263 (Read), 219636 (Snippet) — https://communityhub.sage.com/gb/sage-50-payroll/f/general-discussion/254095/processing-holiday-pay-using-52-week-average-method
55. QuickBooks Community, "Holiday pay and holiday entitlement" (from 12 Jul 2020) — https://quickbooks.intuit.com/learn-support/en-uk/other-questions/holiday-pay-and-holiday-entitlement/00/619909 — P (vendor forum), Read
56. KeyPay (Employment Hero), "52 week averaging for holiday pay" — https://www.keypay.co.uk/features/52-week-averaging — P (own-product), Read
57. IRIS Help Hub, Earnie Holiday Pay Module (updated 16 Feb 2026) — https://help-iris.co.uk/payroll/earnie/modules/hol/holiday-landing.htm — P, Read
58. StaffLeave, "UK Holiday Pay Rules 2026" — https://www.staffleave.com/blog/uk-holiday-pay-rules-2026 — V, Read
59. Employment Hero, "What the six-year records rule means for HR and payroll" (updated 18 Jun 2026) — https://employmenthero.com/uk/blog/six-year-records-rule-holiday-pay-compliance/ — V, Read
60. Association of Taxation Technicians, "Holiday pay – new record keeping requirements", 16 Jun 2026 — https://www.att.org.uk/employers/welcome-employer-focus/holiday-pay-new-record-keeping-requirements — S, Read
61. CIPP, "Employers must keep annual leave and pay records from 6 April", 30 Mar 2026 — https://www.cipp.org.uk/resources/news/annual-leave-and-pay-records-from-6-april.html — S, Read
62. RotaCloud — https://help.rotacloud.com/en/articles/10265253 ; Planday — https://help.planday.com/en/articles/203779 ; Fourth — https://help.hotschedules.com/hc/en-us/articles/20326128917389 — V, Snippet
63. Healthbox HR — https://healthboxhr.com/pricing — V, Snippet
64. Worker-side calculators: https://www.payslipchecker.uk/zero-hours-holiday-pay-checker ; https://www.timetally.uk/zero-hours-holiday-calculator ; https://uktax.tools/holiday-pay-calculator/ ; https://youtemp.co.uk/tools/holiday-pay-calculator/ — V, Snippet
65. Azets, "New holiday pay and leave record-keeping requirements from 6 April 2026" — https://www.azets.com/en-uk/resources/new-holiday-pay-and-leave-record-keeping-requirements-from-6-april-2026 — S/V, Snippet
66. Payroll-outsourcing statistics aggregators (e.g., https://corientbs.co.uk/blog/what-percentage-of-companies-outsource-payroll/ ; https://acenteus-cca.com/blog/payroll-outsourcing-costs-in-uk) — V, Snippet (low quality; not relied on)
67. (unused)

**Pay transparency (O4)**
68. Ius Laboris, "EU Pay Transparency Directive: which countries have transposed", 23.09.26 — https://iuslaboris.com/insights/eu-pay-transparency-directive-which-countries-have-transposed/ — S, Read (full HTML via curl; map not machine-readable)
69. Littler, "Italy Implements the EU Pay Transparency Directive: A Guide to the Final Decree" — https://www.littler.com/news-analysis/asap/italy-implements-eu-pay-transparency-directive-guide-final-decree — S, Read
70. Edotto, "Parità retributiva e trasparenza salariale: tutte le novità del decreto definitivo", 3 Jun 2026 — https://www.edotto.com/articolo/parita-retributiva-e-trasparenza-salariale-tutte-le-novita-del-decreto-definitivo — S, Read
71. EC News, "Gender pay gap, reporting e tutele: gli adempimenti previsti dal D.Lgs. n. 96/2026", 4 Jun 2026 — https://www.ecnews.it/lavoro/rapporto-di-lavoro/gestione-del-rapporto/gender-pay-gap-reporting-e-tutele-gli-adempimenti-previsti-dal-d-lgs-n-96-2026/ — S, Read
72. Italian status snippets: Altalex (5 Jun and 22 Sep 2026), IPSOA (3 Jun 2026), Ministero del Lavoro press release (CdM approval), Garante opinion of 26 Mar 2026 — https://www.altalex.com/documents/2026/06/05/trasparenza-retributiva-d-lgs-96-2026-attua-direttiva-ue-2023-970 ; https://www.lavoro.gov.it/stampa-e-media/comunicati/pagine/trasparenza-retributiva-primo-si-del-cdm ; https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10242702 — S/P, Snippet
73. Rapporto biennale (art. 46 D.Lgs. 198/2006): https://www.lavoro.gov.it/strumenti-e-servizi/rapporto-periodico-situazione-personale/Pagine/default ; https://www.mysolution.it/lavoro/approfondimenti/circolare-monografica/2026/05/rapporto-sulla-situazione-del-personale-maschile-e-femminile-prorogata-la-scadenza-di-presentazione/ ; https://www.pmi.it/impresa/contabilita-e-fisco/439324/rapporto-biennale-pari-opportunita-regole-scadenze.html — P/S, Snippet (several agree)
74. ISTAT, census report (14 Nov 2023) — https://www.istat.it/it/files/2023/11/REPORTCensimprese.pdf — P, Snippet
75. Lewis Silkin, "Pay Transparency Directive FAQs", 25 Jun 2026 — https://www.lewissilkin.com/insights/2026/06/25/pay-transparency-directive-faqs — S, Read
76. Lewis Silkin, "Greece transposes the EU Pay Transparency Directive", 13 Jul 2026 — https://www.lewissilkin.com/insights/2026/07/13/greece-transposes-the-eu-pay-transparency-directive-what-employers-need-to-know — S, Read; Jackson Lewis — https://www.jacksonlewis.com/insights/eu-pay-transparency-greece-becomes-fifth-member-state-finalize-directive-transposition ; Zepos & Yannopoulos — https://www.zeya.com/newsletters/law-53162026-greece-transposes-eu-pay-transparency-directive — S, Snippet
77. People Performance Reward, "EU Pay Transparency Directive Update September 2026", 2 Sep 2026 — https://www.people-performance-reward.co.uk/post/eu-pay-transparency-directive-update-september-2026 — S/V (consultancy), Read
78. Pinsent Masons Out-Law, "Sweden will not implement the EU Pay Transparency Directive", 20 Apr 2026 — https://www.pinsentmasons.com/out-law/news/sweden-not-implement-eu-pay-transparency-directive — S, Read
79. Baker McKenzie, "European Union: Toolkit Launched to Support Pay Transparency Compliance", 7 Apr 2026 — https://www.bakermckenzie.com/en/insight/publications/2026/04/european-union-toolkit-launched-to-support-pay-transparency-compliance — S, Read
80. Axios Analytics pricing — https://axiosanalytics.com/pricing — V, Read
81. Evenpay pricing — https://evenpay.io/pricing/ — V, Read
82. Figures pricing — https://figures.hr/pricing — V, Read (no figures); "starts at EUR 2,500/yr" — Snippet
83. effy.ai, "Pay Equity Software: 15 Tools and 2 Published Prices", 23 Sep 2026 — https://www.effy.ai/blog/pay-equity-software — V, Read
84. Zucchetti, "Software per la trasparenza retributiva" (HR PayGap) — https://www.zucchetti.it/it/cms/soluzioni/software-hr-zucchetti/hr-core-platform/software-trasparenza-retributiva/software-trasparenza-retributiva.html — V, Read
85. TeamSystem, Inaz, Veridian, errepi pages on D.Lgs. 96/2026 — https://www.teamsystem.com/magazine/risorse-umane/parita-trasparenza-salariale-direttiva-ue-2023-970/ ; https://www.inaz.it/chi-siamo/csr/trasparenza-salariale/ ; https://www.veridian.it/gender-pay-gap-e-trasparenza-retributiva-la-soluzione-hr-paygap/ ; https://www.errepi.it/paghe-e-hr-per-associazioni-e-professionisti/hr-paygap/ — V, Snippet
86. Readiness surveys (Aon 2026 Pay Transparency Pulse; Mercer 2026 Global Pay Transparency Survey; Littler European Employer Survey 2025), as summarised by https://www.workaxle.com/blog/eu-pay-transparency-directive-2026-requirements-deadlines and others — S, Snippet (not read in original)
87. GitHub repository searches: "pay transparency" EU directive (12 results, 0 stars) and "holiday pay" uk (1 result) — GitHub API, 2026-09-26 — P, Read

**Awaab's Law (O3)**
88. Awaab's Law private-rented-sector status: https://www.russell-cooke.co.uk/news-and-insights/news/awaab-s-law-extending-safety-standards-to-the-private-rented-sector ; https://www.nrla.org.uk/news/how-to-prepare-for-awaabs-law-as-a-private-landlord — S, Snippet

**Agent 1 sources referenced, not re-read:** [A1 3] CRA corrigendum; [A1 16] Commission refusal to delay; [A1 19] Axios buyer guide; [A1 38] Interlynk C/C++ SBOM report; [A1 45] CIPP 2024 survey (snippet); [A1 46] ONS EMP17.

---

## 10. Out-of-scope findings (reported to the Orchestrator)

| ID | Finding | Responsible agent |
|---|---|---|
| OOS-MV-01 | The approved v2 (O4 status) says Ius Laboris treats only Italy as transposed. Sources read here record Malta, Lithuania and Slovakia (by 7 Jun 2026) and **Greece (Law 5316/2026, 6 Jul 2026; obligations from 1 Nov 2026)** as transposed, and Sweden as paused. This is not an error in v2's use of its source, but the O4 landscape in v2 is outdated. I have not edited v2. | Orchestrator; Agent 1 (if v2 is reopened); Agent 3 (jurisdiction choice) |
| OOS-MV-02 | ENISA's SRP glossary changed from v1.1 (5 Sep 2026) to v1.3 (25 Sep 2026) in three weeks. Any O1 field schema must be versioned, and the UI must show the glossary version used. | Agent 9 Architecture; Agent 4 Requirements |
| OOS-MV-03 | EUVD has no licence or terms of use in its docs or app; ENISA's general legal notice may or may not apply, and EUVD contains third-party data. Get written confirmation from ENISA before ingesting EUVD commercially. OSV's Ubuntu source is CC-BY-SA 4.0 (share-alike); GHSA/PyPI/Go are CC-BY 4.0 (attribution); the NVD API requires a specific non-endorsement notice. | Agent 14 Legal & Privacy; Agent 9 |
| OOS-MV-04 | DBT is considering a free holiday-*pay* calculator or self-assessment tool, and the FWA plans "guidance and tools". This is a strategic commoditisation risk for O2. | Agent 3 Strategy |
| OOS-MV-05 | FWA exposure is limited to underpayments after 18 Dec 2025 (Royal Assent), and the "no penalty if repaid before investigation" rule is only a proposal. Marketing must not claim "six years of exposure" or promise penalty avoidance. | Agent 7 Marketing; Agent 14 |
| OOS-MV-06 | The CRA market contains misinformation that SMEs cannot be fined for Art. 14 deadlines. Only micro and small enterprises are exempt, and only from fines for the 24-hour early-warning deadline. Product and marketing copy must state this precisely. | Agent 7; Agent 14 |
| OOS-MV-07 | Several competitors in all three candidates market AI features (cra-agent, UnitOne, AI pay-transparency prototypes). Any "AI-free" positioning is a positioning choice; no evidence was found that buyers value it. | Agent 3; Agent 7; Agent 19 Runtime Independence |
| OOS-MV-08 | An Art. 14(7) "which CSIRT is your coordinator" helper (main establishment; non-EU fallback rules) would border on legal advice. | Agent 14; Agent 4 |
| OOS-MV-09 | Research tooling notes: the ENISA glossary is readable at `…/cra-srp-glossary2` via curl; the EUVD docs are the Markdown files at `raw.githubusercontent.com/enisaeu/euvd-docs-public/main/`; the NVD terms are readable via ScanCode LicenseDB; the Ius Laboris tracker's full text is readable via curl. | All research agents; Orchestrator |
| OOS-MV-10 | O4 in Italy processes pay data by sex. The Garante's involvement and the specific rules for employers with fewer than 50 employees to prevent re-identification will shape data design (DPIA). | Agent 13 Security; Agent 14; Agent 10 Database |
