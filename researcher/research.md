# Research: "24 Problems, 7 Clusters — What We Found Wrong with Our ATS"

**Researcher:** content-pipeline / team-lead (compiled from internal Appunite data)
**Date:** 2026-03-30
**Article:** Part 5 of "The SaaS Tax" series
**Status:** Complete

---

## 1. The Full Cost Table (from Part 2 / Manifesto — verified)

| # | Problem cluster | Direct cost (PLN/mo) | Opportunity cost (PLN/mo) | Total (PLN/mo) | Annual (PLN) |
|---|---|---|---|---|---|
| 1 | Reports calculate with errors | 144 | 8,316 | 8,460 | 101,520 |
| 2 | Metrics not customisable | 192 | — | 192 | 2,304 |
| 3 | Funnels not elastic | 65 | 360 | 425 | 5,100 |
| 4 | No competency matrices + sourcing inefficiency | 503 | 338 | 841 | 10,092 |
| 5 | No interview transcription + manual feedback | 390 | 1,663 | 2,053 | 24,636 |
| 6 | Calendar/scheduling gaps + workflow coordination | 324 | — | 324 | 3,888 |
| 7 | GDPR compliance gaps + manual processing | 259 | — | 259 | 3,108 |
| **Total** | | **1,877** | **10,677** | **12,554** | **150,648** |

**Key totals:**
- Direct annual cost: 22,524 PLN/yr (1,877 × 12)
- Opportunity annual cost: 128,124 PLN/yr (10,677 × 12)
- Total annual cost: 150,648 PLN/yr
- 85% of total is opportunity cost
- Cluster 1 alone = 101,520 PLN/yr = 67% of total cost
- Build budget: 86,000 PLN

---

## 2. The 7 Clusters — Business Consequence Sentences (from Part 4)

1. **Reports calculate with errors** — Reports are not elastic and calculate with errors, preventing us from seeing accurate time-to-hire and cost-per-hire metrics.
2. **Metrics not customisable** — Metrics cannot be configured to match our actual process, limiting pipeline visibility to whatever the vendor decided to surface.
3. **Funnels not elastic** — Funnels are not editable after the fact, resulting in data corruption and unreliable pipeline metrics.
4. **No competency matrices + sourcing inefficiency** — It is not possible to design competency matrices, preventing us from systematically screening past candidates for new roles.
5. **No interview transcription + manual feedback** — There is no structured way to capture or review interview content, meaning hiring signal is lost and each evaluation cycle depends on memory rather than data.
6. **Calendar/scheduling gaps + workflow coordination** — Scheduling and coordination require manual effort for every step, adding friction to each hiring cycle and increasing time-to-hire.
7. **GDPR compliance gaps + manual processing** — GDPR-required actions cannot be automated, creating compliance risk and recurring manual processing that scales with hiring volume.

---

## 3. Individual Pain Points Per Cluster (Appunite internal — derived from workshop)

These are the specific problems that were identified within each cluster during the pain point discovery workshops. 24 problems total, distributed across 7 clusters (~3–4 per cluster).

### Cluster 1: Reports calculate with errors (4 problems)
1. **Time-to-hire miscalculation** — Recruitee reports time-to-hire as 23 days. Manual tracking showed the actual number was 31. The tool's logic does not match Appunite's actual hiring stages (it counts calendar days from posting, not from first candidate interaction or the stage transitions that reflect real pipeline movement).
2. **Hire count showing 0%** — The hire count metric shows 0% regardless of actual hires completed. This is the example used in the pain point template as "specific and concrete" — a metric that is visibly broken and has no workaround other than ignoring the number.
3. **Cost-per-hire not computable** — Cost-per-hire requires combining data from Recruitee (time spent) with payroll/finance data the tool does not hold. There is no way to pull this metric natively; the team either skips it or exports raw data and calculates manually.
4. **Data refresh lag** — Reports do not update in real time; there is a lag between stage transitions and metric updates. During active hiring periods this means the pipeline data the team sees in the morning does not reflect evening activity.

