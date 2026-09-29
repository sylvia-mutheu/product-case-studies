# EdgeCards

**Sector** FinTech  
**Role** Technical Product Manager  
**Live** https://edge.cards/

## The problem

A consumer fintech app in Kenya moving money between a bank, a mobile money network and a card rail. Users expected the three to behave like one thing. They do not. Each has its own latency, its own failure modes, its own idea of when a transaction is final.

## Constraints

- Integrations with KCB Bank and M-Pesa, neither of which I controlled and both of which could change behaviour without warning
- Card issuance governed by the issuer's rules, which set the shape of the product regardless of what the roadmap said
- A user base for whom a stuck transfer is not an inconvenience, it is rent money

## What I owned

Wallet top-ups, card issuance, peer transfers and transaction security, end to end. That meant the product requirements, the API request and response contracts written and validated in Postman and Swagger, the integration scoping with the partner rails, and QA before release.

## The part that mattered, which was not the happy path

Most of my time went on failure handling rather than features.

The questions that took the longest to answer were these. What does the product do when a partner rail times out mid-transfer and we do not know whether the money moved? Which failures deserve an automatic retry, and which ones does a retry make actively worse by risking a double debit? How does reconciliation catch a state the user never sees, and what does the user get told in the meantime?

The answer that held up was to stop treating timeouts as errors and start treating them as an unknown state with its own lifecycle. A transfer in an unknown state is not failed and not complete. It has its own handling, its own reconciliation path, and its own honest message to the user, which is that we do not know yet and we will tell them when we do.

## What I learned

Card issuance taught me that a large share of payments product work is partner dependency management wearing a product hat. The issuer's constraints arrive as product decisions whether or not anyone invited them onto the roadmap. Scoping that properly at the start is worth more than any amount of prioritisation later.
