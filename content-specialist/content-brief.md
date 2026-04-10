# Content Brief: "24 Problems, 7 Clusters — What We Found Wrong with Our ATS"

**Prepared by:** Content Specialist
**Date:** 2026-03-30
**For:** Content Writer
**Series:** The SaaS Tax — Part 5
**Author byline:** Błażej Cepil (first person — "we" for Appunite decisions, "I" for authorial judgment)
**Content type:** Blog post — analytical breakdown
**Estimated length:** 2,000–2,500 words

---

## 1. Article Metadata

| Dimension | Value |
|---|---|
| Title | 24 Problems, 7 Clusters — What We Found Wrong with Our ATS |
| Series | The SaaS Tax — Part 5 |
| Author | Błażej Cepil |
| Primary Audience | Tier 1 CTOs + Tier 3 engineers who love detailed breakdowns |
| Goal | Show depth of analysis. Make readers think "my tool has these same problems." |
| Tone | Authentic, detailed, transparent. Real data without being boring. |
| SEO Targets | "ATS problems", "Recruitee limitations", "recruitment software issues" |
| Target Length | 2,000–2,500 words |

---

## 2. Strategic Context

### Series Position

| Post | Title / Topic | Status |
|---|---|---|
| #1 | "The SaaS Tax — You're Paying for 100%, Using 12%" | Published |
| #2 | "Hold My Beer — We're Building Our Own ATS (The Manifesto)" | Published |
| #3 | "Why We Chose ATS as Our First Custom Replacement" | Published |
| #4 | "How to Discover What's Actually Broken in Your SaaS Tool" | Published |
| **#5** | **"24 Problems, 7 Clusters — What We Found Wrong with Our ATS"** | **This article** |
| #6 | Does the cost justify building? The ROI decision. | Upcoming |

### What the reader knows coming in

By Part 5, the reader knows: the SaaS tax is real (Part 1), Appunite decided to build their own ATS and found 24 problems costing 150,648 PLN/year (Part 2), they chose ATS as the first replacement (Part 3), and Part 4 walked through the exact methodology used to discover those problems. What they have not yet seen is the full breakdown of all 24 problems across all 7 clusters — what each one looks like in practice, what it costs, and why no generic tool can solve it.

Part 5 is the evidence post. It delivers what Part 2 promised and what Part 4's methodology produced.

### Core argument

When a tool designed for the median case meets a company with a non-median process, the result is not bugs — it is structural limitations that feel invisible until you measure them. These 24 problems are not evidence that Recruitee is bad. They are evidence of what happens when a specific, mature process outgrows a tool designed for the average case.

### What makes this article different

- Part 2 was the manifesto — the big bet, the headline number
- Part 4 was the methodology — how to find problems rigorously
- **Part 5 is the evidence** — here is everything we found, with full detail and honesty

The texture of Part 5 is analytical and transparent. It rewards readers who want the details. It does not summarize — it shows.

---

## 3. Audience

### Primary: Tier 1 — CTOs / Engineering Leaders

They want to see whether Appunite's process is rigorous enough to trust. A headline number (150,648 PLN/yr) is easy to manufacture. Walking through 7 clusters with specific, verifiable problems is not. They are evaluating: is this real analysis or is this post-hoc justification? Every data point, every honest admission, every flagged assumption answers that question.

**What hooks them:** The composition of the cost (85% opportunity, not direct time loss), the specific discrepancies that were embedded for months, the structural explanation for why no configuration change can fix these problems.

### Secondary: Tier 3 — Engineers Who Love Breakdowns

They are not decision-makers but they are amplifiers. They will share this because it validates something they already suspected about their own tools: the workarounds have become invisible. They want to see the specific problems, not just the clusters.

---

## 4. Tone

**Archetype:** Transparent practitioner. Someone who ran a rigorous analysis and is sharing exactly what was found — including the parts that reflect poorly on their own habits.

**Register:** Analytical but human. The enthusiasm here comes from the data being genuinely interesting, not from adjectives. The vulnerability comes from named admissions, not from general self-deprecation.

