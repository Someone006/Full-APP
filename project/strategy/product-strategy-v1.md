# SaaS Product Strategy — v1

| Field | Value |
|---|---|
| Artifact | `project/strategy/product-strategy-v1.md` |
| Owner | Agent 3 — SaaS Strategy |
| Date | 2026-09-26. Statements about the market, law or vendors are "as recorded in the approved research on 2026-09-26" unless a check in §2.8 says otherwise. |
| Status | DRAFT v1, submitted for independent judging |
| Approved inputs | `project/AGENT_CHARTER.md`; `project/research/opportunity-research-v2.md` (Agent 1, APPROVED); `project/research/market-validation-v2.md` (Agent 2, APPROVED); `project/judges/judge-02-market-validation-v2.md` (residual risks §4; open LOW findings J2-009, J2-010); `project/judges/judge-01-opportunity-research-v2.md` (residual risks §4); `project/decisions/ENVIRONMENT_FACTS.md`; `project/decisions/BUSINESS_CONFIG.md` |
| Scope | Choose the opportunity. Define the product, customer, problem, value proposition, positioning, core workflow, MVP boundary, business-model direction, success metrics, assumptions, risks and proposed decisions. **Out of scope:** new market research (only the small confirmatory checks in §2.8), requirements (Agent 4), final prices (Agent 6), UI (Agent 8), technology choices (Agent 9). |

### Evidence labels and reference key

The labels are the charter set: **VERIFIED** · **SUPPORTED INFERENCE** · **ASSUMPTION** · **HYPOTHESIS** · **UNKNOWN**. Statements about future events are labelled UNKNOWN (future event), following Agent 2's convention. **DECISION** marks a choice this document makes. A decision is a judgement, not a fact.

| Reference | Means |
|---|---|
| [OR n] / [OR §x] | Source *n* / section *x* of `opportunity-research-v2.md` (approved) |
| [MV n] / [MV §x] | Source *n* / section *x* of `market-validation-v2.md` (approved) |
| [J1 §4.n] / [J2 §4.n] | Residual risk *n* in Judge 1's or Judge 2's v2 verdict |
| ENV-0nn | Row in `project/decisions/ENVIRONMENT_FACTS.md` |
| [S3-Cn] | Confirmatory check *n* run by Agent 3 in this session (§2.8) |

No customer, statistic, price, testimonial or legal fact in this document is invented. No customer interviews or pricing tests were possible in this build session. **Every statement about what customers want or will pay is a HYPOTHESIS.**

---

## 1. Decision summary

**DECISION: build O1.** O1 is an EU Cyber Resilience Act (CRA) vulnerability-handling, Art. 14 reporting-clock and evidence workspace for EU-market software-product SMEs whose builds can export CycloneDX or SPDX SBOMs. O2 (GB holiday-pay assurance) and O4 (EU pay transparency) are **not pursued**. O2 is kept as the named fallback under an explicit switch gate (§2.6). O4 goes to the watchlist with revival triggers (§2.5).

**Confidence: LOW–MEDIUM.**
- This is a decision under uncertainty, not a finding of proven demand.
- Judge 2 found O1 and O2 "close on the evidence". Both are rated Weak–Moderate for under-service, and neither has independent traction data [J2 §4.1].
- O1 wins on five things:
  - durability of the obligation to 2031 and beyond;
  - consequence of inaction;
  - EU-wide breadth;
  - the ability to build **and test** a real product end to end with open standards and licence-verified data reachable in this environment;
  - price anchors high enough to support a small team.
- O1 accepts three weaknesses: thin differentiation, mixed willingness to pay, and an episodic legal trigger.
- These weaknesses are handled by a deliberately small MVP and by pre-scale validation gates with stated switch and stop conditions (§2.6, §13.3).

**The one core job.** *When a known vulnerability, and above all an actively exploited one, affects a product version we have on the EU market, find out quickly. Then meet the Art. 14 reporting deadlines on time and keep a record of what we knew, when we knew it, and what we decided.*

---

## 2. Decision rationale

### 2.1 How the criteria were weighed
The ten criteria come from the assignment. Each is judged only on approved evidence plus the §2.8 checks. The weights are a DECISION: they reflect what a small team needs to survive and what the charter makes non-negotiable.

- **Gate criteria.** A candidate that fails any of these cannot be chosen:
  - core value deliverable with deterministic software (charter absolute rule);
  - buildable **and testable** as a production-quality MVP in this environment;
  - legal and liability risk containable by product design.
- **Heavily weighted.** Obligation certainty and timing, consequence of inaction, and durability to 2029–2031. They decide whether demand exists for long enough to matter.
- **Weighted.** Documented incumbent gaps, competitive density at SME prices, willingness-to-pay signals, and buyer clarity and reachability. The evidence on these is thin for every candidate, so none of them can decide the choice on its own.

### 2.2 Criterion-by-criterion comparison

| # | Criterion | O1 CRA workspace (SBOM-capable software SMEs) | O2 GB holiday-pay assurance | O4 EU pay transparency (Italy first) | Edge |
|---|---|---|---|---|---|
| 1 | Obligation certainty and timing | EU Regulation, directly applicable. Art. 14 reporting applies since **11 Sep 2026**, including products already on the market [OR 2][MV 1][MV 5]. The rest applies from **11 Dec 2027** (Art. 71(2)) [S3-C7]. Operational churn: the SRP glossary went from v1.1 to v1.3 in three weeks [MV 2][MV 23]. | Records duty in force since 6 Apr 2026 (criminal offence) [OR 12][MV 45]. FWA enforcement is a *plan* ("expected to begin in 2027") [MV 46]. The penalty regime is still a *proposal* (consultation closed 22 Sep 2026) [MV 45]. | Italy in force 7 Jun 2026; Greece from 1 Nov 2026 [MV 69][MV 76]. Italian reporting format **undefined** (decree pending) [MV 68][MV 70]. DE/FR/ES/NL not transposed [MV §4.0]. | O1 |
| 2 | Consequence of inaction | Fines up to €15m / 2.5% of worldwide turnover [OR 2]. Without CE marking there are no EU sales from Dec 2027 [OR 23]. Micro and small firms are relieved **only** from fines for the 24h early warning [OR 3]. | Criminal offence for records [OR 12]. Proposed 200% of arrears, capped at £20k per worker [MV 45]. FWA **cannot** enforce underpayments before 18 Dec 2025 [MV 45]. | Greece: fines €300–€50,000 per violation [MV 76]. Joint pay assessment at a ≥5% unexplained gap [OR 1]. | O1 |
| 3 | Durability to 2029–2031 | Grows over time. Art. 14 continues. From Dec 2027 manufacturers must also "systematically document … vulnerabilities of which they become aware" (Art. 13(7)), report component vulnerabilities to maintainers (Art. 13(6)) and meet Annex I Part II [S3-C7]. Support periods are ≥5 years unless the product's expected use time is shorter (Art. 13(8)) [OR 2]. Technical documentation is kept ≥10 years or for the support period, whichever is longer (Art. 13(13)) [S3-C7]. | The records duty recurs [OR 12]. Differentiation erodes if the government ships a holiday-pay calculator, which DBT is considering [MV 45], or if payroll incumbents close the gap [MV 51][MV 53][MV 56]. | Legally durable: recurring reports [OR 1]. The near-term SME segment is narrow: 150–249 first report Jun 2027; 100–149 not until 2031 [MV 69]. | O1 |
| 4 | Documented incumbent / free-tool gaps (§1.4 standard) | **Moderate.** Dependency-Track has no Art. 14 clock or SRP draft [MV 39]. The SRP has no API [MV 3]. Article 14 Ready does not persist data, by design [MV 23]. | **Strong** for Xero, Moneysoft and Sage 50 [MV 50][MV 51][MV 54], but **already addressed** by paiyroll (below). | **Weak.** No complaint data [MV §4.5]. | O2 on gaps; neutral after competitors |
| 5 | Competitive density at SME prices | CVD Portal Reporting €99/month claims 5 of 6 core functions, with automated SBOM↔CVE alerts Enterprise-only [MV 24]. ConformOps €79/month per product claims 3 of 6 [MV 22]. Article 14 Ready claims 2 of 6 [MV 23]. CRA Evidence (unpriced) claims all 6 [MV 25][J2-010(a)]. Kunnus (unpriced) claims most [MV 26]. Rated Weak–Moderate [MV §2.0(b)]. | paiyroll claims 5 of 7 functions **for exactly the gap products** at 15p/payslip (£30 minimum), plus a free compliance check and a free template [MV 49][MV 90][MV 91]. Payroll-native automation in Staffology and KeyPay [MV 53][MV 56]. Rated Weak–Moderate [MV §3.0(b)]. | Axios publishes €3,000–€4,500/yr for 100–249 employees, all EU [MV 80]. Zucchetti, the local payroll incumbent, sells a pay-gap module [MV 84]. Rated Weak [MV §6]. | Even (O1 vs O2); O4 worst |
| 6 | Willingness-to-pay signals | **Mixed.** Financial support ties with templates as the top support need (73.2%). 68.04% want compliance-assessment tools [MV 8]. No vendor publishes traction [MV §2.1]. | **Low but present.** Priced add-on with vendor-selected customer stories [MV 49][MV 89]. No independent uptake data [MV-U09]. | UNKNOWN [MV §6]. | O2 slightly |
| 7 | Price anchors (revenue per account, not WTP) | €79–€99/month for one product; €249/month for five [MV 22][MV 24]. | ~£30–£35/month for a 50-worker employer (arithmetic) [MV §3.3]. Bureau payroll ~£1–£2 per client per month [MV 90]. Employer full payroll £1.50–£2.20 per employee [J2-010(b)]. | €3,000–€4,900/yr [MV 80][MV 81]. | O1 over O2 (SUPPORTED INFERENCE: about 2–3× per account at published anchors, comparing €79–€99 with ~£32.50; any plausible EUR/GBP conversion keeps it in that range) |
| 8 | Buyer clarity and reachability | **Moderate.** A product or security lead at a software SME [MV §6]. 48% of CRA-aware respondents learned of the CRA in developer spaces [MV 10]. Preferred channels: webinars 57%, EU websites 56%, national authority 55% [MV 8]. Acquisition is hard: technical buyers, free tools, trust [MV §2.7]. | **Weak–moderate.** Employer vs bureau unresolved [MV §3.1c]. Bureau channel size UNKNOWN [MV-U04]. | **Weak.** HR vs consulente del lavoro vs payroll vendor; Italian-language barrier [MV §4.7]. | O1 slightly |
| 9 | Legal / liability risk if the product is wrong | Material, but **containable by design**. The customer decides the legal triggers (awareness, "actively exploited", "severe"). The product computes only deadlines (deterministic arithmetic that can be tested exhaustively) and matches (explainable, with coverage stated). Main hazards: a missed match, or output misread as a compliance guarantee [MV §2.9]. | Material and **direct**. The product would compute the holiday-pay rate the employer actually pays. That embeds legal interpretation ("normal remuneration", EU vs domestic leave) in every number [OR OOS-04][MV §3.8]. An error underpays every affected worker. | Material. Equal-value categorisation; sensitive pay-by-sex data; worker-representative sign-off [MV §4.8]. | O1 (see note ¹) |
| 10 | Deterministic delivery (no runtime AI) | Yes: parsing, package-URL matching, clocks, templates, audit trail [OR §3 O1]. Competitors add optional AI (ConformOps OpenAI, off by default; CVD Portal Enterprise AI triage) [MV 22][MV 24]. | Yes [OR §3 O2]. | Yes [OR §3 O4]. | Even |
| 11 | Feasibility of building **and testing** a real MVP here | **Yes, with real data end to end.** Inputs are open standards. `npm sbom` (npm 10.9.7) produces CycloneDX 1.5 and SPDX 2.3 with a purl on every component [S3-C3]. The OSV API and bulk exports are reachable [ENV-005][S3-C2]. Real matches were returned for those purls [S3-C4]. CISA KEV (CC0) is reachable [S3-C1][MV 19]. The licences needed are verified: GHSA/PyPA/Go CC-BY 4.0; RustSec CC0 [MV 14][MV 15]. The one gap is EUVD terms (UNKNOWN), so EUVD is excluded from the MVP [MV 17][MV 18]. | **Partly.** A rules engine and worked-example tests are feasible, and bank-holiday data is reachable [S3-C6]. **But** real payroll export files (Xero, Sage 50, BrightPay, Moneysoft) cannot be obtained here (MV-O2-06 is an ASSUMPTION). Importers would rest on guessed formats, which is a charter rule 7 risk, or on a generic CSV that adds friction next to paiyroll's 18 formats [MV 49]. Legal rule verification needs employment-law review that this build does not have [OR OOS-04]. | **No, not yet.** The core output (the Italian report) has **no defined format** [MV-U07]. Needs Italian language and NCBA categories [MV §4.0]. | O1 |
| 12 | Market breadth | EU-wide, including non-EU manufacturers selling into the EU [OR §5.3]. Segment size UNKNOWN (S1 proxy about one third of surveyed SMEs; software-SME share UNKNOWN) [MV §2.0]. | GB only; Northern Ireland differs [MV 90][OR A-18]. | One member state at a time. | O1 |

