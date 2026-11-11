# Tell Me About a Time You Improved the Customer Experience

**Leadership Principle:** Customer Obsession  
**Use:** [Making CI/CD Easier for Developers](../core-stories/cicd-pipeline-migration.md)

## Draft answer

> Developers told us that the existing CI/CD pipeline was difficult to follow and gave them limited visibility into how a commit or image moved toward production. That made troubleshooting and day-to-day delivery harder. I treated that feedback as a product requirement, not just a tooling complaint. I recreated a representative environment, built sample developer projects, and tested several approaches from the developer perspective. I chose Kargo after evaluating the options, designed a clearer promotion workflow, and planned a migration that first established an observable EKS and Argo CD foundation. The result was a successful production migration to a pipeline with clear promotion validation and visibility into which commit or digest was in every environment. Development teams fully adopted it, and it now supports deployments for hundreds of services.

## Skim notes

- Customer: developers; problem: confusing promotions and poor deployment visibility.
- Recreated their experience with a representative environment and sample projects.
- Evaluated options; chose Kargo.
- Built observable EKS/Argo CD foundation before migration.
- Result: clear promotion validation and commit/digest visibility per environment.
- Full developer adoption; supports hundreds of services.

## What to emphasize

- Developers were the customer; begin with what was difficult for them.
- Explain how you validated the experience yourself rather than assuming a platform-centric solution.
- Make the customer outcome, not the technology choice, the result.

## Details to confirm

- How you gathered the developer feedback and how many teams were involved.
- Migration sequencing, rollout safety, and whether there was downtime.
- One concrete example of a troubleshooting or promotion task that became easier.

## Likely follow-ups

- Why was Kargo the best fit over the alternatives?
- How did you know developers would adopt the new workflow?
- What tradeoff did you make to improve visibility during the migration?
