# AphiaOne, Medbook Kenya

**Sector** HealthTech  
**Role** Product Manager, QA & Testing

## The problem

A Hospital Management Information System running across multiple facilities in Kenya, covering patient workflows, billing, inventory and lab modules. The system worked. The problem was that what the software assumed about a hospital and what actually happens in a hospital were not the same thing.

## Constraints

- Live facilities. There is no maintenance window in a hospital
- Users who are clinicians first and software users a distant second, under time pressure, with patients waiting
- Four modules that touch each other constantly. A change to billing surfaces in inventory
- Adoption as the real measure. A correctly built feature nobody uses has failed

## What I owned

Improvements across the four modules, the QA process for every release, and user training with both the engineering team and hospital staff.

## The part that mattered

The requirements did not come from a stakeholder meeting. They came from sitting with clinical teams and watching what they actually did, which was frequently not what the documented workflow said.

The gap between the two is where the defects live. A nurse who has developed a workaround is telling you something about the product, and the workaround is the requirement. Writing down the documented process instead produces software that is correct and unused.

## Why QA and training sat with the same person

I ran structured test cycles before every rollout and then trained the people who would use it. That pairing was not an accident of resourcing.

Running the test cycle myself meant I knew exactly which paths were fragile, and training meant I heard the confusion first-hand rather than through a support ticket two weeks later. Each fed the other. The questions people asked in training became test cases in the next cycle.

## What I took from it

In clinical software the cost of a defect is not a bad review. Testing before rollout rather than after is not diligence, it is the minimum. This is where my habit of running QA personally before any client delivery comes from, and I have kept it on every product since, in domains with far lower stakes.