¹ Agent 1 rated (f) legal risk "Even (both material)" [OR §5.3]. This document separates the two on reasoning, not new evidence. In O1 the product never makes the legal determination. In O2 the product's main output *is* a legally determined money amount. This is SUPPORTED INFERENCE.

### 2.3 Why O1: the decisive factors (in order)
1. **The obligation is live, fixed and growing.**
   - Art. 14 has applied since 11 Sep 2026 to the installed base [OR 2][MV 5].
   - From 11 Dec 2027 the documentation and vulnerability-handling duties (Art. 13(6)–(7), Annex I Part II) turn a rare emergency job into a continuous record-keeping job [S3-C7].
   - Support periods (≥5 years unless expected use time is shorter) and documentation retention of ≥10 years carry the need well past 2031 [OR 2][S3-C7].
   - O2's enforcement and penalties are still plans or proposals [MV 45][MV 46]. O4's first SME-band deadline covers only 150–249 employers [MV 69].
2. **The consequence is market access, not only a fine** [OR 23]. It applies EU-wide.
3. **It is the only candidate that can be built and tested for real, end to end, in this environment.** Standard inputs, reachable data and licence-verified sources mean findings can be tested against real advisories [S3-C2–C4]. O2 would need payroll exports we cannot obtain. O4 would need a report format that does not yet exist. This matters under charter rule 7 (no fake functionality) and rule 13 (every critical workflow tested).
4. **The unit economics are plausible if demand exists.** Published SME anchors are €79–€249/month [MV 22][MV 24], against about £30/month for O2 [MV §3.3]. A small team can only recover acquisition cost at the higher anchor.
5. **Liability can be contained by product design.** The human decides, the product explains, and the only computed legal element (deadline arithmetic) can be verified exhaustively.
6. **O2's remaining differentiators are weaker than O1's.** paiyroll already covers calculation, 104-week lookback, audit trail and imports for the gap products [MV 49]. O2's remaining ideas are retention/immutability, an FWA-oriented pack and a companion multi-client view. They depend on FWA guidance that does not exist yet, and a free government calculator may arrive [J2 §4.2][MV 45].

### 2.4 What argues against O1 (accepted, not dismissed)
- **Thin differentiation** [J2 §4.3].
  - CVD Portal lacks only automated SBOM↔CVE alerts at €99/month [MV 24].
  - CRA Evidence claims all six functions at an unpublished price [MV 25].
  - Either could close the gap quickly.
- **Mixed willingness to pay and strong free substitutes.**
  - Financial support is a top-tied need [MV 8].
  - ENISA wants support to be "freely accessible" [MV 8].
  - Dependency-Track now mirrors EU KEV [MV 39].
  - The SRP form itself guides drafting [MV 2].
- **An episodic legal trigger, now partly quantified.** Only 131 of 1,726 KEV entries (7.6%) map to advisories in the eight package ecosystems. Of these, 17 were added in 2025 and 26 in 2026 up to 25 Sep [S3-C5]. SUPPORTED INFERENCE: for any single SME product, a KEV-listed exploited component will be rare. Monthly value must therefore come from continuous monitoring and the documentation record, not from Art. 14 cases alone. This shapes the MVP (§9) and the metrics (§13).
- **Segment size is UNKNOWN** [MV-U01]. **Traction for any CRA tool is UNKNOWN** [MV-U03].
- **Trust barrier.** A new small vendor is asking to hold unpatched, exploited-vulnerability details [MV §2.7].
- **Regulatory and operational churn.** Glossary changes; a possible ENISA API [MV 3]; a possible implementing act on format (Art. 14(10)) [MV 1].

### 2.5 Rejected alternatives

| Alternative | Decision | Why | What would reopen it |
|---|---|---|---|
| **O2 GB holiday-pay assurance** | Not pursued. **Named fallback** under gate G-V3 (§13.3) | 1. A direct add-on already covers 5 of 7 functions for exactly the gap products at 15p/payslip, with free lead-ins [MV 49][MV 90][MV 91]. 2. Remaining differentiators depend on FWA guidance that does not exist, and a government calculator is being considered [MV 45][J2 §4.2]. 3. Enforcement and penalties are still plans or proposals [MV 45][MV 46]. 4. Very low anchors: £30/month minimum; £1–£2 per client for bureaus; £1.50–£2.20 per employee for full payroll [MV 90][J2-010(b)]. 5. Real payroll export formats cannot be obtained to build and test importers here (MV-O2-06). 6. Direct pay-calculation liability (§2.2 row 9). 7. GB-only market. | All of: G-V3 fires for O1; the government response confirms the FWA penalty regime; no free government calculator covers the core by then (MV-O2-04); sample exports are obtained from ≥3 payroll products; an employment-law reviewer is available for rule verification. |
| **O4 EU pay transparency** | Not pursued. **Watchlist** | 1. The core output (the Italian report) has no defined format [MV-U07]. 2. Narrow near-term segment: 150–249 first report Jun 2027; 100–149 in 2031 [MV 69]. 3. A strong local incumbent (Zucchetti) and SME-priced EU-wide tools (Axios €3,000–€4,500/yr) [MV 80][MV 84]. 4. Italian language and NCBA categories are needed [MV §4.0]. 5. Sensitive pay-by-sex data; Garante involvement [MV §4.8]. 6. Weakest evidence on every demand row [MV §6]. | The Italian ministerial format is published **and** at least one of DE/FR/NL transposes with a defined format **and** a pricing test shows willingness to pay above the Axios anchors [MV-O4-04]. |
| **O3 Awaab's Law** | Stays on the watchlist (no change) | No decisive new evidence [MV §5] | Agent 1's revival conditions [OR §5.5] |
| **"None is viable"** | Not concluded **now**, but defined as an exit | The evidence proves demand for **no** candidate (RISK-001). Stopping now would forgo the only way to create that evidence: a small, real product with landing-page and pricing tests. O1 can be tested cheaply because its MVP is small and its data is public. | Gate G-V3 (§13.3). If O1 fails its pricing and activation tests **and** O2's reopen conditions are not met, the recommendation becomes "stop; no candidate viable". What would be needed then is primary customer evidence (interviews, pre-orders) for a new or revised candidate. |

### 2.6 Status of Agent 1's switch condition
Agent 1's condition: "if Market Validation finds that SBOM-capable software SMEs will not pay more than free tooling plus the €79–€99 one-off offers, O2 should become the lead candidate" [OR §5.3].
- **It has not fired.** It is also **untested**, because no pricing interviews were possible [MV §2.0(b)]. It therefore neither blocks nor supports O1.
- Judge 1 asks that it be "applied literally" [J1 §4.2]. This document does so by turning it into pre-scale gate **G-V3** (§13.3), with a measurable test (V1-3 [MV §2.10]) and a named fallback (O2, subject to its own reopen conditions in §2.5).
- The market has moved on from "one-off" offers. The SME anchors are now **recurring**: €79/month per product (ConformOps) and €99/month (CVD Portal) [MV 22][MV 24]. The gate therefore tests willingness to pay against the lowest recurring anchor.

### 2.7 How this document answers the judges' residual risks

| Residual risk | Response here |
|---|---|
| J2 §4.1: candidates close; choice rests on differentiation hypotheses | Stated openly in §1 and §2.4. Differentiation is kept as HYPOTHESES (§6). Validation gates are in §13.3. |
| J2 §4.2: O2 differentiators depend on future guidance | Used as a reason for rejection (§2.5). Kept as a reopen condition. |
| J2 §4.3: O1's remaining differentiator is thin | Accepted. We do not claim a moat (§6.3). The strategy competes on the complete job at an SME price, with coverage transparency, and monitors competitors (R-02, G-V4). |
| J2 §4.4: low price anchors | Business-model direction keeps all core functions in every paid tier and leaves prices to Agent 6 (§12). |
| J2 §4.5: regulatory volatility and gating unknowns | EUVD excluded from the MVP (DECISION-009). Glossary and clock rules versioned as configuration. Monitoring duty (R-06). |
| J2 §4.6: sources to re-read before external use | Only O4-related items are listed there. O4 is not chosen. §19 passes the list on to Agent 7. |
| J1 §4.2: apply the switch condition literally | §2.6 and G-V3. |
| J1 §4.3: O2 penalty regime is still a proposal | Used in §2.2 rows 1–2 and §2.5. |
| Open LOW J2-009 (O4 not function-mapped) | Does not affect the decision. O4 is rejected on format, segment and incumbent grounds, not on the coverage map. |
| Open LOW J2-010 (a) CRA Evidence alone claims all six; (b) employer payroll anchors; (c) Distr Business tier | (a) Used as corrected in §2.2 row 5 and §6. (b) Strengthens the O2 low-anchor point (§2.5). (c) Adds one adjacent vendor with vulnerability management ($160/month); no change to the O1 rating. |

### 2.8 Confirmatory checks run by Agent 3 (2026-09-26)
These are feasibility checks, not new market research. They are recorded here because `ENVIRONMENT_FACTS.md` is the Orchestrator's file. The Orchestrator may import S3-C1 to S3-C6 (see §19).

