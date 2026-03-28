# Handoff: Researcher → Content Specialist

**Article:** "How to Discover What's Actually Broken in Your SaaS Tool"
**Series:** The SaaS Tax — Part 4
**Date:** 2026-03-19
**Status:** Research complete. Ready for content brief.

---

## What Was Found

### Primary Methodology Frameworks
Three established UX/product research frameworks anchor this article's methodology:

1. **Jobs to Be Done (JTBD)** — reframes workshop questions from "what is broken?" to "what are you trying to accomplish at this step?" Surfaces pain that users have adapted around because they assumed it was unfixable. Popularized by Clayton Christensen / Tony Ulwick (Strategyn).
2. **Critical Incident Technique (CIT)** — developed by John C. Flanagan (1954). Collects specific memorable incidents (times the tool significantly failed) rather than general impressions. Key insight: CIT surfaces high-impact problems, not just frequently-reported ones. One user reporting a critical incident may reveal something more important than a problem reported by ten.
3. **Impact × Frequency Matrix** — Pain vs. Frequency prioritization. Individual scoring before group discussion prevents anchoring bias. When scores diverge by 2+ points, discuss evidence — the goal is calibration, not consensus.

### Key External Stats
- **80% of SaaS features are rarely or never used** (Pendo 2019 Feature Adoption Report — still largest study of its kind)
- **12% of features drive 80% of daily usage** (Pendo 2019)
- Appunite's own audit of Recruitee: **~10% of features actively used**

### Carry-Over Stats (from Parts 1–3 — already verified)
- **24 distinct problems, 7 clusters** from Recruitee workshops (Appunite internal)
- **Direct cost: 22,524 PLN/yr; Total cost incl. opportunity: 150,648 PLN/yr; Build budget: 86,000 PLN** (Appunite internal)
- **Direct ROI: -74%; Full ROI: +75%** (Appunite internal)
- **85% of 150,648 PLN total is opportunity cost** — largest contributor is Cluster 1 (reporting errors, 101,520 PLN/yr)
- Single largest attribution assumption: 50% of failed hires attributable to inaccurate reporting data. Changing from 50% to 0% flips ROI from +75% to -74%.

---

## Key Source URLs
- Pendo Feature Adoption Report: https://www.pendo.io/resources/the-2019-feature-adoption-report/
- NN/G — Critical Incident Technique: https://www.nngroup.com/articles/critical-incident-technique/
- Product School — JTBD Framework: https://productschool.com/blog/product-fundamentals/jtbd-framework
- GLIDR — Pain vs Frequency Scores: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores

---

## Caveats
1. Pendo 2019 is dated but still the largest feature adoption study available — cite with year, no newer study supersedes it
2. JTBD framework has two variants (Christensen vs. Ulwick/ODI) — article does not need to adjudicate; reference as a widely-used product discovery framework
3. Appunite's internal cost numbers and workshop outputs are all verified in prior research cycles — no re-sourcing needed

---

## The Narrative Core the Content Specialist Must Know

**The key insight:** Most companies can list what annoys them about their tools. Few can quantify it rigorously enough to make a build-vs-buy decision. The article bridges this gap.

**The "adapted-around problems" insight:** Users stop noticing certain pain because workarounds become automatic. A simple "what's broken?" question misses this entirely. The CIT and JTBD methods are specifically designed to surface these invisible frictions. This is the article's main narrative value-add — not just presenting a methodology, but explaining *why* the methodology is necessary rather than just asking people what hurts.

**What this approach revealed that "just asking" wouldn't:**
- The time-to-hire discrepancy: Recruitee showed 23 days; real number was 31. No one had complained about it because everyone assumed the tool was right and stopped questioning it.
- Problems people had normalized as "just how hiring works" turned out to be tool-specific and fixable.

**The solvability filter is crucial:** The most common failure mode is blaming the tool for process problems. The three-question filter (software or process? could a different SaaS solve this? requires data ownership?) prevents the analysis from becoming a post-hoc justification.

**The cost estimation split (Column A vs. Column B) is the intellectual honesty requirement:** Direct costs rarely justify the build on their own. But presenting only the full opportunity-cost-inclusive number is misleading. The honest split table forces the decision-maker to name the attribution assumption they're accepting — not a black box number.

---

## Full Research File

All details, worksheets, and methodology content:
`/Users/Blazej/Code/content-team/researcher/research.md`

---
**Status:** Research complete — 5 primary sources, full methodology from internal brief incorporated
