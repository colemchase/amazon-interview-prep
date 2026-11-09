# Customer Obsession

## Real example: Making CI/CD easier for developers

### Situation

Developers complained that the existing CI/CD pipeline was complex, difficult to follow, and provided limited visibility into the deployment process. This made it harder for them to understand how changes moved toward production and to troubleshoot issues when something went wrong.

### Task

Improve the developer experience by designing and implementing a clearer CI/CD approach that made promotion easier to understand and gave developers better visibility, while planning a safe migration from the current pipeline.

### Action

I started by listening to the developers’ complaints and treating them as requirements for the new experience: the pipeline needed to be easier to follow and provide better visibility.

I then learned a new CI/CD technology and recreated a representative work environment on my personal setup. To evaluate the experience from the developer’s perspective rather than only the platform perspective, I created sample developer projects and used them to learn the easiest path for promoting changes through the pipeline.

Based on what I learned, I designed the new implementation and a migration strategy. I then carried out the migration at work, moving the team to the improved CI/CD solution.

### Result

The new pipeline addressed the core developer feedback: it was easier to understand and offered improved visibility into how work progressed through the delivery process. The migration was successfully completed in the production work environment.

## How this demonstrates Customer Obsession

The customers in this story were the developers using the delivery platform. Rather than assuming the existing process was acceptable, I started with their experience, learned the workflow firsthand, and designed the solution around the friction they reported.

## Details to add before the interview

- What specifically was hard to follow in the prior pipeline?
- Which CI/CD technology did you learn and implement?
- How many developers, teams, repositories, or services were affected?
- What changed in visibility—for example, deployment status, logs, approvals, or promotion stages?
- What was the migration plan, and how did you reduce risk or avoid downtime?
- What measurable outcome or developer feedback confirmed the improvement?

## Likely follow-ups

- How did you validate that this was the right problem to solve?
- Why did you choose that technology instead of improving the existing pipeline?
- What tradeoffs did you make in the design?
- What would you do differently if you repeated the migration?