| ID | Check | Result | Label |
|---|---|---|---|
| S3-C1 | CISA KEV JSON feed (`https://www.cisa.gov/sites/default/files/feeds/known_exploited_vulnerabilities.json`) and GitHub mirror (`cisagov/kev-data`) | HTTP 200 for both. `catalogVersion` 2026.09.25, released 2026-09-25T18:58Z, 1,726 entries. Licence CC0 per [MV 19]. | VERIFIED (observed) |
| S3-C2 | OSV per-ecosystem bulk exports (`https://osv-vulnerabilities.storage.googleapis.com/<ecosystem>/all.zip`) | HTTP 200 for npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems and Packagist. Compressed sizes: npm 217 MB, PyPI 35 MB, Go 12 MB, Packagist 11 MB, Maven 10 MB, RubyGems 5 MB, crates.io 3.5 MB, NuGet 2.5 MB. Non-withdrawn records: npm 228,730; PyPI 25,154; Go 9,202; Packagist 7,095; Maven 7,040; RubyGems 5,326; crates.io 2,732; NuGet 1,869. | VERIFIED (observed) |
| S3-C3 | `npm sbom --package-lock-only` (npm 10.9.7, ENV-001) on a probe project depending on lodash 4.17.20 and express 4.17.1 | CycloneDX **1.5** JSON: 51 components, 51 with a purl. SPDX **2.3** JSON: 52 packages, 52 with a purl. | VERIFIED (observed) |
| S3-C4 | OSV `POST /v1/querybatch` with the 51 purls from S3-C3 | 8 of 51 components returned advisories (e.g., `pkg:npm/lodash@4.17.20`: 5; `pkg:npm/qs@6.7.0`: 4). Shows the pipeline works with real data. Says nothing about prevalence in customer products, because the probe uses deliberately old versions. | VERIFIED (observed); interpretation SUPPORTED INFERENCE |
| S3-C5 | KEV CVE IDs intersected with the `aliases`/`related` IDs of non-withdrawn OSV records in the 8 ecosystems | 131 of 1,726 KEV CVEs (7.6%) appear. By ecosystem (a CVE can appear in more than one): Maven 53, Packagist 24, PyPI 21, NuGet 16, npm 13, Go 10, RubyGems 4, crates.io 1. By KEV `dateAdded`: 2021 24; 2022 40; 2023 16; 2024 8; 2025 17; 2026 (to 25 Sep) 26. KEV is a CISA (US) catalogue and does not list every exploited vulnerability, so this is a lower bound on exploitation signals, not a per-SME frequency. | VERIFIED (computed); interpretation SUPPORTED INFERENCE |
| S3-C6 | GOV.UK bank holidays JSON (checked so that the O2 feasibility assessment is symmetric) | HTTP 200. Divisions: england-and-wales, scotland, northern-ireland. | VERIFIED (observed) |
| S3-C7 | CRA OJ text re-read (`https://publications.europa.eu/resource/celex/32024R2847`, XHTML, `Accept-Language: en`) | Art. 3: "'actively exploited vulnerability' means a vulnerability for which there is reliable evidence that a malicious actor has exploited it in a system without permission of the system owner". Art. 13(6): report a vulnerability found in a component "to the person or entity manufacturing or maintaining the component". Art. 13(7): "systematically document … relevant cybersecurity aspects … including vulnerabilities of which they become aware". Art. 13(13): keep technical documentation "for at least 10 years after the product … has been placed on the market or for the support period, whichever is longer". Art. 14(5): the severe-incident test. Art. 71(2): applies from 11 Dec 2027; Art. 14 from 11 Sep 2026. Annex I Part II points (1)–(8), including (1) "identify and document vulnerabilities and components … including by drawing up a software bill of materials" and (2) "address and remediate vulnerabilities without delay". | VERIFIED (P, read) |

---

## 3. Product definition

**Working name: "Keelwatch"**. This is a **placeholder brand** pending business-owner approval and trademark, domain and company-name checks, none of which has been done. It must not appear in public material until it is approved (HDP-2).

**Plain-language description.** Keelwatch is a self-serve web workspace for small software companies that sell products in the EU.
- They register their products and the versions on the market, and upload the software bill of materials (SBOM) their build already produces.
- Every day, Keelwatch checks every component against public, licensed vulnerability databases. It flags components listed as known to be exploited and alerts the team by email.
- The team records a decision for each finding. A decision made once is reused across other versions that contain the same component.
- When the company becomes aware of an actively exploited vulnerability or a severe incident, from a finding or from any other source, it opens a case. Keelwatch then:
  - runs the CRA Art. 14 clocks (24-hour early warning, 72-hour notification, final report);
  - reminds the team before each deadline;
  - prepares the fields ENISA's Single Reporting Platform asks for at each stage, checked against the current field glossary, so the company can copy them into the platform itself.
- Everything is kept as a timestamped record that can be exported: which data sources were checked and when, what matched, who decided what, and when each stage was submitted.

Keelwatch does not submit reports, decide legal questions, certify compliance or use AI.

---

## 4. Target customer

### 4.1 Customer type, market and jurisdiction
- **Customer type: B2B only.** DECISION (DECISION-004). The buyer is a manufacturer in the CRA sense. There is no consumer offering.
- **Regulatory jurisdiction: the EU.** The CRA is a regulation, directly applicable in all 27 Member States [OR 2][S3-C7].
- **Primary target market: the EU single market, English-language, self-serve.** DECISION (DECISION-003).
  - It covers software-product SMEs **established in the EU** that place products on the EU market.
  - The evidence base is ENISA's EU SME survey [MV 8].
  - English is acceptable for the MVP because the SRP itself is English-only at launch [MV 3]. Acceptance is an ASSUMPTION (A-S08).
- **Additional target market (secondary):** manufacturers established **outside** the EU (e.g., UK, CH, US) that make products available on the EU market. The CRA applies to them too [OR §2 O1]. They are served by the same product. Art. 14(7) fallback rules for which CSIRT coordinates are entered by the customer, never determined by us (§14).
- Whether the CRA applies in the EEA (non-EU) states was not established in the approved research. It is **UNKNOWN** and must not be claimed.

### 4.2 Ideal Customer Profile (ICP)
The segment definition adopts Agent 2's recommendation verbatim [MV §2.0]: *"EU-market software-product SMEs — software developers, and connected-device makers whose application layer is package-managed — whose build tooling can export CycloneDX or SPDX SBOMs."*

| Attribute | ICP (primary) | Evidence / label |
|---|---|---|
| Role under the CRA | Manufacturer of a product with digital elements placed on the EU market: installable or on-premises software, desktop or mobile apps, commercial libraries and SDKs, or connected devices whose application layer is built with package managers | [OR §3 O1]; ENISA roles: software developers 41%, product manufacturers 20% [MV 8] |
| Size | **Small and medium enterprises, 10–249 staff** (primary); micro enterprises (<10) served self-serve as secondary | ENISA sample: micro 27%, small 36%, medium 37% [OR 27]. Medium firms get **no** fine relief for the 24h early warning; micro and small get relief for that deadline only [OR 3]. Priority order is a HYPOTHESIS (A-S13). |
| Products | 1–20 products (product lines), each with one or more versions under support | HYPOTHESIS (a size band for tiering; Agent 6 to test) |
| Build tooling | Package-managed code in npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems or Packagist; CI able to emit or export CycloneDX or SPDX JSON (e.g., GitHub dependency-graph export [MV 13]; `npm sbom` [S3-C3]) | [MV 13][S3-C2][S3-C3] |
| SBOM maturity | **S1** already producing SBOMs (ICP core; proxy about one third of surveyed SMEs, true share UNKNOWN). **S2** can export but does not yet produce SBOMs (served with onboarding guidance; this is friction, not a solved problem) | [MV §2.0]; MV-O1-01; MV-O1-02 |
| Security organisation | No dedicated product-security team (PSIRT). Security is owned by the CTO, a lead engineer or a "security champion". | SUPPORTED INFERENCE from 36% of micro-companies having no incident-response plan [MV 8] and low readiness [MV 10]; HYPOTHESIS for small and medium firms |
| Purchase mode | Card or self-serve subscription, no procurement process | ASSUMPTION (A-S16) |

**Explicit exclusions (not ICP):**
- **Firmware or embedded C/C++ products** that need binary analysis to get an SBOM. Not MVP-feasible [OR 38]; enterprise tools serve them [MV §2.1 row 13].
- **Pure SaaS companies with no product in CRA scope.** SaaS is generally out of scope unless it is remote data processing for a product [OR 23][OR 34].
- **Enterprises with a PSIRT and enterprise platforms.**
- **Products whose risk sits mainly in OS or container packages** (Debian, Alpine, Ubuntu). Those advisory sources are excluded from the MVP (§11, DECISION-009).

### 4.3 Roles: buyer, user, approver
In an SME these roles often sit with two or three people, or even one. The product must work when one person holds all of them.

| Role | Typical title | What they need | Label |
|---|---|---|---|
| **Economic buyer** | CTO, Head of Engineering, technical founder | Confidence that CRA vulnerability handling is under control, at a predictable monthly cost | SUPPORTED INFERENCE: "product/security lead at a software SME" [MV §6] |
| **Primary user** | Lead engineer, security champion, DevOps engineer | Upload SBOMs (manually or from CI), see findings, record decisions, run cases, prepare SRP fields | SUPPORTED INFERENCE |
| **Approver / accountable** | Managing director or CEO, and legal counsel where one exists | Sign-off on what the company reports and when. They are accountable for the legal exposure. | HYPOTHESIS (approval practice untested) |
| **SRP submitter** | The company's Primary or Secondary Authorised Representative on the SRP, who must hold an EU Login account with MFA; one Primary AR, up to 20 Secondary ARs [MV 3] | Copy-ready, validated fields per stage; a place to record submission time and reference | VERIFIED (platform rules) [MV 3] |
| **Occasional contributor** | Product manager, customer success | Support-period dates; user-notification text (Art. 14(8)) | HYPOTHESIS |

**Trigger events** (all HYPOTHESES unless labelled):
- Art. 14 has applied since 11 Sep 2026 (VERIFIED [MV 5]).
- Preparing for CE marking before 11 Dec 2027 (VERIFIED date [S3-C7]).
- A known-exploited vulnerability appears in their stack.
- A business customer asks for evidence of vulnerability handling. No evidence was found for or against this; it is a HYPOTHESIS.

---

## 5. Problem statement and jobs-to-be-done

### 5.1 Problem statement
- **Reporting duty, live now.** Since **11 September 2026**, every manufacturer of a product with digital elements on the EU market must notify ENISA's Single Reporting Platform of actively exploited vulnerabilities and severe incidents. This includes products already on sale. There are three stages: an early warning within 24 hours, a notification within 72 hours, and a final report [MV 1][MV 5].
- **Wider duties from 11 December 2027.** Manufacturers must also identify and document the vulnerabilities and components in their products, including with an SBOM. They must remediate without delay and systematically document the vulnerabilities they become aware of [S3-C7].
- **The platform does not help with the rest.** It has no API and is English-only at launch [MV 3]. Its field set changed twice in September 2026 [MV 2][MV 23].
- **SMEs are not ready and ask for help.** 36% of micro-companies have no incident-response plan, and 68.04% of SMEs ask for tools that help assess compliance [MV 8].
- **Existing options cover fragments of the job.**
  - Free tools do either matching (Dependency-Track [MV 39]) or drafting without persistence (Article 14 Ready [MV 23]), not both with a retained record.
  - The SME-priced offer closest to the whole job reserves automated SBOM-to-vulnerability alerts for its quote-only Enterprise tier [MV 24].
  - Consultants and labs are quote-only [MV 21].

