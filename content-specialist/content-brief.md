# Content Brief: How to Discover What's Actually Broken in Your SaaS Tool

**Prepared by:** Content Specialist
**Date:** 2026-03-19
**For:** Content Writer
**Series:** The SaaS Tax — Part 4
**Author byline:** Błażej Cepil (first person — "we" for Appunite decisions, "I" for authorial judgment)
**Content type:** Blog post — methodology delivery
**Estimated length:** 2,000–2,500 words

---

## 1. Article Metadata

| Dimension | Value |
|---|---|
| Title | How to Discover What's Actually Broken in Your SaaS Tool |
| Series | The SaaS Tax — Part 4 |
| Journey Stage | Edukacja (Education) |
| Primary Audience | Tier 1 CTOs / Heads of Engineering who want to replicate Appunite's methodology |
| Goal | Teach the methodology. Position Appunite as people who ask the right questions. |
| Tone | Enthusiastic, educational. Sage archetype. Practical and replicable. |
| Author | Błażej Cepil |
| SEO Targets | "SaaS audit methodology", "software pain point discovery", "build vs buy requirements" |
| Estimated Length | 2,000–2,500 words |

---

## 2. Strategic Context

### Series Position

| Post | Title / Topic | Status |
|---|---|---|
| #1 | "The SaaS Tax — You're Paying for 100%, Using 12%" | Published |
| #2 | "Hold My Beer — We're Building Our Own ATS (The Manifesto)" | Published |
| #3 | "Why We Chose ATS as Our First Custom Replacement" | Published |
| **#4** | **"How to Discover What's Actually Broken in Your SaaS Tool"** | **This article** |
| #5 | Full pain point breakdown (all 7 clusters with costs) | Upcoming |

### What the reader knows

By Part 4, the reader knows: the SaaS tax is real (Part 1), Appunite decided to build their own ATS and found 24 problems costing 150,648 PLN/year (Part 2), and they chose ATS as the first replacement using a four-question scoring framework (Part 3). What they do not know yet is *how* the 24 problems were actually discovered. They are now asking: "How did you actually find all of this? Could I do the same thing for my stack?"

This article answers that question end-to-end with a replicable methodology.

### Core argument

Most companies can list what annoys them about their tools. Few can quantify it rigorously enough to make a build-vs-buy decision. Here is the structured approach Appunite used to go from "Recruitee is frustrating" to "here are 24 specific problems costing us 150,648 PLN per year."

### What makes this article different from the series so far

- Part 2 was announcement energy — declaring a bet, presenting the financial case
- Part 3 was analytical/framework — the decision tool for choosing what to replace first
- **Part 4 is educational/methodological** — enthusiastic and practical, "here's exactly how we did it, and here's how you can do it too"

The writer must internalize this shift. Part 4 has a different texture: it is designed to be *used*, not just read. Worksheets and tables belong here.

---

## 3. Audience

### Primary: Tier 1 — CTOs / Heads of Engineering

They have read Parts 1–3. They found the numbers in Part 2 convincing but want to generate equivalent numbers for their own stack. They are not looking for inspiration — they are looking for a process they can run with their team next week.

**What hooks them:** Concrete methodology with templates they can use immediately. The revelation that structured discovery finds problems you would never find by just asking people.

### Secondary: Tier 2 — Amplifiers

Engineering leaders who share "this is how we run rigorous discovery" content. The methodology needs to stand alone as useful regardless of the Appunite/Recruitee specifics.

---

## 4. Tone

**Archetype:** Sage. A senior practitioner sharing exactly how they did something, with enough detail to replicate it.

**Register:** Enthusiastic and practical. This is the "show your work" article — Błażej has genuine enthusiasm for the methodology and it should come through. Not evangelism, not cheerleading — the enthusiasm of someone who found a method that actually works.

**First person conventions:**
- "we" = Appunite's decisions, actions, findings ("we ran the workshop", "we found 24 problems")
- "I" = Błażej's authorial judgment ("I think the solvability filter is the most underrated step", "In my experience...")
- Never "Appunite believes" or "the company decided"

**Rhythm:** Vary sentence length. Short for declarative points. Longer for reasoning. Some paragraphs are one sentence. Don't write in uniform paragraph sizes.

