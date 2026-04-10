# How to Discover What's Actually Broken in Your SaaS Tool

**TL;DR:** Most companies can tell you what annoys them about their tools. Few can quantify it rigorously enough to support a build-vs-buy decision. This post walks through the exact methodology Appunite used to go from "Recruitee is frustrating" to 24 specific problems costing an estimated 150,648 PLN per year. Four steps: feature audit, pain point workshop, clustering, solvability filter. The process is replicable by any team lead in a week. ([Part 3: Why We Chose ATS First](https://appunite.com/blog/why-we-chose-ats-first) covers what to do once you have the numbers.)

---

## Why "what's broken?" is the wrong first question

You already know something is off with your SaaS tool. Your team has complaints. The tool doesn't do quite what you need it to do. Some reports are unreliable. Some workflows require steps that feel unnecessary. You have a list.

The problem with that list is not that it's wrong. It is that it is incomplete in a specific way: it captures what people notice. It does not capture what people have stopped noticing.

When you ask your team "what's broken?", you get a survey of recent frustrations — the friction they encountered this week, the thing that annoyed them in their last session with the tool. What you do not get are the problems they adapted around six months ago. The workarounds that have become so automatic that nobody experiences them as problems anymore. The workaround that takes three extra minutes every Tuesday has become just how Tuesday works. The metric that is slightly wrong has become the metric everyone uses, because everyone stopped trusting the accurate one and nobody remembers when that happened.

The pain is real. The signal is invisible.

This is the core insight behind Jobs to Be Done (JTBD), a product discovery framework popularized by Clayton Christensen and Tony Ulwick (Strategyn). JTBD reframes the question: not "what is broken in this tool?" but "what are you trying to accomplish at this step?" ([Product School JTBD Guide](https://productschool.com/blog/product-fundamentals/jtbd-framework)). When you ask someone about their job — the outcome they are actually trying to reach — you surface the unfulfilled need, not their opinion of how the current tool handles it. Users who have built workarounds have stopped asking for a fix. The job remains unfinished. They just stopped noticing.

Critical Incident Technique works alongside this. Developed by John C. Flanagan in 1954, CIT collects specific memorable incidents — times when a tool significantly failed someone — rather than general impressions ([Nielsen Norman Group on CIT](https://www.nngroup.com/articles/critical-incident-technique/)). The key insight from NN/G: one user reporting a critical incident may reveal something more important than the same low-stakes frustration reported by ten. High-impact failures matter more than frequently-reported annoyances. Asking "tell me about a specific time this tool failed you at a critical moment" breaks the workaround habit — because those critical moments are still memorable, even if the underlying problem has become invisible in daily use.

These two reframes — JTBD for what to ask, CIT for how to ask it — are what separate a structured discovery methodology from a complaint session. The next section is that methodology.

---

## The methodology

This is a four-part process. We ran it over roughly two weeks with our recruitment team before making any build-vs-buy decision about Recruitee. Teams have run compressed versions in as few as three days when they needed to move quickly. The parts are sequential — each one prepares the input for the next.

### Part 1: Feature usage audit

Before you run any workshops, establish the baseline: what fraction of the platform does your team actually use?

The reason this comes first: without it, pain point workshops produce complaints without context. You do not know whether a missing capability is a gap in a tool you use heavily or a gap in a tool you barely use. The ratio changes the interpretation of everything that follows.

**How to run the audit:**

1. Build a complete feature list — from vendor documentation, an admin panel walkthrough, and 20 minutes with daily users. Be specific. Not "reporting" but each distinct report type. Not "integrations" but each integration your team has enabled or considered. Expect 40–150 items depending on the platform.
2. For each feature, classify it on two axes:
   - Usage frequency: Daily / Weekly / Monthly / Never
   - Requirement level: Required / Nice to have / Not needed
3. Calculate your **usage ratio**: features used at least monthly ÷ total features × 100
4. Calculate your **required ratio**: features marked Required ÷ total features × 100

**Feature audit worksheet:**

| Feature | Usage Frequency | Requirement Level | Notes |
|---|---|---|---|
| [Feature name] | Daily / Weekly / Monthly / Never | Required / Nice to have / Not needed | [Optional context] |

**How to read the results:**

- Required ratio above 20%: the tool may be well-matched to your process — or your team has built its workflow around the tool's structure. Both are worth examining before you proceed.
- Required ratio under 15%: territory where a custom build covering that 15% could plausibly replace the full platform.

Two traps to avoid:

Daily usage does not equal Required. Some habits exist only because the current tool forces a particular workaround — the habit disappears if the constraint disappears. The test for Required is: if version 1 of a replacement did not have this feature, would we be blocked?

Do not mark Required just because the feature currently exists. Mark Required only if removing it would genuinely stop work.

---

### Part 2: Pain point discovery workshop

The feature audit tells you how much of the tool you use. The workshop tells you what actually hurts when you use it.

**Workshop setup:**

- **Participants:** 2–3 daily users from different workflow areas, someone who can speak to business impact, and a decision-maker. Cap at six people. Do not invite the vendor relationship owner unless they are also a daily user — their presence changes what people say.
- **Duration:** 90 minutes. First 20 minutes: individual collection. Next 50 minutes: discussion, clarification, and scoring. Final 20 minutes: solvability filter (covered in Part 4 below). Extend to two hours if the group is engaged and generating new insights.
- **Pre-work:** Share the pain point collection template at least 24 hours in advance. We gave our team a week. Ask for at least five entries before the session. Pre-filled templates produce deeper outputs than blank ones filled in during the workshop — people arrive having already thought about it, and the session becomes calibration rather than recollection.

**Pain point collection template:**

| Field | Definition |
|---|---|
| Description | Specific and concrete. Not "reporting doesn't work well" but "hire count always shows 0% regardless of actual hires" |
| Frequency | Daily / Weekly / Monthly / Quarterly |
| Severity | 1–5 anchored to business consequence (see scale below) |
| Current workaround | What the team does today. "Nothing, we just live with it" is a valid answer. |
| Time per occurrence | Minutes per workaround. Estimate conservatively — this number feeds the cost calculation. |

**Severity scale:**

| Score | Definition |
|---|---|
| 1 | Annoying, no workaround needed |
| 2 | Workaround exists, under 5 min, reliable |
| 3 | Workaround exists but time-consuming or introduces data risk |
| 4 | No clean workaround; data quality suffers or significant recurring manual work |
| 5 | Blocking: task cannot be completed, compliance risk, or downstream failures |

Calibration note: a workaround that takes 10 minutes and is done = 3. A workaround that introduces data you will need to reconcile later = 4. A 5 is reserved for genuine blocks, not inconveniences.

Have participants complete their severity scores individually before group discussion. Individual scoring before group discussion prevents anchoring bias — when scores diverge by two or more points, discuss the evidence behind each score ([GLIDR on pain vs. frequency scores](https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores)). The goal is calibration, not consensus. If two people see the same problem very differently, that disagreement is signal.

---

### Part 3: Clustering methodology

After the workshop, you have a list of individual pain points. Some of them are symptoms of the same underlying failure. The clustering step makes that visible.

**Why this matters:** The cost and solvability of a cluster — not of an individual pain point — is what drives the build decision. A tool that fails in five different ways because it cannot edit a funnel after it is created has one root cause, not five separate problems. Cluster it correctly and you can cost it, scope it, and apply the solvability filter to it. Leave it as five separate complaints and you cannot.

**How to cluster:**

1. Group pain points by feature area — the part of the tool where the problem lives.
2. For each group, write a single sentence naming the cluster by its business consequence.

The sentence structure that works:

> *[Feature area] does not [capability], which prevents us from [business outcome] / results in [business consequence].*

Three examples from our Recruitee assessment:

- *Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics.*
- *Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics.*
- *It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles.*

Writing this sentence is the test for whether your cluster is ready. If you cannot articulate the business consequence in one sentence, the cluster is not ready for cost estimation. Either the grouping is wrong, or you need to dig further into what the root cause actually is.

A good cluster has 3–8 individual pain points, one dominant feature area, and a business consequence you can write in one sentence. If 15 pain points land under one cluster, it is probably two clusters.

**Appunite's result:** 24 individual problems collapsed into 7 clusters. A ratio of roughly 3–4 pain points per cluster is typical for a tool that has been in use for a year or more. By that point, users have found most of the friction — even if they have normalized it.

---

### Part 4: The solvability filter

I think the solvability filter is the most underrated step in this entire process. It is the point where the methodology either earns its credibility or loses it.

The most common failure mode in pain point assessment: teams find 20 problems, assume all 20 require new software, build the tool, and six months later three of those problems still exist. Because the root cause was never the software. The filter is what prevents this. Without it, you have a list of complaints with numbers attached. With it, you have a rigorous assessment.

Apply the filter to every cluster before moving to cost estimation.

**Q1: Is this a software problem or a process problem?**

Test: if we had unlimited configuration in the current tool, would this problem still exist? If yes, it is a process problem. Building new software will not fix it.

This is the uncomfortable question. Teams are reluctant to identify process problems in a tool assessment because it feels like a criticism of the team rather than the tool. Run it anyway. A process problem that gets built into a custom tool is a process problem you now own and maintain.

**Q2: Could a different SaaS solve this?**

Switching SaaS is almost always cheaper and faster than building custom software. The bar for building is: no existing product solves this adequately, or the switching cost across all pain points exceeds the build cost. If a different SaaS would solve two of your seven clusters, factor that in before deciding to build everything.

**Q3: Does solving this require data ownership or custom logic no SaaS can provide?**

This is where building typically wins. If the pain requires querying data in ways the vendor does not expose, building workflows that do not exist in any available tool, or maintaining context outside any vendor's data model — custom software has a structural advantage that switching cannot address.

Appunite's answer to Q3: the ability to track candidate relationships over time, surface past candidates for new roles based on competency data, and own the full history of every interaction. No ATS we evaluated offered this as a native feature. That answer cleared the filter.

---

## How we clustered 24 problems into 7 themes

When we finished the clustering step, something clicked. The 24 problems had not felt like 24 separate things during the workshop — there was overlap, similarity, obvious groupings. But it was only when we wrote the business consequence sentence for each cluster that the actual shape of the problem became clear.

Most of the friction traced back to seven root failures. Not 24.

| # | Cluster | Business consequence |
|---|---|---|
| 1 | Reports calculate with errors | Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics. |
| 2 | Metrics not customisable | Metrics cannot be configured to match our actual process, limiting pipeline visibility to whatever the vendor decided to surface. |
| 3 | Funnels not elastic | Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics. |
| 4 | No competency matrices + sourcing inefficiency | It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles. |
| 5 | No interview transcription + manual feedback | There is no structured way to capture or review interview content, meaning hiring signal is lost and each evaluation cycle depends on memory rather than data. |
| 6 | Calendar/scheduling gaps + workflow coordination | Scheduling and coordination require manual effort for every step, adding friction to each hiring cycle and increasing time-to-hire. |
| 7 | GDPR compliance gaps + manual processing | GDPR-required actions cannot be automated, creating compliance risk and recurring manual processing that scales with hiring volume. |

The clustering also revealed which problems were worth the most attention. Cluster 1 — reporting errors — turned out to be the single largest cost contributor at 101,520 PLN per year once we ran the cost model. Not because reports were the most frequently mentioned complaint, but because the business consequence was the largest: inaccurate reporting data touches every downstream decision. The full cost breakdown by cluster is in [Part 2 of this series](https://appunite.com/blog/hold-my-beer-building-custom-ats).

One thing I had not anticipated: several complaints that appeared unrelated during the workshop turned out to share a single root cause once we wrote the cluster sentences. Two problems listed under different workflow areas both traced back to funnels being ineditable after creation. Without the explicit clustering step, those would have been counted separately — and the cost of fixing that one root cause would have been underestimated while the complexity was overstated.

The ratio of 3–4 pain points per cluster also turned out to be meaningful. It is roughly what you expect from a tool in use for a year or more: by that point, users have found most of the surface friction, even if they have stopped registering it as friction.

---

## What this approach revealed that "just asking" wouldn't

The most interesting finding was not the 24 problems. It was the problems nobody had thought to report.

The clearest example: Recruitee told us our time-to-hire was 23 days. The real number was 31. Nobody had flagged this as a problem. Everyone was using the number the tool gave them, because questioning the tool's output at that level of detail had stopped being a habit. The expectation of accuracy had been abandoned so gradually that nobody could point to the moment it happened. The workaround — using the 23-day figure and treating it as roughly correct — was so automatic it had become invisible.

This is the adapted-around problem in its clearest form. The pain is real and measurable. The signal is gone because the user gave up on accuracy and stopped asking.

Direct questioning would not have found this. "What bothers you about Recruitee's reporting?" would have produced complaints about interface quirks, missing filters, slow load times. The JTBD framing — "what are you trying to accomplish when you pull a time-to-hire report?" — surfaced the underlying job: getting an accurate number to make headcount decisions. Once the job was named, the gap between what the tool provided and what the job required became visible. The eight-day discrepancy had been there the whole time.

We found other versions of the same pattern. Problems that participants had categorized as "just how hiring works" turned out to be tool-specific. When users described their actual goal rather than their experience with the current tool, the gap appeared. The JTBD question is not just a reframe — it creates a different kind of answer.

The solvability filter caught one or two items that were process problems, not software problems. Without the filter, those would have been scoped into the build. Built. And not fixed. Because the root cause was never Recruitee.

To give the numbers context: the total estimated annual cost came to 150,648 PLN, of which 85% is opportunity cost. The direct, measurable time losses amount to 22,524 PLN per year. The gap between those two figures is driven almost entirely by the reporting errors cluster and its downstream effect on hiring decisions. That is why the attribution assumption for Cluster 1 is the most important number to examine before committing. Appunite's assumption was that 50% of failed hires traced back to inaccurate reporting data — one number that moves the ROI from -74% to +75%. Changing it changes everything. The full financial breakdown is in [Part 2](https://appunite.com/blog/hold-my-beer-building-custom-ats).

Structured methodology finds these things because it creates the conditions for them to surface. Direct questions get direct answers — which are incomplete by the nature of adapted-around pain. JTBD and CIT are specifically designed to get around the human tendency to stop noticing.

---

## How to do this yourself

This methodology does not require a research background. It requires blocking time, preparing templates, and being rigorous about the solvability filter. Any team lead can run this in a week.

**Seven steps:**

1. Pick one SaaS tool with documented friction — something your team complains about regularly, or that you suspect is mismatched with your actual process. The first article in this series ([The SaaS Tax](https://appunite.com/blog/the-saas-tax)) lays out why mismatched tools are worth examining systematically.
2. Build the feature list from the vendor's documentation and a 30-minute walkthrough. Aim for completeness. Specificity matters more than speed here — a rough list produces rough results.
3. Run the feature audit with 2–3 daily users. Calculate your usage ratio and required ratio. These numbers anchor everything that follows.
4. Send the pain point collection template to workshop participants at least 24 hours in advance. Ask for five or more entries before the session. Pre-work is not optional — it changes the quality of what happens in the room.
5. Run the 90-minute workshop. Individual scoring first, group calibration second. Extend to two hours if the energy is high.
6. Cluster the pain points by feature area. Write the business consequence sentence for each cluster before moving to cost estimation. If you cannot write the sentence, the cluster is not ready.
7. Apply the solvability filter to every cluster. Do not skip this step. This is the one that separates a rigorous assessment from a post-hoc justification.

If you want to have a detailed blueprint, you can download it here. https://www.appunite.com/is-saas-over-honest-evaluation

The next post covers the full pain point breakdown — all 7 clusters, every pain point, and the cost methodology behind each number. If you want to see exactly how a specific cluster was costed, that post will have it. The methodology described here becomes concrete when you see the actual numbers it produced.

---

### Sources

- Pendo — 2019 Feature Adoption Report: https://www.pendo.io/resources/the-2019-feature-adoption-report/
- Nielsen Norman Group — Critical Incident Technique: https://www.nngroup.com/articles/critical-incident-technique/
- Product School — Jobs to Be Done Framework: https://productschool.com/blog/product-fundamentals/jtbd-framework
- GLIDR — Pain vs Frequency Scores: https://help.glidr.io/en/articles/2826779-pain-vs-frequency-scores