**First person conventions:**
- "we" = Appunite's decisions, findings, habits ("we were using the wrong number")
- "I" = Błażej's authorial judgment ("I think the attribution is reasonable, but it cannot be proven")
- Never "Appunite believes" or "the company found"

**Rhythm:** This article has a table-heavy structure in Section 1 and deep narrative in Section 2. The rhythm should reflect that: functional and direct around tables, more expansive in the day-to-day descriptions of what each problem actually looks like.

**Positive campaign requirement (critical):** The article must never read as a Recruitee teardown. "Designed for millions of users" is the explanation for every limitation — not an accusation and not an excuse. A reader who currently uses Recruitee should finish this article thinking "they're right, we're probably a different kind of user" — not "Appunite is attacking the product I chose."

---

## 5. Section-by-Section Instructions

---

### Opening / TL;DR (50–75 words)

**Format:** TL;DR block at the top, per series convention.

**Content:** The discovery methodology from Part 4 produced 24 specific problems across 7 clusters, with a total estimated cost of 150,648 PLN per year — 85% of which is opportunity cost. This post walks through all 7 clusters: what each problem looks like in practice, why Recruitee cannot solve it structurally, and what the financial breakdown behind each cluster means.

The TL;DR must be extractable as a standalone summary.

---

### Section 1: The 7 Clusters at a Glance

**Word count target:** 250–350 words (not counting the table itself)

**Purpose:** Orient the reader with the full picture before the deep dives. The table is the anchor for the entire article — it lets the reader see all 7 clusters and return to it as a reference. The prose around it explains what they are about to read without over-explaining.

**The complete cluster overview table — include exactly as formatted below:**

| # | Cluster | Problems | Direct cost (PLN/yr) | Opportunity cost (PLN/yr) | Total (PLN/yr) | Cost type |
|---|---|---|---|---|---|---|
| 1 | Reports calculate with errors | 4 | 1,728 | 99,792 | 101,520 | Mixed (dominant: opportunity) |
| 2 | Metrics not customisable | 3 | 2,304 | — | 2,304 | Direct only |
| 3 | Funnels not elastic | 3 | 780 | 4,320 | 5,100 | Mixed |
| 4 | No competency matrices + sourcing inefficiency | 4 | 6,036 | 4,056 | 10,092 | Mixed |
| 5 | No interview transcription + manual feedback | 3 | 4,680 | 19,956 | 24,636 | Mixed (dominant: opportunity) |
| 6 | Calendar/scheduling gaps | 3 | 3,888 | — | 3,888 | Direct only |
| 7 | GDPR compliance gaps | 3 | 3,108 | — | 3,108 | Direct only |
| **Total** | | **24** | **22,524** | **128,124** | **150,648** | |

**Writing instructions:**

Before the table: 1–2 sentences that frame what the reader is about to see. The table covers 24 problems across 7 clusters with a total estimated annual cost of 150,648 PLN. Do not write a paragraph of preamble — the table can carry its own weight.

After the table: 2–4 sentences that call out the two most important structural observations:
1. Cluster 1 alone accounts for 101,520 PLN/yr — 67% of the total — despite containing only 4 of the 24 problems.
2. 85% of the total (128,124 PLN/yr) is opportunity cost, not direct time loss. This changes how the numbers should be read.

One sentence may note that the next section goes deeper into the three clusters that matter most, and why.

