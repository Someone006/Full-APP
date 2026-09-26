# Judge 2 verdict: `project/research/market-validation-v1.md`

| Field | Value |
|---|---|
| Judge | Judge 2 (independent judge for Agent 2, Market & Competitive Validation) |
| Artifact judged | `project/research/market-validation-v1.md` (DRAFT v1, 723 lines) |
| Upstream context | `project/research/opportunity-research-v2.md` §5 (approved); finding J1-013 in `project/judges/judge-01-opportunity-research-v2.md` |
| Date of judgment | 2026-09-26 |
| Basis | The artifact text only. Independent checks by this judge: web fetches and local extraction of the ENISA SRP Glossary v1.3 HTML table, the ENISA SRP FAQ, the ENISA *SME CRA Survey Report* PDF, the ENISA *SBOM Adoption State of Play 2026* PDF, the DBT holiday-pay consultation PDF, the ISTAT census PDF, the CRA OJ XHTML (Art. 14), the OSV data page, the GHSA and CISA KEV READMEs, the NVD ToU (ScanCode copy), the EUVD docs, and the vendor pages of paiyroll, CVD Portal, ConformOps, Axios Analytics, KeyPay, Moneysoft, Staffology, BrightPay, Xero Product Ideas, Article 14 Ready, sbomify, Aikido, Regulus, Zealience, Vulert, Evenpay and effy.ai. |

## Verdict: **FAIL**

One HIGH finding (J2-001) makes a FAIL mandatory under the charter. Most of the artifact is well sourced. 38 of 43 spot-checked claims are confirmed, including every price the brief asked me to prioritise and every ENISA SRP, licence, Italy and Greece fact.

The failure is in the one place the brief made central: the fairness of the O1-vs-O2 comparison (J1-013). The artifact applies a strict competitor standard to O1, and even overstates O1's overlap (J2-002). It then describes O2's direct competitor, paiyroll, as lacking capabilities that paiyroll's own cited page states. It also recasts a KeyPay safeguard as a gap. Its headline O2 differentiator, the "evidence pack … not described by paiyroll's page", is contradicted by that page. The J1-013 asymmetry is therefore reversed rather than removed.

### Criteria summary

| # | Criterion | Result |
|---|---|---|
| 1 | Ten elements for each of O1, O2, O4 | Met in structure. All ten are present for each candidate. Some Agent 1 questions were dropped (J2-008). |
| 2 | Candidate-specific extras | O1: met (SBOM reality; OSV/GHSA/NVD/EUVD terms with licence-page citations; Art. 14 content and SRP channel are excellent). O2: payroll coverage met. Buyer identity is only partly met, because readily available evidence was missed (J2-003). O4: met. |
| 3 | J1-013 resolved (segment consistent; comparison fair) | **Not met.** The segment definition is resolved well, but the comparison is not fair (J2-001, J2-002). S1 sizing over-extrapolates (J2-007). |
| 4 | No winner; no unsupported scores or invented market sizes | Met. The ranking is explicitly deferred to Agent 3. The only computed number is a labelled ESTIMATE with correct arithmetic. The ISTAT figure is real (I found it in the PDF). |
| 5 | Evidence discipline | Partly met. There is one false absence claim about a competitor (J2-001), paraphrases inside quotation marks (J2-005) and label/grade slips (J2-006). |
| 6 | Accuracy (≥10 spot-checks) | Partly met. 43 checks: 38 confirmed, 3 contradicted (paiyroll capabilities, paiyroll traction, KeyPay behaviour) and 2 partly contradicted (ENISA "highest single item"; effy.ai list scope). |
| 7 | Internal consistency; evidence-based comparison table | Partly met. §6 uses evidence-strength words, not scores. However, §2.2, §2.7 and §6 contradict the artifact's own §2.1 rows (J2-002). |
| 8 | Sources with URLs | Met. Minor hygiene: four sources are never cited, one claim is unsourced, and one citation is misattributed (J2-006). |

---

## 1. Spot-check table