**Formatting:** This article is designed to be used, so worksheets and tables are appropriate here — more so than in other parts of the series. But use headers only for genuine navigation, not for decoration. Prose for explanatory passages; structured formats only where the content demands structure.

---

## 5. Section-by-Section Instructions

---

### TL;DR / Opening (50–75 words)

**Format:** TL;DR block at the top, per series convention.

**Content:** Most companies can tell you what annoys them about their tools. Few can quantify it rigorously enough to support a build-vs-buy decision. This post walks through the exact methodology Appunite used to go from "Recruitee is frustrating" to 24 specific problems costing an estimated 150,648 PLN per year — and how to run the same process yourself.

**The TL;DR must be extractable as a standalone summary.** An AI quoting it verbatim should produce a coherent result.

---

### Section 1: Why "what's broken?" is the wrong first question (~250–300 words)

**Purpose:** Establish WHY methodology is necessary — not just introduce the methods. This is the section's entire job.

**Opening:** Do not open with a definition of discovery methods or a generic statement about tools. Start from the reader's experience: they already know something is off with their SaaS tool. The question is whether they are looking for it in the right way.

**Required content for this section:**

**The complaint-list problem.** When you ask people "what's broken?", you get a list of recent frustrations. What you do not get are the problems they have adapted around — the workarounds that have become so automatic that users no longer experience them as problems. The pain is real. The signal is invisible.

**The JTBD reframe.** Jobs to Be Done reframes the question: not "what is broken in this tool?" but "what are you trying to accomplish at this step?" This surfaces the underlying job — the outcome the user actually needs — rather than opinions about the current tool's implementation. The distinction matters because users who have workarounds for problems no longer report those problems, even in direct interviews. The job remains unfulfilled; the user just stopped asking.

Reference JTBD as a widely-used product discovery framework (popularized by Clayton Christensen and Tony Ulwick / Strategyn). Do not adjudicate between the Christensen and Ulwick variants. One sentence of attribution is sufficient.

**Source to cite:** Product School JTBD Guide: https://productschool.com/blog/product-fundamentals/jtbd-framework

**The CIT insight.** Critical Incident Technique (developed by John C. Flanagan, 1954) collects specific memorable incidents rather than general impressions. The key insight: one user reporting a critical incident may reveal something more important than the same low-stakes problem reported by ten. High-impact incidents matter more than frequently-reported ones. This is the mechanism behind finding adapted-around problems — asking "tell me about a specific time this tool failed you at a critical moment" breaks the workaround habit.

**Source to cite:** Nielsen Norman Group on CIT: https://www.nngroup.com/articles/critical-incident-technique/

**Closing the section:** These two reframes — JTBD for what to ask, CIT for how to ask it — are what separate a structured methodology from a complaint session. The next section is the methodology.

**What NOT to do here:** Do not preview all four methodology steps. That is Section 2's job. Section 1 earns the reader's buy-in for why methodology is necessary — that's all.

---

### Section 2: The methodology (~700–900 words)

**Purpose:** Deliver the complete, replicable discovery methodology across four parts. This is the article's primary content. The writer should approach this as writing something a team lead could hand to a colleague and say "run this."

**Important format note:** Include the worksheet tables and template structures exactly as specified below. Do not summarize them in prose instead. The article is designed to be used, and users need the actual templates.

---

#### Part 1: Feature usage audit (~150–200 words)

**Purpose of this step:** Establish what fraction of the platform you actually use before running pain point discovery. Makes abstract frustrations concrete ("we don't use half of it" becomes a ratio with a number attached).

**Process (present in numbered list):**
1. Build the feature list — from vendor documentation, admin panel walkthrough, and daily user interviews. Expect 40–150 features depending on the tool. Be specific: not "reporting" but each distinct report type.
2. Classify each feature on two axes: Usage frequency (Daily / Weekly / Monthly / Never) and Requirement level (Required / Nice to have / Not needed).
3. Calculate usage ratio: Features used at least monthly ÷ Total features × 100
4. Calculate required ratio: Features marked Required ÷ Total features × 100

**Include this worksheet table:**

| Feature | Usage Frequency | Requirement Level | Notes |
|---|---|---|---|
| [Feature name] | Daily / Weekly / Monthly / Never | Required / Nice to have / Not needed | [Optional context] |

