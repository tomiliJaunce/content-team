# Why We Chose ATS as Our First Custom Replacement

**Author:** Karol Wojtaszek
**Series:** The SaaS Tax — Part 3

---

**TL;DR:** When deciding which SaaS tool to replace first, we use four questions: Is your process more specific than the tool allows? Is valuable data trapped in the vendor's platform? Do you use less than 20% of features? Could the 10% you need create competitive advantage if custom-built? Our ATS scored yes on all four — winning on process specificity and competitive advantage potential in particular. Project management tools and our CRM each scored around two out of four. This build-vs-buy decision framework produced a clear ranking, not a post-hoc justification.

---

Deciding to build something is straightforward compared to deciding what to build first. After [the first post in this series](https://appunite.com/blog/the-saas-tax) made the case for the SaaS tax, and [our decision post](https://appunite.com/blog/hold-my-beer-building-custom-ats) announced we were doing something about it, the most common follow-up question was: why the ATS?

The answer is not that the ATS was obviously the right place to start. It is that when we applied a consistent build-vs-buy decision framework to every tool in our stack, the ATS scored highest. That distinction matters. A framework that produces "yes" everywhere is a rationalization engine. Ours produced a clear ranking, and the ATS earned the top spot.

Here is the framework, how we applied it, and what it produced.

---

## Four questions to score any SaaS tool

We evaluate any candidate for replacement using four questions. Each is a yes or no. Four yeses make a strong build candidate. Below three and the case needs to be exceptional to hold up. Organizations that use structured build-vs-buy decision frameworks report 30–40% fewer implementation failures than those that make the call on instinct (FullScale, 2025). The point of the framework is not false precision — it is a forcing function that keeps the analysis honest.

**1. Is your process more specific than the tool allows?**

This is about whether your specific way of doing this work is structurally constrained by how the vendor designed the product. Geoffrey Moore's Core vs. Context model, from *Dealing with Darwin* (2005), provides the underlying logic: Core processes are where your specific execution creates competitive advantage. Context processes are everything else — necessary to operate, but not a source of differentiation.

The question to ask is whether this tool handles a Core or Context process for your company. For a generic HR department, recruitment is Context. For a software company competing on team quality, it is Core. The same tool can be the right answer for one company and the wrong answer for another, even if both are looking at the same product on the same pricing page.

**2. Is valuable data trapped in the vendor's platform?**

Not "can I export a CSV?" The question is whether the value of this data compounds over time. Candidate histories, evaluation records, relationship data built over years — these become more useful the longer they accumulate. As [we described in the first post in this series](https://appunite.com/blog/the-saas-tax), lock-in is not just a switching cost you pay once. It is a cost that grows every year as more institutional knowledge accumulates in someone else's database, bounded by their data model and API limits.

**3. Do you use less than 20% of features?**

This maps directly to the SaaS tax argument. The question is what portion of your licensing cost funds features designed for someone else's workflow. The 12% daily feature usage figure from Part 1 is the industry average. For a specialized company using a general-purpose tool, the fraction you actually use is probably lower — and the price reflects all the users who use the rest.

**4. Could the 10% you actually need create competitive advantage if custom-built?**

This is the separator. Many tools score yes on the first three questions but no on the fourth — a custom version would be better, but not in any way that shifts the competitive needle. The test is whether the capabilities that become possible with custom ownership are ones competitors cannot easily replicate, and that compound in value over time.

Score each question yes or no. Four out of four: strong build candidate. Three or below: the case needs to be exceptional.

---

## How ATS answered each question

One note before going through the criteria: the full financial analysis — the 86,000 PLN build budget, the cost breakdown by cluster, the ROI table — lives in [our decision post](https://appunite.com/blog/hold-my-beer-building-custom-ats). This section is about the qualitative scoring. We will reference the figures where they help, but we are not running the table again.

**Q1 — Process specificity: Yes**

Recruitment at a software company is Core, not Context. The quality of the engineering team is the product. Every client engagement depends on it.

More specifically: we hire from one of the smallest senior talent pools in European tech. Senior Elixir engineers are scarce. Our interview process uses technical competency matrices specific to Elixir skills and seniority levels. Our sourcing needs to be surgical.

Recruitee was built for general SMBs with 50 to 500 employees doing moderate-volume hiring across a range of roles. We are not that market. This is not a criticism of Recruitee — it does what it was designed to do. The mismatch between our process and what the tool was designed for is structural. Configuration does not fix it.

**Q2 — Data trap: Yes**

A candidate who was not the right hire two years ago might be the right hire today. For a company drawing from a narrow talent pool, longitudinal relationship data has compounding value. It represents years of evaluation records, technical interview notes, sourcing touchpoints, and context about why someone was or was not hired.

If that data lives in Recruitee's database under Recruitee's data model, what we can do with it is bounded by Recruitee's API and feature set. The data exists — but it cannot be interrogated in any way we have not been explicitly given access to.

**Q3 — Feature underuse: Yes**

Our internal workshops identified 24 documented pain points across 7 clusters. Some of the capabilities we use most are a small fraction of what Recruitee offers. Several of the capabilities we need most — customizable competency tracking, structured technical assessment integration, reliable reporting tied to our actual process — do not exist in the product.

The cost figures from our decision post put direct annual spend at 22,524 PLN and the full estimated cost including opportunity cost at 150,648 PLN, against an 86,000 PLN build budget. The direct ROI case is negative at -74% in year one. The positive case (+75%) depends on whether you believe the opportunity cost estimates are real — and we were transparent in our decision post about exactly where that uncertainty lives. Also the fit did not improve while the Recruitee cost went up.

**Q4 — Competitive advantage potential: Yes (the decisive criterion)**

This is where the ATS separated from everything else in our stack.

Three capabilities become possible with a custom tool that are unavailable on any general-purpose ATS at any price.

First: AI-powered candidate matching calibrated to our specific requirements — Elixir stack depth, seniority level, client-facing capability. Not a generic match score, but one built around the exact profile we hire for and the reasoning behind it.

Second: longitudinal tracking of how our hiring criteria correlate with actual engineer performance after joining. This closes the feedback loop between recruiting and delivery quality. When we know a particular competency signal predicts long-term success on client projects, we can weight it higher. When one turns out not to matter, we can stop measuring it. None of that is possible when recruiting data lives separately from anything that could tell us how those hires performed.

Third: tight integration with our technical assessment process, so interviewers see structured competency data in real time — not reconstructing notes hours after the conversation ended.

None of these require exotic technology. They require owning the data model. That is what makes them impossible on Recruitee and possible on a custom build.

Q4 is the reason the ATS scored 4/4 when other tools in our stack did not.

---

## The maintenance question

70% of total software costs come after implementation (Bobby Bartlett, HiringThing). IBM puts the maintenance share of total software lifecycle costs at 50 to 75%. The Standish Group's 2024 CHAOS data, via FullScale, found 35% of large custom software projects are abandoned, and only 29% are delivered on time and on budget.

These numbers are accurate, and we made the decision knowing them. This section is not a wave-off.

The mitigation we are using: internal tooling is held to the same documentation standards as client projects. All ATS development goes through pair programming and code review. Handoff requirements are explicit — if a team member rolls off, knowledge transfer is a defined process, not an informal conversation. The scope of the build is deliberately narrow. This is not a platform; it is a tool that addresses specific problems in our hiring process. Narrow scope means lower ongoing maintenance surface.

Now the reframe, which matters more than the mitigation.

SaaS tools have maintenance costs too. They are just invisible.

Every workaround script is maintenance. Every manual data export is maintenance. Every custom integration bridging two tools that were not designed to talk to each other is maintenance. Every piece of institutional knowledge about how to interpret a metric that does not match your actual process — like the 23-day time-to-hire figure in Recruitee that was actually 31 days — is maintenance. It just lives in someone's head rather than a changelog. When that person leaves, it goes with them. It never appears on a budget line.

The honest question is not which option has maintenance costs. Both do. The question is which maintenance costs are visible and owned, and which are invisible and accumulating.

For Appunite specifically, the answer to "who maintains it?" is the same team that maintains the production systems we build for clients. Documentation standards, pair programming, handoff tests — this is not a novel operational challenge for us. It is the work we do every day.

That answer only works for a software company with the engineering discipline to follow through on it. If you are not a software company, Shah's concern — laid out in [our decision post](https://appunite.com/blog/hold-my-beer-building-custom-ats) — deserves more weight, not less. The maintenance risk profile is genuinely different when the people responsible for keeping the system running are not professional software engineers. The broader point: the maintenance question should be answered with your specific engineering capacity, not a blanket reassurance that applies to everyone.

---

The project is underway.

The next post covers the full pain point methodology — how we ran the workshops, how we applied the Jobs to Be Done framework, how we scored and clustered all 24 problems, and where the hardest judgment calls were. If you want to run a similar analysis on your own stack to figure out which SaaS to replace first, that post will give you the structure to do it.

After that: the actual architecture decisions, and eventually the real costs as they come in rather than as we estimated them. We said from the beginning this is a public experiment. The methodology post is where the process behind the framework we described here becomes reproducible.

The SaaS tax argument is in [the first post in this series](https://appunite.com/blog/the-saas-tax). The full financial case and go/no-go reasoning are in [our decision post](https://appunite.com/blog/hold-my-beer-building-custom-ats). This post was about the decision framework. After asking the four key questions, you can grab [a polished version of assessment framework here](www.appunite.com/is-saas-over-honest-evaluation). Next comes the work behind it.

---

**Sources:**

- Bobby Bartlett / HiringThing — The Cost of Building an Applicant Tracking System: https://blog.hiringthing.com/the-cost-of-building-an-applicant-tracking-system
- Standish Group CHAOS 2024, via FullScale: https://fullscale.io/blog/build-vs-buy-software-development-decision-guide/
- IBM software maintenance cost research (via SCNSoft): https://www.scnsoft.com/software-development/maintenance-and-support/costs
- Geoffrey Moore, *Dealing with Darwin* (2005)
- FullScale build vs buy decision guide (2025): https://fullscale.io/blog/build-vs-buy-software-development-decision-guide/