| # | Claim (artifact line) | What the judge found | Source URL | Verdict |
|---|---|---|---|---|
| S1 | CVD Portal Reporting €99/mo billed annually €1,188; Compliance €299/mo (€3,588; 3 products then €99 each); automated SBOM↔CVE alerts only in Enterprise (l. 72, 86, 128–129) | Pricing page: Reporting "€99/month (€1,188 annually)", 3 members, with "Article 14 notification workflow (24h / 72h / 14d)", "SRP-ready submission package", "NVD and EUVD threat intelligence feeds". Compliance €299/€3,588. "Automated SBOM ↔ CVE supply chain alerts" is listed under Enterprise only. | https://cvdportal.com/pricing | Confirmed |
| S2 | CVD Portal hosting "EU/Hetzner" [24]; operator Porta Regulus B.V., founded 2026 [21] (l. 86) | The pricing page read shows no hosting. Cyber Vendor Guide states "runs on Hetzner infrastructure in Germany", Porta Regulus B.V., founded 2026. | https://www.cybervendorguide.com/guides/cra-compliance | Confirmed (fact is in [21], not [24]; see J2-006) |
| S3 | ConformOps: free preview 2 products; €99 per product one-off; €79/mo per product ("€790/year"); €249/mo for five (l. 73, 123–126) | All four confirmed verbatim. Art. 14 early-warning/72h workflow, CycloneDX, daily dependency monitoring and GitHub App also confirmed. | https://conformops.eu | Confirmed |
| S4 | Axios Analytics <100: €4,000 one-off; 100–149 €3,000/yr; 150–249 €4,500/yr; onboarding €1,500; Frankfurt hosting; 12-month auto-renew (l. 453, 475–476) | All confirmed verbatim (AWS eu-central-1 Frankfurt). | https://axiosanalytics.com/pricing | Confirmed |
| S5 | paiyroll: 15p per payslip, £30 pcm minimum, optional £90 setup, monthly, no annual contract (l. 281, 329) | Confirmed verbatim. | https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ | Confirmed |
| S6 | paiyroll capabilities; the O2 evidence pack is "the one thing not described by paiyroll's page"; the differentiator includes a lookback of up to 104 weeks (l. 281, 361–362) | The same page states: "Holiday pay XLSX reports (data table and accrual) are available at any point to show the data and calculations. You can be assured you have a complete audit trail"; "Records every payment made by date … looking back 104 weeks to find 52 paid weeks"; "can import 104 weeks of historical pay data"; "specify only the Pay Items that need to be included"; "Generates records and reports for each holiday booking on each pay run". Its 19 integrations include Xero, Sage 50, BrightPay and Moneysoft, the four "gap products". | https://paiyroll.com/automated-holiday-pay-for-existing-payroll-software/ | **Contradicted** (J2-001) |
| S7 | paiyroll "Published traction: None published"; "paiyroll's customer uptake is UNKNOWN" (l. 281, 374) | paiyroll publishes a "Customer Success Stories" page with named customers (e.g., The President Estate Farming Partnership, whose story "resolved holiday pay calculations"; Ignite Nursing) and Trustpilot reviews, including "Recommend Paiyroll for Bureaus". It also publishes bureau payroll tiers at £50/£75/£100 pcm, with "Holiday pay /schemes" in every tier, and a "Holiday Pay Compliance Check … FREE service". | https://paiyroll.com/customers/ ; https://paiyroll.com/payroll-bureau-pricing/ | **Contradicted** (J2-003) |
| S8 | KeyPay "falls back to the current hourly rate if data are insufficient"; "lookback fixed at 52 weeks", presented as a complaint (l. 283, 355) | The page says: "If the average hourly rate calculates to be less than the employees' current hourly rate then the system will default … at the current pay rate" (a floor). It also says "If any data is missing to make 52 weeks, then KeyPay will notify you" and "calculations are held against the employee so the user can see how the holiday amount was calculated". No "fixed lookback" statement; it cites "flexible configuration settings". | https://www.keypay.co.uk/features/52-week-averaging | **Contradicted** (J2-001) |
| S9 | ENISA SRP Glossary "Version 1.3", "Last update: 25 September 2026"; 18 common + 13 vulnerability (v19–v30 incl. v26a) + 9 incident fields; Required sets per stage (l. 219–223) | Parsed the HTML table: header text matches. Field counts 18/13/9 match. Required at EW: fields 1–7, v26, i31. At 72h: v21, v26a, i32, i37, i38, i39. At FR: 16, 17, v22–v25, v27, i33–i36. The artifact's lists match. | https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/cra-srp-glossary2 | Confirmed |
| S10 | SRP: "no Application Programming Interface (API) will be provided at the initial release"; "At launch, the platform will be available in English only"; API "may be considered in a future phase" (l. 160, 228) | FAQ 15 and FAQ 24 verbatim. | https://www.enisa.europa.eu/topics/product-security/single-reporting-platform-srp/frequently-asked-questions | Confirmed |
| S11 | EU Login with MFA; one Primary AR per manufacturer and up to 20 Secondary ARs, cited to [6][7] as "two independent secondary sources" (l. 217) | Stated verbatim in the primary ENISA FAQ 9 ("only one Primary AR per manufacturer and up to 20 Secondary ARs"). | same FAQ URL | Confirmed (weak citation choice; see J2-006) |
| S12 | ENISA launch news: "From today, 11 September 2026, manufacturers are required to report actively exploited vulnerabilities" (l. 145) | Verbatim. | https://www.enisa.europa.eu/news/the-cra-single-reporting-platform-is-launched | Confirmed |
| S13 | CRA Art. 14(8) "structured, machine-readable format"; Art. 14(10) Commission "may" specify format by implementing acts (l. 215) | OJ text verbatim. | https://publications.europa.eu/resource/celex/32024R2847 | Confirmed |
| S14 | OSV per-source licences, incl. Ubuntu CC-BY-SA 4.0, Rust CC0, Drupal MIT, Rocky BSD; converted Debian/Alpine/NVD (l. 198) | All 18 entries match the data page. No licence is stated for converted data. | https://google.github.io/osv.dev/data/ | Confirmed |
| S15 | GHSA "licensed under the terms of the CC-BY 4.0 open source license" (l. 199) | README verbatim. It also points to GitHub's additional-product terms, which the artifact did not read (minor). | https://github.com/github/advisory-database | Confirmed |
| S16 | NVD API notice "This product uses the NVD API but is not endorsed or certified by the NVD."; no endorsement; modified content not attributed; rate limits and key; "as is"; nvd.nist.gov is JavaScript-only (l. 200) | All verbatim in the ScanCode copy (generated 2026-09-21). A curl of nvd.nist.gov returns 12 characters of text, which confirms it is JavaScript-only. | https://scancode-licensedb.aboutcode.org/nist-nvd-api-tou.html | Confirmed |
| S17 | CISA KEV "licensed under the CC0 license" (l. 202) | README verbatim; LICENSE is CC0 1.0. | https://github.com/cisagov/kev-data | Confirmed |
| S18 | EUVD: GET, no authentication, max 100 records; daily CVE↔EUVD CSV and consolidated CISA+EU KEV JSON; no licence in docs; ENISA legal notice reproduction clause (l. 203) | apidoc.md confirms all API facts ("Updated daily at 07:00 UTC"). No licence or terms in apidoc.md or faq.md, and the repo has no licence. Legal notice §1.2 verbatim. | https://raw.githubusercontent.com/enisaeu/euvd-docs-public/main/apidoc.md ; https://www.enisa.europa.eu/about-enisa/legal-notice/legal-notice | Confirmed |
| S19 | Xero idea: created 1 Jun 2022, 93 votes; Xero admin 27 Nov 2025 "for the time being this is not a feature we have planned in our roadmap"; workaround reports (l. 295, 344) | All confirmed (status "Accepted"). | https://productideas.xero.com/forums/967118-payroll-expenses/suggestions/45241594-uk-payroll-reporting-run-a-report-to-calculate | Confirmed |
| S20 | Xero comment quotes (l. 308, 352) | Actual: "I am in the process of switching payroll from Xero to Healthbox HR to comply with the law"; "I too am starting to look elsewhere for better software". The artifact's quoted versions are shortened or reworded inside quotation marks. | same | Confirmed in substance; wording altered (J2-005) |
| S21 | DBT is "considering … a more detailed calculator or self-assessment tool to help employers and workers work out holiday entitlement and holiday pay", worked examples, chatbot, webinars (l. 319, 379, 717) | Verbatim ("Examples of the types of support we are considering include …"). The consultation does **not** say "free". That is an inference, reasonable for a GOV.UK/FWA tool. | https://assets.publishing.service.gov.uk/media/6a3e79add52550a19950f617/make-work-pay-holiday-pay-compliance-and-enforcement.pdf | Confirmed (intention); "free" is inference (J2-006) |
| S22 | DBT: reg. 16B "It is up to the employer how they keep those records"; 200% / £20,000 / £100; Royal Assent 18 Dec 2025 limit; "A penalty would not ordinarily be issued where …"; NI devolved (l. 270–272) | All verbatim in the PDF. | same PDF | Confirmed |
| S23 | FWA delivery plan "published 21 Aug 2026"; "Holiday pay enforcement is expected to begin in 2027"; "Ready to communicate new enforcement approach, guidance and tools to support holiday pay compliance" (l. 273) | Quotes verbatim. GOV.UK: "Published: 10 August 2026 Last updated: 21 August 2026". | https://www.gov.uk/government/publications/fair-work-agency-delivery-plan-for-2026-to-2027/fair-work-agency-delivery-plan-2026-to-2027 | Confirmed (date slip; J2-006) |
| S24 | Moneysoft: "not able to calculate the holiday pay rate automatically"; auto 12.07% accrual; no automatic statutory-leave accrual (l. 300, 354) | Verbatim. | https://moneysoft.co.uk/support/holiday-pay-for-irregular-hours-and-part-year-workers/ | Confirmed |
| S25 | Staffology: lookback "Defaults to 52 weeks"; updated 24 Jun 2026; "Only one statutory pay exclusion option can be active simultaneously" (l. 282, 356) | "Defaults to 52 weeks" and "Last updated 24 June 2026" are verbatim. Actual text: "Only one exclusion option can be selected at a time" (reworded inside quotation marks). | https://help.staffology.co.uk/payroll/leave-and-absence/holidays/average-holiday/configuring-average-hol.htm | Confirmed; wording altered (J2-005) |
| S26 | BrightPay "will not calculate holiday pay amounts" (snippet; not in 2025-26 text) (l. 297, 664) | Not present in either the 24-25 or the 25-26 "Useful Information" page text. The artifact already labels it snippet-only and UNKNOWN (conflicting). | https://www.brightpay.co.uk/docs/25-26/annual-leave/holiday-entitlements-useful-information/ | Unverifiable (correctly labelled) |
| S27 | Italy D.Lgs. 7 May 2026 n. 96; GU n. 125 of 1 Jun 2026; in force 7 Jun 2026; 250+ annual and 150–249 triennial, first by 7 Jun 2027; 100–149 from 7 Jun 2031; none below 100; progression exemption below 50; NCBAs "integrate — and not replace"; technical specs by ministerial decree within 90 days after the Garante's opinion (l. 418–424) | Littler (4 Jun 2026) and Edotto (3 Jun 2026) confirm every element. | https://www.littler.com/news-analysis/asap/italy-implements-eu-pay-transparency-directive-guide-final-decree ; https://www.edotto.com/articolo/parita-retributiva-e-trasparenza-salariale-tutte-le-novita-del-decreto-definitivo | Confirmed |
| S28 | Ius Laboris 23.09.26: Minister "expected to adopt ministerial decrees in September"; adoption not found by 26 Sep (l. 423) | Tracker text verbatim. My own search found only "atteso entro settembre" commentary and no adoption. | https://iuslaboris.com/insights/eu-pay-transparency-directive-which-countries-have-transposed/ | Confirmed (UNKNOWN is correct) |
| S29 | Greece Law 5316/2026, Gazette 6 Jul 2026; most obligations from 1 Nov 2026; 150–249 first by 7 Jun 2027, 100–149 by 7 Jun 2031; Ombudsman with digital platform; fines €300–€50,000; SME assistance (l. 433) | Lewis Silkin (13 Jul 2026) verbatim. Search results (Jackson Lewis, Zepos, Bernitsas, Mondaq) agree: voted 2 Jul, "fifth EU Member State". | https://www.lewissilkin.com/insights/2026/07/13/greece-transposes-the-eu-pay-transparency-directive-what-employers-need-to-know | Confirmed |
| S30 | Ius Laboris items: DE "(unconfirmed) rumours" Oct 2026; HU Oct 2026; IE not priority (16 Sep); PT draft 5 Aug; BG 11 Sep; CY Sep 2026 (l. 435–444) | All present in the tracker text. | same Ius Laboris URL | Confirmed |
| S31 | Sweden will not submit a bill; seeks postponement and renegotiation (Pinsent Masons, 20 Apr 2026) (l. 445) | Confirmed. | https://www.pinsentmasons.com/out-law/news/sweden-not-implement-eu-pay-transparency-directive | Confirmed |
| S32 | ENISA SME survey: roles 80/53/39/33; SBOM 67 (34.54%); "None" 21; no answer 20; tools 132 (68.04%); vulnerability-handling templates 56%; channels 57/56/55/46%; ">⅓ of micro no IR plan"; recommendation "without requiring companies to rely on additional tools …" (l. 60, 146–148, 182) | All verbatim in the PDF. SBOM is Q3.3 "technical practices or standards do you currently implement". | https://www.enisa.europa.eu/sites/default/files/2026-06/SME%20CRA%20survey%20report.pdf | Confirmed |
| S33 | ENISA SME survey: financial support 142 (73.20%) is "the highest single item" / "the most requested item" (l. 146, 231, 559) | Key findings: "the joint highest figure … alongside support in terms of templates and checklists for required technical documentation" (also 142, 73.20%). Also: "Practical templates are the most requested form of support". (§7.6 alone says "highest … in this section".) | same PDF | **Partly contradicted** (J2-004) |
| S34 | ENISA SBOM 2026: n=334; >65% large; micro+small 16%; 10% no SBOMs; CycloneDX 44 / SPDX 29 / 11 / 17%; micro 23% and small 25% mature vs 4%/6%; 62% completeness; 30% vendor SBOMs; 43% accelerated; 34% invested; 33% OSS tools; 39% at build; BSI TR-03183-2 ≥1.6 / ≥3.0.1; micro "providing SBOM tools" (l. 61, 149, 158, 189–192) | Every figure found verbatim. | https://www.enisa.europa.eu/sites/default/files/2026-06/SBOM%20Adoption%20State%20of%20Play%202026.pdf | Confirmed |
| S35 | LF (19 Jun 2026): 32% produce SBOMs for all products; 66% unfamiliar; 41% expect full compliance; 48% vs 25% channels (l. 62, 148, 182) | Verbatim; no sample size in the blog (as the artifact says). | https://www.linuxfoundation.org/blog/the-cra-readiness-reality-what-changed-and-what-didnt-between-2025-and-2026 | Confirmed |
| S36 | Dependency-Track 5.1.0 (31 Aug 2026) "mirrors the CISA and ENISA EU KEV catalogs out of the box"; CRA clock referenced; issue #5992 open, 2 Apr 2026, quote (l. 108, 157) | Release note and issue text verbatim. Stars not re-checked (the GitHub API is not reachable from this session). | https://dependencytrack.org/news/dependency-track-5-1/ ; https://github.com/DependencyTrack/dependency-track/issues/5992 | Confirmed |
| S37 | Article 14 Ready: "24h Dry Run" €79 excl. VAT; aligned to glossary v1.1 (5 Sep 2026); not the official SRP; "Incident entries stay in this browser"; compiler free per [21] ("one-time purchase" ambiguous); operator PEAK Consulting (l. 88, 130) | All confirmed. The site shows "v1.0.2 · one-time purchase", and Cyber Vendor Guide says "Its free field compiler runs in the browser" and names PEAK Consulting Services GmbH. The ambiguity is disclosed. | https://article14ready.com ; https://www.cybervendorguide.com/guides/cra-compliance | Confirmed |
| S38 | sbomify Business $159/mo billed annually, 5 products, 200 components, CRA Compliance Wizard (l. 74, 131) | Confirmed ($191 monthly). | https://sbomify.com/pricing/ | Confirmed |
| S39 | Aikido $0/$300/$600; Regulus €2,500/€15,000/yr, early access; Zealience €4,000→€1,000 per licence/yr, Frankfurt; Vulert $15/$25 ($13/$22), SBOM add-on $13/mo, 30-day trial (l. 92–95, 132–135) | All confirmed on the vendor pages. | https://www.aikido.dev/pricing ; https://goregulus.com/ ; https://zealience.com/pricing/ ; https://vulert.com/pricing | Confirmed |
| S40 | Ask HN: 7 points, 6 comments, one-person German firmware GmbH, ~2 Sep 2026, mostly vendor replies; Toradex Munich event. GitHub: cra-agent 452 stars, 114 results (l. 150, 236) | HN confirmed (24 days old; commenters Toradex, ReARM, Vulert). GitHub search shows cra-agent at 452 stars and 115 results today. | https://news.ycombinator.com/item?id=49520688 ; https://github.com/search?q=cyber+resilience+act&type=repositories&s=stars&o=desc | Confirmed |
| S41 | effy.ai: "only 2 of 15 pay-equity tools published figures", used as an O4 "complaint/feature gap" (l. 496) | Verbatim ("Two of fifteen publish a figure"). The 15 tools are US- and enterprise-heavy (Syndio, Trusaic, DCI…). The list excludes Axios and Evenpay, which the artifact itself records as publishing SME-band prices (S4; Evenpay "4 900 € /year" confirmed). | https://www.effy.ai/blog/pay-equity-software ; https://evenpay.io/pricing/ | Partly contradicted as used (J2-006) |
| S42 | SECURE first call "up to € 30.000" per SME, €5m budget, closed (l. 115) | Verbatim; "First call closed". | https://www.secure4sme.eu/cascade-funding/first-open-call | Confirmed |
| S43 | ISTAT: 22,861 enterprises with 50–249 persons employed (snippet) (l. 426) | Found in the PDF: "le medie (50-249 addetti) … 2,2% (22.861 unità in valori assoluti)" (census of firms with ≥3 persons employed). | https://www.istat.it/it/files/2023/11/REPORTCensimprese.pdf | Confirmed (could be upgraded from snippet to read) |