### 5.2 Jobs-to-be-done
Functional jobs are grounded in legal text and product evidence. Emotional and social jobs are **HYPOTHESES**: no interviews were possible.

| ID | Type | Job statement ("When …, I want to …, so that …") | Traced to |
|---|---|---|---|
| JTBD-F1 | Functional | When a new vulnerability is published, or one is newly listed as exploited, and it affects a component in a product version we have on the EU market, I want to know within a day, so that I can assess it before a legal clock may be running. | Art. 14(1)–(2) [MV 1]; Annex I Part II(1)–(2) [S3-C7]; Dependency-Track matching without Art. 14 [MV 39]; CVD Portal's automated alerts Enterprise-only [MV 24] |
| JTBD-F2 | Functional | When we become aware of an actively exploited vulnerability or a severe incident, from any source, I want to meet the 24h / 72h / final-report deadlines with the fields the SRP requires at each stage, even out of hours, so that we report on time without inventing a process under pressure. | Art. 14(2), (4) [MV 1]; SRP glossary v1.3 required fields [MV 2]; no API [MV 3]; 36% of micro-companies without an IR plan [MV 8]; Art. 3 definition [S3-C7] |
| JTBD-F3 | Functional | For each product version, I want a record of what we knew, when, and what we decided about each vulnerability, so that we can show it to an authority, a notified body or a customer later. | Art. 13(7), Art. 13(13), Annex I Part II(1) [S3-C7]; F6 "evidence / audit trail" [MV §2.0(b)] |
| JTBD-F4 | Functional | When we have a fix or mitigation, I want a draft notice for affected users, so that we can inform them as Art. 14(8) requires, where appropriate. | Art. 14(8) [MV 1]; Annex I Part II(4), (8) [S3-C7] |
| JTBD-E1 | Emotional | I want to stop worrying that a 24-hour clock has started without us noticing. | HYPOTHESIS; indirect support: low readiness [MV 8][MV 10] |
| JTBD-E2 | Emotional | I want to feel we are doing what is reasonable without hiring consultants we cannot afford. | HYPOTHESIS; indirect support: financial support and templates are the joint-top needs [MV 8] |
| JTBD-S1 | Social | As CTO, I want to show the managing director, customers or investors that vulnerability handling is systematic. | HYPOTHESIS |
| JTBD-S2 | Social | As a small vendor, I want to answer a customer's or auditor's "how do you handle vulnerabilities?" with a document, not an anecdote. | HYPOTHESIS |

**Out of the job on purpose:**
- deciding whether the product is "important" or "critical";
- conformity assessment;
- technical-documentation authoring;
- generating SBOMs from binaries.

These are either legal judgments, a different job, or not feasible (§11).

---

## 6. Value proposition and differentiation

### 6.1 Value proposition
*Know within a day when a known or exploited vulnerability hits a product you sell in the EU. Meet the Art. 14 deadlines with SRP-ready fields. Keep a timestamped record of what you knew and decided. All in one self-serve workspace at an SME price, without submitting anything on your behalf and without AI.*

### 6.2 Differentiation hypotheses (only what the evidence supports)

| ID | Hypothesis | Evidence for | Evidence against / limits | Label |
|---|---|---|---|---|
| H-D1 | **The complete core job in one self-serve plan**, with **automated SBOM→advisory matching included in every paid tier**: F1 matching, F2 exploited flag, F3 Art. 14 clocks, F4 SRP-aligned drafts and F6 evidence, plus F5 as a user-notice draft | No published SME-priced offer found claims all six functions. CVD Portal reserves automated SBOM↔CVE alerts for Enterprise. ConformOps lacks F2, F4 and F5. Article 14 Ready does not persist data [MV §2.1a][MV 22][MV 23][MV 24]. | CRA Evidence claims all six at an unpublished price [MV 25][J2-010(a)]. CVD Portal could move one feature down-tier [J2 §4.3]. Whether buyers value the combination is UNKNOWN (V1-3, V1-4 [MV §2.10]). | HYPOTHESIS |
| H-D2 | **Transparent coverage and explainable matches.** Every uploaded SBOM shows which components could and could not be checked (no purl, unsupported ecosystem). Every finding shows the source record, affected range and sync time. | SBOM completeness is "quite a lot or extremely difficult" for 62% [MV 9]. Dependency-Track users complain about false positives [MV 40]. Coverage transparency also mitigates liability (R-04). | Competitors may already show sources. This is not proven to be valued. | HYPOTHESIS |
| H-D3 | **Triage decisions reused across versions and products** for the same component and advisory | Dependency-Track issue #5992: false positives can be marked only per project and component version [MV 40] | ConformOps already matches by package URL [MV 22]. Its reuse behaviour is not documented in the approved research (UNKNOWN). | HYPOTHESIS |
| H-D4 | **Glossary-versioned SRP drafts** with per-stage Required/Optional validation, and the glossary version recorded on every draft | Glossary v1.1 → v1.3 in three weeks [MV 2][MV 23] | CVD Portal, CRA Evidence and Article 14 Ready already claim SRP-aligned output. This is parity plus maintenance discipline, **not a moat** [MV §2.6]. | HYPOTHESIS |
| H-D5 | **Deterministic and reproducible.** The same inputs and the same data snapshot give the same findings and deadlines, with no AI | Competitors add AI [MV 22][MV 24][MV 42] | Buyers valuing "no AI" is an **ASSUMPTION** [MV-O1-07]. **Not a lead message** until tested (§7). | ASSUMPTION |

### 6.3 What we deliberately will NOT compete on
- **Lowest price.** Free Dependency-Track, the free Article 14 Ready compiler and €79/month anchors exist [MV 22][MV 23][MV 39]. We compete on the complete job, not on price.
- **Binary or firmware SBOM generation and analysis.** Not feasible; enterprise incumbents [OR 38][MV §2.1].
- **Conformity assessment, testing, CE marking or certification.** Labs and notified bodies do this [MV 21].
- **Submission to the SRP.** There is no API, and the customer's Authorised Representative must submit [MV 3].
- **Breadth of documentation.** Annex VII technical documentation, the EU declaration of conformity and template libraries. CVD Portal, Kunnus and CRA Evidence already combine these [MV §2.6]. The Commission must specify a free simplified form (Art. 33(5)) [MV §2.8 Q4].
- **AI triage or AI summarisation.** Prohibited at runtime by the charter.
- **Code scanning** (SAST, secrets, containers, DAST). A crowded adjacent market (Aikido, Trivy) [MV 31][MV 38].
- **Enterprise features** (SSO, custom workflows, on-premises). Not the ICP.
- **Human services** (PSIRT-as-a-service, 24×7 monitoring, legal advice).

---

## 7. Positioning statement

> **For** software companies with fewer than 250 staff that sell products in the EU and have no dedicated product-security team, **who** must now handle vulnerabilities and meet the CRA's 24-hour, 72-hour and final-report deadlines, **Keelwatch** (working name) **is** a vulnerability-handling and reporting-clock workspace **that** checks your SBOMs daily against public vulnerability data, flags known-exploited components, runs the Art. 14 clocks, prepares the fields ENISA's reporting platform asks for, and keeps a timestamped record of what you knew and decided. **Unlike** free tools that stop at matching or at drafting, and the SME-priced offer that reserves automated SBOM alerts for its enterprise plan, **it** does the whole job in one self-serve plan at an SME price. It does not submit reports, certify compliance or give legal advice.

Guidance for Agent 7:
- The competitive clause ("unlike …") describes the evidence as of 2026-09-26 [MV §2.1a]. It must be re-checked before any public use, and must not name competitors without current evidence.
- "No AI" and "deterministic" may appear as a factual product property: every finding is traceable to a source record and a rule. They are **not** a lead benefit until tested (H-D5).

---

## 8. Core workflow (sign-up to recurring value)

| Step | Who | What happens | Value / job |
|---|---|---|---|
| 1 | Buyer or user | Signs up with a business email, verifies it, creates a workspace (one manufacturer), and sets up MFA | Trust and security |
| 2 | User | Enters the manufacturer profile: name as used on the SRP, and Member State of main establishment (**selected by the customer**, not determined by us) | Pre-fills SRP fields [MV 2] |
| 3 | User | Creates a product: name as reported to the SRP, Member States where it is made available, optional support-period end date, optional customer-entered product type or class | Pre-fill; product = unit of value (§12) |
| 4 | User | Adds the versions currently on the market and uploads an SBOM per version (CycloneDX or SPDX JSON), in the browser or from CI with an upload-only API token. Without an SBOM, the user follows the "get an SBOM" guide (S2). | JTBD-F1, F3 |
| 5 | System | Parses the SBOM and shows a **coverage summary**: components, components with a purl, components in supported ecosystems, and components **not checked** with the reason | Activation moment 1; H-D2 |
| 6 | System | Matches components against the latest licence-verified advisory data. Shows findings with source, advisory ID, aliases (CVE), affected range and sync time. Highlights findings listed in CISA KEV as "known exploited — triage required". | Activation moment 2 ("first findings viewed"); F1, F2 |
| 7 | User | Triages each finding: under investigation / not affected (with justification) / affected / fixed in version X, with a rationale. The decision can be applied to other versions and products with the same component and advisory. | F6; H-D3 |
| 8 | System (daily) | Syncs advisory data and KEV, re-matches all monitored versions, and emails alerts for new KEV-flagged findings, plus a digest of other new findings. Sync status and time are visible. | Recurring value; JTBD-F1 |
| 9 | User | When the company becomes aware of an actively exploited vulnerability or a severe incident, from a finding, a researcher's report, own-code discovery or any other source, it opens an **Art. 14 case** and records the **awareness time (UTC)**. The system never sets this automatically; it may suggest a time for the user to confirm. | JTBD-F2 |
| 10 | System | Computes the early-warning (24h) and notification (72h) deadlines from the awareness time. Shows countdowns in UTC and local time. Sends reminders before each deadline. | F3 |
| 11 | User | Completes the stage drafts (early warning → notification → final report) pre-filled from case, product and version data. Each draft is validated against the recorded glossary version, then copied or exported for **manual** entry into the SRP. The user records the submission time and SRP reference for each stage. | F4 |
| 12 | User → System | Records when a corrective or mitigating measure became available (vulnerability final report: ≤14 days after) or when the notification was submitted (incident final report: within one month). The system computes the final-report deadline. The user can add CSIRT intermediate-report requests to the case timeline. | F3 |
| 13 | User | Generates a draft notice for affected users (Art. 14(8)) and exports it | F5 (draft), JTBD-F4 |
| 14 | User | Closes the case and exports the **evidence pack**: timeline, decisions, drafts, submissions recorded, data sources and sync times, glossary version | F6, JTBD-F3 |
| 15 | Recurring | On each release, CI uploads a new SBOM and re-matching runs. The user exports a per-version **vulnerability status report** when needed. The audit trail accumulates. Billing renews. | Retention; JTBD-F3, S2 |

Principle: an Art. 14 case **never depends on an SBOM match**. Many exploited vulnerabilities will be in the customer's own code or will arrive through a report, not through a third-party component (SUPPORTED INFERENCE from the Art. 3 definition [S3-C7] and S3-C5).

---