**Interpretation to include:**
- Required ratio above 20%: tool may be well-matched, or the team has built workflow around the tool's structure (both worth examining)
- Required ratio under 15%: territory where a custom build covering that 15% could plausibly replace the full platform

**The common traps to name:**
- Daily usage does not equal Required — some daily habits exist because the current tool forces workarounds
- Do not mark Required just because the feature currently exists. The test: if v1 of a replacement didn't have this, would we be blocked?

**Appunite's result to include:** Their Recruitee audit found approximately 10% of features actively used. Compare this to the Pendo 2019 finding that 12% of features drive 80% of daily usage across the industry — Appunite's number tracks closely with the pattern.

**Source to cite for Pendo:** https://www.pendo.io/resources/the-2019-feature-adoption-report/ — note it as "still the largest study of feature adoption available; no newer study has superseded it." Cite year (2019) explicitly.

---

#### Part 2: Pain point discovery workshop (~200–250 words)

**Purpose of this step:** Structured elicitation of pain points using CIT and JTBD framing, with individual scoring before group discussion.

**Workshop setup (include these specifics):**
- Participants: 2–3 daily users from different workflow areas, someone who can speak to business impact, a decision-maker. Cap at 6 people. Do NOT invite the vendor relationship owner unless they are also a daily user.
- Duration: 90 minutes. First 20 min: individual collection. Next 50 min: discussion, clarification, scoring. Final 20 min: solvability filter. Extend to 2 hours if energy is high.
- Pre-work: Share the collection template at least 24 hours in advance (Appunite gave a week). Ask for at least 5 entries before the session. Pre-filled templates produce deeper outputs than blank ones filled in during the session.

**Include this pain point collection template:**

| Field | Definition |
|---|---|
| Description | Specific and concrete. Not "reporting doesn't work well" but "hire count always shows 0% regardless of actual hires" |
| Frequency | Daily / Weekly / Monthly / Quarterly |
| Severity | 1–5 anchored to business consequence (see scale below) |
| Current workaround | What the team does today. "Nothing, we just live with it" is a valid answer. |
| Time per occurrence | Minutes per workaround. Estimate conservatively — used in cost calculation. |

**Include this severity scale:**

| Score | Definition |
|---|---|
| 1 | Annoying, no workaround needed |
| 2 | Workaround exists, under 5 min, reliable |
| 3 | Workaround exists but time-consuming or introduces data risk |
| 4 | No clean workaround; data quality suffers or significant recurring manual work |
| 5 | Blocking: task cannot be completed, compliance risk, or downstream failures |

**Calibration note to include:** A workaround that takes 10 minutes and is done = 3. A workaround that introduces data you will need to reconcile later = 4. A 5 is reserved for genuine blocks, not inconveniences.

**Source to cite for the Impact × Frequency matrix approach:** GLIDR: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores — individual scoring before group discussion prevents anchoring bias. When scores diverge by 2+ points, discuss the evidence — the goal is calibration, not consensus.

---

#### Part 3: Clustering methodology (~150–200 words)

**Purpose of this step:** Group individual pain points by root cause, not symptom. The cost and solvability of a cluster — not an individual pain point — is what drives the build decision.

**How to cluster (include in numbered list):**
1. Group by feature area — the part of the tool where the problem lives
2. For each group, write a single sentence naming the cluster by its business consequence

**Sentence structure to include (format as a callout or distinct block):**
> [Feature area] does not [capability], which prevents us from [business outcome] / results in [business consequence].

**Appunite examples to include (all three):**
- *Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics.*
- *Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics.*
- *It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles.*

**What a good cluster looks like:** 3–8 individual pain points, single dominant feature area, business consequence articulable in one sentence. If 15 pain points land under one cluster, it is probably two clusters. If you cannot state the business consequence in one sentence, the cluster is not ready for cost estimation.

**Appunite result:** 24 individual problems → 7 clusters. The ratio of roughly 3–4 pain points per cluster is typical for a tool that has been in use for a year or more.

---

#### Part 4: The solvability filter (~150–200 words)

**Purpose of this step:** The most common failure mode is blaming the tool for problems that are actually process problems. The solvability filter is the intellectual honesty requirement. Do not minimize it.