Tally: 38 confirmed (including 3 with minor citation or wording issues), 3 contradicted (S6, S7, S8), 2 partly contradicted (S33, S41). S26 is unverifiable but correctly labelled.

---

## 2. Findings

### J2-001 · HIGH · Criteria 3 (J1-013 comparison fair), 5 (no absence claims), 6 (accuracy), 7 (consistency)
**Issue.** O2's direct competitors are described as lacking capabilities that their own cited pages state. As a result, the §3.6 differentiation claims and the §2.0(b)/§6 "O2 is less contested" framing rest on a false premise. The J1-013 asymmetry has been reversed rather than removed.

**Evidence.**
- l. 362: "Six-year, immutable per-worker ledger and an 'FWA-ready' evidence pack (method, reference weeks, inputs, outputs) — **the one thing not described by paiyroll's page [49]**." The page [49] says: "Holiday pay XLSX reports (data table and accrual) are available at any point to show the data and calculations. You can be assured you have a complete audit trail", and "Generates records and reports for each holiday booking on each pay run" (S6). The six-year duration and "immutable" are not on paiyroll's page. The method/inputs/outputs record is.
- l. 361 offers as a differentiator: "import payroll exports, compute the rate with excluded weeks and a lookback of up to 104 weeks, and document the components used" for "Xero, Sage 50, BrightPay or Moneysoft". paiyroll's page states each element: "looking back 104 weeks to find 52 paid weeks", "import 104 weeks of historical pay data", "specify only the Pay Items that need to be included". Its integration list includes all four named products (S6). The paiyroll row (l. 281) omits the 104-week lookback, the audit trail and Moneysoft.
- l. 283, 355: KeyPay is listed under "complaints and feature gaps" as "lookback fixed at 52 weeks; falls back to the current hourly rate when history is short". The source says the current rate applies only when the average is *lower* (a floor), and that KeyPay *notifies* the user when data are missing. It also says "calculations are held against the employee so the user can see how the holiday amount was calculated", which is an evidence feature the artifact omits (S8).
- Resulting asymmetry: for O1, the existence of SME-priced tools is enough to call under-service "Weak / contradicted" (l. 555), and incumbent gaps (Dependency-Track has no Art. 14 clock) are not counted as under-service. For O2, incumbent gaps in Xero, Moneysoft and Sage 50 are counted as "documented under-service" (l. 76, 303, 555). This is done although a £30/month add-on fills exactly those gaps for exactly those products and advertises the audit trail the artifact claims is missing.

