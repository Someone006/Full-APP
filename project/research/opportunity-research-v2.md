# SaaS Opportunity Research — v2

| Field | Value |
|---|---|
| Artifact | `project/research/opportunity-research-v2.md` |
| Supersedes | `project/research/opportunity-research-v1.md` (frozen; judged FAIL by Judge 1, `project/judges/judge-01-opportunity-research-v1.md`) |
| Owner | Agent 1 — SaaS Opportunity Researcher |
| Research date | 2026-09-26. All "status" statements are as of this date unless a source date is given. |
| Status | DRAFT v2 — resubmitted for independent judging |
| Scope of this artifact | Proposes and ranks opportunity areas for market validation. It does **not** choose the product or set strategy, pricing or requirements. Those belong to Agents 2, 3, 4 and 6. |

**What changed from v1 (one paragraph; details in §9 Revision log).** O3 (Awaab's Law) is demoted from Rank 3 to the watchlist. Its legal scope excludes licence-occupied housing, including almshouses. The small-provider universe is materially smaller than v1 stated. Live tools priced for small providers already exist. O4 (EU Pay Transparency) moves from Rank 4 to Rank 3 and stays conditional. O1 (CRA) keeps Rank 1, but only for software-product SMEs whose builds already produce SBOMs. Firmware and embedded makers that need binary analysis are marked "not MVP-feasible". O2's pain evidence has been rewritten. The v1 figures measured leave denial, not calculation errors. The primary government consultation, which does address calculation errors, is now cited. O2's scope is corrected to Great Britain. Key legal facts were re-verified against Official Journal texts obtained from the EU Publications Office. Every field is now completed for every examined area.

### Evidence labels (charter set only)

| Label | Meaning here |
|---|---|
| **VERIFIED [n]** | Stated by the cited source(s). §7 records for every source whether it was **Read** (fetched and read in this session, including PDFs extracted locally) or seen only as a **Snippet** (search-result summary). A snippet-only claim is VERIFIED only if at least two independent snippets agree. Otherwise it is labelled UNKNOWN or SUPPORTED INFERENCE. Grades in §7: **P** = primary/official, **S** = reputable secondary (law firm, professional body, parliamentary research service, trade press), **V** = vendor page, which only shows what a vendor *claims*. V sources never verify a legal fact. |
| **SUPPORTED INFERENCE** | My reasoning from verified facts. The reasoning is stated. |
| **ASSUMPTION** | Taken as true without evidence; must be tested. |
| **HYPOTHESIS** | Testable proposition, usually about customers or demand. |
| **PREDICTION** | Statement about the future. |
| **UNKNOWN** | Not established. |

There are no numerical market scores and no invented market sizes. Every number is attributed to a source, and the source's date is given wherever the source states one. A number derived by arithmetic is labelled SUPPORTED INFERENCE.

---

## 1. Scope & method

### 1.1 Objective and filters
The aim is to recommend 2–4 opportunities for market validation. Each one is a SaaS product that:
1. **Hard filter — AI-free runtime.** Its core value is delivered deterministically (database, rules or calculation engines, scheduled jobs, search, forms, documents, email, payments), with no LLM or generative-AI dependency at runtime (Agent Charter).
2. **Hard filter — MVP feasibility.** A small team can build a production-quality MVP in a few weeks as one web app with Postgres, payments and email. The filter fails if the core value needs any of: prior certification or accreditation, hardware, binary or firmware analysis engines, deep write-integrations with banks, payroll or government systems, or regulated identity verification.
3. **Soft criteria (qualitative, no scores).** (a) Obligation certainty and timing. (b) Consequence of inaction. (c) Evidence that the segment is underserved. (d) Willingness-to-pay signals. (e) MVP fit. (f) Legal risk of the product being wrong. (g) Durability over a 3–5 year horizon, to about 2029–2031.

### 1.2 Areas searched
- **EU:** Pay Transparency Directive 2023/970; e-invoicing (DE, BE, FR, PL, ES Verifactu); European Accessibility Act; NIS2 (Germany); DORA register of information; AI Act and the Digital Omnibus on AI; CSRD and Omnibus I with the voluntary SME standard; Whistleblowing Directive; Cyber Resilience Act; EUDR; PPWR and packaging EPR; Short-Term Rental Regulation; F-gas Regulation; Spain's digital time-recording decree.
- **UK:** Employment Rights Act 2025 (holiday-record duty, Fair Work Agency, tipping); Renters' Rights Act 2025 and the PRS database; Making Tax Digital for Income Tax; Awaab's Law; Martyn's Law; UK e-invoicing 2029.
- **US:** FSMA 204 food traceability; state pay-transparency laws; state privacy laws.
- **Non-regulatory:** field service and trades; allied-health clinic practice management; construction certificate-of-insurance (COI) tracking; UK landlord self-management; hospitality tip allocation.

Representative queries include "EU Pay Transparency Directive transposition status 2026", "Cyber Resilience Act reporting obligations 11 September 2026", "ENISA SME CRA survey", "Employment Rights Act 2025 holiday records six years", "holiday pay compliance and enforcement consultation 2026", "Awaab's Law licence almshouse", "Rentalize housing management Awaab's Law", "FDA food traceability July 20 2028", "Digital Omnibus AI Act Official Journal", "Martyn's Law myth buster", "PPWR 12 August 2026", "OSV data licence", "SBOM generation C/C++ firmware". Competitor-landscape queries were run for every area.

### 1.3 Method
- Web search to map each area, then direct reading of primary sources.
- **EU legal texts** were read as Official Journal XHTML from the EU Publications Office (`publications.europa.eu/resource/celex/<CELEX>`, which serves the same OJ text as EUR-Lex). EUR-Lex itself returned empty responses in this environment. Texts read: 2023/970, 2024/2847 and its 2 Jul 2025 corrigendum, 2019/882, 2025/40, 2024/1028, 2025/2650, 2026/470, 2026/1744, 2019/1937 and 2024/573.
- **UK legislation** was read on legislation.gov.uk (ERA 2025 s.35).
- **PDFs extracted and read locally:** DBT holiday-pay consultation (30 Jun 2026), ENISA SME CRA Survey Report (24 Jun 2026) and the Home Office Martyn's Law myth buster.
- **Data files analysed:** the RSH register of providers (17 Sep 2026 xlsx) and ONS EMP17 (18 Aug 2026 xlsx).
- Every regulation was checked for 2025–2026 postponements and amendments (§3 per area).
- Competitors were found by searching for them. The lists are **not exhaustive**, and failing to find a competitor is never treated as proof that none exists.

### 1.4 Limitations
- **No primary customer research.** There were no interviews, surveys or pricing tests. Segment-demand statements are HYPOTHESES for Agent 2.
- **Web pages were read through a summarising fetch tool.** For load-bearing EU and UK legal facts, v2 read the legal text itself, as listed in §1.3.
- **Unreadable sources:** House of Commons Library (HTTP 403), Almshouse Association parliamentary evidence (403), Made Tech (403), and one Xero ideas page (404).
- National-language sources (DE/FR/ES/IT/PL) were only sampled.
- Vendor pages are self-descriptions.

---

## 2. Opportunity landscape

The verdicts below are SUPPORTED INFERENCE from §3. "AI-free?" asks whether the core value can be delivered deterministically; competitive handicaps are recorded separately. "MVP?" asks whether the product is feasible as one web app with Postgres, payments and email within a few weeks.

| # | Area | Driver & status (2026-09-26) | Who has the problem | Competition found | AI-free? | MVP? | Verdict |
|---|---|---|---|---|---|---|---|
| O1 | **EU Cyber Resilience Act: SBOM-based vulnerability-handling, reporting-clock and evidence workspace** | Reg. (EU) 2024/2847. Art. 14 reporting applies from **11 Sep 2026**, including products already on the market. Main obligations from **11 Dec 2027** [2][21][22] | SMEs that make software products or components sold in the EU. Connected-hardware makers only where their builds already emit SBOMs | Emerging and fragmented: ConformOps (from €99/product), Article 14 Ready (€79), CVD Portal, ONEKEY, Anchore, Finite State, free OWASP Dependency-Track and others [30][31][32] | Yes | **Conditional.** Yes for customers who can supply CycloneDX/SPDX SBOMs. No where SBOMs must be generated from binaries or firmware | **Recommend #1** (segment-conditional) |
| O2 | **Great Britain holiday-record & holiday-pay assurance for variable-hours employers** | Duty to keep adequate holiday records for 6 years under WTR 1998 reg. 16B (ERA 2025 s.35), a criminal offence, in force **6 Apr 2026**. The FWA intends to start holiday-pay enforcement in **April 2027** [12][41][42] | GB employers with irregular-hours or variable-pay staff, and their payroll bureaus | Crowded in leave tracking. A calculation add-on exists (paiyroll, 15p/payslip, min £30/month) [48][50] | Yes | Yes | **Recommend #2** |
| O4 | **EU Pay Transparency compliance for SME / lower-mid-market employers in transposed states** | Dir. 2023/970, deadline 7 Jun 2026. Morgan Lewis lists IT, SK, LT, MT as implemented on time. Others treat MT and PL as partial and only IT as fully transposed. DE, FR, ES and IE are still at draft or earlier [1][13][14][15] | Employers with 100–249 workers (reporting); all employers for Arts. 5 and 7 | Crowded: Figures, Ravio, Personio, Sysarb, Trusaic, Syndio, PayAnalytics, beqom, Axios Analytics, TracefyHR [19][20] | Yes | Yes (one jurisdiction) | **Recommend #3** (conditional) |
| O3 | Awaab's Law case & statutory-clock management for small social landlords | In force 27 Oct 2025; Phase 2 on **30 Nov 2026**; Phase 3 date unconfirmed. Applies to social housing let on a **tenancy**. Excludes licences (e.g., almshouses), shared ownership and long leases [51][52][53] | Small private registered providers that let on tenancies and manage repairs in-house. Upper bound ~835–990 (derived); true count UNKNOWN [55][56] | Rentalize Core (50–5,000 homes, from €199/month), PyramidG2, HousingSurvey Pro (free sign-up), HazardClock (pre-launch), Weightmans, Netcall, Propsys360, Plentific [58]–[61] | Yes | Yes | **Watchlist** (was Rank 3) |
| O5 | US FSMA 204 food traceability | Not enforced before **20 Jul 2028**; FDA told to consider flexibilities [63][64] | >323,000 US businesses / >484,100 establishments (FDA estimate) [64] | ReposiTrak, iFoodDS, Trustwell, FoodReady, Inecta, Nulogy [65] | Yes | Yes | Watchlist |
| O6 | UK Martyn's Law | Expected in force spring 2027 [66]. Home Office: compliance intended "without needing to buy specialist services" [67] | Premises with 200+ capacity | Many low-price tools [68] | Yes | Yes | Reject (enhanced tier on watchlist) |
| O7 | EU/UK e-invoicing mandates | BE Jan 2026; PL 2026–27; FR Sep 2026/27; DE 2027/28; ES Verifactu 2027; UK Apr 2029 [69]–[73] | VAT-registered B2B businesses | Very crowded; ~137+ French approved platforms [70] | Yes | No (platform approval / Peppol access) | Reject |
| O8 | European Accessibility Act | Applies from 28 Jun 2025; micro-enterprise service providers exempt [4] | E-commerce, banking, e-books, transport ticketing | Very crowded [74] | Yes | Partly | Reject |
| O9 | NIS2 | DE law in force 6 Dec 2025; BSI registration due 6 Mar 2026 [75] | Essential/important entities | Very crowded GRC tools | Yes | Partly | Reject |
| O10 | DORA register of information | Annual submissions (e.g., CSSF window 11 Feb–31 Mar 2026) [76] | EU financial entities | GRC suites + specialist register tools [76] | Yes | Yes | Reject |
| O11 | EU AI Act deployer obligations | Reg. (EU) 2026/1744: Annex III high-risk moved to 2 Dec 2027, Annex I to 2 Aug 2028; Art. 4 softened [9] | AI deployers | Crowded AI-governance tools [78] | Yes | Yes | Reject |
| O12 | CSRD / voluntary SME standard | Dir. (EU) 2026/470: >1,000 employees and >€450m; value-chain cap [8]. Voluntary-standard delegated act adopted 3 Jul 2026 [79] | SME suppliers asked for ESG data | Crowded [80] | Yes | Yes | Reject |
| O13 | Whistleblowing channels | Dir. 2019/1937: private entities with 50+ workers [10] | Employers with 50+ workers | Commoditised; from ~€19/month [81] | Yes | Yes | Reject |
| O14 | EUDR | Reg. (EU) 2025/2650: 30 Dec 2026 (general), 30 Jun 2027 (micro/small) [7] | Operators/traders of in-scope commodities | Crowded | Yes | Partly | Reject |
| O15 | PPWR / multi-country packaging EPR | Reg. (EU) 2025/40 applies 12 Aug 2026; national producer registers; labelling from 12 Aug 2028 at the earliest [5] | Cross-border sellers and producers | Crowded new entrants and compliance schemes [84] | Yes | Partly | Reject |
| O16 | EU Short-Term Rental Regulation | Reg. (EU) 2024/1028 applies 20 May 2026 [6] | STR hosts and managers | Channel managers, guest-registration tools [85] | Yes | Yes | Reject |
| O17 | UK landlord compliance (Renters' Rights Act, PRS database, MTD ITSA) | Tenancy reform 1 May 2026; PRS database from 15 Dec 2026 at £65/property/year [86][88]; MTD from Apr 2026 [91] | Private landlords in England | Saturated incl. free tools [90] | Yes | Yes | Reject |
| O18 | UK tipping | Tips Act since Oct 2024; ERA consultation duty expected by end-2026 [93] | Hospitality employers | Established players [94] | Yes | Yes | Reject |
| O19 | US state pay transparency | Several states in force; DE 2027 [95] | Multi-state employers | ATS/HRIS/payroll suites | Yes | Yes | Reject |
| O20 | US state privacy laws | 20 states; IN, KY, RI from 1 Jan 2026 [96] | Businesses above thresholds | Very crowded | Yes | Yes | Reject |
| O21 | Spain digital time recording | Decree reported as not adopted (vendor blogs); status UNKNOWN [97] | Spanish employers | Dozens of apps [97] | Yes | Yes | Reject |
| O22 | EU F-gas record-keeping | Reg. (EU) 2024/573 Art. 7: records kept ≥5 years [11] | Operators of in-scope equipment; HVAC contractors | Field-service suites, national databases | Yes | Yes | Reject |
| O23 | Non-regulatory: field service / trades | Market pull only | Trades SMBs | Saturated [99] | Yes | Yes | Reject |
| O24 | Non-regulatory: clinic practice management | Market pull only | Allied-health clinics | Saturated, AI-scribe add-ons [100] | Yes | Yes | Reject |
| O25 | Non-regulatory: construction COI tracking | Contractual pull | General contractors | Crowded; AI/OCR extraction widely marketed [101] | **Yes** (competitive handicap noted separately) | Yes | Reject (on competition) |

---

## 3. Detailed analysis per opportunity

Full analyses cover O1–O8, O12 and O15 (10 areas). Every other area has at least one line per required field.

### O1 — EU Cyber Resilience Act: SBOM-based vulnerability-handling, reporting-clock and evidence workspace

**Problem.**
- From **11 September 2026**, manufacturers must notify ENISA's Single Reporting Platform of actively exploited vulnerabilities and severe incidents: an early warning within **24 hours**, a notification within **72 hours**, and a final report (14 days after a corrective measure for vulnerabilities; one month for incidents). VERIFIED [2][21].
- This applies to **all in-scope products placed on the market before 11 Dec 2027**. VERIFIED, Art. 69(3) in the OJ text [2].
- From **11 December 2027**, Annex I applies. Part II requires manufacturers to "identify and document vulnerabilities and components … including by drawing up a software bill of materials in a commonly used and machine-readable format covering at the very least the top-level dependencies". VERIFIED [2].
- The support period must be at least five years, unless the product's expected use time is shorter. VERIFIED, Art. 13(8) [2].
- Fines for breaching Annex I or Arts. 13–14 reach €15m or 2.5% of worldwide turnover. VERIFIED, Art. 64(2) [2].
- After the 2 Jul 2025 corrigendum, micro and small enterprises are not fined for missing the 24-hour early-warning deadline in Art. 14(2)(a) or 14(4)(a). The duty itself remains. VERIFIED [3].
- SUPPORTED INFERENCE: together this is a multi-year job of recording and meeting deadlines: products and versions, then components, known vulnerabilities, triage decisions, reports and advisories, and support-period end dates.

**Target users.**
- ENISA's SME survey had 194 respondents, who could select several roles: 41% software developers, 20% final-product manufacturers, 14% ICT-hardware or connected-device makers, 14% component manufacturers. Company size split: 27% micro, 36% small, 37% medium. VERIFIED [27].
- SUPPORTED INFERENCE: the segment an MVP can serve is **SMEs whose products are built with package managers and can export a CycloneDX or SPDX SBOM**. That is mainly software developers, plus connected-device makers whose application layers use package managers.
- Embedded or firmware products that need binary analysis to produce an SBOM are **not** in the MVP segment (see MVP-feasible below).
- Pure SaaS is generally out of scope unless it is "remote data processing" for a product. VERIFIED [23]; secondary analysis [34].

**Pain severity (evidence).**
- ENISA SME CRA Survey Report (24 Jun 2026; fieldwork Feb–Mar 2026; n=194). VERIFIED [27]:
  - 66% had heard of the CRA.
  - Only 67 respondents (34.5%) use SBOMs, and 47 (24.2%) use threat modelling.
  - Technical-documentation and secure-development templates were each requested by more than 70%.
  - Financial support was selected by 142 respondents, the joint-highest support item.
  - More than a third of micro-companies have no incident-response plan.
- A secondary source cites the Commission impact assessment as counting about 615,000 manufacturers at an average cost of about €47,000. UNKNOWN; not verified against the primary document and not relied on [33].

**What people do today.** SUPPORTED INFERENCE [27][31][32]: spreadsheets and documents, free OWASP Dependency-Track (Apache-2.0; matches SBOMs against NVD/OSV/GitHub advisories [31]), consultants and test labs, and enterprise product-security platforms. About 65% of respondents did not report using SBOMs. The question was multi-select, and 10.3% gave no answer, so this is a ceiling on non-use, not a measured rate [27].

**Existing solutions / competitors (non-exhaustive).**
- The Cyber Vendor Guide (Aug 2026) records published prices [30]:
  - ConformOps: free preview for 2 products; full assessment **€99 per product**; continuous monitoring **€79/month per product**; portfolio plan **€249/month for five products**.
  - Article 14 Ready: free field compiler; "24h Dry Run" **€79** one-off.
  - CVD Portal: permanent free tier for an Art. 13 disclosure intake, plus paid tiers.
  - ONEKEY, pi3g, Bureau Veritas, DEKRA, SGS and TÜV SÜD are quote-only.
- Anchore, Finite State, Cycode, CRA Evidence, Distr and Regulus publish CRA offers. VERIFIED (V, snippets) [32].
- OWASP Dependency-Track is free [31].
- No dominant SME-focused leader was identified. UNKNOWN whether one exists.

**Future need.** PREDICTION: demand builds towards 11 Dec 2027 and continues through support periods of at least five years [2]. Commission guidance with 67 SME examples was published on 27 Jul 2026 [25]. The Commission *may* publish a simplified technical-documentation form for micro and small enterprises [24]; timing UNKNOWN. If published, it could commoditise template-only offerings.

**Barriers.**
- Technical buyers face free alternatives.
- Trust is needed for a security-adjacent tool.
- Product classification (default, important class I/II, critical) is a legal judgment the product must not make [23].
- Data-feed terms:
  - GitHub Advisory Database, PyPI and Go advisories are CC-BY 4.0 via OSV. VERIFIED [35].
  - NVD data is free, but the API terms require an "uses the NVD API but is not endorsed" notice. VERIFIED (two snippets) [36].
  - ENISA EUVD terms are UNKNOWN [37].

**Risks.**
- Low willingness to pay (the financial-support signal [27]) and low price anchors (€79–€249/month [30]).
- The 24-hour fine relief lowers urgency for micro and small firms on that one deadline [3].
- Liability if the tool implies compliance or misses a vulnerability.
- The competitor field is moving fast [30].

**AI-free?** Yes. SBOM parsing, package-URL-based advisory matching, reporting clocks, document assembly, audit trail and alerts are all deterministic. SUPPORTED INFERENCE.

**MVP-feasible? Conditional.**
- **Feasible** for customers who can supply **CycloneDX or SPDX (JSON) SBOMs from their own build tooling**. The MVP would store products, versions and SBOMs, sync advisories from CC-BY-licensed OSV sources on a schedule, match by package URL, record triage decisions, run Art. 14 deadline clocks, and export evidence. It would **not** submit reports; the ENISA SRP is the only legal channel [26].
- **Not MVP-feasible** where SBOMs must be generated from binaries or firmware. C/C++ and embedded builds often lack package metadata, vendored code needs fuzzy fingerprinting, and CPE mapping is error-prone. VERIFIED (S/V, read) [38].
- **Gating UNKNOWN:** commercial terms for EUVD, and any use of NVD beyond the stated notice, must be confirmed before architecture.

**Verdict.** Recommend #1, restricted to SBOM-capable software-product SMEs (§5).

---

### O2 — Great Britain holiday-record and holiday-pay assurance for variable-hours employers

**Problem.**
- ERA 2025 s.35 inserted reg. 16B into the Working Time Regulations 1998 (in force **6 Apr 2026**, SI 2026/323). Employers must "keep records which are adequate to show whether the employer has complied with" the annual-leave entitlements and holiday-pay requirements, "retain such records for six years", and may keep them "in such manner and format as the employer reasonably thinks fit". Failure is an offence under reg. 29. VERIFIED [12]. The fine is unlimited. VERIFIED [40].
- There is no official definition of "adequate". VERIFIED [39].
- DBT's consultation (30 Jun–22 Sep 2026) proposes that the FWA enforce statutory holiday pay from 2027. It would investigate up to six years back, with penalties of 200% of arrears, a **£20,000 maximum per worker** and a £100 minimum (the same settings as minimum-wage enforcement). VERIFIED [41].
- The FWA delivery plan states an intention to begin holiday-pay enforcement in **April 2027**. VERIFIED as stated intention [42]; actual commencement is a PREDICTION.
- Irregular-hours and part-year workers accrue 12.07% of hours worked for leave years starting on or after 1 Apr 2024, and rolled-up holiday pay is lawful for them. VERIFIED (S, two independent snippets) [47].

**Territorial scope.** The FWA's holiday-pay enforcement powers "extend and apply only to England & Wales and Scotland. Employment law is devolved in Northern Ireland". VERIFIED [41]. The duty is framed here as **Great Britain**. Whether Northern Ireland has an equivalent record duty is UNKNOWN.

**Target users.** GB employers with irregular-hours, zero-hours, part-year or variable-pay staff, plus payroll bureaus and accountants. SUPPORTED INFERENCE: hospitality, social care, retail, cleaning, security and agencies; the FWA delivery plan names social care, construction, retail and hospitality as priorities [42]. ONS EMP17 (released 18 Aug 2026): about **1.23 million** people (3.6% of those in employment) were on zero-hours contracts in their main job in Apr–Jun 2026. This figure is UK-wide, not GB. VERIFIED [46].

**Pain severity (corrected evidence).**
- *Leave denial, not calculation error.* DBT cites these as its evidence of non-compliance, while noting that no single data source fully measures it. VERIFIED [41]:
  - Resolution Foundation analysis of ASHE: 2.2 million jobs were not given any annual leave in 2025.
  - TUC analysis of the LFS: about 1.1 million workers were not given holiday pay in 2023, about £2bn.
  - Both measure *workers receiving no paid holiday*. They do **not** measure calculation errors, which is the problem O2 would address.
- *Calculation error (the O2 problem).* This is evidenced qualitatively, not by prevalence:
  - DBT states that "calculating holiday pay entitlement can be complex and can lead to accidental non-compliance and underpayment". VERIFIED [41].
  - The payroll professional body CIPP (1 May 2022) reports that "incorrect calculation methods for holiday pay are often applied to all employees" and are used "over a prolonged period before the issue is identified", including outdated 12-week reference periods instead of the required 52 weeks. VERIFIED [44].
  - A figure of ">30% of respondents non-compliant with holiday pay" attributed to a 2024 CIPP survey was seen only in a snippet. UNKNOWN and not relied on [45].
- *Dispute volume.* About 8,000 Employment Tribunal claims under "Working Time (annual leave)" and 13,000 "Wages Act" claims were filed in 2024/25, according to Acas data cited by DBT. VERIFIED [41].
- *How common miscalculation is among SMEs* remains a **HYPOTHESIS** (A-05).

**What people do today.** Payroll software, some of which supports 52-week averaging (KeyPay advertises it; a Xero ideas thread requests it [49]), spreadsheets, and leave trackers that record balances but not pay-rate correctness [50]. SUPPORTED INFERENCE.

**Existing solutions / competitors.** Leave and HR tools: BrightHR, Breathe, Timetastic, LeaveWizard, edays, Shiftbase, Factorial [50]. Payroll suites: Sage, Xero, QuickBooks, BrightPay, Staffology, KeyPay [49]. **paiyroll** is a holiday-pay add-on for 19+ payroll systems, aimed at employers and bureaus, priced at 15p per payslip, minimum £30/month, optional £90 setup. VERIFIED (V, read) [48].

**Future need.** PREDICTION: demand rises as FWA enforcement begins (stated intention April 2027 [42]) and FWA guidance appears. The records obligation recurs, with a six-year look-back [12][41].

**Barriers.** Crowded HR and payroll ecosystem; low SME willingness to pay; data depends on payroll exports in varying formats; GB-only market.

**Risks.**
- Calculation liability, especially "normal remuneration" and the split between EU-derived and domestic leave.
- Incumbents may close the gap.
- FWA guidance on "adequate records" could change what is needed; timing UNKNOWN.

**AI-free?** Yes. **MVP-feasible?** Yes: CSV import, rules engine, per-worker ledger, immutable history, audit-pack export, email reminders. SUPPORTED INFERENCE.

**Verdict.** Recommend #2 (§5).

---

### O3 — Awaab's Law case and statutory-clock management for small social landlords (England)

**Problem.**
- Timescales for social landlords. VERIFIED [51]:
  - emergency hazards investigated and made safe within **24 hours**;
  - significant hazards investigated within **10 working days**;
  - written summary within **3 working days** of the investigation;
  - safety work within **5 working days**;
  - supplementary work started within 5 working days, or as soon as reasonably practicable and within **12 weeks**;
  - records of all engagement and access attempts kept, to support the "all reasonable endeavours" defence.
- Phase 1 has applied since **27 Oct 2025**. Phase 2 adds excess cold and heat, falls, structural collapse, fire, electrical and domestic hygiene hazards from **30 Nov 2026**. VERIFIED [51].
- Phase 3 (remaining HHSRS hazards except overcrowding) has **no confirmed date** in current GOV.UK material. VERIFIED [51][52]. Secondary sources expect 2027 (PREDICTION).

**Legal scope (corrected).**
- There is no size threshold. Awaab's Law "applies to almost all social housing occupied under a **tenancy** and let by a registered provider". It "does not apply to any housing that is occupied under a **licence**", nor to long leaseholds, other owner-occupied accommodation or shared ownership. It **does** apply to temporary and supported accommodation let under a tenancy. VERIFIED [51].
- Almshouse charities that are registered providers are exempt because residents occupy under licence. VERIFIED [53].
- Supported housing let under licence is out of scope. VERIFIED [54].

**Target users (corrected sizing).**
- The RSH register at 17 Sep 2026 lists **1,577** registered providers: 1,253 non-profit, 92 for-profit and 232 local authorities. VERIFIED [56].
- In 2025, the 227 large private registered providers (1,000+ homes) were 17% of PRPs and owned 96% of their stock. VERIFIED [55].
- SUPPORTED INFERENCE: roughly 1,100 PRPs own fewer than 1,000 homes. This is **an upper bound, not the target universe**. From it, subtract:
  - almshouse charities: 265 entries have corporate form "Charity" and 108 names contain "alms" [56]; a snippet attributes 264 RP almshouse charities to the Almshouse Association [57]; the exact count is UNKNOWN;
  - PRPs that are subsidiaries of larger groups and use group systems (count UNKNOWN);
  - providers letting only under licence (count UNKNOWN);
  - providers whose repairs are run by managing agents (count UNKNOWN).
- Upper bound of small in-scope PRPs: about **835–990** (1,100 minus 108–265). SUPPORTED INFERENCE. The number of *independent, in-scope, self-managing* small buyers is **UNKNOWN** and may be much lower.
- Local authorities with stock are in scope but typically buy enterprise systems (ASSUMPTION).

**Pain severity (evidence).** Statutory working-day clocks, tenant enforceability and Housing Ombudsman scrutiny [51]. v1 claimed that an ombudsman case involved a landlord with fewer than 50 homes. The August 2025 severe-maladministration report names only large landlords [62], so that claim is **withdrawn** (UNKNOWN). Small-provider pain is a **HYPOTHESIS** (A-09).

**What people do today.** UNKNOWN for small providers. A spreadsheet-and-email practice is a HYPOTHESIS (A-09). HazardClock asserts it [58].

**Existing solutions / competitors (corrected; all V).**
- **Rentalize Core**: "50 to 5,000 homes", "repairs with Awaab's Law timescales" (article dated 6 Jul 2026) [59]. From €199/month; a 60-home example at €695/month (snippet, two Rentalize pages) [59].
- **PyramidG2**: "small and mid-size social landlords", "well over a hundred social landlords" [59].
- **Landlord Vision**: cited for very small social landlords, but "not a like-for-like housing management system for a registered provider" [59].
- **HousingSurvey Pro**: live, self-serve ("sign up free — no card"), a tamper-evident damp and mould evidence timeline for associations and councils, charged per surveyor per month [60].
- **HazardClock**: waitlist, aimed at small providers [58].
- Weightmans, Netcall, Propsys360, Enghouse, Alscient, Plentific [61].
- Made Tech: its page returned 403, so its hazard case-management offer is UNKNOWN [61].

**Future need.** PREDICTION: Phase 2 (30 Nov 2026) and Phase 3 widen the hazards covered and increase case volumes. The Renters' Rights Act allows Awaab's Law to be applied to the private rented sector, but the Government has only committed to consult [86]. Extension is UNKNOWN.

**Barriers.** Small and uncertain buyer universe; council procurement; tenant and contractor integration expectations.

**Risks.** Live competitors already priced for this niche [59][60]; buyers may be group members or out of scope; hazard classification needs human judgment; working-day computation must be correct.

**AI-free?** Yes. **MVP-feasible?** Yes. **Verdict.** Moved from Rank 3 to the **watchlist** (§5).

---

### O4 — EU Pay Transparency compliance for SME / lower-mid-market employers

**Problem.** Directive (EU) 2023/970 (OJ text read). VERIFIED [1]:
- **Art. 5:** pay or pay range must be given before interview or contract, and asking about pay history is banned.
- **Art. 6(1):** employers must make easily accessible the objective, gender-neutral criteria used to determine pay, pay levels and pay progression.
- **Art. 6(2):** member states may exempt employers with fewer than 50 workers **from the pay-progression obligation only**.
- **Art. 7:** workers may request information, which must be provided "within a reasonable period of time but in any event within two months".
- **Art. 9:** reporting at 250+ workers annually from 7 Jun 2027; 150–249 every three years from 7 Jun 2027; 100–149 every three years from 7 Jun 2031.
- **Art. 10:** joint pay assessment where an unjustified gap of at least 5% is not remedied within six months.
- **Art. 34:** transposition deadline 7 Jun 2026.

**Status.**
- Morgan Lewis lists Italy, Slovakia, Lithuania and Malta as implemented by the deadline. It lists the Netherlands, Sweden, Czechia and Denmark as indicating 1 Jan 2027. VERIFIED [13].
- Littler (6 May 2026) calls Malta and Poland partial. VERIFIED [14].
- Ius Laboris (last updated **23 Sep 2026**) treats **only Italy** as transposed. VERIFIED [15]. It also reports:
  - France: draft amended 10 Sep 2026.
  - Germany: "(unconfirmed) rumours that the cabinet **is expected to** approve the draft bill" in October 2026. This is a future event.
  - Spain: draft Royal Decree of 3 Aug 2026.
  - Ireland: bill not prioritised.
  - Netherlands: plenary in January 2027, and the 1 Jan 2027 target "now appears uncertain".
- The Commission refused to postpone the directive or include it in an omnibus. VERIFIED (two snippets; also confirmed by Judge 1 spot-check S16) [16][17].
- Without transposition, the obligations do not apply directly to employers, but courts may interpret national equal-pay law consistently with the directive. VERIFIED [13].

**Target users.** Employers with 100–249 workers (reporting), and all employers in transposed states for Arts. 5–7.

**Pain severity.** High in principle: job evaluation for "work of equal value", sex-disaggregated statistics and joint assessments. SUPPORTED INFERENCE from [1]. Readiness-survey percentages seen online could not be traced to a primary source (UNKNOWN).

**Existing solutions.** Figures, Ravio, Personio, Sysarb, Trusaic, Syndio, PayAnalytics, beqom, Axios Analytics, TracefyHR, employsome [19][20]. One buyer's guide says most tools were built for enterprise buyers [19].

**Future need.** PREDICTION: strong from 2027 as reporting starts and large states transpose. Durable, because reports and requests recur.

**Barriers / risks.** National variation and language; the largest markets are not transposed; crowded field with HRIS incumbents; sensitive data; risk of wrong categorisation.

**AI-free?** Yes. **MVP-feasible?** Yes, for one jurisdiction. **Verdict.** Recommend #3, conditional (§5).

---

### O5 — US FSMA 204 food traceability (watchlist)

- **Problem:** firms handling Food Traceability List foods must keep Key Data Elements for Critical Tracking Events, maintain a traceability plan, and give FDA a sortable spreadsheet within 24 hours on request. Restaurants and retail have modified requirements. VERIFIED [63].
- **Timing:** not enforced before **20 Jul 2028** under a congressional directive. VERIFIED [63][64].
- **Target users:** FDA estimates more than 323,000 domestic businesses operating more than 484,100 establishments, including about 12,000 farms and 443,000 retail food establishments and restaurants. VERIFIED (CRS, 29 Apr 2026) [64].
- **Pain / evidence:** low awareness among small and medium suppliers and non-chain restaurants; supplier-data difficulty. VERIFIED [64].
- **Current solutions:** ReposiTrak, iFoodDS, Trustwell, FoodReady, Inecta, Nulogy [65].
- **Future need:** PREDICTION that buying concentrates in 2027–2028.
- **Barriers:** supplier data exchange (GS1/EDI).
- **Risks:** Congress told FDA to consider flexibilities for lot-level tracking, so the rules may change. VERIFIED [64].
- **AI-free / MVP:** Yes / Yes.
- **Verdict:** Watchlist; revisit in 2027.

---

### O6 — UK Martyn's Law (reject; enhanced tier on watchlist)

- **Problem:** responsible persons for premises of 200–799 capacity (standard tier) must notify the SIA and have evacuation, invacuation, lockdown and communication procedures. The enhanced tier (800+) must also implement and document measures and submit them to the SIA. Expected in force spring 2027; SIA portal testing early 2027. VERIFIED [66].
- **Target users:** venues, places of worship, retail and similar premises with a reasonable expectation of 200+ people present at once. SUPPORTED INFERENCE from the tier definitions [66].
- **Pain severity:** low for the standard tier. The Home Office myth buster says the impact assessment estimated **£330/year** per standard-tier premises, mainly staff time rather than cash, and **£5,210/year** per enhanced-tier premises. VERIFIED (primary, read) [67].
- **Evidence against a paid product:** the Home Office intends that in-scope persons "can comply with the Act without needing to buy specialist services". Its guidance will require "no particular expertise nor the use of third-party products", and the Home Office, SIA and NaCTSO "do not endorse any third-party products". VERIFIED [67].
- **Current solutions:** Standard Tier, Martyn's Law Software (from £19/month claimed), Martyn's Law Plan, Policy Pros, plus free ProtectUK resources [68][67].
- **Future need:** PREDICTION: enhanced-tier premises need documented measures and SIA submissions from 2027, which is a more document-heavy, recurring job.
- **Barriers:** official discouragement of third-party products; low budgets.
- **Risks:** SIA section-12 guidance, due autumn 2026, may change expectations (UNKNOWN).
- **AI-free / MVP:** Yes / Yes.
- **Verdict:** Reject the standard tier. The enhanced tier stays on the watchlist.

---

### O7 — EU/UK e-invoicing mandates (reject)

- **Problem:** structured e-invoicing mandates are arriving across Europe. VERIFIED (multiple snippets) [69]–[73]:
  - Belgium B2B Peppol from 1 Jan 2026.
  - Poland KSeF Feb and Apr 2026; micro-enterprises 2027; no penalties until 2027.
  - France: receive from 1 Sep 2026 (all); issue 1 Sep 2026 (large/mid) and 1 Sep 2027 (SMEs), via approved platforms.
  - Germany: receive since 2025; issue from 2027 if prior-year turnover exceeds €800k; all from 2028.
  - Spain Verifactu postponed to 1 Jan 2027 (corporate-tax payers) and 1 Jul 2027 (others).
  - UK: B2B and B2G VAT invoices from 1 Apr 2029, with Peppol confirmed 23 Jun 2026.
- **Target users:** all VAT-registered B2B businesses in those countries.
- **Pain severity:** real but absorbed by accounting and ERP vendors (SUPPORTED INFERENCE).
- **Current solutions:** about 137+ French approved platforms [70]; national accounting suites; Peppol access points.
- **Future need:** strong through 2029. For the UK, a roadmap is expected at Budget 2026, and a phased rollout (larger businesses 2029, smaller possibly 2030) is reported but not confirmed. UNKNOWN; single-source snippets [73].
- **Barriers:** approval or registration (French PA status) and Peppol access-point accreditation (UK requirements still outstanding [73]).
- **Risks:** a scale-driven market dominated by incumbents.
- **AI-free / MVP:** Yes / **No**.
- **Verdict:** Reject. UK 2029 stays on the watchlist only if a niche that needs no certification appears.

---

### O8 — European Accessibility Act (reject)

- **Problem:** in-scope products and services must meet accessibility requirements. Member states apply the measures from **28 Jun 2025** (Art. 31). **Micro-enterprises providing services are exempt** (Art. 4(5)). Transitional provisions run until 28 Jun 2030 for services using products already in use, and self-service terminals may be used for up to 20 years. VERIFIED [4].
- **Target users:** e-commerce, banking, e-books, transport ticketing and similar service providers, plus manufacturers of in-scope products.
- **Pain severity:** rising. French injunctions against large grocers have been reported, including a court order against Carrefour with a daily penalty, and the Dutch ACM has started audits. No fines had been issued under an EAA transposition by mid-2026. VERIFIED (two or more snippets) [74].
- **Current solutions:** very crowded: Level Access, Deque, Siteimprove, AudioEye and many checkers [74].
- **Future need:** PREDICTION of growth as enforcement matures and transitional periods end in 2030 [4].
- **Barriers:** automated checks cover only part of the requirements (SUPPORTED INFERENCE); remediation is service-heavy.
- **Risks:** credibility problems around "overlay" products; no differentiation.
- **AI-free / MVP:** Yes / Partly (a scanner is feasible; meaningful conformance is not a software-only MVP).
- **Verdict:** Reject — crowded.

---

### O12 — CSRD / voluntary SME standard (reject)

- **Problem:** Directive (EU) 2026/470 (OJ 26 Feb 2026) limits individual sustainability reporting to undertakings with net turnover above €450m and an average of more than 1,000 employees. It introduces a "value-chain cap" that lets protected undertakings decline requests beyond the voluntary standard. VERIFIED [8]. The Commission adopted the voluntary-standard delegated act on 3 Jul 2026, subject to scrutiny. VERIFIED (two snippets) [79].
- **Target users:** SME suppliers asked for ESG data by large customers and banks.
- **Pain severity:** reduced. Reporting is voluntary and requests are capped (SUPPORTED INFERENCE from [8]).
- **Current solutions:** osapiens, Dcycle, Sunhat, Coolset and others [80].
- **Future need:** PREDICTION of moderate demand where banks and customers standardise on the voluntary standard. The extent is UNKNOWN.
- **Barriers:** carbon accounting needs emission-factor datasets (licensing UNKNOWN).
- **Risks:** voluntary uptake; crowded market.
- **AI-free / MVP:** Yes / Yes.
- **Verdict:** Reject.

---

### O15 — PPWR / multi-country packaging EPR (reject)

- **Problem:** Regulation (EU) 2025/40 applies from **12 Aug 2026** (Art. 71). Member states keep national producer registers (Art. 44), and registration may be made by the producer or its EPR authorised representative (Annex IX). Harmonised labelling applies from 12 Aug 2028 or 24 months after the implementing acts, whichever is later (Art. 12). Recyclability-grade criteria apply from 1 Jan 2030. VERIFIED [5].
- **Target users:** producers and cross-border distance sellers, including non-EU sellers.
- **Pain severity:** high for multi-country sellers, who must register and report separately in each state [5][84].
- **Current solutions:** Gramta, Repax, Lappa, EPR Insights (Shopify app, per-country pricing claimed) and compliance schemes [84].
- **Future need:** PREDICTION of growth through 2028–2030 as labelling and design requirements start [5].
- **Barriers:** deep per-country scheme knowledge and data formats.
- **Risks:** an environmental-omnibus proposal to suspend the EU-producer authorised-representative obligation. A snippet reports that the Council did not pursue it on 24 Jun 2026 — UNKNOWN [83]. The field is crowded.
- **AI-free / MVP:** Yes / Partly.
- **Verdict:** Reject — crowded and fragmented by country.

---

### Other examined areas (one line per field)

**O9 — NIS2**

| Field | Content |
|---|---|
| Problem | Germany's NIS2 implementation in force 6 Dec 2025; BSI registration was due 6 Mar 2026. VERIFIED (two snippets) [75] |
| Target users | Essential and important entities. A figure of ~29,500 German entities circulates; UNKNOWN precision (single snippet) [75] |
| Pain | Registration, risk management and incident reporting |
| Evidence | [75] |
| Current solutions | Very crowded GRC and ISMS tools |
| Future need | Continuing supervision (PREDICTION) |
| Barriers | Audit credibility; integration depth |
| Risks | Saturation |
| AI-free / MVP | Yes / Partly |
| Verdict | Reject |

**O10 — DORA register of information**

| Field | Content |
|---|---|
| Problem | Annual register submissions. The CSSF window was 11 Feb–31 Mar 2026, with plain-CSV files in a ZIP following the ESA folder structure and wider validation checks. VERIFIED [76] (v1's "xBRL-CSV" wording corrected) |
| Target users | EU financial entities |
| Pain | Data quality and validation rejections [76] |
| Evidence | [76] |
| Current solutions | GRC suites and specialist register tools |
| Future need | Annual, recurring (PREDICTION) |
| Barriers | Regulated, enterprise buyers |
| Risks | Long sales cycles |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O11 — EU AI Act deployer obligations**

| Field | Content |
|---|---|
| Problem | Reg. (EU) 2026/1744 (OJ 24 Jul 2026) moves Annex III high-risk obligations to 2 Dec 2027 and Annex I to 2 Aug 2028. It rewrites Art. 4 so that providers and deployers "take measures to support the development of AI literacy", which "does not require … any specific level". VERIFIED [9] |
| Target users | AI deployers |
| Pain | Low until Dec 2027 |
| Evidence | [9][77] |
| Current solutions | Crowded AI-governance tools [78] |
| Future need | PREDICTION of rising demand into Dec 2027 |
| Barriers | Crowded; positioning an AI-free product for AI governance |
| Risks | Further simplification |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O13 — Whistleblowing channels**

| Field | Content |
|---|---|
| Problem | Internal reporting channels required for private entities with 50+ workers (Art. 8(3)). VERIFIED [10] |
| Target users | Employers with 50+ workers |
| Pain | Low; mature market |
| Evidence | [10][81] |
| Current solutions | Many, from ~€19/month (V) [81] |
| Future need | Stable |
| Barriers | Price commoditisation |
| Risks | No differentiation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O14 — EUDR**

| Field | Content |
|---|---|
| Problem | Reg. (EU) 2025/2650 sets application at 30 Dec 2026, and 30 Jun 2027 for micro/small undertakings established by 31 Dec 2024. VERIFIED [7]. No further postponement per the May 2026 package. VERIFIED (two snippets) [82] |
| Target users | Operators and traders of cattle, cocoa, coffee, palm oil, rubber, soy and wood |
| Pain | Geolocation and due-diligence statements |
| Evidence | [7][82] |
| Current solutions | Crowded |
| Future need | From Dec 2026 (PREDICTION) |
| Barriers | Geo-data and supply-chain data |
| Risks | Rules have been amended repeatedly |
| AI-free / MVP | Yes / Partly |
| Verdict | Reject |

**O16 — EU Short-Term Rental Regulation**

| Field | Content |
|---|---|
| Problem | Reg. (EU) 2024/1028 applies from 20 May 2026. VERIFIED [6]. Registration numbers are needed where member states require them; platforms verify and report [85] |
| Target users | STR hosts and managers |
| Pain | Mostly borne by platforms and authorities |
| Evidence | [6][85] |
| Current solutions | Channel managers, guest-registration tools [85] |
| Future need | Stable |
| Barriers | Platform-centric obligations |
| Risks | Low differentiation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O17 — UK landlord compliance (Renters' Rights Act, PRS database, MTD ITSA)**

| Field | Content |
|---|---|
| Problem | Tenancy reform from 1 May 2026. VERIFIED [86][87]. PRS database opens 15 Dec 2026, West Midlands first (deadline 14 Mar 2027), rolling regionally to Nov 2027, £65 per property per year; landlords provide property, tenancy and safety-certificate data. VERIFIED [88][89]. Civil penalties up to £7,000, or up to £40,000 or prosecution. VERIFIED [86]. MTD ITSA from 6 Apr 2026 above £50k, then £30k (2027) and £20k (2028). VERIFIED (two snippets) [91] |
| Target users | Private landlords in England. Estimates of 2.3–2.8m circulate (single snippet): UNKNOWN precision [92] |
| Pain | Real but low per-landlord budget (SUPPORTED INFERENCE) |
| Evidence | [86]–[92] |
| Current solutions | Saturated incl. free tiers and £8.99–£29.99/month tools [90] |
| Future need | Ombudsman (2028), Decent Homes for PRS (2035/2037) [87] |
| Barriers | Price floor near zero |
| Risks | Saturation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O18 — UK tipping**

| Field | Content |
|---|---|
| Problem | Tips Act (Oct 2024); ERA duty to consult on tipping policies expected by end-2026; draft code consultation closes 29 Sep 2026. VERIFIED (two snippets) [93] |
| Target users | Hospitality employers |
| Pain | Moderate |
| Evidence | [93] |
| Current solutions | TiPJAR, JustTip, IRIS Tronc and others [94] |
| Future need | Recurring three-yearly reviews |
| Barriers | Payments-embedded competitors |
| Risks | Niche |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O19 — US state pay transparency**

| Field | Content |
|---|---|
| Problem | NJ (1 Jun 2025), VT (1 Jul 2025), MA (29 Oct 2025), DE (26 Sep 2027) and others. VERIFIED (two snippets) [95] |
| Target users | Multi-state employers |
| Pain | Job-posting compliance |
| Evidence | [95] |
| Current solutions | ATS, HRIS and payroll suites |
| Future need | More states (PREDICTION) |
| Barriers | Built into incumbents |
| Risks | Feature, not product |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O20 — US state privacy laws**

| Field | Content |
|---|---|
| Problem | 20 comprehensive state laws; IN, KY and RI from 1 Jan 2026. VERIFIED (two snippets) [96] |
| Target users | Businesses above state thresholds |
| Pain | Consent and data-subject requests |
| Evidence | [96] |
| Current solutions | Very crowded |
| Future need | More states (PREDICTION) |
| Barriers | Crowded |
| Risks | Saturation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O21 — Spain digital time recording**

| Field | Content |
|---|---|
| Problem | Royal Decree mandating digital records reported by vendor blogs as not yet adopted in Sep 2026: UNKNOWN (V sources cannot verify legal status) [97] |
| Target users | Spanish employers |
| Pain | UNKNOWN until adopted |
| Evidence | [97] |
| Current solutions | Dozens of time-clock apps and HR suites [97] |
| Future need | Depends on adoption |
| Barriers | Crowded; language |
| Risks | Regulatory uncertainty |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O22 — EU F-gas record-keeping**

| Field | Content |
|---|---|
| Problem | Operators of leak-checked equipment must keep records and retain them for at least 5 years unless stored in a national database (Art. 7). VERIFIED [11] |
| Target users | Equipment operators; HVAC contractors |
| Pain | Low novelty; predecessor regimes existed (SUPPORTED INFERENCE) |
| Evidence | [11][98] |
| Current solutions | Field-service suites, national databases |
| Future need | Stable |
| Barriers | Incumbents |
| Risks | Low differentiation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O23 — Field service / trades**

| Field | Content |
|---|---|
| Problem | Scheduling, quoting and invoicing |
| Target users | Trades SMBs |
| Pain | Real but well served |
| Evidence | Jobber, Housecall Pro, ServiceM8, Tradify, Simpro, ServiceTitan; ~$29–60/month entry (V) [99] |
| Current solutions | As listed |
| Future need | Stable |
| Barriers | Dominant incumbents |
| Risks | Saturation |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O24 — Clinic practice management**

| Field | Content |
|---|---|
| Problem | Booking, notes and billing |
| Target users | Allied-health clinics |
| Pain | Well served |
| Evidence | WriteUpp, Cliniko, Zanda, Pabau, Jane; £15–29 per practitioner per month; AI-scribe add-ons (V) [100] |
| Current solutions | As listed |
| Future need | Stable |
| Barriers | Incumbents |
| Risks | AI-free product at a disadvantage against AI documentation features |
| AI-free / MVP | Yes / Yes |
| Verdict | Reject |

**O25 — Construction COI tracking**

| Field | Content |
|---|---|
| Problem | Tracking subcontractor insurance certificates and expiries |
| Target users | General contractors |
| Pain | Real |
| Evidence | BCS, TrustLayer, myCOI, Jones, Billy, Certificial, COI File, PaperBoss (V) [101] |
| Current solutions | As listed; AI/OCR extraction widely marketed |
| Future need | Stable |
| Barriers | Crowded |
| Risks | Competitive handicap without automated certificate extraction |
| AI-free / MVP | **Yes**: expiry tracking, requests and reminders are deterministic / Yes |
| Verdict | Reject on competition (not on the AI-free filter) |

---

## 4. Rejected opportunities and reasons

| # | Area | Decisive reason(s) | What would change the verdict |
|---|---|---|---|
| O6 | Martyn's Law (standard tier) | Home Office says compliance needs no paid third-party products; £330/year cost estimate; cheap entrants [67][68] | Enhanced-tier buyers found underserved and willing to pay (watchlist) |
| O7 | E-invoicing | Saturated; approval and access-point accreditation fails the MVP filter | A certification-free niche (none found) |
| O8 | EAA | Crowded; conformance is service-heavy | Fines creating demand for evidence management specifically |
| O9 | NIS2 | Saturated GRC market | — |
| O10 | DORA register | Enterprise/regulated buyers; specialist incumbents | — |
| O11 | AI Act | High-risk duties deferred; Art. 4 softened; crowded | — |
| O12 | CSRD / voluntary standard | Scope reduced; voluntary; crowded | Banks mandating voluntary-standard data from SME borrowers at scale (UNKNOWN) |
| O13 | Whistleblowing | Commoditised | — |
| O14 | EUDR | Volatile rules; crowded; geo-data heavy | — |
| O15 | PPWR/EPR | Crowded; deep per-country knowledge | — |
| O16 | STR Regulation | Obligations mainly on platforms | — |
| O17 | UK landlord compliance | Saturated, including free tools | — |
| O18 | UK tipping | Niche; established providers | — |
| O19 | US pay transparency | Absorbed into ATS/HRIS | — |
| O20 | US privacy | Crowded | — |
| O21 | Spain time recording | Not enacted (UNKNOWN); crowded | Adopted decree with requirements existing apps cannot meet |
| O22 | F-gas | Not new; served by incumbents | — |
| O23 | Field service | Saturated | — |
| O24 | Clinic PM | Saturated | — |
| O25 | COI tracking | Crowded; competitors market automated extraction | — |

Watchlist (not rejected): O3 Awaab's Law, O5 FSMA 204, O6 enhanced tier, UK e-invoicing 2029 (§5).

---

## 5. Recommended candidates for validation (re-ranked after corrections)

### 5.1 Ranking criteria
The criteria are (a) obligation certainty and timing, (b) consequence of inaction, (c) evidence the segment is underserved, (d) willingness-to-pay signals, (e) MVP fit, (f) legal risk of the product being wrong, and (g) durability to 2029–2031. All judgments are qualitative (SUPPORTED INFERENCE).

### 5.2 What changed in the ranking and why
- **O3: Rank 3 → watchlist.** Three corrections undermine the v1 rationale:
  - Scope excludes licence-occupied housing, including almshouse charities [51][53].
  - The realistic small-provider universe is an upper bound of about 835–990, with the true count of independent, in-scope buyers UNKNOWN [55][56].
  - Live tools already target providers of 50–5,000 homes, with published pricing from €199/month [59], alongside a free self-serve evidence tool [60].
- **O4: Rank 4 → Rank 3 (still conditional).** Nothing about O4 improved, and only Italy is fully transposed [15]. It moves up because O3 dropped out, and it still carries a durable, EU-wide, legally firm obligation [1].
- **O1: stays Rank 1, but narrowed** to SBOM-capable software-product SMEs, after the feasibility review (J1-006) and the ENISA role data showing software developers are the largest respondent group [27].
- **O2: stays Rank 2.** Its pain evidence was re-characterised (J1-003) and its scope corrected to GB (J1-011). Newly read primary evidence supports calculation complexity and underpayment risk qualitatively [41][44], and adds a firm penalty regime [41][42].

### 5.3 O1 vs O2, criterion by criterion

| Criterion | O1 CRA (SBOM-capable software SMEs) | O2 GB holiday-pay assurance | Edge |
|---|---|---|---|
| (a) Certainty/timing | EU regulation, no transposition; reporting live 11 Sep 2026; main obligations 11 Dec 2027 [2] | In force 6 Apr 2026 [12]; FWA intends enforcement from Apr 2027 [42] | Even |
| (b) Consequence | Up to €15m / 2.5% [2]; no CE marking means no EU sales from Dec 2027 [23]; micro/small fine relief only for the 24h deadline [3] | Criminal offence (records) [12]; 200% penalty capped at £20k/worker (proposed) [41]; 6-year look-back [41] | O1 (market access) |
| (c) Underserved evidence | Regulator survey: 34.5% use SBOMs; >70% want templates [27]; fragmented new vendors [30] | Incumbent payroll/HR tools partly cover it; a dedicated add-on exists [48][49] | O1 |
| (d) WTP signals | Negative (142 of 194 cite financial support [27]); low anchors €79–€249/month [30] | Positive but low: paying market for a £30/month-minimum add-on [48] | O2 (slightly) |
| (e) MVP fit | Conditional on customers supplying SBOMs; feed-licence gating [35]–[37] | Straightforward CSV + rules engine | O2 |
| (f) Legal risk of being wrong | Missed or mismatched vulnerability; must not imply compliance | Calculation errors create customer liability | Even (both material) |
| (g) Durability | Support periods ≥5 years [2] | 6-year records; annual leave cycles [12] | Even |
| Breadth | EU-wide, including non-EU sellers | Great Britain only | O1 |

**Trade-off stated.** O1 ranks first on consequence, documented under-service and breadth. O2 is stronger on willingness-to-pay evidence and MVP simplicity. **Switch condition:** if Market Validation finds that SBOM-capable software SMEs will not pay more than free tooling plus the €79–€99 one-off offers, O2 should become the lead candidate.

### 5.4 Ranked recommendations

**Rank 1 — O1: CRA vulnerability-handling, reporting-clock and evidence workspace for SBOM-capable software-product SMEs**

*Why.* Reporting duties are live for the installed base, main obligations are fixed for Dec 2027, and the regulator's own survey shows low readiness. The work is deterministic record-keeping and deadline tracking.

*Key questions for Market Validation (Agent 2):*
1. **Do target customers already produce SBOMs** (CycloneDX/SPDX), and from which build tools? What share of software-product SMEs, versus connected-device makers, can?
2. Which job is most valuable and least served: vulnerability monitoring, triage evidence, Art. 14 clocks and report preparation, technical documentation, support-period management, or customer-facing advisories?
3. Willingness to pay against the €79/month-per-product and €249/month-for-five anchors [30] and against free Dependency-Track [31].
4. What trust prerequisites (EU hosting, security posture, references) does a small vendor need?
5. What are the commercial terms for EUVD, and are NVD and OSV attribution duties workable? A-03 is a gating UNKNOWN.
6. When and what will the Commission's simplified technical-documentation form for micro and small enterprises be [24]?

**Rank 2 — O2: GB holiday-record and holiday-pay assurance for variable-hours employers**

*Why.* A criminal record-keeping duty is in force, a penalty regime with a stated enforcement start is coming, and the government itself states that calculations are complex. A paying market for a calculation add-on exists.

*Key questions:*
1. Who buys: the employer, the payroll bureau or accountant, or both? How big is the bureau channel (UNKNOWN)?
2. Which payroll systems in 2026 lack correct 52-week averaging, irregular-hours accrual and a six-year evidence trail?
3. Direct evidence of miscalculation prevalence, to test A-05. Can the CIPP 2024 survey be obtained?
4. When will FWA guidance on "adequate" records appear, and what will it contain?
5. Willingness to pay against 15p/payslip [48]; the value of an audit pack versus calculation alone.
6. Which payroll export formats are needed as a minimum? What is the process for verifying the rules (see OOS-04)?

**Rank 3 (conditional) — O4: EU Pay Transparency compliance for SME / lower-mid-market employers in a transposed jurisdiction**

*Why.* The EU-level obligations are durable and firm [1]. Recommended only if validation finds a transposed, underserved jurisdiction with enough employers in the 100–249 band.

*Key questions:*
1. Which jurisdiction is (or will soon be) fully transposed, sizeable, and served in a language the team can support? Italy is the only one confirmed by [15].
2. What are the exact national report formats and deadlines?
3. Will SMEs, worker representatives and equality bodies accept a deterministic job-evaluation method?
4. How far do Personio, Figures and similar tools already cover Arts. 5–10 in that jurisdiction, and at what prices?

### 5.5 Watchlist
- **O3 Awaab's Law.** It returns to the recommended list if validation shows three things: (1) a count of independent, tenancy-letting, self-managing small providers well above a few hundred; (2) those providers still tracking manually despite Rentalize Core, PyramidG2, HousingSurvey Pro and HazardClock; and (3) willingness to pay at or above ~€199/month. It also returns if the Government confirms a timetable for Awaab's Law in the private rented sector. *Key questions if revived:* the in-scope provider count from RSH data tables; traction and pricing of Rentalize Core, PyramidG2, Landlord Vision and HousingSurvey Pro among providers with fewer than 1,000 homes; procurement routes.
- **O5 FSMA 204.** Revisit in 2027 after FDA acts on the flexibilities direction [64].
- **O6 Martyn's Law enhanced tier.** Revisit after SIA guidance and commencement in 2027 [66][67].
- **UK e-invoicing 2029.** Revisit after the Budget 2026 roadmap [73].

---

## 6. Key assumptions & unknowns

| ID | Statement | Label | Why it matters / how to test |
|---|---|---|---|
| A-01 | SBOM-capable software SMEs will pay for a CRA workspace rather than use free tools plus one-off €79–€99 offers | HYPOTHESIS | Core to O1; pricing interviews |
| A-02 | No dominant SME-focused CRA vendor exists as of 2026-09-26 | UNKNOWN | O1 gap; Agent 2 to map traction |
| A-03 | Vulnerability feeds can be used commercially: GHSA/PyPI/Go CC-BY 4.0 (VERIFIED [35]); NVD free with notice (VERIFIED [36]); EUVD terms | UNKNOWN (EUVD) — **gates O1 feasibility** | Check EUVD terms before architecture |
| A-04 | ~615,000 CRA manufacturers; ~€47k average cost | UNKNOWN (secondary only [33]) | Do not use until verified in the impact assessment |
| A-05 | Many GB SME payroll setups calculate variable-pay holiday incorrectly | HYPOTHESIS. Qualitative support only [41][44]; the ">30% non-compliant" figure is snippet-only [45] | O2 demand; test with bureaus, try to obtain CIPP 2024 |
| A-06 | Payroll bureaus are an efficient channel for O2 | HYPOTHESIS | Channel economics |
| A-07 | FWA holiday-pay enforcement begins in April 2027 | VERIFIED as stated intention [42]; actual commencement PREDICTION | O2 timing |
| A-08 | Small in-scope PRPs number at most ~835–990 | SUPPORTED INFERENCE from [55][56]; independent self-managing buyers UNKNOWN | O3 (watchlist) sizing |
| A-09 | Small tenancy-letting providers that are not group subsidiaries track Awaab's Law cases manually | HYPOTHESIS; excludes exempt almshouses [53] | O3 revival test |
| A-10 | Awaab's Law will be extended to the private rented sector | UNKNOWN (consultation only) [86] | Would change O3 materially |
| A-11 | DE, FR and ES transpose the Pay Transparency Directive in 2026–2027 | PREDICTION [15] | O4 timing |
| A-12 | The Commission will not postpone the Pay Transparency Directive | VERIFIED as of the statements found [16]; future change UNKNOWN | O4 |
| A-13 | CRA Art. 14 applies to products placed on the market before 11 Dec 2027 | VERIFIED (OJ text) [2] | O1 urgency |
| A-14 | Micro/small enterprises are not fined for missing the 24h early warning | VERIFIED (OJ corrigendum 2 Jul 2025) [3] | Lowers O1 urgency for the smallest firms |
| A-15 | Martyn's Law cost estimates £330 / £5,210 per year | VERIFIED (Home Office myth buster, read) [67] | Supports O6 rejection |
| A-16 | Council did not pursue the PPWR authorised-representative suspension (24 Jun 2026) | UNKNOWN (single snippet) [83] | O15 only |
| A-17 | Snippet-only sources should be re-read in the original before external use: [16], [17], [20] (part), [26], [29], [31]–[34], [36], [43], [45], [47], [49], [50], [57], [59] (price), [61], [65], [68]–[75], [78]–[85], [89]–[101] | Process note | Summaries may paraphrase or misdate |
| A-18 | Whether Northern Ireland has an equivalent holiday-record duty | UNKNOWN | O2 market boundary |
| A-19 | Share of CRA-relevant SMEs whose products are package-managed, not firmware or embedded | UNKNOWN; ENISA roles are a proxy only [27] | O1 segment size |

---

## 7. Sources

Access date for all sources: 2026-09-26. **Read** means fetched and read in this session; for PDFs and xlsx files this was a local extraction. **Snippet** means seen only as a search-result summary. Grades: **P** primary/official, **S** secondary, **V** vendor.

**Primary legal texts (Official Journal XHTML via the EU Publications Office; the same text as EUR-Lex)**
1. Directive (EU) 2023/970 (Pay Transparency), OJ L 132, 17.5.2023 — https://publications.europa.eu/resource/celex/32023L0970 ; EUR-Lex https://eur-lex.europa.eu/eli/dir/2023/970/oj/eng — P, Read
2. Regulation (EU) 2024/2847 (Cyber Resilience Act), OJ L 20.11.2024 — https://publications.europa.eu/resource/celex/32024R2847 ; EUR-Lex https://eur-lex.europa.eu/eli/reg/2024/2847/oj — P, Read (Arts. 13(8), 14, 64, 69, 71; Annex I Part II)
3. Corrigendum to Regulation (EU) 2024/2847, OJ L 2025/90555, 2.7.2025 (Art. 64(10): "paragraphs 3 to 9" becomes "2 to 9") — http://data.europa.eu/eli/reg/2024/2847/corrigendum/2025-07-02/oj (via https://publications.europa.eu/resource/celex/32024R2847R%2802%29) — P, Read
4. Directive (EU) 2019/882 (European Accessibility Act), OJ L 151, 7.6.2019 — https://publications.europa.eu/resource/celex/32019L0882 ; EUR-Lex https://eur-lex.europa.eu/eli/dir/2019/882/oj — P, Read (Arts. 4(5), 31, 32)
5. Regulation (EU) 2025/40 (PPWR), OJ L 22.1.2025 — https://publications.europa.eu/resource/celex/32025R0040 — P, Read (Arts. 12, 44, 71; Annex IX)
6. Regulation (EU) 2024/1028 (Short-term rentals), OJ L 29.4.2024 — https://publications.europa.eu/resource/celex/32024R1028 — P, Read
7. Regulation (EU) 2025/2650 (EUDR amendment), OJ L 23.12.2025 — https://publications.europa.eu/resource/celex/32025R2650 — P, Read
8. Directive (EU) 2026/470 (Omnibus I), OJ L 26.2.2026 — https://publications.europa.eu/resource/celex/32026L0470 — P, Read
9. Regulation (EU) 2026/1744 (Digital Omnibus on AI), OJ L 24.7.2026 — https://publications.europa.eu/resource/celex/32026R1744 — P, Read
10. Directive (EU) 2019/1937 (Whistleblowing), OJ L 305, 26.11.2019 — https://publications.europa.eu/resource/celex/32019L1937 — P, Read (Art. 8(3))
11. Regulation (EU) 2024/573 (F-gas), OJ L 20.2.2024 — https://publications.europa.eu/resource/celex/32024R0573 — P, Read (Art. 7)
12. Employment Rights Act 2025, s.35 (inserts WTR 1998 reg. 16B; in force 6.4.2026 by SI 2026/323) — https://www.legislation.gov.uk/ukpga/2025/36/section/35 — P, Read

**Pay transparency (O4)**

13. Morgan Lewis, "EU Pay Transparency Directive: The Deadline for Transposition Has Passed—What Now?", 8 Jun 2026 — https://www.morganlewis.com/pubs/2026/06/eu-pay-transparency-directive-the-deadline-for-transposition-has-passed-what-now — S, Read
14. Littler, "In the Eleventh Hour: Implementation Status of the EU Pay Transparency Directive", 6 May 2026 — https://www.littler.com/news-analysis/asap/eleventh-hour-implementation-status-eu-pay-transparency-directive — S, Read
15. Ius Laboris, "EU Pay Transparency Directive: which countries have transposed", last updated 23 Sep 2026 — https://iuslaboris.com/insights/eu-pay-transparency-directive-which-countries-have-transposed/ — S, Read
16. Ius Laboris, "The EU Commission does not intend to delay the Pay Transparency Directive" — https://iuslaboris.com/insights/eu-pay-transparency-no-delay/ ; Agence Europe, 22 May 2026 — https://agenceurope.eu/en/bulletin/article/13874/22/hadja-lahbib-rejects-any-pause-or-simplification-of-pay-transparency-directive — S, Snippet (also confirmed by Judge 1 spot-check S16)
17. Lewis Silkin, "BusinessEurope calls for a 'Stop the clock' …", 10 Mar 2026 — https://www.lewissilkin.com/insights/2026/03/10/businesseurope-calls-for-a-stop-the-clock-on-the-pay-transparency-directive — S, Snippet
18. Haufe, "Entgelttransparenzgesetz: Verschiebung mit Ansage", 30 Apr 2026 — https://www.haufe.de/personal/personalszene/entgelttransparenzgesetz-verschiebung-mit-ansage_74_684262.html — S, Read
19. Axios Analytics, "Best EU Pay Transparency Software 2026", Jun 2026 — https://axiosanalytics.com/en/resources/best-eu-pay-transparency-software-2026 — V, Read
20. Trusaic — https://trusaic.com/resources/best-eu-pay-transparency-directive-software/ ; Figures — https://figures.hr/solutions/pay-equity ; TracefyHR — https://tracefyhr.com/blog/eu-pay-transparency-directive-2026-guide ; Sysarb (updated 12 Nov 2025) — https://resources.sysarb.com/buyers-guides/what%E2%80%99s-the-best-equal-pay-software-in-the-eu — V, Snippet (Sysarb Read)

**Cyber Resilience Act (O1)**

21. European Commission, "CRA – Reporting obligations", updated 11 Sep 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-reporting — P, Read
22. European Commission, "Cyber Resilience Act", updated 7 Sep 2026 — https://digital-strategy.ec.europa.eu/en/policies/cyber-resilience-act — P, Read
23. European Commission, "CRA – Summary of the legislative text", 3 Dec 2025 — https://digital-strategy.ec.europa.eu/en/policies/cra-summary — P, Read
24. European Commission, "CRA – MSMEs", updated 31 Jul 2026 — https://digital-strategy.ec.europa.eu/en/policies/cra-msmes — P, Read
25. European Commission, "Commission publishes new guidance to support timely CRA implementation", 27 Jul 2026 — https://digital-strategy.ec.europa.eu/en/library/commission-publishes-new-guidance-support-timely-cyber-resilience-act-implementation — P, Read
26. ENISA, "The CRA Single Reporting Platform is launched" (Sep 2026) — https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched ; Industrial Cyber — https://industrialcyber.co/regulation-standards-and-compliance/enisa-launches-single-reporting-platform-as-eu-cyber-resilience-act-vulnerability-reporting-obligations-take-effect/ — P/S, Snippet
27. ENISA, *SME CRA Survey Report*, 24 Jun 2026 (PDF, CC BY 4.0) — https://www.enisa.europa.eu/publications/sme-cra-survey-report (PDF: https://www.enisa.europa.eu/sites/default/files/2026-06/SME%20CRA%20survey%20report.pdf) — P, Read ; ENISA news "Where do SMEs stand in preparing for the CRA?", 13 Jul 2026 — https://www.enisa.europa.eu/news/where-do-smes-stand-in-preparing-for-the-cyber-resilience-act — P, Read
28. european-cyber-resilience-act.com, Art. 69 reproduction — https://www.european-cyber-resilience-act.com/Cyber_Resilience_Act_Article_69.html — S (third-party reproduction), Read; superseded by [2]
29. Art. 64 secondary: Venvera — https://venvera.com/learn/cra/fines-and-penalties ; StreamLex — https://streamlex.eu/articles/cra-en-art-64/ ; Faegre Drinker (Sep 2026) — https://www.faegredrinker.com/en/insights/publications/2026/9/september-2026-eu-compliance-deadlines-for-connected-product-manufacturers — S/V, Snippet; superseded by [2][3]
30. Cyber Vendor Guide, "CRA Compliance Companies (2026)", Aug 2026 — https://www.cybervendorguide.com/guides/cra-compliance — S, Read (price anchors)
31. OWASP Dependency-Track — https://dependencytrack.org/ ; https://owasp.org/projects/dependency-track — P (project), Snippet
32. CRA vendor pages: ONEKEY — https://www.onekey.com/resource/cyber-resilience-act-sbom ; Anchore — https://anchore.com/sbom/eu-cra/ ; Finite State — https://finitestate.io/blog/eu-cra-sbom-technical-documentation-guide ; Cycode — https://cycode.com/blog/cyber-resilience-act/ ; CRA Evidence — https://craevidence.com/cra-compliance/support-period-basics ; Distr — https://distr.sh/cyber-resilience-act/monitoring-and-reporting/ ; Regulus — https://goregulus.com/cra-basics/owasp-dependency-check/ — V, Snippet
33. CircleID, "EU Cyber Resilience Act Costs and Economic Impact" — https://circleid.com/posts/eu-cyber-resilience-act-costs-and-economic-impact — S, Snippet (not relied on)
34. DLA Piper, "CRA: the fine line between SaaS and digital products", Feb 2026 — https://www.dlapiper.com/en/insights/publications/2026/02/cyber-resilience-act-the-fine-line-between-saas-and-digital-products — S, Snippet
35. OSV, "Data sources" (per-source licences; GHSA, PyPI and Go: CC-BY 4.0) — https://google.github.io/osv.dev/data/ — P (project docs), Read
36. NVD, "Terms of Use" (free API; required notice "This product uses the NVD API but is not endorsed or certified by the NVD") — https://nvd.nist.gov/developers/terms-of-use ; ScanCode LicenseDB — https://scancode-licensedb.aboutcode.org/nist-nvd-api-tou.html — P/S, Snippet (two)
37. ENISA EUVD API documentation — https://euvd.enisa.europa.eu/apidoc — P, not readable; terms UNKNOWN
38. Interlynk, "The State of SBOM Generation for C/C++: 2026 Edition", 9 Apr 2026 — https://www.interlynk.io/resources/the-state-of-sbom-generation-for-c-c-2026-edition — V/S, Read ; RunSafe, "How to Validate SBOM Accuracy for Embedded C/C++" — https://runsafesecurity.com/blog/validate-sbom-accuracy/ — V, Snippet

**Holiday records and pay (O2)**

39. Baker McKenzie, "United Kingdom: New Record-Keeping Obligations for Annual Leave", 15 Apr 2026 — https://www.bakermckenzie.com/en/insight/publications/2026/04/united-kingdom-new-record-keeping-obligations-for-annual-leave — S, Read
40. DLA Piper, "Duty to keep holiday records means new legal risks for employers", 9 Apr 2026 — https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2026/employment-rights-act-preparing-for-change-duty-to-keep-holiday-records-means-new-legal-risks-for-employers — S, Read
41. Department for Business and Trade, *Make Work Pay: Holiday Pay Compliance and Enforcement* (consultation), 30 Jun 2026, closed 22 Sep 2026 — PDF https://assets.publishing.service.gov.uk/media/6a3e79add52550a19950f617/make-work-pay-holiday-pay-compliance-and-enforcement.pdf ; page https://www.gov.uk/government/consultations/make-work-pay-holiday-pay-compliance-and-enforcement — P, Read (territorial extent; penalty settings; evidence section citing Resolution Foundation 2026, TUC 2024 and Acas 2024/25)
42. Lewis Silkin, "The Fair Work Agency's first Delivery Plan", 16 Sep 2026 — https://www.lewissilkin.com/insights/2026/09/16/the-fair-work-agencys-first-delivery-plan — S, Read
43. GOV.UK ERA implementation roadmap — https://www.gov.uk/government/publications/implementing-the-plan-to-make-work-pay-and-employment-rights-act ; Lewis Silkin ERA timeline, 23 Jul 2026 — https://www.lewissilkin.com/en/insights/2026/07/23/employment-rights-act-timeline — P/S, Snippet
44. CIPP, "The complexities of holiday pay", 1 May 2022 — https://www.cipp.org.uk/resources/news/the-complexities-of-holiday-pay.html — S (professional body), Read
45. CIPP Payslip Statistics Survey Report 2024 — https://www.cipp.org.uk/resourceLibrary/payslip-statistics-survey-report-2024.html — S, Snippet (">30% non-compliant" not verified; not relied on)
46. ONS, EMP17 "People in employment on zero hours contracts", release 18 Aug 2026 (xlsx) — https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/datasets/emp17peopleinemploymentonzerohourscontracts — P, Read (Table 1, Apr–Jun 2026)
47. Irregular-hours accrual (12.07%, leave years from 1 Apr 2024): DLA Piper (2024) — https://knowledge.dlapiper.com/dlapiperknowledge/globalemploymentlatestdevelopments/2024/latest-changes-to-holiday-pay-and-what-they-mean-for-employers ; Payne Hicks Beach — https://www.phb.co.uk/article/holiday-pay-and-entitlement-reforms-in-2024/ — S, Snippet (two)
48. paiyroll, "Automated holiday pay for existing payroll software" — https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ — V, Read
49. Xero Product Ideas (52-week averaging request) — https://productideas.xero.com/forums/939198-for-small-businesses/suggestions/45241594-uk-payroll-reporting-run-a-report-to-calculate ; KeyPay — https://www.keypay.co.uk/features/52-week-averaging — V, Snippet
50. LeaveWizard — https://www.leavewizard.com/best-employee-holiday-tracker/ ; edays — https://www.e-days.com/news/top-8-best-absence-management-software-providers ; Shiftbase — https://www.shiftbase.com/blog/best-absence-management-software-uk — V, Snippet

**Awaab's Law (O3)**

51. GOV.UK, "Awaab's Law Phase 2: Guidance for social landlords", updated 31 Jul 2026 — https://www.gov.uk/government/publications/awaabs-law-phase-2-guidance-for-social-housing-landlords/awaabs-law-phase-2-guidance-for-social-landlords — P, Read (s.1.5 scope; timescales)
52. GOV.UK, "Awaab's Law in the social rented sector" (collection), 13 Jul 2026 — https://www.gov.uk/government/collections/awaabs-law-in-the-social-rented-sector — P, Read (no Phase 3 date)
53. The Almshouse Association, "Update: Awaab's Law", 28 Oct 2025 — https://www.almshouses.org/news/update-awaabs-law/ — S, Read
54. Homeless Link, "Awaab's Law: what supported housing providers need to know", 1 Jun 2026 — https://homeless.org.uk/news/awaabs-law-what-supported-housing-providers-need-to-know/ — S, Read
55. Regulator of Social Housing, PRP stock and rents 2024–25, key facts, 31 Oct 2025 — https://www.gov.uk/government/statistics/private-registered-provider-social-housing-stock-and-rents-in-england-2024-to-2025/private-registered-providers-stock-and-rents-in-england-summary-key-facts — P, Read
56. Regulator of Social Housing, *List of registered providers*, 17 Sep 2026 (xlsx) — https://assets.publishing.service.gov.uk/media/6aad16bcce3f006bd4346c9b/List_of_registered_providers_17_September_2026.xlsx (publication page https://www.gov.uk/government/publications/registered-providers-of-social-housing) — P, Read (counts computed locally)
57. Almshouse Association written evidence (RSH 021) — https://committees.parliament.uk/writtenevidence/41930/pdf/ — S, Snippet (264 figure; page returned 403; date unconfirmed)
58. HazardClock — https://hazardclock.co.uk/tools/compliance-checklist/ — V, Read
59. Rentalize, "Best Housing Management Systems UK 2026", 6 Jul 2026 — https://rentalize.com/best-housing-management-systems-uk-2026/ — V, Read ; pricing (from €199/month; 60-home example €695/month) — https://rentalize.com/ — V, Snippet
60. HousingSurvey Pro — https://housingsurvey.pro/ — V, Read
61. Weightmans — https://www.weightmans.com/products/awaab-s-law-compliance-tool/ ; Netcall — https://www.netcall.com/complying-with-awaabs-law-what-good-looks-like/ ; Propsys360 — https://neotechnologysolutions.com/propsys360/case-management-dynamics-365/awaabs-law-practical-compliance-for-damp-mould/ ; Plentific — https://www.plentific.com/resource-center/blog/awaabs-law-phase-2-explained-the-new-hhsrs-hazards-and-statutory-deadlines-for-2026/ ; Made Tech — https://www.madetech.com/blog/awaabs-law-phase-2-what-it-covers-and-what-housing-providers-should-be-doing-now/ (HTTP 403) — V, Snippet
62. Housing Ombudsman, "Learning from severe maladministration – August 2025" — https://www.housing-ombudsman.org.uk/reports/learning-from-severe-maladministration-reports/august-2025/ — P, Read

**FSMA 204 (O5)**

63. FDA, "FSMA Final Rule on Requirements for Additional Traceability Records for Certain Foods", updated 24 Jul 2026 — https://www.fda.gov/food/food-safety-modernization-act-fsma/fsma-final-rule-requirements-additional-traceability-records-certain-foods — P, Read
64. Congressional Research Service, R48925, 29 Apr 2026 — https://www.everycrsreport.com/reports/R48925.html (also https://www.congress.gov/crs-product/R48925) — S, Read
65. ReposiTrak — https://repositrak.com/fda-food-traceability/food-traceability/ ; iFoodDS — https://www.ifoodds.com/software-solutions/food-traceability-software/ ; Flux IoT — https://flux-iot.com/blog/best-food-traceability-software-fsma-204 ; Inecta — https://www.inecta.com/blog/fsma-204-compliance-guide — V, Snippet

**Martyn's Law (O6)**

66. GOV.UK / SIA, "Understanding Martyn's Law and the SIA's role as regulator", 17 Jul 2026 — https://www.gov.uk/guidance/understanding-martyns-law-and-the-sias-role-as-regulator — P, Read
67. Home Office, *Martyn's Law myth buster* (PDF, Nov 2025) — https://assets.publishing.service.gov.uk/media/69281f35b3b9afff34e960f0/martyns-law-mythbuster.pdf — P, Read
68. Standard Tier — https://www.standardtier.co.uk/about ; Martyn's Law Software — https://martynslawsoftware.co.uk/ ; Martyn's Law Plan — https://martynslawplan.co.uk/guides/enhanced-tier-explained/ ; Policy Pros — https://www.policypros.co.uk/martyns-law-2027-compliance-guide/ — V, Snippet

**E-invoicing (O7)**

69. Finbite — https://finbite.eu/en/e-invoicing-mandates-europe-2026/ ; SPS Commerce — https://www.spscommerce.com/community/articles/e-invoicing-mandates-in-europe-the-2026-business-guide — V/S, Snippet
70. impots.gouv.fr — https://www.impots.gouv.fr/facturation-electronique-et-plateformes-agreees ; Pennylane — https://www.pennylane.com/fr/fiches-pratiques/facture-electronique/liste-des-pdp — P/V, Snippet
71. BMF FAQ E-Rechnung — https://www.bundesfinanzministerium.de/Content/DE/FAQ/e-rechnung.html ; e-rechnungs-studio — https://e-rechnungs-studio.de/de/e-rechnung-uebergangsregeln-2027-800000-2028 — P/V, Snippet
72. Noticias Jurídicas (RDL 15/2025) — https://noticias.juridicas.com/actualidad/noticias/20735-nueva-prorroga:-verifactu-no-sera-obligatorio-hasta-2027-para-sociedades-y-otros-contribuyentes/ — S, Snippet
73. ICAS — https://www.icas.com/news-insights-events/news/tax/autumn-budget-2025-e-invoicing-will-go-ahead-from-2029 ; vatcalc — https://www.vatcalc.com/united-kingdom/uk-2029-mandatory-b2b-e-invoicing/ ; Sovos — https://sovos.com/regulatory-updates/vat/uk-confirms-adoption-of-peppol-as-the-framework-for-its-upcoming-e-invoicing-mandate/ — S/V, Snippet

**Other areas**

74. EAA enforcement: Deque — https://www.deque.com/blog/early-signs-of-eaa-enforcement-across-europe/ ; auditsu — https://auditsu.com/resources/eaa-enforcement-2026 ; Plaintest — https://www.plaintest.dev/blog/eu-accessibility-act-enforcement-2026/ ; LI Solutions — https://li.solutions/blog/eaa-enforcement-2026/ — V/S, Snippet
75. DLA Piper, NIS2 Germany (Feb 2026) — https://www.dlapiper.com/en/insights/publications/2026/02/nis-2-directive-transposed-in-germany ; Privacy World (Dec 2025) — https://www.privacyworld.blog/2025/12/germany-implements-nis2-registration-portal-will-open-on-january-6-2026/ — S, Snippet
76. CSSF, DORA register of information submission, 11 Feb 2026 — https://www.cssf.lu/en/2026/02/dora-submission-timeframe-for-register-of-information-edesk-portal-open-as-of-11-february-2026/ — P, Read
77. Gibson Dunn, 27 May 2026 — https://www.gibsondunn.com/eu-ai-act-omnibus-agreement-postponed-high-risk-deadlines-and-other-key-changes/ ; Usercentrics — https://usercentrics.com/knowledge-hub/eu-ai-act-high-risk-delay-article-50-transparency-consent/ — S/V, Read
78. Themio — https://www.themio.ai/en/blog/best-ai-act-compliance-tools-sme-2026 ; Legalithm — https://www.legalithm.com/en/blog/eu-ai-act-compliance-software-tools-compared-2026 — V, Snippet
79. IAS Plus, Jul 2026 — https://www.iasplus.com/en/news/2026/07/ec-voluntary-standard ; European Commission delegated act — https://ec.europa.eu/finance/docs/level-2-measures/csrd-delegated-act-2026-5011_en.pdf — S/P, Snippet
80. osapiens — https://osapiens.com/en/regulations/vsme-voluntary-sustainability-reporting-standard-for-smes ; Dcycle — https://dcycle.io/blog/vsme-voluntary-standard-smes-2026/ ; Sunhat — https://www.getsunhat.com/blog/csrd-vsme — V, Snippet
81. Elker — https://elker.com/articles/whistleblowing-software ; TrueSpeak — https://truespeak.eu/en/blog/comparisons/best-whistleblowing-software-2026-comparison ; WeMoral — https://wemoral.com/business/best-whistleblowing-software — V, Snippet
82. Council of the EU, 18 Dec 2025 — https://www.consilium.europa.eu/en/press/press-releases/2025/12/18/deforestation-council-signs-off-targeted-revision-to-simplify-and-postpone-the-regulation/ ; Hogan Lovells (May 2026) — https://www.hoganlovells.com/en/publications/eu-deforestation-regulation-commission-publishes-simplification-package-ahead-of-december-2026 ; IntegrityNext — https://www.integritynext.com/resources/blog/article/eudr-review-out-now-minor-simplifications-same-deadline — P/S/V, Snippet
83. business.gov.uk PPWR — https://www.business.gov.uk/campaign/europe/european-union-eu-regulations/eu-packaging-and-packaging-waste-regulation-eu-ppwr/ ; Coolset — https://www.coolset.com/academy/ppwr-authorised-representative — P/V, Snippet
84. Gramta — https://gramta.com/articles/epr-ppwr-compliance-software-landscape ; Repax — https://www.repax.io/blog/best-epr-software ; Lappa — https://lappa.org/articles/extended-producer-responsibility-ecommerce-eu — V, Snippet
85. European Commission news, 20 May 2026 — https://single-market-economy.ec.europa.eu/news/new-rules-bring-increased-transparency-short-term-rentals-sector-2026-05-20_en ; Chekin — https://chekin.com/en/blog/regulation-eu-2024-1028/ ; Minut — https://www.minut.com/blog/eu-short-term-rental-regulations — P/V, Snippet
86. GOV.UK, "Guide to the Renters' Rights Act", updated 6 Nov 2025 — https://www.gov.uk/government/publications/guide-to-the-renters-rights-act/guide-to-the-renters-rights-act — P, Read
87. RICS, "Renters' Rights Act: what's happening and when?", 16 Jan 2026 — https://ww3.rics.org/uk/en/journals/property-journal/renters-rights-act-implementation-roadmap.html — S, Read
88. NRLA, "Landlord database: register your rental property service" — https://www.nrla.org.uk/resources/renters-rights/landlord-database-register-your-rental-property-service — S, Read
89. GOV.UK Housing Hub — https://housinghub.campaign.gov.uk/renting-is-changing/ ; MHCLG blog, 20 Mar 2026 — https://mhclgmedia.blog.gov.uk/2026/03/20/%F0%9F%9B%8E%EF%B8%8F-landlords-here-are-6-ways-to-get-yourself-ready-for-new-renters-rights/ — P, Snippet
90. LetDeck — https://letdeck.co.uk/ ; Dwelyx — https://www.dwelyx.co.uk/ ; LLCR — https://www.llcr.uk/ ; ComplianceBot — https://compliancebot.uk/ ; LetCompliance — https://letcompliance.com/landlord-compliance-software-uk ; LandlordOS — https://landlord-os.com/best-landlord-software-uk — V, Snippet
91. GOV.UK, MTD for Income Tax — https://www.gov.uk/guidance/find-out-if-and-when-you-need-to-use-making-tax-digital-for-income-tax ; LITRG — https://www.litrg.org.uk/tax-nic/making-tax-digital-income-tax/when-does-making-tax-digital-start-me — P/S, Snippet
92. OpenRent, EPLS 2024 summary — https://blog.openrent.co.uk/english-private-landlord-survey-summary/ — V/S, Snippet
93. Lewis Silkin, 20 Aug 2026 — https://www.lewissilkin.com/en/insights/2026/08/20/top-tips-to-get-ahead-of-the-upcoming-tipping-changes ; Blake Morgan — https://www.blakemorgan.co.uk/employment-rights-act-2025-revised-code-of-practice-tipping-and-umbrella-companies-consultations/ — S, Snippet
94. JustTip — https://justtip.co.uk/ ; IRIS Tronc — https://www.iris.co.uk/products/tronc-payroll/ ; Slashdot list — https://slashdot.org/software/tip-distribution/in-uk/ — V, Snippet
95. Employment Law Insights, Jul 2026 — https://www.employmentlawinsights.com/2026/07/show-and-tell-new-state-salary-disclosure-laws-go-into-effect/ ; Paycor — https://www.paycor.com/resource-center/articles/pay-transparency-laws-by-state/ — S/V, Snippet
96. IAPP — https://iapp.org/news/a/new-year-new-rules-us-state-privacy-requirements-coming-online-as-2026-begins ; MultiState, 4 Feb 2026 — https://www.multistate.us/insider/2026/2/4/all-of-the-comprehensive-privacy-laws-that-take-effect-in-2026 — S, Snippet
97. Mi Fichaje Legal — https://mifichajelegal.com/blog/real-decreto-registro-horario-digital-mayo-2026-estado-tramitacion-pymes/ ; Kronjop — https://kronjop.com/es/newsroom/control-horario/digital/obligatorio/ — V, Snippet
98. Compliance & Risks, F-gas — https://www.complianceandrisks.com/blog/regulation-eu-2024-573-european-commission-adopts-new-f-gas-regulation/ — S, Snippet
99. Jobber Academy — https://www.getjobber.com/academy/housecall-pro-competitors/ ; Simpro — https://www.simprogroup.com/blog/best-field-service-management-software — V, Snippet
100. WriteUpp — https://www.writeupp.com/blog/best-practice-management-software-for-therapists-in-the-uk-2026-guide ; esremedia — https://esremedia.co.uk/blog/physiotherapy-software-uk-comparison — V/S, Snippet
101. Certificial — https://www.certificial.com/blog-post/best-mycoi-alternatives-2026 ; COI File — https://coifile.com/coi-tracking/best-software/ ; BCS — https://www.getbcs.com/blog/top-certificate-of-insurance-tracking-companies — V, Snippet

---

## 8. Out-of-scope findings (for other agents; reported to the Orchestrator)

| ID | Finding | Responsible agent |
|---|---|---|
| OOS-01 | All recommended areas are compliance-adjacent. Product and marketing copy must avoid "CRA compliant", "guarantees compliance" or legal-advice framing. Outputs should be positioned as records and evidence prepared by the customer. | Agent 14 Legal & Privacy; Agent 7 Marketing |
| OOS-02 | O2 and O4 process pay data by sex and possibly health or disability data. O3 would process tenant vulnerability data. A DPIA, retention rules and access control will be material. | Agent 13 Security; Agent 14; Agent 10 Database |
| OOS-03 | O1 feed licensing: OSV per-source licences (GHSA, PyPI and Go are CC-BY 4.0, requiring attribution) [35]. The NVD API requires a specific non-endorsement notice [36]. ENISA EUVD terms are UNKNOWN [37]. This must be settled before architecture. | Agent 9 Architecture; Agent 14 |
| OOS-04 | O2 calculation engine: needs authoritative bank-holiday data, a documented rule-verification and update process (normal remuneration, 52-week reference period, 12.07% accrual, rolled-up pay, EU vs domestic leave), and regression tests against worked examples. | Agent 9; Agent 11 Backend; Agent 16 QA; Agent 14 |
| OOS-05 | Several competitor categories market AI features (clinic practice management, COI tracking, landlord certificate reading). An AI-free product may need to position determinism and auditability as the benefit. This is a positioning question, not a runtime change. | Agent 3 Strategy; Agent 7; Agent 19 Runtime Independence |
| OOS-06 | If O1 is chosen, the company's own SaaS is generally outside CRA scope. Any downloadable component (CLI, uploader or agent) could itself be a "product with digital elements" [23][34]. | Agent 9; Agent 14 |
| OOS-07 | Jurisdiction interacts with candidate choice. O2 covers Great Britain only (NI UNKNOWN). O1 and O4 are EU-market candidates. O5 is US. Relevant to `BUSINESS_COUNTRY` in `project/decisions/BUSINESS_CONFIG.md`. | Agent 3; Orchestrator |
| OOS-08 | Research tooling note: EUR-Lex returned empty responses here, while the EU Publications Office endpoint (`https://publications.europa.eu/resource/celex/<CELEX>` with `Accept: application/xhtml+xml`) returned full OJ texts, including corrigenda (e.g., `32024R2847R%2802%29`). Downstream agents should use it for verbatim legal re-reads. | All agents; Orchestrator |
| OOS-09 | The Home Office explicitly does not endorse third-party Martyn's Law compliance products [67]. If Martyn's Law content is ever used, marketing claims must respect this. | Agent 7; Agent 14 |
| OOS-10 | The ENISA SME CRA Survey Report is licensed CC BY 4.0 [27], so its figures can be reused with attribution. | Agent 7; Agent 14 |

---

## 9. Revision log (Judge 1 findings on v1 → changes in v2)

| Finding | Severity | Accepted? | What changed in v2 (section references) |
|---|---|---|---|
| **J1-001** | HIGH | Accepted | §3 O3 "Legal scope (corrected)" restates applicability from GOV.UK s.1.5 [51]: tenancies only; licences excluded (almshouses [53], licence-based supported or temporary housing [54]); shared ownership and long leases excluded; supported/temporary housing under a tenancy included. §3 O3 "Target users" replaces "~1,100 small PRPs" with an explicitly labelled upper bound (~835–990, SUPPORTED INFERENCE). The bound is computed from the RSH register (17 Sep 2026: 1,577 providers; 265 "Charity" corporate form; 108 "alms" names) [56] and RSH stock data [55]. Excluded groups are named, and the independent in-scope count is labelled UNKNOWN. The v1 ASSUMPTION about volunteer-run providers was removed, and A-09 now excludes exempt almshouses. §5.2 and §5.5 demote O3 from Rank 3 to the watchlist, with reasoning. §2 row O3 updated. |
| **J1-002** | MEDIUM | Accepted | §2 row O3 and §3 O3 "Existing solutions" now list Rentalize Core (50–5,000 homes, Awaab timers, from €199/month), PyramidG2, Landlord Vision (with its caveat), HousingSurvey Pro (live, free sign-up) and Made Tech (page 403, UNKNOWN), each graded V with URLs [59][60][61]. HazardClock is no longer presented as the only niche tool. "Plausibly underserved" is now HYPOTHESIS A-09. §5.5 adds the key question on traction and pricing of these tools among providers with fewer than 1,000 homes. |
| **J1-003** | MEDIUM | Accepted | §3 O2 "Pain severity (corrected evidence)" now states that the Resolution Foundation (2.2m jobs with no annual leave in 2025) and TUC (1.1m workers with no holiday pay in 2023, ~£2bn) figures measure leave denial, not calculation error. Both are dated and taken from the primary DBT consultation [41]. Calculation-error evidence is added: DBT's statement on complexity and accidental underpayment [41], CIPP (2022) on incorrect methods persisting [44], and Acas tribunal claim volumes [41]. A-05 is relabelled HYPOTHESIS. The §5.2 and §5.4 Rank 2 rationale is reworded. |
| **J1-004** | MEDIUM | Accepted | (i) Martyn's Law costs now come from the primary Home Office myth buster, read [67]. (ii) The SBOM requirement is now verified from the CRA OJ text, Annex I Part II [2], not vendor snippets. (iii) The EAA claims are verified from Directive 2019/882 Arts. 4(5), 31 and 32, read [4]. (iv) The Art. 69 reproduction is regraded S [28], with the OJ text [2] as the read primary. (v) Single-snippet claims fixed: zero-hours now from ONS EMP17, read [46]; 12.07% has two independent snippets [47]; the Housing Ombudsman "fewer than 50 homes" claim is withdrawn after reading [62]; CSSF was read [76]. (vi) "UNVERIFIED" replaced by UNKNOWN (A-16, O15). (vii) The header claim is amended to say figures are dated where the source states a date; derived figures are labelled. In addition, the label rule now states that V sources never verify legal facts, and other single-snippet figures (NIS2 ~29,500; 2.3–2.8m landlords; Spain status) are downgraded to UNKNOWN. |
| **J1-005** | MEDIUM | Accepted | §3 now gives the full structure for 10 areas: O1–O8, O12 and O15. Every other area (O9–O11, O13, O14, O16–O25) has one line per field: problem, target users, pain, evidence, current solutions, future need, barriers, risks, AI-free, MVP, verdict. |
| **J1-006** | MEDIUM | Accepted | The §3 O1 "MVP-feasible" verdict is now conditional. Feasible for customers supplying CycloneDX/SPDX SBOMs, with a stated description of what the MVP ingests and does. Not MVP-feasible where binary or firmware SBOM generation is needed, per [38]. CPE-matching imprecision is noted. Feed licensing is carried into the verdict as a gating UNKNOWN (A-03, partly resolved by [35][36]). §2 row O1 and §5.4 are narrowed to SBOM-capable software-product SMEs. The key question "Do target customers already produce SBOMs?" is added (§5.4 Q1). A-19 is added. |
| **J1-007** | LOW | Accepted | §5.3 adds an O1-vs-O2 comparison covering criteria (a)–(g), including (d) WTP and (f) legal risk. The [30] price anchors (ConformOps €99/product, €79/month/product, €249/month for five; Article 14 Ready €79) are recorded in §3 O1. The ranking is unchanged, with the trade-off and a switch condition stated. |
| **J1-008** | LOW | Accepted | Awaab's Law Phase 3 is shown everywhere as "date unconfirmed" [51][52], with 2027 given only as a PREDICTION from secondary sources. The FWA timing is harmonised: April 2027 is recorded as VERIFIED stated intention (delivery plan, reported 16 Sep 2026 [42]), and actual commencement as PREDICTION (A-07). |
| **J1-009** | LOW | Accepted | [27] now cites the ENISA report (24 Jun 2026) and the ENISA news page (13 Jul 2026) separately. The Ius Laboris tracker [15] is re-checked as "last updated 23 Sep 2026" (v1's "26 Sep" came from a mis-summarised fetch). |
| **J1-010** | LOW | Accepted | Art. 6(2) is corrected: the exemption for employers with fewer than 50 workers covers pay progression only [1]. The German status is reworded as an unconfirmed, expected October 2026 cabinet approval [15]. The §2 row O4 cell now attributes the "on time" list to Morgan Lewis and adds that others treat MT and PL as partial and only IT as fully transposed [13][14][15]. |
| **J1-011** | LOW | Accepted | O2 is reframed as Great Britain throughout (§2, §3 O2, §5, OOS-07), citing ERA 2025 s.35 / WTR reg. 16B [12] and DBT's statement that enforcement powers extend to England & Wales and Scotland, with NI devolved [41]. NI equivalence is UNKNOWN (A-18). The penalty cap is verified: 200% of arrears, £20,000 maximum per worker and £100 minimum (proposed) [41], also reported in the FWA delivery plan [42]. |
| **J1-012** | LOW | Accepted | O25's AI-free column is changed to "Yes" (§2, §3 O25). The rejection reason is competition, with the automated-extraction handicap noted separately (§4). |
| Self-identified | — | — | O10: v1's "xBRL-CSV" wording is corrected to the CSSF-stated plain-CSV-in-ZIP format [76]. O17: PRS database fee (£65/property/year) and regional deadlines added [88]. EU dates in O7–O16 are re-anchored to OJ texts where available [4]–[11]. |

**Disagreements with Judge 1:** none. Every finding was accepted, and the new evidence supported each correction.
