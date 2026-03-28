# Hold My Beer — We're Building Our Own ATS (The Manifesto)

**Author:** Karol Wojtaszek
**Series:** The SaaS Tax — Part 2

---

**TL;DR:** Appunite is an Elixir software company that spent 12 years building custom systems for clients. We decided to test the build-vs-buy debate on ourselves by building a custom ATS to replace Recruitee. Budget: 86,000 PLN. We found 24 documented problems costing an estimated 150,648 PLN per year — but 85% of that is opportunity cost, and the direct savings alone produce a negative ROI. We are doing it anyway, and we are documenting everything publicly.

---

## The setup

We are an Elixir company. We have been building custom software for clients for 12 years. Our recruitment process — the thing that determines who joins this team, who shapes the products, who talks to our clients — runs on a tool designed for the average mid-market HR department.

That always bothered me.

Not because the tool is bad. Recruitee was built to give SMBs an overview of the hiring process, and it does that well. But we are not the average case. We hire from one of the smallest senior talent pools in European tech. Our interview process has technical depth that a general-purpose ATS was never designed to support. We pay for 100% of a product and use maybe 20% of it — while the specific 20% we actually need does not exist.

If you read [the first post in this series](https://appunite.com/blog/the-saas-tax), you know where this argument leads. The SaaS tax is real: you subsidize features built for someone else's workflow, and you cannot redirect that investment toward what you are missing. For commodity workflows — expense tracking, office management — that trade-off is fine. For a process that directly determines the quality of your engineering team, it is not.

So we stopped arguing about it.

## Why now

I have been watching the "SaaS is dead" debate for over a year. The camps are well-established.

Camp one: the maximalists. AI can build anything, SaaS is a relic, every company should own its stack. Vibe-code your way to freedom. Camp two: the skeptics. Dharmesh Shah, HubSpot's co-founder and CTO, asked the question everyone is thinking: "Who's going to maintain it?" I have an answer for him — but first, the data.

And then there is the Klarna saga — which went from "AI replaces 700 agents and saves $40 million" to the CEO saying he was "tremendously embarrassed" by the Salesforce fallout, to quietly re-hiring human agents. It is the debate everyone has been following. It is also a lesson in how fast the narrative can get ahead of the reality.

I got tired of watching these arguments go in circles. Opinions are cheap. Data is expensive. So we decided to generate some.

We are putting money on the table to find out whether a software company can build a better internal tool than the one it buys off the shelf. This is not a weekend hackathon and it is not a vibe-coded prototype. If it works, we have proof. If it fails, that is equally valuable data. Either way, we are documenting everything.

AI has meaningfully shifted the economics of building software. I am not going to claim "10x cheaper" — nobody honest can. But the math on replacing SaaS with custom software has changed enough that experiments like this one are worth running. We happen to be in the business of building software, so the experiment starts at home.

## Why the ATS

Out of every tool we use internally, the ATS was the obvious target for a build vs buy decision. Four reasons.

**Process specificity.** Recruitment at a software company is a core competitive process, not a commodity workflow. How you evaluate engineers, how you run technical interviews, how you source from a small Elixir talent pool — a generic tool cannot optimize for any of this. Unlike expense tracking, where the off-the-shelf solution is fine, recruitment is where your specific process is the competitive advantage. Building a custom ATS makes sense when the hiring process itself is what sets you apart.

**Measurable pain.** We did not have to guess that something was wrong. We ran structured workshops with our recruitment team and found 24 documented problems grouped into 7 clusters. I will get to the specifics shortly — but the point is, we had signal before we had opinions.

**Candidate relationships.** For a company that depends on attracting senior Elixir engineers from a small talent pool, the relationship with candidates over time matters more than it does for a company hiring generalists at volume. Owning that data and that workflow is a strategic decision. A 2020 ATS buyer's guide found nearly half of companies were dissatisfied with their current ATS — and the most common complaint was inflexibility. That matches our experience.

**Data ownership.** When you own the system, you own the data — and you can do things with it that a SaaS vendor's API never intended. Custom analytics. AI-powered candidate matching. Longitudinal tracking of how your hiring criteria correlate with actual performance. None of that is available when your data lives behind someone else's rate limits.

Recruitee is a good product for its target market. It was designed for general SMBs with 50 to 500 employees and moderate hiring volumes. We are not that market. We need something built for how we actually work — and the build vs buy ATS question, for us, had a clear answer once we looked at the numbers.

## What we found

### How we looked

We did not start with a solution. We started with workshops.

The recruitment team sat down and mapped every friction point in the current process — from job posting to offer letter. We used an impact-times-frequency matrix to score each problem: how often does it happen, and how much damage does it cause when it does? We applied the Jobs to Be Done framework to understand what people actually needed at each step, not what the current tool happened to provide.

The result: 24 distinct problems, organized into 7 clusters, each with a cost estimate. We will publish the full methodology breakdown in an upcoming post — the scoring criteria, the workshop structure, and how we handled disagreements. For now, here is what we found.

### The problems worth naming

Twenty-four problems is a lot to list. The complete pain point analysis is coming in a separate post, with every cluster broken down. Here are the four that hit hardest — the ones I think most engineering-led companies will recognize in their own processes.

**Reports that lie to you.** Our ATS told us our time-to-hire was 23 days. The real number was 31. When your reporting data is wrong, every decision built on it is wrong too. We caught this discrepancy multiple times. It was not a one-off glitch — the calculation logic itself did not match our actual process. If you are making headcount decisions based on ATS-generated metrics, you should probably audit those numbers.

**No interview transcription, manual feedback.** Every interviewer writes up their notes from memory, hours after the conversation. Half the signal is lost. There is no searchable record, no way to compare candidate responses side by side, no audit trail for hiring decisions. Each feedback cycle takes longer than the interview itself.

**No competency matrices, generic sourcing.** We cannot track how candidates compare against the specific technical competencies we care about. Our sourcing ends up generic when it should be surgical. For a niche talent pool like senior Elixir engineers, this is not an inconvenience — it is a structural disadvantage in a build vs buy ATS context where the "buy" option was never designed for this level of specificity.

**Calendar and scheduling gaps.** The mundane friction that adds up. Every manual scheduling round-trip is 15 minutes nobody gets back. Multiply that across every candidate, every interview loop, every reschedule. It sounds trivial until you total the hours.

## The math

Here is where I owe you honesty instead of enthusiasm.

The 24 problems we identified cost us an estimated 150,648 PLN per year. That is the headline number. Now let me immediately complicate it.

85% of that figure is opportunity cost. The direct, measurable time savings — the hours our team actually burns on manual work that a custom tool would eliminate — amount to 22,524 PLN per year. That is the number you can point to on a timesheet.

Here is the full breakdown. Every cluster, every cost type, nothing hidden.

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

### The honest interpretation

Let me start with the bad news.

Direct savings alone — 22,524 PLN per year — do not justify an 86,000 PLN build. The ROI on hard, measurable savings is roughly -74% in year one. By any straightforward financial measure, the direct cost case does not work.

The case only becomes positive if you believe a meaningful share of the opportunity costs are real. At the full 150,648 PLN annually against an 86,000 PLN build cost, the ROI is approximately +75%. That looks much better. But 85% of that number is opportunity cost — and the single largest contributor is Cluster 1 (reporting errors) at 101,520 PLN per year, almost entirely driven by one assumption: that bad reporting data leads to bad hiring decisions, which leads to failed hires.

Is that assumption reasonable? I think so. Can I prove the exact causal chain in a spreadsheet? No.

If the opportunity costs turn out to be less than 50% real, the ROI is negative in year one. The entire financial case lives or dies on Cluster 1. If inaccurate reporting genuinely causes worse hiring outcomes, the opportunity cost is enormous. If we are overstating that connection, we are building a custom ATS that will not pay for itself through cost savings alone.

We have a framework for mitigating this uncertainty, [which we outlined here](www.appunite.com/is-saas-over-honest-evaluation).

### What the numbers do tell us

Even the conservative case — direct savings only — reaches break-even in about four years. Not exciting, but not catastrophic.

If even a fraction of the opportunity costs are real — say 30 to 40 percent — the payback period shrinks to roughly two years.

And then there is a category of value the spreadsheet cannot capture at all: capabilities that are impossible to build on top of Recruitee at any price. Custom AI-powered candidate matching tailored to our technical stack. Longitudinal hiring analytics tied to actual engineer performance after they join. Tight integration with our technical assessment process. These do not appear in a cost table, but they are a real part of the decision.

### The go/no-go

I am not going to sugarcoat the risk. The data on custom software builds is sobering.

Only about 1.7% of companies under 100 employees build their own ATS. The vast majority buy off the shelf. Of custom software projects broadly, 53% end up costing 189% more than initially estimated. And 70% of total software costs come after implementation — in maintenance, updates, and the slow accumulation of complexity.

Bobby Bartlett, who has spent years in the ATS market at TargetRecruit, put it directly: "I have seen top 10 companies in the US and UK with deep pockets sink years into a custom build on Salesforce, only to abandon the effort and opt for a pre-built solution."

I take that seriously. This is not a project where naivety is a defensible position.

But the spreadsheet is not the only input. Three things tip the balance.

First: learning value. We are a software company that advises clients on build-vs-buy decisions every week. Running this experiment on ourselves — with our own money, on a real process — produces knowledge we cannot get any other way. Whether the build succeeds or fails, the data is worth having.

Second: content and awareness value. You are reading this right now. Documenting the journey publicly — the honest numbers, the methodology, the mistakes when they happen — creates something the build-vs-buy debate badly needs. Actual data from an actual company.

Third: proof of concept for a strategic thesis. We believe the economics of replacing SaaS with custom software have shifted for companies with in-house engineering teams. If we can demonstrate that on a contained, well-scoped project like building a custom ATS, the implications for our clients — and our business — are significant.

We are proceeding, with exact scoping workshops underway. This will let us pinpoint the budget we need to build an ATS that matches our process.

## The counterargument — and our answer

Dharmesh Shah, HubSpot's co-founder and CTO, posted the sharpest critique of the "replace SaaS" movement last year. His rhetorical challenge was specific:

> "Who's going to maintain it? Who's going to keep up with industry trends? What are you going to do when the 20-something genius that vibe coded it over a weekend leaves the company?"

Fair questions. And for most companies, the honest answer is: nobody, nobody, and panic. That is exactly Shah's point, and he is right — for most companies.

But Shah explicitly frames this as advice for non-software companies. He says even Fortune 500 companies might pull it off only "for some discrete use cases." His warning targets a specific scenario: companies that confuse a prototype with a product.

We are a software company. Building production-grade systems and maintaining them for years is our entire business. We are not vibe-coding a replacement over a weekend. We are scoping it with the same discipline we bring to client projects — professional engineers, proper architecture, a team that will be here in five years.

Who is going to maintain it? The same people who maintain the systems we build for clients. Who keeps up with industry trends? The same people who do it professionally, every working day. What happens when someone leaves? The same thing that happens on any well-run engineering team — documentation, code review, knowledge transfer, and structured handoffs. That is what a software development company does.

Shah's argument is actually the strongest case for working with a professional development partner rather than going it alone. If you are not a software company, he is right — you probably should not build your own tools. But that does not mean custom software is the wrong answer. It means you need a partner who builds software for a living, not a prompt and a long weekend.

And another critical caveat is: don't build replacements for processes that are not business-critical, that don't contribute to revenue. The effort will not pay off.

## What comes next

This post is the manifesto. What follows is the work.

We will publish the full methodology breakdown — every workshop, every scoring matrix, every judgment call — in an upcoming post. After that, the complete pain point analysis: all 24 problems across all 7 clusters, and how we costed each one. Then the build itself. The architecture decisions. The costs as they come in, not as we estimated them. The mistakes, when they happen.

We are sharing this publicly because the build-vs-buy debate has too many opinions and not enough data. We are contributing data.

If we succeed, this becomes a real case study for every CTO weighing the same decision — whether it is an ATS or any other internal tool where the SaaS tax has gotten too high. If we fail, at least you will know exactly why and what it cost. Either outcome is more useful than another opinion piece.

Follow along. [Via newsletter, where we'll share more details](www.appunite.com/is-saas-over-honest-evaluation), or via our blog.

---

**Sources:**

- Dharmesh Shah, LinkedIn, June 2025: [Why should companies pay for SaaS when they could just vibe code them?](https://www.linkedin.com/posts/dharmesh_why-should-companies-pay-for-saas-hrcrm-activity-7401711547091144704-EyJt)
- Klarna press release, February 2024: [Klarna AI assistant handles two-thirds of customer service chats](https://www.klarna.com/international/press/klarna-ai-assistant-handles-two-thirds-of-customer-service-chats-in-its-first-month/)
- Sebastian Siemiatkowski, X, March 2025: [Clarification on Salesforce/SaaS shutdowns](https://x.com/klarnaseb/status/1896698293759230429)
- Bobby Bartlett / TargetRecruit, via HiringThing: [The Cost of Building an Applicant Tracking System](https://blog.hiringthing.com/the-cost-of-building-an-applicant-tracking-system)
- RecruitmentTech: [Building versus buying an ATS](https://www.recruitmenttech.com/building-versus-buying-an-applicant-tracking-system-ats/)
- Select Software Reviews: [Applicant Tracking System Statistics 2026](https://www.selectsoftwarereviews.com/blog/applicant-tracking-system-statistics)