**Why it matters.** J1-013 was forwarded to make the O1/O2 comparison fair, and Agent 3 will choose the lead candidate from §2.0(b), §3.6 and §6. The O2 "evidence pack" differentiator and the "Moderate" under-service rating would mislead that decision. The claim that a competitor lacks something its page states is the kind of absence claim the charter forbids.

**Exact correction required.**
1. Rewrite the paiyroll row (l. 281): add the 104-week lookback and historic import, pay-item selection, "complete audit trail" via XLSX reports of data and calculations, per-booking records per pay run, and the Moneysoft integration. Quote the page.
2. Rewrite §3.6 items 1–2 (l. 361–362). State that calculation, the 104-week lookback and a calculation audit trail are already offered by paiyroll for the named payroll products. Keep only what the evidence shows paiyroll does not describe (six-year retention guarantees, immutability, an FWA-oriented pack format, multi-client bureau view), labelled HYPOTHESIS. Delete "the one thing not described by paiyroll's page".
3. Correct the KeyPay text (l. 283, 355): describe the floor and the missing-data notification accurately, record the stored-calculation feature, and remove it from "complaints" unless a real complaint source exists.
4. Re-assess §6 "Evidence the target segment is underserved" for O2 (l. 555) and the §2.0(b) sentence "By contrast, O2 has documented incumbent gaps" (l. 76). Use the same standard as O1: the incumbent gaps are real, but a published, SME-priced add-on covering those products exists. State the result in evidence terms (e.g., "Weak–Moderate: incumbent gaps documented; the direct add-on covers the gap products; uptake UNKNOWN").

