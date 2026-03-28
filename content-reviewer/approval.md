# Review: "How to Discover What's Actually Broken in Your SaaS Tool"

**Reviewer:** Content Reviewer (content-pipeline team)
**Article:** The SaaS Tax — Part 4
**Author:** Błażej Cepil
**Date:** 2026-03-19
**Status: PASS WITH CHANGES**

---

## Verdict

**PASS WITH CHANGES**

The article is structurally sound, tonally clean, and delivers every required element except for three blocking items. Two are factual omissions (86,000 PLN build budget absent from Section 5; 50% attribution assumption not named). One is an ambiguous internal reference ("Section 4 of the cost model") that will confuse readers. Additionally, one sentence requires author confirmation before publish (the "three days" claim). All other criteria across fact accuracy, brief compliance, tone, SEO, and clarity pass cleanly.

---

## 1. Fact Accuracy

| Claim | Source | Status |
|---|---|---|
| 80% of features rarely or never used | Pendo 2019 — confirmed in research.md Section 2 | VERIFIED |
| 12% of features drive 80% of daily usage | Pendo 2019 — confirmed in research.md Section 2 | VERIFIED |
| Pendo 2019 noted as still the largest study, no newer study superseded it | Brief requirement and research.md — present in article Section 2 Part 1 | VERIFIED |
| ~10% of Recruitee features actively used (Appunite internal) | research.md Section 2 | VERIFIED |
| 24 pain points, 7 clusters | research.md Section 2 | VERIFIED |
| Total cost 150,648 PLN/yr | research.md Section 2 — present in TL;DR and Section 4 | VERIFIED |
| Direct cost 22,524 PLN/yr | research.md Section 2 — present in Section 4 | VERIFIED |
| 85% of total is opportunity cost | research.md Section 2 — present in Section 4 | VERIFIED |
| Cluster 1 (reporting errors) at 101,520 PLN/yr | research.md Section 2 — present in Section 3 narrative | VERIFIED |
| 23-day Recruitee vs. 31-day actual time-to-hire | research.md Section 2 — present in Section 4 as lead example | VERIFIED |
| CIT developed by John C. Flanagan (1954) | research.md — present in Section 1 with NN/G citation | VERIFIED |
| JTBD popularized by Clayton Christensen and Tony Ulwick / Strategyn | research.md — present in Section 1 with Product School citation | VERIFIED |
| Individual scoring before group discussion prevents anchoring bias | research.md (GLIDR) — present in Section 2 Part 2 | VERIFIED |
| Divergence of 2+ points triggers discussion; calibration not consensus | research.md (GLIDR) — present in Section 2 Part 2 | VERIFIED |
| All four source URLs present in footer | Pendo, NN/G, Product School, GLIDR — all four present | VERIFIED |
| Build budget 86,000 PLN — required in Section 5 | research.md Section 2 — ABSENT from article Section 5 | FAIL |
| Attribution assumption: 50% of failed hires attributable to reporting data | research.md Section E — ABSENT from article | FAIL |
| Direct ROI -74% / Full ROI +75% | research.md Section 2 — not required by brief explicitly, but needed to anchor the Column A/B table in Section 5 | FAIL (see note) |

### Fact accuracy notes

**FAIL 1 — 86,000 PLN build budget absent from Section 5.**
The brief (Section 6 data table, placement: "Section 5 reference") requires the build budget figure to appear in Section 5. The Column A/B table in Section 5 uses "[your budget]" as a placeholder in the Build Budget row. Appunite's actual figure of 86,000 PLN is never stated in the article. This also means the -74% direct ROI and +75% full ROI figures are absent, which leaves the Column A/B table as a template with no worked Appunite example — weakening the section's credibility as "here's exactly what we did." Required fix: add one sentence giving Appunite's specific numbers (86,000 PLN build budget, -74% direct ROI, +75% full ROI) in or immediately after the Column A/B table.

