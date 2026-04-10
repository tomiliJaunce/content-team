# Handoff: Researcher → Content Specialist

**Article:** "24 Problems, 7 Clusters — What We Found Wrong with Our ATS"
**Series:** The SaaS Tax — Part 5
**Date:** 2026-03-30
**Status:** Research complete. Ready for content brief.

---

## What Was Found

### Core Data: The 7 Clusters with Full Cost Breakdown

All data is Appunite internal, verified in prior research cycles.

| # | Cluster | Direct (PLN/yr) | Opportunity (PLN/yr) | Total (PLN/yr) |
|---|---|---|---|---|
| 1 | Reports calculate with errors | 1,728 | 99,792 | 101,520 |
| 2 | Metrics not customisable | 2,304 | — | 2,304 |
| 3 | Funnels not elastic | 780 | 4,320 | 5,100 |
| 4 | No competency matrices + sourcing | 6,036 | 4,056 | 10,092 |
| 5 | No interview transcription + feedback | 4,680 | 19,956 | 24,636 |
| 6 | Calendar/scheduling gaps | 3,888 | — | 3,888 |
| 7 | GDPR compliance gaps | 3,108 | — | 3,108 |
| **Total** | | **22,524** | **128,124** | **150,648** |

Key facts to communicate throughout the article:
- 85% of 150,648 PLN total is opportunity cost
- Cluster 1 alone = 67% of total cost (101,520 PLN/yr)
- Cluster 1's opportunity cost rests on one attribution assumption: 50% of failed hires attributable to inaccurate reporting data
- Build budget: 86,000 PLN; Direct ROI: -74%; Full ROI: +75%

### Individual Pain Points (24 total across 7 clusters)

Detailed breakdown in research.md Section 3. Summary counts:
- Cluster 1: 4 problems (time-to-hire miscalculation, hire count showing 0%, cost-per-hire not computable, data refresh lag)
- Cluster 2: 3 problems (custom pipeline stages, custom metric definitions, non-configurable dashboard)
- Cluster 3: 3 problems (stages can't be edited after candidates enter, no retroactive reassignment, templates don't carry weights)
- Cluster 4: 4 problems (no competency scoring, past candidates not surfaced, sourcing not competency-level, no structured assessment integration)
- Cluster 5: 3 problems (no recording/transcription, freeform feedback only, no side-by-side comparison)
- Cluster 6: 3 problems (no native calendar integration, no automated reminders, no reschedule workflow)
- Cluster 7: 3 problems (no automated deletion, no consent tracking, no data export for portability requests)

### The Meta-Pattern (Section 3 Key Insight)

These aren't bugs. Recruitee works fine for its target market. The structural limitations exist because the tool was built for the median case — SMBs with moderate hiring volumes of generalist roles. Appunite is not that case:
- Low volume, high quality bar → tool optimized for throughput
- Narrow talent pool → needs relationship tracking over time
- Complex technical evaluation → standard notes field can't hold structured competency data
- Strategic data ownership → needs to cross-reference hiring outcomes with engineer performance

This framing is essential: every limitation can be explained as "designed for millions of users." Never as "badly built."

### Vulnerability Element (Required by Brief)

The brief explicitly requires showing vulnerability. Honest admissions available:
- The 23-day vs 31-day discrepancy had been there for months before the audit. Everyone was using the wrong number.
- Several workarounds had become so embedded they were no longer experienced as problems — they were "just how hiring works."
- GDPR gaps could have been caught with a routine compliance review.

---

## The Narrative Core the Content Specialist Must Know

**The surprising finding:** 85% of the financial impact comes from opportunity costs, not from time wasted on workarounds. The headline number (150,648 PLN/yr) is not primarily about lost productivity — it is primarily about decisions made on bad data.

**The article's structure per user brief:**
1. 7 clusters at a glance (table overview)
2. Top 3 deep dives — most relatable and impactful: **Cluster 1** (bad data, biggest cost), **Cluster 5** (interview feedback loss, universally relatable), **Cluster 4** (competency tracking, specific to engineering hiring). Writer may choose Cluster 6 (scheduling) as an alternative for Cluster 4 if more universal appeal is preferred.
3. The meta-pattern — these are structural limitations, not bugs
4. Transferable lesson for readers' own tools
5. Closing setup for Part 6 (does the cost justify building?)

**Tone requirements:**
- Positive campaign — no snark about Recruitee. "Designed for millions of users" is the explanation.
- Show vulnerability — some of these should have been addressed sooner
- Authentic and detailed — real data, nothing hidden
- Audience: Tier 1 CTOs + Tier 3 engineers who love detailed breakdowns

---

## Full Research File

All cluster details, individual pain points, meta-pattern analysis:
`/Users/Blazej/Code/content-team/researcher/research.md`

---
**Status:** Research complete — all data Appunite internal, verified. No external sources needed for this article beyond Pendo 2019 for context.