**Responsible agent.** Agent 2

### J2-002 · MEDIUM · Criteria 3 (comparison fair), 7 (internal consistency)
**Issue.** The O1 competitive overlap is overstated relative to the artifact's own §2.1 evidence. This is the other half of the J1-013 fairness problem.

**Evidence.**
- l. 117: "Several **paid SME-priced** tools claim to [combine SBOM matching, actively-exploited triggers, Art. 14 clocks, SRP-glossary drafts, Art. 14(8) notification and evidence retention] (rows 1–5 of §2.1)." The artifact's own rows contradict this:
  - Row 3, Article 14 Ready: "No SBOM link, no persistence by design" (l. 112).
  - Row 1, CVD Portal: "automated SBOM-to-CVE alerts listed only in Enterprise" (l. 86), which is quote-only (confirmed, S1).
  - Rows 4–5, CRA Evidence and Kunnus: prices are "Custom" and "Not published" (l. 89–90), so "SME-priced" is unsupported.
- l. 181: "the SME-priced Art. 14 niche has at least five offers (§2.1 rows 1–6)". Row 6 (sbomify) lists no Art. 14 workflow (l. 91), and rows 4–5 are unpriced. On the artifact's evidence, offers that are both SME-priced and include Art. 14 are CVD Portal, ConformOps and Article 14 Ready.
- l. 556: "Direct SME-priced competitors found: Many (CVD Portal, ConformOps, sbomify, Article 14 Ready, Kunnus, CRA Evidence)" includes two vendors with no published price. O2 by contrast gets "Few (paiyroll; payroll-native features)".
- l. 555: "Weak / **contradicted**". Under-service cannot be *contradicted* by V-grade self-descriptions with no traction, by the artifact's own rule that a V page "shows only what a vendor claims" (l. 25) and its note that no vendor publishes traction (l. 102).