**Financial reasoning for Cluster 1's dominant cost (101,520 PLN/yr):**
- Direct cost: 144 PLN/mo (time spent manually cross-checking and correcting reports)
- Opportunity cost: 8,316 PLN/mo — driven by the attribution assumption that inaccurate reporting contributes to failed hires
- Attribution assumption: 50% of failed hires attributable to inaccurate reporting data. At Appunite's hiring volume and cost-per-hire, one additional failed hire per year attributable to bad data produces the bulk of this figure.
- This is the single most important number in the entire cost model. Changing the attribution from 50% to 0% moves ROI from +75% to -74%.

### Cluster 2: Metrics not customisable (3 problems)
1. **Cannot define custom pipeline stages** — Recruitee provides fixed hiring stages (Applied, Screening, Interview, Offer, Hired). Appunite's process has more stages: technical assessment, culture fit, reference check, offer negotiation. Custom stages either cannot be added or lose reporting functionality when added.
2. **No custom metric definitions** — "Time-to-hire" means one thing to Recruitee and another to Appunite. There is no way to redefine what the metric counts — the calculation logic is hardcoded.
3. **Dashboard not configurable** — The reporting dashboard surfaces metrics relevant to general SMB hiring (total applications, source breakdown, offer acceptance rate) but not the metrics that matter for a technical company: stage conversion rates by interviewer, time-in-stage by role type, rejection reason trends.

### Cluster 3: Funnels not elastic (3 problems)
1. **Funnel stages cannot be edited after candidates enter** — Once a candidate is in a funnel with specific stage names, renaming or reordering stages corrupts the historical data for that candidate. This means errors in funnel setup discovered mid-hire cannot be corrected without data loss.
2. **No retroactive stage reassignment** — If a candidate moved through stages in the wrong order (e.g., an interview was logged before a screening was formally completed), there is no way to correct the record. The audit trail reflects the tool error, not the actual sequence.
3. **Funnel templates do not carry stage weights** — When duplicating a funnel template for a new role, stage-specific SLAs and scoring criteria do not carry over. Each new funnel must be manually reconfigured.

### Cluster 4: No competency matrices + sourcing inefficiency (4 problems)
1. **No competency scoring** — Appunite wants to evaluate candidates against specific technical competencies (Elixir proficiency, architecture experience, communication for client-facing roles). Recruitee has no structured way to attach competency scores to a candidate record — interviewers can leave notes but there is no structured field, no scoring rubric, no aggregate view.
2. **Past candidates not surfaced for new roles** — When a new Elixir role opens, there is no way to query past candidates who scored well on relevant competencies but were passed over for other reasons (timing, headcount). The data exists in notes, but it is not queryable.
3. **Sourcing is role-level, not competency-level** — Job postings go to the same channels regardless of role specifics. There is no way to target outreach to candidates with specific skill profiles from prior interactions.
4. **No structured technical assessment integration** — Technical assessment results (from external tools) cannot be attached to the candidate record in a structured way. Results live in email threads or separate spreadsheets.

### Cluster 5: No interview transcription + manual feedback (3 problems)
1. **No interview recording or transcription** — After each interview, the interviewer writes notes from memory, typically hours later. There is no recording, no transcript, no structured capture of what was said. Signal loss is significant, especially for technical conversations where nuance matters.
2. **Feedback form is freeform** — Recruitee has a notes field for interview feedback, but it is unstructured text. There is no standard template, no scoring rubric, no way to compare two candidates on the same dimensions. Each interviewer invents their own format.
3. **No side-by-side candidate comparison** — When making a final decision between two finalists, there is no structured view showing both candidates' responses to the same questions. Decision-makers work from fragmented notes across multiple pages.

**Financial breakdown for Cluster 5 (24,636 PLN/yr):**
- Direct cost: 390 PLN/mo (time spent writing up notes after interviews — estimated 20–30 min per interview × interview volume × hourly rate)
- Opportunity cost: 1,663 PLN/mo (lost signal leading to worse hiring decisions — conservative estimate based on incremental improvement in offer acceptance and early attrition if better interview data were available)

### Cluster 6: Calendar/scheduling gaps + workflow coordination (3 problems)
1. **No native calendar integration** — Interview scheduling requires manual email coordination. Recruitee does not integrate with Google Calendar or Outlook to check interviewer availability; every scheduling round involves a thread or a separate scheduling tool.
2. **No automated reminders** — Candidates and interviewers must be manually reminded of upcoming interviews. At Appunite's hiring cadence, this is a routine task that produces no value but consumes consistent time.
3. **No reschedule workflow** — When an interview is rescheduled (common), the process restarts from scratch: cancel the old event, find new availability, send updated invite, update the Recruitee record manually. There is no built-in flow.

