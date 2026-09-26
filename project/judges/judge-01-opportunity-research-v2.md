# Judge 1 verdict: `project/research/opportunity-research-v2.md` (re-evaluation)

| Field | Value |
|---|---|
| Judge | Judge 1 (independent judge for Agent 1, SaaS Opportunity Researcher) |
| Artifact judged | `project/research/opportunity-research-v2.md` (DRAFT v2, 917 lines) |
| Prior verdict | `project/judges/judge-01-opportunity-research-v1.md`: FAIL (1 HIGH, 5 MEDIUM, 6 LOW) |
| Date of judgment | 2026-09-26 |
| Basis | The artifact text only. The §9 revision log was treated as a claim, and each change was checked in the body. Independent checks by this judge: web fetches, plus local extraction of the DBT consultation PDF, the ENISA SME CRA Survey Report PDF, the Home Office Martyn's Law myth buster PDF, the RSH register xlsx (17 Sep 2026) and ONS EMP17 xlsx (Aug 2026). OJ texts were fetched from `publications.europa.eu/resource/celex/…` (CRA corrigendum, Directive 2023/970, Regulation 2026/1744). |

## Verdict: **PASS**

All 12 v1 findings are resolved in the body of the artifact, not only in the revision log. I found no new BLOCKER, CRITICAL or HIGH problem. Every load-bearing new claim I spot-checked is correct. Four new findings are open (one MEDIUM, three LOW). Under the charter they do not block a PASS, but they should be fixed before downstream agents quote the ranking rationale or the O2 penalty exposure. See J1-013 to J1-016.

### Criteria summary (v2)

| # | Criterion | Result |
|---|---|---|
| 1 | Scope and required sections | Met. 25 areas; full analysis for 10 (O1–O8, O12, O15); one line per field for the rest; 3 recommendations with validation questions; assumptions, sources and out-of-scope sections present. |
| 2 | Evidence discipline | Met. Labels are consistent. Minor residual label hygiene issues (J1-016); one overstated inference (J1-014). |
| 3 | Accuracy | Met. 16 of 16 new or changed claims confirmed (table below); one omission (J1-015). |
| 4 | AI-free filter | Met. O25 fixed. |
| 5 | MVP-feasibility filter | Met. O1 is now segment-conditional, with a stated ingestion boundary and a gating unknown. |
| 6 | Recommendations follow from evidence | Met with a caveat. The re-ranking is reasoned and has a switch condition. One comparison criterion is unevenly applied (J1-013). |
| 7 | Internal consistency | Met with a caveat. The O1 segment is defined inconsistently (J1-013). |
| 8 | Sources and VERIFIED citations | Met. |

---

## 1. Resolution of v1 findings

