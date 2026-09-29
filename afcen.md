# AfCEN, Africa Climate & Energy Nexus

**Sector** AI, Climate-Tech, impact investment  
**Role** AI Product Manager, QA & Testing  
**Client** Bayes Consulting

## The problem

African climate and energy infrastructure has capital looking for projects and projects looking for capital, and the two rarely find each other. Not because the money is unwilling, but because an investor cannot assess a project that has never been packaged into something assessable, and a developer with a viable idea cannot afford the six-figure feasibility work needed to package it.

AfCEN is an AI intelligence layer built to close that gap: a multi-agent system spanning project prioritisation, developer support and investor matching.

## Constraints

- Outputs that feed real investment decisions, where a confidently wrong number is worse than no number
- Agentic modules doing genuine analytical work, not retrieval dressed up as analysis
- Two user groups, developers and investors, who need the same underlying analysis presented completely differently

## What I owned

Product management across the multi-agent system, plus QA and testing. The two flagship agentic modules were the Interconnector Agent, which proposes technically viable power-grid routing optimised for co-location with existing rail and highway corridors and sizes capacity around anchor loads such as mines, ports and special economic zones, and the Corridor Development Agent, which quantifies economic impact for proposed corridors, identifies bankable project nodes and re-runs its analysis as financing or milestones change.

Alongside those, the Project Developer module turns a plain-language project idea into an investment-ready dataroom, and the Investor module delivers curated, mandate-aligned pipelines.

## The hard part: specifying an agent that has to be right

A chat assistant that is wrong wastes a minute. A routing proposal that is wrong, and that a developer takes to an investor, wastes a great deal more than that and damages the credibility of the platform permanently.

So the specification work was less about what the agents produce and more about what they must show alongside it. An agent output that cannot be traced back to its inputs and assumptions is not usable in an investment context, no matter how good it sounds. The same discipline I applied to a citation pipeline on a research platform applies here at much higher stakes: the user has to be able to check the work, and the product has to make checking easy rather than possible in principle.

The re-running behaviour of the Corridor Development Agent is the other half of that. An analysis that was true when financing was at one stage and is quietly still displayed after the stage changed is a wrong answer with a timestamp on it.

## Testing analytical output

QA on a product like this does not look like QA on a transactional system. There is no single correct answer to compare against.

What you can test is consistency, traceability and behaviour at the edges: does the same input produce the same output, does every figure resolve to a source or a stated assumption, and does the agent degrade honestly when the data underneath it is thin rather than producing a confident number from nothing.

## What I took from it

This is the clearest example I have of where AI genuinely earns its place. The analytical work AfCEN automates is work that, done by hand, costs more than most of these projects can raise, which means without it the analysis simply does not happen. That is a very different proposition from automating something a person was already doing adequately.
