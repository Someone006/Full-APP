# SaaS Opportunity Research — v1

| Field | Value |
|---|---|
| Artifact | `project/research/opportunity-research-v1.md` |
| Owner | Agent 1 — SaaS Opportunity Researcher |
| Research date | 2026-09-26 (all "status" statements are as of this date unless a source date is given) |
| Status | DRAFT v1 — submitted for independent judging |
| Scope of this artifact | Proposes and ranks opportunity areas for market validation. It does **not** choose the product, define strategy, pricing, or requirements (Agents 2, 3, 4, 6). |

### Evidence labels used in this document

| Label | Meaning here |
|---|---|
| **VERIFIED [n]** | Stated by the cited source(s). Section 7 records for every source whether the page was **read** (fetched and read in this session) or seen only as a **snippet** (search-result summary). Where only snippets exist for an important claim, at least two independent snippets were required, and the claim is listed in §6 for re-reading by Market Validation. Source grade in §7: **P** = primary/official, **S** = reputable secondary (law firm, parliamentary library, trade body, news), **V** = vendor/marketing page (only used to show that a vendor *claims* an offering). |
| **SUPPORTED INFERENCE** | My reasoning from verified facts; not directly stated by a source. |
| **ASSUMPTION** | Taken as true for the analysis without evidence; must be tested. |
| **HYPOTHESIS** | A testable proposition, usually about customers or demand. |
| **PREDICTION** | A statement about the future. |
| **UNKNOWN** | Not established. |

No numerical market scores or invented market sizes appear in this document. Every number quoted is attributed to a source and dated.

---

## 1. Scope & method

### 1.1 Objective
Produce an evidence-based landscape of SaaS opportunities and recommend 2–4 for market validation, where the eventual product:

1. **Hard filter — AI-free runtime:** primary value delivered by deterministic software (database, rules/calculation engines, scheduled jobs, search, forms, documents, email, payments). No LLM/generative-AI dependency at runtime (Agent Charter, "Absolute runtime rule").
2. **Hard filter — MVP feasibility:** a production-quality MVP is realistic for a small team in a few weeks of focused engineering as a single web app + Postgres + payments + email. Opportunities that fundamentally require certification/accreditation before selling, hardware, deep bank/payroll/government write-integrations, or regulated identity verification fail this filter.
3. **Soft criteria (qualitative, no scores):** pain severity and consequence of inaction; obligation certainty and timing (in force / fixed deadline vs. postponed / draft); buyer reachability and plausible willingness to pay; competitive density and whether a small team can be differentiated; legal-risk of the product being wrong; durability over a 3–5 year horizon (to ~2029–2031).

### 1.2 Areas searched (2026-09-26)
- **EU regulatory drivers:** Pay Transparency Directive 2023/970 (transposition status by country, delay requests); e-invoicing mandates (Germany, Belgium, France, Poland, Spain Verifactu) and UK e-invoicing 2029; European Accessibility Act enforcement; NIS2 (German transposition); DORA register of information; EU AI Act and the 2026 "Digital Omnibus on AI"; CSRD after Omnibus I and the voluntary SME standard (VSME/"VS"); Whistleblowing Directive; **Cyber Resilience Act** (reporting obligations from 11 Sep 2026); EUDR (2025 amendment, 2026 simplification review); PPWR/EPR packaging (applies 12 Aug 2026); Short-Term Rental Regulation 2024/1028; F-gas Regulation 2024/573; Spain digital working-time recording decree.
- **UK drivers:** Employment Rights Act 2025 (holiday-record duty from 6 Apr 2026, Fair Work Agency, tipping consultation duty); Renters' Rights Act 2025 (tenancy reform 1 May 2026, PRS database, ombudsman); Making Tax Digital for Income Tax (from 6 Apr 2026); Awaab's Law (social housing, Phase 1 Oct 2025, Phase 2 Nov 2026); Martyn's Law (Terrorism (Protection of Premises) Act 2025).
- **US drivers:** FDA Food Traceability Rule (FSMA 204) extension; state pay-transparency laws; state comprehensive privacy laws.
- **Non-regulatory SMB operations:** field service/trades job management; allied-health clinic practice management; construction subcontractor certificate-of-insurance (COI) tracking; UK landlord self-management; hospitality tip allocation.

Representative queries (abridged): "EU Pay Transparency Directive transposition status member states 2026"; "pay transparency directive delay omnibus 2026"; "Cyber Resilience Act reporting obligations 11 September 2026 ENISA single reporting platform"; "ENISA SME CRA survey"; "Employment Rights Act 2025 holiday records six years"; "Awaab's Law phase 2 2026"; "FDA food traceability compliance date July 20 2028"; "Digital Omnibus AI Act high-risk delay"; "Omnibus I CSRD Official Journal"; "EUDR simplification review 2026"; "PPWR 12 August 2026 authorised representative"; plus competitor-landscape queries for each area (e.g., "pay transparency software SMB", "CRA compliance platform SME", "landlord compliance software UK 2026", "Martyn's Law compliance software", "EPR software small EU sellers", "FSMA 204 software small business").