**Why this matters (include this framing):** Without a solvability filter, pain point analysis becomes post-hoc justification. Teams find 24 problems, assume they all require new software, build the tool, and six months later three of those problems still exist — because the root cause was never the software. The filter is what separates a rigorous assessment from wishful thinking.

**Include all three questions with their tests:**

**Q1: Is this a software problem or a process problem?**
Test: If we had unlimited configuration in the current tool, would this problem still exist? Yes → process problem. Building new software will not fix it.

**Q2: Could a different SaaS solve this?**
Switching SaaS is almost always cheaper and faster than building. The bar for building: no existing product solves this adequately, or the switching cost across all pain points exceeds the build cost. If a different SaaS solves 2 of 7 clusters, factor that in before deciding to build.

**Q3: Does solving this require data ownership or custom logic no SaaS can provide?**
This is where building typically wins. If the pain requires querying data in ways the vendor does not expose, building workflows that do not exist in any available tool, or maintaining context outside any vendor's data model — custom software has a structural advantage that switching cannot address.

**Appunite's answer to Q3 to include:** The ability to track candidate relationships over time, surface past candidates for new roles based on competency data, and own the full history of every interaction. No ATS evaluated offered this as a native feature.

---

### Section 3: How we clustered 24 problems into 7 themes (~250–300 words)

**Purpose:** Show Appunite's actual output from the clustering step. Make the methodology concrete by showing what it produced. Illustrate how seemingly different complaints connect to the same root cause.

**Key points to make:**
- The categorization logic: 24 problems did not feel like 24 separate things once clustering was done. Most problems traced back to 7 root failures in the tool.
- The ratio of roughly 3–4 pain points per cluster is typical for a tool in use for a year or more — by that point, users have found most of the friction, even if they have normalized it.
- Individual complaints that seemed unrelated often shared a single root cause once the cluster sentence was written.

**Include the 7 cluster names with their business consequence sentences (these come from the research, include them all):**

| # | Cluster | Business consequence |
|---|---|---|
| 1 | Reports calculate with errors | Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics. |
| 2 | Metrics not customisable | Metrics cannot be configured to match our actual process, limiting pipeline visibility to whatever the vendor decided to surface. |
| 3 | Funnels not elastic | Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics. |
| 4 | No competency matrices + sourcing inefficiency | It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles. |
| 5 | No interview transcription + manual feedback | There is no structured way to capture or review interview content, meaning hiring signal is lost and each evaluation cycle depends on memory rather than data. |
| 6 | Calendar/scheduling gaps + workflow coordination | Scheduling and coordination require manual effort for every step, adding friction to each hiring cycle and increasing time-to-hire. |
| 7 | GDPR compliance gaps + manual processing | GDPR-required actions cannot be automated, creating compliance risk and recurring manual processing that scales with hiring volume. |

**Note to writer:** The cost breakdown by cluster (101,520 PLN for Cluster 1, etc.) is the full cost table from Part 2. Do NOT reproduce it here. Reference Part 2 for the detailed numbers. This section is about the clustering methodology and its output, not the financial model.

Cross-link Part 2: https://appunite.com/blog/hold-my-beer-building-custom-ats

---

### Section 4: What this approach revealed that "just asking" wouldn't (~250–300 words)

**Purpose:** Demonstrate the value of structured methodology versus informal discovery. Make the "adapted-around problems" insight concrete using Appunite's specific examples.

**Critical opening instruction:** Do NOT open this section with cost figures. Start with the narrative insight — the discovery of invisible problems. Bring in costs after the narrative is established.

**The narrative to tell:**

The most interesting finding was not the 24 problems. It was the problems that nobody had thought to report.

**The 23-day / 31-day discrepancy is the key example — use it prominently.** Recruitee reported a time-to-hire of 23 days. The actual number was 31. No one had flagged this as a problem, because everyone assumed the tool was right and had stopped questioning it. This is the adapted-around problem in its purest form: the pain is real and measurable, the workaround is invisible (using whatever number the tool gives you), and no one registers it as a friction point because the expectation of accuracy was abandoned so gradually that the moment of abandonment is unlocatable.

