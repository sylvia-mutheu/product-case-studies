# Breach monitoring and alerting platform

**Sector** Cybersecurity, SaaS  
**Role** Technical Project Manager  
**Client** Under NDA. Anonymised throughout.

## The problem

Real-time dark web breach alerting, serving two audiences at once: small and medium businesses, and law enforcement agencies. Those two want different things from the same data, and the product had to serve both without becoming two products.

An SME wants to know whether they are exposed and what to do about it this morning. A law enforcement agency wants to see the pattern, the source and the chain of evidence.

## Constraints

- Third party threat intelligence sources I did not control, each with its own format, latency and reliability
- Real-time responsiveness as the core promise, measured against false positives as the core risk
- Two audiences with different tolerance for noise and different definitions of urgent

## What I owned

Requirements for the platform architecture, the dashboard design, and the alerting and notification logic that fires the moment a breach is detected. Coordination directly with the threat intelligence data sources.

## The trade-off the whole product turns on

Every alerting product has one number that decides whether it is useful: how aggressively it fires.

Too sensitive and the SME stops reading the alerts within a fortnight, at which point the product has failed even though it is technically working. Too conservative and you miss the breach the customer bought the product for, which is worse.

This cannot be resolved by choosing a better threshold, because the right threshold differs by audience. The answer was to separate detection from notification. Detection stays aggressive, so nothing is lost and the evidence trail is complete for the law enforcement view. Notification is tiered and tuned per audience, so the SME sees what is actionable now and can go looking for the rest.

That also meant the dashboard and the alert could not be the same surface. An alert has to be a single decision. A dashboard is for investigation.

## On working with external data sources

This is the part that does not appear on a roadmap. Every threat intelligence feed had its own schema, its own freshness guarantee and its own failure mode, and a product whose core promise is real-time cannot quietly degrade when one source goes stale.

So source health became a product requirement rather than an operational concern. If a feed is behind, the product has to know, and the confidence of what it is showing has to reflect that.

## What I took from it

In security products, a false positive is not a minor defect. It spends the user's attention, and attention is the resource the entire product depends on. I now treat alert fatigue as a first-class failure mode and specify it, rather than leaving it to be discovered after launch.