**FAIL 2 — 50% attribution assumption not named.**
Research.md Section E is explicit: "Appunite's largest assumption: 50% of failed hires attributable to inaccurate reporting data. That one assumption drove 67% of total estimated opportunity cost. Changing it from 50% to 0% turned +75% ROI into -74% ROI." The brief's Section 5 instruction says: "If the build only works in Column B, name the attribution assumption that drives the gap." The article gives this advice generically ("name the attribution assumption") but does not apply it to Appunite's own case. The 50% figure is never stated anywhere in the article. This is a material omission — naming the assumption is the entire point of the Column A / Column B split. Required fix: name the 50% assumption explicitly in Section 4 or Section 5 (see Change 1 below for combined fix with FAIL from clarity section).

**NOTE — "Section 4 of the cost model" phrasing (also a clarity blocking issue).**
Section 4, final paragraph: "That is why Section 4 of the cost model is where most of the uncertainty lives." There is no "Section 4 of the cost model" in any document readers have seen or will see. Part 2 of the series covers the financial model but is not presented to readers with numbered internal sections. The writer correctly flagged this in Judgment Call #5. This sentence must change. Recommended replacement integrates FAIL 2 fix: "That is why the attribution assumption for Cluster 1 is the most important number to examine before committing. Appunite's assumption was that 50% of failed hires traced back to inaccurate reporting data — one number that moves the ROI from -74% to +75%. Changing it changes everything." This resolves both the confusing reference and the missing attribution assumption.

---

## 2. Brief Compliance

| Requirement | Status | Notes |
|---|---|---|
| Length: 2,000–2,500 words (prose from TL;DR through closing) | PASS | Full file wc = 3,641 total words. Accounting for metadata header, table cell content, horizontal rules, and sources list, body prose estimate is 2,100–2,300 words — within range. Writer's note about table content counting as primary content is correct per brief intent. |
| TL;DR present and 60–80 words | PASS | Present. Approximately 75 words including the Part 3 parenthetical. Brief ceiling is 75 (brief says 50–75). At ceiling but not over. Non-blocking. |
| TL;DR extractable as standalone summary | PASS | Reads coherently without surrounding context. States the method (four steps), the output (24 problems, 150,648 PLN), and the claim (replicable in a week). |
| All 5 sections present in correct order | PASS | Section 1 (why methodology), Section 2 (methodology), Section 3 (clustering output), Section 4 (what it revealed), Section 5 (how to do it yourself) — all present, correctly ordered. |
| Section 2 has all four sub-parts | PASS | Feature audit (Part 1), workshop (Part 2), clustering (Part 3), solvability filter (Part 4) — all present with correct structures. |
| Feature audit worksheet table (4 columns) | PASS | Present. Columns: Feature, Usage Frequency, Requirement Level, Notes — correct. |
| Pain point collection template table (5 fields) | PASS | Present. All 5 fields: Description, Frequency, Severity, Current workaround, Time per occurrence — correct. |
| Severity scale table (5 levels with definitions) | PASS | Present. All 5 levels with definitions matching research.md and brief exactly. |
| Calibration note present | PASS | Present: "a workaround that takes 10 minutes and is done = 3. A workaround that introduces data you will need to reconcile later = 4. A 5 is reserved for genuine blocks, not inconveniences." |
| Column A / Column B cost split table | PASS (partial) | Table is present with correct structure and all required rows. FAIL on Build Budget row — shows "[your budget]" not Appunite's 86,000 PLN. See Fact Accuracy FAIL 1. |
| Section 3 has all 7 cluster rows with business consequence sentences | PASS | All 7 clusters present in table, all 7 business consequence sentences present, wording matches research.md and brief exactly. |
| Section 4 opens with narrative, NOT cost figures | PASS | Section 4 opens: "The most interesting finding was not the 24 problems. It was the problems nobody had thought to report." Costs appear only in the fourth paragraph of the section. |
| 23-day/31-day narrative used prominently in Section 4 | PASS | Present as the lead example. Writer's extended JTBD framing (connecting to "getting an accurate number to make headcount decisions") earns its additional ~50 words — it explains the mechanism, not just the symptom. |
| All four cross-links present | PASS | Part 1 (The SaaS Tax): Section 5 Step 1 — correct. Part 2 (hold-my-beer): Section 3 and Section 5 — correct. Part 3 (why-we-chose-ats-first): TL;DR parenthetical — present (see placement note). Part 5 forward reference: Section 5 closing — present, no URL. All four satisfied. |
| Part 3 cross-link placement | NON-BLOCKING | Brief allowed "Intro or TL;DR as natural series reference." TL;DR parenthetical placement works. Link text is clean and does not damage TL;DR extractability. Acceptable as written. Writer offered an alternative placement in Section 1 closing — viable but not required. |
| Author: Błażej Cepil | PASS | Present in metadata. |
| Series: The SaaS Tax — Part 4 | PASS | Present in metadata. |
| Recruitee framed as mismatch, not failure | PASS | Recruitee is never disparaged. The framing is consistent: the mismatch is between Appunite's evolved process and what any general-purpose ATS was designed to handle. The solvability filter section explicitly acknowledges some problems were process problems, not Recruitee's fault — this actively protects against the "Recruitee is bad" framing the brief prohibits. |
| Solvability filter given full weight | PASS | Section 2 Part 4 gives it genuine prominence. "I think the solvability filter is the most underrated step in this entire process" is appropriate authorial voice (first-person "I" for judgment). All three questions present with their tests. Appunite's Q3 answer included. |
| Forward reference to Part 5 is description only, no URL | PASS | "The next post covers the full pain point breakdown — all 7 clusters, every pain point, and the cost methodology behind each number." No URL. Correct. |