**Other examples to include:**
- Problems people had normalized as "just how hiring works" turned out to be tool-specific and fixable. The JTBD framing — "what are you trying to accomplish here?" — surfaced these: when users described their actual goal rather than their experience of the current tool, the gap became visible.
- The solvability filter caught one or two items that were process problems masquerading as tool problems. Without the filter, those would have been scoped into a build, built, and not fixed — because the root cause was never the software.

**Then bring in the broader point:** Structured methodology finds these things because it creates the conditions for them to surface. Direct questions get direct answers. The JTBD and CIT methods are specifically designed to get around the human tendency to adapt and stop noticing.

**You may mention the cost figures briefly here** (150,648 PLN total, 22,524 PLN direct) to connect the narrative to the numbers — but this section's job is the insight, not the financial breakdown. The full breakdown is in Part 2.

---

### Section 5: How to do this yourself (~250–300 words)

**Purpose:** Give the reader a practical starting point. Frame this as something any team lead can run in a week, without specialist UX knowledge.

**Opening framing:** This methodology does not require a research background. It requires blocking time, preparing templates, and being rigorous about the solvability filter.

**Include a practical checklist (numbered):**

1. Pick one SaaS tool with documented friction — something your team complains about regularly, or that you suspect is mis-matched with your process.
2. Build the feature list from the vendor's documentation and a 30-minute walkthrough. Aim for completeness; specificity matters more than speed.
3. Run the feature audit with 2–3 daily users. Calculate your usage ratio and required ratio.
4. Send the pain point collection template to workshop participants at least 24 hours in advance. Ask for 5+ entries before the session.
5. Run the 90-minute workshop (or 2 hours if the group is engaged). Individual scoring first, group calibration second.
6. Cluster the pain points by feature area. Write the business consequence sentence for each cluster before moving to cost estimation.
7. Apply the solvability filter to every cluster. Do not skip this step.

**Reference the Column A / Column B cost split from research.md Section E.** Include it as follows:

When you move to cost estimation, keep two columns visibly separate:

| | Column A: Direct costs only | Column B: Direct + opportunity |
|---|---|---|
| Annual cost of current pain | Time your team loses to workarounds | Direct costs + attributed opportunity costs |
| Build budget | [your budget] | [same] |
| ROI | (A − budget) ÷ budget | (B − budget) ÷ budget |
| Payback period | Budget ÷ A savings | Budget ÷ B savings |
| Break-even attribution | N/A | Minimum % of opportunity costs that must be real to justify the build |