**Why it matters.** Combined with J2-001, both errors push the comparison the same way. Agent 3 would see O1 as more saturated and O2 as more open than the evidence supports.

**Exact correction required.** Restate l. 117, 181 and 556 using only vendors whose published price and published capabilities meet each claim. Name which of the six functions each vendor claims, and put CRA Evidence and Kunnus in an "unpriced" group. Change "Weak / contradicted" (l. 555) to wording that reflects V-grade claims with traction UNKNOWN (e.g., "Weak: 2–3 SME-priced offers claim overlapping Art. 14 functions; traction UNKNOWN").

**Responsible agent.** Agent 2

### J2-003 · MEDIUM · Criteria 1, 2 (O2 buyer identity; substitutes; traction)
**Issue.** Evidence on O2 buyer identity, bureau pricing, traction and free substitutes was on the pages the artifact read or linked, but was missed. The artifact then concludes "Evidence for either route is weak" and "no bureau evidence found".

**Evidence (S7).**
- paiyroll publishes bureau payroll tiers: "Bureau 25 … £50 pcm", "Bureau 75 … £75 pcm", "100+ clients £100 pcm … additional clients £1", with "Holiday pay /schemes" in all tiers. This is a published bureau price anchor (about £1–£2 per client per month for payroll including holiday-pay schemes). It bears directly on V2-1 and V2-4 (l. 393, 396) and on the "switching payroll" substitute (l. 323).
- paiyroll publishes a Customer Success Stories page with named customers (one "resolved holiday pay calculations") and a Trustpilot review titled "Recommend Paiyroll for Bureaus". The artifact states "Published traction: None published" (l. 281) and "no bureau evidence found" (l. 364).
- paiyroll offers a "Holiday Pay Compliance Check … FREE service … Audit holiday pay process" and a free holiday pay template, which are free substitutes missing from §3.2.
- Xero Ideas contains an adviser voice ("This lack of functionality is stopping our client using Xero payroll, so going elsewhere", 25 Apr 2023). The artifact's inference that commenters "write as employers or in-house payroll administrators" (l. 308) is incomplete.