---

## 3. Tone

### Banned word scan (all words from tone-of-voice.md absolute bans)

| Word / Phrase | Found? |
|---|---|
| delve | NO |
| tapestry | NO |
| vibrant | NO |
| nestled | NO |
| groundbreaking (figurative) | NO |
| rich (figurative) | NO |
| intricate / intricacies / interplay | NO |
| cultivate / fostering (figurative) | NO |
| testament | NO |
| indelible / enduring | NO |
| pivotal | NO |
| crucial | NO |
| landscape (abstract noun) | NO |
| underscore (as verb meaning "emphasize") | NO |
| showcase (as verb) | NO |
| garner | NO |
| resonate | NO |
| align with | NO |

**Result: CLEAN.** Zero banned words found.

### Structural red flag scan

| Pattern | Found? |
|---|---|
| "stands as / serves as / marks a" | NO |
| "boasts" | NO |
| "highlighting the importance of" | NO |
| "reflecting broader trends in" | NO |
| "contributing to" | NO |
| "Additionally," as paragraph opener | NO |
| "In today's [landscape/world]" | NO |
| "It is worth noting that" | NO |
| "Needless to say" | NO |

**Result: CLEAN.**

### Floating analytical clauses

Scanning for present-participle sentence endings ("...underscoring," "...highlighting," "...reflecting," "...fostering," "...demonstrating"):

**Result: CLEAN.** None found anywhere in the article.

### Vague attribution

**Result: CLEAN.** All claims are attributed to named sources (Pendo 2019, GLIDR, NN/G, Product School) or stated as first-person Appunite experience ("we found," "our audit found," "we ran"). No "experts say," "industry reports show," or "many companies find" constructions present.

### "Not just X but Y" constructions

**Result: CLEAN.** None found.

### "Additionally," paragraph openers

**Result: CLEAN.** None found.

### Double hyphens used as dashes in prose

**Result: CLEAN.** All em dashes are proper typographic em dashes (—). Horizontal rules use `---` which is correct markdown syntax, not prose dashes.

### Overall register assessment

The article achieves the required tone throughout. Section 1 earns buy-in without being preachy — the adapted-around problems concept is explained with a specific, relatable mechanism (the Tuesday workaround, the metric everyone uses). The "The pain is real. The signal is invisible." line is well-deployed: short declarative sentences for emphasis, used once, not repeated. Section 2 reads as something a team lead could genuinely hand to a colleague. The Part 4 solvability filter section uses first-person "I" correctly for authorial judgment ("I think the solvability filter is the most underrated step") — this is exactly the right register for methodology articles. The 23-day/31-day narrative in Section 4 has genuine momentum. The article does not tip into manifesto energy (the concern for Part 2) and is not dry or academic. The enthusiasm for the methodology is present without being forced.

---

## 4. SEO