| ID | v1 severity | Status | Evidence in v2 (line numbers refer to v2) |
|---|---|---|---|
| J1-001 | HIGH | **RESOLVED** | "Legal scope (corrected)" (l. 224–227) states that the law applies to tenancies only and excludes licences, long leases and shared ownership. It correctly adds that tenancy-based temporary and supported housing *is* in scope. I verified this against GOV.UK s.1.5: "Awaab's Law applies to temporary and supported accommodation … where the property is occupied under a tenancy agreement." The almshouse exemption is cited [53]. "~1,100" is now an explicitly labelled upper bound (l. 232–237), and in-scope independent buyers are UNKNOWN. The volunteer-run ASSUMPTION is removed. A-08 and A-09 are revised (l. 734–735). O3 is demoted to the watchlist with reasons (l. 656–659) and revival conditions (l. 716). The §2 row is updated (l. 72). |
| J1-002 | MEDIUM | **RESOLVED** | Rentalize Core, PyramidG2, Landlord Vision (with caveat), HousingSurvey Pro and Made Tech (403, UNKNOWN) are listed as V (l. 244–251, §2 l. 72). "Underserved" becomes a HYPOTHESIS. A traction and pricing question is added (l. 716). I re-checked HousingSurvey Pro: it has a genuine free "Solo plan, full engine, one surveyor seat, no card" plus paid per-surveyor plans, so "free sign-up / free self-serve" is fair. |
| J1-003 | MEDIUM | **RESOLVED** | l. 181–190 now say the RF and TUC figures measure leave denial, dated and taken from DBT [41]. I verified verbatim in the DBT PDF: "2.2 million jobs were not given any annual leave in 2025", "around 1.1 million workers were not given holiday pay in 2023 … £2 billion", "calculating holiday pay entitlement can be complex and can lead to accidental non-compliance and underpayment", and Acas "around 8,000 … and 13,000" claims in 2024/25. A-05 is now a HYPOTHESIS (l. 731). |
| J1-004 | MEDIUM | **RESOLVED** (minor residue, see J1-016) | Martyn's Law figures and quotes come from the primary myth buster. I verified "£330 per year", "£5,210 per year", "without needing to buy specialist services" and "do not endorse any third-party products". The SBOM legal fact is now cited to the OJ [2]. The EAA to [4]. The Art. 69 reproduction is regraded S [28]. Zero-hours now uses ONS EMP17, verified (1,230,049; 3.57%; UK). The Housing Ombudsman claim is withdrawn. "UNVERIFIED" is removed (grep: none). The header is amended (l. 25). |
| J1-005 | MEDIUM | **RESOLVED** | Full structure for O1–O8, O12 and O15 (10 areas). Per-field tables for O9–O11, O13, O14 and O16–O25 (l. 392–617). |
| J1-006 | MEDIUM | **RESOLVED** (wording residue, see J1-013) | Conditional MVP verdict with a stated ingestion boundary (customer-supplied CycloneDX/SPDX; no binary analysis), gating UNKNOWN on EUVD terms, A-19, and §5.4 Q1 (l. 158–161, 686, 745). OSV per-source licences checked: GHSA, PyPI and Go are CC-BY 4.0 (osv.dev data page). |
| J1-007 | LOW | **RESOLVED** (content issue, see J1-013) | §5.3 compares O1 and O2 criterion by criterion, (a)–(g) plus breadth, including (d) and (f). It states the trade-off and a switch condition (l. 664–677). The [30] price anchors are recorded (l. 130–134). I verified them: ConformOps free preview for 2 products, €99 per product one-time, €79/month per product, €249/month for five; Article 14 Ready €79 one-time. |
| J1-008 | LOW | **RESOLVED** | Phase 3 is "date unconfirmed" in §2, §3 and §5 (l. 72, 222). 2027 appears only as a PREDICTION, though the "secondary sources" for it are uncited (trivial). FWA April 2027 is VERIFIED as stated intention, and commencement is a PREDICTION (l. 173, 733). I confirmed with Lewis Silkin (16 Sep 2026): "intends to begin holiday pay enforcement in April 2027". |
| J1-009 | LOW | **RESOLVED** | [27] now lists the report (24 Jun 2026) and the news page (13 Jul 2026) separately. [15] is dated 23 Sep 2026. |
| J1-010 | LOW | **RESOLVED** | Art. 6(2) now says "pay-progression obligation only". I verified in the OJ text: "Member States may exempt employers with fewer than 50 workers from the obligation related to the pay progression set out in paragraph 1". Germany is reworded as an expected, unconfirmed event. The §2 caveat is added (l. 71). |
| J1-011 | LOW | **RESOLVED** (related omission, see J1-015) | GB framing throughout, plus A-18. DBT territorial extent verified: "extend and apply only to England & Wales and Scotland. Employment law is devolved in Northern Ireland". The cap is verified: "a maximum penalty of £20,000 per worker and a minimum penalty of £100". SI 2026/323 reg. 3(8) commences s.35 on 6 Apr 2026 (verified on legislation.gov.uk). |
| J1-012 | LOW | **RESOLVED** | O25 is AI-free "Yes" and rejected on competition (l. 93, 616–617). |

---

## 2. Spot-check table (new or changed claims in v2)

