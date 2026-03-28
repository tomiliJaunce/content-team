# Research: "How to Discover What's Actually Broken in Your SaaS Tool"

**Researcher:** content-pipeline / team-lead (web research conducted directly)
**Date:** 2026-03-19
**Article:** Part 4 of "The SaaS Tax" series
**Status:** Complete

---

## 1. Methodology Frameworks Referenced in This Article

### Jobs to Be Done (JTBD)

The JTBD framework, popularized by Harvard professor Clayton Christensen and Tony Ulwick (Strategyn), reframes requirements discovery: instead of asking what users want, you ask what "job" they are hiring the software to do. The distinction matters — features are guesses about solutions; jobs describe outcomes users actually need.

In software requirements discovery, JTBD is most useful during early discovery to determine *what* to build before deciding *how*. Applied to SaaS pain point workshops, it surfaces what workflows teams are actually trying to accomplish — not what the current tool happens to provide.

**Key principle for the article:** When running pain point workshops, JTBD reframes the question from "What is broken in Recruitee?" to "What are you trying to accomplish at this step in the hiring process?" This distinction surfaces pain points that users have adapted around — they stopped asking for a fix because they assumed it wasn't possible, but the underlying job remains unfulfilled.

**Sources:**
- Product School JTBD Guide: https://productschool.com/blog/product-fundamentals/jtbd-framework
- Great Question JTBD Guide 2025: https://greatquestion.co/blog/jobs-to-be-done

---

### Critical Incident Technique (CIT)

Developed by American psychologist John C. Flanagan (1954), CIT collects specific, memorable incidents — moments when a tool significantly helped or failed — rather than general impressions. It surfaces problems users have adapted to because they're too routine to be memorable as complaints, but which cluster around significant friction events.

**Why CIT surfaces adapted-around problems:** Users often don't complain about routine friction because they've normalized workarounds. CIT breaks this by asking: "Tell me about a specific time the tool failed you at a critical moment." Concrete incidents reveal patterns that general satisfaction questions miss.

**Key application for this article:** CIT is the mechanism behind finding problems people "didn't even notice anymore" — the pain points that would not surface in a simple "what bothers you about Recruitee?" question.

