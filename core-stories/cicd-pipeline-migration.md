# Making CI/CD Easier for Developers

## Leadership Principles demonstrated

- [Customer Obsession](../leadership-principles/customer-obsession.md)
- [Ownership](../leadership-principles/ownership.md)
- [Invent and Simplify](../leadership-principles/invent-and-simplify.md)
- [Learn and Be Curious](../leadership-principles/learn-and-be-curious.md)
- [Dive Deep](../leadership-principles/dive-deep.md)
- [Deliver Results](../leadership-principles/deliver-results.md)

## STAR story

### Situation

Developers complained that the existing CI/CD pipeline was complex, difficult to follow, and provided limited visibility into the deployment process. This made it harder for them to understand how changes/commits/images moved toward production and to troubleshoot issues when something wrong

### Task

Improve the developer experience by designing and implementing a clearer CI/CD approach that made promotion easier to understand and gave developers better visibility, while planning a safe migration from the current pipeline.

### Action

I started by listening to the developers’ complaints and treating them as requirements for the new experience: the pipeline needed to be easier to follow and provide better visibility.

I learned a new CI/CD technology and recreated a representative work environment on my personal setup. To evaluate the experience from the developer’s perspective rather than only the platform perspective, I created sample developer projects and used them to learn the easiest path for promoting changes through the pipeline.

Based on what I learned, I designed the new implementation and a migration strategy. I then carried out the migration at work, moving the team to the improved CI/CD solution.

### Result

The new pipeline addressed the core developer feedback: it was easier to understand and offered improved visibility into how work progressed through the delivery process. The migration was successfully completed in the production work environment, and the pipeline was used for hundreds of services.

## Impact metrics

- **Adoption:** Used for deployments across **hundreds of services**.
- **Developer experience:** Replaced a difficult-to-follow promotion process with a clearer delivery workflow and better deployment visibility.

## Details to add before the interview

- Legacy ECR/SNS/Argo flow.
- Clunky Argo promotion.
- Missing production digest.
- Per-environment commit visibility.
- Promotion validation UI.
- EKS build foundation.
- Kargo/Argo dashboards.
- Full developer adoption.

## Likely follow-ups

- Developer interviews.
- Home environment replica.
- Trialed platform options.
- Chose Kargo.
- Visibility before migration.
- Approve phases separately.