**Why it matters.** Buyer identity is an assigned O2 extra (criterion 2). Bureau pricing and a free competitor audit service change the WTP and substitute picture that Agent 3 and Agent 6 will use.

**Exact correction required.** Add paiyroll's bureau tiers to §3.3 (state that they are full-payroll tiers that include holiday-pay schemes). Add the customer-stories page and the bureau testimonial to the traction column (graded V, "vendor-selected"). Add the free compliance check and template to §3.2. Revise l. 308–310 and V2-1 to reflect the adviser and bureau signals. Keep the conclusion a HYPOTHESIS, with the new evidence cited.

**Responsible agent.** Agent 2

### J2-004 · LOW · Criterion 6 (accuracy)
**Issue.** The artifact reports ENISA's financial-support figure as "the highest single item" (l. 146), "the most requested item" (l. 231) and "top request" (l. 559). ENISA's key findings call it "the joint highest figure … alongside … templates and checklists for required technical documentation" (both 142, 73.20%), and state "Practical templates are the most requested form of support" (S33).

**Why it matters.** The WTP inference still holds (cost pressure is real), but the artifact omits that a tool-like need ties for first place. That is relevant to how negative the WTP signal really is.

**Exact correction required.** Say "joint highest (142, 73.2%), tied with templates for technical documentation" at l. 146, 231 and 559, and cite the key-findings wording.

**Responsible agent.** Agent 2

### J2-005 · LOW · Criterion 5 (no fabricated or altered quotes)
**Issue.** Several passages in quotation marks are paraphrases, not verbatim text:
- l. 308, 352: "I am switching payroll to Healthbox HR to comply". The source says "I am in the process of switching payroll from Xero to Healthbox HR to comply with the law". l. 285 also turns this into "the product they switched to".
- l. 352: "I'm starting to look elsewhere for better software". The source says "I too am starting to look elsewhere for better software".
- l. 356: "Only one statutory pay exclusion option can be active simultaneously". The source says "Only one exclusion option can be selected at a time".

**Exact correction required.** Quote verbatim, or mark omissions with an ellipsis, or remove the quotation marks and label the text as paraphrase. Change "switched to" to "is switching to" at l. 285.

**Responsible agent.** Agent 2

### J2-006 · LOW · Criteria 5, 8 (label, grade and citation hygiene)
**Issue.** Several small discipline slips:
- (a) Label set: "ESTIMATE" (l. 23, 330) is not a charter label. Use SUPPORTED INFERENCE (arithmetic on [49]) or state explicitly that it is an arithmetic illustration under SUPPORTED INFERENCE.
- (b) l. 217 cites [6][7] as "two independent secondary sources" for the AR limits. [7] is sbomify, graded V (l. 613) and a listed competitor. The primary FAQ [3], which the artifact read, states the fact verbatim (S11). Cite [3].
- (c) l. 496 labels a market-level claim "VERIFIED (V)" from a vendor blog, contrary to the artifact's own rule (l. 25). The 15-tool list excludes Axios and Evenpay, which the artifact shows publishing SME prices (S41). Relabel as SUPPORTED INFERENCE limited to that list, or remove it from "complaints".
- (d) The DBT tool is called "free" (l. 717; "Free" cost at l. 319), but the consultation does not say free (S21). Label "free" as SUPPORTED INFERENCE.
- (e) l. 162 reports "search snippets" of CRA misinformation with no source. Cite at least one URL or mark it as unsourced.
- (f) l. 86 attributes "EU/Hetzner" to [24]; the fact comes from [21] (S2).
- (g) l. 273 gives the FWA plan as "published 21 Aug 2026". GOV.UK shows published 10 Aug 2026, last updated 21 Aug 2026 (S23). Also fix [46] at l. 658.
- (h) Sources [11], [34], [38] and [48] are listed as read but never cited in the body. Cite or remove them ([11] matters; see J2-008).
- (i) The ISTAT figure (l. 426, [74]) can be upgraded from snippet to read. The figure is in the PDF (S43).

