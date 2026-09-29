# SoccerNet 3.0

**Sector** SaaS, Sports Tech  
**Role** Technical Product Manager

## The problem

A club management system built for one club, being asked to serve many. The commercial ambition was a subscription SaaS product. The technical reality was a single tenant application with one club's assumptions baked into it.

## Constraints

- An existing production system with real users who could not be disrupted by the migration
- Clubs that expected their own branding and their own domain, not a shared one
- A tiered subscription model that had to be a product capability rather than a manual arrangement negotiated per club

## What I owned

Product delivery on the migration: per-club environments, custom domains, the subscription tiers and the billing behind them.

## The hard question

The migration itself was not the hard part. The hard part was drawing a line that had never needed to exist.

Where does the platform end and tenant configuration begin? Every feature had to be sorted into one of three buckets: the same for everyone, configurable per club, or genuinely bespoke and therefore not part of the product at all. Getting that boundary wrong in either direction is expensive. Draw it too far toward configuration and every club becomes a support burden. Draw it too far toward the platform and you cannot sell to the second club.

## The part that went wrong

We scoped the boundary once and it turned out to be in the wrong place. Things we had assumed were universal were not, and things we had built as configurable, nobody ever configured.

What fixed it was not another round of meetings. It was writing the boundary down as an explicit document that named what the platform owned, what the tenant configured, and what we would decline, and then getting agreement on that document before more code was written. The specification did the arguing so the standups did not have to.

## Outcome

Clubs onboarded onto their own environments without a developer touching each one, and the subscription tier became a product decision rather than a conversation.
