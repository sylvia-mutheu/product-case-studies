# iMe Work, AI for corporate wellbeing

**Sector** AI, HealthTech, HR-Tech  
**Role** AI Product Manager

## The problem

A corporate wellbeing platform pairing an AI coach with personalised recommendations drawn from a person's calendar and connected health apps, plus an employer-facing view of burnout risk.

The structural problem is in that last sentence. The employee is the user. The employer is the buyer. What serves one can harm the other, and a wellbeing product that employees do not trust is worse than no product, because it collects data and delivers nothing.

## Constraints

- GDPR, with genuinely sensitive data: calendar contents, health app readings, engagement patterns
- Two parties with opposed interests reading the same underlying data
- An AI coach that has to be motivating without being manipulative, and has to know when to stop

## What I owned

The complete product requirements, written from the ground up: 78 user stories and the full functional and non-functional requirement set. The AI coach with five distinct motivational personas, the personalisation drawing on calendar availability and connected health apps, the gamification and points system, and the employer-facing burnout risk indicators.

## The decision that shaped the product

The employer never sees an individual.

Burnout risk surfaces to the employer as aggregate and threshold-based signal, never as a named person's data. This was not a compliance checkbox that arrived late. It was a constraint written into the requirements before the feature was designed, because it determines what the feature can be.

The reasoning is straightforward. The moment an employee suspects their manager can see their individual wellbeing data, the honest inputs stop. They stop logging, or they log what looks good. The data becomes worthless and the product becomes a surveillance tool that does not even work as one.

Protecting the individual view is what makes the aggregate view worth anything. That is a product argument before it is a privacy argument, which is why it survived the prioritisation conversations.

## Five personas, and why the number is not arbitrary

The AI coach ranges from a tough-love style to a gentler holistic one. People respond to encouragement very differently, and a single coaching voice will actively put off a large share of any workforce.

The non-negotiable was that the persona changes the tone and never the safety behaviour. A coach that pushes harder is still a coach that recognises when someone is struggling and stops pushing. That had to be specified explicitly, because it is exactly the requirement that gets lost between a specification and an implementation.

## What I took from it

When a product has a user and a separate buyer, the requirements document is where you decide which one you are actually building for. Leave it implicit and the buyer wins every prioritisation call, and the product slowly stops working.