**NN/G summary:** CIT focuses on high-impact problems rather than collecting a preponderance of low-importance issues (which most methods produce because they're more numerous). One or two users may pinpoint important issues that others have missed — frequency of report does not equal importance.

**Sources:**
- Nielsen Norman Group — CIT in UX: https://www.nngroup.com/articles/critical-incident-technique/
- UX24/7 — CIT in UX Research: https://ux247.com/critical-incident-technique/

---

### Impact × Frequency Matrix

The Pain vs. Frequency Matrix evaluates pain points on two axes: how often the pain occurs and how severe it is when it does. Produces four quadrants: high-frequency/high-pain (solve first), high-frequency/low-pain (irritants), low-frequency/high-pain (serious but rare), low-frequency/low-pain (deprioritize).

**Key workflow note:** Individual scoring before group discussion prevents anchoring bias. When scores diverge by more than 2 points, discuss the evidence — the goal is calibration, not consensus.

**Sources:**
- GLIDR: Pain vs Frequency Scores: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores
- Smaply: Pain Point Prioritization: https://www.smaply.com/blog/pain-point-prioritization

---

## 2. Carry-Over Stats (Verified in Prior Research Cycles)

These were verified previously and can be reused:

- **80% of SaaS features are rarely or never used** (Pendo 2019 Feature Adoption Report)
- **12% of features drive 80% of daily usage volume** (Pendo 2019)
- Appunite's Recruitee assessment: **~10% of features actively used**
- **24 distinct problems, 7 clusters** identified in Recruitee pain point workshops (Appunite internal)
- **Direct annual cost: 22,524 PLN/yr; Total including opportunity cost: 150,648 PLN/yr; Build budget: 86,000 PLN** (Appunite internal)
- **85% of 150,648 PLN total is opportunity cost** — single largest contributor is Cluster 1 (reporting errors at 101,520 PLN/yr)
- **Direct ROI: -74%; Full ROI: +75%** (Appunite internal, math verified)
- Source for Pendo: https://www.pendo.io/resources/the-2019-feature-adoption-report/

---

## 3. The Full Methodology Content (Internal — From User Brief)

The following is the complete methodology Appunite used. This is the primary content source for sections 2–5 of the article.

### Section A: Feature Usage Audit

**Purpose:** Establish what fraction of the platform you actually use before running pain point discovery. Makes abstract frustrations ("we don't use half of it") concrete.

**Process:**
1. **Build feature list** — from vendor documentation, admin panel walk-through, and daily user interviews. Expect 40–150 features depending on tool. Be specific (not "reporting" but each distinct report type).
2. **Classify each feature** on two axes:
   - *Usage frequency:* Daily / Weekly / Monthly / Never
   - *Requirement level:* Required / Nice to have / Not needed
3. **Calculate usage ratio:** Features used at least monthly ÷ Total features × 100
4. **Calculate required ratio:** Features marked Required ÷ Total features × 100

**Interpretation:**
- Required ratio above 20%: tool may be well-matched, or team has built workflow around tool's structure (both worth examining)
- Required ratio under 15%: territory where a custom build covering that 15% could plausibly replace the full platform

**Common traps:**
- Don't conflate "used daily" with "required" — some daily habits exist only because the current tool forces workarounds
- Don't mark "required" just because it currently exists — ask: if v1 of a replacement didn't have this, would we be blocked?

**Worksheet:** (Feature | Usage Frequency | Requirement Level | Notes)

---

### Section B: Pain Point Discovery Workshop

**Workshop setup:**
- **Participants:** Daily users (2–3 across different workflow areas) + someone who can speak to business impact + decision-maker. Cap at 6 people. Do NOT invite the vendor relationship owner unless also a daily user.
- **Duration:** 90 minutes. First 20 min: individual collection. Next 50 min: discussion, clarification, scoring. Final 20 min: solvability filter. Extend to 2 hours if energy is high.
- **Pre-work:** Share pain point collection template at least 24 hours in advance (Appunite gave a week). Ask for at least 5 entries before arrival. Pre-filled templates produce deeper outputs than blank ones filled in during the session.

**Pain point collection template fields:**
| Field | Definition |
|---|---|
| Description | Specific, concrete. Not "reporting doesn't work well" but "hire count always shows 0% regardless of actual hires" |
| Frequency | Daily / Weekly / Monthly / Quarterly |
| Severity | 1–5 anchored to business consequence (see scale) |
| Current workaround | What the team does today. "Nothing, we just live with it" is a valid answer |
| Time per occurrence | Minutes per workaround. Estimate conservatively — used in cost calculation |

**Severity scale:**
| Score | Definition |
|---|---|
| 1 | Annoying, no workaround needed |
| 2 | Workaround exists, under 5 min, reliable |
| 3 | Workaround exists but time-consuming or introduces data risk |
| 4 | No clean workaround; data quality suffers or significant recurring manual work |
| 5 | Blocking: task cannot be completed, compliance risk, or downstream failures |

Key calibration note: a workaround that takes 10 min and is done = 3. A workaround that introduces data you'll need to reconcile later = 4. A 5 is reserved for genuine blocks, not inconveniences.

---

### Section C: Clustering Methodology

**Why cluster:** Individual pain points often share a root cause. Cost and solvability of the cluster is what matters for the build decision, not individual frictions.

**How to cluster:**
1. Group by feature area (part of the tool where the problem lives)
2. For each group, write a single sentence naming the cluster by its **business consequence**

**Sentence structure:** *[Feature area] does not [capability], which prevents us from [business outcome] / results in [business consequence].*

**Examples:**
- *Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics.*
- *Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics.*
- *It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles.*

**What a good cluster looks like:** 3–8 individual pain points, single dominant feature area, business consequence articulable in one sentence. If 15 pain points under one cluster → probably two clusters. If you can't state the business consequence → cluster isn't ready for cost estimation.

**Appunite result:** 24 individual problems → 7 clusters. Ratio of ~3–4 pain points per cluster is typical for a tool in use for 1+ years.

---

### Section D: The Solvability Filter

**Why this matters:** The most common way this assessment goes wrong is teams use it to confirm a decision already made — they blame the tool for everything, numbers favour building, and 6 months later 3 pain points exist in the new system because the root cause was never the software.

**Three questions per cluster:**

**Q1: Is this a software problem or a process problem?**
Test: If we had unlimited configuration in the current tool, would this problem still exist? Yes → process problem. Build won't fix it.

**Q2: Could a different SaaS solve this?**
Switching SaaS is almost always cheaper and faster than building. Bar for building: no existing product solves this adequately, or switching cost across all pain points exceeds build cost. If a different SaaS solves 2 of 7 clusters, factor that in.

**Q3: Does solving this require data ownership or custom logic no SaaS can provide?**
This is where building typically wins. If the pain requires querying data in ways the vendor doesn't expose, building workflows that don't exist in any available tool, or maintaining context outside any vendor's data model — custom software has a structural advantage switching cannot address.

**Appunite's answer to Q3 on ATS:** Ability to track candidate relationships over time, surface past candidates for new roles based on competency data, and own full history of every interaction. No ATS evaluated offered this as a native feature.

---

### Section E: Cost Estimation Framework

**Budget ceiling rule:** Maximum build budget should not exceed two years of current SaaS subscription cost, plus 20%. Rationale: if you spend the full budget, break-even is 2 years assuming 100% of problems solved and opportunity cost estimates accurate — both are optimistic, hence the ceiling.

*Example: 43,000 PLN annual subscription → ceiling = (43,000 × 2) × 1.2 = 103,200 PLN.*

**Two cost types (kept visibly separate):**

**Direct costs** — time your team loses to workarounds. Formula:
*Occurrences per month × minutes per occurrence × (hourly rate ÷ 60) × 12 = annual direct cost*

Use fully-loaded cost rate (not base salary). Fully-loaded includes employer taxes, benefits, equipment, overhead — typically 30–40% above gross salary. Working assumption: monthly gross salary × 1.35 ÷ 168 hours = hourly rate.

**Opportunity costs** — downstream business impact. For each cluster, capture:
- Downstream consequence (specific, not "worse hiring" but "increased failed hire rate")
- Consequence size (financial value of one occurrence)
- Frequency (occurrences per month)
- Gross opportunity cost (consequence × frequency × 12)
- Attribution % (what % of this consequence is actually caused by the software vs. other factors?)
- Attributed opportunity cost (gross × attribution %)

**The attribution % is the uncomfortable part.** Appunite's largest assumption: 50% of failed hires attributable to inaccurate reporting data. That one assumption drove 67% of total estimated opportunity cost. Changing it from 50% to 0% turned +75% ROI into -74% ROI.

**Break-even attribution test:** Calculate minimum attribution % required for break-even. If break-even requires 80% attribution but your estimate is 30%, you're proceeding on belief — document it explicitly.

**Honest split table:**
| | Column A: Direct costs only | Column B: Direct + opportunity |
|---|---|---|
| Annual cost of current pain | Direct costs only | Direct + attributed opp. costs |
| Build budget | [budget] | [same] |
| ROI | (A − budget) ÷ budget | (B − budget) ÷ budget |
| Payback period | Budget ÷ A savings | Budget ÷ B savings |
| Break-even attribution | N/A | Min % opp. costs that must be real |

If Column A ROI is positive: strong case, defensible under scrutiny.
If Column A ROI is negative and Column B positive: you're betting on attribution assumptions. Frame it honestly.

**If case only works in Column B:** Pick 2–3 attribution assumptions driving the gap. Design quick validations (1–2 week sanity checks, not research projects). For the bad-data-to-bad-decisions assumption: pull 12 months of hiring outcomes, look for correlation with reporting reliability by role/stage. For manual-workaround-to-delay assumption: time a single recruitment cycle end-to-end, break by stage.

---

## 4. Research Gaps / Caveats

- JTBD framework — popularized by Clayton Christensen but Tony Ulwick (Strategyn) originated ODI variant. For this article, cite as widely-used product discovery framework without needing to adjudicate between variants.
- Pendo 2019 Feature Adoption Report is the best available data on feature usage; no newer study has superseded it with larger sample.
- All Appunite internal numbers (24 problems, 7 clusters, cost figures) are verified in prior research cycles. No need to re-source.
- The "adapted-around problems" framing is the key narrative insight of this article — problems users stopped noticing because they built workarounds so automatic they're invisible. This is the gap between "just asking" and running structured methodology.

---

## 5. Key Source URLs

- Pendo Feature Adoption Report: https://www.pendo.io/resources/the-2019-feature-adoption-report/
- NN/G — Critical Incident Technique: https://www.nngroup.com/articles/critical-incident-technique/
- Product School — JTBD Framework: https://productschool.com/blog/product-fundamentals/jtbd-framework
- GLIDR — Pain vs Frequency Scores: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores
- Smaply — Pain Point Prioritization: https://www.smaply.com/blog/pain-point-prioritization
