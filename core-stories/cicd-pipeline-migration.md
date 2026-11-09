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

- What specifically was hard to follow in the prior pipeline?
  - Cross region replication of images using a ecr evets, sns topic, and an argo events watcher
  - promotion to next environment was a clunky argo workflow
  - no easy visibility to what digest is in prod
- What changed in visibility—for example, deployment status, logs, approvals, or promotion stages?
  - which commit/digest was in each env for every service
  - clear promotion validation in a ui
- What was the migration plan, and how did you reduce risk or avoid downtime?
  - created a eks cluster that would function as the build env workhorse. i would build images, and provide the compute for kargo and argo dashboards.
- What measurable outcome or developer feedback confirmed the improvement?
  - complete adoption for all the development teams

## Likely follow-ups

- How did you validate that this was the right problem to solve? Interviewing developers on their currect struggles, understanding the current system. recreating the baseline eks infra at home and making my own cicd process for personal project, then implementing that system at work.
- Why did you choose that technology instead of improving the existing pipeline? Tech lead gave me several options, I trial them myself and ended up with Kargo.
- What tradeoffs did you make in the design? Since we were migrating from a complex cicd pipeline in an env with no visibility. I decided to implement an improved eks cluster with argocd first, before tackeling the migration. The tradeoff off was a delayed reward in exchange for greater visibility during the migration.
- What would you do differently if you repeated the migration? Instead, I would define a small first phase—for example, establishing the observable EKS and Argo CD foundation—explain its standalone value, and secure approval for that phase first. Each subsequent phase would build on the prior one, with a clear benefit, success criterion, and decision point. That would make prioritization easier, create earlier value, and let stakeholders gain confidence through visible progress while still moving toward the same final outcome.
