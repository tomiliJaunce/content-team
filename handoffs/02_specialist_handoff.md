# Content Specialist Handoff: How to Discover What's Actually Broken in Your SaaS Tool

**From:** Content Specialist
**To:** Content Writer
**Date:** 2026-03-19
**Series:** The SaaS Tax — Part 4
**Status:** Brief complete — ready for drafting

---

## Summary

The content brief is complete and located at:

**`/Users/Blazej/Code/content-team/content-specialist/content-brief.md`**

It contains everything needed to write the article without asking follow-up questions: section-by-section structure with word targets, the complete worksheet tables and template structures (copy-ready), tone guidance, curated data points with placement instructions, cross-link requirements, "What NOT to Do" table (13 items), the full banned-word list from tone-of-voice.md, and a pre-handoff checklist (30+ items).

---

## Quick Reference for the Writer

### Article at a Glance

| Dimension | Value |
|---|---|
| Title | How to Discover What's Actually Broken in Your SaaS Tool |
| Author | Błażej Cepil ("we" for Appunite decisions, "I" for authorial judgment) |
| Type | Blog post — methodology delivery |
| Series | The SaaS Tax — Part 4 |
| Length | 2,000–2,500 words |
| Journey Stage | Edukacja (Education) |
| Primary Audience | Tier 1 CTOs / Heads of Engineering who want to replicate Appunite's methodology |
| Goal | Teach the methodology. Position Appunite as people who ask the right questions. |
| Tone | Enthusiastic, educational. Sage archetype. Practical and replicable. |
| SEO | "SaaS audit methodology", "software pain point discovery", "build vs buy requirements" |

---

### Article Structure

| Section | Word Target | Core Job |
|---|---|---|
| TL;DR | 50–75 | BLUF: from "Recruitee is frustrating" to 24 problems / 150,648 PLN/yr. LLM-extractable. |
| 1: Why "what's broken?" is the wrong first question | 250–300 | Establish WHY methodology is necessary. JTBD reframe + CIT insight. Earns buy-in for Section 2. |
| 2: The methodology | 700–900 | Four-part methodology with complete worksheets and templates. The article's primary content. |
| 3: How we clustered 24 problems into 7 themes | 250–300 | Show the actual output. All 7 clusters with business consequence sentences. |
| 4: What this approach revealed that "just asking" wouldn't | 250–300 | The adapted-around problems. 23-day/31-day discrepancy as the key example. Opens with narrative, not costs. |
| 5: How to do this yourself | 250–300 | Practical checklist + Column A/B cost split table + forward reference to Part 5. |

---

## The 5 Most Important Things the Writer Must Get Right

**1. Section 1 is about WHY, not what.** The common mistake is to use Section 1 as a preamble that previews the four methodology steps. It is not that. Its job is to make the reader understand why structured methodology is necessary at all — why "just asking your team what's broken" produces incomplete and misleading results. JTBD and CIT are introduced because they solve a specific problem (adapted-around pain that direct questions miss), not because they are the steps in the methodology. If the reader finishes Section 1 without understanding the adapted-around problem concept, the section has failed.

**2. Section 2 must include all four worksheets and templates as tables — not prose descriptions of them.** The feature audit worksheet, pain point collection template, severity scale, and Column A/B cost split table must appear as formatted tables. This is a deliberate editorial choice: Part 4 is designed to be a reusable reference, not just a narrative article. A reader who bookmarks it should be able to pull up the templates directly. Do not substitute "you can create a spreadsheet with columns for Feature, Usage Frequency, Requirement Level, and Notes" for the actual table.

**3. The solvability filter (Section 2, Part 4) must not be minimized.** It is the intellectual honesty requirement that makes the whole methodology credible. All three questions must be present with their tests. Appunite's answer to Q3 must be included. If the filter is compressed to a paragraph or skipped, the methodology is just a complaint-quantification exercise — and skeptical CTOs will notice. The brief explains why this matters at length; the writer should read that framing carefully.

**4. Section 4 opens with the 23-day/31-day narrative, not with cost figures.** This is non-negotiable. The section's value is the adapted-around problems insight, and the time-to-hire discrepancy is the best concrete illustration of it: a measurable, documentable failure that nobody reported because everyone had silently accepted the tool's output as correct. Leading with costs (150,648 PLN, 85% opportunity cost) turns this into a financial summary, which belongs in Part 2. Lead with the story; the numbers follow.

**5. The Column A / Column B cost split table must appear in Section 5.** This is the intellectual honesty requirement for cost estimation. Presenting only the full opportunity-cost total (150,648 PLN) without the Column A direct-costs-only figure (22,524 PLN) is misleading. The table forces the decision-maker to name the attribution assumption they are accepting — which is exactly what makes this methodology credible rather than a post-hoc justification. The brief includes the full table structure; use it.

---

## Non-Obvious Creative Decisions in This Brief

**Why the methodology gets 700–900 words (Section 2 is the longest section).** Part 4's identity in the series is "the methodology post." Parts 1–3 established what the problem is, why Appunite acted, and how to decide what to build. Part 4 delivers the process. Shortchanging Section 2 to balance word count across all five sections would undermine the article's reason for existing. The templates and worksheets are not supplementary material — they are the primary deliverable for the CTOs who came to this article specifically to replicate what Appunite did.