**Responsible agent.** Agent 2

### J2-007 · LOW · Criterion 3 (J1-013 segment sizing)
**Issue.** MV-O1-01 (l. 256) states that S1 SMEs "are about a third of **CRA-relevant software SMEs**" as SUPPORTED INFERENCE from [8] and [10]. [8] is a whole-sample figure. Its sample includes 27% service providers or integrators and 17% importers or distributors, and 34.54% is computed over all 194 responses including 20 non-answers. [10] is an open-source-ecosystem sample that is not SME-specific. J1-013 flagged exactly this sample-composition problem. §2.0 (l. 68) correctly says "about one third of surveyed firms", but MV-O1-01 extends that to a population it does not measure.

**Exact correction required.** Reword MV-O1-01 to "about one third of surveyed SMEs (all roles) report implementing SBOMs; the share among CRA-relevant software-product SMEs is UNKNOWN". Label it UNKNOWN with a whole-sample proxy, consistent with MV-U01.

**Responsible agent.** Agent 2

### J2-008 · LOW · Criterion 1 (open validation questions carried forward)
**Issue.** Some of Agent 1's approved key questions are neither answered nor carried into the open-question tables:
- O1 Q6 ("When and what will the Commission's simplified technical-documentation form for micro and small enterprises be?"). The artifact read [11], which says only that the Commission "may also establish" such a form, with no date. It never uses that source.
- O4 Q3 (acceptance of a deterministic job-evaluation method by SMEs, worker representatives and equality bodies). This is related to the EIGE toolkit (l. 465) but is not an open question in §4.9.
- O4 Q4 (how far Personio covers Arts. 5–10 in the chosen jurisdiction, and at what price). Personio appears only in a grouped row with no Italian coverage or price (l. 459).

**Exact correction required.** Add a short answer to O1 Q6 from [11] (status: "may", no date → UNKNOWN; also a free-provision risk). Add V4 rows for O4 Q3 and Q4 with the evidence that would answer them.

**Responsible agent.** Agent 2

---

## 3. What is solid (no action needed)
- The O1 extras are strong and accurate: the SRP glossary field and stage mapping (S9), the SRP channel facts (S10, S11), the OSV/GHSA/NVD/KEV/EUVD terms with licence-page citations (S14–S18), the EUVD gating unknown, and the Art. 14 legal minimum (S13).
- All priority prices are confirmed (S1, S3, S4, S5, S38, S39).
- The O2 payroll-coverage table is accurate where it relies on vendor docs (Moneysoft, Staffology, Xero), and the BrightPay and QuickBooks conflicts are honestly left UNKNOWN.
- The J1-015 Royal Assent limit and the self-audit incentive are correctly carried into O2 and into OOS-MV-05.
- The O4 Italy and Greece status, and the other transposition statuses, are accurate and dated. OOS-MV-01, correcting Agent 1's "only Italy" framing, is justified.
- No winner is picked, no numerical scores are given, and no market size is invented. Snippet-only items are marked.

---

## 4. Residual risks for Agent 3 (Strategy)
1. **Do not rely on §3.6 or the §6 O2 under-service rating until J2-001, J2-002 and J2-003 are fixed.** On corrected evidence, both O1 and O2 have at least one published, SME-priced direct competitor covering the core job, and no competitor traction is known for either. The deciding evidence (willingness to pay above existing anchors) is still untested for both candidates, because no customer interviews or pricing tests were run.
2. **Low price anchors on both candidates.** O1: €79–€99/month plus free Dependency-Track and SRP form. O2: 15p/payslip (£30 minimum), and bureau payroll including holiday-pay schemes from £50 pcm for 25 clients. The ENISA financial-support signal and a possible free DBT/FWA calculator are commoditisation risks.
3. **Regulatory volatility.** The DBT consultation response (penalty settings, claim period, 2027 start) is pending. The SRP glossary changed v1.1→v1.3 in three weeks, and an ENISA API "may be considered". The Italian ministerial decree on reporting format was due by about 5 Sep 2026 (90 days after 7 Jun) and is not yet found.
4. **Gating unknowns.** O1: EUVD commercial-reuse terms and the frequency of actively exploited vulnerabilities in SME products (retention risk). O2: employer vs bureau buyer, and Northern Ireland equivalence. O4: the reporting format, a narrow 2027 segment (150–249 only), and a strong local incumbent (Zucchetti).
5. **Secondary-only legal sources.** The Italian and Greek transposition facts rest on law-firm summaries (consistent with each other and with the Directive's dates). The primary texts (Gazzetta Ufficiale / Normattiva; the Greek FEK) should be read before any requirement is built on national details.
6. **Snippet-only items** still need original reads before external use: [20] CVE ToU, [52] BrightPay, [72]–[73], [86] readiness surveys, [88] Awaab's Law PRS status.