## 9. MVP scope

**MVP in one sentence:** a self-serve B2B workspace that monitors uploaded CycloneDX or SPDX SBOMs daily against licence-verified OSV data and CISA KEV, records triage decisions, and, when the customer becomes aware of an actively exploited vulnerability or severe incident, runs the Art. 14 clocks, prepares glossary-validated SRP field drafts for manual submission and exports a timestamped evidence pack.

**Boundary parameters** (part of DECISION-005):
- **Inputs.** CycloneDX JSON 1.4–1.6 and SPDX JSON 2.2–2.3. `npm sbom` emits CycloneDX 1.5 and SPDX 2.3 [S3-C3]; GitHub exports SPDX 2.3 [MV 13].
- **Ecosystems.** npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems and Packagist, matched by package URL (purl) [S3-C2].
- **Advisory data.** Only OSV records whose originating source licence is verified as allowing commercial reuse (e.g., GHSA, PyPA and Go CC-BY 4.0; RustSec CC0 [MV 14][MV 15]), with attribution.
- **Exploited signal.** CISA KEV (CC0) [MV 19][S3-C1].
- **Excluded from MVP:** EUVD / ENISA EU KEV (terms UNKNOWN), NVD, and distro advisories (e.g., Ubuntu CC-BY-SA; converted Debian/Alpine data with no licence stated) [MV 14][MV 17][MV 18].
- **Language.** English.

Classification key: **Core** = delivers the core job; **Activation** = gets a new customer to first value; **Legal/Security** = required by law, the charter or security; **Commercial** = required to operate as a paid SaaS.

| ID | MVP feature | Class | Justification (validated problem / evidence) | Anti-bloat test (launch without it?) |
|---|---|---|---|---|
| M1 | **Accounts, workspace, roles.** Email sign-up with verification; one workspace per manufacturer; invite members; at least two server-enforced roles (admin, member); MFA available to all users and enforceable by the workspace admin | Legal/Security | The workspace holds details of unpatched and exploited vulnerabilities (R-08). Charter rule 9. The SRP itself requires MFA for its users [MV 3]. Trust prerequisite V1-7 [MV §2.10]. | No |
| M2 | **Manufacturer profile.** Name used on the SRP; Member State of main establishment (customer-selected) | Core | SRP early-warning fields [MV 2] | No: drafts cannot be pre-filled |
| M3 | **Product and version register.** Products (SRP product name, Member States made available, optional support-period end, optional customer-entered type/class); versions (version string, on-market flag) | Core | "Product name" and "product version or range" are required at the early warning [MV 2]. Monitoring scope. Unit of value (§12). | No |
| M4 | **SBOM ingestion and coverage summary.** Upload in the UI or through one upload-only API endpoint with a workspace token (for CI). Parse the supported formats, keep the original file with its hash, and show the coverage summary (checked / not checked, with reason). | Core + Activation | Annex I Part II(1) SBOM [S3-C7]; SBOM completeness pain [MV 9]; S2 onboarding friction [MV §2.0]. The API is **HTTP only**; no downloadable CLI or agent (DECISION-010, [OR OOS-06]). | No (core). The API is needed for per-release freshness (retention) and costs one endpoint. |
| M5 | **Advisory data sync.** Scheduled sync of licence-verified OSV records for the 8 ecosystems and of CISA KEV. Per-source sync status and last-success time shown in the product. Attribution for every source. | Core + Legal | F1, F2 [MV §2.0(b)]; licences [MV 14][MV 15][MV 19]; reachability [ENV-005][S3-C1][S3-C2] | No |
| M6 | **Matching engine and findings.** Deterministic purl + version-range matching. Re-run on every sync and every new SBOM. Each finding explained (source record, aliases, affected range, sync time). Severity shown as published by the source, never computed by us. | Core | F1 [MV §2.0(b)]; H-D2 | No |
| M7 | **Exploited-signal flag and alerts.** Findings whose aliases appear in CISA KEV are flagged "known exploited — triage required". Immediate email alert for new flagged findings; daily digest of other new findings; in-app notification list. | Core | F2; JTBD-F1. S3-C5 shows such events are rare but real, so alerts must be reliable. | No |
| M8 | **Triage decisions.** Status vocabulary aligned with VEX practice (under investigation / not affected with justification / affected / fixed in version); rationale; author and time; apply to matching findings in other versions and products | Core | F6; Art. 13(7) documentation [S3-C7]; H-D3 [MV 40] | No |
| M9 | **Art. 14 case and clocks.** Case types "actively exploited vulnerability" and "severe incident". Created from a finding **or manually**. Awareness time entered or confirmed by the user in UTC. Deadlines: 24h, 72h, final report (vulnerability: 14 days after the corrective measure is available; incident: one month after notification). Reminders before each deadline. Clock rules held as versioned configuration. | Core | Art. 14(2), (4) [MV 1]; JTBD-F2 | No: this is the legal core |
| M10 | **SRP stage drafts.** Per-stage field sets from the ENISA glossary (v1.3 at 25 Sep 2026), held as versioned configuration. Required/Optional validation per stage. Pre-fill from profile, product, version and finding. Copy per field; export (printable and JSON). Glossary version recorded. Submission time and SRP reference recorded by the user. | Core | F4; [MV 2][MV 3]; H-D4 | No |
| M11 | **Affected-user notice draft.** Template-based plain-language notice filled from case data; export as text or Markdown and JSON | Core (partial F5) | Art. 14(8) [MV 1]; Annex I Part II(4), (8) [S3-C7] | Yes in principle ("where appropriate"). Kept because it is a small template on existing data and completes the Art. 14 job. Full CSAF is POST-MVP (P1). |
| M12 | **Evidence record and exports.** Append-only event log per workspace: SBOM uploads (hash), sync runs (source, time), findings, decisions, case events, drafts, submissions recorded. Per-case evidence-pack export and per-version vulnerability status report (printable and JSON). | Core + Legal | F6; JTBD-F3; Art. 13(7), 13(13) [S3-C7]; charter rule 14 | No |
| M13 | **"Get an SBOM" guidance.** In-app help for S2 customers on generating CycloneDX or SPDX JSON with common free tooling, plus the supported formats and ecosystems | Activation | MV-O1-02; S2 friction [MV §2.0] | Yes, but activation would suffer. Static content, low cost. |
| M14 | **Subscription billing.** Provider-hosted checkout and customer portal. Plan state set only from verified provider events. Plan limits (number of monitored products) enforced on the server. | Commercial + Legal | Business model (§12); charter rules 9 and 12 | No (cannot charge) |
| M15 | **Legal, attribution and data-rights basics.** Terms, privacy notice, processor terms for B2B customers, a data-source attribution page (CC-BY and others), the non-endorsement and no-compliance-claim wording, full workspace data export, and account and workspace deletion | Legal | Charter rules 6, 10 and 15; CC-BY attribution [MV 14][MV 15]; RISK-003 | No |

Deliberately **not** in the MVP: integrations (GitHub App, Slack, Jira), CSAF and VEX export, EUVD and EU KEV, NVD, distro advisories, a disclosure intake portal, localisation, multi-workspace consultant views and SSO. See §10 and §11.

**MVP quality bar** (for Agents 4 and 16):
- Findings for the regression SBOMs must equal OSV's own results for the same purls and data snapshot.
- Every deadline rule must pass exhaustive boundary tests.
- Sync failures must be visible to customers and alert operators.
- No part of the MVP may show "compliant", "safe" or "no vulnerabilities" language (§14).

---

## 10. POST-MVP bucket

Ordered roughly by expected value. Each item passes "solves the validated problem" but fails "needed for MVP".

| ID | Item | Why post-MVP (anti-bloat reason) | Pre-condition / trigger |
|---|---|---|---|
| P1 | **CSAF 2.0 advisory export and VEX export** (CycloneDX VEX / OpenVEX) | Completes F5 and gives parity with CVD Portal and CRA Evidence [MV 24][MV 25]. Needs schema-valid product trees and schema validation. The MVP can launch with the M11 draft ("where appropriate", Art. 14(8)). | Activation met (G-V2); customer requests |
| P2 | **ENISA EUVD / EU KEV as data sources** | Would strengthen F2 for EU buyers. EUVD **terms are UNKNOWN** [MV 17][MV 18]. | Written confirmation from ENISA (HDP-7) and Legal sign-off |
| P3 | **More formats:** SPDX 3.0.1 JSON-LD, CycloneDX XML | BSI TR-03183-2 expects CycloneDX ≥1.6 or SPDX ≥3.0.1 [MV 9]. The MVP accepts CycloneDX 1.6 JSON already. | Measured upload failures by format |
| P4 | **More ecosystems and OS/distro advisories** | Widens the segment. Licence and share-alike questions (Ubuntu CC-BY-SA; converted data with no licence stated) [MV 14]. | Legal clearance; demand |
| P5 | **Integrations:** GitHub App SBOM pull, webhooks (Slack, Teams), issue-tracker links | Improves retention. The MVP has the upload API and email. | G-V2 met; customer requests |
| P6 | **Art. 13(6) upstream-report record and Annex I Part II(4) public advisory publishing** | These duties apply from 11 Dec 2027 [S3-C7]. Needed before then, not at launch. | Before Q3 2027 |
| P7 | **Coordinated-disclosure intake** (Annex I Part II(5)–(6) contact point) | A different job. CVD Portal offers a free intake tier [MV 24]. Adds public attack surface. | Demand evidence |
| P8 | **Pre-fill the Commission's Art. 33(5) simplified technical-documentation form** from product records | The form does not exist yet (UNKNOWN, future event) [MV §2.8 Q4] | Form published |
| P9 | **Consultant / multi-workspace view** | Channel hypothesis (consultants and integrators) is untested | Channel evidence (Agent 7) |
| P10 | **Support-period management and end-of-support notices** | Art. 13(8) support periods [OR 2]. The MVP stores the date only. | Customer requests |
| P11 | **Localisation** (e.g., DE, FR, IT) | The SRP is English-only at launch [MV 3]. Demand for other languages is UNKNOWN. | Market data |
| P12 | **Sample-SBOM sandbox for onboarding** (clearly labelled, processed by the real engine) | Activation experiment. Must not become demo behaviour (charter rule 7). | G-V2 shows activation shortfall |
| P13 | **SSO/SAML, advanced roles, custom retention** | Enterprise needs, not the ICP | Upmarket demand |

---

## 11. REJECTED / OUT OF SCOPE bucket