Column A is the defensible case. Column B is the ambitious case. If the build only works in Column B, name the attribution assumption that drives the gap — and design a 1–2 week sanity check before committing. (See Part 2 for how Appunite handled this: https://appunite.com/blog/hold-my-beer-building-custom-ats)

**Forward reference to Part 5:** The next post covers the full pain point breakdown — all 7 clusters, every pain point, and the cost methodology behind each number. If you want to see exactly how a specific cluster was costed, that post will have it.

**Cross-link Part 1 somewhere in this section** to connect back to the series origin: https://appunite.com/blog/the-saas-tax

---

## 6. Data Points the Writer Must Use

All verified. Use exactly as cited.

| Fact | Source | Placement |
|---|---|---|
| 80% of SaaS features are rarely or never used | Pendo 2019 Feature Adoption Report | Section 2, Part 1 (feature audit) |
| 12% of features drive 80% of daily usage | Pendo 2019 Feature Adoption Report | Section 2, Part 1 |
| Appunite's Recruitee assessment: ~10% of features actively used | Appunite internal | Section 2, Part 1 |
| 24 distinct problems, 7 clusters | Appunite internal | Section 2 (Part 3 / clustering), Section 3, Section 4 |
| Direct annual cost: 22,524 PLN/yr | Appunite internal | Section 4 (narrative reference), Section 5 |
| Total annual cost including opportunity: 150,648 PLN/yr | Appunite internal | TL;DR, Section 4, Section 5 |
| 85% of total cost is opportunity cost | Appunite internal | Section 4 (supporting the narrative) |
| Single largest cluster: Cluster 1 (reporting errors) at 101,520 PLN/yr | Appunite internal | Section 3 (table) |
| Build budget: 86,000 PLN | Appunite internal | Section 5 reference (do not re-run full financial model) |
| Time-to-hire discrepancy: Recruitee showed 23 days, real was 31 | Appunite internal | Section 4 — this is the key concrete example |
| CIT developed by John C. Flanagan (1954) | NN/G | Section 1 |
| JTBD popularized by Clayton Christensen / Tony Ulwick (Strategyn) | Product School | Section 1 |
| Individual scoring before group discussion prevents anchoring bias | GLIDR | Section 2, Part 2 |
| When scores diverge by 2+ points, discuss evidence — goal is calibration, not consensus | GLIDR | Section 2, Part 2 |

**Source URLs:**
- Pendo Feature Adoption Report: https://www.pendo.io/resources/the-2019-feature-adoption-report/
- NN/G — Critical Incident Technique: https://www.nngroup.com/articles/critical-incident-technique/
- Product School — JTBD Framework: https://productschool.com/blog/product-fundamentals/jtbd-framework
- GLIDR — Pain vs Frequency Scores: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores

**Do not invent statistics.** If a claim needs a number and none exists in this brief or the research file, write from Appunite's direct experience: "In our experience..." or "The teams we work with tell us..."

---

## 7. Cross-Link Requirements (Non-Negotiable)

| Link Target | URL | Required Placement |
|---|---|---|
| Part 1: The SaaS Tax | https://appunite.com/blog/the-saas-tax | Section 1 or Section 5 (natural reference to the series origin) |
| Part 2: The Manifesto | https://appunite.com/blog/hold-my-beer-building-custom-ats | Section 3 (when referencing the cost table) and Section 5 (Column A/B reference) |
| Part 3: Why We Chose ATS | https://appunite.com/blog/why-we-chose-ats-first | Intro or TL;DR as natural series reference |
| Part 5: Full pain point breakdown | Forward reference only — no URL yet | Section 5 closing (what's next) |

---

## 8. What NOT to Do

| Do NOT | Why | Do Instead |
|---|---|---|
| Open Section 4 with cost figures | This section's power is the narrative insight — adapted-around problems. Costs follow the story. Leading with numbers makes it feel like a press release, not discovery. | Start with the 23-day/31-day discrepancy story. Introduce costs after the narrative is established. |
| Make this a "Recruitee is bad" article | Recruitee is a good product for its target market (general SMBs, 50–500 employees). Positioning this as a product tear-down makes Appunite look petty and undermines the methodology's credibility. | "Recruitee was built for a different market. Our process diverged from what any general-purpose ATS was designed to handle." |
| Skip or abbreviate the solvability filter | The solvability filter is the intellectual honesty requirement. Without it, the methodology is just a list of complaints with numbers attached. Reviewers and skeptical CTOs will notice its absence. | Give it its full weight in Section 2, Part 4. All three questions. Appunite's Q3 answer. |
| Present only the full opportunity-cost ROI number | 85% of the 150,648 PLN figure is opportunity cost driven by a single attribution assumption. Presenting the headline without the Column A/B split is misleading and will be caught by any financially literate reader. | Always pair the total with the direct-cost-only figure and the Column A/B split. |
| Invent statistics or use vague sourcing | "Experts say," "industry reports show" are AI tells and weak writing per tone-of-voice.md. | Cite specific sources. Write from Appunite's direct experience where no source exists. |
| Use the Pendo 2019 data without noting the year | The 2019 date is a potential credibility hit if not addressed. Acknowledge it is dated but still the largest study available. | "According to Pendo's 2019 Feature Adoption Report — still the largest study of its kind..." (model this after Part 1's exact handling) |
| Reproduce the full cost table from Part 2 | The cost breakdown by cluster (with monthly/annual figures) lives in Part 2. Reproducing it here is redundant and breaks the article's focus on methodology. | Reference the table and link to Part 2. Use the 7-cluster summary table in Section 3 only. |
| Over-explain JTBD or CIT | This audience is technically literate. One sentence of attribution per framework is sufficient. The article is not a literature review. | Name the framework, describe its application to this specific problem, cite one source, move on. |
| Present Section 2 as purely prose | The methodology article is designed to be used. Worksheets and templates belong here — they are the point. | Include the feature audit worksheet, pain point collection template, severity scale, and cost split table as formatted tables. |
| Use banned words from tone-of-voice.md | See Section 9 below | Check the full list before finalizing |
| Start any sentence with "Additionally," | Per tone-of-voice.md — structural red flag | Restructure the sentence flow |
| Use floating analytical clauses at sentence endings | "...underscoring our commitment," "...highlighting the importance of" — AI tells per tone-of-voice.md | If the point is worth making, give it its own sentence with actual content |
| Use "not just X, but Y" constructions unless both sides are concrete | Hollow parallel constructions per tone-of-voice.md | If contrasting, make both sides specific |
| Open with a definition or Wikipedia-style lead | "Pain point discovery is the process of..." is an AI tell | Start from the reader's situation or Appunite's specific context |

---

## 9. Banned Words and Phrases (from tone-of-voice.md)

**Absolute bans:**
delve, tapestry, vibrant, nestled, groundbreaking (figurative), rich (figurative), intricate, intricacies, interplay, cultivate / fostering (figurative), testament, indelible, enduring, pivotal (when avoidable), crucial (when avoidable), landscape (as abstract noun), underscore (as verb meaning "emphasize"), showcase (as verb), garner, resonate, align with

**Structural red flags — cut or rewrite:**
- "stands as / serves as / marks a" → use "is"
- "boasts" → use "has"
- "highlighting the importance of…" → just state the thing
- "reflecting broader trends in…" → only use if you can be specific
- "contributing to…" → name the contribution concretely or cut it
- "Additionally," at the start of a sentence → restructure instead
- "In today's [landscape/world]…" → skip the opener entirely
- "It is worth noting that…" → just note it
- "Needless to say…" → then don't say it

**Substitution reference:**

| AI phrase | Human alternative |
|---|---|
| "stands as a testament to" | "is evidence of" / just state the fact |
| "in today's rapidly evolving landscape" | delete entirely |
| "fosters a culture of" | "creates" / "leads to" / cut |
| "pivotal moment" | "turning point" / name the actual change |
| "delve into" | "look at" / "examine" / "cover" |
| "showcases" | "shows" / "demonstrates" |
| "it is worth noting" | just note it |
| "comprehensive solution" | name the actual components |
| "Additionally," [new sentence] | restructure the sentence flow |
| "holistic approach" | explain the actual approach |
| "leveraging our expertise" | say what the expertise is |

**Real em dashes (—) throughout. Not double hyphens (--).**

---

## 10. SEO Integration

### Primary Keywords

| Keyword | Target Placements | Suggested Locations |
|---|---|---|
| SaaS audit methodology | 2–3 | TL;DR, Section 2 intro, Section 5 |
| software pain point discovery | 2–3 | Section 1, Section 2 (Part 2), Section 5 |
| build vs buy requirements | 1–2 | Section 2 (Part 4 solvability filter), Section 5 |

### Secondary / Long-Tail Keywords

| Keyword | Where |
|---|---|
| SaaS pain point workshop | Section 2, Part 2 |
| feature usage audit | Section 2, Part 1 |
| JTBD product discovery | Section 1 |
| ATS pain points | Section 3 |
| build vs buy decision | Section 5, closing |

### LLM Optimization

- **BLUF / TL;DR:** Answer the core question (how to discover what's broken in your SaaS) in the first 75 words. Must be extractable as a standalone summary.
- **Declarative sentences:** Especially in TL;DR and methodology steps.
- **Entity richness:** Name Recruitee, JTBD, Critical Incident Technique, John C. Flanagan, Clayton Christensen, Pendo, Nielsen Norman Group, Błażej Cepil explicitly.
- **Table format:** The worksheets and templates are LLM-friendly and also serve as direct answer targets for "SaaS audit template" queries.
- **Freshness signals:** Use 2019 for Pendo (acknowledge it explicitly), 2026-03 for Appunite's methodology.

---

## 11. Structural Notes for the Writer

### Opening line

Do NOT open with:
- A definition of pain point discovery or SaaS audits
- "In today's competitive environment..." or any abstract scene-setting
- A rhetorical question framing

DO open with:
- The reader's situation (they already know something is wrong with their tools)
- Appunite's specific experience (the gap between "Recruitee is frustrating" and "here are 24 quantified problems")
- The core problem: complaints are real but incomplete

Example energy (not exact words):
- "Every team that runs Recruitee for a year has a list of things that annoy them. We had one too. The problem was our list wasn't the same as our problems."
- "Before we could decide whether to build our own ATS, we needed to know exactly what we were trying to fix. 'Recruitee is frustrating' is not a specification."

### Headers

Part 4 has 5 main sections. Use headers for navigation. The headers in this brief are directional, not prescriptive — adapt them if a more natural phrasing works better. The essential thing is the structure: why methodology → the methodology → clustering output → what you learn → how to run it yourself.

### Paragraph length

Vary it. This article is educational but should not read like a manual. Short declarative sentences for key points. Longer sentences for reasoning and context. Some paragraphs are one sentence — use them for emphasis.

### Tables and worksheets

Include them. This is a deliberate choice: Part 4 is designed to be useful as a standalone reference. A reader who bookmarks this article should be able to pull up the templates directly. Do not substitute prose descriptions for tables when tables are more usable.

### Word count distribution

| Section | Target |
|---|---|
| TL;DR | 50–75 words |
| Section 1 | 250–300 words |
| Section 2 | 700–900 words |
| Section 3 | 250–300 words |
| Section 4 | 250–300 words |
| Section 5 | 250–300 words |
| **Total** | **~2,000–2,500 words** |

---

## 12. Pre-Handoff Checklist

The writer must verify every item before passing the draft to the reviewer.

**Structure and completeness:**
- [ ] Word count is within 2,000–2,500 words
- [ ] TL;DR is present, 50–75 words, and extractable as standalone summary
- [ ] Section 1 explains WHY methodology is necessary (not just introduces the methods)
- [ ] JTBD is explained as a question reframe ("what are you trying to accomplish at this step?")
- [ ] CIT is explained with the Flanagan attribution and the NN/G source linked
- [ ] Section 2 contains all four parts of the methodology (feature audit, workshop, clustering, solvability filter)
- [ ] Feature audit worksheet table is included (4 columns: Feature, Usage Frequency, Requirement Level, Notes)
- [ ] Pain point collection template table is included (all 5 fields)
- [ ] Severity scale table is included (all 5 levels with definitions)
- [ ] All three solvability filter questions are present with their tests
- [ ] Section 3 includes all 7 cluster names with business consequence sentences
- [ ] Section 3 includes the 7-cluster summary table
- [ ] Section 4 opens with narrative insight, NOT cost figures
- [ ] The 23-day/31-day time-to-hire discrepancy is included in Section 4 as the key concrete example
- [ ] Column A / Column B cost split table is included in Section 5
- [ ] Section 5 includes a numbered practical checklist (7 steps)

**Data accuracy:**
- [ ] Pendo 2019 cited with year and acknowledged as still the largest study available
- [ ] Appunite figures used correctly: 24 problems, 7 clusters, 22,524 PLN direct, 150,648 PLN total, 86,000 PLN build budget, ~10% features used
- [ ] 23-day Recruitee figure vs. 31-day actual figure cited correctly
- [ ] 85% opportunity cost figure mentioned in connection with the total
- [ ] Cluster 1 (reporting errors) identified as the single largest cost contributor at 101,520 PLN/yr
- [ ] No invented statistics
- [ ] No vague sourcing ("experts say", "industry reports show")

**Cross-links:**
- [ ] Part 1 linked: https://appunite.com/blog/the-saas-tax
- [ ] Part 2 linked: https://appunite.com/blog/hold-my-beer-building-custom-ats (at minimum when referencing cost table in Section 3 and Column A/B in Section 5)
- [ ] Part 3 linked: https://appunite.com/blog/why-we-chose-ats-first
- [ ] Forward reference to Part 5 (full pain point breakdown) in Section 5 closing — no URL needed

**Tone and voice:**
- [ ] No banned words from tone-of-voice.md (Section 9 of this brief)
- [ ] No floating analytical clauses ("...underscoring," "...highlighting," "...reflecting")
- [ ] No "Additionally," sentence starters
- [ ] No hollow "not just X, but Y" constructions unless both sides are specific
- [ ] No Wikipedia-style definitional opening
- [ ] Real em dashes (—) throughout, not double hyphens (--)
- [ ] First person consistent: "we" for Appunite decisions, "I" for authorial judgment
- [ ] Recruitee not disparaged — framed as a product designed for a different market
- [ ] Solvability filter not minimized — given full weight

---

*Brief complete. Ready for writer handoff.*