**Why Section 1 argues for methodology rather than introducing it.** The methodological steps are not self-evidently necessary to a reader who has not yet internalized the "adapted-around problems" concept. Without that setup, JTBD and CIT sound like academic frameworks being imported to justify a foregone conclusion. With it, they sound like practical tools that solve a specific, recognizable problem (the pain you stopped noticing). The buy-in work in Section 1 makes Section 2 land differently.

**Why the 7-cluster table in Section 3 uses business consequence sentences rather than just cluster names.** The sentence structure ([Feature area] does not [capability], which prevents us from [business outcome]) is part of the clustering methodology itself — it is what forces you to articulate the root cause rather than just grouping symptoms. Presenting the clusters in this format shows the methodology in action, not just the output. It also makes each cluster's business significance immediately legible, which matters for readers who are scanning.

**Why Part 4's tone is explicitly different from Parts 2 and 3.** The brief specifies "enthusiastic and educational" rather than "analytical and methodical" (Part 3) or "declarative and energetic" (Part 2). This was a deliberate choice: methodology delivery done purely analytically reads like documentation. Done with Błażej's genuine enthusiasm for the process — the enthusiasm of someone who found something that works — it reads like a practitioner sharing hard-won knowledge. The Sage archetype here is a teacher who is also excited about the subject, not a detached analyst.

**The solvability filter gets its own Part in Section 2 (not a footnote).** There was a temptation to present the filter as a brief qualifier at the end of the clustering step. It is not a qualifier — it is a methodological gate that fundamentally changes what the output means. Elevating it to its own named Part, with all three questions and their tests, signals that this step is as important as the others. The brief explains the most common failure mode this prevents (blaming the tool for process problems); the writer should use that framing.

---

## Flags for the Writer

**The Pendo 2019 citation needs explicit date handling.** The data is from 2019, which some readers will flag. The correct handling — modeled on Part 1 of the series — is to name the year and immediately note it is still the largest study of its kind. Do not omit the year and do not treat it as a weakness without the offsetting context.

**Do not reproduce the full cost table from Part 2.** The cluster-level financial breakdown (direct cost, opportunity cost, monthly, annual for all 7 clusters) lives in Part 2 and should not be reproduced here. Section 3 uses a summary table showing cluster names and business consequence sentences only. Section 5 uses the Column A/B cost structure table. Neither replaces the Part 2 financial table.

**The 7-cluster business consequence sentences are sourced from research.md (Section C examples and the internal methodology).** Three of the seven sentences appear directly in the research file as examples; the other four were derived from the cluster descriptions in the Part 2 cost table. All seven are in the brief's Section 3 table — the writer does not need to reconstruct them.

**Recruitee is not a bad product.** This point appears in the "What NOT to Do" table but deserves emphasis here. Any language that reads as a product critique (even implicit — "surprisingly poor," "basic errors," "unacceptable") will undermine Appunite's credibility with readers who currently use or have evaluated Recruitee. The correct framing is structural mismatch: Recruitee was designed for a different market. Appunite's process outgrew it. This is a story about fit, not quality.

**The forward reference to Part 5 in Section 5 does not have a URL yet.** Reference it by description only: "the next post covers the full pain point breakdown — all 7 clusters, every pain point, and the cost methodology behind each number." No URL, no publication date.

---

## Files to Read Before Writing

| Priority | File | What it Contains |
|---|---|---|
| 1 (Required) | `/Users/Blazej/Code/content-team/content-specialist/content-brief.md` | Full brief: all section instructions, complete worksheet tables, data placement, tone rules, banned-word list, What NOT to Do table, pre-handoff checklist |
| 2 (Reference) | `/Users/Blazej/Code/content-team/researcher/research.md` | All source URLs, framework citations, full methodology details (Sections A–E), and the cost estimation framework |
| 3 (Reference) | `/Users/Blazej/Code/content-team/assets/tone-of-voice.md` | Complete banned-word list and Appunite brand voice guidelines — read before finalizing |
| 4 (Context) | `/Users/Blazej/Code/content-team/final-output/saas-tax-article.md` | Part 1 — for series tone reference and to see how the Pendo 2019 citation was handled |
| 5 (Context) | `/Users/Blazej/Code/content-team/final-output/ats-manifesto.md` | Part 2 — the financial table lives here; do not reproduce it. Also reference for the 23-day/31-day example. |
| 6 (Context) | `/Users/Blazej/Code/content-team/final-output/ats-selection-framework.md` | Part 3 — for series continuity and to understand the tone shift Part 4 makes |

---

## Cross-Links to Include

| Link Target | URL | Where in Article |
|---|---|---|
| Part 1: The SaaS Tax | https://appunite.com/blog/the-saas-tax | Section 1 or 5 (series origin reference) |
| Part 2: The Manifesto | https://appunite.com/blog/hold-my-beer-building-custom-ats | Section 3 (referencing cost table) and Section 5 (Column A/B reference) |
| Part 3: Why We Chose ATS | https://appunite.com/blog/why-we-chose-ats-first | Intro or TL;DR (natural series reference) |
| Part 5: Full pain point breakdown | Forward reference only — no URL yet | Section 5 closing |

---

*Handoff complete. Writer, please begin drafting.*