| ID | Item | Reason |
|---|---|---|
| R1 | Any AI or LLM feature: AI triage, summarisation, chat, "suggested decisions" | Charter absolute runtime rule (DECISION-007). Competitors' AI features are not matched. |
| R2 | Submitting to the ENISA SRP or CSIRTs on the customer's behalf; asking for or storing the customer's EU Login credentials | No API [MV 3]. The customer's Authorised Representative must submit with MFA [MV 3]. Storing their credentials would be a serious security and legal hazard. |
| R3 | Deciding legal questions: whether a vulnerability is "actively exploited", whether an incident is "severe", product class (important/critical), which CSIRT coordinates | Legal judgments [OR §3 O1 barriers; MV OOS-MV-08]. The product shows signals and records the customer's decision. |
| R4 | Binary or firmware SBOM generation and analysis | Not MVP-feasible [OR 38]; enterprise incumbents [MV §2.1 row 13]; ICP exclusion |
| R5 | Generating SBOMs from source code in-product, or shipping a downloadable CLI or agent | A downloadable component could itself be a CRA "product with digital elements" [OR OOS-06]. Free generators exist [MV 13][S3-C3]. |
| R6 | Code scanning (SAST, secrets, containers, DAST) and automatic remediation (PRs, upgrades) | A different job, in a crowded market [MV 31][MV 38] |
| R7 | Conformity assessment, CE marking, EU declaration of conformity, generic Annex VII template library | Legal-advice risk; a different job; free templates exist; the Art. 33(5) form will be free [MV §2.2][MV §2.8 Q4] |
| R8 | NVD CPE-based matching | CPE false positives [MV 40][OR 38]. Purl-first matching suits the segment. The NVD notice duty [MV 16] is avoided. Revisit only if measured purl coverage is poor (A-S04). |
| R9 | Compliance scores, "CRA compliant" badges, readiness percentages | Would imply certification. Charter rule 15; RISK-003. |
| R10 | Human services (PSIRT-as-a-service, 24×7 monitoring, legal advice) | Not software. Liability. Not deliverable by the business as configured. |
| R11 | Features for O2 (holiday pay) or O4 (pay transparency) | Candidates not chosen (§2.5) |
| R12 | Per-incident or per-case charges, or paywalling an open Art. 14 case | Charges the customer at the moment of legal distress; a dark-pattern risk (charter rule 15). See §12 guardrails. |

---

## 12. Business model direction
Prices, tiers, currency, trial length and discounts are **Agent 6's decisions**. This section sets the model direction and the constraints the strategy depends on.

**12.1 Model (DECISION direction).**
- Recurring B2B SaaS subscription, monthly and annual, self-serve through provider-hosted checkout.
- No sales-led enterprise motion at MVP.

**12.2 Unit of value: the monitored product (DECISION-006).**
- A monitored product is a product with digital elements as the manufacturer names it to the SRP, including all its versions on the market.
- Rationale:
  - It maps to the SRP's own "product name" / "product version or range" fields [MV 2].
  - It matches how the market prices: ConformOps per product [MV 22]; CVD Portal's Compliance tier includes 3 products, then €99/month for each additional product [MV 24]; Zealience per product [MV 29]; sbomify 5 products per plan [MV 27].
  - It grows with the customer's regulatory surface.
- Alternatives rejected:
  - **Per seat.** It discourages adding approvers and responders during a 24-hour window; the SRP allows up to 20 Secondary ARs [MV 3].
  - **Per component.** Unpredictable, and it penalises complete SBOMs.
  - **Per case.** See R12.
  - **Flat fee.** Does not scale with value.
- Acceptance is a HYPOTHESIS (A-S14).

**12.3 Strategic constraints for Agent 6:**
1. Every paid tier includes the whole core job (M4–M12), including **automated matching and KEV alerts**. This is H-D1. Gating it would copy the gap we exploit [MV 24].
2. No per-case or per-incident fees (R12).
3. **No lock-out during an open Art. 14 case.** If a trial ends or a subscription lapses while a case is open, the case, its clocks and its drafts stay usable until it is closed, and data export is always available. This is a charter rule 15 guardrail; details go to Agents 4 and 14.
4. Pricing must be published on the website. All SME-priced competitors publish theirs [MV §2.3].

**12.4 Free tier / trial: hypotheses for Agent 6 to test.**
- **HB-1:** a time-limited full-feature trial converts better than a free tier. Monitoring value appears within days, and a free tier would compete with free Dependency-Track on its home ground.
- **HB-2:** a permanent free tier of one product with limits is needed to win against free tools and the free previews offered by ConformOps (2 products) and CVD Portal [MV 22][MV 24].

Neither has evidence. Test both with V1-3 [MV §2.10].

**12.5 Grants.**
- SECURE-type grants offer "up to € 30.000" per SME [MV 12].
- Whether SaaS subscriptions are eligible costs is **UNKNOWN** (V1-8) [MV §2.10]. Agent 6 should check before relying on annual prepayment framed around grants.

**12.6 Cost-to-serve drivers (rough; for Agents 6, 9 and 17).**
- **Advisory data.** The 8 ecosystem exports total about 300 MB compressed; the npm export alone is 217 MB [S3-C2]. The sync design (incremental or full) drives bandwidth and compute. This is Architecture's choice. It is a largely **fixed** cost, independent of customer count.
- **Matching compute.** Scales with components × monitored versions × advisory changes.
- **Storage.** SBOM originals, findings and the append-only evidence log. Retention may run for years, because customers keep technical documentation for ≥10 years (Art. 13(13)) [S3-C7]. Our retention period is for Agents 4 and 14 to set.
- **Transactional email.** Alerts, digests, deadline reminders.
- **Payment-provider fees.**
- **Hosting.** Region to be set by Architecture/DevOps. EU data residency is a trust HYPOTHESIS (A-S10): competitors stress "EU hosted" and "hosted exclusively with European providers" [MV 24][MV 26].
- **Fixed people costs:**
  - SRP glossary and clock-rule updates (the glossary changed twice in September 2026 [MV 2]);
  - data-source monitoring;
  - onboarding support for S2 customers;
  - security operations.
- **No AI inference cost** (runtime prohibition).
- SUPPORTED INFERENCE: the cost base is mostly fixed, so viability depends on reaching a minimum number of paying products. Agent 6 should model break-even.

---

## 13. Measurable product success criteria
All targets below are **HYPOTHESES** set as starting thresholds. No benchmark evidence was available. They must be recalibrated after the first cohort, and the recalibration must be recorded.

Measurement:
- first-party, server-side product events stored in the application database, with timestamps and workspace IDs;
- provider webhooks for billing;
- no third-party tracking is needed for these metrics.

Any analytics provider is Architecture's choice. The privacy notice must reflect whatever is actually used (charter rule 10).

### 13.1 Metric definitions

| Area | Metric | Definition / measurement | Starting target (HYPOTHESIS) |
|---|---|---|---|
| Activation | **A1 Activation rate** | Share of new workspaces that, within 7 days of sign-up, have ≥1 product with ≥1 successfully parsed SBOM **and** have opened the findings view (events: `sbom.parsed`, `findings.viewed`) | ≥40% |
| Activation | **A2 Time to first findings** | Median minutes from sign-up to the first `findings.viewed` | ≤20 minutes for S1 workspaces |
| Activation | **A3 SBOM parse success** | Parsed uploads ÷ uploads that claim a supported format; every failure returns an actionable error | ≥95%; 100% actionable errors |
| Activation | **A4 purl coverage** | Median share of components per SBOM with a purl in a supported ecosystem | Observe only (feeds A-S04); no target |
| Retention | **R1 Monthly active paying workspaces** | Share of paying workspaces with ≥1 SBOM upload or triage decision in each 30-day window | ≥60% |
| Retention | **R2 SBOM freshness** | Share of monitored products with an SBOM uploaded in the last 90 days | ≥70% |
| Retention | **R3 Logo retention** | Share of paying workspaces still paying at months 3 and 12 | M3 ≥85%; M12 set after the first cohort |
| Retention | **R4 Flagged-finding triage** | Share of KEV-flagged findings with a triage decision within 72h of the alert | ≥80% |
| Conversion | **C1 Trial (or free) to paid** | Paid conversions ÷ trial or free starts, per cohort | ≥8% (recalibrate after 50 starts) |
| Conversion | **C2 Visitor to trial** | Trial starts ÷ unique pricing-page or landing-page visitors | Observe; set after 4 weeks |
| Conversion | **C3 Willingness-to-pay test** | Share of S1 respondents or fake-door visitors choosing a price at or above the lowest recurring anchor (€79/month for one product [MV 22]) | See G-V3 |
| Quality | **Q1 Advisory freshness** | Maximum age of the last successful sync per source, shown to customers | ≤24h; breach alerts operators |
| Quality | **Q2 Matching parity** | For the regression SBOM corpus, findings equal OSV API results for the same purls and snapshot | 100% (release gate) |
| Quality | **Q3 Deadline correctness** | Clock rule test suite (boundaries, UTC and local display, month arithmetic) | 100% pass (release gate) |
| Quality | **Q4 Alert latency** | Time from the sync that creates a KEV-flagged finding to the email being accepted by the email provider | ≤60 minutes |
| Quality | **Q5 Matching-error reports** | Triage decisions marked "not affected: component not present / match error" ÷ all decisions | Observe; investigate any rise |
| Outcome | **O1 Stages recorded before deadline** | Share of case stages whose customer-recorded SRP submission time is before the deadline | Observe. Self-reported, **not verifiable** by us; never marketed as a compliance rate. |

### 13.2 What these metrics do not prove
None of them proves that a customer is compliant or that a report was accepted by a CSIRT. O1 is self-reported.

### 13.3 Pre-scale validation gates (switch and stop conditions)
Thresholds are HYPOTHESES for the business owner to approve (HDP-6).