| # | Claim (v2 location) | What the judge found | Source URL | Verdict |
|---|---|---|---|---|
| N1 | RSH register (17 Sep 2026): 1,577 providers (1,253 non-profit, 92 for-profit, 232 LA); 265 with corporate form "Charity"; 108 names containing "alms" (l. 230, 233) | Downloaded and counted locally: 1,577 rows; Non-profit 1,253, Profit 92, Local authority 232; "Charity" form 265; "alms" in name 108 (96 Charity, 11 CIO, 1 charitable company). | https://assets.publishing.service.gov.uk/media/6aad16bcce3f006bd4346c9b/List_of_registered_providers_17_September_2026.xlsx | Confirmed |
| N2 | Awaab's Law applies to tenancy-based temporary and supported accommodation; licences excluded (l. 225) | GOV.UK s.1.5 quotes both points. | https://www.gov.uk/government/publications/awaabs-law-phase-2-guidance-for-social-housing-landlords/awaabs-law-phase-2-guidance-for-social-landlords | Confirmed |
| N3 | DBT consultation 30 Jun–22 Sep 2026: FWA enforcement from 2027; 200% of arrears, **£20,000 max per worker**, £100 min; six-year claim period; GB extent (l. 172, 176) | All verified verbatim in the PDF. The PDF also says claims from before Royal Assent (18 Dec 2025) are not enforceable by the FWA, which v2 omits (J1-015). | https://assets.publishing.service.gov.uk/media/6a3e79add52550a19950f617/make-work-pay-holiday-pay-compliance-and-enforcement.pdf | Confirmed (omission noted) |
| N4 | FWA intends holiday-pay enforcement from **April 2027**; priority sectors (l. 173, 178) | Lewis Silkin, 16 Sep 2026: "intends to begin holiday pay enforcement in April 2027"; social care and construction, with retail and hospitality also flagged; 200% capped at £20,000. | https://www.lewissilkin.com/insights/2026/09/16/the-fair-work-agencys-first-delivery-plan | Confirmed |
| N5 | CRA Art. 64(10) corrigendum (2 Jul 2025): "paragraphs 3 to 9" → "2 to 9" (l. 109, [3]) | OJ L 2025/90555 text: "for: 'By way of derogation from paragraphs 3 to 9 …' read: 'By way of derogation from paragraphs 2 to 9 …'". | https://publications.europa.eu/resource/celex/32024R2847R%2802%29 | Confirmed |
| N6 | CRA price anchors €79–€249/month; €99 one-off; Article 14 Ready €79; CVD Portal free tier (l. 130–134, 151, 688) | Cyber Vendor Guide (Aug 2026): ConformOps free preview (2 products), €99 per product one-time, €79/month per product, €249/month for five; Article 14 Ready €79 one-time; CVD Portal free intake tier plus paid tiers. | https://www.cybervendorguide.com/guides/cra-compliance | Confirmed |
| N7 | ENISA report: roles 41% software dev, 20% final product, 14% ICT hardware, 14% component; size 27/36/37%; 67 (34.5%) SBOM; 47 (24.2%) threat modelling; 142 financial support "joint-highest"; >⅓ of micro-companies have no IR plan; CC BY 4.0 (l. 113, 119–124, OOS-10) | All verified in the PDF: Q1.5 answers 28/80/28/39 (14.43/41.24/14.43/20.10%); sizes 53/69/72; SBOM 67 (34.54%); threat modelling 47 (24.23%); "joint highest figure … alongside … templates"; "More than one third (36 %)" of micro-companies; CC BY 4.0 notice. Note: service providers and integrators are 27% of respondents, which v2 does not mention. | https://www.enisa.europa.eu/sites/default/files/2026-06/SME%20CRA%20survey%20report.pdf | Confirmed |
| N8 | ONS EMP17 (18 Aug 2026): ~1.23m (3.6%) on zero-hours contracts, Apr–Jun 2026, UK-wide (l. 178) | Table 1: Apr–Jun 2026 = 1,230,049; 3.573%; "UK, not seasonally adjusted". | https://www.ons.gov.uk/employmentandlabourmarket/peopleinwork/employmentandemployeetypes/datasets/emp17peopleinemploymentonzerohourscontracts | Confirmed |
| N9 | Martyn's Law myth buster: £330 / £5,210 per year; "without needing to buy specialist services"; no endorsement of third-party products (l. 319–320) | All verified verbatim in the PDF. | https://assets.publishing.service.gov.uk/media/69281f35b3b9afff34e960f0/martyns-law-mythbuster.pdf | Confirmed |
| N10 | Directive 2023/970 Art. 6(2), 7(4), 9(2)–(4), 10(1), 34(1) as quoted (l. 265–272) | Verified in OJ XHTML: progression-only exemption; "in any event within two months"; 7 Jun 2027 / 7 Jun 2031 schedule; ≥5% / not justified / not remedied within six months; 7 Jun 2026. | https://publications.europa.eu/resource/celex/32023L0970 | Confirmed |
| N11 | Reg. (EU) 2026/1744: OJ 24 Jul 2026; Annex III to 2 Dec 2027, Annex I to 2 Aug 2028; Art. 4 "take measures to support the development of AI literacy … does not require … any specific level" (l. 428) | Verified in OJ text. | https://publications.europa.eu/resource/celex/32026R1744 | Confirmed |
| N12 | OSV per-source licences: GHSA, PyPI, Go = CC-BY 4.0 (l. 146, A-03) | OSV data page lists these as CC-BY 4.0 (Rust CC0; Ubuntu CC-BY-SA 4.0). | https://google.github.io/osv.dev/data/ | Confirmed |
| N13 | SI 2026/323 commences ERA 2025 s.35 on 6 Apr 2026 (l. 170) | SI 2026/323 (made 16 Mar 2026), reg. 3(8): s.35 in force 6 Apr 2026. | https://www.legislation.gov.uk/uksi/2026/323/made | Confirmed |
| N14 | Rentalize Core from €199/month; 60-home example €695/month (snippet) (l. 245) | Search summary of Rentalize pages: entry €199/month (25 properties); 60-home association €695/month. | https://rentalize.com/ | Confirmed (snippet, correctly labelled) |
| N15 | UK B2B/B2G e-invoicing from Apr 2029; Peppol confirmed 23 Jun 2026; roadmap at the Nov 2026 Budget (l. 338, 342) | Multiple secondary sources confirm. | https://www.vatcalc.com/united-kingdom/uk-2029-mandatory-b2b-e-invoicing/ ; https://sovos.com/regulatory-updates/vat/uk-confirms-adoption-of-peppol-as-the-framework-for-its-upcoming-e-invoicing-mandate/ | Confirmed |
| N16 | CSSF RoI window 11 Feb–31 Mar 2026; plain-CSV files in a ZIP with a predefined folder structure; wider validation (l. 413) | CSSF page confirms all three. | https://www.cssf.lu/en/2026/02/dora-submission-timeframe-for-register-of-information-edesk-portal-open-as-of-11-february-2026/ | Confirmed |

