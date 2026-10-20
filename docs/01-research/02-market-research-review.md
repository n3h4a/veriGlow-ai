# Design Review — `02-market-research.md` v1.0

| Field | Value |
|---|---|
| **Document reviewed** | [`02-market-research.md`](./02-market-research.md) v1.0 |
| **Outcome** | Revised to v2.0 |
| **Review date** | 20 October 2026 |
| **Review lenses** | Product strategy, software architecture, management-consulting quality bar |
| **Verdict on v1** | **Not ready for executive review.** The structure was sound, but two factual overstatements, undisclosed sponsor bias, and missing problem sizing would not survive the first ten minutes of a partner review. |

> [!NOTE]
> Each issue below states **what was wrong**, **why it matters**, and **how v2 fixes it**, with the v2 section where the rewrite lives. Severity: **Critical** = could lead to a wrong decision; **Major** = would undermine credibility in review; **Minor** = polish.

---

## 1. Scorecard

Scores are reviewer judgment on a 1–5 scale (5 = executive-ready).

| Dimension | v1 | v2 | Main driver of change |
|---|:-:|:-:|---|
| Research depth | 3 | 4 | Added recourse, complaint, dupe and verification-landscape research |
| Accuracy | 2 | 4 | Fixed two false "not found" claims, the DPP conflict, and a per-capita misattribution |
| Credibility | 2 | 4 | Evidence-quality register disclosing sponsor bias; one tag per claim |
| Structure | 3 | 4 | Definitions, stakeholders and "case against" sections; de-duplicated insights |
| Readability | 3 | 4 | Four headline conclusions; defined scales; plainer tables |
| Completeness | 2 | 4 | Problem sizing, segments, category risk, recourse stage |
| Business insight | 2 | 4 | Business-model economics; incentives; "so what" on each insight |
| Product thinking | 2 | 4 | Separated need from willingness to act; prioritised P0 questions |
| Technical awareness | 2 | 4 | Distinguished product ID, unit serialisation, freshness and sourcing claims |
| Interview quality | 3 | 4 | Appendix A with evidence-backed answers to hard questions |
| GitHub doc quality | 3 | 5 | Clickable thematic citations; verified anchors and links |

**Why not 5 across the board:** v2 still rests entirely on third-party, mostly self-reported data. Only primary research can move research depth and credibility to 5.

---

## 2. Critical issues

### CR-1 — False claim: "no consumer-facing verification exists"
- **What was wrong.** v1 said no consumer-facing way to verify a unit after delivery was found. **No search for one was ever run.** A targeted search found Amazon Transparency (consumers scan codes in the Amazon or Transparency app; 90,000+ brands, 10 countries), brand-owned QR and hologram labels (e.g., Rasasi), GS1 India's Smart Consumer App, and batch-code date decoders (CheckFresh).
- **Why it matters.** This was the claim closest to a product thesis. An executive who knows about Transparency would have discounted the whole document.
- **Fix.** Reframed as *fragmented, opt-in, brand-by-brand coverage*. Added a verification landscape table that separates what each mechanism actually verifies (product identity, unit validity, freshness, sourcing). → v2 §11.2, §9.3, insight #18.

### CR-2 — Unsearched claim: "quick commerce has no authenticity programme"
- **What was wrong.** Stated as "no publicly documented programme found" without a targeted search.
- **Why it matters.** Same failure mode as CR-1 — absence of evidence presented as evidence of absence.
- **Fix.** Ran a targeted search. Still nothing published; now stated with its search scope. Added the QC recourse evidence that *was* found (returns dissatisfaction; helpline complaint counts). → v2 §9.2 (Quick commerce).

### CR-3 — Sponsor bias undisclosed
- **What was wrong.** Key prevalence statistics came from organisations that profit when the counterfeit problem looks large — ASPA (an association of authentication-solution providers), MarkMonitor, Smart Protection, MarqVision, Red Points — and from platform-commissioned studies (Meta–GWI on Meta platforms; Google on YouTube). None of this was disclosed.
- **Why it matters.** Consultants are trained to ask "who paid for this?" Undisclosed sponsorship is the fastest way to lose credibility in review.
- **Fix.** Added an evidence-quality register (sponsor, interest, method, sample, geography, year, bias risk, intended use). Downgraded affected claims to 🟡. → v2 §2.4.