| Gate | When | Test | Pass → | Fail → |
|---|---|---|---|---|
| **G-V1** Demand signal | Before any paid acquisition spend | Landing page with a segmentation question (S1 / S2 / firmware) and pricing test V1-3 [MV §2.10] | Proceed to launch cohort | Revisit positioning and ICP; do not scale |
| **G-V2** Activation | After the first 30 workspaces | A1 and A2 against targets | Invest in P1/P5 | Fix onboarding (P12, M13); re-examine S2 share (V1-1) |
| **G-V3** Switch / stop (Agent 1's condition, applied literally) | After G-V1 and the first cohort, or 6 months after launch, whichever is earlier | Do S1 SMEs pay at or above the lowest recurring anchor (C3, C1)? | Continue O1 | Strategy review. Options, in order: (a) reposition within the CRA (e.g., consultant channel, P9); (b) switch to O2 **only if** its reopen conditions in §2.5 hold; (c) stop, with "no candidate viable" and a request for primary customer research |
| **G-V4** Differentiation watch | Quarterly | Re-check the published tiers of CVD Portal, CRA Evidence, ConformOps and Dependency-Track against F1–F6 | Continue | Re-position; accelerate P1/P5 |
| **G-V5** Regulatory watch | Monthly | ENISA SRP API, glossary versions, Art. 14(10) implementing act, Art. 33(5) form, EUVD terms | Continue | Update configuration; reassess M10's value if ENISA ships an API or drafting tool (MV-O1-08) |

---

## 14. What the product does NOT do
These statements must stay true in the product, the website and legal texts (Agents 4, 7, 12 and 14).
1. It does **not** certify, assess or guarantee compliance with the CRA or any law, and never displays a compliance score or badge.
2. It does **not** submit anything to ENISA's Single Reporting Platform or to any CSIRT. The SRP is the only submission channel. The customer's own Authorised Representative submits [MV 3].
3. It does **not** ask for, store or use the customer's EU Login or SRP credentials.
4. It does **not** decide whether a vulnerability is actively exploited, whether an incident is severe, the product's CRA class, the coordinating CSIRT, or the customer's main establishment. It shows signals and records the customer's decisions.
5. It does **not** give legal advice.
6. It does **not** guarantee that all vulnerabilities are found. Matching covers only the listed sources, ecosystems and formats, and depends on the accuracy of the customer's SBOM. Components it cannot check are listed as unchecked.
7. It does **not** treat absence from CISA KEV as proof that a vulnerability is not exploited. KEV is one signal, not the legal test [S3-C7].
8. It does **not** generate SBOMs, analyse binaries or firmware, or scan source code.
9. It does **not** fix vulnerabilities or change customer code.
10. It does **not** use AI, LLMs or agents at runtime.
11. It does **not** send notices to the customer's users. It drafts them for the customer to send.
12. It does **not** tell micro or small enterprises that they cannot be fined. The only relief is from fines for the 24h early-warning deadline [OR 3][MV OOS-MV-06].

---

## 15. Major assumptions

| ID | Statement | Label | Confidence | How to validate | Owner |
|---|---|---|---|---|---|
| A-S01 | S1 software SMEs will pay a recurring fee at or above the lowest recurring anchor (€79/month for one product) for the combined job | HYPOTHESIS (mixed signal [MV 8]; no traction data) | LOW | G-V1 / G-V3 pricing test (V1-3) | Agent 6 (with Agent 7) |
| A-S02 | The S1 share among CRA-relevant software-product SMEs is large enough to sustain the business | UNKNOWN (whole-sample proxy only [MV-U01]) | — | Landing-page segmentation question; screener (V1-1) | Agent 7 |
| A-S03 | Continuous monitoring plus the evidence record creates monthly value even though Art. 14 events are rare | HYPOTHESIS (S3-C5 shows rarity; MV-O1-04) | LOW–MEDIUM | R1, R2, R3 | Agent 3 (review at G-V3) |
| A-S04 | Most components in ICP SBOMs carry purls in supported ecosystems | ASSUMPTION (51/51 and 52/52 in the `npm sbom` probe [S3-C3]; other generators unmeasured) | MEDIUM | A4 metric; regression corpus from 3+ generators | Agent 4 / Agent 16 |
| A-S05 | The selected OSV sources and CISA KEV can be used commercially with attribution | VERIFIED for GHSA, PyPA, Go (CC-BY 4.0), RustSec (CC0), KEV (CC0) [MV 14][MV 15][MV 19]; per-record source filtering is a design duty | HIGH | Legal review of the attribution text | Agent 14 / Agent 9 |
| A-S06 | EUVD data can be reused commercially | UNKNOWN [MV 17][MV 18] | — | Written ENISA confirmation (V1-6) | Agent 14 (HDP-7) |
| A-S07 | CISA KEV is an acceptable exploited signal for EU manufacturers while EU KEV is unavailable | ASSUMPTION (KEV is US-centric and incomplete; legal test is the manufacturer's evidence [S3-C7]) | MEDIUM | Interviews; P2 once EUVD is cleared | Agent 4 / Agent 14 |
| A-S08 | ICP buyers accept an English-only product | ASSUMPTION (SRP English-only at launch [MV 3]) | MEDIUM | Landing-page language question; support requests | Agent 7 |
| A-S09 | Buyers value "deterministic / no AI" | ASSUMPTION [MV-O1-07] | LOW | A/B test of the positioning line | Agent 7 |
| A-S10 | EU hosting, a security page and MFA are prerequisites for conversion | HYPOTHESIS (competitor emphasis [MV 24][MV 26]; V1-7) | MEDIUM | Interviews; A/B test of the security page | Agent 7 / Agent 13 / Agent 9 |
| A-S11 | ENISA will not ship, within 12 months, a free API or drafting tool that removes the value of M10 | UNKNOWN (future event; "may be considered" [MV 3]; MV-O1-08) | — | G-V5 monitoring | Agent 3 |
| A-S12 | Glossary and clock-rule changes can be absorbed by versioned configuration updates within days | ASSUMPTION | MEDIUM | Architecture design review; drill after the first glossary change | Agent 9 / Agent 17 |
| A-S13 | Small and medium firms (10–249 staff) are a better ICP than micro firms | HYPOTHESIS (fine relief for micro and small applies to the 24h deadline only [OR 3]) | LOW | Segment-level conversion in C1 and C3 | Agent 6 / Agent 7 |
| A-S14 | "Monitored product" is an understood and accepted unit of value | HYPOTHESIS (competitor precedent [MV 22][MV 24][MV 29]) | MEDIUM | Pricing test; support questions | Agent 6 |
| A-S15 | SME grants can pay for SaaS subscriptions | UNKNOWN (V1-8) | — | SECURE eligible-cost rules | Agent 6 |
| A-S16 | ICP buyers buy self-serve by card without procurement | ASSUMPTION | MEDIUM | Checkout funnel data; lost-deal reasons | Agent 6 |
| A-S17 | The CRA's core Art. 14 and Annex I obligations are not postponed or materially reduced before 2028 | UNKNOWN (future event); no postponement found in the approved research [OR §1.3] | — | G-V5 | Agent 3 |

---

## 16. Major risks

| ID | Risk | Probability | Impact | Mitigation | Owner |
|---|---|---|---|---|---|
| R-01 | **No paying demand.** Willingness to pay is mixed; free substitutes are strong; no vendor shows traction [MV 8][MV 39][MV §2.1]. (Registry RISK-001) | HIGH | HIGH | Small MVP; G-V1 before spend; G-V3 switch or stop; published pricing tests | Agent 3 / Agent 6 / Agent 7 |
| R-02 | **Differentiation erodes.** CVD Portal moves automated alerts down-tier; CRA Evidence publishes an SME price; Dependency-Track adds Art. 14 features [J2 §4.3][MV 24][MV 25][MV 39] | MEDIUM–HIGH | HIGH | Compete on the complete job, coverage transparency, decision reuse and update speed; G-V4 quarterly watch; P1/P5 roadmap | Agent 3 / Agent 7 |
| R-03 | **Commoditisation by public tools.** ENISA API or drafting tools; the free Art. 33(5) form [MV 3][MV §2.8 Q4] | MEDIUM | HIGH | Core value is monitoring plus record, not drafting alone; integrate an ENISA API if it ships (G-V5) | Agent 3 |
| R-04 | **Liability and misreading.** A missed match, a wrong deadline, or output read as a compliance guarantee (registry RISK-003) | MEDIUM | HIGH | Coverage summary; sync freshness shown; human decides all legal triggers; Q2 and Q3 release gates; §14 statements in the product and terms; no compliance language (R9) | Agent 14 / Agent 7 / Agent 16 |
| R-05 | **Episodic value leads to churn.** Exploited-package events are rare [S3-C5] | MEDIUM | HIGH | Daily monitoring of all advisories; CI uploads; status reports; Annex I duties from Dec 2027; R1–R3 metrics | Agent 3 / Agent 6 |
| R-06 | **Regulatory and schema churn.** Glossary v1.1→v1.3 in three weeks; possible Art. 14(10) implementing act [MV 1][MV 2] (registry RISK-002) | MEDIUM | MEDIUM | Glossary and clock rules as versioned configuration; version recorded on each draft; G-V5 monitoring; update runbook | Agent 9 / Agent 17 |
| R-07 | **Data-source dependency.** OSV or KEV outage, format change or licence change | LOW | HIGH | Keep the last good snapshot; show staleness to customers (Q1); operator alerts; attribution kept current | Agent 9 / Agent 17 / Agent 14 |
| R-08 | **Security breach of highly sensitive data.** Unpatched, exploited-vulnerability details per customer | MEDIUM | HIGH | MFA; least-privilege roles; upload-only tokens; server-side authorisation; encryption; security review before launch | Agent 13 |
| R-09 | **Onboarding friction (S2) and small segment** [MV §2.0] | MEDIUM | MEDIUM–HIGH | M13 guidance; upload API; A1/A2 tracking; G-V2 | Agent 8 / Agent 7 |
| R-10 | **Trust barrier for a new vendor** in a security-adjacent category [MV §2.7] | MEDIUM | HIGH | Accurate security page without unverified claims (charter rule 15); clear data handling; EU hosting direction (A-S10) | Agent 7 / Agent 13 / Agent 14 |
| R-11 | **Owner-supplied launch values missing** (legal entity, country, contacts) [BUSINESS_CONFIG] | HIGH | HIGH | Explicit placeholders; launch blocked until supplied | Business owner / Orchestrator |
| R-12 | **Payments and email not verifiable end to end in this session.** No Stripe keys; no SMTP credentials [ENV-007][ENV-008]. | HIGH | MEDIUM | Build against provider test modes and local capture; mark as release blockers until verified with real credentials | Agent 17 / Agent 16 |
| R-13 | **Acquisition difficulty with technical buyers** [MV §2.7] | HIGH | MEDIUM | Developer-channel content, webinars and national-authority-aligned education [MV 8][MV 10]; accurate, citation-backed content | Agent 7 |
| R-14 | **Support expectations outside business hours.** Clocks run 24/7; the business may not | MEDIUM | MEDIUM | No 24/7 support claims; the product works without support; owner decides support hours (HDP-5) | Business owner / Agent 14 |

---

## 17. Proposed decisions for the registry
Numbering assumes the registry is empty (`DECISIONS.md` has no entries). The Orchestrator may renumber.

```
DECISION-001
Title: Chosen opportunity
Decision: Build O1, an EU Cyber Resilience Act vulnerability-handling, Art. 14 reporting-clock and evidence workspace for EU-market software-product SMEs whose builds can export CycloneDX/SPDX SBOMs. O2 and O4 are not pursued (O2 named fallback under gate G-V3; O4 watchlist). Confidence LOW–MEDIUM; demand unproven.
Owner: SaaS Strategy Agent
Evidence: product-strategy-v1 §1, §2.2–§2.5; [OR 2][OR 23][MV §2.0(b)][MV §2.1a][MV §3.0(b)][MV §6][J2 §4.1–§4.3][S3-C2–C5][S3-C7]
Status: PROPOSED
```

```
DECISION-002
Title: Target customer (ICP)
Decision: Primary ICP = manufacturers (CRA sense) of software products, or of connected devices with package-managed application layers, placing products on the EU market; 10–249 staff (micro firms secondary); 1–20 products; builds in npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems or Packagist; can export CycloneDX/SPDX JSON (S1 core, S2 served with guidance); no dedicated PSIRT. Buyer: CTO / Head of Engineering. User: lead engineer / security champion. Approver: managing director (and counsel where present). Excluded: firmware/embedded needing binary analysis, pure SaaS out of CRA scope, enterprises with PSIRT platforms, OS/container-package-centric products.
Owner: SaaS Strategy Agent
Evidence: §4.2–§4.3; [MV §2.0 recommended segment][OR 27][OR 3][OR 23][OR 34][OR 38][MV 8][MV 13][S3-C3]
Status: PROPOSED
```

```
DECISION-003
Title: Primary target market and jurisdiction
Decision: PRIMARY_TARGET_MARKET = EU single market (27 Member States; EU CRA jurisdiction), English-language, self-serve, starting with EU-established SMEs. ADDITIONAL_TARGET_MARKETS = non-EU manufacturers making products available on the EU market (same product). EEA applicability not claimed (UNKNOWN).
Owner: SaaS Strategy Agent
Evidence: §4.1; [OR 2][S3-C7][MV 3][MV 8]
Status: PROPOSED
```

```
DECISION-004
Title: Customer type
Decision: CUSTOMER_TYPE = B2B only. No consumer offering; sign-up is for businesses acting as manufacturers.
Owner: SaaS Strategy Agent
Evidence: §4.1; the obligation falls on manufacturers [MV 1][S3-C7]
Status: PROPOSED
```

```
DECISION-005
Title: MVP scope boundary
Decision: MVP = features M1–M15 in product-strategy-v1 §9 and nothing else. Inputs CycloneDX JSON 1.4–1.6 and SPDX JSON 2.2–2.3; ecosystems npm, PyPI, Maven, Go, crates.io, NuGet, RubyGems, Packagist (purl matching); advisory data = OSV records from licence-verified sources plus CISA KEV; English only. Everything in §10 is POST-MVP and everything in §11 is REJECTED. Adding to MVP requires a change request routed by the Orchestrator.
Owner: SaaS Strategy Agent
Evidence: §9–§11; [MV §2.0(b)][MV 1][MV 2][MV 3][MV 14][MV 15][MV 19][ENV-005][S3-C1–C4]
Status: PROPOSED
```

```
DECISION-006
Title: Core unit of value
Decision: The billable unit of value is the "monitored product" (a product with digital elements as named to the ENISA SRP, including all its versions on the market). Every paid tier includes the full core job (M4–M12), including automated matching and KEV alerts; no per-seat pricing, no per-case/per-incident charges; no lock-out of an open Art. 14 case. Prices, tiers, trial/free-tier choice: Agent 6.
Owner: SaaS Strategy Agent
Evidence: §12; [MV 2][MV 22][MV 24][MV 27][MV 29][MV 3]
Status: PROPOSED
```

```
DECISION-007
Title: Runtime AI prohibition reaffirmed
Decision: The product has no AI, LLM, ML-inference or agent dependency at runtime: no AI triage, summarisation, chat, suggested decisions or generated text. All matching, clocks, validation and document assembly are deterministic and reproducible from inputs and recorded data snapshots. Competitors' AI features are deliberately not matched.
Owner: SaaS Strategy Agent
Evidence: AGENT_CHARTER "Absolute runtime rule"; §6.3, §11 R1; [MV 22][MV 24][MV-O1-07]
Status: PROPOSED
```

```
DECISION-008
Title: Decision support, not compliance or submission
Decision: The product never submits to the SRP/CSIRTs, never stores EU Login credentials, never makes legal determinations (actively exploited, severe, product class, coordinating CSIRT, main establishment), never displays compliance scores or claims, and never gives legal advice. The customer decides; the product records, computes deadlines and prepares drafts.
Owner: SaaS Strategy Agent
Evidence: §14, §11 R2/R3/R9; [MV 3][MV OOS-MV-08][OR OOS-01]; registry RISK-003
Status: PROPOSED
```

```
DECISION-009
Title: Vulnerability data sources limited to licence-verified sources
Decision: MVP uses only OSV records whose originating source licence is verified for commercial reuse (e.g., GHSA/PyPA/Go CC-BY 4.0, RustSec CC0) with attribution, and CISA KEV (CC0). EUVD/ENISA EU KEV, NVD, and distro advisories (Ubuntu CC-BY-SA; unlicensed converted data) are excluded until Legal clears them.
Owner: SaaS Strategy Agent
Evidence: §9 boundary; [MV 14][MV 15][MV 16][MV 17][MV 18][MV 19][S3-C1][S3-C2]
Status: PROPOSED
```

```
DECISION-010
Title: No downloadable components
Decision: The MVP ships no downloadable CLI, agent, plugin or GitHub Action; CI integration is an authenticated HTTP upload endpoint only. Reason: a downloadable component could itself be a CRA "product with digital elements".
Owner: SaaS Strategy Agent
Evidence: [OR OOS-06][OR 23][OR 34]; §11 R5
Status: PROPOSED
```

```
DECISION-011
Title: Pre-scale validation gates and switch/stop conditions
Decision: Adopt gates G-V1 to G-V5 (§13.3). Agent 1's switch condition is applied literally as G-V3 against the lowest recurring anchor; failure triggers a Strategy review with options reposition / switch to O2 (only if its §2.5 reopen conditions hold) / stop.
Owner: SaaS Strategy Agent
Evidence: [OR §5.3][J1 §4.2][J2 §4.1][MV §2.10]; registry RISK-001
Status: PROPOSED
```

---

## 18. Human decision points (business owner must confirm)

| ID | Decision needed | Why it matters | Default if unanswered |
|---|---|---|---|
| HDP-1 | Confirm the choice of O1 and accept that demand is **unproven**; approve the validation gates and their thresholds (§13.3) | The choice is a judgement between close candidates [J2 §4.1] | Build proceeds; no paid acquisition before G-V1 |
| HDP-2 | Approve a brand name. "Keelwatch" is a placeholder: trademark, domain and company-name checks are not done. | Public use needs clearance | Placeholder only in internal artifacts |
| HDP-3 | Supply `BUSINESS_LEGAL_NAME`, `BUSINESS_COUNTRY`, entity type and contacts (BUSINESS_CONFIG). Consider that an EU establishment and EU hosting may affect buyer trust (A-S10, HYPOTHESIS). Legal implications of a non-EU business (e.g., data-protection representation) are for Agent 14 to advise; nothing is asserted here. | Launch blocker; governing law; trust | Launch blocked |
| HDP-4 | Confirm the primary market: EU-wide English-first (proposed), or a single-country start | Marketing focus; language | EU-wide English |
| HDP-5 | Decide support hours and response commitments | Art. 14 clocks run at weekends; no 24/7 claim will be made without approval (R-14) | Business-hours email support; no 24/7 claim |
| HDP-6 | Approve a budget and timeline for validation (landing page, pricing test, 10–15 interviews V1-2/V1-3) | G-V1/G-V3 need evidence the build cannot create | Minimal self-run landing-page test |
| HDP-7 | Decide whether to request written confirmation from ENISA on EUVD reuse | Unblocks P2 (EU KEV) | EUVD stays excluded |
| HDP-8 | Decide the liability posture with Legal (e.g., whether to seek professional-indemnity cover; limitation clauses) | Security-adjacent product (R-04) | Agent 14 drafts standard limitation terms for review |
| HDP-9 | Later: approve prices (Agent 6) and hosting region/cost (Agents 9 and 17) | Commercial and trust effects | — |
| HDP-10 | Decide whether "no AI" appears in public messaging | Positioning untested (A-S09) | Stated only as a factual property, not a headline |

---

## 19. Out-of-scope findings (reported to the Orchestrator)

| ID | Finding | Responsible agent |
|---|---|---|
| OOS-S01 | Clock semantics need precise definitions: awareness time in UTC; "one month after notification" for incidents (calendar-month arithmetic, month-end cases); 14 days after the corrective measure; intermediate reports on CSIRT request (Art. 14(6)). They need legal review of the interpretation, and should be held as versioned configuration. | Agent 4; Agent 14; Agent 9 |
| OOS-S02 | The SRP glossary must be modelled as versioned data (v1.3, 25 Sep 2026), with per-stage Required/Optional rules and the version stamped on every draft [MV OOS-MV-02]. A glossary-update runbook is needed. | Agent 9; Agent 4; Agent 17 |
| OOS-S03 | Attribution and terms: CC-BY 4.0 attribution for GHSA/PyPA/Go-derived data, CC0 sources acknowledged as good practice, and per-record source filtering so that unlicensed or share-alike data is never ingested. If NVD is ever used, its exact non-endorsement notice is required [MV 16]. EUVD needs written confirmation [MV OOS-MV-03]. | Agent 14; Agent 9 |
| OOS-S04 | Security: the product stores details of unpatched, exploited vulnerabilities. It needs MFA, upload-only scoped API tokens and strict tenant isolation, and it must never request SRP/EU Login credentials. Free-text incident fields may contain personal data (DPIA question). | Agent 13; Agent 14; Agent 10 |
| OOS-S05 | Copy precision: no "compliant", "guarantee" or "no vulnerabilities" language. Fine relief applies only to micro and small firms and only to the 24h early warning [MV OOS-MV-06]. ENISA survey figures are CC BY 4.0 and need attribution [OR OOS-10]. Competitor comparisons must be re-verified before public use [MV §9]. KEV must never be presented as the legal test. | Agent 7; Agent 14 |
| OOS-S06 | ENVIRONMENT_FACTS candidates from S3-C1 to S3-C6: CISA KEV reachable; OSV bulk exports reachable (sizes); `npm sbom` produces CycloneDX 1.5 and SPDX 2.3 with purls; OSV `querybatch` end-to-end match; GOV.UK bank holidays reachable. Agent 3 has not edited the file. | Orchestrator |
| OOS-S07 | Test corpus: build regression SBOMs from ≥3 generators (e.g., `npm sbom`, GitHub SPDX export, one CycloneDX tool) and pin data snapshots so matching parity with OSV (Q2) is reproducible. Clock tests must cover boundaries and time zones (Q3). | Agent 16; Agent 11 |
| OOS-S08 | UI must separate what the system computed (matches, deadlines) from what the customer decided (awareness, exploited, severe, triage). Countdowns must not rely on colour alone (WCAG 2.2 AA), and deadlines must be shown in UTC and local time. | Agent 8; Agent 15; Agent 12 |
| OOS-S09 | Registry updates on approval: set `PRIMARY_TARGET_MARKET`, `ADDITIONAL_TARGET_MARKETS` and `CUSTOMER_TYPE` in BUSINESS_CONFIG from DECISION-003/004; import A-S01 to A-S17 and R-01 to R-14 (mapping R-01 → RISK-001, R-04 → RISK-003, R-06 → RISK-002). | Orchestrator |
| OOS-S10 | Operations: advisory-sync freshness (Q1) and alert latency (Q4) are production SLOs with operator alerting. Monthly monitoring of ENISA SRP pages is a standing task (G-V5). | Agent 17 |
| OOS-S11 | Our own SaaS: dogfooding is optional but useful. Generate our own SBOM and monitor it with the product. We ship no downloadable component (DECISION-010), so the SaaS is expected to stay generally outside CRA scope [OR 23][OR 34]. Legal to confirm. | Agent 17; Agent 14 |
| OOS-S12 | Open research items that remain relevant: V1-1 (S1 share), V1-2 (exploited-event frequency; S3-C5 is a partial proxy), V1-3 (willingness to pay), V1-5 (competitor traction), V1-6 (EUVD), V1-7 (trust), V1-8 (grants) [MV §2.10]. O4-specific open items (J2-009; OOS-MV-01; re-reads [72][73][86][94]) are no longer decision-relevant. | Orchestrator; Agent 6; Agent 7 |
| OOS-S13 | Trial and cancellation behaviour must implement "no lock-out during an open Art. 14 case" and "export always available" (§12.3), and must be reflected in the terms. | Agent 4; Agent 6; Agent 14 |

---

## 20. Evidence gaps stated plainly
The weakest evidence points, together:
- No paying traction is known for any CRA SME tool.
- Willingness to pay is mixed.
- The S1 segment size is unknown.
- Exploited-package events are rare at catalogue level.

The decision therefore rests on four things:
- the legal durability and consequence of the CRA obligation;
- the feasibility of building and testing the product for real here;
- higher price anchors than the alternative;
- the weakness of the alternatives.

It does **not** rest on demonstrated demand. Gates G-V1 to G-V3 are how that gap gets closed.