**What NOT to write in this section:**
- Do not open with a definition or a general statement about SaaS tools
- Do not editorialize about what the table "reveals" — let the table do that
- Do not explain how the methodology worked (that is Part 4's job)

**Required data points:**
- 150,648 PLN/yr total
- 22,524 PLN/yr direct
- 128,124 PLN/yr opportunity
- 85% opportunity cost share
- Cluster 1 = 101,520 PLN/yr = 67% of total

**Cross-link to include:** Near the table, link to Part 2 (where this table first appeared in summary form) and Part 4 (which explains how the 24 problems were found). Natural anchor text examples: "the methodology behind these numbers" → Part 4 link; "first introduced in Part 2" → Part 2 link.

**SEO note:** "ATS problems" fits naturally in the prose around the table — in a sentence like "the ATS problems we found fell into two cost categories."

---

### Section 2: The Top 3 That Matter Most

**Word count target:** 900–1,100 words (300–370 words per cluster deep-dive)

**Purpose:** Move from table to experience. For three clusters, give the reader a day-to-day picture of what the problem actually looks like, explain why the tool cannot solve it structurally, and anchor it with the financial breakdown.

**The three clusters to deep-dive — in this order:**

1. **Cluster 1 — Reports calculate with errors** (101,520 PLN/yr)
2. **Cluster 5 — No interview transcription + manual feedback** (24,636 PLN/yr)
3. **Cluster 4 — No competency matrices + sourcing inefficiency** (10,092 PLN/yr)

**Rationale for this selection (writer context — do not publish):**
- Cluster 1 is non-negotiable: it is 67% of the cost and the location of the most important vulnerability admission in the article.
- Cluster 5 is the most universally relatable — any company running structured interviews loses signal to memory-based note-taking.
- Cluster 4 is specific to technical hiring and will connect with the CTOs and engineers who are this article's primary audience.

**Required structure for each cluster:**

Each cluster deep-dive must cover three things in roughly this order:
1. What does this look like day-to-day? (concrete, specific, a scene if possible)
2. Why can't the generic tool solve it? (the structural explanation — built for the median case, not this one)
3. What does it cost? (the number, with direct/opportunity split shown)

---

#### Cluster 1 — Reports calculate with errors

**Day-to-day narrative:**

The tool reports time-to-hire as 23 days. Manual tracking shows the real number is 31. The difference is not a rounding error — Recruitee counts calendar days from job posting, not from the stage transitions that reflect actual pipeline movement. The two numbers measure different things.

The honest part: this discrepancy had been there for months before the audit. Every planning meeting, every hiring retrospective, every headcount discussion was built on the wrong number. Not because nobody cared about accuracy — because questioning the tool's output at that level had stopped being a habit. The expectation of accuracy had been abandoned so gradually that nobody could locate the moment it happened. Name this directly. It is the key vulnerability admission of the article.

**Four specific problems the writer must reference:**
1. Time-to-hire calculation logic counts from job posting, not from first candidate interaction or actual stage transitions — does not match how Appunite's real pipeline moves
2. Hire count metric shows 0% regardless of completed hires — not a data lag, a metric that is visibly broken with no workaround other than ignoring it
3. Cost-per-hire requires combining Recruitee data with payroll data the tool cannot access — no native path; team either skips the metric or exports and calculates manually
4. Data refresh lag — reports do not update in real time; morning pipeline data does not reflect previous evening's activity during active hiring periods

**Why the generic tool can't fix it:**
The calculation logic is hardcoded. "Time-to-hire" means one thing in Recruitee's codebase and another in Appunite's actual process. A tool built for the median SMB defines hiring stages in a standard way because that definition works for most of its customers. Appunite is not most customers. There is no configuration option that changes the underlying calculation logic — this is not a settings problem.

**Cost:**
- Total: 101,520 PLN/yr
- Direct: 1,728 PLN/yr (time manually cross-checking and correcting reports)
- Opportunity: 99,792 PLN/yr

The writer must flag the attribution assumption here, explicitly and honestly: the opportunity cost rests on the assumption that 50% of failed hires trace back to decisions made on inaccurate reporting data. At 0% attribution, the ROI on the entire build project goes from +75% to -74%. This is the most consequential single number in the cost model. It cannot be proven. It can be argued — and Appunite believes the argument is reasonable. But the assumption must be named.

---

#### Cluster 5 — No interview transcription + manual feedback

**Day-to-day narrative:**

The interview ends. The interviewer goes back to their desk. Somewhere between two hours and the following morning, they write their notes from memory. The feedback form in Recruitee is an open text field. No template, no scoring rubric, no standard questions to respond to. One interviewer writes three sentences. Another writes three paragraphs in a format nobody else uses. When the team meets to decide between two finalists, they are comparing things that cannot be compared.

**Three specific problems the writer must reference:**
1. No recording or transcription — after the interview is done, what was said exists only in the interviewer's memory; signal loss is structural, not occasional
2. Freeform feedback only — no template, no rubric, no scoring dimensions; each interviewer invents their own format, making candidate-to-candidate comparison close to impossible
3. No side-by-side candidate comparison — when making a final decision between two candidates, there is no structured view; decision-makers work from fragmented notes across separate pages

**Why the generic tool can't fix it:**
Recruitee's feedback model was designed for the use case where notes are sufficient — generalist roles, standard interview formats, low technical depth. For a company evaluating senior Elixir engineers on architecture decisions, communication quality in client-facing contexts, and system design thinking, an open text field is not a data structure. No amount of configuring Recruitee's existing fields produces structured, comparable, searchable interview data.

**Cost:**
- Total: 24,636 PLN/yr
- Direct: 4,680 PLN/yr (estimated 20–30 min per interview for post-interview writeups × interview volume × hourly rate)
- Opportunity: 19,956 PLN/yr (conservative estimate of lost signal leading to worse offer acceptance rates and early attrition outcomes)

---

#### Cluster 4 — No competency matrices + sourcing inefficiency

**Day-to-day narrative:**

A new Elixir role opens. The team remembers that six months ago they interviewed someone who was strong — the timing was wrong, headcount was not approved. That candidate exists somewhere in Recruitee. Their interview notes exist. But there is no way to search for "candidates with strong Elixir scores, passed over for non-performance reasons." The data is in a text field. It is not queryable. The recruiter starts from zero: same job boards, same outreach, same channels.

**Four specific problems the writer must reference:**
1. No competency scoring — no structured field, no rubric, no aggregate view across interviewers; only free-text notes that cannot be systematically compared
2. Past candidates not surfaced for new roles — data exists in the system but is not searchable by skill profile; every new role effectively resets the candidate pipeline
3. Sourcing is role-level, not competency-level — job postings go to the same channels regardless of specific skill requirements; no way to target outreach to candidates with documented profiles from prior interactions
4. Technical assessment results from external tools cannot be attached to the candidate record in a structured way — results live in email threads or separate spreadsheets, disconnected from the candidate's history in Recruitee

**Why the generic tool can't fix it:**
Recruitee was designed for companies hiring generalists at moderate volume, where the talent pool is large and each candidate interaction is relatively self-contained. Appunite's situation is different: senior Elixir engineers are a small community, and the relationship with a candidate who was good-but-wrong-timing has potential value months or years later. The tool's data model was never built to support longitudinal candidate relationships because most of its customers do not need that.

**Cost:**
- Total: 10,092 PLN/yr
- Direct: 6,036 PLN/yr (recruiter time on manual sourcing steps that a competency-indexed system would reduce)
- Opportunity: 4,056 PLN/yr (cost of re-sourcing from scratch vs. surfacing known, pre-qualified candidates)

---

**Transition between clusters:**

Each cluster should open with a scene or a specific observation — not with a category label. Sub-headers using the cluster name are fine for navigation. The opening sentence of each deep-dive should pull the reader into the problem rather than describe it from outside.

**SEO note:** "Recruitee limitations" fits naturally in one of the cluster sections when explaining why the tool cannot solve the problem structurally. Frame it as design boundaries, not product failures: "These are not Recruitee limitations in the sense of defects — they are boundaries of what the product was built to do."

---

### Section 3: The Pattern Across All 7

**Word count target:** 300–400 words

**Purpose:** Step back from the individual clusters and name the structural explanation that applies to all of them. This is the analytical reward for a reader who has followed the detail. It is also the section that protects the article from reading as a product criticism.

**The meta-pattern the writer must convey:**

These are not bugs. Recruitee works correctly for its target market. The structural limitations exist because the product was built for the median case: SMBs with moderate hiring volumes, generalist roles, standard funnel structures, and standard reporting needs. That product is well-designed for that use case.

Appunite is not that use case:
- **Low volume, high quality bar** — the tool is optimized for throughput; Appunite needs depth of evaluation at each step
- **Narrow talent pool** — senior Elixir engineers are a small community; relationship tracking over time matters in a way it does not for a company hiring generalists at volume
- **Complex technical evaluation** — a standard notes field cannot hold what a structured competency matrix needs to capture
- **Strategic data ownership** — Appunite needs to cross-reference hiring outcomes with actual engineer performance post-hire; this requires owning the data model, not renting access to it

This is not a product-quality problem. It is a product-market fit problem. A tool built for one market applied to a different market. The structural limitations serve the majority of Recruitee's users. They just do not serve Appunite.

**Vulnerability element required in this section:**

This section is also where the second honest admission belongs. Several of the workarounds discovered in the audit had become so embedded that team members no longer experienced them as problems — they were just "how hiring works." Manual calendar coordination. Memory-based interview feedback. The audit revealed how much normalized friction had accumulated. The team was not oblivious — the friction had simply become invisible, one small adaptation at a time.

Name this without dramatizing it. The tone is: this is a real thing that happens to tools used long enough, and it happened to us.

**What NOT to write here:**
- Do not write a generic paragraph about SaaS industry trends or "in today's market"
- Do not imply Recruitee made poor design choices — the framing throughout is that they built the right product for their target customer
- Do not use "landscape," "pivot," or any other banned words

---

### Section 4: What This Means for Your Tools

**Word count target:** 250–350 words

**Purpose:** Make the article useful beyond Appunite's specific situation. Give readers a transferable lens for their own SaaS stack.

**The transferable lesson framing:**

This article is not a Recruitee review. It is a case study in what happens when a mature, specific process meets a generic tool. The reader's tool may not be an ATS. The patterns are the same.

**Three questions to surface for the reader** (not necessarily as a bulleted list — integrate naturally into prose if that reads better):

1. Are there metrics in your tool you cannot customize — where the vendor's definition of "conversion rate," "time-to-hire," or "utilization" does not match what your process actually needs to measure?
2. Are there workflows you cannot modify — where the tool's fixed structure forces your process to conform to its logic rather than the other way around?
3. Is there data in your tool you cannot cross-reference — where the information exists inside the system but cannot be queried in the way your decisions require?

**Tone note:** Write this as a genuine observation from someone who just ran this exercise — not as a "key takeaways" slide, not as a lecture. The reader is being given a lens, not instructions.

**SEO note:** "recruitment software issues" fits most naturally here, when framing the parallel to the reader's own tools. Example: "The recruitment software issues we found aren't unique to Recruitee or to hiring — they are a specific version of a general problem."

---

### Section 5: Closing Note — The Question This Raised

**Word count target:** 150–200 words

**Purpose:** Close the article at the right moment. Set up Part 6 without summarizing it or teasing it. The discovery is complete. Now the question is what to do with it.

**What to convey:**

- The process was rigorous. The data is as honest as it can be given the constraints (especially the attribution assumption in Cluster 1).
- The numbers raise a question this article cannot answer: does 150,648 PLN/yr in estimated cost actually justify an 86,000 PLN build?
- The answer is not obvious. Direct savings alone (22,524 PLN/yr) produce a negative ROI on an 86,000 PLN build. The case only works if a meaningful fraction of the opportunity costs are real.
- That question — whether the assumptions hold — is what Part 6 addresses.

**What NOT to write:**
- Do not say "stay tuned" or "next time" or "coming soon"
- Do not write a cliffhanger
- Do not answer the question. The door opens; that is all.
- Do not introduce any data about the build itself — that belongs in Part 6

**Suggested closing structure:** End with a sentence or two that names the genuine uncertainty and points at it honestly. The financial case is stronger with opportunity costs included. But opportunity costs rest on assumptions. Part 6 is about whether those assumptions hold. No title, no URL for Part 6 — forward reference only.

---

## 6. All Data Points the Writer Must Include

All figures are Appunite internal, verified. Use exactly as cited.

| Fact | Placement |
|---|---|
| 150,648 PLN/yr total cost | Section 1 (table), Section 1 (prose), closing |
| 22,524 PLN/yr direct cost | Section 1 (table), closing |
| 128,124 PLN/yr opportunity cost | Section 1 (table) |
| 85% of total is opportunity cost | Section 1 (prose after table), Section 3 or closing |
| Cluster 1 = 101,520 PLN/yr = 67% of total | Section 1 (prose after table), Cluster 1 deep-dive |
| 1,728 PLN/yr direct cost for Cluster 1 | Cluster 1 deep-dive |
| 99,792 PLN/yr opportunity cost for Cluster 1 | Cluster 1 deep-dive |
| 50% attribution assumption drives Cluster 1 opportunity cost | Cluster 1 deep-dive — must be flagged as assumption |
| Build budget: 86,000 PLN | Section 5 closing |
| Direct-only ROI: -74% | Section 5 closing |
| Full ROI (with opportunity): +75% | Section 5 closing |
| 23 days (Recruitee reported) vs. 31 days (actual) time-to-hire | Cluster 1 deep-dive |
| Discrepancy had been there for months before audit | Cluster 1 deep-dive (vulnerability admission) |
| Cluster 5 = 24,636 PLN/yr total | Cluster 5 deep-dive |
| 4,680 PLN/yr direct cost for Cluster 5 | Cluster 5 deep-dive |
| 19,956 PLN/yr opportunity cost for Cluster 5 | Cluster 5 deep-dive |
| Cluster 4 = 10,092 PLN/yr total | Cluster 4 deep-dive |
| 6,036 PLN/yr direct cost for Cluster 4 | Cluster 4 deep-dive |
| 4,056 PLN/yr opportunity cost for Cluster 4 | Cluster 4 deep-dive |
| 24 distinct problems, 7 clusters | Section 1, Section 3 |
| Several workarounds had become invisible before audit | Section 3 (vulnerability element) |

**Do not invent statistics.** If a claim needs a number not in this list, write from Appunite's direct experience or cut the claim.

---

## 7. Cross-Link Requirements

| Link Target | URL | Required Placement |
|---|---|---|
| Part 1: The SaaS Tax | https://appunite.com/blog/the-saas-tax | Optional — include if a natural anchor exists in Section 4 |
| Part 2: The Manifesto | https://appunite.com/blog/hold-my-beer-building-custom-ats | Section 1, near the table ("this table first appeared in Part 2 in summary form") |
| Part 4: Methodology | https://appunite.com/blog/how-to-discover-whats-broken-in-your-saas | Section 1, before the table ("the methodology that produced these 24 problems") |
| Part 6: ROI decision | Forward reference only — no URL | Section 5 closing only |

---

## 8. What NOT to Do

1. **Do not editorialize about Recruitee's quality.** Any phrasing that implies Recruitee is poorly built, surprisingly limited, or badly designed is wrong. The framing throughout: it is the right product for its market. Appunite is not that market. A reader who chose Recruitee for a standard SMB hiring process should not feel attacked.

2. **Do not hide the attribution assumption.** The 50% attribution for Cluster 1's opportunity cost must be named and flagged. Presenting 101,520 PLN/yr without noting that this figure depends on an unverifiable assumption would undermine the article's core promise of transparency. The entire ROI case rests on this number.

3. **Do not write a generic SaaS criticism piece.** Every claim must be grounded in Appunite's specific data about their specific tool. The pattern in Section 3 is general; the evidence in Sections 1 and 2 is always specific.

4. **Do not use present-participle analytical tails.** No sentences ending in "…highlighting the importance of data quality," "…underscoring the need for flexibility," "…reflecting the challenges of modern hiring." These sound like AI output and add nothing.

5. **Do not let 150,648 PLN float free of its context.** Every appearance of the total cost figure should either include the direct/opportunity split or reference it from a recently established context. The headline number without its composition is misleading.

6. **Do not open any section with a definition or a Wikipedia-style lead.** No "An ATS is…" No "Recruitment software is designed to…" The reader knows. Start with Appunite's situation or a specific observation.

7. **Do not force three things everywhere.** The data has 7 clusters. The deep-dives cover 3. If a point is best made in two sentences, use two. Avoid packaging everything into artificially balanced structures.

8. **Do not write the vulnerability admissions as confessions.** The tone for honest admissions is plain observation, not self-flagellation. "The discrepancy had been there for months" — not "we were embarrassed to discover" or "we must admit."

9. **Do not resolve the Part 6 forward reference.** Section 5 opens the question of whether the build is justified. That question stays open. Do not hint at the answer.

10. **Do not over-format.** Headers for navigation are fine. Bullet points for things that can be said in a sentence are not. Bold for genuinely critical numbers and terms only — not for decoration. The table in Section 1 is structural; do not add more tables in the deep-dive sections unless strictly necessary.

11. **Do not write Section 4 as a "key takeaways" slide.** It should read as a genuine observation from someone who has just gone through this exercise, not as a listicle.

12. **Do not compress the three deep-dives to save words.** The article's value proposition for this audience is specificity. Each deep-dive must cover all required individual problems for that cluster, the day-to-day narrative, the structural explanation, and the cost breakdown with split. Compressing any of these undermines the article's core goal: making readers think "my tool has these same problems."

---

## 9. Banned Words List

From Appunite tone-of-voice guidelines. Do not use any of the following.

**Absolute bans:**
delve, tapestry, vibrant, nestled, groundbreaking (figurative), rich (figurative), intricate, intricacies, interplay, cultivate / fostering (figurative), testament, indelible, enduring, pivotal (when avoidable), crucial (when avoidable), landscape (as abstract noun — "the competitive landscape"), underscore (as a verb meaning "emphasize"), showcase (as a verb), garner, resonate, align with

**Structural bans — cut or rewrite:**
- "stands as / serves as / marks a" → use "is"
- "boasts" → use "has"
- "highlighting the importance of…" → state the thing directly
- "reflecting broader trends in…" → only if you can be specific
- "contributing to…" → name the contribution concretely or cut it
- "Additionally," at sentence start → restructure
- "In today's [landscape/world]…" → delete entirely
- "It is worth noting that…" → just note it
- "Needless to say…" → then don't say it
- "holistic approach" → explain the actual approach
- "comprehensive solution" → name the components
- "leveraging our expertise" → say what the expertise is

**Substitution reference:**

| AI phrase | Human alternative |
|---|---|
| "stands as a testament to" | "is evidence of" / state the fact |
| "in today's rapidly evolving landscape" | delete entirely |
| "fosters a culture of" | "creates" / "leads to" / cut |
| "pivotal moment" | "turning point" / name the actual change |
| "delve into" | "look at" / "examine" / "cover" |
| "showcases" | "shows" / "demonstrates" |
| "it is worth noting" | just note it |
| "comprehensive solution" | name the actual components |
| "Additionally," [new sentence] | restructure the sentence flow |
| "holistic approach" | explain the actual approach |

Real em dashes (—) throughout. Not double hyphens (--).

---

## 10. SEO Placement Guidance

| Keyword | Where to place | Suggested framing |
|---|---|---|
| "ATS problems" | Section 1, in prose around the table | "The ATS problems we found fell into two cost categories: direct costs and opportunity costs." |
| "Recruitee limitations" | Section 2, in one of the cluster deep-dives when explaining structural constraints | "These are not Recruitee limitations in the defect sense — they are design boundaries." |
| "recruitment software issues" | Section 4, when transitioning to the reader's own context | "The recruitment software issues we found are a specific version of a more general pattern." |

All placements should sound like they belong. If a sentence sounds strained, sacrifice the keyword for readability. The primary goal is a credible, readable article — SEO is secondary.

---

## 11. Pre-Handoff Checklist for the Writer

The writer must verify every item before passing the draft to the content reviewer.

**Data accuracy — non-negotiable:**
- [ ] Table in Section 1 matches the brief exactly: all 7 rows, all cost figures, all problem counts, totals row
- [ ] 150,648 PLN/yr appears at least twice and always with direct/opportunity context nearby
- [ ] 22,524 PLN/yr direct cost is stated
- [ ] 128,124 PLN/yr opportunity cost is stated (or shown in the table)
- [ ] 85% opportunity cost share is stated at least once in prose
- [ ] Cluster 1 = 101,520 PLN/yr = 67% of total stated in Section 1 prose after table
- [ ] The 50% attribution assumption for Cluster 1 opportunity cost is named and flagged as an assumption in the Cluster 1 deep-dive
- [ ] The 23 vs 31 day time-to-hire discrepancy is named in the Cluster 1 deep-dive
- [ ] The discrepancy had been present for months before the audit — named explicitly
- [ ] Cluster 5 = 24,636 PLN/yr with 4,680 PLN direct and 19,956 PLN opportunity
- [ ] Cluster 4 = 10,092 PLN/yr with 6,036 PLN direct and 4,056 PLN opportunity
- [ ] Build budget of 86,000 PLN mentioned in the closing section
- [ ] Direct-only ROI (-74%) stated in the closing section
- [ ] Full ROI (+75%) stated in the closing section

**Structural completeness:**
- [ ] All 5 sections present in the correct order
- [ ] Section 1 table is complete: 7 rows + totals row, cost type column populated
- [ ] Cluster 1 deep-dive references all 4 specific problems (time-to-hire logic, hire count = 0%, cost-per-hire not computable, data refresh lag)
- [ ] Cluster 5 deep-dive references all 3 specific problems (no recording/transcription, freeform feedback, no side-by-side comparison)
- [ ] Cluster 4 deep-dive references all 4 specific problems (no competency scoring, past candidates not surfaced, role-level sourcing only, no structured assessment integration)
- [ ] Each deep-dive covers: day-to-day narrative + structural explanation + cost with direct/opportunity split
- [ ] Section 3 contains the meta-pattern explanation (structural limitation vs. bug, built for median case)
- [ ] Section 3 contains a vulnerability admission about normalized workarounds
- [ ] Section 4 is addressed to the reader's own tools, not just Appunite's situation
- [ ] Section 5 does not resolve the Part 6 forward reference — the question stays open

**Cross-links:**
- [ ] Part 2 linked near the table in Section 1
- [ ] Part 4 linked in Section 1, before or around the table
- [ ] Part 6 referenced in Section 5 — no URL (does not exist yet)
- [ ] Part 1 link included if a natural anchor exists

**Tone and style:**
- [ ] No banned words from Section 9 of this brief
- [ ] No present-participle analytical tails ("…highlighting," "…underscoring," "…reflecting")
- [ ] No "In today's world" or equivalent openers
- [ ] No editorialization about Recruitee being bad or poorly designed
- [ ] The Cluster 1 vulnerability admission (months of wrong data) is named plainly, not dramatized
- [ ] Recruitee framed consistently as: right product for its market, wrong fit for Appunite's use case
- [ ] Section 4 reads as observation, not as a structured "key takeaways" list
- [ ] Section 5 closes with a genuine open question, not a teaser
- [ ] Word count is between 2,000 and 2,500 words

**SEO:**
- [ ] "ATS problems" appears once, naturally, in Section 1
- [ ] "Recruitee limitations" appears once, naturally, in a cluster deep-dive
- [ ] "recruitment software issues" appears once, naturally, in Section 4

---

*Brief complete. Ready for writer handoff.*
*Content Specialist — content-pipeline team — 2026-03-30*
