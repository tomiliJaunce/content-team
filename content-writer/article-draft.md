# 24 Problems, 7 Clusters — What We Found Wrong with Our ATS

**Author:** Błażej Cepil
**Series:** The SaaS Tax — Part 5

---

**TL;DR:** The discovery methodology from [Part 4](https://www.appunite.com/blog/how-to-discover-whats-actually-broken-in-your-saas-tool) produced 24 specific problems across 7 clusters, with a total estimated cost of 150,648 PLN per year — 85% of which is opportunity cost, not direct time loss. This post walks through all 7 clusters: what each problem looks like in practice, why Recruitee cannot solve it structurally, and what the financial breakdown behind each cluster means for the decision ahead.

---

## The 7 clusters at a glance

The ATS problems we found fell into two cost categories: direct costs (time your team actually burns doing manual work) and opportunity costs (the harder-to-measure downstream consequences). The full picture, across all 7 clusters, looks like this.

The methodology behind these numbers is in [Part 4](https://www.appunite.com/blog/how-to-discover-whats-actually-broken-in-your-saas-tool). The cost model was [first introduced in Part 2](https://www.appunite.com/blog/manifesto-building-our-own-ats) in monthly form. What follows is the annual view with problem counts added.

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

Two things worth naming before the deep dives. Cluster 1 alone accounts for 101,520 PLN/yr — 67% of the total — despite containing only 4 of the 24 problems. And 85% of the total (128,124 PLN/yr) is opportunity cost, not direct time loss. That composition matters for how the numbers should be read, and for what it would take to justify the build. The next section covers the three clusters where that story is most concentrated.

---

## The top 3 that matter most

### Cluster 1 — Reports calculate with errors

On a typical morning during an active hiring period, someone opens the tool to check the pipeline before a planning meeting. The time-to-hire metric reads 23 days. Manual tracking shows the real number is 31. That is not a rounding error — it is an eight-day gap between what the tool reports and what the process actually does.

The calculation logic counts calendar days from job posting. Appunite's pipeline does not start the clock there. What matters is from first candidate interaction, or from the stage transitions that reflect actual movement through the funnel. Those two definitions produce different numbers. There is no configuration option that changes the underlying logic. It is hardcoded — built for the median case, and the median case defines time-to-hire differently than we do.

The other three problems in this cluster compound this. The hire count metric shows 0% regardless of actual completed hires — this is not a data lag, it is a metric that is visibly broken with no workaround other than ignoring it. Cost-per-hire requires combining Recruitee data with payroll data the tool cannot access, so the team either skips the metric or exports raw data and calculates manually. Reports do not update in real time, so morning pipeline data does not reflect the previous evening's activity during active hiring periods.

Here is the honest part. The 23-day discrepancy had been there for months before the audit. Every planning meeting, every hiring retrospective, every headcount conversation was built on the wrong number. Not because nobody cared about accuracy — because questioning the tool's output at that level had stopped being a habit. The expectation of accuracy had been abandoned so gradually that nobody could locate the moment it happened.

Cost: 101,520 PLN/yr total — 1,728 PLN/yr direct (time manually cross-checking and correcting reports) and 99,792 PLN/yr opportunity.

That opportunity cost figure carries an assumption that must be named explicitly. It rests on the estimate that 50% of failed hires trace back to decisions made on inaccurate reporting data. At Appunite's hiring volume and cost-per-hire, one additional failed hire per year attributable to bad data produces the bulk of that number. I think the attribution is reasonable. Inaccurate pipeline data does affect headcount decisions, and headcount decisions do affect hiring outcomes. But I cannot prove the exact causal chain. At 0% attribution, the ROI on the entire build project moves from +75% to -74%. That is not a footnote. It is the most consequential single number in the cost model, and every figure that follows should be read with that in mind.

---

### Cluster 5 — No interview transcription + manual feedback

The interview ends. The interviewer goes back to their desk. Somewhere between two hours and the following morning, they write their notes from memory. The feedback form is an open text field. No template, no scoring rubric, no standard dimensions to respond to. One interviewer writes three sentences. Another writes three paragraphs. A third uses bullets that map to nothing the next interviewer used for the same candidate.

When the hiring team meets to decide between two finalists, they are comparing things that cannot actually be compared. The notes exist. The signal from the conversation — the candidate's explanation of a system design decision, the specific way they navigated a difficult scenario — mostly does not.

This is not a failure of the interviewers. It is what happens when the feedback structure is a blank text field. There is no recording, no transcript, no structured capture of what was said. After each technical conversation, what was discussed lives only in the interviewer's memory until they write it up, and degrades from the moment the call ends. When making a final decision between two strong candidates, there is no structured view showing both side by side. Decision-makers work from fragmented notes in different formats written at different times.

Recruitee's feedback model was designed for the use case where notes are sufficient — generalist roles, standard interview formats, lower technical depth. For evaluating senior Elixir engineers on architecture decisions, system design thinking, and communication quality in client-facing contexts, an open text field is not a data structure. These are not Recruitee limitations in the defect sense — they are design boundaries. No configuration of the existing fields produces structured, comparable, searchable interview data. The product was not built for this, because most of its customers do not need this.

Cost: 24,636 PLN/yr total — 4,680 PLN/yr direct (20–30 minutes per interview for post-interview writeups, multiplied by interview volume and hourly rate) and 19,956 PLN/yr opportunity (lost signal leading to worse offer acceptance rates and early attrition outcomes, at a conservative estimate).

---

### Cluster 4 — No competency matrices + sourcing inefficiency

A new senior Elixir role opens. The team remembers that six months ago, they interviewed someone strong — the timing was wrong, headcount had not been approved. That candidate exists in the system. Their interview notes exist too. But there is no way to search for "candidates with strong Elixir scores, passed over for timing rather than performance." The data is in a text field. It is not queryable.

So the recruiter starts from zero: same job boards, same outreach, same channels. A candidate the team already knew was qualified goes untouched, because there is no path from "new role opens" to "here are the people we already evaluated."

The four specific problems: no structured competency scoring, so there is no aggregate view across interviewers and no way to compare candidates systematically; past candidates are not surfaceable for new roles, because the data exists in notes rather than in queryable fields; sourcing is role-level, not competency-level, so there is no way to target outreach based on documented profiles from prior interactions; and technical assessment results from external tools cannot be attached to the candidate record in a structured way — they live in email threads or spreadsheets, disconnected from the candidate's history.

Recruitee was designed for companies hiring generalists at moderate volume, where each candidate interaction is relatively self-contained and the talent pool is large enough that re-sourcing from scratch is manageable. Senior Elixir engineers are a small community, and the relationship with a candidate who was good-but-wrong-timing has real value months or years later. The tool's data model was never built to support longitudinal candidate relationships because most of its customers do not need that.

Cost: 10,092 PLN/yr total — 6,036 PLN/yr direct (recruiter time on manual sourcing steps that a competency-indexed system would reduce) and 4,056 PLN/yr opportunity (cost of re-sourcing from scratch rather than surfacing known, pre-qualified candidates).

---

## The pattern across all 7

The seven clusters are not a list of failures. They share a single structural root cause: Recruitee was built for the median case, and Appunite is not that case.

The median case looks like this: a company with moderate hiring volumes, generalist roles, a standard funnel structure, standard reporting needs, and standard GDPR handling. That product is well-designed for that market. The calculation logic, the feedback model, the sourcing structure, the compliance handling — all of it makes sense for an SMB hiring across a range of roles from a large talent pool.

Appunite's use case differs on four dimensions. Hiring volume is low and the quality bar is high — the tool was optimized for throughput, but what matters here is depth of evaluation at each step. The talent pool is narrow — senior Elixir engineers are a small community where relationship tracking over time carries strategic value. Technical evaluation is complex in ways a standard notes field cannot accommodate. And data ownership is strategic — cross-referencing hiring outcomes with actual engineer performance post-hire requires owning the data model, not renting access to it.

This is a product-market fit problem, not a product quality problem. A tool built for one market, applied to a different market. The structural limitations in all seven clusters are features of what Recruitee built — they just do not serve Appunite's specific use case.

There is a second thing worth naming here, less comfortable than the structural analysis. When we ran the audit, several of the workarounds had become invisible. Manual calendar coordination. Memory-based interview feedback. The 23-day time-to-hire figure. These were not experienced as problems — they had become "how hiring works." One small adaptation at a time, the friction had accumulated until it was just the texture of the process. The team was not oblivious. The friction had simply stopped registering, which is a different thing, and the audit was what made it visible again.

---

## What this means for your tools

This article is not a Recruitee review. It is a case study in what happens when a mature, specific process meets a generic tool. The recruitment software issues we found are a specific version of a more general pattern. If you manage a technical team and use any SaaS for a process that is central to how you work, the pattern is probably familiar.

The thing that made our audit productive was not the software we were auditing — it was the questions we asked. Three in particular cut through the normalized friction.

Are there metrics in your tool you cannot customize, where the vendor's definition does not match what your process actually needs to measure? In our case, "time-to-hire" meant one thing in the codebase and another in our actual pipeline. We did not know the gap was eight days until we measured it directly. If you are using tool-generated metrics to make decisions — headcount, capacity planning, team sizing — it is worth verifying that the calculation matches your process definition, not just the general-purpose one.

Are there workflows you cannot modify, where the tool's structure forces your process to conform to its logic? The inelastic funnel structure and the fixed feedback form both fall here. The cost is not just friction — it is decisions made on data shaped by the tool's constraints rather than by what your process actually requires.

Is there data in your tool you cannot cross-reference, where the information exists inside the system but cannot be queried in the ways your decisions require? Past candidates, assessment results, competency scores, longitudinal outcome data — these exist in our system as text in fields that cannot be searched or combined. The data is there. It is just not accessible in a useful form.

If the answer to any of these is yes, the [SaaS Tax framework](https://www.appunite.com/blog/business-paying-for-100-saas-using-12) applies. The question is not whether your tool is good. The question is whether it is right for your specific use case — and whether the gap has become invisible enough that you have stopped asking.

---

## Closing note

The audit is complete. The numbers are as honest as they can be given the constraints.

24 problems across 7 clusters. Total estimated cost: 150,648 PLN/yr — 22,524 PLN/yr in direct costs that show up on timesheets, and 128,124 PLN/yr in opportunity costs that require attribution assumptions to reach. Cluster 1 alone accounts for 67% of the total, and its opportunity cost rests on the assumption that 50% of failed hires trace back to inaccurate reporting data. That assumption is reasonable. It cannot be proven.

Against a build budget of 86,000 PLN, the evidence raises a question it cannot fully answer. Direct savings alone produce a -74% ROI. Including opportunity costs produces +75%. The case only works if a meaningful fraction of those opportunity costs are real — and the largest portion depends on a single attribution assumption that can be argued, not verified.

That question — whether the assumptions hold, and whether the cost evidence actually justifies building — is what the next post addresses. The evidence is on the table. The verdict is not.

---

### Sources

- Part 1 — The SaaS Tax: https://www.appunite.com/blog/business-paying-for-100-saas-using-12
- Part 2 — Hold My Beer (The Manifesto): https://www.appunite.com/blog/manifesto-building-our-own-ats
- Part 4 — How to Discover What's Actually Broken in Your SaaS Tool: https://www.appunite.com/blog/how-to-discover-whats-actually-broken-in-your-saas-tool