### CR-4 — No definition of "inauthentic"
- **What was wrong.** Counterfeit, grey-market, unregistered import, expired, tampered and "dupe" products were treated as one problem.
- **Why it matters.** These involve different actors, harms and remedies. Mixing them inflates problem size and will confuse the PRD. A knowing dupe buyer is not a victim.
- **Fix.** Added a definitions table, including Indian legal terms, and YouGov data separating knowing dupe purchases (9% of US adults) from unknowing imitation purchases (~13%). → v2 §3.

### CR-5 — No problem sizing
- **What was wrong.** Market size was given, but not the size of the *problem*.
- **Why it matters.** "How many people does this affect?" is the first executive question. Without an answer, prioritisation is guesswork.
- **Fix.** Added an explicit, assumption-labelled order-of-magnitude frame (~1.5–12 m affected online buyers a year). It deliberately refuses to produce a value-at-risk figure because no defensible input exists. → v2 §4.5, Appendix A.

---

## 3. Accuracy issues

| ID | Severity | v1 problem | Why it matters | v2 fix |
|---|---|---|---|---|
| AC-1 | Major | EU DPP timing for cosmetics shown as "conflicting" | Unresolved conflicts look like unfinished work | Resolved: cosmetics are not in the April 2025 ESPR working plan; the GS1 "Q2 2026" row refers to a Cosmetic Products Regulation revision, not a DPP; Omnibus VI added (§11.3) |
| AC-2 | Major | DPDP Act status "not verified" | Avoidable gap on a material regulatory risk | Verified: Rules notified 14 Nov 2025, phased over 12–18 months (R-REG-3) |
| AC-3 | Major | Per-capita spend of ~US$313 attributed to the US | The source names only "the highest-spending market"; misattribution | Corrected wording (§4.4) |
| AC-4 | Major | LocalCircles 2026 described as "Bengaluru-focused" with "21% via online" | Scope and percentage base are not stated in the source | Marked scope and base unclear; demoted to context (§6.2) |
| AC-5 | Major | "EU losses roughly doubled 2015→2020" presented as a time series | EUIPO methods changed between editions | Added a method caveat; kept the direction only (§7.1) |
| AC-6 | Major | "Only 36% cite price, so purchases are accidental" | Logical leap; ignores 31% knowing buyers (2024) and 20% intentional buyers (vendor study) | Weakened to "suggests"; counter-evidence shown; confidence Low (§7.4, insight #15) |
| AC-7 | Minor | Redseer's ~US$25 bn → ~US$40 bn (~10% CAGR) shown next to its stated 11–14% without comment | Internal inconsistency in a cited source went unnoticed | Flagged ❓ with a reconciliation note (§4.4) |
| AC-8 | Minor | "~40% spread" between market-size definitions | Actual spread is 42–50% | Corrected (§4.1) |
| AC-9 | Minor | Fewer Amazon brand notices read as "the problem is shrinking" | Could equally mean brands report less | Alternative explanation added (§13 #3) |
| AC-10 | Minor | Tira's ~28 stores taken from an aggregator | Same source lists Nykaa at 331 stores vs. Nykaa's own 313 | Marked unreliable with the reason (§9.2) |
| AC-11 | Minor | QC makeup "2.2× Amazon" shown without caveats | One month, one comparator; headline figure inconsistent in source | Caveats added (§5) |
| AC-12 | Minor | FTC penalty shown as fixed | Inflation-indexed annually | "2024, inflation-indexed" (§6.2) |

---

## 4. Credibility and evidence issues

| ID | Severity | v1 problem | Why it matters | v2 fix |
|---|---|---|---|---|
| EV-1 | Major | Mixed tags in one cell ("✅ / 🟡") | Reader cannot tell which part of a claim is solid | One tag per claim where possible; split rows where not (§2.2) |
| EV-2 | Major | India e-commerce counterfeit headline anchored on 2018 data | Stale primary evidence when newer exists | LocalCircles Jan 2025 (>102k responses) promoted to primary; 2018 kept as context (§6.2) |
| EV-3 | Major | Non-India data (US, EU, HK, Ireland) used without a relevance flag | Transferability was assumed silently | Limitations and register flag geography; insights marked "(non-India)" where relevant |
| EV-4 | Minor | Meta–GWI sample includes ages 6–64 | Minors in a purchase-behaviour survey weaken adult inferences | Disclosed in register (§2.4) |
| EV-5 | Minor | LocalCircles 2022 cosmetics panel was 61% male | Panel skew for a cosmetics topic | Disclosed in register (§2.4) |
| EV-6 | Minor | Conclusions had no confidence rating | Executives cannot weigh findings | High/Medium/Low criteria defined; applied to conclusions and insights (§2.3, §15) |

---

## 5. Completeness gaps (missing research)

| ID | Severity | Gap | Why it matters | v2 fix |
|---|---|---|---|---|
| CP-1 | Critical | Recourse not researched | Turned out to be the strongest evidence of harm (41% left with fakes; 43% had no way to report) | New data (LocalCircles 2025; National Consumer Helpline 2025); ninth journey stage "Recourse" (§6.2, §10) |
| CP-2 | Major | No stakeholder or incentive analysis | Who pays and who holds the data determines whether any market can function | Stakeholder map and incentive table (§8) |
| CP-3 | Major | No disconfirming evidence | Team building in this space risks motivated reasoning | "The Case Against" with falsification criteria (§13) |
| CP-4 | Major | No category differentiation | Fragrance, makeup, skincare and sun care differ in harm and verifiability | Category risk profile (§7.2) |
| CP-5 | Major | No segmentation | Opportunities read as one undifferentiated consumer | Hypothesised segments with tests, including a likely non-addressable segment (§12.3) |
| CP-6 | Minor | Import shelf-life rule (>6 months at import) missing from body | Directly relevant to expiry risk | Added (§6.2) |
| CP-7 | Minor | Helpline complaint data unused | Official, recent signal on recourse | Added with a normalisation warning (§9.2–9.3) |

---

## 6. Business insight and product thinking

| ID | Severity | v1 problem | Why it matters | v2 fix |
|---|---|---|---|---|
| BI-1 | Major | Platform profiles described *what* each platform does, not *why* | Strategy reviewers expect the economic logic | Business-model trade-offs table; Purplle's shift used as evidence that control has economic value (§9.1) |
| BI-2 | Major | Unmet need N1 rated "High" despite unknown willingness to act | Conflates pain with demand | Need evidence and action evidence scored separately (§12.1) |
| BI-3 | Major | Executive summary was ten dense bullets with no "so what" | Executives need conclusions, confidence and implications | Four conclusions with confidence; explicit next-phase implications (§1) |
| BI-4 | Major | Key Insights repeated the summary | Duplication without added value | Each insight now carries a "so what" and confidence (§15) |
| BI-5 | Minor | Risks presupposed a specific product (e.g., "trust in the verifier") | Breaks the scope guardrail | Reframed as risks to any entrant in the space (§14) |
| BI-6 | Minor | Open questions not prioritised | Teams cannot tell what blocks a go/no-go | P0/P1/P2 priorities (§16) |

---

## 7. Technical awareness

| ID | Severity | v1 problem | Why it matters | v2 fix |
|---|---|---|---|---|
| TA-1 | Major | "Verification" used as one concept | Product ID (barcode), unit serialisation, freshness (batch date) and sourcing claims are different problems with different data owners | Verification landscape separates the four (§11.2) |
| TA-2 | Major | DPP and GS1 presented as anti-counterfeit tools | DPP is sustainability-driven product data; GS1 Sunrise is a POS barcode transition. Neither authenticates units by itself | Clarified in §11.3–11.5 |
| TA-3 | Minor | No mention that static identifiers can be copied | Basic constraint for any later architecture | R-TEC-4 added (§14.4) |

---

## 8. Structure, readability and GitHub quality

| ID | Severity | v1 problem | Why it matters | v2 fix |
|---|---|---|---|---|
| GH-1 | Major | Citation IDs (R1…R77) were not clickable; inconsistent scheme (gap at R7; ad-hoc IDs like R-ET, R17-AMR) | Readers cannot verify claims quickly; IDs break as sources are added | Thematic IDs (MKT, IND, CON, CF, PLT, REG, TEC) as GFM reference-style links that resolve directly to sources; 107/107 resolve, verified by rendering |
| GH-2 | Minor | Severity, likelihood, impact and maturity labels undefined | Ratings were not reproducible | Scales defined (§10.2, §11.1, §14) |
| GH-3 | Minor | No reading guide | Different audiences need different paths | "How to read this document" note |
| GH-4 | Minor | No interview or executive Q&A preparation | The project explicitly requires interview readiness | Appendix A |

---

## 9. Residual weaknesses in v2 (accepted for now)

1. **No primary research.** Every consumer number is third-party. *Owner:* `04-user-research.md`.
2. **Several India figures rest on press summaries** of reports we could not read in full (ASPA–CRISIL, Redseer). *Action:* obtain the full reports.
3. **The problem-sizing inputs are assumptions.** They are labelled, but still assumptions.
4. **Mermaid diagrams were reviewed manually**, not machine-validated (the package registry was unavailable in the review environment). *Action:* check rendering on GitHub after the first push.