---

## 3. New findings

### J1-013 · MEDIUM · Criteria 6 (recommendations follow from evidence), 7 (internal consistency)
**Issue.** The narrowed Rank 1 (O1) segment is defined inconsistently. Criterion (c) in the §5.3 comparison is also scored with evidence that does not apply to that segment, and competitors are treated differently for O1 and O2.
**Evidence.**
- *Segment wording:* "software-product SMEs whose builds **already produce** SBOMs" (l. 12); "Connected-hardware makers only where their builds **already emit** SBOMs" (l. 69); "can **export**" (l. 114); "who **can supply**" (l. 159); "Do target customers **already produce** SBOMs" (l. 686). "Already produce" and "can export or supply" describe populations of very different size.
- *Criterion (c):* §5.3 (l. 670) gives O1 the "underserved" edge, citing "34.5% use SBOMs; >70% want templates [27]". These are whole-sample SME figures, and the sample includes 27% service providers and integrators and ~17% importers or distributors (N7). If the segment is SMEs that already produce SBOMs, the 34.5% statistic bounds the segment's size (≤ about a third of respondents, and the more mature ones). It is not evidence that this segment is underserved.
- *Competitor asymmetry:* for O2, "a dedicated add-on exists [48]" counts against O2. For O1, the artifact's own [30] records ConformOps selling continuous monitoring at €79/month per product and a €249/month five-product portfolio plan (N6), and CVD Portal selling Art. 14 workflow tiers. That is at least as direct an SME-priced overlap with the O1 MVP, yet (c) is scored for O1 as "fragmented new vendors".

**Why it matters.** Criterion (c) is one of three edges behind O1's Rank 1. If (c) is scored "Even" or for O2, the §5.3 tally is balanced on the artifact's own framing. The order then rests only on (b) and breadth. Agent 2 needs the segment definition to be exact to size and sample it.
**Exact correction required.**
1. Choose one segment definition (recommended: "SMEs whose build tooling can export CycloneDX/SPDX SBOMs") and use it at l. 12, 69, 114, 159, 686 and §5.4.
2. In §5.3 (c), either re-score it "Even" (or for O2), or give segment-specific evidence of under-service. State that [27] is not segmented by role and that SBOM non-users would need to start generating SBOMs before the MVP can serve them.
3. Score ConformOps continuous monitoring and CVD Portal tiers under (c) the same way paiyroll is scored for O2.
4. Re-state the §5.3 trade-off and the Rank 1 "Why" (l. 683) accordingly. The switch condition can stay.