### 1.3 Method
- Web search to map each area, then direct reading (WebFetch) of primary sources where reachable (EUR-Lex, European Commission, ENISA, GOV.UK, FDA, Regulator of Social Housing, Congressional Research Service) and of dated law-firm analyses for transposition/implementation status.
- Explicit check, for every regulation relied on, for 2025–2026 postponements or amendments (found and recorded: AI Act Digital Omnibus; CSRD Omnibus I; EUDR amendment 2025/2650 and 2026 simplification package; FSMA 204 30-month extension; Verifactu postponement; ERA 2025 revised roadmap; PPWR environmental-omnibus proposal; and the Commission's refusal to postpone the Pay Transparency Directive).
- Competitors were identified by searching for them; the lists are **not exhaustive** and absence of a found competitor is never treated as absence of competition.

### 1.4 Limitations (read before relying on this document)
- **No primary customer research** (no interviews, surveys, or pricing tests). All demand statements about specific segments are HYPOTHESES for Agent 2.
- **WebFetch returns a model-generated summary** of each page, not the verbatim page. Quotations and dates were taken from those summaries; material legal facts should be re-read in the original by Market Validation (list in §6).
- Some sources could not be read: the Home Office Martyn's Law impact assessment PDF was not machine-readable in this environment; the House of Commons Library Renters' Rights briefing returned HTTP 403; one Xero product-ideas page returned 404.
- Search is US-hosted and English-biased; national-language sources (DE/FR/ES/IT/PL) were only sampled.
- Vendor pages are self-descriptions. They establish that a vendor *claims* an offering, not that it works or has customers.

---

## 2. Opportunity landscape

Qualitative verdicts are SUPPORTED INFERENCE from the evidence in §3. "AI-free?" = can the core value be delivered deterministically. "MVP?" = feasible as a single web app + Postgres + payments + email in a few weeks.

| # | Area | Driver & status (as of 2026-09-26) | Who has the problem | Competition found | AI-free? | MVP? | Verdict |
|---|---|---|---|---|---|---|---|
| O1 | **EU Cyber Resilience Act (CRA) evidence, vulnerability-handling & reporting workspace for small manufacturers** | Reg. (EU) 2024/2847. Art. 14 reporting in force **11 Sep 2026** incl. for products already on market; main obligations **11 Dec 2027** [12][13][14][20] | SME makers of connected hardware, firmware and software products sold in the EU | Emerging, fragmented: ONEKEY, Article 14 Ready, CVD Portal, ConformOps, Anchore, Finite State, Cycode, free OWASP Dependency-Track, test/cert houses [22][23][24] | Yes | Yes | **Recommend #1** |
| O2 | **UK holiday-record & holiday-pay assurance for variable-hours employers** | ERA 2025 duty to keep adequate holiday records for 6 years, criminal offence, from **6 Apr 2026**; Fair Work Agency live 7 Apr 2026; holiday-pay enforcement expected 2027 [27][28][30] | UK SMEs with irregular-hours / variable-pay staff (hospitality, care, retail, cleaning, agencies) and their payroll bureaus | Crowded in leave tracking (BrightHR, Breathe, Timetastic, etc.); calc-specific add-on exists (paiyroll) [32][34] | Yes | Yes | **Recommend #2** |
| O3 | **Awaab's Law case & statutory-clock management for small social landlords** | Phase 1 in force 27 Oct 2025; Phase 2 (more hazards) **30 Nov 2026**; Phase 3 expected 2027 [37] | ~1,100 small private registered providers (<1,000 homes) plus stock-holding councils [38] | Enterprise HMS/CX vendors (Netcall, Propsys360, Plentific), law-firm tool (Weightmans), pre-launch small-provider tool (HazardClock) [39][40] | Yes | Yes | **Recommend #3** |
| O4 | **EU Pay Transparency compliance for SME / lower-mid-market employers** | Dir. 2023/970; transposition deadline 7 Jun 2026 missed by most; only IT, SK, LT, MT on time; DE/FR/ES/IE still draft or earlier [1][2][4] | Employers 100–249 (reporting) and all employers (pay-range and right-to-information duties) | Crowded: Figures, Ravio, Personio, Sysarb, Trusaic, Syndio, PayAnalytics, beqom, Axios Analytics, TracefyHR [8][9][10][11] | Yes | Yes (single jurisdiction) | **Recommend #4 (conditional)** |
| O5 | US FSMA 204 food traceability for small food businesses | Compliance/enforcement not before **20 Jul 2028** (Congressional directive); FDA told to consider flexibilities [42][43] | >323,000 US businesses / >484,100 establishments (FDA estimate) [43] | ReposiTrak, iFoodDS, Trustwell, FoodReady, Inecta, Nulogy and others [44] | Yes | Yes | Watchlist |
| O6 | UK Martyn's Law (standard-tier premises) | Expected in force **spring 2027**; SIA portal testing early 2027 [45] | Venues/premises with capacity 200+ (standard tier 200–799) | Many low-price tools already (from £19/month claimed) [47] | Yes | Yes | Watchlist / reject now |
| O7 | EU/UK e-invoicing mandates | BE Jan 2026; PL KSeF 2026–27; FR Sep 2026/Sep 2027 via approved platforms; DE issue 2027/2028; ES Verifactu 2027; UK Apr 2029 [48]–[52] | All VAT-registered B2B businesses | Very crowded; ~137+ French approved platforms; accounting suites [49] | Yes | No (certification/network access) | Reject |
| O8 | European Accessibility Act | Applies since 28 Jun 2025; enforcement starting, no fines found in year one [53] | E-commerce, banking, e-books, transport ticketing (micro-enterprise services exempt) | Very crowded (Level Access, Deque, Siteimprove, many checkers) [53] | Yes | Partly | Reject |
| O9 | NIS2 | DE law in force 6 Dec 2025; BSI registration due 6 Mar 2026 [55] | Essential/important entities (DE ~29,500 per secondary source) | Very crowded GRC (Vanta, Drata, Secfix, ISMS tools) | Yes | Partly | Reject |
| O10 | DORA register of information | Annual RoI submissions (e.g., CSSF window 11 Feb–31 Mar 2026) [56] | EU financial entities | GRC suites + specialist RoI tools | Yes | Yes | Reject |
| O11 | EU AI Act deployer obligations | Digital Omnibus in force 27 Jul 2026: Annex III high-risk to 2 Dec 2027, Annex I to 2 Aug 2028; Art. 4 literacy softened [57][58][59] | AI deployers | Crowded AI-governance tools [60] | Yes | Yes | Reject |
| O12 | CSRD / voluntary SME standard (VSME/"VS") | Omnibus I in OJ 26 Feb 2026 (>1,000 staff & >€450m); VS delegated act adopted 3 Jul 2026 [61][62] | SME suppliers asked for ESG data | Crowded (osapiens, Dcycle, Sunhat, Coolset, etc.) [63] | Yes | Yes | Reject |
| O13 | Whistleblowing Directive channels | In force since transposition; 50+ workers [64] | Employers 50+ | Commoditised; published prices from ~€19/month [64] | Yes | Yes | Reject |
| O14 | EUDR due-diligence | Applies 30 Dec 2026 (large/medium), 30 Jun 2027 (micro/small); no further postponement per May 2026 package [65][66] | Operators/traders of cattle, cocoa, coffee, palm, rubber, soy, wood | Crowded, geo-data heavy | Yes | Partly | Reject |
| O15 | PPWR / multi-country packaging EPR | PPWR applies 12 Aug 2026; national EPR registers per country [67][68] | Cross-border e-commerce sellers | Crowded new entrants (Gramta, Repax, Lappa, EPR Insights) + compliance schemes [68] | Yes | Partly | Reject |
| O16 | EU Short-Term Rental Regulation | Applies 20 May 2026; obligations mainly on member states and platforms [69] | STR hosts, property managers | Channel managers, guest-registration tools (Chekin etc.) [70] | Yes | Yes | Reject |
| O17 | UK landlord compliance (Renters' Rights Act, PRS database, MTD ITSA) | Tenancy reform 1 May 2026; PRS database rollout from 15 Dec 2026; MTD ITSA from 6 Apr 2026 [71][72][73][75] | ~2.3–2.8m private landlords (estimates vary) [76] | Saturated incl. free tools (LetDeck, LetCompliance, Landlord Studio, Hammock…) [74] | Yes | Yes | Reject |
| O18 | UK tipping allocation & consultation duty | Tips Act in force Oct 2024; ERA consultation duty expected by end 2026 [77] | Hospitality employers | TiPJAR, JustTip, IRIS Tronc, others [78] | Yes | Yes | Reject |
| O19 | US state pay-transparency job-posting compliance | Multiple states in force; Delaware 2027 [79] | Multi-state employers | Covered by ATS/HRIS/payroll suites [79] | Yes | Yes | Reject |
| O20 | US state privacy laws | 20 states with comprehensive laws; IN/KY/RI from 1 Jan 2026 [80] | Businesses above state thresholds | Very crowded consent/DSAR tools | Yes | Yes | Reject |
| O21 | Spain mandatory digital time recording | Draft Royal Decree not adopted as of early Sep 2026 (secondary sources) [81] | Spanish employers | Dozens of Spanish "fichaje" apps + HR suites [81] | Yes | Yes | Reject |
| O22 | EU F-gas record-keeping | Reg. 2024/573 record-keeping (5 years) [85] | Operators of refrigeration/AC/heat pumps; HVAC contractors | Field-service suites, national logbook tools | Yes | Yes | Reject |
| O23 | Non-regulatory: SMB field service / trades job management | Market pull only | Trades and home-service SMBs | Saturated (Jobber, Housecall Pro, ServiceM8, Tradify, Simpro, ServiceTitan) [82] | Yes | Yes | Reject |
| O24 | Non-regulatory: allied-health clinic practice management | Market pull only | Physio/therapy clinics | Saturated (Cliniko, WriteUpp, Zanda, Pabau, Jane) with AI-scribe add-ons [83] | Yes | Yes | Reject |
| O25 | Non-regulatory: construction COI tracking | Contractual/insurance pull | General contractors | Crowded; AI/OCR extraction is table stakes (BCS, TrustLayer, myCOI, Jones, Billy, COI File) [84] | Weak | Yes | Reject |

---

## 3. Detailed analysis per opportunity

### O1 — EU Cyber Resilience Act: evidence, vulnerability-handling and reporting workspace for small manufacturers

**Problem.** Manufacturers of "products with digital elements" placed on the EU market must, since **11 September 2026**, notify actively exploited vulnerabilities and severe incidents through ENISA's Single Reporting Platform with an early warning within **24 hours**, a notification within **72 hours**, and a final report (14 days after a corrective measure for vulnerabilities; one month for incidents) — VERIFIED [12][17]. This reporting duty applies to **all in-scope products already placed on the market**, not only new ones — VERIFIED (Art. 69(3)) [20][14]. From **11 December 2027** the main obligations apply: cybersecurity risk assessment, due diligence over third-party components, technical documentation, a declared support period (at least five years in general), vulnerability handling, EU declaration of conformity and CE marking — VERIFIED [13][14]. The CRA requires manufacturers to draw up an SBOM covering at least top-level dependencies — VERIFIED (vendor/secondary snippets; Market Validation to re-read Annex I Part II in the OJ text [20]) [24]. SUPPORTED INFERENCE: this creates a continuous, multi-year record-keeping and deadline-management job (inventory of products/versions → components → known vulnerabilities → triage decisions → reports/advisories → support-period end dates) that small manufacturers must evidence.

**Target users.** EU and non-EU SMEs that manufacture connected hardware (IoT, industrial devices), firmware, or software products sold in the EU; importers/distributors have lighter verification duties — VERIFIED [14]. Pure SaaS is generally outside scope unless it is "remote data processing" for a product — VERIFIED (secondary) [14][26]. Whether the best initial segment is hardware/IoT makers or software-product vendors is UNKNOWN.

**Pain severity (evidence).**
- ENISA's first SME CRA survey (194 organisations, 31 countries, fieldwork Feb–Mar 2026): 66% had heard of the CRA; over 70% asked for technical-documentation and secure-development templates; 142 respondents emphasised a need for financial support; micro-companies were weakest on incident response and product lifecycle management — VERIFIED [18]. Secondary analyses of the same survey report SBOM use by only about 35% of respondents — VERIFIED (secondary, snippet) [19].
- Fines for breaches of essential requirements and Art. 13/14 obligations up to €15m or 2.5% of worldwide turnover; micro and small enterprises are not fined specifically for missing the 24-hour early-warning deadline (the duty itself remains) — VERIFIED (secondary, multiple snippets) [21].
- A secondary source quotes the Commission impact assessment as counting ~615,000 manufacturers and an average compliance cost near €47,000 per manufacturer — **not verified against the primary impact assessment; do not rely on it** [25].

**What people do today.** SUPPORTED INFERENCE from sources [18][23][24]: spreadsheets and ad-hoc documents; open-source SBOM tooling (OWASP Dependency-Track is free, Apache-2.0, and matches SBOMs against NVD/OSV/GitHub advisories — VERIFIED (snippet) [23]); consultants and test labs; enterprise product-security platforms for larger firms.

**Existing solutions / competitors (non-exhaustive).** ONEKEY (firmware analysis, SBOM, CRA evidence), Article 14 Ready (browser tool for Art. 14 reports), CVD Portal (Art. 13 disclosure contact + Art. 14 workflow), ConformOps (fixed-price repository readiness pass), pi3g (engineering help for SME IoT makers), Bureau Veritas, DEKRA, SGS, TÜV SÜD (testing/certification) — VERIFIED (vendor list, Aug 2026) [22]; Anchore, Finite State, Cycode, CRA Evidence, Distr, Regulus and others publish CRA SBOM/compliance offers — VERIFIED (V, snippets) [24]; OWASP Dependency-Track (free) [23]. No dominant SME-focused leader was identified — UNKNOWN whether one exists.

**Future need (3–5 years).** PREDICTION: demand rises into 11 Dec 2027 (main obligations) and persists because vulnerability handling runs for the whole support period and security updates must remain available — the CRA summary describes support periods and ongoing handling [14]. Commission guidance with 67 SME examples was published 27 Jul 2026 [16]; the Commission *may* publish a simplified technical-documentation form for micro/small enterprises [15] (UNKNOWN when; could commoditise template-only offerings).

**Barriers.** Buyer is technical and sceptical; free OSS alternatives; trust/credibility needed for a security-adjacent tool; product classification (default / important class I/II / critical) requires legal judgment the software must not pretend to make [14]; vulnerability-data feed licensing terms (NVD, OSV, GitHub Advisory, ENISA EUVD) must be checked (UNKNOWN).

**Risks.** Fast-growing competitor field; price sensitivity (ENISA respondents' emphasis on financial support [18]); liability if the tool implies compliance; possible future simplification by the Commission (UNKNOWN; none found as of 2026-09-26 — the Digital Omnibus changes found concern the AI Act [57][58]).

**AI-free?** Yes — SBOM parsing (CycloneDX/SPDX), deterministic version-range matching against published advisories, reporting clocks, document assembly, audit trail, email alerts. SUPPORTED INFERENCE.

**MVP-feasible?** Yes — a single web app with Postgres, a scheduled advisory-sync job, file upload, e-mail alerts, and payments. Must avoid building the reporting submission itself (the ENISA SRP is the only legal channel [17]); the product can prepare and time-stamp content. SUPPORTED INFERENCE.

---

### O2 — UK holiday-record and holiday-pay assurance for variable-hours employers

**Problem.** Since **6 April 2026**, UK employers must keep records adequate to show compliance with annual-leave and holiday-pay rules — how entitlement and pay are calculated, approved, taken and paid, including carry-over and payments in lieu — and retain them for **six years**; failure is a **criminal offence** with an unlimited fine; no prescribed format and no official definition of "adequate" yet — VERIFIED [27][28]. The Fair Work Agency launched 7 April 2026 with information-gathering and entry powers; notices of underpayment can carry penalties up to 200% of the underpayment; holiday-pay enforcement is expected from 2027 — VERIFIED (secondary) [28][30]. Calculations for irregular-hours and variable-pay workers are error-prone: accrual at 12.07% of hours worked for irregular-hours workers, 52-week average pay reference periods, correct exclusion of zero-pay weeks — VERIFIED (secondary, snippet) [36].

**Target users.** UK employers with hourly, zero-hours, part-year or commission/overtime-paid staff (SUPPORTED INFERENCE: hospitality, social care, retail, cleaning, security, agencies), and payroll bureaus/accountants serving them. Over one million people were on zero-hours contracts in Apr–Jun 2024 (ONS LFS via Commons Library) — VERIFIED (snippet) [35].

**Pain severity (evidence).** Resolution Foundation research reported ~900,000 workers not receiving their holiday entitlement (April 2023) — VERIFIED (S, snippet) [31]; the TUC cites ~£2bn of holiday pay lost per year — VERIFIED (S, snippet; trade-union source with advocacy position) [31]. New criminal record-keeping duty + 6-year look-back + FWA enforcement = SUPPORTED INFERENCE that exposure grows materially in 2027.

**What people do today.** Payroll software (some support 52-week averaging, some reportedly do not — a Xero customer-ideas thread requests it; KeyPay/Employment Hero advertises it) [33]; spreadsheets; HR/absence tools that track leave balances but not necessarily pay-rate correctness [34]. SUPPORTED INFERENCE.

**Existing solutions / competitors.** Absence/leave tools: BrightHR, Breathe, Timetastic, LeaveWizard, edays, Shiftbase, Factorial and others [34]; payroll suites (Sage, Xero, QuickBooks, BrightPay, Staffology, KeyPay) [33]; **paiyroll "holiday pay companion"** — claims automated UK holiday-pay calculation alongside 19+ payroll systems for employers and bureaus, at 15p per payslip (min £30/month) — VERIFIED (V, read) [32]. This is direct evidence that the calculation-add-on concept exists and of a low price anchor.

**Future need.** PREDICTION: awareness and demand rise when FWA holiday-pay enforcement begins (expected 2027) [30]; records accumulate for 6 years, so the need is recurring.

**Barriers.** Crowded HR/payroll ecosystem; SMEs' low willingness to pay; data access depends on payroll exports (formats vary); UK-only market.

**Risks.** Legal complexity (case law on "normal remuneration"; EU-derived vs UK-only leave pots) — a calculation defect creates customer liability; incumbents may close the gap natively; FWA "adequate records" guidance could change requirements (UNKNOWN timing).

**AI-free?** Yes — rules engine over pay-period data, ledger, immutable history, exports. **MVP-feasible?** Yes — CSV import, rules engine, per-worker ledger, audit pack export, email reminders, payments. SUPPORTED INFERENCE.

---

### O3 — Awaab's Law case and statutory-clock management for small social landlords (England)

**Problem.** Social landlords must investigate emergency hazards and make them safe within **24 hours**; investigate significant hazards within **10 working days**; send a written summary within **3 working days** of the investigation; complete safety work within **5 working days**; start supplementary preventative work within 5 working days or as soon as reasonably practicable and within **12 weeks**; and keep clear records of all engagement, investigations, communications and access attempts (needed for the "all reasonable endeavours" defence) — VERIFIED [37]. Phase 1 (damp/mould and emergency hazards) has applied since **27 Oct 2025**; Phase 2 adds excess cold/heat, falls, structural collapse, fire, electrical and domestic hygiene hazards from **30 Nov 2026**; Phase 3 (remaining HHSRS hazards except overcrowding) is planned without a confirmed date — VERIFIED [37]. The duties apply to **all registered providers regardless of size** — VERIFIED [37].

**Target users.** Small private registered providers: in 2025, the 227 large PRPs (1,000+ units) were 17% of PRPs and owned 96% of PRP stock — VERIFIED [38]; SUPPORTED INFERENCE: roughly 1,100 PRPs own fewer than 1,000 homes. Also councils that retain stock (count not verified here). Many small providers are volunteer- or part-time-run (ASSUMPTION).

**Pain severity (evidence).** Statutory working-day clocks with tenant enforceability and ombudsman scrutiny; the Housing Ombudsman publishes damp-and-mould maladministration learning, including cases against a landlord with fewer than 50 homes — VERIFIED (snippet) [41]. Phase 2 widens the hazards covered, so case volumes should rise (SUPPORTED INFERENCE).

**What people do today.** Housing management systems (enterprise, for large providers), spreadsheets and email for small providers (HYPOTHESIS; HazardClock's positioning asserts small providers struggle with manual tracking [39]).

**Existing solutions / competitors.** Weightmans (law-firm-built Awaab's Law compliance tool), Netcall Tenant Hub, Propsys360 (Dynamics 365 case management), Enghouse, Alscient, Plentific — VERIFIED (V, snippets) [40]; **HazardClock** — "automated deadline tracking, countdown alerts, and audit-ready evidence — built for small UK housing providers", currently a waitlist (pre-launch) — VERIFIED (V, read) [39].

**Future need.** PREDICTION: Phase 3 in 2027 extends scope again. The Renters' Rights Act allows Awaab's Law to be applied to the private rented sector, but the Government has only committed to consult and no timetable is set — VERIFIED [71]. If extended, the addressable market would change radically (HYPOTHESIS; not relied on).

**Barriers.** Small buyer universe; public-sector-style procurement for councils; small providers' budgets UNKNOWN; tenant-facing communications and contractor coordination expectations.

**Risks.** A direct small-provider competitor is forming [39]; hazard classification needs professional judgment (software must record decisions, not make them); working-day computation must be correct (bank holidays).

**AI-free?** Yes — case workflow, working-day clocks, templated letters, evidence log, alerts. **MVP-feasible?** Yes. SUPPORTED INFERENCE.

---

### O4 — EU Pay Transparency compliance for SME / lower-mid-market employers

**Problem.** Directive (EU) 2023/970 requires: pay or pay range before interview/contract and a ban on asking pay history (Art. 5); accessible, gender-neutral pay-setting and progression criteria (Art. 6; states may exempt employers with fewer than 50 workers); a worker right to request their pay level and average pay levels by sex for workers doing the same work or work of equal value, answered within two months (Art. 7); gender-pay-gap reporting — 250+ workers annually from 7 Jun 2027, 150–249 every three years from 7 Jun 2027, 100–149 every three years from 7 Jun 2031 (Art. 9); and a joint pay assessment where an unjustified gap of at least 5% in a worker category is not remedied within six months (Art. 10). Transposition deadline 7 Jun 2026 (Art. 34) — VERIFIED [1].

**Status.** Only Italy, Slovakia, Lithuania and Malta had implemented by the deadline per one firm (another describes Malta's implementation as partial [3]); the Netherlands, Sweden, Czechia and Denmark indicated 1 Jan 2027 — VERIFIED (S) [2][3]. As of 26 Sep 2026: France's draft law amended again on 10 Sep 2026 targeting adoption before the 2027 elections; Germany at initial steps (unconfirmed reports of cabinet approval in Oct 2026); Spain published a draft Royal Decree on 3 Aug 2026; Ireland's bill not given priority drafting; Dutch plenary debate scheduled January 2027 — VERIFIED (S) [4]. The Commission refused to postpone or include the directive in an omnibus — VERIFIED (S, snippets) [5][6]. Absent national transposition the Directive's obligations do not directly apply to employers, although courts may interpret existing national equal-pay law consistently with it — VERIFIED (S) [2]. German commentary (30 Apr 2026) expected no law "soon" — VERIFIED (S) [7].

**Target users.** Employers with 100–249 workers (reporting) and all employers in transposed states (Arts. 5–7). SUPPORTED INFERENCE: HR teams in SMEs lack job-architecture data.

**Pain severity.** High in principle (job evaluation for "work of equal value", sex-disaggregated pay statistics, joint assessments, reversal of burden of proof) — SUPPORTED INFERENCE from [1]. Readiness-survey statistics circulating online could not be attributed to a primary source in this session — UNKNOWN.

**Existing solutions.** Figures, Ravio, Personio (SME HRIS add-on), Sysarb, Trusaic, Syndio, PayAnalytics, beqom, Axios Analytics (DACH mid-market), TracefyHR (SME), employsome and others — VERIFIED (V/S) [8][9][10][11]. A buyer's guide notes most tools were built for enterprise buyers, with mid-market between enterprise suites and HRIS add-ons [8].

**Future need.** PREDICTION: strong from 2027 as reporting starts in transposed states and larger states adopt laws; durable (recurring reports, ongoing requests).

**Barriers / risks.** National variation and language; large markets (DE, FR, ES, IE) not yet transposed → building now means building against drafts; crowded field with HRIS incumbents; sensitive pay data; legal risk of wrong categorisation.

**AI-free?** Yes (calculation, categorisation workflows, reports). **MVP-feasible?** Yes for one jurisdiction; multi-country compliance is not an MVP. SUPPORTED INFERENCE.

---

### O5 — US FSMA 204 food traceability for small food businesses (watchlist)

**Problem.** Businesses that manufacture, process, pack or hold foods on the Food Traceability List must keep Key Data Elements for Critical Tracking Events (e.g., receiving, shipping, transformation), maintain a traceability plan, and provide an electronic sortable spreadsheet to FDA within 24 hours on request; restaurants and retail food establishments have modified requirements — VERIFIED [42]. Compliance date moved from 20 Jan 2026; Congress directed FDA not to enforce before **20 Jul 2028** — VERIFIED [42][43].

**Who.** FDA estimated the rule covers more than 323,000 domestic businesses operating more than 484,100 establishments, including about 12,000 farms and 443,000 retail food establishments and restaurants — VERIFIED (S, CRS 29 Apr 2026) [43].

**Pain.** CRS reports low awareness among small/medium suppliers and non-chain restaurants and difficulty obtaining supplier data — VERIFIED [43]. Congress directed FDA to consider additional flexibilities for lot-level tracking — VERIFIED [43].

**Current solutions.** ReposiTrak, iFoodDS, Trustwell (FoodLogiQ), FoodReady (claims $99/month entry), Inecta, Nulogy, Folio3, others — VERIFIED (V, snippets) [44].

**Future need / risks.** PREDICTION: buying concentrates in 2027–2028; rule content may still change (flexibilities) → building now risks rework. Supplier data exchange (GS1/EDI) is a barrier.

**AI-free?** Yes. **MVP-feasible?** Yes (lot/event capture, spreadsheet export). **Verdict:** Watchlist — revisit in 2027 when FDA's response to the Congressional direction is known.

---

### O6 — UK Martyn's Law, standard-tier premises (watchlist / reject now)

**Problem.** Responsible persons for premises where 200–799 people may be present must notify the SIA and have public-protection procedures (evacuation, invacuation, lockdown, communication); enhanced tier (800+) must also implement measures, document them and submit to the SIA. Expected in force spring 2027; SIA portal testing from early 2027 — VERIFIED [45].

**Pain / WTP.** The Home Office impact assessment reportedly estimated ~£330/year per standard-tier premises and ~£5,210/year per enhanced-tier premises (mainly staff time) — VERIFIED (snippet only; primary PDF not machine-readable here) [46]. SUPPORTED INFERENCE: low per-premises budget for standard tier.

**Current solutions.** Standard Tier, Martyn's Law Software (claims from £19/month), Martyn's Law Plan, Policy Pros, Serious Incident Manager, plus security/access-control vendors and free ProtectUK guidance — VERIFIED (V, snippets) [47].

**AI-free / MVP.** Yes / Yes. **Verdict:** Reject now — low budget, many cheap entrants, rules not in force until 2027; enhanced-tier niche may merit a later look.

---

### O7 — EU/UK e-invoicing mandates (reject)
- **Problem / status:** Belgium B2B Peppol from 1 Jan 2026; Poland KSeF Feb/Apr 2026 with micro-enterprises 2027 and no penalties until 2027; France: receive from 1 Sep 2026 (all), issue 1 Sep 2026 (large/mid) and 1 Sep 2027 (SMEs) via approved platforms; Germany: receive since 2025, issue from 2027 if prior-year turnover >€800k, all from 2028; Spain Verifactu postponed to 1 Jan 2027 (corporate taxpayers) / 1 Jul 2027 (others); UK B2B/B2G e-invoicing from 1 Apr 2029 using Peppol — VERIFIED (mostly S/P snippets, multiple sources) [48][49][50][51][52].
- **Who / pain:** all VAT-registered businesses; pain real but largely absorbed by accounting/ERP vendors (SUPPORTED INFERENCE).
- **Current solutions:** French DGFiP list of approved platforms (~137 cited by Pennylane) [49]; national accounting suites; Peppol access points.
- **Barriers:** platform approval/certification (France), Peppol access-point accreditation; clearance integrations (Poland KSeF).
- **AI-free:** Yes. **MVP:** No (certification + integration depth). **Verdict:** Reject — saturated and gated.

### O8 — European Accessibility Act (reject)
- Applies since 28 Jun 2025; all member states transposed; micro-enterprise *service* providers exempt — VERIFIED (S snippets) [53][54]. No fine found in the first year; first French court order (Carrefour, June 2026) and Swedish PTS e-commerce inspections reported — VERIFIED (S snippets) [53].
- Who: e-commerce, banking, e-books, transport ticketing, etc. Current solutions: very crowded (Level Access, Deque, Siteimprove, AudioEye, many checkers). Barriers: automated testing covers only part of WCAG (SUPPORTED INFERENCE); credibility issues around overlays. AI-free: Yes. MVP: partly (scanner feasible, meaningful conformance is service-heavy). **Verdict:** Reject — crowded, enforcement light so far.

### O9 — NIS2 (reject)
- Germany's NIS2 implementation in force 6 Dec 2025; BSI registration due 6 Mar 2026; ~29,500 entities under BSI supervision (secondary estimate) — VERIFIED (S snippets) [55].
- Current solutions: extensive GRC market (ISMS/ISO 27001 platforms, compliance automation). Barriers: buyers expect integrations and audit credibility. AI-free: Yes. MVP: partly. **Verdict:** Reject — saturated; deadline-driven registration already passed in DE.

### O10 — DORA register of information (reject)
- Annual RoI submissions in xBRL-CSV; e.g., CSSF window 11 Feb–31 Mar 2026 — VERIFIED (P snippet) [56]. Buyers are regulated financial entities with enterprise procurement; GRC suites and specialist RoI tools exist [56]. AI-free: Yes. MVP: feasible technically, but sales cycle and trust barriers are high. **Verdict:** Reject.

### O11 — EU AI Act deployer obligations (reject)
- Digital Omnibus on AI published in OJ 24 Jul 2026, in force 27 Jul 2026; Annex III high-risk obligations deferred to 2 Dec 2027, Annex I to 2 Aug 2028; Art. 50 transparency applies from Aug 2026 with watermarking grace to 2 Dec 2026; Art. 4 AI-literacy changed from ensuring a "sufficient level" to taking measures to support literacy — VERIFIED (S; read [57][58], snippets [59]). A secondary source cites the act as Regulation (EU) 2026/1744 — number not verified.
- Current solutions: numerous AI-governance/AI-Act tools for SMEs (Legalithm, TrailBit, Annexa, AktAI, ComplyOne and others) [60]. AI-free: yes (an inventory/register need not use AI). **Verdict:** Reject — obligations deferred/softened, crowded.

### O12 — CSRD / voluntary SME standard (reject)
- Omnibus I published in OJ 26 Feb 2026; CSRD scope raised to >1,000 employees and >€450m turnover; value-chain cap shields companies <1,000 employees from requests beyond the voluntary standard; Commission adopted the voluntary-standard delegated act on 3 Jul 2026 (subject to scrutiny) — VERIFIED (S snippets, multiple) [61][62].
- Who: SME suppliers asked for ESG data by customers/banks. Current solutions: crowded (osapiens, Dcycle, Sunhat, others) [63]. AI-free: Yes. MVP: Yes. **Verdict:** Reject — voluntary, scope shrunk, crowded.

### O13 — Whistleblowing Directive channels (reject)
- Internal reporting channels mandatory for 50+ workers; many vendors, published prices from ~€19/month to ~€99/month; enterprise vendors quote-only — VERIFIED (V/S snippets) [64]. AI-free: Yes. MVP: Yes. **Verdict:** Reject — commoditised.

### O14 — EUDR (reject)
- Amended by Regulation (EU) 2025/2650: applies 30 Dec 2026 (large/medium) and 30 Jun 2027 (micro/small); May 2026 simplification package confirmed no further postponement — VERIFIED (P/S snippets) [65][66]. Requires geolocation/polygon data and supply-chain declarations; crowded (osapiens, Coolset and many others); regulation has changed repeatedly (SUPPORTED INFERENCE: volatility risk). AI-free: Yes. MVP: partly. **Verdict:** Reject.

### O15 — PPWR / multi-country packaging EPR (reject)
- PPWR (Reg. (EU) 2025/40) applies from 12 Aug 2026; no single EU registry — each member state runs its own EPR register; non-EU producers need an authorised representative — VERIFIED (S/P snippets) [67][68]. Environmental-omnibus proposal to suspend the authorised-representative obligation for EU producers; a Council decision not to proceed was reported — **UNVERIFIED (single snippet)** [67].
- Current solutions: Gramta, Repax, Lappa, EPR Insights (Shopify app, from €24.90 per country claimed), compliance schemes (e.g., Der Grüne Punkt/Verpackgo) [68]. Barrier: deep per-country scheme knowledge. **Verdict:** Reject — crowded and country-fragmented.

### O16 — EU Short-Term Rental Regulation (reject)
- Reg. (EU) 2024/1028 applies from 20 May 2026; registration numbers where states require registration; platforms verify/display numbers and report data via national single digital entry points — VERIFIED (P/S snippets) [69][70]. Obligations fall mainly on platforms and authorities; hosts rely on channel managers and guest-registration tools (Chekin and others) [70]. **Verdict:** Reject.

### O17 — UK landlord compliance: Renters' Rights Act, PRS database, MTD ITSA (reject)
- Tenancy reforms from 1 May 2026; PRS database registration rolling out regionally from 15 Dec 2026 (starting West Midlands); civil penalties up to £7,000 and up to £40,000 or prosecution for serious/repeat breaches; ombudsman membership expected 2028; Decent Homes Standard for PRS in 2035/2037 — VERIFIED [71][72][73]. MTD for Income Tax from 6 Apr 2026 for qualifying income >£50,000, falling to £30,000 (2027) and £20,000 (2028) — VERIFIED (P snippet) [75]. England has an estimated 2.3–2.8m private landlords depending on source — VERIFIED (S snippet) [76].
- Current solutions: saturated, including free tiers and £8.99–£29.99/month tools (LetDeck, Dwelyx, LLCR, ComplianceBot, CalmLet, LetCompliance, LandlordOS, Landlord Studio, Hammock, Landlord Vision, August) [74]. AI-free/MVP: Yes/Yes. **Verdict:** Reject — saturated, low price points.

### O18 — UK tipping (reject)
- Tips Act in force since Oct 2024 (records, fair allocation); ERA 2025 adds consultation on tipping policies with 3-yearly review, expected by end-2026; draft revised code consultation closing 29 Sep 2026 — VERIFIED (S snippets) [77]. Current solutions: TiPJAR, JustTip, IRIS Tronc, Grateful and others [78]. **Verdict:** Reject — niche with established players.

### O19 — US state pay-transparency job postings (reject)
- NJ (1 Jun 2025), VT (1 Jul 2025), MA (29 Oct 2025), DE (26 Sep 2027) among others; city ordinances in Ohio — VERIFIED (S snippets) [79]. Handled inside ATS/HRIS/payroll suites (SUPPORTED INFERENCE from vendor guides [79]). **Verdict:** Reject.

### O20 — US state privacy laws (reject)
- 20 states with comprehensive privacy laws; Indiana, Kentucky and Rhode Island effective 1 Jan 2026 — VERIFIED (S snippets) [80]. Consent/DSAR tooling market is crowded (SUPPORTED INFERENCE). **Verdict:** Reject.

### O21 — Spain digital working-time recording (reject)
- A Royal Decree mandating fully digital time records had not passed the Council of Ministers as of early Sep 2026 and received a critical Council of State opinion in Mar 2026, per secondary (vendor) sources — VERIFIED (V/S snippets, low grade) [81]. Dozens of Spanish time-clock apps exist [81]. **Verdict:** Reject — not in force, crowded.

### O22 — EU F-gas record-keeping (reject)
- Reg. (EU) 2024/573 requires operators to keep records (quantities, leak checks, interventions) for five years — VERIFIED (S snippets) [85]. Not a new obligation (predecessor regimes since 2006/2014 — SUPPORTED INFERENCE); served by HVAC field-service software and national logbook tools. **Verdict:** Reject.

### O23 — Non-regulatory: SMB field service / trades (reject)
- Saturated: Jobber, Housecall Pro, ServiceM8, Tradify, Simpro, ServiceTitan, Workiz, Kickserv; entry pricing ~$29–60/month, mid-market $150–350/month per vendor guides — VERIFIED (V/S snippets) [82]. **Verdict:** Reject — no regulatory forcing function, dominant incumbents.

### O24 — Non-regulatory: allied-health clinic practice management (reject)
- Saturated: WriteUpp, Cliniko, Zanda, Pabau, Jane, TM3; £15–29 per practitioner/month; incumbents are adding AI-scribe add-ons — VERIFIED (V/S snippets) [83]. **Verdict:** Reject — saturated; AI-free positioning a weakness against AI documentation features.

### O25 — Non-regulatory: construction COI tracking (reject)
- Crowded (BCS, TrustLayer, myCOI, Jones, Billy, Certificial, COI File, PaperBoss); competitors market AI/OCR extraction of certificates as core value — VERIFIED (V snippets) [84]. **Verdict:** Reject — AI-free filter is a competitive handicap here; crowded.

---

## 4. Rejected opportunities and reasons

| # | Area | Decisive reason(s) | What would change the verdict |
|---|---|---|---|
| O6 | Martyn's Law | Not in force until spring 2027; low per-premises budget per IA (snippet); many cheap entrants | Evidence of enhanced-tier buyers underserved and willing to pay |
| O7 | E-invoicing | Saturated; certification/access-point gating fails MVP filter | A narrow pre-/post-processing niche with no certification need (not found) |
| O8 | EAA | Crowded; enforcement light; automated checks only partially meaningful | Material fines creating demand for evidence management specifically |
| O9 | NIS2 | Saturated GRC market; registration deadline passed (DE) | — |
| O10 | DORA RoI | Enterprise/regulated buyers; specialist incumbents | — |
| O11 | AI Act | High-risk duties deferred to Dec 2027/Aug 2028; Art. 4 softened; crowded | — |
| O12 | CSRD/VSME | Scope reduced; standard voluntary; crowded | Banks mandating VS-format data from SME borrowers at scale (UNKNOWN) |
| O13 | Whistleblowing | Commoditised (from ~€19/month) | — |
| O14 | EUDR | Volatile rules, crowded, geo-data heavy | — |
| O15 | PPWR/EPR | Crowded new entrants; deep per-country knowledge | — |
| O16 | STR Regulation | Obligations mainly on platforms/authorities; channel managers cover hosts | — |
| O17 | UK landlord compliance | Saturated with free/cheap tools | — |
| O18 | UK tipping | Niche; established providers | — |
| O19 | US pay transparency | Absorbed into ATS/HRIS | — |
| O20 | US privacy | Crowded | — |
| O21 | Spain time recording | Not enacted; crowded | Decree adopted with requirements existing apps cannot meet (UNKNOWN) |
| O22 | F-gas | Not new; served by incumbents | — |
| O23 | Field service | Saturated, no forcing function | — |
| O24 | Clinic PM | Saturated; AI features expected | — |
| O25 | COI tracking | Crowded; AI extraction is table stakes | — |
| O5 | FSMA 204 | (Watchlist, not rejected) 2028 enforcement and possible rule changes → premature | FDA's response on flexibilities (2027) |

---

## 5. Recommended candidates for validation (ranked)

Ranking basis (qualitative, SUPPORTED INFERENCE): (a) obligation certainty and timing; (b) consequence of inaction; (c) evidence that the target segment is underserved; (d) buyer reachability / willingness-to-pay signals; (e) fit with AI-free, small-team MVP; (f) legal-risk of the product being wrong; (g) durability to 2029–2031.

### Rank 1 — O1: CRA evidence, vulnerability-handling and reporting workspace for small manufacturers
**Why first.** An EU *regulation* (no transposition uncertainty) whose reporting duty is already live and covers the installed base [12][20], with main obligations 15 months away [13] and multi-year recurring duties [14]; the regulator's own SME survey documents low readiness and explicit demand for templates [18]; the work is inherently record-keeping, version matching and deadline tracking — a strong fit for deterministic software. No dominant SME-focused player was identified, though the field is filling quickly [22][24].
**Key questions for Market Validation (Agent 2).**
1. Which segment feels the most pain and has budget: connected-hardware/IoT SMEs, embedded/firmware makers, or packaged-software vendors? Which member states first?
2. What do they use today (Dependency-Track, spreadsheets, consultants, enterprise platforms), and where does it break?
3. Which job is most valuable and least served: SBOM-based vulnerability monitoring, triage evidence, Art. 14 reporting preparation/clocks, technical-documentation assembly, support-period/end-of-support management, or customer-facing security advisories?
4. Price anchors and willingness to pay given the reported need for financial support [18]; competitor pricing (ConformOps fixed price, Article 14 Ready, CVD Portal, ONEKEY) [22].
5. Trust prerequisites a small vendor must meet (EU hosting, security posture, references) and whether an AI-free product is disadvantaged against AI-marketed competitors.
6. Licensing and reliability of vulnerability data sources (NVD, OSV, GitHub Advisory Database, ENISA EUVD) — UNKNOWN.
7. Timing and content of any Commission simplified technical-documentation form for micro/small enterprises [15].

### Rank 2 — O2: UK holiday-record and holiday-pay assurance for variable-hours employers
**Why second.** The duty is in force with criminal liability and a new enforcement agency [27][28][30]; documented, widespread underpayment [31]; deterministic calculation and ledger work. Ranked below O1 because the ecosystem is crowded, a calculation add-on already exists at a low price point (paiyroll) [32], and payroll incumbents may close the gap [33].
**Key questions.**
1. Who buys: the employer, the payroll bureau/accountant, or both? Size of the bureau channel (UNKNOWN).
2. Which payroll systems in 2026 still lack correct 52-week averaging, irregular-hours accrual and a six-year evidence trail?
3. What will the FWA consider "adequate" records, and when will guidance appear?
4. Willingness to pay relative to 15p/payslip [32]; value of an "audit pack" vs. calculation alone.
5. Integration minimum: which payroll export formats cover most target customers?
6. Appetite for the liability of a calculation engine; need for legal review of rules.

### Rank 3 — O3: Awaab's Law case and statutory-clock management for small social landlords
**Why third.** In force, applies to every registered provider regardless of size, with precise statutory clocks and an evidence burden [37]; scope expands on 30 Nov 2026 and again in 2027; large providers already have enterprise systems while ~1,100 small providers are plausibly underserved [38]. Ranked below O2 because the buyer universe is small, budgets/procurement are unknown, and a competitor (HazardClock) targets exactly this niche [39].
**Key questions.**
1. How many small providers manage repairs in-house vs. via managing agents or larger partners?
2. How do they track Awaab's Law cases today, and what failed in Phase 1?
3. Budget, decision-maker and procurement route (board approval? framework?) for small RPs and stock-holding councils.
4. Required integrations (contractor job systems, tenant contact channels, HMS exports).
5. Competitor traction and pricing (HazardClock launch, Weightmans tool).
6. Any Government timetable for applying Awaab's Law to the private rented sector [71].

### Rank 4 (conditional) — O4: EU Pay Transparency compliance for SME / lower-mid-market employers in already-transposed states
**Why fourth.** Severe, durable HR pain and a firm EU-level framework [1], but national laws are missing in the largest markets as of 2026-09-26 [4], and the vendor field is crowded including HRIS incumbents [8]. Recommended only if validation finds an underserved, transposed jurisdiction with enough employers in the 100–249 band.
**Key questions.**
1. Which transposed (or soon-transposed) jurisdiction offers an underserved SME segment and a language the team can support?
2. Exact national reporting formats, thresholds and deadlines (e.g., Italy's ministerial decrees reported as expected Sep 2026 [4]).
3. Do SMEs accept a deterministic job-evaluation (points-factor) method for "work of equal value", and will equality bodies/works councils accept its outputs?
4. How far do Personio/Figures/other SME tools already cover Arts. 5–10 in that jurisdiction; price anchors.

### Watchlist
- **O5 FSMA 204** — revisit in 2027 once FDA acts on the Congressional direction to consider flexibilities [43].
- **O6 Martyn's Law (enhanced tier)** — revisit after SIA guidance (autumn 2026) and commencement (spring 2027) [45].
- **UK e-invoicing 2029** — only if a non-certified niche emerges [52].

---

## 6. Key assumptions & unknowns

| ID | Statement | Label | Why it matters / how to test |
|---|---|---|---|
| A-01 | Small manufacturers will pay for a CRA workspace rather than rely on free OSS + templates | HYPOTHESIS | Core to O1; test with pricing interviews; ENISA reports financial-support need [18] |
| A-02 | No dominant SME-focused CRA vendor exists as of 2026-09-26 | UNKNOWN | Competitive gap for O1; Agent 2 to map traction |
| A-03 | Vulnerability feeds (NVD, OSV, GHSA, EUVD) can be used commercially on acceptable terms | UNKNOWN | O1 feasibility; check licences |
| A-04 | ~615,000 manufacturers in CRA scope; ~€47k average compliance cost | UNKNOWN (secondary only, not verified) [25] | Do not use until verified in the primary impact assessment |
| A-05 | Many UK SME payroll setups calculate variable-pay holiday incorrectly | SUPPORTED INFERENCE [31][33][36] | O2 demand; test with bureaus |
| A-06 | Payroll bureaus are an efficient channel for O2 | HYPOTHESIS | Channel economics |
| A-07 | FWA holiday-pay enforcement begins in 2027 | PREDICTION (secondary sources) [28][30] | Timing of O2 demand |
| A-08 | ~1,100 small PRPs exist (<1,000 homes) | SUPPORTED INFERENCE from 227 large = 17% [38] | O3 market count; confirm with RSH data tables |
| A-09 | Small social landlords track Awaab's Law cases manually | HYPOTHESIS [39] | O3 problem validation |
| A-10 | Awaab's Law will be extended to the private rented sector | UNKNOWN (consultation only) [71] | Would transform O3's market; not relied on |
| A-11 | Germany/France/Spain transpose the Pay Transparency Directive in 2026–2027 | PREDICTION [4] | O4 timing |
| A-12 | Commission will not postpone the Pay Transparency Directive | VERIFIED as of statements found [5][6]; future change UNKNOWN | O4 |
| A-13 | CRA reporting applies to products placed on the market before 11 Dec 2027 | VERIFIED [20][14] | O1 urgency |
| A-14 | Micro/small enterprises are not fined for missing the 24h early warning | VERIFIED (secondary, multiple) [21] — re-read Art. 64(10) in the OJ text | Reduces O1 urgency for smallest firms |
| A-15 | Martyn's Law IA per-premises cost estimates (£330 / £5,210) | VERIFIED (snippet only) [46] | O6 WTP; primary PDF unread |
| A-16 | PPWR authorised-representative suspension not pursued by Council (24 Jun 2026) | UNKNOWN (single snippet) [67] | O15 only |
| A-17 | Claims resting only on snippet-level sources should be re-read in the original before external use: [5], [6], [9], [10], [11] (TracefyHR part), [17], [19], [21], [23]–[26], [29]–[31], [33]–[36], [40], [41], [44], [46]–[53], [55], [56], [59]–[70], [73]–[85]; [54] was not re-read at all | Process note | WebFetch/search summaries may paraphrase or misdate |

---

## 7. Sources

Access date for all sources: 2026-09-26. "Read" = page fetched and read in this session (via a summarising fetch tool); "Snippet" = seen only as a search-result summary. Grade: P = primary/official, S = secondary, V = vendor.

1. Directive (EU) 2023/970 (Pay Transparency), EUR-Lex, OJ 17 May 2023 — https://eur-lex.europa.eu/eli/dir/2023/970/oj/eng — P, Read
2. Morgan Lewis, "EU Pay Transparency Directive: The Deadline for Transposition Has Passed—What Now?", 8 Jun 2026 — https://www.morganlewis.com/pubs/2026/06/eu-pay-transparency-directive-the-deadline-for-transposition-has-passed-what-now — S, Read
3. Littler, "In the Eleventh Hour: Implementation Status of the EU Pay Transparency Directive", 6 May 2026 — https://www.littler.com/news-analysis/asap/eleventh-hour-implementation-status-eu-pay-transparency-directive — S, Read
4. Ius Laboris, "EU Pay Transparency Directive: which countries have transposed", updated 26 Sep 2026 — https://iuslaboris.com/insights/eu-pay-transparency-directive-which-countries-have-transposed/ — S, Read
5. Ius Laboris, "The EU Commission does not intend to delay the Pay Transparency Directive" (2026) — https://iuslaboris.com/insights/eu-pay-transparency-no-delay/ ; Ogletree (2026) — https://ogletree.com/insights-resources/blog-posts/european-commission-confirms-the-eu-pay-transparency-directive-implementation-deadline-remains-7-june-2026/ — S, Snippet
6. Lewis Silkin, "BusinessEurope calls for a 'Stop the clock' on the Pay Transparency Directive", 10 Mar 2026 — https://www.lewissilkin.com/insights/2026/03/10/businesseurope-calls-for-a-stop-the-clock-on-the-pay-transparency-directive — S, Snippet
7. Haufe, "Entgelttransparenzgesetz: Verschiebung mit Ansage", 30 Apr 2026 — https://www.haufe.de/personal/personalszene/entgelttransparenzgesetz-verschiebung-mit-ansage_74_684262.html — S, Read
8. Axios Analytics, "Best EU Pay Transparency Software 2026: A Buyer's Guide", Jun 2026 — https://axiosanalytics.com/en/resources/best-eu-pay-transparency-software-2026 — V, Read
9. Trusaic, "EU Pay Transparency Directive Software Buyer's Guide 2026" — https://trusaic.com/resources/best-eu-pay-transparency-directive-software/ — V, Snippet
10. Figures, pay-equity solution page — https://figures.hr/solutions/pay-equity — V, Snippet
11. TracefyHR, "EU Pay Transparency Directive 2026: SME Guide" — https://tracefyhr.com/blog/eu-pay-transparency-directive-2026-guide ; Sysarb buyer's guide, updated 12 Nov 2025 — https://resources.sysarb.com/buyers-guides/what%E2%80%99s-the-best-equal-pay-software-in-the-eu — V, Snippet/Read
12. European Commission, "Cyber Resilience Act – Reporting obligations", updated 11 Sep 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-reporting — P, Read
13. European Commission, "Cyber Resilience Act" policy page, updated 7 Sep 2026 — https://digital-strategy.ec.europa.eu/en/policies/cyber-resilience-act — P, Read
14. European Commission, "The Cyber Resilience Act – Summary of the legislative text", 3 Dec 2025 — https://digital-strategy.ec.europa.eu/en/policies/cra-summary — P, Read
15. European Commission, "Cyber Resilience Act – MSMEs", updated 31 Jul 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-msmes — P, Read
16. European Commission, "Commission publishes new guidance to support timely Cyber Resilience Act implementation", 27 Jul 2026 — https://digital-strategy.ec.europa.eu/en/library/commission-publishes-new-guidance-support-timely-cyber-resilience-act-implementation — P, Read
17. ENISA, "The CRA Single Reporting Platform is launched" (Sep 2026) — https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched ; Industrial Cyber (Sep 2026) — https://industrialcyber.co/regulation-standards-and-compliance/enisa-launches-single-reporting-platform-as-eu-cyber-resilience-act-vulnerability-reporting-obligations-take-effect/ — P/S, Snippet
18. ENISA, "Where do SMEs stand in preparing for the Cyber Resilience Act?", 24 Jun 2026 — https://www.enisa.europa.eu/news/where-do-smes-stand-in-preparing-for-the-cyber-resilience-act (report: https://www.enisa.europa.eu/publications/sme-cra-survey-report) — P, Read (news page)
19. cyberresilienceact.eu, "ENISA's First SME Survey Found High CRA Awareness but Low Readiness" (Jun 2026) — https://www.cyberresilienceact.eu/news/enisa-sme-cra-survey-high-awareness-low-readiness.html ; Cloud Security Alliance research note, 15 Jul 2026 — https://labs.cloudsecurityalliance.org/research/csa-research-note-enisa-cra-sme-maturity-20260715-csa-styled/ — S, Snippet
20. CRA Article 69 (transitional provisions), text reproduced at european-cyber-resilience-act.com — https://www.european-cyber-resilience-act.com/Cyber_Resilience_Act_Article_69.html — P (reproduction), Read. Official text: Regulation (EU) 2024/2847, OJ 20 Nov 2024, EUR-Lex — https://eur-lex.europa.eu/eli/reg/2024/2847/oj — P, identifier confirmed via search snippet, text not re-read
21. CRA Article 64 fines: Venvera — https://venvera.com/learn/cra/fines-and-penalties ; StreamLex — https://streamlex.eu/articles/cra-en-art-64/ ; Faegre Drinker, Sep 2026 — https://www.faegredrinker.com/en/insights/publications/2026/9/september-2026-eu-compliance-deadlines-for-connected-product-manufacturers — S/V, Snippet
22. Cyber Vendor Guide, "Cyber Resilience Act Compliance Companies (2026)", Aug 2026 — https://www.cybervendorguide.com/guides/cra-compliance — S, Read
23. OWASP Dependency-Track — https://dependencytrack.org/ ; https://owasp.org/projects/dependency-track — P (project), Snippet
24. CRA vendor pages: ONEKEY — https://www.onekey.com/resource/cyber-resilience-act-sbom ; Anchore — https://anchore.com/sbom/eu-cra/ ; Finite State — https://finitestate.io/blog/eu-cra-sbom-technical-documentation-guide ; Cycode — https://cycode.com/blog/cyber-resilience-act/ ; CRA Evidence — https://craevidence.com/cra-compliance/support-period-basics ; Distr — https://distr.sh/cyber-resilience-act/monitoring-and-reporting/ ; Regulus — https://goregulus.com/cra-basics/owasp-dependency-check/ — V, Snippet
25. CircleID, "EU Cyber Resilience Act Costs and Economic Impact" — https://circleid.com/posts/eu-cyber-resilience-act-costs-and-economic-impact — S, Snippet (not verified against primary)
26. DLA Piper, "Cyber Resilience Act: the fine line between SaaS and digital products", Feb 2026 — https://www.dlapiper.com/en/insights/publications/2026/02/cyber-resilience-act-the-fine-line-between-saas-and-digital-products — S, Snippet
27. Baker McKenzie, "United Kingdom: New Record-Keeping Obligations for Annual Leave", 15 Apr 2026 — https://www.bakermckenzie.com/en/insight/publications/2026/04/united-kingdom-new-record-keeping-obligations-for-annual-leave — S, Read
28. DLA Piper, "Employment Rights Act: Preparing for change: Duty to keep holiday records…", 9 Apr 2026 — https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/employment-rights-act-preparing-for-change-duty-to-keep-holiday-records-means-new-legal-risks-for-employers — S, Read
29. GOV.UK, "Implementing the Plan to Make Work Pay and Employment Rights Act" — https://www.gov.uk/government/publications/implementing-the-plan-to-make-work-pay-and-employment-rights-act ; Lewis Silkin ERA timeline, 23 Jul 2026 — https://www.lewissilkin.com/en/insights/2026/07/23/employment-rights-act-timeline — P/S, Snippet
30. Milsted Langdon, "Fair Work Agency set to strengthen holiday pay enforcement from 2027" — https://www.milstedlangdon.co.uk/fair-work-agency-set-to-strengthen-holiday-pay-enforcement-from-2027/ ; Personnel Today, "Consultation on holiday pay compliance launched" — https://www.personneltoday.com/hr/consultation-on-holiday-pay-compliance-launched/ — S, Snippet
31. Bloomberg, "UK Employers Skimp on Holiday and Pay for 1 Million, Report Says" (Resolution Foundation), 25 Apr 2023 — https://www.bloomberg.com/news/articles/2023-04-25/uk-employers-skimp-on-holiday-and-pay-for-1-million-report-says ; TUC, "Workers 'cheated' out of £2bn of holiday pay" — https://www.tuc.org.uk/news/workers-cheated-out-ps2bn-holiday-pay-last-year-under-tories — S, Snippet
32. paiyroll, "Automated holiday pay for existing payroll software" — https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ — V, Read
33. Xero Product Ideas, "UK Payroll: run a report to calculate holiday pay based on a 52 week average" — https://productideas.xero.com/forums/939198-for-small-businesses/suggestions/45241594-uk-payroll-reporting-run-a-report-to-calculate ; KeyPay, "52 week averaging for holiday pay" — https://www.keypay.co.uk/features/52-week-averaging — V, Snippet
34. LeaveWizard, "Best Employee Holiday Tracker: 10 Tools Compared" — https://www.leavewizard.com/best-employee-holiday-tracker/ ; edays, "Best Absence Management Software UK 2026" — https://www.e-days.com/news/top-8-best-absence-management-software-providers ; Shiftbase — https://www.shiftbase.com/blog/best-absence-management-software-uk — V, Snippet
35. House of Commons Library, "Zero-hours contracts" (SN06553) — https://commonslibrary.parliament.uk/research-briefings/sn06553/ — S, Snippet
36. DavidsonMorris, "Irregular Hours Holiday Pay UK 2026" — https://www.davidsonmorris.com/irregular-hours-holiday-pay/ — S, Snippet
37. GOV.UK, "Awaab's Law Phase 2: Guidance for social landlords", updated 31 Jul 2026 — https://www.gov.uk/government/publications/awaabs-law-phase-2-guidance-for-social-housing-landlords/awaabs-law-phase-2-guidance-for-social-landlords — P, Read
38. Regulator of Social Housing, "Private registered providers stock and rents in England – Summary (key facts)", 2024–25, published 31 Oct 2025 — https://www.gov.uk/government/statistics/private-registered-provider-social-housing-stock-and-rents-in-england-2024-to-2025/private-registered-providers-stock-and-rents-in-england-summary-key-facts — P, Read
39. HazardClock, compliance checklist / product page — https://hazardclock.co.uk/tools/compliance-checklist/ — V, Read
40. Weightmans Awaab's Law Compliance Tool — https://www.weightmans.com/products/awaab-s-law-compliance-tool/ ; Netcall — https://www.netcall.com/complying-with-awaabs-law-what-good-looks-like/ ; Propsys360 — https://neotechnologysolutions.com/propsys360/case-management-dynamics-365/awaabs-law-practical-compliance-for-damp-mould/ ; Plentific — https://www.plentific.com/resource-center/blog/awaabs-law-phase-2-explained-the-new-hhsrs-hazards-and-statutory-deadlines-for-2026/ — V, Snippet
41. Housing Ombudsman, damp and mould learning (Feb 2025) — https://www.housing-ombudsman.org.uk/2025/02/25/latest-learning-from-complaints/ ; learning from severe maladministration (Aug 2025) — https://www.housing-ombudsman.org.uk/reports/learning-from-severe-maladministration-reports/august-2025/ — P, Snippet
42. FDA, "FSMA Final Rule on Requirements for Additional Traceability Records for Certain Foods", updated 24 Jul 2026 — https://www.fda.gov/food/food-safety-modernization-act-fsma/fsma-final-rule-requirements-additional-traceability-records-certain-foods — P, Read
43. Congressional Research Service, "The Food and Drug Administration's Food Traceability Rule: Overview and Issues for Congress" (R48925), 29 Apr 2026 — https://www.everycrsreport.com/reports/R48925.html (also https://www.congress.gov/crs-product/R48925) — S (official research service), Read
44. FSMA 204 vendors: ReposiTrak — https://repositrak.com/fda-food-traceability/food-traceability/ ; iFoodDS — https://www.ifoodds.com/software-solutions/food-traceability-software/ ; Flux IoT list — https://flux-iot.com/blog/best-food-traceability-software-fsma-204 ; Inecta — https://www.inecta.com/blog/fsma-204-compliance-guide — V, Snippet
45. GOV.UK / SIA, "Understanding Martyn's Law and the SIA's role as regulator", 17 Jul 2026 — https://www.gov.uk/guidance/understanding-martyns-law-and-the-sias-role-as-regulator — P, Read
46. Home Office, Terrorism (Protection of Premises) Bill impact assessment (PDF) — https://assets.publishing.service.gov.uk/media/66e30684e47cfc6de429d612/TPOP_Signed_IA.pdf — P, fetch attempted, not machine-readable; cost figures from snippet (imabi) — https://www.imabi.com/blog/martyns-law-home-office-myth-buster-guidance
47. Martyn's Law tools: Standard Tier — https://www.standardtier.co.uk/about ; Martyn's Law Software — https://martynslawsoftware.co.uk/ ; Martyn's Law Plan — https://martynslawplan.co.uk/guides/enhanced-tier-explained/ ; Policy Pros — https://www.policypros.co.uk/martyns-law-2027-compliance-guide/ — V, Snippet
48. Finbite, "E-Invoicing Mandates in Europe 2026: The Full Table" — https://finbite.eu/en/e-invoicing-mandates-europe-2026/ ; SPS Commerce — https://www.spscommerce.com/community/articles/e-invoicing-mandates-in-europe-the-2026-business-guide — V/S, Snippet
49. impots.gouv.fr, "Facturation électronique et plateformes agréées" — https://www.impots.gouv.fr/facturation-electronique-et-plateformes-agreees ; Pennylane list of approved platforms — https://www.pennylane.com/fr/fiches-pratiques/facture-electronique/liste-des-pdp — P/V, Snippet
50. Bundesfinanzministerium, FAQ E-Rechnung — https://www.bundesfinanzministerium.de/Content/DE/FAQ/e-rechnung.html ; e-rechnungs-studio (transition rules) — https://e-rechnungs-studio.de/de/e-rechnung-uebergangsregeln-2027-800000-2028 — P/V, Snippet
51. Noticias Jurídicas, "Nueva prórroga: Verifactu no será obligatorio hasta 2027" (RDL 15/2025, BOE 3 Dec 2025) — https://noticias.juridicas.com/actualidad/noticias/20735-nueva-prorroga:-verifactu-no-sera-obligatorio-hasta-2027-para-sociedades-y-otros-contribuyentes/ — S, Snippet
52. ICAS, "Autumn Budget 2025: E-invoicing will go ahead from 2029" — https://www.icas.com/news-insights-events/news/tax/autumn-budget-2025-e-invoicing-will-go-ahead-from-2029 ; vatcalc — https://www.vatcalc.com/united-kingdom/uk-2029-mandatory-b2b-e-invoicing/ — S, Snippet
53. Deque, "Early signs of EAA enforcement across Europe" — https://www.deque.com/blog/early-signs-of-eaa-enforcement-across-europe/ ; auditsu, "EAA at One Year" — https://auditsu.com/resources/eaa-enforcement-2026 — V/S, Snippet
54. Directive (EU) 2019/882 (European Accessibility Act), EUR-Lex — https://eur-lex.europa.eu/eli/dir/2019/882/oj — P, not re-read in this session
55. DLA Piper, "NIS 2 Directive Transposed in Germany – Time to Register with the BSI", Feb 2026 — https://www.dlapiper.com/en/insights/publications/2026/02/nis-2-directive-transposed-in-germany ; Privacy World, Dec 2025 — https://www.privacyworld.blog/2025/12/germany-implements-nis2-registration-portal-will-open-on-january-6-2026/ — S, Snippet
56. CSSF, "DORA – Submission timeframe for register of information – eDesk Portal open as of 11 February 2026" — https://www.cssf.lu/en/2026/02/dora-submission-timeframe-for-register-of-information-edesk-portal-open-as-of-11-february-2026/ — P, Snippet
57. Gibson Dunn, "EU AI Act Omnibus Agreement — Postponed High-Risk Deadlines and Other Key Changes", 27 May 2026 — https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/ — S, Read
58. Usercentrics, "EU AI Act Deal: Digital Omnibus Now in Force" (2026) — https://usercentrics.com/knowledge-hub/eu-ai-act-high-risk-delay-article-50-transparency-consent/ — V/S, Read
59. lawandtechnology.eu, "AI literacy: the Digital Omnibus rewrites Article 4" — https://lawandtechnology.eu/en/ai-literacy-digital-omnibus-article-4-ai-act/ ; Spicy Advisory (cites Regulation (EU) 2026/1744) — https://spicyadvisory.com/blog/digital-omnibus-ai-act-2026-what-changed — S, Snippet
60. Themio, "Best AI Act Compliance Tools for SMEs in 2026" — https://www.themio.ai/en/blog/best-ai-act-compliance-tools-sme-2026 ; Legalithm comparison — https://www.legalithm.com/en/blog/eu-ai-act-compliance-software-tools-compared-2026 — V, Snippet
61. Regulation Tomorrow (Norton Rose Fulbright), Omnibus I adoption, Feb 2026 — https://www.regulationtomorrow.com/2026/02/omnibus-i-csrd-and-cs3d-simplification-council-of-european-union-adopts-final-text-t-simplify-sustainability-reporting-and-due-diligence-requirements/ ; DLA Piper, "EU Council approves Omnibus I Directive" — https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/eu-council-approves-omnibus-i-directive — S, Snippet
62. IAS Plus, "European Commission publishes delegated act on voluntary standard for sustainability reporting", Jul 2026 — https://www.iasplus.com/en/news/2026/07/ec-voluntary-standard ; European Commission delegated act PDF — https://ec.europa.eu/finance/docs/level-2-measures/csrd-delegated-act-2026-5011_en.pdf — S/P, Snippet
63. VSME tools: osapiens — https://osapiens.com/en/regulations/vsme-voluntary-sustainability-reporting-standard-for-smes ; Dcycle — https://dcycle.io/blog/vsme-voluntary-standard-smes-2026/ ; Sunhat — https://www.getsunhat.com/blog/csrd-vsme — V, Snippet
64. Whistleblowing comparisons: Elker — https://elker.com/articles/whistleblowing-software ; TrueSpeak — https://truespeak.eu/en/blog/comparisons/best-whistleblowing-software-2026-comparison ; WeMoral — https://wemoral.com/business/best-whistleblowing-software — V, Snippet
65. Council of the EU, "Deforestation: Council signs off targeted revision to simplify and postpone the regulation", 18 Dec 2025 — https://www.consilium.europa.eu/en/press/press-releases/2025/12/18/deforestation-council-signs-off-targeted-revision-to-simplify-and-postpone-the-regulation/ — P, Snippet
66. Hogan Lovells, "EU Deforestation Regulation: Commission publishes simplification package ahead of December 2026 application date" (May 2026) — https://www.hoganlovells.com/en/publications/eu-deforestation-regulation-commission-publishes-simplification-package-ahead-of-december-2026 ; European Commission news, 13 Jul 2026 — https://environment.ec.europa.eu/news/commission-updates-product-scope-and-tools-support-eudr-2026-07-13_en — S/P, Snippet
67. business.gov.uk, "EU Packaging and Packaging Waste Regulation (PPWR)" — https://www.business.gov.uk/campaign/europe/european-union-eu-regulations/eu-packaging-and-packaging-waste-regulation-eu-ppwr/ ; Coolset, "PPWR authorised representative" — https://www.coolset.com/academy/ppwr-authorised-representative — P/V, Snippet
68. EPR software landscape: Gramta — https://gramta.com/articles/epr-ppwr-compliance-software-landscape ; Repax — https://www.repax.io/blog/best-epr-software ; Lappa — https://lappa.org/articles/extended-producer-responsibility-ecommerce-eu — V, Snippet
69. Regulation (EU) 2024/1028, EUR-Lex — https://eur-lex.europa.eu/eli/reg/2024/1028/oj/eng ; European Commission news, 20 May 2026 — https://single-market-economy.ec.europa.eu/news/new-rules-bring-increased-transparency-short-term-rentals-sector-2026-05-20_en — P, Snippet
70. Chekin, "Regulation (EU) 2024/1028: Be Ready for May 2026" — https://chekin.com/en/blog/regulation-eu-2024-1028/ ; Minut — https://www.minut.com/blog/eu-short-term-rental-regulations — V, Snippet
71. GOV.UK, "Guide to the Renters' Rights Act", updated 6 Nov 2025 — https://www.gov.uk/government/publications/guide-to-the-renters-rights-act/guide-to-the-renters-rights-act — P, Read
72. RICS, "Renters' Rights Act: what's happening and when?", 16 Jan 2026 — https://ww3.rics.org/uk/en/journals/property-journal/renters-rights-act-implementation-roadmap.html — S, Read
73. GOV.UK Housing Hub, "Private landlords" — https://housinghub.campaign.gov.uk/renting-is-changing/ ; MHCLG blog, 20 Mar 2026 — https://mhclgmedia.blog.gov.uk/2026/03/20/%F0%9F%9B%8E%EF%B8%8F-landlords-here-are-6-ways-to-get-yourself-ready-for-new-renters-rights/ — P, Snippet
74. Landlord tools: LetDeck — https://letdeck.co.uk/ ; Dwelyx — https://www.dwelyx.co.uk/ ; LLCR — https://www.llcr.uk/ ; ComplianceBot — https://compliancebot.uk/ ; LetCompliance — https://letcompliance.com/landlord-compliance-software-uk ; LandlordOS — https://landlord-os.com/best-landlord-software-uk — V, Snippet
75. GOV.UK, "Find out if and when you need to use Making Tax Digital for Income Tax" — https://www.gov.uk/guidance/find-out-if-and-when-you-need-to-use-making-tax-digital-for-income-tax — P, Snippet
76. OpenRent, "A Summary of the English Private Landlord Survey 2024" — https://blog.openrent.co.uk/english-private-landlord-survey-summary/ — V/S, Snippet
77. Lewis Silkin, "Top tips to get ahead of the upcoming tipping changes", 20 Aug 2026 — https://www.lewissilkin.com/en/insights/2026/08/20/top-tips-to-get-ahead-of-the-upcoming-tipping-changes ; Blake Morgan — https://www.blakemorgan.co.uk/employment-rights-act-2025-revised-code-of-practice-tipping-and-umbrella-companies-consultations/ — S, Snippet
78. JustTip — https://justtip.co.uk/ ; IRIS Tronc — https://www.iris.co.uk/products/tronc-payroll/ ; Slashdot tip-distribution list — https://slashdot.org/software/tip-distribution/in-uk/ — V, Snippet
79. Employment Law Insights, "Show and Tell: New State Salary Disclosure Laws Go into Effect", Jul 2026 — https://www.employmentlawinsights.com/2026/07/show-and-tell-new-state-salary-disclosure-laws-go-into-effect/ ; Paycor, "2026 Pay Transparency Laws by State" — https://www.paycor.com/resource-center/articles/pay-transparency-laws-by-state/ — S/V, Snippet
80. IAPP, "New year, new rules: US state privacy requirements coming online as 2026 begins" — https://iapp.org/news/a/new-year-new-rules-us-state-privacy-requirements-coming-online-as-2026-begins ; MultiState, 4 Feb 2026 — https://www.multistate.us/insider/2026/2/4/all-of-the-comprehensive-privacy-laws-that-take-effect-in-2026 — S, Snippet
81. Mi Fichaje Legal, "Real Decreto registro horario digital… estado real de tramitación" — https://mifichajelegal.com/blog/real-decreto-registro-horario-digital-mayo-2026-estado-tramitacion-pymes/ ; Kronjop — https://kronjop.com/es/newsroom/control-horario/digital/obligatorio/ — V, Snippet
82. Jobber Academy, "Housecall Pro competitors" — https://www.getjobber.com/academy/housecall-pro-competitors/ ; Simpro, "Best Field Service Management Software" — https://www.simprogroup.com/blog/best-field-service-management-software — V, Snippet
83. WriteUpp, "Best Practice Management Software for Therapists in the UK (2026)" — https://www.writeupp.com/blog/best-practice-management-software-for-therapists-in-the-uk-2026-guide ; esremedia comparison — https://esremedia.co.uk/blog/physiotherapy-software-uk-comparison — V/S, Snippet
84. Certificial, "Best myCOI Alternatives in 2026" — https://www.certificial.com/blog-post/best-mycoi-alternatives-2026 ; COI File, "Best COI Tracking Software 2026" — https://coifile.com/coi-tracking/best-software/ ; BCS — https://www.getbcs.com/blog/top-certificate-of-insurance-tracking-companies — V, Snippet
85. Compliance & Risks, "Regulation (EU) 2024/573: Reviewing the New F-gas Regulation" — https://www.complianceandrisks.com/blog/regulation-eu-2024-573-european-commission-adopts-new-f-gas-regulation/ ; Refrigeration store guide — https://refrigerationstore.eu/gas/eu-f-gas-compliance-2026-certification-leak-checks-record-keeping/ — S/V, Snippet

---

## 8. Out-of-scope findings (for other agents; reported to the Orchestrator)

| ID | Finding | Responsible agent |
|---|---|---|
| OOS-01 | All four recommended areas are compliance-adjacent. Any product copy must avoid claims such as "CRA compliant", "guarantees compliance" or legal-advice framing; outputs should be positioned as records/evidence prepared by the customer. | Agent 14 Legal & Privacy; Agent 7 Marketing |
| OOS-02 | O2 and O4 would process payroll and pay data by sex (sensitive personal data, potentially health/disability data under national pay-transparency variants). O3 processes tenant data including vulnerability information. Data-protection design (DPIA, retention, access control) will be material. | Agent 13 Security; Agent 14 Legal & Privacy; Agent 10 Database |
| OOS-03 | O1 depends on third-party vulnerability data feeds; licence terms and attribution duties (e.g., OSV, NVD, GitHub Advisory Database, ENISA EUVD) are UNKNOWN and must be checked before architecture decisions. | Agent 9 Architecture; Agent 14 Legal |
| OOS-04 | O2 and O3 need authoritative UK bank-holiday data for working-day/pay-period calculations (a GOV.UK bank-holidays data feed exists — to be verified by Architecture). Calculation engines need a documented rule-update process when law/guidance changes (e.g., FWA "adequate records" guidance). | Agent 9 Architecture; Agent 11 Backend |
| OOS-05 | Several competitor categories (clinic PM, COI tracking, landlord certificate reading) market AI features as core value. An AI-free product may need to position determinism/auditability as a benefit; this is a positioning question, not a runtime change. | Agent 3 Strategy; Agent 7 Marketing; Agent 19 Runtime Independence |
| OOS-06 | If O1 is chosen, the company's own SaaS is generally outside CRA scope, but any downloadable component (CLI, agent, SBOM uploader) could itself be a "product with digital elements" [14][26]. | Agent 9 Architecture; Agent 14 Legal |
| OOS-07 | Jurisdiction choice (BUSINESS_COUNTRY in `project/decisions/BUSINESS_CONFIG.md`) interacts with candidate choice: O2/O3 are England/UK-only; O1/O4 are EU-market; O5 is US. | Agent 3 Strategy; Orchestrator |
| OOS-08 | Process caveat: research tooling returns summarised page content; §6 A-17 lists snippet-only sources that should be re-read in original before any claim is used externally (website, sales, legal pages). | Agent 2 Market Validation; Orchestrator |
