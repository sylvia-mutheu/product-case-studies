# Mediwrite

**Sector** InsurTech  
**Role** Technical Product & Project Manager

## The problem

Insurers underwriting by hand, or by spreadsheet, which is by hand with extra steps. The product was a cloud underwriting engine automating risk profiling, policy management and quote generation across insurer partners.

## Constraints

- Multiple insurer partners, each with their own underwriting rules, none of whom considered their rules negotiable
- A regulated domain where the audit trail is not a feature, it is the point
- A rollout across partners rather than a single launch, so the product had to be explainable to people who had not been in the room

## What I owned

The product requirements covering risk profiling, policy management and quote generation, the product documentation, and support through rollout across insurer partners.

## What the domain taught me

I went in expecting the hard part to be the rules engine. It was not.

The hard part was that a regulated money product is mostly licensing, audit trail and evidence, and only then features. Every automated decision has to be reconstructable after the fact: what data was used, which rule fired, who could have overridden it, and when. A rule engine that produces the right answer but cannot show its work is not usable in this market, no matter how good the answer is.

That reframed the requirements. Auditability stopped being a non-functional requirement at the bottom of the document and became a constraint on how every feature was designed.

## The documentation point

Rollout across partners is where documentation stops being overhead. Each new insurer arrived without the context of the build, and the product documentation was the only thing standing between them and a discovery call that repeated the previous six. Writing it properly the first time was the highest-leverage work on the project.