| Keyword | Status | Locations |
|---|---|---|
| "SaaS audit methodology" | PARTIAL | Concept present throughout but exact phrase does not appear as a string. Brief target: 2–3 placements. One natural insertion: Section 2 intro ("This is a four-part process" could become "This SaaS audit methodology is a four-part process"). |
| "software pain point discovery" | PARTIAL | "Pain point discovery workshop" present as a sub-header. "Pain point discovery" without "software" appears. Exact phrase "software pain point discovery" absent. Brief target: 2–3 placements. |
| "build vs buy requirements" | PARTIAL | "build-vs-buy decision" present in TL;DR and Section 5. Concept of requirements and solvability filter covered thoroughly. Exact phrase absent. Brief target: 1–2 placements. |
| Recruitee (named entity) | PASS | Present in TL;DR, Section 2 Part 1, Section 3, Section 4. |
| Pendo (named entity) | PASS | Named in Section 2 Part 1 with year (2019) and context note. |
| JTBD / Jobs to Be Done (named entity) | PASS | Named in Section 1 with full attribution (Clayton Christensen, Tony Ulwick / Strategyn). "JTBD framing" used in Section 4. |
| Critical Incident Technique / Flanagan (named entity) | PASS | Named in Section 1 with "John C. Flanagan (1954)" attribution and NN/G link. |
| Błażej Cepil (named entity) | PASS | Present in metadata. Normal for this series. |

### SEO summary

The three primary keyword phrases are present as concepts but not as exact strings. The brief target was 2–3 placements each. Forcing exact insertions into mid-paragraph prose would degrade readability. However, one targeted insertion per keyword in a section opener, header, or strong declarative sentence would satisfy the brief requirement without feeling forced. This is non-blocking.

---

## 5. Clarity and Flow

### Section 1: Why "what's broken?" is the wrong first question

Does its job well. The adapted-around problem is established with a clear mechanism before JTBD and CIT are introduced. The framing that users "stopped noticing" is concrete — not vague theory. JTBD and CIT are introduced with just enough attribution and application to be credible without over-explaining for a technically literate audience. The closing transition ("These two reframes — JTBD for what to ask, CIT for how to ask it — are what separate a structured discovery methodology from a complaint session. The next section is that methodology.") is a clean pivot.

No clarity issues.

### Section 2: The methodology

All four parts execute cleanly. The numbered lists and tables are well-integrated with explanatory prose. The required structures (worksheet, template, severity scale, solvability filter questions) are all present and formatted correctly.