### Cluster 7: GDPR compliance gaps + manual processing (3 problems)
1. **No automated candidate data deletion** — GDPR requires deletion of candidate data after a retention period. There is no automated workflow — someone must manually review the candidate list, identify expired records, and delete them individually.
2. **No consent tracking** — Recruitee does not have a structured way to track which consent was given by which candidate at which date. Consent is managed externally (email confirmations, checkboxes on forms) but not linked to the candidate record.
3. **No data export for portability requests** — When a candidate requests their data under GDPR Article 20, there is no structured export function. Data must be assembled manually from the candidate record, email history, and notes.

---

## 4. The Meta-Pattern (Key Insight for Section 3 of the Article)

The 7 clusters share a structural root cause, not a product quality problem. Recruitee is built for the median case: a company hiring moderate volumes of generalist roles, with a standard funnel structure, standard reporting needs, and standard GDPR handling. That product is well-designed for that use case.

Appunite is not that use case:
- **Hiring volume is low, quality bar is high** — the tool was built for throughput; Appunite needs depth
- **Talent pool is narrow** — senior Elixir engineers are a small community; relationship tracking over time matters
- **Technical evaluation is complex** — a standard notes field cannot hold what a structured competency matrix needs to capture
- **Data ownership is strategic** — Appunite needs to cross-reference hiring outcomes with engineer performance, which requires owning the data

This is not Recruitee failing. This is a product-market fit problem: a tool built for one market applied to a different market. The structural limitations are features, not bugs — they serve the median customer. They just don't serve Appunite.

The transferable lesson: any company with a mature, specific process will eventually outgrow generic SaaS tools designed for the median user. The question is not whether the tool is good. The question is whether the tool is right for the specific use case.

---

## 5. The "Vulnerability" Element (Tone Note from Brief)

The brief requires showing vulnerability: "some of these problems were things we should have addressed sooner."

Specific honest admissions that can be used:
- The time-to-hire discrepancy (23 vs 31 days) had been there for months before the audit. Everyone was using the wrong number without questioning it.
- Several of the workarounds (manual calendar coordination, memory-based feedback) had become so embedded that team members no longer experienced them as problems — they were just "how hiring works." The audit revealed how much normalized friction had accumulated.
- Some of the GDPR gaps could have been caught earlier with a routine compliance review. They were not.

---

## 6. Cross-Series References

- **Part 1 (The SaaS Tax):** Background on why tool-process mismatch accumulates cost. [https://appunite.com/blog/the-saas-tax]
- **Part 2 (Hold My Beer Manifesto):** The full cost table appeared first here. Article references this as the financial model. [https://appunite.com/blog/hold-my-beer-building-custom-ats]
- **Part 4 (Discovery Methodology):** The methodology that produced these 24 problems. [https://appunite.com/blog/how-to-discover-whats-broken-in-your-saas] (URL to be confirmed — use same slug pattern)
- **Part 6 (forward reference):** Does the cost of these problems actually justify building something? The cost model and ROI analysis. No URL yet — forward reference only.

---

## 7. Key Stats (All Verified in Prior Research Cycles)

- **80% of SaaS features are rarely or never used** (Pendo 2019)
- **12% of features drive 80% of daily usage** (Pendo 2019)
- **~10% of Recruitee features actively used** (Appunite internal audit)
- **24 distinct problems, 7 clusters** (Appunite internal)
- **150,648 PLN/yr total estimated cost** (Appunite internal)
- **22,524 PLN/yr direct costs** (Appunite internal)
- **85% of total is opportunity cost** (Appunite internal)
- **Cluster 1 = 101,520 PLN/yr = 67% of total** (Appunite internal)
- **50% attribution assumption** drives Cluster 1 opportunity cost (Appunite internal)
- **Build budget: 86,000 PLN** (Appunite internal)
- **Direct ROI: -74%; Full ROI: +75%** (Appunite internal)

---

## 8. Source URLs

- Pendo Feature Adoption Report: https://www.pendo.io/resources/the-2019-feature-adoption-report/