**Responsible agent.** Agent 1

### J1-014 · LOW · Criterion 2 (evidence discipline)
**Issue.** "A paying market for a calculation add-on exists" (l. 695) and "paying market for a £30/month-minimum add-on [48]" (l. 671) rest only on paiyroll's own price page (grade V). A published price shows that an offer exists. It does not show that paying customers exist, and the artifact's own rule (l. 18) says V sources only show what a vendor *claims*.
**Exact correction required.** Reword to "a calculation add-on is offered at a published price (15p/payslip, £30/month minimum) [48]; customer uptake UNKNOWN". Add uptake to the O2 key questions.
**Responsible agent.** Agent 1

### J1-015 · LOW · Criterion 3 (accuracy of O2 exposure)
**Issue.** v2 says the FWA "would investigate up to six years back" (l. 172) and cites a "6-year look-back" as part of O2's consequence (l. 196, §5.3 (b) l. 669). It omits a limit stated in the same DBT source [41], which v2 lists as read: "Holiday pay claims will not be enforceable by the FWA if they occurred before Royal Assent … Royal Assent was 18 December 2025 so claims from before this date cannot be enforced by the FWA."
**Why it matters.** For enforcement starting in 2027, FWA exposure only covers periods from 18 Dec 2025. Even at enforcement start that is a little over a year, not six. The artifact overstates near-term exposure, and that feeds the (b) comparison and any future sales messaging.
**Exact correction required.** Add the Royal Assent limit with a citation [41] wherever the six-year look-back appears (l. 172, 196, 669). Note that the six-year *record-retention* duty (reg. 16B) is separate and unaffected. Note that the proposed claim period is still subject to the consultation outcome.
**Responsible agent.** Agent 1

### J1-016 · LOW · Criteria 2, 8 (label hygiene residue)
**Issue.**
- (a) l. 283 supports a VERIFIED claim with "also confirmed by Judge 1 spot-check S16". A judge's verdict is not a research source, so the artifact must stand on its own citations.
- (b) The same line cites [17] (Lewis Silkin, 10 Mar 2026). That article predates the Commission's refusal (reported 22 May 2026), so it cannot support "The Commission refused …". The two independent snippets are the two URLs inside [16].
- (c) l. 354 labels EAA enforcement events (Carrefour court order, ACM audits, no fines) VERIFIED on [74]. Those sources are vendor or vendor-adjacent blogs, graded V/S. The new rule at l. 18 says V sources never verify a legal fact.

**Exact correction required.** Remove the judge reference and [17] from l. 283 (keep [16], or read Agence Europe). For l. 354, either add one non-vendor source (regulator, court or reputable press) or relabel as UNKNOWN or SUPPORTED INFERENCE.
**Responsible agent.** Agent 1

---

## 4. Residual risks for downstream agents

1. **O3 upper bound.** The 835–990 range subtracts all 265 "Charity"-form providers from the ~1,100 *small* PRPs. The Charity list contains non-almshouse entries, and some may be large providers already excluded (for example Bournville Village Trust appears with Charity form). So the lower figure may over-subtract. The range is labelled SUPPORTED INFERENCE and O3 is only on the watchlist, so no finding is raised. If O3 is revived, recompute using RSH size data.
2. **O1 remains exposed to fast-moving SME-priced competition**, including €79/month per-product monitoring. Agent 2's pricing interviews are the decisive test, and the §5.3 switch condition should be applied literally.
3. **O2 penalty regime is still a proposal.** The DBT consultation closed on 22 Sep 2026. The penalty settings, claim period and April 2027 start are unconfirmed until the government response.
4. **Pay transparency status is volatile.** Only Italy is fully transposed per [15], so O4 (Rank 3, conditional) depends on events after 26 Sep 2026.
5. **Summarised web reads.** Snippet-level sources in A-17 still need verbatim re-reads before external use. v2's OOS-08 tip (the `publications.europa.eu` CELEX endpoint) worked for this judge and should be used for legal quotes.