**Flag — "three days" claim (writer's Judgment Call #3).**
"I have seen teams run shorter versions in three days when they needed to move quickly." This is first-person asserted experience. The writer flagged uncertainty about whether Błażej has personally observed this. If he has not, this sentence must change to "Teams have run compressed versions in as few as three days" or be cut. The structural impact of cutting it is zero. This requires author confirmation before publish — reviewer cannot resolve it.

The GLIDR citation in Section 2 Part 2 appears mid-paragraph ("individual scoring before group discussion prevents anchoring bias — when scores diverge by two or more points, discuss the evidence behind each score ([GLIDR on pain vs. frequency scores])"). The link placement is functional but would read more cleanly if the hyperlink moved to the sentence end. Non-blocking.

### Section 3: How we clustered 24 problems into 7 themes

Executes its purpose: makes the methodology concrete by showing Appunite's actual output. The 7-cluster table is correct and complete. The post-table narrative adds genuine value — the observation about "problems that appeared unrelated during the workshop turned out to share a single root cause" demonstrates real discovery rather than scripted outcome. The Cluster 1 / 101,520 PLN mention is placed correctly in the narrative after the table, not in the table itself (matching brief instruction). Part 2 cross-link is natural.

No clarity issues.

### Section 4: What this approach revealed that "just asking" wouldn't

The narrative opens correctly with the adapted-around problem, not with numbers. The 23-day/31-day example is the strongest paragraph in the article — specific, concrete, and illustrates the methodology's value precisely. The JTBD connection to "getting an accurate number to make headcount decisions" is earned, not forced.

**BLOCKING — "Section 4 of the cost model" phrasing.**
Final paragraph: "That is why Section 4 of the cost model is where most of the uncertainty lives — and why naming the attribution assumption explicitly is the most important thing you can do before committing to a build." No "Section 4 of the cost model" exists in any document the reader has seen. Part 2 is the financial model post, but readers have not seen it structured as numbered sections. This will read as a broken internal reference. Required fix: replace this sentence and use the opportunity to introduce the missing 50% attribution assumption (Fact Accuracy FAIL 2). Suggested replacement: "That is why the attribution assumption for Cluster 1 is the most important number to examine before committing. Appunite's assumption was that 50% of failed hires traced back to inaccurate reporting data — one number that moves the ROI from -74% to +75%. Changing it changes everything." This resolves both the confusing reference and the missing attribution assumption in approximately the same word count.

### Section 5: How to do this yourself

The 7-step checklist is clear, complete, and actionable. The Column A/B table is present with the correct structure. Part 1 and Part 2 cross-links are placed correctly. The forward reference to Part 5 closes the section cleanly — "The next post covers the full pain point breakdown — all 7 clusters, every pain point, and the cost methodology behind each number" creates pull without hype.

**BLOCKING — Build budget absent.**
The Column A/B table Build Budget row shows "[your budget]" with no Appunite example figure. 86,000 PLN is entirely absent from the article. The fix is one sentence added in or after the table: "For Appunite's Recruitee assessment: build budget 86,000 PLN, Column A ROI -74%, Column B ROI +75%." This demonstrates the template with real numbers, which is the entire purpose of including the table.

---

## Required Changes (Blocking)

### Change 1 — Fix "Section 4 of the cost model" phrasing and add 50% attribution assumption (Section 4, final paragraph)

**Current text:**
> "That is why Section 4 of the cost model is where most of the uncertainty lives — and why naming the attribution assumption explicitly is the most important thing you can do before committing to a build."

**Required replacement (suggested):**
> "That is why the attribution assumption for Cluster 1 is the most important number to examine before committing. Appunite's assumption was that 50% of failed hires traced back to inaccurate reporting data — one number that moves the ROI from -74% to +75%. Changing it changes everything. The full breakdown is in [Part 2](https://appunite.com/blog/hold-my-beer-building-custom-ats)."

This simultaneously resolves: the confusing "Section 4 of the cost model" reference, the missing 50% attribution assumption (Fact Accuracy FAIL 2), and adds the -74%/+75% ROI figures that the Column A/B table in Section 5 implies but does not state.

### Change 2 — Add 86,000 PLN build budget to Section 5 (Column A/B table or adjacent sentence)

**Required addition:** One sentence giving Appunite's specific figures in or immediately after the Column A/B table. Suggested placement: as a note row in the table or as a sentence following the table: "For Appunite's Recruitee assessment: build budget 86,000 PLN, Column A ROI -74%, Column B ROI +75%."

### Change 3 — Author confirmation required for "three days" claim (Section 2 intro)

"I have seen teams run shorter versions in three days when they needed to move quickly." This must be confirmed by Błażej before publish. If he has personally seen or run a compressed version: keep it. If not: change "I have seen" to "Teams have run" or cut the sentence entirely. The section structure is unaffected by either change.

---

## Non-Blocking Suggestions

**Suggestion 1 — SEO exact-phrase insertions.**
The three primary keywords ("SaaS audit methodology," "software pain point discovery," "build vs buy requirements") are present as concepts but not as exact strings. One targeted insertion each — in a section opener, closing sentence, or strong declarative sentence — would satisfy the brief's 2–3 placement target without forcing unnatural phrasing. Highest-value insertion: "SaaS audit methodology" in Section 2's opening sentence.

**Suggestion 2 — GLIDR citation placement.**
The GLIDR hyperlink in Section 2 Part 2 appears mid-paragraph. Moving it to a sentence end would improve readability. No content change required.

**Suggestion 3 — TL;DR length.**
The TL;DR runs approximately 75 words — at the brief's ceiling of 75. The Part 3 parenthetical cross-link accounts for ~15 words. If the link is ever moved to the Section 1 closing (the writer's alternative placement), the TL;DR would tighten to ~60 words and be cleaner. Leave as is unless a second edit pass is planned.

---

*Review complete. Draft requires three targeted changes before publish. No structural rewrites needed. After changes are made, article is approved.*
